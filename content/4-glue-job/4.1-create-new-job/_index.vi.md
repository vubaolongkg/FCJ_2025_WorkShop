---
title: "Tạo Glue Job mới"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 4.1 </b> "
---

## 4.1 Tạo Glue Job mới

1. Vào AWS Glue → chọn **Jobs** → **Add Job**
2. Tên Job: `ProcessJob`
3. IAM Role: chọn IAM đã tạo từ bước trước
4. Type: Spark, Python
5. Script path: Tạo script xử lý dữ liệu từ bảng `sales_raw` và ghi kết quả ra `s3://bucket/processed/`
