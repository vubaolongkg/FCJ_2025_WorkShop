---
title : "Mục tiêu đề tài"
date : 2025-07-05
weight : 2
chapter : false
pre : " <b> 1.1 </b> "
---

**Nội dung | Content:**
- [🎯 Mục tiêu tổng quan](#-mục-tiêu-tổng-quan)
- [⚙️ Tự động hóa quy trình ETL](#️-tự-động-hóa-quy-trình-etl)
- [📊 Hỗ trợ truy vấn và trực quan hóa](#-hỗ-trợ-truy-vấn-và-trực-quan-hóa)

---

#### 🎯 Mục tiêu tổng quan  

1. Xây dựng pipeline xử lý dữ liệu sử dụng các dịch vụ AWS: **S3**, **Glue**, và **Athena**.  
2. Thiết kế kiến trúc linh hoạt, có khả năng mở rộng, dễ dàng tích hợp thêm dịch vụ.

> Build a data processing pipeline using AWS services: **S3**, **Glue**, and **Athena**.  
> Design a flexible, scalable architecture that supports easy integration.

---

#### ⚙️ Tự động hóa quy trình ETL  

- Toàn bộ quy trình ETL (Extract, Transform, Load) sẽ được tự động hóa bằng AWS Glue và các tác vụ lịch trình.
- Đảm bảo xử lý dữ liệu định kỳ, giảm thiểu lỗi do thao tác thủ công.

> The entire ETL process will be automated using AWS Glue and scheduled jobs.  
> Ensure periodic data processing with minimal manual intervention.

---

#### 📊 Hỗ trợ truy vấn và trực quan hóa  

- Dữ liệu sau xử lý được lưu trữ trên S3 và truy vấn bằng **Athena** thông qua SQL.
- Tùy chọn kết nối với **Amazon QuickSight** để trực quan hóa dữ liệu qua biểu đồ, dashboard.

> Processed data is stored in S3 and queried using **Athena** with SQL.  
> Optionally connect to **Amazon QuickSight** for visualization via charts and dashboards.
