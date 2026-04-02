# Hướng Dẫn Sử Dụng Bokuchi Editor

Hướng dẫn này giới thiệu các cách sử dụng tiện lợi của trình soạn thảo Bokuchi.

## Sử Dụng Tính Năng Tab

### Chỉnh Sửa Nhiều Tệp
- **Tệp mới**: `Ctrl+N` (Windows/Linux) hoặc `Cmd+N` (Mac)
- **Mở tệp**: `Ctrl+O` (Windows/Linux) hoặc `Cmd+O` (Mac)
- **Chuyển tab**: `Ctrl+Tab` để sang tab tiếp theo, `Ctrl+Shift+Tab` để quay lại tab trước

### Ví Dụ Thực Tế
1. Chỉnh sửa tài liệu chính
2. Mở tài liệu tham khảo ở tab riêng
3. Quản lý tệp mẫu ở tab riêng
4. Sao chép & dán giữa nhiều tab

## Tính Năng Thu Phóng

### Điều Chỉnh Thu Phóng
- **Phóng to**: `Ctrl++` (Windows/Linux) hoặc `Cmd++` (Mac)
- **Thu nhỏ**: `Ctrl+-` (Windows/Linux) hoặc `Cmd+-` (Mac)
- **Đặt lại**: `Ctrl+0` (Windows/Linux) hoặc `Cmd+0` (Mac)

### Trường Hợp Sử Dụng
- **Thuyết trình**: Chữ lớn để dễ nhìn hơn
- **Chỉnh sửa chi tiết**: Chữ nhỏ để nhìn tổng quan
- **Hai màn hình**: Điều chỉnh cho vừa với một màn hình

## Tính Năng Giao Diện

### Chuyển Đổi Giao Diện
- **Chế độ tối**: Dễ chịu cho mắt, phù hợp cho làm việc lâu
- **Chế độ sáng**: Phù hợp cho in ấn hoặc làm việc trong môi trường sáng

### Tùy Chỉnh
- Có thể tùy chỉnh chi tiết bằng biến CSS
- Cũng có thể cấu hình CSS tùy chỉnh cho bản xem trước

## Lưu Trữ Trạng Thái

### Tính Năng Tự Động Lưu
- Trạng thái được khôi phục khi khởi động lại ứng dụng
- Các tab đang mở, tab đang hoạt động và nội dung chưa lưu đều được giữ lại
- Đường dẫn tệp cũng được ghi nhớ, nên các tệp bị sửa đổi bên ngoài sẽ tự động được tải lại

### Mẹo Sử Dụng
- Khi tạm dừng công việc, chỉ cần đóng ứng dụng
- Lần khởi động tiếp theo sẽ khôi phục trạng thái làm việc trước đó
- Đặc biệt tiện lợi khi làm việc song song trên nhiều dự án

## Ứng Dụng Tính Năng Biến

### Tạo Mẫu
```markdown
<!-- @var projectName: Dự Án Của Tôi -->
<!-- @var version: 1.0.0 -->
<!-- @var author: Tên Của Bạn -->

# Tài liệu {{projectName}}

Phiên bản: {{version}}
Tác giả: {{author}}

## Tổng quan
Tài liệu này mô tả dự án {{projectName}}.
```

### Sử Dụng Biến Toàn Cục
- Đặt thông tin chung như tên công ty, tên phòng ban, tên tác giả làm biến toàn cục
- Quản lý thông tin nhất quán trên nhiều tài liệu

## Sử Dụng Tính Năng Checkbox

### Quản Lý Công Việc
```markdown
## Công Việc Hôm Nay
- [ ] Chuẩn bị tài liệu họp
- [ ] Thực hiện đánh giá mã nguồn
- [ ] Cập nhật tài liệu
- [x] Kiểm tra email buổi sáng
```

### Quản Lý Dự Án
- Trực quan hóa trạng thái tiến độ
- Xác nhận các công việc đã hoàn thành
- Chia sẻ tiến độ trong nhóm

## Thực Hành Tốt Nhất Cho Thao Tác Tệp

### Quy Ước Đặt Tên Tệp
- Bao gồm ngày tháng: `2025-01-15-meeting-notes.md`
- Bao gồm tên dự án: `project-alpha-spec.md`
- Quản lý phiên bản: `api-docs-v2.md`

### Cấu Trúc Thư Mục
```
docs/
├── meetings/
│   ├── 2025-01-15-weekly.md
│   └── 2025-01-22-weekly.md
├── specs/
│   ├── api-spec.md
│   └── ui-spec.md
└── templates/
    ├── meeting-template.md
    └── project-template.md
```

## Tóm Tắt

Bokuchi Editor không chỉ là một trình soạn thảo markdown đơn thuần, mà còn cung cấp môi trường tạo tài liệu hiệu quả.
Nó đặc biệt xuất sắc trong các lĩnh vực sau:

- **Hỗ trợ đa nhiệm**: Chỉnh sửa đồng thời nhiều tệp
- **Tính dễ sử dụng**: Thao tác trực quan và lưu trữ trạng thái
- **Khả năng tùy chỉnh**: Cài đặt linh hoạt với giao diện và biến
- **Tính thực dụng**: Các tính năng thực tế như checkbox và thu phóng

Bằng cách kết hợp các tính năng này, việc tạo tài liệu hiệu quả và thoải mái hơn trở nên khả thi.
