---
title: "Chạy Job & kiểm tra output"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 4.3 </b> "
---

## 4.3 Chạy Job & kiểm tra output

1. Vào Glue → Jobs → chọn `ProcessJob` → **Run**
2. Theo dõi trạng thái job: `RUNNING → SUCCEEDED`
3. Mở S3 Bucket → thư mục `processed/`
4. Kiểm tra file được sinh ra có đúng định dạng: Parquet hoặc CSV
