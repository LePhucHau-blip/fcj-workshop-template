---
title: "Nhật ký công việc Tuần 6"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

## Tuần 6: Xử lý theo sự kiện & AI kiểm duyệt hình ảnh
**Thời gian: 22/05/2026 - 26/05/2026**

### Mục tiêu tuần:
- Hiểu pipeline xử lý ảnh bất đồng bộ sử dụng Amazon S3 Events và DynamoDB Streams.
- Hiểu cách dự án sử dụng Amazon Rekognition để tự động gắn nhãn và kiểm duyệt hình ảnh.

### Kiến thức AWS:
- Kiến trúc hướng sự kiện (Event-Driven Architecture).
- Amazon S3 ObjectCreated Event.
- DynamoDB Streams.
- Amazon Rekognition DetectLabels và DetectModerationLabels.
- Confidence Score và cơ chế Retry.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Đọc **image-processor/src/index.ts** để xác định cách Lambda được kích hoạt bởi Amazon S3 ObjectCreated Event. Ghi chú quy trình xử lý gồm đọc ảnh từ Raw Bucket, tạo ảnh thu nhỏ (thumbnail), lưu ảnh đã xử lý vào Processed Bucket và cập nhật trạng thái ảnh trong DynamoDB. | 22/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/NotificationHowTo.html |
| **2** | Đọc **ai-analyzer/src/index.ts** để tìm hiểu cách DynamoDB Streams kích hoạt Lambda phân tích AI. Kiểm tra cách Amazon Rekognition phát hiện nhãn (labels), nhãn kiểm duyệt (moderation labels) và cách kết quả được cập nhật trở lại DynamoDB. | 23/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html |
| **3** | Theo dõi toàn bộ pipeline xử lý ảnh từ lúc upload, xử lý ảnh, phân tích AI cho đến khi hoàn thành. Ước lượng thời gian xử lý của từng bước thông qua CloudWatch Logs và xác định các điểm có nguy cơ gây chậm hoặc phát sinh lỗi. | 24/05/2026 | Repo code |
| **4** | Đọc **labeling.ts**, **moderation.ts** và **tagMapper.ts** để tìm hiểu cách ánh xạ nhãn từ Amazon Rekognition sang các tag của ứng dụng, cách sử dụng Confidence Score và cách xử lý các hình ảnh bị đánh dấu vi phạm. | 25/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/labels-detect-labels-image.html |
| **5** | Kiểm tra vòng đời trạng thái của hình ảnh gồm **UPLOADING**, **PROCESSING**, **COMPLETED**, **FLAGGED** và **ERROR**. Tìm hiểu cách hàng đợi kiểm duyệt của quản trị viên xử lý các ảnh bị gắn cờ và hoàn thiện bảng ánh xạ giữa kết quả Rekognition và mô hình dữ liệu của ứng dụng. | 26/05/2026 | https://docs.aws.amazon.com/rekognition/latest/dg/moderation.html |

### Phối hợp nhóm:
- Cùng các thành viên trong nhóm thử nghiệm upload các hình ảnh mẫu phù hợp với chính sách để quan sát hoạt động thực tế của quy trình kiểm duyệt tự động.
- Chia sẻ và cùng rà soát sơ đồ tuần tự của pipeline xử lý theo sự kiện nhằm thống nhất cách hiểu và tên gọi của từng bước trong hệ thống.

### Kết quả đạt được:
- Hoàn thành sơ đồ tuần tự của pipeline xử lý ảnh theo sự kiện.
- Hoàn thành bảng trạng thái hình ảnh gồm **UPLOADING**, **PROCESSING**, **COMPLETED**, **FLAGGED** và **ERROR**.
- Hoàn thành bảng ánh xạ giữa kết quả Amazon Rekognition và mô hình dữ liệu của ứng dụng.

### Tự đánh giá:
- Nếu Lambda xử lý ảnh gặp lỗi, hệ thống sẽ phản ứng như thế nào?
- Các hình ảnh bị gắn cờ nên được hiển thị và xử lý trên giao diện người dùng ra sao?