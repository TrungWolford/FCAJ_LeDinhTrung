---
title: "Worklog Tuần 2"
date: 2026-06-29
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:
- Khởi tạo môi trường AWS an toàn và thiết lập các biện pháp bảo mật hạ tầng cơ bản.
- Tìm hiểu cấu hình lưu trữ tĩnh với Amazon S3, bao gồm thiết lập quyền truy cập và cấu hình CORS.
- Làm quen với giao diện dòng lệnh AWS CLI, kiến trúc Serverless, và bộ công cụ hạ tầng dạng mã nguồn AWS CDK (C#).
- Tải tài nguyên game ban đầu lên S3 bucket phục vụ phát triển game.

### Các công việc triển khai:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Kích hoạt MFA cho tài khoản Root AWS để bảo vệ tối đa quyền quản trị cao nhất | 29/06/2026 | 29/06/2026 | AWS MFA Setup Guide |
| 3 | Tạo các tài khoản IAM User/Role tuân thủ nguyên lý quyền tối thiểu (Least Privilege) | 30/06/2026 | 30/06/2026 | AWS IAM Best Practices |
| 4 | Cấu hình Amazon S3 Bucket lưu trữ tài nguyên game, thiết lập S3 Bucket Policy | 01/07/2026 | 01/07/2026 | Amazon S3 Developer Guide |
| 5 | Thiết lập CORS (Cross-Origin Resource Sharing) cho S3 để cho phép game client truy xuất | 02/07/2026 | 02/07/2026 | Amazon S3 CORS Guide |
| 6 | Cài đặt AWS CLI dưới máy cá nhân và thực hiện cấu hình Credentials | 03/07/2026 | 03/07/2026 | AWS CLI User Guide |
| 7 | Nghiên cứu tổng quan về Serverless, giới thiệu AWS CDK (C#) và tải tài nguyên game lên S3 | 04/07/2026 | 04/07/2026 | AWS CDK Intro / Game Assets |

### Kết quả đạt được:
- Tài khoản AWS root được bảo vệ an toàn bằng MFA. Không sử dụng tài khoản root cho tác vụ hàng ngày.
- Khởi tạo thành công S3 bucket chứa assets của game, cấu hình CORS hợp lệ để Unity Client có thể download trực tiếp tài nguyên qua HTTPS.
- Cài đặt và chạy thử thành công các lệnh kiểm tra cấu hình thông qua AWS CLI. Nắm vững tư duy thiết kế IaC cơ bản với AWS CDK.
