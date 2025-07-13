---
title : "Tạo IAM Role"
date : 2025-07-05
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

## Tạo IAM Role

Để các dịch vụ AWS có thể hoạt động đúng, cần tạo IAM Role với quyền thích hợp:

Vào dịch vụ IAM, đi đến phần Role.
![Role](../../../images/02/021/1.png?featherlight=false&width=90pc)

### 🔹 Cho Lambda:
- `AWSGlueServiceRole`
- `AWSS3FullAccess`
- `CloudWatchLogsFullAccess`

Chọn Create Role, chọn Service là Lambda.
![Role](../../../images/02/021/2.png?featherlight=false&width=90pc)

Tìm kiếm và chọn các vai trò mà mình mong muốn.
![Role](../../../images/02/021/3.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/4.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/5.png?featherlight=false&width=90pc)

Đặt tên `LambdaRole`, kiểm tra lại và nhấn Create Role.
![Role](../../../images/02/021/6.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/7.png?featherlight=false&width=90pc)  

![Role](../../../images/02/021/8.png?featherlight=false&width=90pc)

### 🔹 Cho Glue:
- `AWSGlueServiceRole`
- `AmazonAthenaFullAccess`
- `AmazonQuicksightAthenaFullAccess`
- `AmazonS3FullAccess`
 
Tương tự chọn Create Role, sau đó chọn dịch vụ Glue.
![Role](../../../images/02/021/9.png?featherlight=false&width=90pc)

Tìm kiếm và chọn các vai trò mà mình mong muốn.
![Role](../../../images/02/021/10.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/11.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/12.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/13.png?featherlight=false&width=90pc)

Đặt tên `GlueRole`, kiểm tra lại và nhấn Create Role.
![Role](../../../images/02/021/14.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/15.png?featherlight=false&width=90pc)

![Role](../../../images/02/021/16.png?featherlight=false&width=90pc)

> Các quyền này cho phép Glue đọc/ghi dữ liệu từ S3 và Lambda có thể gọi Glue Job.



