---
title: "Nhật ký công việc Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

## Tuần 2: IAM, Cognito và Cơ chế xác thực
**Thời gian: 24/04/2026 - 28/04/2026**

### Mục tiêu của tuần:
- Hiểu cách người dùng đăng ký tài khoản, đăng nhập và được cấp quyền truy cập vào hệ thống.
- Hiểu vai trò của Amazon Cognito, IAM Role và IAM Policy trong việc quản lý xác thực và phân quyền.

### Kiến thức AWS:
- IAM User, IAM Role, IAM Policy.
- Nguyên tắc **Least Privilege** (Cấp quyền tối thiểu cần thiết).
- Amazon Cognito User Pool.
- JWT Token, Access Token, ID Token.
- Cognito Group: Admin, User.

### Công việc thực hiện:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| 1 | Tìm hiểu về IAM User, IAM Role, IAM Policy và nguyên tắc cấp quyền tối thiểu | 24/04/2026 | https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html |
| 2 | Đọc file `auth-stack.ts`, tìm hiểu cấu hình Cognito User Pool trong dự án | 25/04/2026 | https://docs.aws.amazon.com/cognito/latest/developerguide/user-pools.html |
| 3 | Kiểm tra luồng đăng nhập/đăng ký từ Frontend đến Backend | 26/04/2026 | Mã nguồn của Repository |
| 4 | Ghi chú các Route công khai, Route yêu cầu xác thực và Route yêu cầu quyền Admin | 27/04/2026 | Ghi chú của dự án |
| 5 | Hoàn thiện danh sách kiểm tra bảo mật cho cơ chế xác thực hiện tại | 28/04/2026 | Ghi chú của dự án |

### Kết quả đạt được:
- Hoàn thành bảng phân tích ma trận xác thực và phân quyền (Authentication/Authorization Matrix).
- Hoàn thành tài liệu ghi chú về IAM và Cognito trong dự án.
- Hoàn thành danh sách kiểm tra bảo mật của hệ thống xác thực hiện tại.

### Tự đánh giá:
- Dự án đã triển khai cơ chế phân quyền một cách chính xác và an toàn chưa?
- Các Route dành cho Admin đã được bảo vệ đủ tốt chưa?