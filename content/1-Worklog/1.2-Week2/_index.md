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
- Understand how users register, log in, and receive authorization within the system.
- Understand the role of Amazon Cognito, IAM Roles, and IAM Policies in protecting AWS resources.

### AWS Knowledge:
- IAM user, IAM role, and IAM policy.
- Principle of least privilege.
- Amazon Cognito User Pool (attributes, password policy).
- JWT tokens: access token, ID token, and refresh token.
- Cognito Groups for user and administrator authorization.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Study the differences between IAM users, IAM roles, and IAM policies. Review sample IAM policy JSON files in the project and identify the allowed actions and resources. Record examples where permissions may be broader than necessary according to the least privilege principle. | 24/04/2026 | https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html |
| **2** | Review **auth-stack.ts** and analyze the Cognito User Pool configuration, including required user attributes, password policy, MFA settings, User Pool Client configuration, authentication flow, callback URLs, and Cognito Groups for administrators and users. | 25/04/2026 | https://docs.aws.amazon.com/cognito/latest/developerguide/user-pools.html |
| **3** | Trace the complete registration and login flow from the frontend to the backend. Identify where access tokens and ID tokens are stored, how they are attached to API requests, and how the backend validates JWT tokens before processing protected routes. | 26/04/2026 | Repo code |
| **4** | Create an authorization matrix by classifying application routes into public, authenticated, and administrator-only endpoints. Verify that middleware protection is correctly applied and identify routes that may require stronger access control. | 27/04/2026 | Repo notes |
| **5** | Finalize the authentication security checklist, including password policy, MFA configuration, token expiration, and administrator route protection. Document possible security improvements such as enabling MFA and reducing token lifetime where appropriate. | 28/04/2026 | Repo notes |

### Team Collaboration:
- Conducted peer reviews of the authorization matrix to ensure no application routes were overlooked.
- Agreed on a consistent naming convention for public, authenticated, and administrator routes across the development team.

### Expected Results:
- An authentication and authorization matrix.
- Documentation of IAM and Cognito implementation within the project.
- A completed authentication security checklist.

### Reflection:
- Has the project implemented authorization correctly?
- Are the administrator routes sufficiently protected, or are there remaining security risks?