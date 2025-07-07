---
title: "Viết truy vấn nâng cao"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 6.3 </b> "
---

## 6.3 Viết các câu truy vấn nâng cao (tuỳ chọn)

Một số ví dụ truy vấn phổ biến:

- Tổng doanh thu theo sản phẩm:

```sql
SELECT product, SUM(amount) AS total_amount
FROM sales_db.sales_processed
GROUP BY product;

Doanh thu theo ngày:

SELECT order_date, SUM(amount) AS total
FROM sales_db.sales_processed
GROUP BY order_date
ORDER BY order_date;