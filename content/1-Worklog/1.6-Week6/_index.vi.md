---
title: "Worklog Tuần 6"
date: 2026-07-27
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* **Tích hợp Generative AI:** Kết nối Backend C# với dịch vụ Amazon Bedrock (Claude AI) để tự động hóa dẫn dắt cốt truyện game RPG linh hoạt theo tương tác của người chơi.
* **Giải quyết độ trễ Cold Start:** Phân tích và khắc phục hiện tượng đứng màn hình (freeze UI) trên client Unity do thời gian khởi động lạnh của .NET Lambda.
* **Native AOT & SnapStart:** Áp dụng công nghệ Native AOT cho các API nhẹ và cấu hình AWS Lambda SnapStart cho các API xử lý nặng.
* **Học hỏi công nghệ mới:** Tham gia sự kiện công nghệ Agent Force - Deepdive.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tích hợp SDK Amazon Bedrock vào Backend C# <br> - Viết system prompt định hình lối dẫn truyện RPG của Claude AI | 27/07/2026 | 27/07/2026 | Hướng dẫn Amazon Bedrock |
| 3 | - Thiết lập truyền tham số lựa chọn của người chơi vào Bedrock API <br> - Parse kết quả JSON trả về hiển thị lên giao diện Unity | 28/07/2026 | 28/07/2026 | Kỹ nghệ Prompt với Claude |
| 4 | - Đo đạc log Unity và CloudWatch Logs để cô lập nguyên nhân giật lag do Lambda khởi động lạnh | 29/07/2026 | 29/07/2026 | Tài liệu CloudWatch Logs |
| 5 | - Cấu hình Native AOT compile cho các API đọc nhanh (Get Profile, Inventory Check) và test tốc độ | 30/07/2026 | 30/07/2026 | Hướng dẫn Native AOT .NET |
| 6 | - Kích hoạt AWS Lambda SnapStart cho các API tính toán nặng (xử lý trận đấu, gọi Bedrock AI) | 31/07/2026 | 31/07/2026 | Tài liệu Lambda SnapStart |
| 7 | - Tham dự sự kiện Agent Force - Deepdive <br> - Tham gia các buổi thảo luận chuyên sâu về hệ thống Agent AI | 01/08/2026 | 01/08/2026 | Chương trình Event Agent Force |

### Kết quả đạt được tuần 6:

* **Tạo cốt truyện động bằng AI:** Tích hợp thành công Amazon Bedrock sử dụng mô hình Claude. Game có khả năng sinh các tình huống truyện và nhiệm vụ ngẫu nhiên dựa vào hành vi của người chơi một cách tự nhiên.
* **Tìm ra nguyên nhân lag:** Xác định hiện tượng giật màn hình 3-5 giây trên Unity là do thời gian khởi chạy (bootstrap runtime) của .NET CLR trên Lambda trong lần đầu gọi API (cold start).
* **Native AOT đạt hiệu năng cao:** Áp dụng thành công Native AOT cho các Lambda API đọc dữ liệu. Thời gian phản hồi cold start giảm đáng kể từ vài giây xuống chỉ còn 20-50ms, giúp trải nghiệm game mượt mà.
* **SnapStart tối ưu chi phí:** Cấu hình thành công SnapStart cho các Lambda API viết phức tạp. Việc sử dụng snapshot lưu sẵn trạng thái giúp loại bỏ độ trễ cold start mà không làm tăng chi phí hạ tầng (không cần dùng Provisioned Concurrency).
* **Mở rộng kiến thức AI Agent:** Tích lũy nhiều kiến thức giá trị về cách triển khai các hệ thống AI tự trị, mô hình Multi-Agent tại sự kiện Agent Force, hỗ trợ định hướng phát triển sản phẩm tiếp theo.
