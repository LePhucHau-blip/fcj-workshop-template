---
title: "Nhật ký công việc Tuần 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

## Tuần 3: Amazon S3 và Lưu trữ hình ảnh
**Thời gian: 01/05/2026 - 05/05/2026**

### Mục tiêu của tuần:
- Hiểu cách dự án lưu trữ hình ảnh gốc và hình ảnh đã qua xử lý.
- Hiểu cơ chế **Presigned URL** và các quy tắc quản lý vòng đời (Lifecycle Rules) trong Amazon S3.

### Kiến thức AWS:
- S3 Bucket.
- Thiết kế Object Key.
- Block Public Access.
- Server-side Encryption.
- Presigned PUT/GET URL.
- S3 Lifecycle: Standard, IA, Glacier.
- Cấu hình CORS trên S3.

### Công việc thực hiện:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| 1 | Đọc file `storage-stack.ts` để tìm hiểu cấu hình lưu trữ trong dự án | 01/05/2026 | Mã nguồn của Repository |
| 2 | Đọc Route tạo Presigned URL trong `api-handler` | 02/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/PresignedUrlUploadObject.html |
| 3 | Theo dõi luồng Upload hình ảnh từ Frontend đến S3 | 03/05/2026 | Mã nguồn của Repository |
| 4 | Ghi chú mục đích sử dụng của Raw Bucket và Processed Bucket | 04/05/2026 | Ghi chú của dự án |
| 5 | Hoàn thiện Sequence Diagram cho quá trình Upload hình ảnh và Checklist bảo mật S3 | 05/05/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html |

### Kết quả đạt được:
- Hoàn thành sơ đồ tuần tự (Sequence Diagram) cho quy trình Upload hình ảnh.
- Hoàn thành tài liệu ghi chú về bảo mật và tối ưu chi phí khi sử dụng S3.
- Hoàn thành Checklist kiểm tra:
  - Public Access (Quyền truy cập công khai).
  - Encryption (Mã hóa dữ liệu).
  - SSL/TLS.
  - Lifecycle Policy (Chính sách vòng đời dữ liệu).

### Tự đánh giá:
- Vì sao việc Upload trực tiếp lên S3 tốt hơn so với việc Upload thông qua Lambda?
- Chính sách Lifecycle hiện tại có phù hợp với dữ liệu hình ảnh của người dùng hay không?