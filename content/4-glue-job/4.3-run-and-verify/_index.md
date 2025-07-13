---
title: "Run Job & Verify Output"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 4.3 </b> "
---

## 4.3 Run Job & Verify Output

1. Go to Glue → Jobs → select `ProcessJob` → **Run**
![Glue](../../images/04/043/1.png?featherlight=false&width=90pc)
2. Monitor job status: `RUNNING → SUCCEEDED`
![Glue](../../images/04/043/2.png?featherlight=false&width=90pc)
3. Open S3 Bucket → check the `processed/` folder
4. Verify output file format: Parquet or CSV
