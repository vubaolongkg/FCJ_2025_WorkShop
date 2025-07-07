---
title: "Create Glue Crawler"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 3.2 </b> "
---

## 3.2 Create Glue Crawler

1. Go to **Crawlers** → click **Add crawler**
2. Provide:
   - Name: `salesdatacrawler`
   - Data source: `s3://my-data-pipeline-bucket/raw/`
   - IAM Role: choose the created role
3. Output:
   - Database: `sales_db`
   - Table: `sales_raw`

> The crawler auto-detects the schema from the CSV file.
