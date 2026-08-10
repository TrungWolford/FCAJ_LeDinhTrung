---
title: "Worklog Tuần 5"
date: 2026-07-20
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* **Hệ thống Vật phẩm & Loot đồ:** Thiết kế mô hình dữ liệu chi tiết cho các nhóm vật phẩm game (Weapon, Armor, Accessory, Consumable) được phân theo 4 cấp độ hiếm.
* **Thuật toán rớt đồ:** Viết mã thuật toán xác suất rơi vật phẩm có trọng số và công thức tự động điều chỉnh lượng Vàng/Kinh nghiệm theo cấp độ của quái/Boss.
* **Backend API Kho đồ:** Xây dựng các hàm AWS Lambda xử lý các quy tắc ràng buộc số lượng kho đồ (tối đa 100 ô/nhân vật).
* **Logic Trang bị/Gỡ trang bị:** Lập trình logic thay đổi trang bị nhân vật, tính toán lại các chỉ số nhân vật (Stats) theo thời gian thực và cập nhật dữ liệu vào DB.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày kết thúc | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Thiết kế các class vật phẩm (Weapon, Armor, Accessory, Consumable) trong dự án `GameShared` <br> - Thêm định nghĩa Enum độ hiếm (Common, Rare, Epic, Legendary) | 20/07/2026 | 20/07/2026 | Lý thuyết thiết kế game RPG |
| 3 | - Lập trình thuật toán rớt đồ có trọng số (Weighted Random Algorithm) bằng C# <br> - Viết logic tính toán Gold/XP thưởng theo cấp độ Boss | 21/07/2026 | 21/07/2026 | Thuật toán phân bổ ngẫu nhiên |
| 4 | - Xây dựng Lambda API bằng C# xử lý thao tác lấy danh sách túi đồ <br> - Viết code check giới hạn sức chứa kho đồ (Capacity Check tối đa 100 ô) | 22/07/2026 | 22/07/2026 | Lập trình AWS Lambda với C# |
| 5 | - Phát triển API xử lý Logic Trang bị (Equip) và Gỡ trang bị (Unequip) <br> - Thiết lập các ràng buộc logic: 1 vị trí (slot) chỉ được mang tối đa 1 item | 23/07/2026 | 23/07/2026 | Mẫu thiết kế logic nghiệp vụ |
| 6 | - Viết hàm tự động cộng/trừ các chỉ số nhân vật (Strength, Defense, HP, v.v.) dựa trên thông số cộng thêm của trang bị vừa mặc/gỡ | 24/07/2026 | 24/07/2026 | Công thức tính toán chỉ số game |
| 7 | - Liên kết API kho đồ với Amazon DynamoDB để cập nhật thông tin túi đồ và chỉ số nhân vật một cách đồng thời, tránh xung đột dữ liệu | 25/07/2026 | 25/07/2026 | Giao dịch (Transactions) trên DynamoDB |

### Kết quả đạt được tuần 5:

* **Mô hình hóa dữ liệu vật phẩm:** Thiết kế thành công các cấu trúc class đại diện cho vật phẩm game, phân chia rõ ràng theo các nhóm chức năng và 4 cấp độ hiếm (Common, Rare, Epic, Legendary).
* **Thuật toán Loot hoạt động chính xác:** Hoàn thành thuật toán rơi vật phẩm có trọng số ngẫu nhiên. Lượng Vàng và XP nhận được tự động nhân theo hệ số cấp độ Boss, đảm bảo cân bằng game.
* **API Kho đồ hoàn chỉnh:** Xây dựng xong API kiểm tra giới hạn túi đồ. Hệ thống tự động ngăn chặn nhặt thêm vật phẩm khi túi đồ đã đầy 100 ô và trả về thông báo lỗi trực quan cho người chơi.
* **Logic trang bị chặt chẽ:** Hiện thực hóa thành công nghiệp vụ mặc/gỡ đồ. Đảm bảo đúng quy chuẩn game: khi mặc vũ khí mới, vũ khí cũ tự động chuyển về túi đồ chung, giải phóng slot.
* **Đồng bộ chỉ số nhân vật thời gian thực:** Các thuộc tính bổ trợ của trang bị (ví dụ: giáp cộng thêm từ áo giáp Epic) được cộng trực tiếp vào tổng chỉ số nhân vật thời gian thực và ghi nhận đồng bộ vào DynamoDB qua cơ chế Transaction.
