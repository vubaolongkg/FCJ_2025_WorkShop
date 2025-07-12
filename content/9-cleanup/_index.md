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
- Delete **Crawler**: `salesdatacrawler`, `salesdatacrawler_processed`
![CleanUp](/images/09/4.png?featherlight=false&width=90pc)
- Delete **Job**: `ProcessJob`
![CleanUp](/images/09/5.png?featherlight=false&width=90pc)
- Delete **Database**: `sales_analysis_db`
![CleanUp](/images/09/3.png?featherlight=false&width=90pc)
![CleanUp](/images/09/6.png?featherlight=false&width=90pc)

#### AWS Lambda
- Delete function: `gluecrawljob`
![CleanUp](/images/09/7.png?featherlight=false&width=90pc)

#### Amazon S3
- Delete bucket: `sales-data-bucket-2025` (or just delete folder `raw/`, `processed/` if keeping bucket)
![CleanUp](/images/09/9.png?featherlight=false&width=90pc)
![CleanUp](/images/09/10.png?featherlight=false&width=90pc)

#### IAM
- Delete IAM Roles if not reused

#### CloudWatch
- Go to CloudWatch → Logs → Delete Lambda log group
![CleanUp](/images/09/8.png?featherlight=false&width=90pc)

#### QuickSight
- Go to QuickSight:

- Delete dataset `sales_data_processed`

- Delete dashboard if created
![CleanUp](/images/09/1.png?featherlight=false&width=90pc)
![CleanUp](/images/09/2.png?featherlight=false&width=90pc)