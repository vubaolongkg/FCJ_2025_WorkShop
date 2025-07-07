---
title : "Create IAM Role"
date : 2025-07-05
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

## Create IAM Role

To ensure AWS services work correctly, you must create IAM roles with proper permissions:

### 🔹 For Glue:
- `AWSGlueServiceRole`
- `AmazonS3FullAccess`

### 🔹 For Lambda:
- `AWSLambdaBasicExecutionRole`
- `AWSGlueConsoleFullAccess`

> These permissions allow Glue to access S3 and Lambda to trigger Glue jobs.
