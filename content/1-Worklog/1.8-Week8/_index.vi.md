---
title: "Nhật ký công việc Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

## Tuần 8: Đánh giá bảo mật, độ tin cậy và CI/CD
**Thời gian: 05/06/2026 - 09/06/2026**

### Mục tiêu của tuần:
- Đánh giá lại dự án theo phương pháp **AWS Well-Architected Framework** (Security, Reliability).
- Chuẩn bị triển khai Frontend và xây dựng quy trình CI/CD.

### Kiến thức AWS:
- AWS Well-Architected Framework.
- Least Privilege, Encryption at Rest và Encryption in Transit.
- DynamoDB Point-In-Time Recovery (PITR).
- CloudFront, Origin Access Control (OAC).
- Kiến thức cơ bản về CI/CD.

### Công việc thực hiện:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| 1 | Rà soát các thành phần S3, IAM, Cognito, API Gateway theo AWS Well-Architected Framework | 05/06/2026 | https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html |
| 2 | Kiểm tra DynamoDB PITR và Removal Policy trong dự án | 06/06/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/PointInTimeRecovery.html |
| 3 | Kiểm tra việc thiếu DLQ/On-failure Destination và đánh giá Public Route `/v1/images/public` | 07/06/2026 | Mã nguồn của Repository |
| 4 | Đọc file `frontend-stack.ts`, tìm hiểu lý do CloudFront hiện đang bị vô hiệu hóa | 08/06/2026 | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html |
| 5 | Chạy `cdk synth` / `cdk diff`, đề xuất Pipeline GitHub Actions (Lint, Build, Test) | 09/06/2026 | https://docs.github.com/en/actions |

### Kết quả đạt được:
- Hoàn thành đánh giá tổng quan dự án theo AWS Well-Architected Framework.
- Hoàn thành Checklist kiểm tra bảo mật hệ thống.
- Xây dựng danh sách các vấn đề cần cải thiện về độ tin cậy (Reliability Improvement Backlog).
- Đề xuất quy trình CI/CD tối thiểu bao gồm:
  - Lint.
  - Build.
  - Test.

### Tự đánh giá:
- Hệ thống hiện tại đã đủ an toàn để triển khai trong môi trường Production hay chưa?
- Kịch bản lỗi nghiêm trọng nhất có thể xảy ra đối với hệ thống là gì?