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
   - Data source: `s3://my-data-pipeline-bucket/processed/`
   - IAM Role: reuse the existing Glue role
3. Output:
   - Database: `sales_db`
   - New table: `sales_processed`
