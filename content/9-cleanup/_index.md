---
title: "Clean Up Resources"
date: 2025-07-05
weight: 9
chapter: true
pre: " <b> 9. </b> "
---

## Clean Up Resources

After completing the pipeline, it's recommended to clean up your AWS resources to avoid unnecessary costs.

### 🧹 Delete resources by category:

#### AWS Glue
- Delete **Crawlers**: `salesdatacrawler`, `salesdatacrawler_processed`
- Delete **Job**: `ProcessJob`
- Delete **Database**: `sales_db`

#### AWS Lambda
- Delete Lambda function: `RunETLPipeline`

#### Amazon S3
- Delete the bucket: `my-data-pipeline-bucket` (or just delete `raw/`, `processed/` folders if keeping the bucket)

#### IAM
- Delete IAM roles if no longer needed:
  - `AWSGlueServiceRole`
  - `AWSLambdaExecutionRole`

#### CloudWatch
- Go to CloudWatch → Logs → Delete Lambda log groups

#### QuickSight
- In QuickSight:
  - Delete the dataset: `sales_processed`
  - Delete the dashboard (if created)
