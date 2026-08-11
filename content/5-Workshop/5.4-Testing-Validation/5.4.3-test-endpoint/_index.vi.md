---
title : "Kiểm thử API Cốt truyện AI Bedrock & Trận đánh"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.4.3 </b> "
---

#### Kiểm thử "Dungeon Master AI" & Xử lý Giao tranh

Trong bước này, bạn sẽ kiểm thử khả năng sinh cốt truyện thời gian thực thông qua **AWS Bedrock** và tính toán kết quả trận đánh theo lượt (Turn-based combat).

---

#### 1. Khởi tạo Session Cốt truyện (`POST /story/start`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "characterId": "char-uuid-1234",
    "theme": "Dark Forest Crypt"
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "sessionId": "session-5566",
    "narrative": "Bạn đang đứng trước lối vào Khu Rừng Thầm Thì. Chiếc cổng sắt hoen gỉ kêu ken két dẫn vào một hầm mộ cổ...",
    "choices": [
      "Thắp đuốc và bước vào trong",
      "Kiểm tra các ký tự cổ trên cổng",
      "Dùng phép dò tìm năng lượng"
    ]
  }
  ```

---

#### 2. Gửi Hành động Chơi game (`POST /story/action`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "sessionId": "session-5566",
    "playerAction": "Tôi thắp đuốc và hô to vào trong bóng tối."
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "sessionId": "session-5566",
    "narrative": "Ánh lửa thắp sáng những bức tường đá ẩm ướt. Đôi mắt đỏ rực lóe lên trong bóng tối khi một Chiến Binh Xương rút kiếm lao ra!",
    "encounterTriggered": true,
    "bossId": "boss-skeleton-01"
  }
  ```

---

#### 3. Xử lý Lượt Chiến đấu (`POST /battle/resolve`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "characterId": "char-uuid-1234",
    "bossId": "boss-skeleton-01",
    "action": "Holy Strike"
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "playerDamageDealt": 35,
    "bossDamageDealt": 8,
    "characterCurrentHp": 92,
    "bossCurrentHp": 0,
    "isVictory": true,
    "lootDropped": [
      { "itemId": "item-sun-pendant", "name": "Sun Pendant", "type": "Accessory" }
    ]
  }
  ```
