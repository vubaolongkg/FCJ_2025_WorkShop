---
title: "Gắn trigger S3 event"
date: 2025-07-05
weight: 3
chapter: false
pre: " <b> 7.3 </b> "
---

## 7.3 Gắn trigger S3 event

Tại Lambda Function, chọn **Add Trigger**
- Trigger Configuration: S3
- Bucket: `s3/sales-data-bucket-2025`
- Event types: All Object create events
![Lambda](../../images/07/073/2.png?featherlight=false&width=90pc)
Sau đó nhấn `Add Trigger`
![Lambda](../../images/07/073/3.png?featherlight=false&width=90pc)
Test thử Lambda và Trigger
- Thêm file mới vào S3
![Lambda](../../images/07/073/4.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/5.png?featherlight=false&width=90pc)
- salesdatacrawler bắt đầu chạy
![Lambda](../../images/07/073/6.png?featherlight=false&width=90pc)
- salesdatacrawler chạy xong
![Lambda](../../images/07/073/7.png?featherlight=false&width=90pc)
Cấu hình Amazon EventBridge để các hành động khác cũng được kích hoạt sau khi crawl dữ liệu
- Vào trang chủ Amazon EventBridge
![Lambda](../../images/07/073/8.png?featherlight=false&width=90pc)
- Chọn *Create rule*
![Lambda](../../images/07/073/9.png?featherlight=false&width=90pc)
- Chọn Event Pattern là JSON
```json
{
  "detail": {
    "crawlerName": ["salesdatacrawler"],
    "state": ["SUCCEEDED"]
  }
}
```
![Lambda](../../images/07/073/10.png?featherlight=false&width=90pc)
- Sau đó cấu hình như ảnh, role là `LambdaRole`
![Lambda](../../images/07/073/11.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/12.png?featherlight=false&width=90pc)
Test lại thì sau khi Crawl xong lần 1 thì sẽ tự động chạy ETL Job
![Lambda](../../images/07/073/13.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/14.png?featherlight=false&width=90pc)
![Lambda](../../images/07/073/15.png?featherlight=false&width=90pc)
