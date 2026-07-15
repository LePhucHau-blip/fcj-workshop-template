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
- Understand the project's serverless backend.
- Understand API Gateway REST API and Lambda proxy integration.

### AWS Knowledge:
- AWS Lambda runtime, memory, timeout.
- Lambda cold start.
- API Gateway REST API.
- CORS.
- Request validation.
- Throttling.
- Lambda log retention.

### Project Practice:
| Day | Task | Date | Reference Material |
|---|---|---|---|
| 1 | Read api-stack.ts | 08/05/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html |
| 2 | Read backend/api-handler/src/index.ts | 09/05/2026 | Repo code |
| 3 | Read the routes: upload, images, search, profile, admin | 10/05/2026 | Repo code |
| 4 | Run the backend/infrastructure build | 11/05/2026 | Repo code |
| 5 | Note down the list of API endpoints | 12/05/2026 | Repo docs |

### Expected Results:
- API endpoint catalog.
- Notes on Lambda functions: memory, timeout, responsibility.
- A clear understanding of what the API Handler Lambda does.

### Reflection:
- Is the API Handler currently taking on too many responsibilities?
- Which routes should be split out if the system scales up?
