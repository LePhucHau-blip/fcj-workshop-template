---
title: "Nhật ký công việc Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

## Tuần 4: Lambda & API Gateway
**Thời gian: 08/05/2026 - 12/05/2026**

### Mục tiêu tuần:
- Hiểu kiến trúc backend serverless của dự án.
- Hiểu Amazon API Gateway REST API và cơ chế Lambda Proxy Integration.

### Kiến thức AWS:
- AWS Lambda Runtime, Memory và Timeout.
- Lambda Cold Start.
- Amazon API Gateway REST API.
- Cấu hình CORS.
- Request Validation.
- API Throttling.
- Lambda Log Retention.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Đọc **api-stack.ts** để xác định các resource và HTTP method được định nghĩa trong API Gateway. Kiểm tra cấu hình CORS, giới hạn tốc độ (throttling) và cấu hình triển khai của API Gateway. | 08/05/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html |
| **2** | Đọc **backend/api-handler/src/index.ts** để tìm hiểu cách Lambda Handler định tuyến request theo path và HTTP method. Kiểm tra các middleware dùng chung như xác thực, ghi log và xử lý lỗi. Đo thời gian Lambda Cold Start sau một khoảng thời gian không hoạt động. | 09/05/2026 | Repo code |
| **3** | Đọc các route **upload**, **images**, **search**, **profile** và **admin**. Ghi chú cấu trúc request, response của từng API và xác định route nào chứa nhiều logic nghiệp vụ phức tạp nhất. | 10/05/2026 | Repo code |
| **4** | Build backend và hạ tầng bằng cách chạy quá trình build của dự án và **cdk synth**. Ghi lại các lỗi cấu hình hoặc lỗi build (nếu có), tìm cách khắc phục và kiểm tra kích thước gói Lambda cũng như thời gian build. | 11/05/2026 | Repo code |
| **5** | Lập danh mục đầy đủ các API Endpoint bao gồm HTTP method, đường dẫn, mô tả chức năng và yêu cầu xác thực. Ghi chú cấu hình Memory, Timeout và trách nhiệm của từng Lambda Function trong hệ thống. | 12/05/2026 | Repo docs |

### Phối hợp nhóm:
- Phân chia các API route cho từng thành viên, mỗi người phụ trách phân tích từ hai đến ba route rồi tổng hợp thành danh mục API hoàn chỉnh.
- Thảo luận trong nhóm về những route nên được tách thành các Lambda Function riêng khi hệ thống mở rộng trong tương lai.

### Kết quả đạt được:
- Hoàn thành danh mục API Endpoint.
- Hoàn thành tài liệu mô tả các Lambda Function gồm Memory, Timeout và trách nhiệm của từng hàm.
- Hiểu rõ vai trò và trách nhiệm của API Handler Lambda trong kiến trúc serverless của dự án.

### Tự đánh giá:
- API Handler Lambda hiện tại có đang đảm nhiệm quá nhiều chức năng hay không?
- Những API route nào nên được tách thành các Lambda Function độc lập khi hệ thống mở rộng?