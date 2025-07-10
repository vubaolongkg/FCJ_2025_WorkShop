---
title: "Run Crawler"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 3.3 </b> "
---

## 3.3 Run Glue Crawler

- After creating, select the `salesdatacrawler` and click **Run Crawler**.
![Glue](/images/03/033/1.png?featherlight=false&width=90pc)
- Verify the table:
  - Open Glue Console → `Databases` → `sales_analysis_db`
![Glue](/images/03/033/2.png?featherlight=false&width=90pc)
  - Ensure `sales_data_raw` table has correct structure matching `sales_dataset.csv`.
![Glue](/images/03/033/3.png?featherlight=false&width=90pc)
> This confirms that schema extraction was successful.
