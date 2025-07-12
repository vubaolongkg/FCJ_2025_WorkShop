---
title: "Kết nối Athena với QuickSight"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 8.1 </b> "
---

## 8.1 Kết nối Athena với QuickSight
1. Thiết lập IAM Role.
- Từ trang chủ QuickSight, chọn Manage QuickSight, ở góc trên bên phải
![Quicksight](/images/08/081/1.png?featherlight=false&width=90pc)
- Chọn Security & Permission
![Quicksight](/images/08/081/2.png?featherlight=false&width=90pc)
- Chọn Manage
![Quicksight](/images/08/081/3.png?featherlight=false&width=90pc)
- Ta thấy tên role, vào phần Roles của IAM, tìm tên role đó
![Quicksight](/images/08/081/4.png?featherlight=false&width=90pc)
- Attach Policy cho role: `AmazonAthenaFullAccess`, `AmazonS3FullAccess`,`AWSGlueServiceRole`,`AWSQuicksightAthenaAccess`
![Quicksight](/images/08/081/5.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/6.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/7.png?featherlight=false&width=90pc)
2. Truy cập Amazon QuickSight → **Manage data**
3. Chọn **New dataset** → **Athena**
![Quicksight](/images/08/081/8.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/9.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/10.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/11.png?featherlight=false&width=90pc)
4. Đặt tên và chọn **Athena workgroup**
![Quicksight](/images/08/081/12.png?featherlight=false&width=90pc)
5. Chọn database `sales_analysis_db`, table `sales_data_processed`
6. Import dữ liệu hoặc dùng chế độ SPICE để tăng tốc
![Quicksight](/images/08/081/13.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/14.png?featherlight=false&width=90pc)
