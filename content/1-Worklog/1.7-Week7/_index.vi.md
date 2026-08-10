---
title: "Worklog Tuần 7"
date: 2024-02-12
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Hiểu Elastic Load Balancing và Auto Scaling cho high availability.
* Tìm hiểu về Application Load Balancer (ALB), Network Load Balancer (NLB), và Classic Load Balancer.
* Overstend EC2 Auto Scaling groups và scaling policies.
* Triển khai các kiến trúc ứng dụng có fault-tolerant và có khả năng mở rộng.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 1   | - Tìm hiểu Load Balancing fundamentals <br> - Hiểu ALB, NLB, và CLB khác biệt <br> - Khám phá health checks và routing | 23/07/2026 | 23/07/2026 | AWS Load Balancing User Guide |
| 2   | - Tạo Application Load Balancer <br> - Cấu hình target groups và listeners <br> - Thiết lập SSL/TLS certificates | 24/07/2026 | 24/07/2026 | AWS ALB Configuration |
| 3   | - Tìm hiểu Auto Scaling fundamentals <br> - Tạo launch templates và Auto Scaling groups <br> - Cấu hình scaling policies | 25/07/2026 | 25/07/2026 | AWS Auto Scaling Guide |
| 4-5 | - Thiết lập dynamic scaling policies (target tracking, step scaling) <br> - Tạo multi-AZ deployments <br> - Kiểm tra scaling và failover scenarios | 26/07/2026 | 27/07/2026 | AWS Scaling Best Practices |

### Kết quả đạt được tuần 7:

* Hiểu được Elastic Load Balancing và vai trò của nó trong phân phối lưu lượng truy cập.
* Tìm hiểu được các loại load balancer khác nhau và hiệu suất cao.
* Tạo thành công các Application Load Balancers với nhiều target groups.
* Cấu hình health checks để giám sát sức khỏe instance backend.
* Thiết lập SSL/TLS certificates cho giao tiếp HTTPS an toàn.
* Tạo launch templates với các cấu hình phù hợp cho khởi chạy instance nhất quán.
* Tạo EC2 Auto Scaling groups trên nhiều Availability Zones.
* Cấu hình target tracking scaling policies, step scaling policies.
* Kiểm tra các kịch bản scaling và failover scenarios.
* Triển khai các kiến trúc ứng dụng multi-tier với load balancing.
* Đạt được high availability và fault tolerance trong triển khai ứng dụng.

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


### Kết quả đạt được tuần 7:

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


