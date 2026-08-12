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
    "storyFileId": "chapter_1"
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "success": true,
    "message": "Success",
    "data": {
      "sessionId": "session-5566",
      "currentNodeId": "node_01",
      "currentLocation": "Dark Forest Crypt",
      "narrativeText": "Bạn đang đứng trước lối vào Khu Rừng Thầm Thì. Chiếc cổng sắt hoen gỉ kêu ken két dẫn vào một hầm mộ cổ...",
      "choices": [
        {
          "label": "Lựa chọn 1",
          "description": "Thắp đuốc và bước vào trong",
          "nextNodeId": "node_02"
        },
        {
          "label": "Lựa chọn 2",
          "description": "Kiểm tra các ký tự cổ trên cổng",
          "nextNodeId": "node_03"
        }
      ],
      "character": null,
      "triggerBattle": false,
      "bossId": null,
      "bossName": null,
      "bossLevel": null,
      "debugPrompt": null,
      "storyCompleted": false
    }
  }
  ```

---

#### 2. Gửi Hành động Chơi game (`POST /story/action`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "characterId": "char-uuid-1234",
    "sessionId": "session-5566",
    "playerInput": "Tôi thắp đuốc và hô to vào trong bóng tối."
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "success": true,
    "message": "Success",
    "data": {
      "sessionId": "session-5566",
      "currentNodeId": "node_02",
      "currentLocation": "Dark Forest Crypt",
      "narrativeText": "Ánh lửa thắp sáng những bức tường đá ẩm ướt. Đôi mắt đỏ rực lóe lên trong bóng tối khi một Chiến Binh Xương rút kiếm lao ra!",
      "choices": [],
      "character": null,
      "triggerBattle": true,
      "bossId": "boss-skeleton-01",
      "bossName": "Skeleton Warrior",
      "bossLevel": 1,
      "debugPrompt": null,
      "storyCompleted": false
    }
  }
  ```

---

#### 3. Xử lý Lượt Chiến đấu (`POST /battle/resolve`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "characterId": "char-uuid-1234",
    "encounterId": "encounter-8888",
    "equippedItemIds": [
      "item_rusty_sword"
    ]
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "success": true,
    "message": "Success",
    "data": {
      "battleId": "battle-uuid-9999",
      "encounterId": "encounter-8888",
      "isPlayerVictory": true,
      "playerPower": 150.0,
      "bossPower": 80.0,
      "battleScore": 70.0,
      "luckyEffects": [
        "Critical Hit"
      ],
      "turns": [
        {
          "attackerName": "Valerius",
          "logMessage": "Valerius gây 35 sát thương!",
          "damage": 35,
          "playerHpRemaining": 92,
          "bossHpRemaining": 0,
          "isCritical": true
        }
      ],
      "rewards": {
        "goldEarned": 50,
        "expEarned": 100,
        "lootItems": [
          {
            "itemId": "item-sun-pendant",
            "itemName": "Sun Pendant",
            "rarity": "Rare",
            "quantity": 1
          }
        ]
      },
      "updatedCharacter": {
        "characterId": "char-uuid-1234",
        "name": "Valerius the Paladin",
        "level": 2,
        "experience": 100,
        "hp": 92,
        "maxHp": 100,
        "attack": 10,
        "defense": 5,
        "criticalRate": 0.05,
        "luckyRate": 0.05,
        "gold": 100,
        "className": "Paladin",
        "status": "Alive",
        "currentLocationId": "spawn_village"
      }
    }
  }
  ```
