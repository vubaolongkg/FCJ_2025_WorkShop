---
title : "Mục đích và Ứng dụng"
date : 2025-07-05
weight : 3
chapter : false
pre : " <b> 1.2 </b> "
---

**Nội dung:**
- [🌐 Tại sao dùng AWS cho Data Pipeline?](#-tại-sao-dùng-aws-cho-data-pipeline)
- [📌 Trường hợp sử dụng thực tế](#-trường-hợp-sử-dụng-thực-tế)
- [🚀 Khả năng mở rộng trong tương lai](#-khả-năng-mở-rộng-trong-tương-lai)

---

#### 🌐 Tại sao dùng AWS cho Data Pipeline?

AWS cung cấp các dịch vụ mạnh mẽ như **S3**, **Glue**, và **Athena**, giúp xây dựng hệ thống xử lý dữ liệu hiệu quả, không cần quản lý hạ tầng phức tạp, và hỗ trợ tự động hóa toàn diện.

> Với mô hình tính phí theo mức sử dụng, khả năng mở rộng toàn cầu và tích hợp dịch vụ linh hoạt, AWS là lựa chọn hàng đầu cho các bài toán kỹ thuật dữ liệu hiện đại.

---

#### 📌 Trường hợp sử dụng thực tế

- 🔍 **Làm sạch và chuyển đổi dữ liệu**: Tự động xử lý, chuẩn hóa file CSV, JSON hoặc log với Glue  
- 📊 **Phân tích kinh doanh**: Truy vấn trực tiếp dữ liệu trên S3 bằng SQL qua Athena  
- 🏢 **Chuẩn bị dữ liệu cho kho dữ liệu**: Chuyển dữ liệu về dạng có cấu trúc để đưa vào Redshift hoặc công cụ BI khác  
- 🔁 **Cập nhật dữ liệu định kỳ**: Chạy các job theo lịch để cập nhật dữ liệu báo cáo

---

#### 🚀 Khả năng mở rộng trong tương lai

- Dễ dàng tích hợp thêm các dịch vụ như:
  - **Amazon QuickSight** để trực quan hóa
  - **Amazon Redshift** làm kho dữ liệu
  - **AWS Lambda** để kích hoạt tự động theo sự kiện

- Hỗ trợ thêm nguồn dữ liệu và dung lượng lớn mà không cần thay đổi hệ thống hiện tại.

> Kiến trúc có tính mô-đun, linh hoạt và “cloud-native”, phù hợp cho mọi nhu cầu mở rộng về sau.
