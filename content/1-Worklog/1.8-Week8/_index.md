---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---


## Week 8: Security, Reliability Review & CI/CD
**Duration: 05/06/2026 - 09/06/2026**

### Weekly Objectives:
- Review the project following the AWS Well-Architected approach (Security, Reliability).
- Prepare for frontend deployment and CI/CD.

### AWS Knowledge:
- AWS Well-Architected Framework.
- Least privilege, encryption at rest/in transit.
- DynamoDB PITR.
- CloudFront, Origin Access Control.
- Basic CI/CD.

### Project Practice:
| Day | Task | Date | Reference Material |
|---|---|---|---|
| 1 | Review S3, IAM, Cognito, API Gateway | 05/06/2026 | https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html |
| 2 | Review DynamoDB PITR and removal policy | 06/06/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/PointInTimeRecovery.html |
| 3 | Check for missing DLQ/on-failure destination, check the public route /v1/images/public | 07/06/2026 | Repo code |
| 4 | Read frontend-stack.ts, note down why CloudFront is currently disabled | 08/06/2026 | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html |
| 5 | Run cdk synth/diff, propose a GitHub Actions pipeline (lint, build, test) | 09/06/2026 | https://docs.github.com/en/actions |

### Expected Results:
- Well-Architected mini-review.
- Security checklist.
- Reliability improvement backlog.
- A proposal for a minimal CI/CD pipeline.

### Reflection:
- Is the project secure enough for production?
- What is the most serious failure scenario?
