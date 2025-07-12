---
title: "Create Lambda Function"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 7.1 </b> "
---

## 7.1 Create Lambda Function
1. Go to **AWS Lambda** → Select **Create function**
![Lambda](/images/07/071/1.png?featherlight=false&width=90pc)
2. Select Author from scratch:
- Name: `gluecrawljob`
- Runtime: Python 3.13
- Role: select the IAM Role created (with Glue + CloudWatch + S3 permissions)
![Lambda](/images/07/071/2.png?featherlight=false&width=90pc)
![Lambda](/images/07/071/3.png?featherlight=false&width=90pc)
![Lambda](/images/07/073/1.png?featherlight=false&width=90pc)
3. In the function code section, you will write code to perform:
- Start crawler for `sales_data_raw`
- Run Glue Job `ProcessJob`
- Run crawler for `sales_data_processed`
![Lambda](/images/07/071/4.png?featherlight=false&width=90pc)
