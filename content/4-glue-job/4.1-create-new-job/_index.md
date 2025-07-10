---
title: "Create New Glue Job"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 4.1 </b> "
---

## 4.1 Create New Glue Job

1. Open AWS Glue → go to **Jobs** → **Add Job**
![Glue](/images/04/041/1.png?featherlight=false&width=90pc)
2. Job name: `ProcessJob`
3. IAM Role: select the one created earlier
4. Type: Spark
![Glue](/images/04/041/5.png?featherlight=false&width=90pc)
5. Script: Process data from `sales_data_raw` and write output to `s3://sales-data-bucket-2025/processed/`
![Glue](/images/04/041/2.png?featherlight=false&width=90pc)
![Glue](/images/04/041/3.png?featherlight=false&width=90pc)
![Glue](/images/04/041/4.png?featherlight=false&width=90pc)