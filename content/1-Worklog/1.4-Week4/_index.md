---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

## Week 4: Lambda & API Gateway
**Duration: 08/05/2026 - 12/05/2026**

### Weekly Objectives:
- Understand the project's serverless backend architecture.
- Understand Amazon API Gateway REST APIs and Lambda Proxy Integration.

### AWS Knowledge:
- AWS Lambda runtime, memory allocation, and timeout configuration.
- Lambda cold start.
- Amazon API Gateway REST API.
- CORS configuration.
- Request validation.
- API throttling.
- Lambda log retention.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Review **api-stack.ts** to identify the API Gateway resources and HTTP methods defined in the project. Examine CORS configuration, request throttling settings, and API Gateway deployment configuration. | 08/05/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html |
| **2** | Review **backend/api-handler/src/index.ts** to understand how the Lambda handler routes requests based on HTTP methods and paths. Examine common middleware such as authentication, logging, and error handling. Measure Lambda cold start time after a period of inactivity. | 09/05/2026 | Repo code |
| **3** | Study the application routes, including **upload**, **images**, **search**, **profile**, and **admin**. Record the request and response structure of each endpoint and identify which routes contain the most complex business logic. | 10/05/2026 | Repo code |
| **4** | Build the backend and infrastructure components by running the project build process and **cdk synth**. Record any build or configuration errors encountered, investigate solutions, and review the generated Lambda package size and build duration. | 11/05/2026 | Repo code |
| **5** | Create a complete API endpoint catalog including HTTP method, endpoint path, description, and authentication requirements. Document the memory allocation, timeout configuration, and responsibilities of each Lambda function used by the project. | 12/05/2026 | Repo docs |

### Team Collaboration:
- Divided the API routes among team members, allowing each member to analyze two or three routes before combining the findings into a complete API catalog.
- Discussed which routes should eventually be separated into dedicated Lambda functions as the system grows and becomes more scalable.

### Expected Results:
- A complete API endpoint catalog.
- Documentation of Lambda functions, including memory allocation, timeout settings, and responsibilities.
- A clear understanding of the responsibilities of the API Handler Lambda.

### Reflection:
- Is the API Handler Lambda currently responsible for too many tasks?
- Which API routes should be separated into independent Lambda functions as the application scales?