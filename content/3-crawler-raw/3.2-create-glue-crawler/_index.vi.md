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
   - Data source: `s3://my-data-pipeline-bucket/raw/`
   - IAM Role: chọn role đã tạo
3. Output:
   - Database: `sales_db`
   - Bảng: `sales_raw`

> Crawler giúp tự động phát hiện schema từ file CSV.
