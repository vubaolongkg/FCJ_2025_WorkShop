---
title : "Create IAM Role"
date : 2025-07-05
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

## Create IAM Roles

To ensure AWS services operate correctly, appropriate IAM Roles must be created:

Go to the IAM service and navigate to the **Roles** section.  
![Role](../../images/02/021/1.png?featherlight=false&width=90pc)

### 🔹 For Lambda:
- `AWSGlueServiceRole`
- `AWSS3FullAccess`
- `CloudWatchLogsFullAccess`

Click **Create Role**, select **Service** as **Lambda**.  
![Role](../../images/02/021/2.png?featherlight=false&width=90pc)

Search for and select the roles you need.  
![Role](../../images/02/021/3.png?featherlight=false&width=90pc)

![Role](../../images/02/021/4.png?featherlight=false&width=90pc)

![Role](../../images/02/021/5.png?featherlight=false&width=90pc)

Name it `LambdaRole`, review the settings, and click **Create Role**.  
![Role](../../images/02/021/6.png?featherlight=false&width=90pc)

![Role](../../images/02/021/7.png?featherlight=false&width=90pc)

![Role](../../images/02/021/8.png?featherlight=false&width=90pc)

### 🔹 For Glue:
- `AWSGlueServiceRole`
- `AmazonAthenaFullAccess`
- `AmazonQuicksightAthenaFullAccess`
- `AmazonS3FullAccess`

Similarly, click **Create Role**, then choose the service as **Glue**.  
![Role](../../images/02/021/9.png?featherlight=false&width=90pc)

Search for and select the roles you need.  
![Role](../../images/02/021/10.png?featherlight=false&width=90pc)

![Role](../../images/02/021/11.png?featherlight=false&width=90pc)

![Role](../../images/02/021/12.png?featherlight=false&width=90pc)

![Role](../../images/02/021/13.png?featherlight=false&width=90pc)

Name it `GlueRole`, review the settings, and click **Create Role**.  
![Role](../../images/02/021/14.png?featherlight=false&width=90pc)

![Role](../../images/02/021/15.png?featherlight=false&width=90pc)

![Role](../../images/02/021/16.png?featherlight=false&width=90pc)


> These permissions allow Glue to access S3 and Lambda to trigger Glue jobs.
