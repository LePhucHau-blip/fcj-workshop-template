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
- Understand the asynchronous image processing pipeline (S3 event, DynamoDB Stream).
- Understand how the project uses AI to tag and moderate images.

### AWS Knowledge:
- Event-driven architecture.
- S3 ObjectCreated event.
- DynamoDB Streams.
- Rekognition DetectLabels, DetectModerationLabels.
- Confidence score, retry behavior.

### Project Practice:
| Day | Task | Date | Reference Material |
|---|---|---|---|
| 1 | Read image-processor/src/index.ts | 22/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/NotificationHowTo.html |
| 2 | Read ai-analyzer/src/index.ts | 23/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html |
| 3 | Trace the flow: upload → process → analyze → completed | 24/05/2026 | Repo code |
| 4 | Read labeling.ts, moderation.ts, tagMapper.ts | 25/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/labels-detect-labels-image.html |
| 5 | Check the image status lifecycle and the admin moderation queue | 26/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/moderation.html |

### Expected Results:
- Sequence diagram of the event-driven pipeline.
- Image status table: UPLOADING, PROCESSING, COMPLETED, error.
- Mapping table: Rekognition output → app data model.

### Reflection:
- If the Lambda that processes images fails, how does the system react?
- How should a flagged image be handled in the UI?
