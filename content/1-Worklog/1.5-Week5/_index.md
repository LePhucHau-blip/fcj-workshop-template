---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

## Week 5: DynamoDB Data Modeling
**Duration: 15/05/2026 - 19/05/2026**

### Weekly Objectives:
- Understand the single-table design used in the project.
- Learn when to use Query, Scan, and Global Secondary Indexes (GSIs).

### AWS Knowledge:
- DynamoDB partition key and sort key.
- Query versus Scan.
- Global Secondary Index (GSI).
- Projection types.
- On-demand billing mode.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Review **database-stack.ts** to identify the primary table's partition key and sort key. Record the configured Global Secondary Indexes (GSIs), their purposes, and verify whether the table uses on-demand or provisioned billing mode. | 15/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/UserGuide/HowItWorks.html |
| **2** | Analyze the database queries implemented in **images.ts**, **search.ts**, and **admin.ts**. Identify whether each operation uses Query or Scan, evaluate filtering conditions, and determine which queries may cause performance issues when the dataset grows. | 16/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Query.html |
| **3** | Design and document the project's single-table data model, including image metadata items, tag items, and moderation items. Record the partition key (PK), sort key (SK), entity relationships, and the structure of each item type. | 17/05/2026 | Repo notes |
| **4** | Identify opportunities for optimization by reviewing the public gallery implementation, which currently relies on Scan operations. Analyze the performance and cost implications of Scan and investigate how a Global Secondary Index (GSI) could improve query efficiency. | 18/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GSI.html |
| **5** | Finalize the DynamoDB data model documentation, create an access pattern table that maps application features to database queries, and propose a new GSI design for the public gallery, including the recommended partition key and sort key. | 19/05/2026 | Repo notes |

### Team Collaboration:
- Worked with the team to identify the most important access patterns that should be optimized first.
- Collaborated with the member responsible for the administration module to review database queries in **admin.ts** and verify the overall data model.

### Expected Results:
- A complete DynamoDB data model document.
- An access pattern table for the application.
- A Global Secondary Index (GSI) proposal for the public gallery.

### Reflection:
- What advantages does the single-table design provide for this project?
- Which access patterns still require optimization?