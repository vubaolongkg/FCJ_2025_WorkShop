---
title: "Project Proposal - AWS Data Pipeline"
date: 2025-07-30
weight: 1
---

# 💼 Đề xuất dự án (Project Proposal)  
## **Tự động hóa Pipeline xử lý dữ liệu với AWS Glue, Lambda và QuickSight**

---

## 📄 Executive Summary

Trong thời đại dữ liệu bùng nổ, các tổ chức cần xây dựng hệ thống xử lý dữ liệu tự động, linh hoạt và có khả năng mở rộng. Dự án này đề xuất triển khai một hệ thống **ETL pipeline serverless** sử dụng các dịch vụ của AWS như **S3, Lambda, Glue, Athena và QuickSight** để xử lý và trực quan hóa dữ liệu bán hàng theo thời gian thực.

Các tệp CSV sẽ được tải lên Amazon S3, tự động kích hoạt chuỗi hành động từ việc crawl schema, làm sạch dữ liệu, ghi sang vùng đã xử lý, đến trực quan hóa trên QuickSight. Dự án còn tích hợp CloudTrail để theo dõi hành vi và EventBridge để quản lý các luồng xử lý nối tiếp.

**Lợi ích chính**:
- Tự động hóa hoàn toàn quy trình xử lý dữ liệu
- Giảm thiểu thao tác thủ công, tăng tính nhất quán
- Trực quan hóa dữ liệu linh hoạt qua QuickSight
- Kiến trúc không máy chủ giúp tiết kiệm chi phí và dễ mở rộng

---

## 🎯 Problem Statement

### Tình trạng hiện tại
Các doanh nghiệp thường lưu trữ dữ liệu bán hàng ở dạng CSV rải rác và xử lý thủ công, gây mất thời gian và thiếu đồng nhất.

### Vấn đề gặp phải
- Dữ liệu không được xử lý đúng định dạng/schema
- Quá trình tổng hợp, phân tích bị chậm trễ
- Khó khăn khi trực quan hóa theo thời gian thực

### Hệ quả
- Thiếu dữ liệu cho ra quyết định kịp thời
- Giảm năng suất làm việc của nhân sự
- Không phát hiện được bất thường trong dữ liệu

---

## 🏗️ Solution Architecture

### Kiến trúc tổng thể

```plaintext
[S3] --> [Lambda] --> [Glue Crawler Raw] --> [Glue Job] --> [Glue Crawler Processed] --> [Athena] --> [QuickSight]
```

S3: Nơi lưu dữ liệu raw và processed

Lambda: Xử lý chuỗi hành động ETL qua trigger & EventBridge

Glue Crawler: Tạo schema tự động

Glue Job: Làm sạch và chuẩn hóa dữ liệu

Athena: Truy vấn dữ liệu dạng SQL

QuickSight: Trực quan hóa và dashboard

Mô hình bảo mật
IAM roles giới hạn truy cập từng service

Sử dụng CloudTrail để theo dõi hành vi và ghi log

🔧 Technical Implementation
Các giai đoạn chính:
Tạo Bucket S3: raw/ và processed/

Tạo Glue Crawler: Phân tích schema raw và processed

Viết Glue Job ETL: làm sạch, định dạng, làm tròn số

Viết Lambda function: trigger từ S3, gọi Glue Crawler/Job

Thiết lập EventBridge: nối kết các bước xử lý

Truy vấn bằng Athena

Xây dựng Dashboard trên QuickSight

DevOps
Quản lý mã nguồn qua GitHub

Ghi log Lambda qua CloudWatch

Dùng versioning trong S3

📅 Timeline & Milestones
Giai đoạn	Thời gian	Kết quả
Khởi tạo môi trường	Tuần 1	S3, IAM, Glue config
Tự động hóa Pipeline	Tuần 2	Lambda + EventBridge
Làm sạch dữ liệu	Tuần 3	Glue Job thành công
Trực quan hóa	Tuần 4	Dashboard QuickSight
Tài liệu hóa	Tuần 5	Báo cáo + Slide

💰 Budget Estimation
Thành phần	Chi phí ước tính/tháng
S3 Storage	$0.10 (cho 1-5 GB dữ liệu)
AWS Glue (Crawler + Job)	~$5 (cho <1000 phút)
Lambda	$0.20 (dưới 1M request)
Athena	$1.00 (cho ~1TB scanned)
QuickSight (Standard User)	$9.00
Tổng	~$15–20/tháng

⚠️ Risk Assessment
Rủi ro	Giải pháp
Crawler nhận sai schema	Thêm schema manually
Lambda timeout	Tối ưu Glue Job runtime
Chi phí vượt kiểm soát	Giới hạn dung lượng file đầu vào
Dashboard không cập nhật	Tạo trigger định kỳ hoặc realtime

🎯 Expected Outcomes
Tự động xử lý dữ liệu tải lên → không cần thao tác tay

Truy vấn bằng Athena dễ dàng

Dashboard hiện thị các chỉ số như:

Doanh thu theo khu vực

Top sản phẩm bán chạy

Sản phẩm có lợi nhuận thấp

Dễ dàng mở rộng sang tích hợp AI/ML
