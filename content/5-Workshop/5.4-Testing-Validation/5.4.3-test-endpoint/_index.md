---
title : "Testing AWS Bedrock AI Story & Combat APIs"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.4.3 </b> "
---

#### Testing AI Dungeon Master & Combat Resolution

In this step, you will test generating real-time AI story choices via **AWS Bedrock** and resolving turn-based combat encounters.

---

#### 1. Start Story Session (`POST /story/start`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "characterId": "char-uuid-1234",
    "theme": "Dark Forest Crypt"
  }
  ```
- **Expected Response (200 OK):**
  ```json
  {
    "sessionId": "session-5566",
    "narrative": "You stand at the edge of the Whispering Woods. A rusted gate creaks open in front of an ancient crypt...",
    "choices": [
      "Light a torch and step inside",
      "Inspect the stone glyphs on the gate",
      "Cast a detection spell"
    ]
  }
  ```

---

#### 2. Execute Custom Story Action (`POST /story/action`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "sessionId": "session-5566",
    "playerAction": "I light my torch and call out into the darkness."
  }
  ```
- **Expected Response (200 OK):**
  ```json
  {
    "sessionId": "session-5566",
    "narrative": "Your flame illuminates damp stone walls. Red eyes gleam from the shadows as a Skeleton Warrior draws its blade!",
    "encounterTriggered": true,
    "bossId": "boss-skeleton-01"
  }
  ```

---

#### 3. Resolve Battle Action (`POST /battle/resolve`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "characterId": "char-uuid-1234",
    "bossId": "boss-skeleton-01",
    "action": "Holy Strike"
  }
  ```
- **Expected Response (200 OK):**
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
