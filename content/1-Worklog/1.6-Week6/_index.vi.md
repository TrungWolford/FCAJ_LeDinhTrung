---
title: "Worklog Tuần 6"
date: 2026-07-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:
- Tự động hóa việc khởi tạo và cập nhật hạ tầng đám mây bằng công cụ AWS CDK (Cloud Development Kit) sử dụng ngôn ngữ C#.
- Khai báo định nghĩa mã nguồn cho toàn bộ tài nguyên: Cognito, DynamoDB, Lambda, API Gateway, S3 và CloudWatch.
- Thiết kế phân rã hạ tầng thành nhiều Stack nhỏ độc lập để tăng tính dễ bảo trì và cập nhật.
- Thực hành và làm quen với vòng đời triển khai hạ tầng: `cdk synth`, `cdk deploy` và `cdk destroy`.

### Các công việc triển khai:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Cài đặt AWS CDK CLI, khởi tạo project C# CDK mới và tìm hiểu các khái niệm Constructs, Stacks, App | 27/07/2026 | 27/07/2026 | AWS CDK Getting Started |
| 3 | Lập trình khai báo hạ tầng lưu trữ (S3 bucket, DynamoDB tables) và thiết lập chỉ mục GSIs | 28/07/2026 | 28/07/2026 | AWS CDK Database Construct |
| 4 | Định nghĩa tài nguyên Cognito User Pool, App Client và các thiết lập xác thực người dùng | 29/07/2026 | 29/07/2026 | AWS CDK Cognito Construct |
| 5 | Viết code Stack chứa Lambda Functions, cấp quyền IAM Role tối thiểu (Read/Write DynamoDB, Invoke Bedrock) | 30/07/2026 | 30/07/2026 | AWS CDK IAM & Lambda |
| 6 | Định nghĩa Stack API Gateway để phơi bày các endpoint RESTful và gắn Cognito Authorizers | 31/07/2026 | 31/07/2026 | AWS CDK API Gateway |
| 7 | Thực hành triển khai hệ thống: chạy `cdk synth` sinh mẫu CloudFormation, `cdk deploy` đẩy hạ tầng lên AWS, và `cdk destroy` để làm sạch môi trường | 01/08/2026 | 01/08/2026 | AWS CDK CLI Commands |

### Kết quả đạt được:
- Toàn bộ hạ tầng đám mây của dự án game được đặc tả bằng mã nguồn (Infrastructure as Code) viết bằng C#, loại bỏ hoàn toàn việc click chọn thủ công trên console.
- Tổ chức hạ tầng khoa học thành 4 Stacks riêng biệt: StorageStack, IdentityStack, ComputeStack và ApiGatewayStack.
- Thành thạo thao tác tự động hóa hệ thống bằng các dòng lệnh CDK, giảm thiểu tối đa sai sót khi nhân bản môi trường.
