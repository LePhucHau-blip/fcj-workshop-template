---
title: "Nhật ký công việc Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

## Tuần 7: Giám sát hệ thống & Tối ưu chi phí
**Thời gian: 29/05/2026 - 02/06/2026**

### Mục tiêu tuần:
- Hiểu về giám sát (Monitoring) và Observability trên AWS.
- Hệ thống hóa chiến lược tối ưu chi phí của dự án.

### Kiến thức AWS:
- Amazon CloudWatch Logs, Metrics và Alarms.
- AWS X-Ray.
- AWS Budgets và Cost Explorer.
- Amazon S3 Lifecycle.
- DynamoDB On-Demand và Provisioned Capacity.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Đọc **monitoring-stack.ts** để xác định các CloudWatch Alarm được cấu hình cho dự án, bao gồm Lambda Errors, Duration, Throttling và API Gateway 5xx. Ghi chú các kênh nhận cảnh báo như Amazon SNS hoặc Email và xác định các Custom Metric nếu có. | 29/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html |
| **2** | Kiểm tra các CloudWatch Alarm dành cho Lambda Functions. Đánh giá ngưỡng cảnh báo đối với Errors, Duration và Throttling, xác định các Lambda chưa được giám sát và đánh giá mức độ phù hợp của từng ngưỡng cảnh báo. | 30/05/2026 | Repo code |
| **3** | Kiểm tra hệ thống giám sát của API Gateway thông qua các Alarm cho HTTP 5xx và độ trễ (Latency). Nếu có thể, mô phỏng một tình huống lỗi để xác minh hoạt động của Alarm và ghi nhận quy trình gửi thông báo khi cảnh báo được kích hoạt. | 31/05/2026 | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html |
| **4** | Phân tích các nguồn phát sinh chi phí chính của dự án gồm Amazon S3, AWS Lambda, DynamoDB, API Gateway, Amazon Rekognition và CloudWatch. Ước lượng dịch vụ có nguy cơ phát sinh chi phí lớn nhất khi lượng người dùng tăng và ghi chú các chỉ số cần theo dõi trong AWS Cost Explorer. | 01/06/2026 | https://aws.amazon.com/aws-cost-management/aws-cost-explorer/ |
| **5** | Rà soát các giải pháp tối ưu chi phí đã được áp dụng như kiến trúc ARM64 cho Lambda, Amazon S3 Lifecycle và CloudWatch Log Retention. Đánh giá hiệu quả của từng giải pháp và phân loại thành **đã tối ưu**, **chưa tối ưu** hoặc **cần tiếp tục theo dõi**. | 02/06/2026 | https://aws.amazon.com/aws-cost-management/aws-budgets/ |

### Phối hợp nhóm:
- Phân công mỗi thành viên theo dõi chi phí của một đến hai dịch vụ AWS trong tuần, sau đó tổng hợp kết quả thành tài liệu tối ưu chi phí chung của nhóm.
- Họp ngắn vào cuối tuần để thống nhất các hạng mục tối ưu chi phí cần ưu tiên triển khai trong giai đoạn tiếp theo.

### Kết quả đạt được:
- Hoàn thành checklist giám sát hệ thống.
- Hoàn thành danh mục CloudWatch Dashboard và Alarm của dự án.
- Hoàn thành tài liệu tối ưu chi phí được phân loại thành **đã tối ưu**, **chưa tối ưu** và **cần tiếp tục theo dõi**.

### Tự đánh giá:
- Khi người dùng báo lỗi upload ảnh, mình nên bắt đầu quá trình kiểm tra từ đâu?
- Dịch vụ AWS nào có nguy cơ phát sinh chi phí cao nhất khi hệ thống mở rộng?