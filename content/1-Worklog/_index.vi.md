---
title: "Nhật ký công việc"
date: 2026-06-22
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

**Trong trang này**, bạn sẽ tìm thấy nhật ký công việc chi tiết hàng tuần mô tả các mục tiêu, nhiệm vụ và kết quả đạt được trong quá trình thực tập của tôi tại chương trình **First Cloud AI Journey (FCAJ)**.

Lộ trình thực tập của tôi diễn ra trong vòng 2 tháng (8 tuần), tập trung vào các mốc thời gian sau:

**Tuần 1:** [Onboarding, Công cụ & Cơ bản về Đám mây](1.1-week1/) (22/06/2026 - 27/06/2026)  
Kết nối với các thành viên, làm quen với lộ trình thực tập 2 tháng và cài đặt các công cụ Hugo, Markdown, VS Code, draw.io. Nghiên cứu các khái niệm cơ bản về điện toán đám mây và tối ưu hóa chi phí AWS.

**Tuần 2:** [Khởi tạo & Bảo mật hạ tầng cơ bản](1.2-week2/) (29/06/2026 - 04/07/2026)  
Bật MFA cho Root account, tạo IAM user theo Least Privilege. Tìm hiểu S3 Bucket, cấu hình quyền truy cập và CORS. Cài đặt AWS CLI, làm quen với AWS CDK và tải tài nguyên game lên S3.

**Tuần 3:** [Xác thực Cognito & Cơ sở dữ liệu Game](1.3-week3/) (06/07/2026 - 11/07/2026)  
Tạo Cognito User Pool, lập trình các API Auth (Register, Login, RefreshToken) trên C# Backend kết nối Unity. Thiết kế cơ sở dữ liệu và triển khai DynamoDB Repository cho game.

**Tuần 4:** [Tích hợp Amazon Bedrock AI](1.4-week4/) (13/07/2026 - 18/07/2026)  
Kết nối C# với Bedrock AI, lập trình PromptBuilder và xử lý đầu ra JSON từ Bedrock sinh câu chuyện, lựa chọn hành động và bối cảnh Boss động.

**Tuần 5:** [Kiến trúc Serverless với Lambda & API Gateway](1.5-week5/) (20/07/2026 - 25/07/2026)  
Tách logic thành các Lambda functions, cấu hình API Gateway và tối ưu hóa RAM, Timeout cho Lambda thông qua dotnet publish.

**Tuần 6:** [Tự động hóa hạ tầng bằng AWS CDK](1.6-week6/) (27/07/2026 - 01/08/2026)  
Định nghĩa hạ tầng hoàn chỉnh bằng AWS CDK (C#), phân tách thành các Stack dễ quản lý, thực hành các lệnh `cdk deploy`, `cdk synth`, và `cdk destroy`.

**Tuần 7:** [Bảo mật, Giám sát & Tối ưu chi phí](1.7-week7/) (03/08/2026 - 08/08/2026)  
Chuyển thông tin nhạy cảm vào Environment Variables, cấu hình CloudWatch Dashboard & Alarms, phân tích chi phí với Cost Explorer.

**Tuần 8:** [Kiểm thử End-to-End & Bàn giao đồ án](1.8-week8/) (09/08/2026 - 15/08/2026)  
Kiểm thử tích hợp toàn bộ các tính năng game, đánh giá theo AWS Well-Architected Framework, hoàn thiện báo cáo và đóng gói mã nguồn.