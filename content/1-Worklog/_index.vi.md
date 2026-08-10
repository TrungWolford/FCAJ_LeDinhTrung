---
title: "Nhật ký công việc"
date: 2026-06-22
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

**Trong trang này**, bạn sẽ tìm thấy nhật ký công việc chi tiết hàng tuần mô tả các mục tiêu, nhiệm vụ và kết quả đạt được trong quá trình thực tập của tôi tại chương trình **First Cloud AI Journey (FCAJ)**.

Trong suốt lộ trình huấn luyện 6 tuần này, tôi đã tập trung xây dựng hạ tầng đám mây dạng mã nguồn (IaC), triển khai xác thực bảo mật người dùng, phát triển các API backend có khả năng mở rộng cho cơ chế game, đồng thời tích hợp trí tuệ nhân tạo tạo sinh (Generative AI) và tối ưu hóa hiệu năng máy chủ serverless.

Dưới đây là tóm tắt các dấu mốc theo từng tuần:

**Tuần 1:** [Hội nhập, Công cụ lập trình & Cơ bản về Đám mây](1.1-week1/)
Làm quen với lộ trình thực tập FCAJ, cài đặt các công cụ viết tài liệu và thiết kế (Hugo, Markdown, VS Code, draw.io), nghiên cứu hạ tầng toàn cầu của AWS.

**Tuần 2:** [Tài khoản AWS Free Tier, Bảo mật & Kiểm soát ngân sách](1.2-week2/)
Tạo lập tài khoản AWS cá nhân an toàn, kích hoạt mã tài trợ credit 200$, thao tác console và thiết lập AWS Budgets chống phát sinh chi phí ngoài mong muốn.

**Tuần 3:** [Lưu trữ tĩnh, Cơ sở dữ liệu & Quản trị qua dòng lệnh](1.3-week3/)
Triển khai hosting website tĩnh trên S3, thiết lập CSDL quan hệ RDS và NoSQL DynamoDB, theo dõi tài nguyên bằng CloudWatch Alarms và thao tác qua AWS CLI.

**Tuần 4:** [Tự động hóa hạ tầng (IaC) & Xác thực người chơi bằng Cognito](1.4-week4/)
Sử dụng AWS CDK (C#) để định nghĩa và deploy tài nguyên tự động, đồng bộ thư viện dùng chung với Unity client qua MSBuild, cấu hình Cognito và API đăng nhập tự động (Silent Login).

**Tuần 5:** [Thuật toán Loot vật phẩm & API quản lý kho đồ](1.5-week5/)
Thiết kế cấu hình vật phẩm game, lập trình thuật toán rơi đồ ngẫu nhiên có trọng số, xây dựng API quản lý giới hạn kho đồ bằng Lambda C# và cập nhật đồng bộ DynamoDB.

**Tuần 6:** [Tích hợp Generative AI cốt truyện game & Tối ưu hiệu năng Lambda](1.6-week6/)
Liên kết backend với Amazon Bedrock (Claude model) sinh cốt truyện nhập vai động, phân tích hiện tượng lag cold start của Lambda và tối ưu hóa bằng Native AOT kết hợp SnapStart.