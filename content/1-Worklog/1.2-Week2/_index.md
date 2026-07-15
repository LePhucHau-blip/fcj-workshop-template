---
title: "Week 2 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---


## Week 2: IAM, Cognito & Authentication
**Duration: 24/04/2026 - 28/04/2026**

### Weekly Objectives:
- Understand how users register, log in, and get authorized.
- Understand the role of Cognito, IAM Role, and IAM Policy.

### AWS Knowledge:
- IAM user, role, policy.
- Principle of least privilege.
- Amazon Cognito User Pool.
- JWT token, access token, id token.
- Cognito group: admin, user.

### Project Practice:
| Day | Task | Date | Reference Material |
|---|---|---|---|
| 1 | Learn IAM user, role, policy and the least privilege principle | 24/04/2026 | https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html |
| 2 | Read auth-stack.ts, learn about the Cognito User Pool configuration | 25/04/2026 | https://docs.aws.amazon.com/cognito/latest/developerguide/user-pools.html |
| 3 | Check the login/signup flow from frontend to backend | 26/04/2026 | Repo code |
| 4 | Note down which routes are public, which need auth, and which need admin | 27/04/2026 | Repo notes |
| 5 | Finalize the current auth security checklist | 28/04/2026 | Repo notes |

### Expected Results:
- An authentication/authorization matrix table.
- Notes on IAM/Cognito in the project.
- Current auth security checklist.

### Reflection:
- Has the project implemented authorization correctly?
- Is the admin route secure enough?
