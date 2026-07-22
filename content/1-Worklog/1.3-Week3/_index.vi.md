---
title: "Nhật ký công việc Tuần 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

## Tuần 3: Amazon S3 & Lưu trữ hình ảnh
**Thời gian: 01/05/2026 - 05/05/2026**

### Mục tiêu tuần:
- Hiểu cách dự án lưu trữ ảnh gốc và ảnh đã xử lý.
- Hiểu cơ chế hoạt động của Presigned URL và Lifecycle Rule trong Amazon S3.

### Kiến thức AWS:
- Amazon S3 Bucket và thiết kế Object Key.
- Block Public Access.
- Server-Side Encryption.
- Presigned PUT và GET URL.
- Amazon S3 Lifecycle (Standard, Standard-IA, Glacier).
- Cấu hình CORS trên Amazon S3.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Đọc **storage-stack.ts** để xác định các bucket được tạo trong dự án, bao gồm bucket lưu ảnh gốc và bucket lưu ảnh đã xử lý. Kiểm tra cấu hình Block Public Access, Server-Side Encryption, Versioning và CORS của từng bucket. | 01/05/2026 | Repo code |
| **2** | Đọc route trong **api-handler** chịu trách nhiệm tạo Presigned PUT URL. Ghi chú thời gian hết hạn của URL, các điều kiện upload như loại tệp và kích thước tệp, đồng thời so sánh việc upload trực tiếp lên Amazon S3 với upload thông qua AWS Lambda. | 02/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/PresignedUrlUploadObject.html |
| **3** | Theo dõi toàn bộ quy trình upload ảnh từ frontend, bao gồm chọn ảnh, gọi API lấy Presigned URL, upload trực tiếp lên Amazon S3 và cập nhật trạng thái upload. Quan sát cách hệ thống xử lý lỗi và hiển thị tiến trình upload trên giao diện người dùng. | 03/05/2026 | Repo code |
| **4** | Ghi chú vai trò của bucket lưu ảnh gốc (raw bucket) và bucket lưu ảnh đã xử lý (processed bucket). Kiểm tra quy tắc đặt tên Object Key, cách lưu trữ ảnh và cơ chế dọn dẹp ảnh gốc sau khi xử lý nếu có. | 04/05/2026 | Repo notes |
| **5** | Hoàn thiện sơ đồ tuần tự (Sequence Diagram) cho quy trình upload ảnh và checklist bảo mật Amazon S3, bao gồm Block Public Access, Server-Side Encryption, SSL-only và Lifecycle Policy. Đề xuất chính sách Lifecycle phù hợp hơn cho các ảnh ít được truy cập. | 05/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html |

### Phối hợp nhóm:
- Trao đổi với thành viên phụ trách frontend để hiểu chính xác cách giao diện người dùng lấy Presigned URL trước khi upload ảnh.
- Cùng các thành viên trong nhóm rà soát checklist bảo mật Amazon S3, mỗi người kiểm tra một nhóm cấu hình rồi tổng hợp thành tài liệu hoàn chỉnh.

### Kết quả đạt được:
- Hoàn thành sơ đồ tuần tự cho quy trình upload ảnh.
- Hoàn thành tài liệu ghi chú về bảo mật và tối ưu chi phí Amazon S3.
- Hoàn thành checklist gồm Block Public Access, Encryption, SSL và Lifecycle Policy.

### Tự đánh giá:
- Vì sao upload trực tiếp lên Amazon S3 hiệu quả hơn so với upload thông qua AWS Lambda?
- Chính sách Lifecycle hiện tại đã phù hợp với dữ liệu hình ảnh của người dùng hay vẫn còn có thể tối ưu thêm?