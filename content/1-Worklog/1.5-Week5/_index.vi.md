---
title: "Worklog Tuần 5"
date: 2026-07-20
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:
- Tách biệt logic nghiệp vụ C# .NET 8 thành các hàm xử lý nhỏ gọn chạy trên môi trường AWS Lambda.
- Cấu hình Amazon API Gateway làm cổng HTTP REST API tập trung, chịu trách nhiệm nhận yêu cầu từ Unity Client và định tuyến đến các Lambda tương ứng.
- Tối ưu hóa quá trình biên dịch và đóng gói ứng dụng (dotnet publish) để giảm thiểu kích thước package và thời gian khởi động lạnh (cold start) của Lambda.

### Các công việc triển khai:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Phân rã mã nguồn thành các module xử lý độc lập: Auth, Character, Inventory, Story, Battle | 20/07/2026 | 20/07/2026 | Serverless Architecture Guide |
| 3 | Lập trình các handler AWS Lambda tương ứng sử dụng thư viện `Amazon.Lambda.AspNetCoreServer` hoặc các Lambda Native Handlers | 21/07/2026 | 21/07/2026 | AWS Lambda .NET Programming |
| 4 | Cấu hình Amazon API Gateway làm cổng REST API, thiết lập CORS Rules và Cognito Authorizers | 22/07/2026 | 22/07/2026 | AWS API Gateway Guide |
| 5 | Tích hợp Route Mapping và Query/Body Parameter binding từ API Gateway sang các Lambda function | 23/07/2026 | 23/07/2026 | API Gateway Integrations |
| 6 | Sử dụng lệnh `dotnet publish` kết hợp các cờ tối ưu hóa biên dịch để tạo tệp zip deploy | 24/07/2026 | 24/07/2026 | .NET CLI Publish Command |
| 7 | Tối ưu hóa dung lượng bộ nhớ RAM (Memory Size) và thời gian chờ (Timeout) cho từng Lambda tùy theo đặc thù tác vụ (ví dụ: Lambda xử lý AI cần timeout lớn hơn Lambda Auth) | 25/07/2026 | 25/07/2026 | Lambda Performance Tuning |

### Kết quả đạt được:
- Hệ thống backend .NET 8 được chia nhỏ thành 5 Lambda Functions riêng biệt vận hành độc lập, tăng tính mở rộng và khả năng chịu lỗi.
- API Gateway được cấu hình bảo mật với Cognito User Pool Authorizer, chặn mọi request không kèm token hợp lệ trước khi gửi tới Lambda.
- Đóng gói code thành công qua `dotnet publish` với cấu hình gọn nhẹ, giảm kích thước deploy package và tối ưu hóa thời gian chạy. Điều chỉnh RAM từ 256MB đến 1024MB tùy theo độ phức tạp của nghiệp vụ (Lambda xử lý AI/Bedrock cần tài nguyên lớn hơn).
