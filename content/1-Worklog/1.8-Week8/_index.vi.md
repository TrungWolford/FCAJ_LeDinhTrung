---
title: "Worklog Tuần 8"
date: 2024-02-19
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Hiểu AWS messaging services: SQS, SNS, và SES.
* Tìm hiểu về các kiến trúc ứng dụng decoupled.
* Overstend xử lý dựa trên queue và các thiết kế event-driven.
* Khám phá các mô hình pub/sub và message filtering.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 1   | - Tìm hiểu SQS fundamentals (Standard vs FIFO) <br> - Hiểu message visibility timeout <br> - Khám phá queue attributes và permissions | 30/07/2026 | 30/07/2026 | AWS SQS User Guide |
| 2   | - Tạo và cấu hình SQS queues <br> - Gửi và nhận messages sử dụng SDK <br> - Triển khai message processing workers | 31/07/2026 | 31/07/2026 | AWS SQS Configuration |
| 3   | - Tìm hiểu SNS fundamentals và pub/sub pattern <br> - Tạo SNS topics và subscriptions <br> - Cấu hình message filtering | 01/08/2026 | 01/08/2026 | AWS SNS User Guide |
| 4-5 | - Tích hợp SNS với SQS cho fan-out pattern <br> - Thiết lập email notifications sử dụng SES <br> - Xây dựng event-driven application | 02/08/2026 | 03/08/2026 | AWS Messaging Patterns |

### Kết quả đạt được tuần 8:

* Hiểu được AWS messaging services cho việc xây dựng các ứng dụng decoupled.
* Tìm hiểu được SQS Standard queues và SQS FIFO.
* Tạo thành công SQS queues với các cấu hình phù hợp.
* Triển khai message visibility timeout để xử lý lỗi.
* Xây dựng các message processing workers để tiêu thụ messages.
* Tìm hiểu được SNS là dịch vụ pub/sub messaging được quản lý.
* Tạo SNS topics và cấu hình nhiều loại subscriptions.
* Triển khai message filtering để định tuyến messages.
* Thiết lập mô hình fan-out SNS-to-SQS.
* Cấu hình Amazon SES để gửi transactional emails.
* Xây dựng các ứng dụng event-driven sử dụng SNS và SQS.
* Triển khai dead-letter queues để xử lý messages bị lỗi.
* Tạo các kiến trúc ứng dụng có khả năng mở rộng, decoupled.

* Kết nối, làm quen với các thành viên trong First Cloud AI Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Làm quen với các thành viên FCAJ <br> - Đọc và lưu ý các nội quy, quy định tại đơn vị thực tập                                                                                             | 11/08/2025   | 11/08/2025      |
| 3   | - Tìm hiểu AWS và các loại dịch vụ <br>&emsp; + Compute <br>&emsp; + Storage <br>&emsp; + Networking <br>&emsp; + Database <br>&emsp; + ... <br>                                            | 12/08/2025   | 12/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tạo AWS Free Tier account <br> - Tìm hiểu AWS Console & AWS CLI <br> - **Thực hành:** <br>&emsp; + Tạo AWS account <br>&emsp; + Cài AWS CLI & cấu hình <br> &emsp; + Cách sử dụng AWS CLI | 13/08/2025   | 13/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 14/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 15/08/2025   | 15/08/2025      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 8:

* Hiểu AWS là gì và nắm được các nhóm dịch vụ cơ bản: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Đã tạo và cấu hình AWS Free Tier account thành công.

* Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web.

* Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:
  * Access Key
  * Secret Key
  * Region mặc định
  * ...

* Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  * Kiểm tra thông tin tài khoản & cấu hình
  * Lấy danh sách region
  * Xem dịch vụ EC2
  * Tạo và quản lý key pair
  * Kiểm tra thông tin dịch vụ đang chạy
  * ...

* Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
* ...


