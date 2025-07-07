---
title: "Advanced Queries"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 6.3 </b> "
---

## 6.3 Advanced Queries (optional)

Some useful examples:

- Total revenue by product:

```sql
SELECT product, SUM(amount) AS total_amount
FROM sales_db.sales_processed
GROUP BY product;

Revenue by day:

SELECT order_date, SUM(amount) AS total
FROM sales_db.sales_processed
GROUP BY order_date
ORDER BY order_date;