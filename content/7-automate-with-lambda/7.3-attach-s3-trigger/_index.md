---
title: "Attach S3 Trigger"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 7.3 </b> "
---

## 7.3 Attach S3 Trigger

1. Go to S3 → select your bucket (`my-data-pipeline-bucket`)
2. Navigate to **Properties** → **Event notifications**
3. Add a new trigger:
   - Prefix: `raw/`
   - Event type: `PUT` (ObjectCreated)
   - Destination: Lambda function `RunETLPipeline`

> Every time a new file is uploaded to `raw/`, the Lambda function will automatically run the pipeline.
