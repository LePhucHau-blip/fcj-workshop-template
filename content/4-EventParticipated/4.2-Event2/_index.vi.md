---
title: "Sự kiện 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo tổng kết: "Cuộc thi Kiến thức AWS & Các buổi Chia sẻ Kỹ thuật"

## Thông tin chung

- **Tên sự kiện:** Chưa xác định (sẽ cập nhật sau)
- **Thời gian:** Sẽ cập nhật sau
- **Địa điểm:** Sẽ cập nhật sau
- **Vai trò:** Người tham dự

## Nội dung trình bày và điểm nổi bật

### 1. Vòng chung kết cuộc thi tìm hiểu kiến thức về các dịch vụ AWS

**Người dẫn chương trình:** Anh Long

**Nội dung:** Chương trình mở đầu bằng vòng chung kết cuộc thi kiểm tra kiến thức về các dịch vụ của AWS. Những thí sinh vượt qua các vòng trước đã tham gia tranh tài bằng cách trả lời các câu hỏi liên quan đến những khái niệm cốt lõi của AWS, các trường hợp sử dụng dịch vụ và những thực tiễn tốt nhất khi triển khai trên nền tảng đám mây. Hình thức thi đấu tạo không khí sôi động, thu hút sự tham gia của khán giả và giúp củng cố kiến thức AWS theo hướng thực tiễn thay vì chỉ ghi nhớ lý thuyết. Trong suốt chương trình, anh Long điều phối cuộc thi và giải thích thêm các khái niệm quan trọng khi cần thiết.

### 2. Giới thiệu và trình diễn AWS Security Agent

**Diễn giả:** Anh Thịnh

**Nội dung:** Bài trình bày giới thiệu **AWS Security Agent**, một dịch vụ bảo mật ứng dụng sử dụng AI nhằm hỗ trợ các nhóm phát triển phần mềm phát hiện và khắc phục lỗ hổng bảo mật nhanh hơn so với các công cụ truyền thống. Diễn giả giải thích rằng dịch vụ này không chỉ dừng lại ở việc phân tích mã nguồn theo mẫu (pattern matching), mà còn có khả năng phân tích kiến trúc hệ thống, ranh giới tin cậy (trust boundaries) và luồng dữ liệu để phát hiện các lỗ hổng bảo mật ở mức thiết kế mà các công cụ quét thông thường thường bỏ sót.

Phần trình diễn giới thiệu các tính năng chính của dịch vụ, bao gồm:

- **Rà soát toàn bộ mã nguồn (Full Repository Code Review):** Quét toàn bộ kho mã nguồn được kết nối từ GitHub, GitLab hoặc Bitbucket, sau đó đưa ra các cảnh báo gắn với từng tệp và dòng mã cụ thể, đồng thời đánh giá mức độ nghiêm trọng và độ tin cậy của từng lỗ hổng.
- **Khắc phục lỗ hổng tự động (Automated Remediation):** AI tự động tạo bản vá cho các vấn đề đã phát hiện. Đối với kho mã nguồn riêng tư, hệ thống có thể tạo Pull Request trực tiếp; đối với kho công khai, hệ thống cung cấp tệp diff để tránh công khai lỗ hổng trước khi được khắc phục.
- **Phân tích mô hình đe dọa (Threat Modeling):** Phân tích tài liệu thiết kế hoặc mã nguồn để xác định các mối đe dọa bảo mật và đề xuất biện pháp giảm thiểu dựa trên mô hình STRIDE.
- **Kiểm thử xâm nhập (Penetration Testing):** Cho phép nhóm phát triển xác minh các lỗ hổng và tạo mã khai thác (exploit) trực tiếp thông qua CLI trước khi triển khai ứng dụng lên môi trường thực tế.
- **Tích hợp với IDE và quy trình phát triển:** Hỗ trợ thực hiện quét bảo mật và khắc phục lỗi trực tiếp từ môi trường phát triển thông qua Kiro, plugin Claude Code hoặc giao thức MCP mở, giúp lập trình viên không cần chuyển đổi giữa nhiều công cụ khác nhau.

