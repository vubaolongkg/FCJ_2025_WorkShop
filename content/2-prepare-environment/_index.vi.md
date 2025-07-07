---
title : "Các bước chuẩn bị"
date : 2025-07-05
weight : 2
chapter : true
pre : " <b> 2. </b> "
---

## Tổng quan các bước chuẩn bị

Trước khi triển khai pipeline xử lý dữ liệu với Glue và S3, cần chuẩn bị các tài nguyên và quyền sau trên AWS:

### Nội dung:

- [2.1 Tạo IAM Role](./2.1-create-iam-role)
- [2.2 Tạo Bucket S3](./2.2-create-s3-bucket)
- [2.3 Upload dữ liệu mẫu](./2.3-upload-sample-data)

---

### 🔐 1. IAM Role

Tạo IAM Role cho Glue và Lambda để đảm bảo quyền truy cập dịch vụ và S3.

---

### 🪣 2. S3 Bucket

Tạo bucket chứa dữ liệu đầu vào và đầu ra, với 2 thư mục chính: `raw/` và `processed/`.

---

### 📂 3. Upload dữ liệu mẫu

Chuẩn bị tệp CSV đơn giản (ví dụ: `sales.csv`) và upload vào thư mục `raw/`.



