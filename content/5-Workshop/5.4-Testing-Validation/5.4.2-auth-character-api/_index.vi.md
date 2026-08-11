---
title : "Kiểm thử API Xác thực & Nhân vật"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.4.2 </b> "
---

#### Kiểm thử Xác thực & Khởi tạo Nhân vật

Trong bước này, bạn sẽ kiểm thử đăng ký, đăng nhập người dùng, lấy JWT token từ Amazon Cognito và tạo mới một nhân vật RPG.

---

#### 1. Đăng ký Tài khoản (`POST /auth/register`)

- **Request Body:**
  ```json
  {
    "username": "player1",
    "password": "Password123!",
    "email": "player1@example.com"
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "message": "User registered successfully. Please check your email for confirmation."
  }
  ```

---

#### 2. Đăng nhập Tài khoản (`POST /auth/login`)

- **Request Body:**
  ```json
  {
    "username": "player1",
    "password": "Password123!"
  }
  ```
- **Phản hồi mong đợi (200 OK):**
  ```json
  {
    "idToken": "eyJraWQiOiJ...",
    "accessToken": "eyJraWQiOiJ...",
    "refreshToken": "eyJjdHkiOiJ..."
  }
  ```

---

#### 3. Tạo Nhân vật RPG (`POST /character`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "name": "Valerius the Paladin",
    "characterClass": "Paladin"
  }
  ```
- **Phản hồi mong đợi (201 Created):**
  ```json
  {
    "characterId": "char-uuid-1234",
    "name": "Valerius the Paladin",
    "class": "Paladin",
    "level": 1,
    "hp": 100,
    "maxHp": 100,
    "attack": 15,
    "defense": 10
  }
  ```