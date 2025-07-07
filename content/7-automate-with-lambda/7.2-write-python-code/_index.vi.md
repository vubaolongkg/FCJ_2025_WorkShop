---
title: "Viết mã Python cho Lambda"
date: 2025-07-05
weight: 2
chapter: false
pre: " <b> 7.2 </b> "
---

## 7.2 Viết mã Python cho Lambda

Sử dụng thư viện `boto3` để gọi AWS Glue APIs:

```python
import boto3
import logging
import time

logger = logging.getLogger()
logger.setLevel(logging.INFO)

glue = boto3.client('glue')

def lambda_handler(event, context):
    logger.info("🔁 Lambda triggered")

    crawler_name = 'salesdatacrawler'
    try:
        glue.start_crawler(Name=crawler_name)
        logger.info(f"✅ Successfully started crawler: {crawler_name}")
    except glue.exceptions.CrawlerRunningException:
        logger.warning(f"⚠️ Crawler {crawler_name} is already running.")
    except Exception as e:
        logger.error(f"❌ Failed to start crawler {crawler_name}: {str(e)}")
        return {
            'statusCode': 500,
            'body': f"Error starting crawler {crawler_name}: {str(e)}"
        }

    logger.info(f"⏳ Waiting for crawler {crawler_name} to complete...")
    while True:
        crawler_state = glue.get_crawler(Name=crawler_name)['Crawler']['State']
        if crawler_state == 'READY':
            logger.info(f"✅ Crawler {crawler_name} finished.")
            break
        time.sleep(10)

    job_name = 'ProcessJob'
    try:
        while True:
            job_runs = glue.get_job_runs(JobName=job_name, MaxResults=1)
            if not job_runs['JobRuns']:
                break
            current_status = job_runs['JobRuns'][0]['JobRunState']
            if current_status in ['RUNNING', 'STARTING', 'STOPPING']:
                logger.info(f"🕒 Glue Job {job_name} is currently {current_status}, waiting...")
                time.sleep(15)
            else:
                break

        logger.info(f"🚀 Starting Glue Job: {job_name}")
        response = glue.start_job_run(JobName=job_name)
        job_run_id = response['JobRunId']

    except Exception as e:
        logger.error(f"❌ Failed to start Glue Job: {str(e)}")
        return {
            'statusCode': 500,
            'body': f"Error starting Glue job: {str(e)}"
        }

    logger.info(f"⏳ Waiting for Glue Job {job_name} to complete...")
    while True:
        job_status = glue.get_job_run(JobName=job_name, RunId=job_run_id)
        state = job_status['JobRun']['JobRunState']
        logger.info(f"🧪 Glue Job status: {state}")
        if state in ['SUCCEEDED', 'FAILED', 'STOPPED']:
            break
        time.sleep(15)

    if state != 'SUCCEEDED':
        logger.error(f"❌ Glue Job ended with status: {state}")
        return {
            'statusCode': 500,
            'body': f"Glue Job failed or stopped with status: {state}"
        }

    logger.info(f"✅ Glue Job {job_name} completed successfully.")

    second_crawler = 'salesdatacrawler_processed'
    try:
        glue.start_crawler(Name=second_crawler)
        logger.info(f"✅ Successfully started crawler: {second_crawler}")
        return {
            'statusCode': 200,
            'body': f"Workflow completed. Crawler {second_crawler} started."
        }
    except Exception as e:
        logger.error(f"❌ Failed to start second crawler: {str(e)}")
        return {
            'statusCode': 500,
            'body': f"Error starting second crawler {second_crawler}: {str(e)}"
        }
```
>Đừng quên log trạng thái để kiểm tra trong CloudWatch Logs.

