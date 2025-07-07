---
title: "Gắn trigger S3 event"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 7.3 </b> "
---

## 7.3 Gắn trigger S3 event

1. Truy cập S3 → chọn bucket chứa dữ liệu (`my-data-pipeline-bucket`)
2. Vào tab **Properties** → **Event notifications**
3. Thêm trigger:
   - Prefix: `raw/`
   - Event type: `PUT` (ObjectCreated)
   - Destination: Lambda function `RunETLPipeline`

> Mỗi khi có file mới trong thư mục `raw/`, Lambda sẽ tự động chạy pipeline.