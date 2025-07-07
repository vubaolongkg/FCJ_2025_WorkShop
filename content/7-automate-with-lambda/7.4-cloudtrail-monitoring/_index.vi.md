---
title: "Ghi lại hành vi người dùng với AWS CloudTrail"
date: 2025-07-05
weight: 4
chapter: false
pre: " <b> 7.4 </b> "
---

## Mục đích

**AWS CloudTrail** giúp theo dõi và ghi nhật ký tất cả hoạt động của người dùng và dịch vụ AWS, bao gồm các thao tác trên **S3**, **IAM**, **Lambda**, và nhiều dịch vụ khác.

## Các bước thực hiện

### 1. Truy cập dịch vụ CloudTrail

- Vào AWS Console → Tìm `CloudTrail` → Nhấn **Create trail**

### 2. Tạo Trail mới

- **Trail name**: `fcj-trail`
- **Storage location**: Tạo hoặc chọn 1 S3 Bucket để chứa log
- Bật tùy chọn `Log file validation`
- Bật chế độ: **Multi-region trail**

### 3. Cấu hình nhật ký

- Chọn ghi nhật ký **Management events**
- Loại hành động: **Write-only**
- Bật tùy chọn: `Data events` → Chọn **S3** → Add bucket:
  - Bucket name: `your-data-pipeline-bucket`
  - Event type: `PUT` (để ghi lại hành vi ghi dữ liệu)

### 4. Kiểm tra hoạt động

- Upload một file CSV mới vào S3
- Truy cập lại CloudTrail → **Event history**
- Lọc theo `EventName = PutObject` và `Resource = your-data-pipeline-bucket`
- Bạn sẽ thấy ai (IAM user hoặc Lambda) đã thao tác, vào lúc nào

## Lợi ích

- Giúp kiểm tra xem ai đã upload file nào, lúc nào
- Phát hiện bất thường trong thao tác dữ liệu
- Phục vụ mục đích audit và bảo mật

## Gợi ý

Bạn có thể kết hợp CloudTrail với:
- **AWS CloudWatch Logs** để giám sát theo thời gian thực
- **AWS Config** để theo dõi cấu hình tài nguyên
