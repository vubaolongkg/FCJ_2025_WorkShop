---
title: "Connect Athena to QuickSight"
date: 2025-07-05
weight: 1
chapter: false
pre: " <b> 8.1 </b> "
---

## 8.1 Connect Athena to QuickSight
1. Set up IAM Role.
- From the QuickSight home page, select Manage QuickSight, in the upper right corner
![Quicksight](/images/08/081/1.png?featherlight=false&width=90pc)
- Select Security & Permission
![Quicksight](/images/08/081/2.png?featherlight=false&width=90pc)
- Select Manage
![Quicksight](/images/08/081/3.png?featherlight=false&width=90pc)
- We see the role name, go to the Roles section of IAM, find that role name
![Quicksight](/images/08/081/4.png?featherlight=false&width=90pc)
- Attach Policy for the role: `AmazonAthenaFullAccess`, `AmazonS3FullAccess`,`AWSGlueServiceRole`,`AWSQuicksightAthenaAccess`
![Quicksight](/images/08/081/5.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/6.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/7.png?featherlight=false&width=90pc)
2. Go to Amazon QuickSight → **Manage data**
3. Select **New dataset** → **Athena**
![Quicksight](/images/08/081/8.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/9.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/10.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/11.png?featherlight=false&width=90pc)
4. Name and select **Athena workgroup**
![Quicksight](/images/08/081/12.png?featherlight=false&width=90pc)
5. Select database `sales_analysis_db`, table `sales_data_processed`
6. Import data or use SPICE mode to speed up
![Quicksight](/images/08/081/13.png?featherlight=false&width=90pc)
![Quicksight](/images/08/081/14.png?featherlight=false&width=90pc)
