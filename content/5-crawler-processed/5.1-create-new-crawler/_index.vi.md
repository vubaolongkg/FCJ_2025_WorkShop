---
title: "Tạo Crawler mới"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 5.1 </b> "
---

## 5.1 Tạo Crawler mới
1. Truy cập AWS Glue → **Crawlers** → **Add crawler**
2. Nhập:
   - Tên: `salesdatacrawler_processed`
![Glue](../../images/05/051/1.png?featherlight=false&width=90pc)
   - Data source: `s3://my-data-pipeline-bucket/processed/`
![Glue](../../images/05/051/2.png?featherlight=false&width=90pc)
![Glue](../../images/05/051/3.png?featherlight=false&width=90pc)
   - IAM Role: sử dụng role Glue đã tạo trước đó
![Glue](../../images/05/051/4.png?featherlight=false&width=90pc)
3. Output:
   - Database: `sales_analysis_db`
   - Tên bảng mới: `sales_data_processed`
![Glue](../../images/05/051/5.png?featherlight=false&width=90pc)
![Glue](../../images/05/051/6.png?featherlight=false&width=90pc)