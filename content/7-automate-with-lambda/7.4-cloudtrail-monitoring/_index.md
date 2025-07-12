---
title: "Track User Behavior with AWS CloudTrail"
date: 2025-07-05
weight: 4
chapter: false
pre: " <b> 7.4 </b> "
---

## Purpose

**AWS CloudTrail** records API calls and actions across your AWS account. This is crucial for auditing user activities, especially actions like file uploads into S3.

## Steps

### 1. Access CloudTrail

- Go to AWS Console → Search `CloudTrail` → Click **Create trail**
![Lambda](/images/07/074/1.png?featherlight=false&width=90pc)

### 2. Create a new Trail

- **Trail name**: `fcj-trail`
- **Storage**: Choose or create an S3 bucket for logs
- Enable `Log file validation`
- Enable **Multi-region trail**
![Lambda](/images/07/074/2.png?featherlight=false&width=90pc)

### 3. Verify in Event History

- Upload a file to S3
- Navigate to `Event history`
- Filter: `EventName = PutObject`, `Resource = your-data-pipeline-bucket`
- You’ll see who uploaded what and when
![Lambda](/images/07/074/3.png?featherlight=false&width=90pc)
![Lambda](/images/07/074/4.png?featherlight=false&width=90pc)
![Lambda](/images/07/074/5.png?featherlight=false&width=90pc)
![Lambda](/images/07/074/6.png?featherlight=false&width=90pc)

## Benefits

- Track user actions on critical data
- Detect abnormal behavior or misuse
- Improve security and auditing posture

## Tip

Integrate CloudTrail with:
- **CloudWatch Logs** for real-time alerts
- **AWS Config** for resource state tracking