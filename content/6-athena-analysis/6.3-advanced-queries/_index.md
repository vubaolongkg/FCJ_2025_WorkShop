---
title: "Advanced Queries"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 6.3 </b> "
---

## 6.3 Advanced Queries (optional)
Some common query examples:
- The order is placed in Paris.
![Athena](/images/06/063/1.png?featherlight=false&width=90pc)
```sql
SELECT *
FROM sales_db.sales_processed
WHERE city = 'Paris';
```
![Athena](/images/06/063/2.png?featherlight=false&width=90pc)
- The order belongs to the beverage product group.
![Athena](/images/06/063/3.png?featherlight=false&width=90pc)
```sql
SELECT 
FROM sales_db.sales_processed
WHERE product = 'Beverages'
```
![Athena](/images/06/063/4.png?featherlight=false&width=90pc)