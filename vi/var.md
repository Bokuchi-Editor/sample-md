<!-- @var title: Kiểm Tra Biến Cục Bộ -->
<!-- @var author: Người Dùng Thử Nghiệm -->
<!-- @var date: 2026-03-07 -->
<!-- @var version: 1.0.0 -->

# {{title}}

Tài liệu này là bài kiểm tra tính năng biến cục bộ.

## Thông Tin Cơ Bản

- **Tác giả**: {{author}}
- **Ngày**: {{date}}
- **Phiên bản**: {{version}}

## So Sánh Với Biến Toàn Cục

Bằng cách vào [Cài đặt] > Biến toàn cục > Thêm biến mới
và đặt "Tên biến" = globalVar, "Giá trị" = Global,
phần hiển thị sau sẽ thay đổi trong bản xem trước khi áp dụng biến.

Giá trị được đặt bởi biến toàn cục: **{{globalVar}}**

## Mức Ưu Tiên Của Biến Cục Bộ

Biến cục bộ được ưu tiên hơn biến toàn cục.
Hãy thử đăng ký một biến toàn cục và xem liệu phần hiển thị sau có thay đổi không.
Ngoài ra, hãy thử xóa khai báo biến ở đầu tệp và xem liệu phần hiển thị có thay đổi không.

Giá trị biến cục bộ `title`: {{title}}
Giá trị biến cục bộ `author`: {{author}}
