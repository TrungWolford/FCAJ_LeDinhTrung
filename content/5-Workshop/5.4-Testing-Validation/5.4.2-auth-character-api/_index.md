---
title : "Authentication & Character APIs"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.4.2 </b> "
---

#### Testing Authentication & Character Creation

In this step, you will test user registration, login, JWT token retrieval from Amazon Cognito, and creating a new RPG character.

---

#### 1. Register User (`POST /auth/register`)

- **Request Body:**
  ```json
  {
    "username": "player1",
    "password": "Password123!",
    "email": "player1@example.com"
  }
  ```
- **Expected Response (200 OK):**
  ```json
  {
    "message": "User registered successfully. Please check your email for confirmation."
  }
  ```

---

#### 2. Login User (`POST /auth/login`)

- **Request Body:**
  ```json
  {
    "username": "player1",
    "password": "Password123!"
  }
  ```
- **Expected Response (200 OK):**
  ```json
  {
    "idToken": "eyJraWQiOiJ...",
    "accessToken": "eyJraWQiOiJ...",
    "refreshToken": "eyJjdHkiOiJ..."
  }
  ```

---

#### 3. Create RPG Character (`POST /character`)

- **Headers:** `Authorization: Bearer {{ID_TOKEN}}`
- **Request Body:**
  ```json
  {
    "name": "Valerius the Paladin",
    "characterClass": "Paladin"
  }
  ```
- **Expected Response (201 Created):**
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