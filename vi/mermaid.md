# Mẫu Biểu Đồ Mermaid

Bộ sưu tập các biểu đồ Mermaid để xác minh hiển thị trong Bokuchi.

## Lưu Đồ

```mermaid
graph TD
    A[Bắt đầu] --> B{Nó hoạt động không?}
    B -- Có --> C[Tuyệt vời!]
    B -- Không --> D[Gỡ lỗi]
    D --> B
    C --> E[Triển khai]
```

## Biểu Đồ Trình Tự

```mermaid
sequenceDiagram
    participant Người dùng
    participant Frontend
    participant Backend
    participant DB

    Người dùng->>Frontend: Nhấn "Lưu"
    Frontend->>Backend: POST /api/save
    Backend->>DB: INSERT INTO documents
    DB-->>Backend: OK
    Backend-->>Frontend: 200 Thành công
    Frontend-->>Người dùng: Hiển thị thông báo
```

## Biểu Đồ Gantt

```mermaid
gantt
    title Tiến Độ Dự Án
    dateFormat  YYYY-MM-DD
    section Lập kế hoạch
    Yêu cầu            :done,    req, 2025-01-01, 14d
    Thiết kế            :done,    des, after req, 10d
    section Phát triển
    Frontend            :active,  fe,  after des, 30d
    Backend             :         be,  after des, 25d
    section Kiểm thử
    Kiểm thử tích hợp  :         test, after fe, 14d
    Phát hành           :milestone, rel, after test, 0d
```

## Biểu Đồ Lớp

```mermaid
classDiagram
    class Editor {
        -content: string
        -theme: string
        +onChange(content)
        +setTheme(theme)
    }
    class Preview {
        -markdown: string
        +render()
    }
    class Tab {
        -id: string
        -title: string
        -isModified: boolean
        +save()
        +close()
    }
    Editor --> Preview : hiển thị
    Tab --> Editor : chứa
```

## Biểu Đồ Trạng Thái

```mermaid
stateDiagram-v2
    [*] --> Trống
    Trống --> Đang_chỉnh_sửa : Tệp mới / Mở tệp
    Đang_chỉnh_sửa --> Đã_sửa_đổi : Nội dung thay đổi
    Đã_sửa_đổi --> Đã_lưu : Lưu (Ctrl+S)
    Đã_lưu --> Đã_sửa_đổi : Nội dung thay đổi
    Đã_sửa_đổi --> Đã_đóng : Đóng mà không lưu
    Đã_lưu --> Đã_đóng : Đóng
    Đã_đóng --> Trống : Tab cuối cùng đã đóng
    Trống --> [*]
```

## Biểu Đồ Tròn

```mermaid
pie title Ngôn Ngữ Được Hỗ Trợ
    "Tiếng Anh" : 1
    "Tiếng Nhật" : 1
    "Tiếng Trung (Giản thể)" : 1
    "Tiếng Trung (Phồn thể)" : 1
    "Tiếng Hàn" : 1
    "Tiếng Tây Ban Nha" : 1
    "Tiếng Pháp" : 1
    "Tiếng Đức" : 1
    "Tiếng Bồ Đào Nha (BR)" : 1
    "Tiếng Nga" : 1
    "Tiếng Hindi" : 1
    "Tiếng Ả Rập" : 1
    "Tiếng Indonesia" : 1
    "Tiếng Việt" : 1
```

## Kiểm Tra Xử Lý Lỗi

Khối sau chứa lỗi cú pháp có chủ đích để xác minh hiển thị lỗi:

```mermaid
invalid diagram syntax !!!
this should show an error message
```
