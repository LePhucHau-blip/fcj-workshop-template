---
title: "Nhật ký công việc Tuần 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

## Tuần 1: Nền tảng AWS & Tổng quan dự án
**Thời gian: 17/04/2026 - 21/04/2026**

### Mục tiêu tuần:
- Nắm tổng quan về AWS Cloud Journey và mô hình bootcamp.
- Hiểu rõ bài toán mà dự án Smart Image Platform đang giải quyết.
- Xác định các dịch vụ AWS được sử dụng trong dự án và vai trò của từng dịch vụ.

### Kiến thức AWS:
- AWS Account, Region và Availability Zone.
- Kiến thức cơ bản về IAM (root account, IAM user và permission).
- Tổng quan về Amazon S3, AWS Lambda, API Gateway và DynamoDB.
- Khái niệm và lợi ích của kiến trúc serverless so với kiến trúc máy chủ truyền thống.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Đọc **README.md** và **README.vi.md** để hiểu mục tiêu, phạm vi và công nghệ sử dụng của dự án. Ghi chú các khái niệm chưa rõ như serverless, single-table design và presigned URL. Tìm hiểu cấu trúc thư mục của repository gồm frontend, backend và infrastructure. | 17/04/2026 | Repo README |
| **2** | Tìm hiểu hạ tầng toàn cầu của AWS gồm Region, Availability Zone và Edge Location. So sánh các yếu tố khi lựa chọn Region như độ trễ, chi phí và yêu cầu tuân thủ dữ liệu. Vẽ sơ đồ minh họa mối quan hệ giữa Region, AZ và Edge Location. | 18/04/2026 | https://aws.amazon.com/about-aws/global-infrastructure/ |
| **3** | Rà soát thư mục **infrastructure/lib/stacks**. Xác định các stack như storage, database, authentication, API, monitoring và frontend. Ghi chú mối quan hệ phụ thuộc giữa các stack và đánh dấu những phần chưa hiểu để trao đổi với mentor và nhóm. | 19/04/2026 | Repo code |
| **4** | Vẽ lại sơ đồ kiến trúc tổng thể của hệ thống từ frontend → API Gateway → Lambda → S3/DynamoDB → Rekognition. Mô tả luồng dữ liệu chính gồm upload ảnh, xử lý ảnh và tra cứu ảnh. Đối chiếu sơ đồ với tài liệu dự án để kiểm tra lại mức độ hiểu hệ thống. | 20/04/2026 | Repo docs |
| **5** | Lập bảng tổng hợp các dịch vụ AWS đang sử dụng trong dự án, mô tả vai trò và lý do lựa chọn của từng dịch vụ. Ghi chú những dịch vụ có thể tối ưu hoặc thay thế trong tương lai. Hoàn thiện tài liệu **week-01-project-overview.md**. | 21/04/2026 | Repo notes |

### Phối hợp nhóm:
- Họp nhóm đầu tuần để phân công mỗi thành viên nghiên cứu chuyên sâu từ một đến hai dịch vụ AWS trước khi chia sẻ lại với cả nhóm.
- Họp cuối tuần để đối chiếu sơ đồ kiến trúc của từng thành viên và thống nhất một sơ đồ kiến trúc chung cho dự án.

### Kết quả đạt được:
- Hoàn thành tài liệu **week-01-project-overview.md**.
- Hoàn thành sơ đồ kiến trúc tổng thể của Smart Image Platform.
- Hoàn thành bảng tổng hợp các dịch vụ AWS và vai trò của từng dịch vụ trong hệ thống.

### Tự đánh giá:
- Dự án này phù hợp với mô hình kiến trúc serverless ở những điểm nào?
- Thành phần nào của kiến trúc hệ thống mà mình vẫn chưa hiểu rõ và cần tìm hiểu thêm trong tuần tiếp theo?