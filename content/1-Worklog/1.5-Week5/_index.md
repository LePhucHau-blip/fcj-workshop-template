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
- Know when to use Query, Scan, and GSI.

### AWS Knowledge:
- DynamoDB partition key, sort key.
- Query vs Scan.
- GSI.
- Projection.
- On-demand billing.

### Project Practice:
| Day | Task | Date | Reference Material |
|---|---|---|---|
| 1 | Read database-stack.ts | 15/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/UserGuide/HowItWorks.html |
| 2 | Read the queries in images.ts, search.ts, admin.ts | 16/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Query.html |
| 3 | Draw the data model: image metadata, tag item, moderation item | 17/05/2026 | Repo notes |
| 4 | Identify optimization gaps: the public gallery currently uses Scan | 18/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GSI.html |
| 5 | Finalize the data model document and propose a GSI for the public gallery | 19/05/2026 | Repo notes |

### Expected Results:
- Data model document.
- Access pattern table.
- GSI proposal for the public gallery.

### Reflection:
- What benefits does the single-table design provide?
- Which access pattern is not well designed?
