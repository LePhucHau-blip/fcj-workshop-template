---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

## Week 7: Observability & Cost Optimization
**Duration: 29/05/2026 - 02/06/2026**

### Weekly Objectives:
- Understand monitoring and observability on AWS.
- Systematically analyze the project's cost optimization strategy.

### AWS Knowledge:
- Amazon CloudWatch Logs, Metrics, and Alarms.
- AWS X-Ray tracing.
- AWS Budgets and Cost Explorer.
- Amazon S3 Lifecycle.
- DynamoDB On-Demand versus Provisioned Capacity.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Review **monitoring-stack.ts** to identify the CloudWatch alarms configured for the project, including Lambda errors, execution duration, throttling, and API Gateway 5xx responses. Record notification channels such as Amazon SNS or email and identify any custom CloudWatch metrics defined by the project. | 29/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html |
| **2** | Review CloudWatch alarms configured for Lambda functions. Evaluate alarm thresholds for errors, duration, and throttling, determine whether the thresholds are appropriate, and identify Lambda functions that are not currently monitored. | 30/05/2026 | Repo code |
| **3** | Review API Gateway monitoring by examining alarms for HTTP 5xx errors and request latency. If possible, simulate an error scenario to verify alarm behavior and document how notifications are delivered when an alarm is triggered. | 31/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| **4** | Identify the project's primary cost drivers, including Amazon S3, AWS Lambda, DynamoDB, API Gateway, Amazon Rekognition, and CloudWatch. Estimate which service is most likely to generate the highest costs as application usage increases and record the metrics that should be monitored in AWS Cost Explorer. | 01/06/2026 | https://aws.amazon.com/aws-cost-management/aws-cost-explorer/ |
| **5** | Review the cost optimization techniques already implemented, including ARM64 Lambda architecture, Amazon S3 Lifecycle policies, and CloudWatch log retention settings. Evaluate the effectiveness of each optimization and classify them as implemented, pending, or requiring further monitoring. | 02/06/2026 | https://aws.amazon.com/aws-cost-management/aws-budgets/ |

### Team Collaboration:
- Assigned each team member responsibility for monitoring the cost of one or two AWS services throughout the week before combining the results into a shared cost optimization document.
- Held a short meeting at the end of the week to prioritize the most important cost optimization opportunities for future implementation.

### Expected Results:
- A monitoring checklist.
- An inventory of CloudWatch dashboards and alarms.
- A cost optimization document categorized as **optimized**, **not yet optimized**, and **requires monitoring**.

### Reflection:
- When a user reports an image upload failure, where should the debugging process begin?
- Which AWS service presents the highest potential cost risk as the system scales?