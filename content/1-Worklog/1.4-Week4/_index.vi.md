---
title: "Worklog Tuần 4"
date: 2026-07-13
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:
- Tích hợp dịch vụ trí tuệ nhân tạo Amazon Bedrock để xây dựng tính năng người dẫn truyện tự động (AI Storyteller).
- Thiết kế và phát triển Module `PromptBuilder` kết hợp ngữ cảnh nhân vật, trang bị và lịch sử cốt truyện.
- Thiết kế cấu trúc JSON đầu ra cho mô hình AI và viết bộ phân tích cú pháp (Parser) trên Backend để kiểm soát dữ liệu trả về cho client.

### Các công việc triển khai:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Kích hoạt quyền truy cập mô hình AI trên Amazon Bedrock Console (chọn các dòng model Amazon Nova / Claude) | 13/07/2026 | 13/07/2026 | Amazon Bedrock User Guide |
| 3 | Lập trình module kết nối AWS SDK C# với Bedrock Client sử dụng API `InvokeModel` | 14/07/2026 | 14/07/2026 | AWS SDK for .NET - Bedrock |
| 4 | Xây dựng logic PromptBuilder để tạo System Prompt và User Prompt có cấu trúc | 15/07/2026 | 15/07/2026 | Prompt Engineering Guide |
| 5 | Định nghĩa cấu trúc JSON đầu ra yêu cầu AI trả về (bao gồm text cốt truyện, list choices, thông số quái vật) | 16/07/2026 | 16/07/2026 | Bedrock JSON Schema Setup |
| 6 | Lập trình Response Parser để chuyển đổi chuỗi text JSON nhận được thành các DTOs đối tượng C# | 17/07/2026 | 17/07/2026 | C# System.Text.Json Guide |
| 7 | Thực hiện kiểm thử tích hợp (Integration Test) cuộc gọi API Bedrock để đo lường chất lượng phản hồi và độ trễ | 18/07/2026 | 18/07/2026 | Bedrock API Reference |

### Kết quả đạt được:
- Kết nối thành công .NET Backend với mô hình AI trên Amazon Bedrock (`amazon.nova-pro-v1:0` hoặc `anthropic.claude-v3`).
- Hoàn thiện `PromptBuilder` có khả năng tự động gom thông tin level nhân vật, vũ khí đang đeo và lịch sử lựa chọn để gửi cho AI.
- Xử lý thành công việc phân tích cú pháp JSON trả về từ Bedrock, đảm bảo thông tin câu chuyện, 3 nút lựa chọn hành động và thông số chỉ số Boss được hiển thị chính xác lên giao diện Unity mà không bị lỗi cấu trúc chuỗi.
