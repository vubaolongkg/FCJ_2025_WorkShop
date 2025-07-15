---
title: "Workshop Pipeline AWS Xử lý Dữ liệu"
date: 2025-07-05
weight: 1
chapter: false
---

# 👋 Chào mừng đến với Workshop AWS - FCJ 2025
# Xây dựng hệ thống xử lý và trực quan hóa dữ liệu bán hàng tự động trên nền tảng AWS
#### Giới thiệu

Trong workshop thực hành này, bạn sẽ học cách xây dựng **pipeline xử lý dữ liệu không dùng máy chủ** (serverless) sử dụng các dịch vụ AWS, từ việc nhận dữ liệu CSV đầu vào cho đến hiển thị dữ liệu qua QuickSight. Ngoài ra bạn còn được tự động hóa quy trình với Lambda và bảo mật bằng IAM & CloudTrail.

#### Dịch vụ Sử dụng

- **Amazon S3** – Lưu trữ dữ liệu đầu vào và sau xử lý
- **AWS Glue Crawler** – Đọc và nhận diện cấu trúc CSV
- **AWS Glue Job** – Làm sạch và chuyển đổi dữ liệu
- **Amazon Athena** – Truy vấn dữ liệu đã xử lý
- **Amazon QuickSight** – Tạo dashboard trực quan
- **AWS Lambda** – Tự động hóa các bước xử lý
- **AWS CloudTrail** – Ghi lại hoạt động và giám sát

#### Quy trình tổng quát

![Pipeline Architecture](../images/00/0001.png?featherlight=false&width=90pc)

#### Mục tiêu Workshop

- Nắm được kiến trúc xử lý dữ liệu serverless với AWS
- Làm sạch, tính toán dữ liệu với Glue
- Truy vấn kết quả bằng Athena
- Hiển thị dữ liệu qua QuickSight
- Tự động hóa xử lý với Lambda
- Ghi nhận và kiểm tra qua CloudTrail

---

### Nội dung chính

1. [Giới thiệu Pipeline và Kiến trúc](1-introduction/)
2. [Chuẩn bị môi trường AWS](2-prepare-environment/)
3. [Crawler dữ liệu thô](3-crawler-raw/)
4. [Xử lý dữ liệu với Glue Job](4-glue-job/)
5. [Crawler dữ liệu đã xử lý](5-crawler-processed/)
6. [Truy vấn với Athena](6-athena-analysis/)
7. [Tự động hóa bằng Lambda](7-automation-lambda/)
8. [Dashboard với QuickSight](8-quicksight-dashboard/)
9. [Xoá và dọn dẹp tài nguyên](9-cleanup/)
