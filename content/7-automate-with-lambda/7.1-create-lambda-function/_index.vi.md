---
title: "Tạo Lambda Function"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 7.1 </b> "
---

## 7.1 Tạo Lambda Function

1. Truy cập **AWS Lambda** → Chọn **Create function**
2. Chọn Author from scratch:
   - Tên: `RunETLPipeline`
   - Runtime: Python 3.12
   - Role: chọn IAM Role đã tạo (có quyền Glue + CloudWatch + S3)
3. Trong phần function code, bạn sẽ viết mã để thực hiện:

- Start crawler cho `sales_raw`
- Chạy Glue Job `ProcessJob`
- Chạy crawler cho `sales_processed`
