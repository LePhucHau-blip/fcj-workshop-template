---
title: "Nhật ký công việc Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

## Tuần 2: IAM, Cognito & Authentication
**Thời gian: 24/04/2026 - 28/04/2026**

### Mục tiêu tuần:
- Hiểu cách người dùng đăng ký, đăng nhập và được cấp quyền trong hệ thống.
- Hiểu vai trò của Amazon Cognito, IAM Role và IAM Policy trong việc bảo vệ tài nguyên AWS.

### Kiến thức AWS:
- IAM User, IAM Role và IAM Policy.
- Nguyên tắc cấp quyền tối thiểu (Least Privilege).
- Amazon Cognito User Pool.
- JWT Token: Access Token, ID Token và Refresh Token.
- Cognito Group dành cho người dùng và quản trị viên.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Tìm hiểu sự khác nhau giữa IAM User, IAM Role và IAM Policy. Đọc các ví dụ IAM Policy trong dự án, xác định action và resource được cấp quyền. Ghi chú những trường hợp quyền được cấp rộng hơn mức cần thiết theo nguyên tắc Least Privilege. | 24/04/2026 | https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html |
| **2** | Đọc **auth-stack.ts** để tìm hiểu cấu hình Cognito User Pool, bao gồm các thuộc tính bắt buộc, chính sách mật khẩu, MFA, User Pool Client, luồng xác thực, callback URL và Cognito Group dành cho admin và user. | 25/04/2026 | https://docs.aws.amazon.com/cognito/latest/developerguide/user-pools.html |
| **3** | Theo dõi toàn bộ luồng đăng ký và đăng nhập từ frontend đến backend. Xác định nơi lưu Access Token và ID Token, cách token được gửi trong các yêu cầu API và cách backend xác thực JWT trước khi xử lý các API yêu cầu đăng nhập. | 26/04/2026 | Repo code |
| **4** | Lập ma trận phân quyền bằng cách phân loại các route thành public, yêu cầu đăng nhập và chỉ dành cho quản trị viên. Kiểm tra middleware đã được áp dụng đúng hay chưa và ghi chú các route có nguy cơ thiếu kiểm soát quyền truy cập. | 27/04/2026 | Repo notes |
| **5** | Hoàn thiện checklist bảo mật cho hệ thống xác thực, bao gồm password policy, MFA, thời gian hết hạn của token và bảo vệ các route quản trị. Đề xuất các cải tiến như bật MFA hoặc giảm thời gian sống của token nếu cần thiết. | 28/04/2026 | Repo notes |

### Phối hợp nhóm:
- Thực hiện review chéo ma trận phân quyền để đảm bảo không bỏ sót bất kỳ route nào trong hệ thống.
- Thống nhất quy ước đặt tên cho các nhóm route gồm public, authenticated và administrator để toàn bộ nhóm sử dụng nhất quán.

### Kết quả đạt được:
- Hoàn thành bảng ma trận Authentication và Authorization.
- Hoàn thành tài liệu ghi chú về IAM và Cognito trong dự án.
- Hoàn thành checklist bảo mật cho hệ thống xác thực.

### Tự đánh giá:
- Dự án đã triển khai cơ chế phân quyền (Authorization) đúng và đầy đủ hay chưa?
- Các route dành cho quản trị viên đã đủ an toàn hay vẫn còn những rủi ro bảo mật cần cải thiện?