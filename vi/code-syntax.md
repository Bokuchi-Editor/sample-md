# Bộ Sưu Tập Mẫu Tô Sáng Cú Pháp Mã Nguồn

Mẫu này trình bày cách hiển thị tô sáng cú pháp cho các ngôn ngữ lập trình khác nhau bằng chức năng markdown của Bokuchi Editor.

## JavaScript

```javascript
// Mẫu sử dụng tính năng ES6+
class User {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }

  greet() {
    return `Hello, I'm ${this.name}`;
  }

  // Ví dụ xử lý bất đồng bộ
  async fetchUserData() {
    try {
      const response = await fetch(`/api/users/${this.email}`);
      return await response.json();
    } catch (error) {
      console.error('Error fetching user data:', error);
    }
  }
}

// Hàm mũi tên và thao tác mảng
const users = [
  new User('Alice', 'alice@example.com'),
  new User('Bob', 'bob@example.com')
];

const greetings = users.map(user => user.greet());
console.log(greetings);
```

## TypeScript

```typescript
// Interface và generics
interface ApiResponse<T> {
  data: T;
  status: number;
  message: string;
}

class ApiClient {
  private baseUrl: string;

  constructor(baseUrl: string) {
    this.baseUrl = baseUrl;
  }

  async get<T>(endpoint: string): Promise<ApiResponse<T>> {
    const response = await fetch(`${this.baseUrl}${endpoint}`);
    return await response.json();
  }
}

// Ví dụ sử dụng
const client = new ApiClient('https://api.example.com');
const userData = await client.get<User>('/users/123');
```

## Python

```python
# Data class và gợi ý kiểu
from dataclasses import dataclass
from typing import List, Optional
import asyncio

@dataclass
class User:
    name: str
    email: str
    age: Optional[int] = None

class UserService:
    def __init__(self, api_url: str):
        self.api_url = api_url

    async def fetch_users(self) -> List[User]:
        """Lấy dữ liệu người dùng bất đồng bộ"""
        # Trong triển khai thực tế, sử dụng aiohttp v.v.
        return []

    def filter_adults(self, users: List[User]) -> List[User]:
        """Lọc chỉ người dùng trưởng thành"""
        return [user for user in users if user.age and user.age >= 18]
```

## Java

```java
// Ví dụ controller Spring Boot
package com.example.controller;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.*;
import java.util.List;
import java.util.Optional;

@RestController
@RequestMapping("/api/users")
public class UserController {

    @Autowired
    private UserService userService;

    @GetMapping
    public ResponseEntity<List<User>> getAllUsers() {
        List<User> users = userService.findAll();
        return ResponseEntity.ok(users);
    }

    @GetMapping("/{id}")
    public ResponseEntity<User> getUserById(@PathVariable Long id) {
        Optional<User> user = userService.findById(id);
        return user.map(ResponseEntity::ok)
                  .orElse(ResponseEntity.notFound().build());
    }
}
```

## Go

```go
// Ví dụ HTTP server và handler
package main

import (
    "encoding/json"
    "fmt"
    "net/http"
)

type User struct {
    ID    int    `json:"id"`
    Name  string `json:"name"`
    Email string `json:"email"`
}

func getUsers(w http.ResponseWriter, r *http.Request) {
    users := []User{
        {ID: 1, Name: "Alice", Email: "alice@example.com"},
        {ID: 2, Name: "Bob", Email: "bob@example.com"},
    }

    w.Header().Set("Content-Type", "application/json")
    json.NewEncoder(w).Encode(users)
}

func main() {
    http.HandleFunc("/users", getUsers)
    fmt.Println("Server starting on :8080")
    http.ListenAndServe(":8080", nil)
}
```

## Rust

```rust
// Ví dụ web server và xử lý lỗi
use actix_web::{web, App, HttpServer, Result, HttpResponse};
use serde::{Deserialize, Serialize};

#[derive(Serialize, Deserialize, Clone)]
struct User {
    id: u32,
    name: String,
    email: String,
}

async fn get_users() -> Result<HttpResponse> {
    let users = vec![
        User { id: 1, name: "Alice".to_string(), email: "alice@example.com".to_string() },
        User { id: 2, name: "Bob".to_string(), email: "bob@example.com".to_string() },
    ];
    Ok(HttpResponse::Ok().json(users))
}

#[actix_web::main]
async fn main() -> std::io::Result<()> {
    HttpServer::new(|| {
        App::new()
            .route("/users", web::get().to(get_users))
    })
    .bind("127.0.0.1:8080")?
    .run()
    .await
}
```

## SQL

```sql
-- Truy vấn mẫu PostgreSQL
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Ví dụ truy vấn phức tạp
SELECT
    u.name,
    u.email,
    COUNT(p.id) as post_count
FROM users u
LEFT JOIN posts p ON u.id = p.user_id
WHERE u.created_at >= '2024-01-01'
GROUP BY u.id, u.name, u.email
ORDER BY post_count DESC
LIMIT 10;
```

## HTML/CSS

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Management System</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f5f5f5; color: #333; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; }
        .user-card { background: white; border-radius: 8px; padding: 1.5rem; margin-bottom: 1rem; box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); }
    </style>
</head>
<body>
    <div class="container">
        <h1>User Management System</h1>
        <div id="user-list"></div>
    </div>
</body>
</html>
```
