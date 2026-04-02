# Koleksi Contoh Penyorotan Sintaks Kode

Contoh ini mendemonstrasikan cara menampilkan penyorotan sintaks untuk berbagai bahasa pemrograman menggunakan fitur markdown Bokuchi Editor.

## JavaScript

```javascript
// Contoh menggunakan fitur ES6+
class User {
  constructor(name, email) {
    this.name = name;
    this.email = email;
  }

  greet() {
    return `Hello, I'm ${this.name}`;
  }

  // Contoh pemrosesan asinkron
  async fetchUserData() {
    try {
      const response = await fetch(`/api/users/${this.email}`);
      return await response.json();
    } catch (error) {
      console.error('Error fetching user data:', error);
    }
  }
}

// Fungsi panah dan operasi array
const users = [
  new User('Alice', 'alice@example.com'),
  new User('Bob', 'bob@example.com')
];

const greetings = users.map(user => user.greet());
console.log(greetings);
```

## TypeScript

```typescript
// Interface dan generics
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

// Contoh penggunaan
const client = new ApiClient('https://api.example.com');
const userData = await client.get<User>('/users/123');
```

## Python

```python
# Kelas data dan petunjuk tipe
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
        """Mengambil data pengguna secara asinkron"""
        # Dalam implementasi sebenarnya, gunakan aiohttp dll.
        return []

    def filter_adults(self, users: List[User]) -> List[User]:
        """Memfilter hanya pengguna dewasa"""
        return [user for user in users if user.age and user.age >= 18]
```

## Java

```java
// Contoh controller Spring Boot
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
// Contoh server HTTP dan handler
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
// Contoh web server dan penanganan error
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
-- Contoh kueri PostgreSQL
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Contoh kueri kompleks
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
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistem Manajemen Pengguna</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f5f5f5; color: #333; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; }
        .user-card { background: white; border-radius: 8px; padding: 1.5rem; margin-bottom: 1rem; box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); }
    </style>
</head>
<body>
    <div class="container">
        <h1>Sistem Manajemen Pengguna</h1>
        <div id="user-list"></div>
    </div>
</body>
</html>
```
