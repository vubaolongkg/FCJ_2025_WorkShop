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
   - Data source: `s3://my-data-pipeline-bucket/processed/`
   - IAM Role: sử dụng role Glue đã tạo trước đó
3. Output:
   - Database: `sales_db`
   - Tên bảng mới: `sales_processed`
