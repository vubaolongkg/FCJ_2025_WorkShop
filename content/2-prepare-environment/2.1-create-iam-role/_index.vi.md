---
title : "Tạo IAM Role"
date : 2025-07-05
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

## Tạo IAM Role

Để các dịch vụ AWS có thể hoạt động đúng, cần tạo IAM Role với quyền thích hợp:

### 🔹 Cho Glue:
- `AWSGlueServiceRole`
- `AmazonS3FullAccess`

### 🔹 Cho Lambda:
- `AWSLambdaBasicExecutionRole`
- `AWSGlueConsoleFullAccess`

> Các quyền này cho phép Glue đọc/ghi dữ liệu từ S3 và Lambda có thể gọi Glue Job.
