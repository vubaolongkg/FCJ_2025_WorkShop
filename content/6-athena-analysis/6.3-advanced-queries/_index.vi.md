---
title: "Viết truy vấn nâng cao"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 6.3 </b> "
---

## 6.3 Viết các câu truy vấn nâng cao (tuỳ chọn)
Một số ví dụ truy vấn phổ biến:
- Đơn hàng ở được đặt Paris.
![Athena](../../images/06/063/1.png?featherlight=false&width=90pc)
```sql
SELECT *
FROM sales_db.sales_processed
WHERE city = 'Paris';
```
![Athena](../../images/06/063/2.png?featherlight=false&width=90pc)
- Đơn hàng thuộc nhóm sản phẩm nước uống. 
![Athena](../../images/06/063/3.png?featherlight=false&width=90pc)
```sql
SELECT 
FROM sales_db.sales_processed
WHERE product = 'Beverages'
```
![Athena](../../images/06/063/4.png?featherlight=false&width=90pc)
