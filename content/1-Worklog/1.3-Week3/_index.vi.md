---
title: "Worklog Tuần 3"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:
- Tích hợp dịch vụ xác thực người dùng sử dụng Amazon Cognito.
- Xây dựng API và giao diện Đăng ký / Xác nhận Đăng ký / Đăng nhập / Làm mới Token trên C# Backend và Unity.
- Thiết kế mô hình dữ liệu game NoSQL lưu trữ trạng thái người chơi và màn chơi.
- Khởi tạo Amazon DynamoDB và xây dựng các lớp xử lý dữ liệu (Repository) bằng C# .NET.

### Các công việc triển khai:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Khởi tạo Cognito User Pool, Client App cho game và thiết lập các thuộc tính người dùng | 06/07/2026 | 06/07/2026 | AWS Cognito Developer Guide |
| 3 | Lập trình logic các API Register, ConfirmSignUp, Login và RefreshToken trên Backend C# | 07/07/2026 | 07/07/2026 | AWS SDK for .NET - Cognito |
| 4 | Xây dựng UI đăng ký/đăng nhập trên Unity Client, tích hợp xử lý & lưu trữ JWT Token cục bộ | 08/07/2026 | 08/07/2026 | Unity WebRequest & Auth |
| 5 | Thiết kế cấu trúc bảng dữ liệu NoSQL gồm User, Character, Inventory, StorySession, Battle | 09/07/2026 | 09/07/2026 | DynamoDB Modeling Best Practices |
| 6 | Khởi tạo bảng dữ liệu DynamoDB, xác định Primary Key (Partition/Sort Keys) và GSI (Global Secondary Index) | 10/07/2026 | 10/07/2026 | Amazon DynamoDB Developer Guide |
| 7 | Viết các lớp Data Repository bằng C# để thực hiện đọc, ghi, cập nhật trạng thái game thời gian thực | 11/07/2026 | 11/07/2026 | AWS SDK for .NET - DynamoDB |

### Kết quả đạt được:
- Xây dựng thành công hệ thống Identity Provider qua Amazon Cognito. Game client có thể đăng ký tài khoản mới, xác nhận mã OTP, đăng nhập và lấy Access Token/ID Token/Refresh Token.
- Hoàn thiện mô hình dữ liệu Single-table design hoặc Multi-table design trên DynamoDB tối ưu chi phí và độ trễ.
- Triển khai xong mã nguồn CRUD trạng thái nhân vật và phiên chơi thông qua AWS SDK .NET DynamoDB Context.
