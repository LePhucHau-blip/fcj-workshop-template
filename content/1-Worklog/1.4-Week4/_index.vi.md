---
title: "Nhật ký công việc Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

## Tuần 4: Lambda và API Gateway
**Thời gian: 08/05/2026 - 12/05/2026**

### Mục tiêu của tuần:
- Hiểu kiến trúc Backend Serverless của dự án.
- Hiểu cơ chế hoạt động của API Gateway REST API và Lambda Proxy Integration.

### Kiến thức AWS:
- AWS Lambda Runtime, Memory, Timeout.
- Lambda Cold Start.
- API Gateway REST API.
- CORS.
- Request Validation.
- Throttling.
- Lambda Log Retention.

### Công việc thực hiện:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| 1 | Đọc file `api-stack.ts` để tìm hiểu cấu hình API Gateway trong dự án | 08/05/2026 | https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html |
| 2 | Đọc file `backend/api-handler/src/index.ts` để tìm hiểu xử lý Backend | 09/05/2026 | Mã nguồn của Repository |
| 3 | Phân tích các Route: `upload`, `images`, `search`, `profile`, `admin` | 10/05/2026 | Mã nguồn của Repository |
| 4 | Thực hiện Build Backend và Infrastructure của dự án | 11/05/2026 | Mã nguồn của Repository |
| 5 | Tổng hợp danh sách các API Endpoint của hệ thống | 12/05/2026 | Tài liệu của Repository |

### Kết quả đạt được:
- Hoàn thành danh sách các API Endpoint của hệ thống.
- Hoàn thành tài liệu ghi chú về các Lambda Function:
  - Memory (Bộ nhớ).
  - Timeout (Thời gian chờ).
  - Responsibility (Trách nhiệm xử lý).
- Hiểu rõ vai trò của **API Handler Lambda** trong kiến trúc Backend Serverless của dự án.

### Tự đánh giá:
- API Handler hiện tại có đang đảm nhiệm quá nhiều chức năng hay không?
- Nếu hệ thống mở rộng, những Route nào nên được tách thành các Lambda Function riêng?