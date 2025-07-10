---
title: "Tạo Glue Job mới"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 4.1 </b> "
---

## 4.1 Tạo Glue Job mới

1. Vào AWS Glue → chọn **Jobs** → **Add Job**
![Glue](/images/04/041/1.png?featherlight=false&width=90pc)
2. Tên Job: `ProcessJob`
3. IAM Role: chọn IAM đã tạo từ bước trước
4. Type: Spark
![Glue](/images/04/041/5.png?featherlight=false&width=90pc)
5. Vào phần Script, chọn **Edit Script**, Script path: Tạo script xử lý dữ liệu từ bảng `sales_data_raw` và ghi kết quả ra `s3://sales-data-bucket-2025/processed/`
![Glue](/images/04/041/2.png?featherlight=false&width=90pc)
![Glue](/images/04/041/3.png?featherlight=false&width=90pc)
![Glue](/images/04/041/4.png?featherlight=false&width=90pc)