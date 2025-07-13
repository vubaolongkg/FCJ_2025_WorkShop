---
title: "Dọn dẹp tài nguyên"
date: 2025-07-05
weight: 9
chapter: true
pre: " <b> 9. </b> "
---


## Dọn dẹp tài nguyên

Sau khi hoàn tất pipeline, bạn nên dọn dẹp các tài nguyên AWS để tránh phát sinh chi phí không cần thiết.

### 🧹 Xoá tài nguyên theo danh mục:

#### AWS Glue
- Xoá **Crawler**: `salesdatacrawler`, `salesdatacrawler_processed`
![CleanUp](../../images/09/4.png?featherlight=false&width=90pc)
- Xoá **Job**: `ProcessJob`
![CleanUp](../../images/09/5.png?featherlight=false&width=90pc)
- Xoá **Database**: `sales_analysis_db`
![CleanUp](../../images/09/3.png?featherlight=false&width=90pc)
![CleanUp](../../images/09/6.png?featherlight=false&width=90pc)

#### AWS Lambda
- Xoá function: `gluecrawljob`
![CleanUp](../../images/09/7.png?featherlight=false&width=90pc)

#### Amazon S3
- Xoá bucket: `sales-data-bucket-2025` (hoặc chỉ xoá thư mục `raw/`, `processed/` nếu giữ bucket)
![CleanUp](../../images/09/9.png?featherlight=false&width=90pc)
![CleanUp](../../images/09/10.png?featherlight=false&width=90pc)

#### IAM
- Xoá các IAM Role nếu không tái sử dụng

#### CloudWatch
- Vào CloudWatch → Logs → Xoá log group của Lambda
![CleanUp](../../images/09/8.png?featherlight=false&width=90pc)

#### QuickSight
- Vào QuickSight:
  - Xoá dataset `sales_data_processed`
  - Xoá dashboard nếu đã tạo
![CleanUp](../../images/09/1.png?featherlight=false&width=90pc)
![CleanUp](../../images/09/2.png?featherlight=false&width=90pc)