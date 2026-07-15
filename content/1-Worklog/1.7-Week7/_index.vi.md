---
title: "Nhật ký công việc Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

## Tuần 7: Giám sát hệ thống và Tối ưu chi phí
**Thời gian: 29/05/2026 - 02/06/2026**

### Mục tiêu của tuần:
- Hiểu cách triển khai Monitoring và Observability trên nền tảng AWS.
- Hệ thống hóa chiến lược tối ưu chi phí đang được áp dụng trong dự án.

### Kiến thức AWS:
- CloudWatch Logs, Metrics, Alarms.
- AWS X-Ray Tracing.
- AWS Budgets, Cost Explorer.
- S3 Lifecycle.
- DynamoDB On-demand và Provisioned Capacity.

### Công việc thực hiện:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| 1 | Đọc file `monitoring-stack.ts` để tìm hiểu cấu hình giám sát hệ thống | 29/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html |
| 2 | Kiểm tra các Alarm cho Lambda Error, Duration và Throttling | 30/05/2026 | Mã nguồn của Repository |
| 3 | Kiểm tra Alarm của API Gateway liên quan đến lỗi 5xx và độ trễ (Latency) | 31/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| 4 | Tổng hợp các yếu tố ảnh hưởng đến chi phí: S3, Lambda, DynamoDB, API Gateway, Rekognition, CloudWatch | 01/06/2026 | https://aws.amazon.com/aws-cost-management/aws-cost-explorer/ |
| 5 | Rà soát các phương án tối ưu đã được triển khai: ARM64, Lifecycle, Log Retention | 02/06/2026 | https://aws.amazon.com/aws-cost-management/aws-budgets/ |

### Kết quả đạt được:
- Hoàn thành Checklist giám sát hệ thống (Monitoring Checklist).
- Hoàn thành danh sách Dashboard và Alarm hiện có trong dự án.
- Hoàn thành tài liệu tối ưu chi phí với các nhóm:
  - Đã tối ưu (Optimized).
  - Chưa tối ưu (Not yet optimized).
  - Cần theo dõi thêm (To be monitored).

### Tự đánh giá:
- Khi người dùng báo lỗi trong quá trình Upload hình ảnh, tôi nên bắt đầu kiểm tra và debug từ đâu?
- Dịch vụ AWS nào có nguy cơ phát sinh chi phí cao nhất trong hệ thống?