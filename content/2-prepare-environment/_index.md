---
title : "Preparation Steps"
date : 2025-07-05
weight : 2
chapter : true
pre : " <b> 2. </b> "
---

## Preparation Overview

Before deploying the data processing pipeline with Glue and S3, you need to prepare essential AWS resources and permissions.

### Contents:

- [2.1 Create IAM Role](./2.1-create-iam-role)
- [2.2 Create S3 Bucket](./2.2-create-s3-bucket)
- [2.3 Upload Sample Data](./2.3-upload-sample-data)


---

### 🔐 1. IAM Role

Create IAM roles for Glue and Lambda to grant necessary permissions to access AWS services and S3.

---

### 🪣 2. S3 Bucket

Create a bucket to store input and output data with two main folders: `raw/` and `processed/`.

---

### 📂 3. Upload Sample Data

Prepare a simple CSV file (e.g., `sales.csv`) and upload it to the `raw/` folder in the bucket.

---
