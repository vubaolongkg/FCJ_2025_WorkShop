---
title: "Attach S3 Trigger"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 7.3 </b> "
---

## 7.3 Attach S3 Trigger
At Lambda Function, select **Add Trigger**
- Trigger Configuration: S3
- Bucket: `s3/sales-data-bucket-2025`
- Event types: All Objects create events
![Lambda](../../images/07/073/2.png?featherlight=false&width=90pc)
Then press `Add Trigger`
![Lambda](../../images/07/073/3.png?featherlight=false&width=90pc)
Test Lambda and Trigger
- Add new files to S3
![Lambda](../../images/07/073/4.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/5.png?featherlight=false&width=90pc)
- salesdatacrawler started run
![Lambda](../../images/07/073/6.png?featherlight=false&width=90pc)
- salesdatacrawler finished running
![Lambda](../../images/07/073/7.png?featherlight=false&width=90pc)
Configure Amazon EventBridge so that other actions are also triggered after crawling data
- Go to Amazon EventBridge home page
![Lambda](../../images/07/073/8.png?featherlight=false&width=90pc)
- Select *Create rule*
![Lambda](../../images/07/073/9.png?featherlight=false&width=90pc)
- Select Event Pattern as JSON
```json
{
"detail": {
"crawlerName": ["salesdatacrawler"],
"state": ["SUCCEEDED"]
}
}
```
![Lambda](../../images/07/073/10.png?featherlight=false&width=90pc)
- Then configure as shown, role is `LambdaRole`
![Lambda](../../images/07/073/11.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/12.png?featherlight=false&width=90pc)
Test again, after the first Crawl is finished, ETL will automatically run Job
![Lambda](../../images/07/073/13.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/14.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/15.png?featherlight=false&width=90pc)
