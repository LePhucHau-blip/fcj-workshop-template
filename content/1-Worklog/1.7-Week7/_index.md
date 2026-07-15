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
- Understand monitoring/observability in AWS.
- Systematize the project's cost optimization strategy.

### AWS Knowledge:
- CloudWatch Logs, Metrics, Alarms.
- X-Ray tracing.
- AWS Budgets, Cost Explorer.
- S3 lifecycle, DynamoDB on-demand vs provisioned.

### Project Practice:
| Day | Task | Date | Reference Material |
|---|---|---|---|
| 1 | Read monitoring-stack.ts | 29/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html |
| 2 | Check the alarms for Lambda errors, duration, throttle | 30/05/2026 | Repo code |
| 3 | Check the API Gateway 5xx/latency alarm | 31/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| 4 | Note down cost drivers: S3, Lambda, DynamoDB, API Gateway, Rekognition, CloudWatch | 01/06/2026 | https://aws.amazon.com/aws-cost-management/aws-cost-explorer/ |
| 5 | Review the optimizations already in place: ARM64, lifecycle, log retention | 02/06/2026 | https://aws.amazon.com/aws-cost-management/aws-budgets/ |

### Expected Results:
- Monitoring checklist.
- Dashboard/alarm inventory.
- Cost optimization document: "optimized / not yet optimized / to be monitored".

### Reflection:
- When a user reports an upload error, where would I start debugging?
- Which service carries the highest cost risk?
