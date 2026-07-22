---
title: "Nhật ký công việc Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

## Tuần 8: Đánh giá bảo mật, độ tin cậy & CI/CD
**Thời gian: 05/06/2026 - 09/06/2026**

### Mục tiêu tuần:
- Đánh giá dự án theo AWS Well-Architected Framework, tập trung vào hai trụ cột Security và Reliability.
- Chuẩn bị cho việc triển khai frontend và xây dựng quy trình CI/CD cơ bản.

### Kiến thức AWS:
- AWS Well-Architected Framework.
- Nguyên tắc Least Privilege và mã hóa dữ liệu khi lưu trữ (at rest) và truyền tải (in transit).
- DynamoDB Point-in-Time Recovery (PITR).
- Amazon CloudFront và Origin Access Control (OAC).
- Kiến thức cơ bản về CI/CD.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Rà soát cấu hình bảo mật của **Amazon S3**, **IAM**, **Amazon Cognito** và **API Gateway**. Kiểm tra Block Public Access, mã hóa dữ liệu, IAM Policy, Password Policy, MFA, Throttling và CORS. Đối chiếu kết quả với các khuyến nghị của AWS Well-Architected và checklist bảo mật đã thực hiện ở các tuần trước. | 05/06/2026 | https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html |
| **2** | Kiểm tra **DynamoDB Point-in-Time Recovery (PITR)** và Removal Policy của bảng dữ liệu. Xác định PITR đã được bật hay chưa, Removal Policy đang sử dụng **RETAIN** hay **DESTROY**, đánh giá rủi ro đối với môi trường Production và đề xuất cấu hình phù hợp. | 06/06/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/PointInTimeRecovery.html |
| **3** | Kiểm tra các Lambda xử lý bất đồng bộ như **image-processor** và **ai-analyzer** để xác định đã cấu hình Dead Letter Queue (DLQ) hoặc On-Failure Destination hay chưa. Đánh giá rủi ro mất dữ liệu khi không có cơ chế khôi phục sự kiện và kiểm tra endpoint **/v1/images/public** để đảm bảo không làm lộ dữ liệu nhạy cảm. | 07/06/2026 | Repo code |
| **4** | Đọc **frontend-stack.ts** để tìm hiểu cách frontend được triển khai. Ghi chú lý do Amazon CloudFront hiện chưa được sử dụng và đánh giá thời điểm phù hợp để triển khai CloudFront nhằm cung cấp HTTPS, CDN và hỗ trợ tên miền riêng. | 08/06/2026 | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html |
| **5** | Chạy **cdk synth** và **cdk diff** để kiểm tra template CloudFormation được tạo ra và xem trước các thay đổi của hạ tầng trước khi triển khai. Đề xuất quy trình GitHub Actions CI/CD tối thiểu gồm ba bước **lint**, **build** và **test**. | 09/06/2026 | https://docs.github.com/en/actions |

### Phối hợp nhóm:
- Phân công mỗi thành viên phụ trách đánh giá một trụ cột của AWS Well-Architected Framework, sau đó tổng hợp thành một báo cáo đánh giá chung cho toàn dự án.
- Thảo luận và thống nhất quy trình CI/CD đề xuất để đảm bảo tất cả thành viên sử dụng cùng một quy trình phát triển và triển khai.

### Kết quả đạt được:
- Hoàn thành báo cáo đánh giá theo AWS Well-Architected Framework.
- Hoàn thành checklist bảo mật của hệ thống.
- Hoàn thành danh sách các hạng mục cần cải thiện về Reliability.
- Đề xuất quy trình GitHub Actions CI/CD tối thiểu.

### Tự đánh giá:
- Dự án đã đủ an toàn để triển khai trên môi trường Production hay chưa?
- Kịch bản sự cố nghiêm trọng nhất có thể xảy ra trong kiến trúc hiện tại là gì?