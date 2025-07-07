---
title: "Create Lambda Function"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 7.1 </b> "
---

## 7.1 Create Lambda Function

1. Go to **AWS Lambda** → Select **Create function**
2. Choose Author from scratch:
   - Name: `RunETLPipeline`
   - Runtime: Python 3.12
   - Role: select existing IAM Role (with Glue, S3, CloudWatch permissions)
3. In the function code section, you'll implement:

- Start crawler for `sales_raw`
- Run Glue Job `ProcessJob`
- Run crawler for `sales_processed`
