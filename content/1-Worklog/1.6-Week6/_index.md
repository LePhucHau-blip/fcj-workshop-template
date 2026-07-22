---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

## Week 6: Event-Driven Processing & AI Moderation
**Duration: 22/05/2026 - 26/05/2026**

### Weekly Objectives:
- Understand the asynchronous image processing pipeline using Amazon S3 Events and DynamoDB Streams.
- Understand how the project uses Amazon Rekognition to automatically tag and moderate images.

### AWS Knowledge:
- Event-driven architecture.
- Amazon S3 ObjectCreated events.
- DynamoDB Streams.
- Amazon Rekognition DetectLabels and DetectModerationLabels.
- Confidence score and retry mechanisms.

### Project Practice:

| Day | Task | Date | Reference Material |
|---|---|---|---|
| **1** | Review **image-processor/src/index.ts** to identify how the Lambda function is triggered by Amazon S3 ObjectCreated events. Document the processing workflow, including reading images from the raw bucket, generating resized images and thumbnails, storing processed images, and updating the image status in DynamoDB. | 22/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/NotificationHowTo.html |
| **2** | Review **ai-analyzer/src/index.ts** to understand how DynamoDB Streams trigger the AI analysis Lambda. Examine how Amazon Rekognition detects image labels and moderation labels, and how the analysis results are written back to DynamoDB. | 23/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html |
| **3** | Trace the complete event-driven processing pipeline from image upload through image processing, AI analysis, and completion. Estimate the execution time of each processing stage using CloudWatch logs and identify potential bottlenecks or failure points. | 24/05/2026 | Repo code |
| **4** | Review **labeling.ts**, **moderation.ts**, and **tagMapper.ts** to understand how Rekognition labels are mapped to application tags, how confidence thresholds are applied, and how inappropriate images are handled after moderation analysis. | 25/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/labels-detect-labels-image.html |
| **5** | Review the complete image status lifecycle, including **UPLOADING**, **PROCESSING**, **COMPLETED**, **FLAGGED**, and **ERROR** states. Examine how the administrator moderation queue manages flagged images and complete the mapping between Rekognition output and the application's data model. | 26/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/moderation.html |

### Team Collaboration:
- Collaborated with team members to upload sample test images (containing only appropriate, policy-compliant content) to observe how the moderation pipeline processed different scenarios.
- Shared and reviewed the event-driven sequence diagram with the team to establish consistent terminology and understanding of each processing stage.

### Expected Results:
- A complete sequence diagram of the event-driven image processing pipeline.
- An image status table covering **UPLOADING**, **PROCESSING**, **COMPLETED**, **FLAGGED**, and **ERROR** states.
- A mapping table between Amazon Rekognition output and the application's data model.

### Reflection:
- How does the system respond when the image processing Lambda function fails?
- How should flagged images be presented and managed within the application's user interface?