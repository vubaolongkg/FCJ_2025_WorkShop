---
title: "Tạo Glue Crawler"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 3.2 </b> "
---

## 3.2 Tạo Glue Crawler
1. Vào **Crawlers** → chọn **Add crawler**
2. Nhập:
   - Tên: `salesdatacrawler`
  ![Glue](../../images/03/032/1.png?featherlight=false&width=90pc)
   - Data source: `s3://sales-data-bucket-2025/raw/`
  ![Glue](../../images/03/032/2.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/3.png?featherlight=false&width=90pc)
   - IAM Role: chọn role đã tạo
  ![Glue](../../images/03/032/4.png?featherlight=false&width=90pc)
3. Output:
   - Database: `sales_analysis_db`
   - Bảng: `sales_data_raw`
  ![Glue](../../images/03/032/5.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/6.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/7.png?featherlight=false&width=90pc)
  ![Glue](../../images/03/032/8.png?featherlight=false&width=90pc) 
> Crawler giúp tự động phát hiện schema từ file CSV.
