# Mẫu Bố cục Bảng

Tệp này minh họa cách thiết lập **Bố cục bảng (Xem trước)** trong Bokuchi thay đổi cách bảng được hiển thị.

> Vị trí thiết lập: **Cài đặt → Nâng cao → Bố cục bảng (Xem trước)**

Hãy chuyển đổi giữa ba chế độ trong khi xem trước tệp này để thấy rõ sự khác biệt.

## Sự khác biệt giữa các chế độ

| Chế độ | Chiều rộng cột | Nội dung dài |
|--------|----------------|--------------|
| Chiều rộng cột bằng nhau | Tất cả như nhau | Xuống dòng trong ô |
| Theo nội dung (xuống dòng trong ô) — mặc định | Theo nội dung | Xuống dòng trong ô |
| Theo nội dung (cuộn ngang) | Theo nội dung | Bảng cuộn ngang |

---

## Ví dụ 1: Chỉ một cột chứa mô tả dài

Đây là nơi sự khác biệt giữa **Chiều rộng bằng nhau** và **Theo nội dung** rõ ràng nhất.
Ở chế độ **Chiều rộng bằng nhau**, các cột ngắn như "ID", "Ngày", "Trạng thái" bị gán cùng chiều rộng với cột mô tả dài, khiến cột mô tả trở thành dải hẹp và cao, khó đọc.
Ở chế độ **Theo nội dung**, cột mô tả nhận được không gian cần thiết, các cột ngắn vẫn gọn gàng.

| ID | Ngày | Mô tả | Trạng thái |
|----|------|-------|------------|
| 001 | 2026-05-01 | Bổ sung luồng đăng ký người dùng mới. Hỗ trợ cả đăng nhập OAuth2 (Google / GitHub / Microsoft) và email/mật khẩu, đồng thời yêu cầu người dùng điền hồ sơ ở lần đăng nhập đầu tiên. | Hoàn thành |
| 002 | 2026-05-03 | Chuyển lớp cache sang Redis, giảm thời gian phản hồi API trung bình từ 280ms xuống 95ms. | Hoàn thành |
| 003 | 2026-05-05 | Tái cấu trúc phân trang cho API tìm kiếm. Việc lấy tổng số được làm chậm để tăng tốc phản hồi đầu tiên. | Đang xét |
| 004 | 2026-05-08 | Làm mới giao diện cài đặt thông báo: hỗ trợ chủ đề tối/sáng và cải thiện khả năng tiếp cận. | Đang chạy |

---

## Ví dụ 2: Quá nhiều cột không vừa màn hình

Đây là nơi chế độ **cuộn ngang** phát huy giá trị.
Ở chế độ **Chiều rộng bằng nhau** và **Theo nội dung (xuống dòng trong ô)**, mọi ô đều bị thu hẹp để toàn bộ bảng vừa với khung. Ở chế độ **cuộn ngang**, mỗi cột giữ chiều rộng tự nhiên và bảng tự cuộn sang ngang.

| Mã đơn | Khách hàng | Thời gian đặt | Mã SP | Sản phẩm | SL | Đơn giá (₫) | Tạm tính (₫) | Địa chỉ giao | Trạng thái | Phụ trách |
|--------|------------|---------------|-------|----------|----|-------------|--------------|--------------|------------|-----------|
| ORD-20260501-001 | Nguyễn Văn An | 2026-05-01 09:14 | SKU-A1023 | Laptop hiệu năng cao Pro 15 | 1 | 45.800.000 | 45.800.000 | 12 Lê Lợi, Phường Bến Nghé, Quận 1, TP.HCM | Đã giao | Sato |
| ORD-20260502-007 | Trần Thị Bình | 2026-05-02 13:22 | SKU-B2240 | Bàn phím cơ không dây | 2 | 3.450.000 | 6.900.000 | 88 Trần Hưng Đạo, Hoàn Kiếm, Hà Nội | Đang giao | Suzuki |
| ORD-20260503-014 | Lê Hoàng Chương | 2026-05-03 18:47 | SKU-C0098 | Màn hình 4K 32 inch HDR | 1 | 16.500.000 | 16.500.000 | 27 Bạch Đằng, Hải Châu, Đà Nẵng | Chuẩn bị | Tanaka |

---

## Ví dụ 3: Bảng so sánh đơn giản

Khi tất cả nội dung đều ngắn, ba chế độ gần như không có khác biệt nhìn thấy được. Bảng so sánh hằng ngày vẫn dễ đọc ở mọi chế độ.

| Mục | Gói A | Gói B | Gói C |
|-----|-------|-------|-------|
| Hằng tháng | 199.000₫ | 399.000₫ | 799.000₫ |
| Lưu trữ | 10 GB | 100 GB | 1 TB |
| Hỗ trợ | Email | Email / Chat | Điện thoại 24h |

---

## Cách thử

1. Mở tệp này trong Bokuchi và hiển thị xem trước
2. Mở **Cài đặt → Nâng cao → Bố cục bảng (Xem trước)**
3. Chọn **Chiều rộng cột bằng nhau** và quan sát cột mô tả ở Ví dụ 1 trở nên hẹp và cao, khó đọc
4. Quay lại **Theo nội dung (xuống dòng trong ô)** (mặc định) và thấy các cột tự điều chỉnh theo nội dung
5. Chuyển sang **Theo nội dung (cuộn ngang)** và xác nhận bảng ở Ví dụ 2 cuộn ngang thay vì bị thu hẹp

> Tệp HTML xuất ra qua nút **Download** (góc trên bên phải của xem trước) cũng tuân theo thiết lập này.
