---
title: "Query Processed Data"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 6.2 </b> "
---

## 6.2 Query Processed Data

Once the crawler has created the `sales_processed` table, try running:

```sql
SELECT * FROM sales_db.sales_processed LIMIT 10;