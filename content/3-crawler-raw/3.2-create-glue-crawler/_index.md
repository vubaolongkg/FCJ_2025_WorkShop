---
title: "Create Glue Crawler"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 3.2 </b> "
---

## 3.2 Create Glue Crawler

1. Go to **Crawlers** → select **Add crawler**
2. Enter:
   - Name: `salesdatacrawler`
  ![Glue](../../images/03/032/1.png?featherlight=false&width=90pc)
   - Data source: `s3://sales-data-bucket-2025/raw/`
  ![Glue](../../images/03/032/2.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/3.png?featherlight=false&width=90pc)
   - IAM Role: select the created role
  ![Glue](../../images/03/032/4.png?featherlight=false&width=90pc)
3. Output:
   - Database: `sales_analysis_db`
   - Board: `sales_data_raw`
  ![Glue](../../images/03/032/5.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/6.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/7.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/8.png?featherlight=false&width=90pc) 
> The crawler auto-detects the schema from the CSV file.
