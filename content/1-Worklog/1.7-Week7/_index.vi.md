---
title: "Worklog Tuần 7"
date: 2026-08-03
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:
- Đảm bảo an toàn bảo mật hệ thống bằng cách chuyển thông tin nhạy cảm khỏi mã nguồn và rà soát quyền hạn IAM.
- Thiết lập hệ thống giám sát thời gian thực với Amazon CloudWatch Dashboards và Alarms.
- Quản lý và kiểm soát ngân sách vận hành bằng AWS Cost Explorer, dọn dẹp các tài nguyên không sử dụng.

### Các công việc triển khai:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Loại bỏ các chuỗi cấu hình cứng nhạy cảm (như Client IDs, Table Names) đưa vào Environment Variables của Lambda | 03/08/2026 | 03/08/2026 | AWS Lambda Env Variables |
| 3 | Rà soát và cấu hình chặt chẽ IAM Roles cho từng hàm Lambda, đảm bảo tính biệt lập quyền truy xuất | 04/08/2026 | 04/08/2026 | AWS IAM Policies Review |
| 4 | Cấu hình Amazon CloudWatch Logs để thu thập lỗi và vết ghi nhận từ code Lambda | 05/08/2026 | 05/08/2026 | CloudWatch Logs Guide |
| 5 | Tạo CloudWatch Dashboard tùy chỉnh để theo dõi các chỉ số quan trọng (Lambda Duration, Errors, Throttles) | 06/08/2026 | 06/08/2026 | CloudWatch Dashboards Setup |
| 6 | Cấu hình CloudWatch Alarms gửi cảnh báo email khi Lambda lỗi đột biến hoặc chi phí vượt ngưỡng | 07/08/2026 | 07/08/2026 | CloudWatch Alarms Guide |
| 7 | Sử dụng AWS Cost Explorer để phân tích báo cáo chi tiêu, phát hiện và xóa bỏ các tài nguyên dư thừa gây tốn phí | 08/08/2026 | 08/08/2026 | AWS Cost Explorer Guide |

### Kết quả đạt được:
- Bảo mật hệ thống được cải thiện rõ rệt, bảo vệ các thông tin kết nối và định danh thông qua các tham số môi trường động.
- Hệ thống giám sát vận hành được tự động hóa. Có bảng điều khiển (Dashboard) trực quan giúp theo dõi hiệu năng hệ thống API.
- Tối ưu hóa hóa đơn chi tiêu AWS, đảm bảo các tài nguyên thử nghiệm được quản lý chặt chẽ và không phát sinh hóa đơn ngoài ý muốn.
