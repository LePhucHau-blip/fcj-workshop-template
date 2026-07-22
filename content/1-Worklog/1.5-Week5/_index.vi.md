---
title: "Nhật ký công việc Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

## Tuần 5: Mô hình dữ liệu DynamoDB
**Thời gian: 15/05/2026 - 19/05/2026**

### Mục tiêu tuần:
- Hiểu mô hình Single-table Design được sử dụng trong dự án.
- Biết khi nào nên sử dụng Query, Scan và Global Secondary Index (GSI).

### Kiến thức AWS:
- Partition Key và Sort Key trong DynamoDB.
- So sánh Query và Scan.
- Global Secondary Index (GSI).
- Projection.
- Chế độ tính phí On-demand.

### Thực hành dự án:

| Ngày | Công việc | Thời gian | Tài liệu tham khảo |
|---|---|---|---|
| **1** | Đọc **database-stack.ts** để xác định Partition Key và Sort Key của bảng chính. Ghi chú các Global Secondary Index (GSI) đã được cấu hình, mục đích của từng GSI và kiểm tra bảng đang sử dụng chế độ tính phí On-demand hay Provisioned. | 15/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/UserGuide/HowItWorks.html |
| **2** | Phân tích các truy vấn trong **images.ts**, **search.ts** và **admin.ts**. Xác định truy vấn nào sử dụng Query hoặc Scan, đánh giá điều kiện lọc và ghi chú những truy vấn có nguy cơ ảnh hưởng đến hiệu năng khi dữ liệu tăng lên. | 16/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Query.html |
| **3** | Thiết kế và mô tả mô hình dữ liệu Single-table của dự án, bao gồm Image Metadata, Tag Item và Moderation Item. Ghi chú cấu trúc Partition Key (PK), Sort Key (SK), mối quan hệ giữa các thực thể và cách tổ chức dữ liệu trong bảng. | 17/05/2026 | Repo notes |
| **4** | Xác định các điểm cần tối ưu bằng cách phân tích chức năng Public Gallery hiện đang sử dụng Scan. Đánh giá ảnh hưởng của Scan đến hiệu năng và chi phí, đồng thời nghiên cứu cách sử dụng Global Secondary Index (GSI) để cải thiện tốc độ truy vấn. | 18/05/2026 | https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GSI.html |
| **5** | Hoàn thiện tài liệu mô hình dữ liệu DynamoDB, lập bảng Access Pattern cho từng chức năng của hệ thống và đề xuất thiết kế một Global Secondary Index (GSI) mới cho Public Gallery, bao gồm Partition Key và Sort Key phù hợp. | 19/05/2026 | Repo notes |

### Phối hợp nhóm:
- Thảo luận cùng nhóm để xác định những Access Pattern quan trọng nhất cần được ưu tiên tối ưu.
- Phối hợp với thành viên phụ trách module quản trị để rà soát các truy vấn trong **admin.ts** và đối chiếu với mô hình dữ liệu chung của dự án.

### Kết quả đạt được:
- Hoàn thành tài liệu mô hình dữ liệu DynamoDB.
- Hoàn thành bảng Access Pattern của hệ thống.
- Hoàn thành đề xuất Global Secondary Index (GSI) cho chức năng Public Gallery.

### Tự đánh giá:
- Mô hình Single-table Design mang lại những lợi ích gì cho dự án?
- Những Access Pattern nào vẫn chưa được thiết kế tối ưu và cần cải thiện?