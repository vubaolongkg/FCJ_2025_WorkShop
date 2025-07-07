---
title: "Create New Glue Job"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 4.1 </b> "
---

## 4.1 Create New Glue Job

1. Open AWS Glue → go to **Jobs** → **Add Job**
2. Job name: `ProcessJob`
3. IAM Role: select the one created earlier
4. Type: Spark, Python
5. Script: Process data from `sales_raw` and write output to `s3://bucket/processed/`