Diễn giả cũng nhấn mạnh rằng AWS Security Agent không nhằm thay thế đội ngũ bảo mật mà đóng vai trò hỗ trợ bằng cách tự động phát hiện và xử lý những vấn đề phổ biến, giúp các chuyên gia bảo mật tập trung nhiều hơn vào các quyết định liên quan đến thiết kế và kiến trúc hệ thống.

### 3. Tổng quan về Amazon CloudWatch

**Nội dung:** Phần trình bày cuối cùng giới thiệu **Amazon CloudWatch**, dịch vụ giám sát và quan sát hệ thống (Monitoring & Observability) của AWS. Diễn giả giải thích cách CloudWatch thu thập các chỉ số (Metrics), nhật ký (Logs) và sự kiện (Events) từ các tài nguyên AWS cũng như ứng dụng, giúp người dùng theo dõi tình trạng hệ thống thông qua Dashboard trực quan, thiết lập cảnh báo khi có dấu hiệu bất thường và hỗ trợ xử lý sự cố gần như theo thời gian thực.

Ngoài việc giám sát hạ tầng như máy chủ tính toán, lưu trữ và mạng, CloudWatch còn hỗ trợ quan sát hoạt động của ứng dụng, bao gồm theo dõi **Service Level Objectives (SLOs)** để xác định, giám sát và cảnh báo khi các mục tiêu về độ tin cậy của hệ thống không được đáp ứng. Diễn giả nhấn mạnh rằng CloudWatch là một trong những dịch vụ nền tảng quan trọng giúp duy trì khả năng quan sát hệ thống và chủ động phát hiện sự cố trước khi ảnh hưởng đến người dùng cuối.

## Kiến thức tiếp thu và kế hoạch áp dụng

### Kiến thức và tư duy mới:

- **Củng cố kiến thức AWS thông qua cuộc thi:** Hình thức thi đố vui giúp ghi nhớ và hiểu rõ hơn về các dịch vụ AWS trong thực tế, đồng thời xác định những nội dung cần tiếp tục ôn tập.
- **Bảo mật ứng dụng bằng AI:** Hiểu rõ hơn cách AWS Security Agent sử dụng AI để tự động phát hiện và khắc phục lỗ hổng bảo mật ở cấp độ kho mã nguồn, vượt xa phương pháp phân tích tĩnh truyền thống bằng cách xem xét kiến trúc và luồng dữ liệu.
- **Tích hợp bảo mật vào quy trình phát triển:** Nhận thức được cách các công cụ bảo mật hiện đại có thể tích hợp trực tiếp vào IDE, CLI và quy trình CI/CD nhằm giảm thời gian xử lý và nâng cao hiệu quả phát triển phần mềm.
- **Nền tảng về Monitoring và Observability:** Hiểu rõ hơn vai trò của Amazon CloudWatch trong việc giám sát hệ thống, thiết lập cảnh báo và theo dõi độ tin cậy (SLOs) cho hạ tầng và ứng dụng trên nền tảng đám mây.

### Kế hoạch áp dụng:

- Ôn tập lại các dịch vụ AWS xuất hiện trong cuộc thi nhằm củng cố kiến thức nền tảng và bổ sung những nội dung còn thiếu.
- Thử nghiệm AWS Security Agent trên một dự án cá nhân hoặc môi trường thử nghiệm để tìm hiểu quy trình quét bảo mật và tự động khắc phục lỗ hổng.
- Xây dựng Dashboard và Alarm cơ bản bằng Amazon CloudWatch cho một dự án cá nhân nhằm thực hành các khái niệm về giám sát và cảnh báo.
- Tìm hiểu cách tích hợp các công cụ bảo mật và giám sát vào quy trình CI/CD để áp dụng trong các dự án phát triển phần mềm trong tương lai.

## Hình ảnh sự kiện

![Event photo 1](/images/4-eventparticipated/event2-1.jpg)

![Event photo 2](/images/4-eventparticipated/event2-2.jpg)

![Event photo 3](/images/4-eventparticipated/event2-3.jpg)
