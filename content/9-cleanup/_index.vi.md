---
title: "Dọn dẹp tài nguyên"
date: 2025-07-05
weight: 9
chapter: true
pre: " <b> 9. </b> "
---

## Dọn dẹp tài nguyên

Sau khi hoàn tất pipeline, bạn nên dọn dẹp các tài nguyên AWS để tránh phát sinh chi phí không cần thiết.

### 🧹 Xoá tài nguyên theo danh mục:

#### AWS Glue
- Xoá **Crawler**: `salesdatacrawler`, `salesdatacrawler_processed`
- Xoá **Job**: `ProcessJob`
- Xoá **Database**: `sales_db`

#### AWS Lambda
- Xoá function: `RunETLPipeline`

#### Amazon S3
- Xoá bucket: `my-data-pipeline-bucket` (hoặc chỉ xoá thư mục `raw/`, `processed/` nếu giữ bucket)

#### IAM
- Xoá các IAM Role nếu không tái sử dụng:
  - `AWSGlueServiceRole`
  - `AWSLambdaExecutionRole`

#### CloudWatch
- Vào CloudWatch → Logs → Xoá log group của Lambda

#### QuickSight
- Vào QuickSight:
  - Xoá dataset `sales_processed`
  - Xoá dashboard nếu đã tạo
