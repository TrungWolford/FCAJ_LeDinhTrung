---
title: "Worklog Tuần 3"
date: 2026-07-06
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* **S3 Static Hosting:** Tìm hiểu cách cấu hình lưu trữ đối tượng, phân quyền public và triển khai lưu trữ website tĩnh trên Amazon S3.
* **Cơ sở dữ liệu RDS:** Khởi tạo, cấu hình và kết nối ứng dụng với các hệ quản trị cơ sở dữ liệu quan hệ (MySQL/PostgreSQL) bằng Amazon RDS.
* **Cơ sở dữ liệu DynamoDB:** Khám phá kiến trúc NoSQL, cách tạo bảng, quản lý key (Partition Key/Sort Key) và thực hiện các thao tác CRUD cơ bản.
* **Giám sát hệ thống:** Cấu hình thu thập số liệu (Metrics), thiết lập cảnh báo (Alarms) và theo dõi log hệ thống của các tài nguyên AWS qua CloudWatch.
* **Quản trị qua Dòng lệnh:** Cài đặt, cấu hình bảo mật ứng dụng (AWS Configure) và thực thi các câu lệnh quản trị tài nguyên AWS trực tiếp từ Terminal/Command Prompt thông qua AWS CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tạo S3 bucket, cấu hình chính sách bucket (Bucket Policy) và CORS <br> - Upload file HTML/CSS để chạy thử website tĩnh | 06/07/2026 | 06/07/2026 | Hướng dẫn Hosting trên S3 |
| 3 | - Khởi tạo một RDS instance (MySQL hoặc PostgreSQL) <br> - Cấu hình Security Group bảo mật và kết nối thử qua client SQL (DBeaver) | 07/07/2026 | 07/07/2026 | Hướng dẫn sử dụng RDS |
| 4 | - Thiết kế bảng DynamoDB, chọn Partition Key và Sort Key phù hợp <br> - Viết kịch bản test CRUD dữ liệu trên DynamoDB console | 08/07/2026 | 08/07/2026 | Hướng dẫn DynamoDB |
| 5 | - Khám phá giao diện metrics của CloudWatch <br> - Tạo CloudWatch Alarm gửi mail qua SNS khi RDS CPU vượt quá ngưỡng | 09/07/2026 | 09/07/2026 | Tài liệu Amazon CloudWatch |
| 6 | - Tải và cài đặt công cụ AWS CLI trên máy cá nhân <br> - Chạy lệnh `aws configure` để liên kết thông tin IAM User Access Key | 10/07/2026 | 10/07/2026 | Hướng dẫn cài đặt AWS CLI |
| 7 | - Thực hành viết các câu lệnh CLI quản trị S3 bucket, start/stop RDS, và query dữ liệu DynamoDB | 11/07/2026 | 11/07/2026 | Tài liệu lệnh AWS CLI |

### Kết quả đạt được tuần 3:

* **Host website tĩnh thành công:** Hiểu cách hoạt động của Amazon S3. Biết cách phân quyền public, tắt chặn truy cập công cộng và tạo Bucket Policy cho phép người dùng bên ngoài đọc file (Read-Only).
* **Kết nối cơ sở dữ liệu quan hệ ổn định:** Triển khai được cơ sở dữ liệu PostgreSQL trên RDS. Nắm vững việc bảo mật tầng mạng bằng Security Group, chỉ cho phép kết nối đến từ IP máy cá nhân.
* **Nắm vững tư duy NoSQL:** Phân biệt được sự khác nhau giữa DynamoDB và RDBMS. Thiết kế bảng DynamoDB và thực hiện trơn tru các thao tác CRUD dữ liệu.
* **Thiết lập giám sát tự động:** Cấu hình thành công CloudWatch Alarms để theo dõi trạng thái tải của hệ thống, giúp phát hiện lỗi hoặc quá tải kịp thời.
* **Làm chủ dòng lệnh CLI:** Tiết kiệm thời gian quản trị AWS thông qua việc viết command-line thay vì click tay trên giao diện Console, cải thiện đáng kể tốc độ thao tác.
