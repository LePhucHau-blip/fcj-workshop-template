---
title: "Nhật ký công việc Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

## Tuần 5: Thiết kế dữ liệu với DynamoDB
**Thời gian: 15/05/2026 - 19/05/2026**

### Mục tiêu của tuần:
- Hiểu mô hình **Single-table Design** được sử dụng trong dự án.
- Hiểu khi nào nên sử dụng **Query**, **Scan** và **GSI** trong DynamoDB.

### Kiến thức AWS:
- DynamoDB Partition Key, Sort Key.
- Query và Scan.
- Global Secondary Index (GSI).
- Projection.
- On-demand Billing.

### Công việc thực hiện:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| 1 | Đọc file `database-stack.ts` để tìm hiểu cấu trúc Database trong dự án | 15/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/UserGuide/HowItWorks.html |
| 2 | Đọc và phân tích các câu truy vấn trong `images.ts`, `search.ts`, `admin.ts` | 16/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Query.html |
| 3 | Vẽ mô hình dữ liệu cho các thành phần: Image Metadata, Tag Item, Moderation Item | 17/05/2026 | Ghi chú của dự án |
| 4 | Xác định các điểm cần tối ưu: Public Gallery hiện tại đang sử dụng Scan | 18/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GSI.html |
| 5 | Hoàn thiện tài liệu mô hình dữ liệu và đề xuất GSI cho Public Gallery | 19/05/2026 | Ghi chú của dự án |

### Kết quả đạt được:
- Hoàn thành tài liệu mô hình dữ liệu (Data Model Document).
- Hoàn thành bảng phân tích các mẫu truy cập dữ liệu (Access Pattern Table).
- Đề xuất thiết kế GSI cho chức năng Public Gallery nhằm cải thiện hiệu năng truy vấn.

### Tự đánh giá:
- Mô hình **Single-table Design** mang lại những lợi ích gì cho hệ thống?
- Mẫu truy cập dữ liệu nào trong hệ thống hiện tại chưa được thiết kế tối ưu?