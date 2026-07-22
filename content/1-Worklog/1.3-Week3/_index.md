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
- Understand presigned URLs and Amazon S3 lifecycle rules.

### AWS Knowledge:
- Amazon S3 buckets and object key design.
- Block Public Access.
- Server-Side Encryption.
- Presigned PUT and GET URLs.
- Amazon S3 Lifecycle (Standard, Standard-IA, Glacier).
- CORS configuration for Amazon S3.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Review **storage-stack.ts** to identify the S3 buckets created for the project, including raw and processed image buckets. Examine the configuration of Block Public Access, Server-Side Encryption, versioning, and CORS settings for each bucket. | 01/05/2026 | Repo code |
| **2** | Review the API route responsible for generating presigned PUT URLs in the **api-handler**. Record the expiration time, upload conditions such as content type and file size, and compare uploading directly to Amazon S3 with uploading through AWS Lambda. | 02/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/PresignedUrlUploadObject.html |
| **3** | Trace the complete image upload process from the frontend, including selecting an image, requesting a presigned URL, uploading directly to Amazon S3, and updating the upload status. Observe how upload failures and progress are handled in the user interface. | 03/05/2026 | Repo code |
| **4** | Document the responsibilities of the raw bucket and processed bucket. Review the object key naming convention, determine how original and processed images are stored, and investigate whether raw images are automatically cleaned up after processing. | 04/05/2026 | Repo notes |
| **5** | Complete the image upload sequence diagram and finalize the Amazon S3 security checklist, including Block Public Access, Server-Side Encryption, SSL-only access, and lifecycle policies. Propose a more suitable lifecycle rule for infrequently accessed images. | 05/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html |

### Team Collaboration:
- Worked with the frontend team member to understand how the user interface requests presigned URLs before uploading images.
- Collaborated with the team to review the Amazon S3 security checklist, with each member validating different security controls before combining the final results.

### Expected Results:
- A complete image upload sequence diagram.
- Documentation on Amazon S3 security and cost optimization.
- A security checklist covering public access, encryption, SSL, and lifecycle policies.

### Reflection:
- Why is uploading images directly to Amazon S3 more efficient than uploading them through AWS Lambda?
- Is the current lifecycle policy suitable for storing user images, or could it be further optimized?