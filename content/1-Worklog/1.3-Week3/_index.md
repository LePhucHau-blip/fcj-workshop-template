---
title: "Week 3 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---


## Week 3: Amazon S3 & Image Storage
**Duration: 01/05/2026 - 05/05/2026**

### Weekly Objectives:
- Understand how the project stores original and processed images.
- Understand presigned URLs and lifecycle rules.

### AWS Knowledge:
- S3 bucket.
- Object key design.
- Block public access.
- Server-side encryption.
- Presigned PUT/GET URL.
- S3 lifecycle: Standard, IA, Glacier.
- CORS on S3.

### Project Practice:
| Day | Task | Date | Reference Material |
|---|---|---|---|
| 1 | Read storage-stack.ts | 01/05/2026 | Repo code |
| 2 | Read the route that creates the presigned URL in api-handler | 02/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/PresignedUrlUploadObject.html |
| 3 | Trace the image upload flow from the frontend | 03/05/2026 | Repo code |
| 4 | Note down what the raw bucket and processed bucket are used for | 04/05/2026 | Repo notes |
| 5 | Finalize the image upload sequence diagram and S3 security checklist | 05/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html |

### Expected Results:
- Image upload sequence diagram.
- Notes on S3 security/cost optimization.
- Checklist: public access, encryption, SSL, lifecycle.

### Reflection:
- Why is uploading directly to S3 better than uploading through Lambda?
- Is the current lifecycle policy reasonable for user images?
