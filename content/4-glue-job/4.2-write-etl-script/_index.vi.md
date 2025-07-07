---
title: "Viết script ETL"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 4.2 </b> "
---

## 4.2 Viết script ETL

Trong script Python (Spark):

- Đọc dữ liệu từ bảng `sales_raw`
- Đổi tên cột nếu cần (`order_id` → `id`, v.v.)
- Ép kiểu dữ liệu phù hợp (ví dụ: date, float)
- Ghi ra `s3://my-data-pipeline-bucket/processed/` dưới dạng Parquet hoặc CSV

```python
import sys
from pyspark.context import SparkContext
from awsglue.utils import getResolvedOptions
from awsglue.context import GlueContext
from awsglue.job import Job
from pyspark.sql.functions import col, trim, regexp_replace, round
from awsglue.dynamicframe import DynamicFrame

args = getResolvedOptions(sys.argv, ['JOB_NAME'])
sc = SparkContext()
glueContext = GlueContext(sc)
spark = glueContext.spark_session
job = Job(glueContext)
job.init(args['JOB_NAME'], args)

input_dyf = glueContext.create_dynamic_frame.from_catalog(
    database="sales_analysis_db",
    table_name="raw_sales_dataset"  
)

df = input_dyf.toDF()

for col_name in df.columns:
    if df.schema[col_name].dataType.simpleString() == 'string':
        df = df.withColumn(
            col_name,
            trim(
                regexp_replace(  
                    regexp_replace(col(col_name), '^"|"$', ''),
                    '\s+', ' '
                )
            )
        )

if 'price' in df.columns and 'quantity' in df.columns:
    df = df.withColumn("revenue", round(col("price") * col("quantity"), 2))

output_dyf = DynamicFrame.fromDF(df, glueContext, "output_dyf")

output_path = "s3://your-data-pipeline-bucket/processed/"

glueContext.write_dynamic_frame.from_options(
    frame=output_dyf,
    connection_type="s3",
    connection_options={
        "path": output_path,
        "partitionKeys": []
    },
    format="csv"
)

glueContext.write_dynamic_frame.from_options(
    frame=output_dyf,
    connection_type="s3",
    connection_options={"path": "s3://your-data-pipeline-bucket/processed/"},
    format="csv"
)

job.commit()
```

> Nên dùng định dạng Parquet để tối ưu chi phí & hiệu năng khi query bằng Athena.
