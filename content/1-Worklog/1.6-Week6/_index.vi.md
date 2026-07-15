---
title: "Nhật ký công việc Tuần 6"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

## Tuần 6: Xử lý hướng sự kiện và Kiểm duyệt hình ảnh bằng AI
**Thời gian: 22/05/2026 - 26/05/2026**

### Mục tiêu của tuần:
- Hiểu quy trình xử lý hình ảnh bất đồng bộ (Asynchronous Image Processing Pipeline) thông qua S3 Event và DynamoDB Stream.
- Hiểu cách dự án ứng dụng AI để gắn nhãn (Tag) và kiểm duyệt (Moderate) hình ảnh.

### Kiến thức AWS:
- Kiến trúc hướng sự kiện (Event-driven Architecture).
- S3 ObjectCreated Event.
- DynamoDB Streams.
- Amazon Rekognition:
  - DetectLabels.
  - DetectModerationLabels.
- Confidence Score.
- Cơ chế Retry Behavior.

### Công việc thực hiện:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| 1 | Đọc file `image-processor/src/index.ts` để tìm hiểu quy trình xử lý hình ảnh | 22/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/NotificationHowTo.html |
| 2 | Đọc file `ai-analyzer/src/index.ts` để tìm hiểu quy trình phân tích AI | 23/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html |
| 3 | Theo dõi luồng xử lý: Upload → Process → Analyze → Completed | 24/05/2026 | Mã nguồn của Repository |
| 4 | Đọc các file `labeling.ts`, `moderation.ts`, `tagMapper.ts` | 25/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/labels-detect-labels-image.html |
| 5 | Kiểm tra vòng đời trạng thái hình ảnh và hàng đợi kiểm duyệt của Admin | 26/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/moderation.html |

### Kết quả đạt được:
- Hoàn thành sơ đồ tuần tự (Sequence Diagram) mô tả Pipeline xử lý hướng sự kiện.
- Hoàn thành bảng trạng thái vòng đời của hình ảnh:
  - UPLOADING.
  - PROCESSING.
  - COMPLETED.
  - ERROR.
- Hoàn thành bảng ánh xạ dữ liệu:
  - Kết quả trả về từ Amazon Rekognition.
  - Mô hình dữ liệu của ứng dụng.

### Tự đánh giá:
- Nếu Lambda xử lý hình ảnh gặp lỗi, hệ thống sẽ phản ứng và xử lý như thế nào?
- Hình ảnh bị đánh dấu vi phạm nên được xử lý và hiển thị trên giao diện người dùng như thế nào?