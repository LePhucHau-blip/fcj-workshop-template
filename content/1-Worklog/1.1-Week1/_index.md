---
title: "Week 1 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

## Week 1: AWS Foundation & Project Overview
**Duration: 17/04/2026 - 21/04/2026**

### Weekly Objectives:
- Gain an overview of the AWS Cloud Journey and the bootcamp structure.
- Understand the problem that the Smart Image Platform project is designed to solve.
- Identify the AWS services used in the project and understand the role of each service.

### AWS Knowledge:
- AWS Account, Region, and Availability Zone.
- Basic IAM concepts (root account, IAM user, and permissions overview).
- Introduction to Amazon S3, AWS Lambda, API Gateway, and DynamoDB.
- The concept and advantages of serverless architecture compared with traditional server-based architecture.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Read **README.md** and **README.vi.md** to understand the project objectives, scope, and technologies. Take notes on unfamiliar concepts such as serverless architecture, single-table design, and presigned URLs. Review the repository structure including frontend, backend, and infrastructure folders. | 17/04/2026 | Repo README |
| **2** | Learn about AWS Global Infrastructure including Regions, Availability Zones, and Edge Locations. Compare factors for choosing a region such as latency, cost, and data compliance. Draw a simple diagram showing the relationship between Region, AZ, and Edge Location. | 18/04/2026 | https://aws.amazon.com/about-aws/global-infrastructure/ |
| **3** | Review the **infrastructure/lib/stacks** directory. Identify infrastructure stacks including storage, database, authentication, API, monitoring, and frontend. Record stack dependencies and note unclear implementation details for later discussion with the mentor and team. | 19/04/2026 | Repo code |
| **4** | Redraw the overall system architecture from frontend through API Gateway, Lambda, S3, DynamoDB, and Rekognition. Document the main data flow for image upload, image processing, and image retrieval. Compare the diagram with the project documentation to verify understanding. | 20/04/2026 | Repo docs |
| **5** | Create a summary table of all AWS services used in the project, describing each service's role and the reason it was selected. Identify possible services that could be optimized or replaced in future improvements. Complete the **week-01-project-overview.md** notes. | 21/04/2026 | Repo notes |

### Team Collaboration:
- Held a team meeting at the beginning of the week to assign each member one or two AWS services for deeper research before sharing the findings with the group.
- Conducted a review session at the end of the week to compare individual architecture diagrams and finalize a common architecture design.

### Expected Results:
- A documentation file: **week-01-project-overview.md**.
- A complete architecture diagram of the Smart Image Platform.
- A summary table describing the AWS services used in the project and the role of each service.

### Reflection:
- In what ways is this project suitable for a serverless architecture?
- Which component of the system architecture do I still need to understand better before moving on to the next week?