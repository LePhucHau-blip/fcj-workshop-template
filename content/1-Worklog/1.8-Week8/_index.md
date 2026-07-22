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
- Review the project based on the AWS Well-Architected Framework, focusing on the Security and Reliability pillars.
- Prepare the project for frontend deployment and a basic CI/CD pipeline.

### AWS Knowledge:
- AWS Well-Architected Framework.
- Principle of least privilege and data encryption at rest and in transit.
- DynamoDB Point-in-Time Recovery (PITR).
- Amazon CloudFront and Origin Access Control (OAC).
- Basic CI/CD concepts.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Review the security configuration of **Amazon S3**, **IAM**, **Amazon Cognito**, and **API Gateway**. Verify Block Public Access, encryption settings, IAM policies, password policies, MFA configuration, throttling, and CORS. Compare the implementation against the AWS Well-Architected Security recommendations and previous security checklists. | 05/06/2026 | https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html |
| **2** | Review **DynamoDB Point-in-Time Recovery (PITR)** and the table removal policy. Verify whether PITR is enabled, determine whether the removal policy is configured as **RETAIN** or **DESTROY**, and evaluate the associated production risks. Recommend an appropriate configuration for production environments. | 06/06/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/PointInTimeRecovery.html |
| **3** | Check whether asynchronous Lambda functions such as **image-processor** and **ai-analyzer** have a configured Dead Letter Queue (DLQ) or on-failure destination. Evaluate the risk of losing events without a recovery mechanism. Review the **/v1/images/public** endpoint to ensure that no sensitive information is exposed. | 07/06/2026 | Repo code |
| **4** | Review **frontend-stack.ts** to understand how the frontend is deployed. Determine why Amazon CloudFront is currently disabled or unused, and evaluate when CloudFront should be enabled to provide HTTPS, CDN functionality, and custom domain support. | 08/06/2026 | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html |
| **5** | Run **cdk synth** and **cdk diff** to validate the generated CloudFormation templates and review infrastructure changes before deployment. Design a minimal GitHub Actions CI/CD pipeline consisting of **lint**, **build**, and **test** stages. | 09/06/2026 | https://docs.github.com/en/actions |

### Team Collaboration:
- Assigned each team member responsibility for reviewing one AWS Well-Architected pillar before combining the findings into a shared project assessment.
- Discussed and agreed on a proposed CI/CD workflow to ensure all team members followed a consistent deployment and development process.

### Expected Results:
- A mini review based on the AWS Well-Architected Framework.
- A comprehensive security checklist.
- A backlog of reliability improvements.
- A proposal for a minimal GitHub Actions CI/CD pipeline.

### Reflection:
- Is the project sufficiently secure for deployment in a production environment?
- What is the most critical failure scenario that could occur in the current architecture?