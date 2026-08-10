---
title: "Worklog Tuần 4"
date: 2026-07-13
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* **Thiết lập hạ tầng mã nguồn (IaC):** Sử dụng AWS CDK trên nền tảng C# (.NET 8) để tự động hóa định nghĩa và cấu hình toàn bộ hạ tầng đám mây (Amazon API Gateway, AWS Lambda, Amazon DynamoDB, Amazon Cognito).
* **Mô hình Thư viện dùng chung:** Tạo thư viện `GameShared.dll` (chuẩn .NET Standard 2.1) chứa Data Models và DTOs; thiết lập luồng MSBuild PostBuild Event tự động đồng bộ file .dll sang Unity Client nhằm chống sai lệch kiểu dữ liệu.
* **Module Xác thực (Authentication System):** Tích hợp dịch vụ Amazon Cognito để xử lý quy trình đăng ký/đăng nhập, xác thực tài khoản qua Email OTP nhằm tối ưu chi phí vận hành.
* **Quản lý phiên đăng nhập:** Lập trình API Silent Login cho phép tự động khôi phục phiên hoạt động bằng Refresh Token, giúp người chơi không cần nhập lại mật khẩu khi mở lại ứng dụng.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Khởi tạo dự án AWS CDK bằng C# và .NET 8 <br> - Định nghĩa các tài nguyên cơ bản như DynamoDB table và Cognito User Pool | 13/07/2026 | 13/07/2026 | Tài liệu AWS CDK C# |
| 3 | - Xây dựng CDK stack liên kết API Gateway với các Lambda handler phục vụ game client | 14/07/2026 | 14/07/2026 | Tài liệu API Gateway Integration |
| 4 | - Khởi tạo project class library `GameShared` (.NET Standard 2.1) <br> - Viết các class mô hình hóa vật phẩm và DTOs dùng chung | 15/07/2026 | 15/07/2026 | Tài liệu .NET Standard |
| 5 | - Cấu hình thẻ MSBuild PostBuild Event trong backend project để tự động copy file .dll sang folder Client của Unity | 16/07/2026 | 16/07/2026 | Tài liệu MSBuild Tasks |
| 6 | - Tích hợp SDK Cognito vào Lambda C# <br> - Lập trình luồng đăng ký, đăng nhập và xác thực qua mã OTP được gửi về Email | 17/07/2026 | 17/07/2026 | AWS Cognito SDK .NET |
| 7 | - Xây dựng API Silent Login, sử dụng Refresh Token để lấy Access Token và ID Token mới <br> - Kiểm thử luồng đăng nhập tự động | 18/07/2026 | 18/07/2026 | Hướng dẫn Cognito Token Refresh |

### Kết quả đạt được tuần 4:

* **Tự động hóa hạ tầng đám mây:** Triển khai hạ tầng dưới dạng code (IaC) thông qua AWS CDK. Toàn bộ tài nguyên backend được định nghĩa tập trung bằng C# giúp dễ dàng theo dõi và tái sử dụng hạ tầng.
* **Đồng bộ hóa dữ liệu Front-Backend:** Xây dựng thành công cơ chế chia sẻ thư viện `GameShared.dll`. Nhờ MSBuild PostBuild Event, mỗi lần backend compile thì client Unity tự động nhận được DLL mới nhất, triệt tiêu lỗi không khớp kiểu dữ liệu.
* **Hệ thống Auth bảo mật cao:** Thiết lập thành công Cognito User Pool quản lý đăng ký/đăng nhập của người chơi. Cấp phát bộ ba token chuẩn (Access, ID, Refresh Token) để phân quyền API.
* **Tối ưu chi phí gửi mã xác thực:** Tích hợp thành công Email OTP mặc định của Cognito để gửi mã xác nhận tài khoản, loại bỏ nhu cầu sử dụng các cổng dịch vụ SMS đắt đỏ.
* **Nâng cao trải nghiệm người chơi:** Hoàn thành API Silent Login giúp game client tự động khôi phục session bằng Refresh Token, tăng tính liền mạch khi người chơi tắt/mở lại game.
