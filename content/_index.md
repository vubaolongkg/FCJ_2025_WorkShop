---
title: "AWS Data Pipeline Workshop"
date: 2025-07-05
weight: 1
chapter: false
---

# 👋 Welcome to the FCJ 2025 AWS Workshop

#### Overview

In this hands-on workshop, you will build a **serverless data pipeline** using AWS services, from ingesting raw CSV files to visualizing clean data through QuickSight. You will also automate the process using Lambda and secure your solution with IAM & CloudTrail.

#### Technologies Used

- **Amazon S3** – Store raw and processed files
- **AWS Glue Crawler** – Catalog CSV structure
- **AWS Glue Job** – Clean and transform data
- **Amazon Athena** – Query processed data
- **Amazon QuickSight** – Visualize insights
- **AWS Lambda** – Automate data flow
- **AWS CloudTrail** – Track actions & monitor

#### Pipeline Flow

![Pipeline Architecture](/images/00/0001.png?featherlight=false&width=90pc)

#### Workshop Goals

- Understand serverless data architecture on AWS
- Clean and enrich raw data using Glue
- Query data with Athena
- Build dashboards in QuickSight
- Automate with Lambda
- Monitor activity using CloudTrail

---

### Main Content

1. [Introduction to Pipeline Concepts](1-introduction/)
2. [Prepare AWS Environment](2-prepare-environment/)
3. [Crawl Raw Data](3-crawler-raw/)
4. [Clean Data with Glue Job](4-glue-job/)
5. [Catalog Processed Data](5-crawler-processed/)
6. [Query with Athena](6-athena-analysis/)
7. [Automate Flow with Lambda](7-automation-lambda/)
8. [Visualize in QuickSight](8-quicksight-dashboard/)
9. [Clean Up AWS Resources](9-cleanup/)
