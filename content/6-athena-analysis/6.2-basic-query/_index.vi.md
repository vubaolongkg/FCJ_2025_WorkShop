---
title: "Truy vấn dữ liệu đã xử lý"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 6.2 </b> "
---

## 6.2 Truy vấn dữ liệu đã xử lý

Sau khi crawler đã tạo bảng `sales_data_processed`, bạn có thể truy vấn thử:
![Athena](/images/06/062/1.png?featherlight=false&width=90pc)
```sql
SELECT * FROM sales_db.sales_processed LIMIT 10;
```
Kết quả:
![Athena](/images/06/062/2.png?featherlight=false&width=90pc)
