---
title: "Create New Crawler"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 5.1 </b> "
---

## 5.1 Create New Crawler

1. Go to AWS Glue → **Crawlers** → **Add crawler**
2. Fill in:
   - Name: `salesdatacrawler_processed`
![Glue](../../images/05/051/1.png?featherlight=false&width=90pc)
   - Data source: `s3://my-data-pipeline-bucket/processed/`
![Glue](../../images/05/051/2.png?featherlight=false&width=90pc)
![Glue](../../images/05/051/3.png?featherlight=false&width=90pc)
   - IAM Role: reuse the existing Glue role
![Glue](../../images/05/051/4.png?featherlight=false&width=90pc)
1. Output:
   - Database: `sales_analysis_db`
   - New table: `sales_data_processed`
![Glue](../../images/05/051/5.png?featherlight=false&width=90pc)
![Glue](../../images/05/051/6.png?featherlight=false&width=90pc)