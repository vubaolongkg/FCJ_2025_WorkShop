---
title: "Run Crawler and Verify Table"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 5.2 </b> "
---

## 5.2 Run Crawler and Verify Table

1. After creation, select `salesdatacrawler_processed` and click **Run Crawler**
![Glue](../../images/05/052/1.png?featherlight=false&width=90pc)
2. Go to Glue → `Databases` → `sales_analysis_db`
3. Check that the `sales_data_processed` table was created correctly with the expected schema
![Glue](../../images/05/052/2.png?featherlight=false&width=90pc)
> The schema should now be normalized and ready for analytics.
