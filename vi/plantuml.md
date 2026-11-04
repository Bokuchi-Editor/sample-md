# Mẫu Biểu Đồ PlantUML

Bộ sưu tập các biểu đồ PlantUML để xác minh hiển thị trong Bokuchi.

> Hãy bật Cài đặt → Nâng cao → "PlantUML (Sơ đồ)" trước khi xem trước. Khi tắt, một thông báo ở đầu phần xem trước sẽ hướng dẫn cách bật.

## Biểu Đồ Lớp

```plantuml
@startuml
package "External API (Facade)" {
    class ClientFacade {
        - _internalBuffer: ResourceBuffer
        - _context: ExecutionContext
        + Execute(node: IExecutableNode): void
        + ExportData(): byte[]
        + Dispose(): void
        + {static} Combine(a: ClientFacade, b: ClientFacade): IExecutableNode
        + {static} Transform(a: ClientFacade, b: ClientFacade): IExecutableNode
    }

    interface IExecutableNode {
        + Execute(context: ExecutionContext, destination: ResourceHandle): void
    }

    ClientFacade ..> IExecutableNode : uses / produces
}
@enduml
```

## Biểu Đồ Tuần Tự (không có `@startuml`, định danh `puml`)

`@startuml` / `@enduml` sẽ được tự động thêm vào khi bị bỏ qua. Định danh `puml` cũng hoạt động.

```puml
actor "Người dùng" as U
participant "Dịch vụ xác thực" as A
U -> A : Yêu cầu đăng nhập
A --> U : Cấp token
note right of A : Một ghi chú
```

## Biểu Đồ Hoạt Động (định danh `uml`)

```uml
start
:Đọc tệp;
if (Là Markdown?) then (có)
  :Hiển thị xem trước;
else (không)
  :Hiển thị thô;
endif
stop
```

## Sơ Đồ Tư Duy

Các thẻ bắt đầu khác `@startuml`, chẳng hạn `@startmindmap`, được giữ nguyên.

```plantuml
@startmindmap
* Bokuchi
** Trình soạn thảo
*** Monaco
** Xem trước
*** Mermaid
*** PlantUML
@endmindmap
```

## Dùng Chung Với Mermaid

```mermaid
graph TD
  A[Markdown] --> B[Xem trước]
```

```plantuml
A -> B : hello
```

## Khối Mã Thông Thường Không Bị Ảnh Hưởng

```javascript
const a = 1;
```

## Kiểm Tra Xử Lý Lỗi

Khối sau chứa lỗi cú pháp. Biểu đồ lỗi của chính PlantUML sẽ được hiển thị:

```plantuml
class A {
A -> ;;; B ->-> C
```

Khối tiếp theo là loại biểu đồ không được hỗ trợ (ditaa). Một hộp lỗi sẽ được hiển thị:

```plantuml
@startditaa
+-------+   +-------+
| A     |-->| B     |
+-------+   +-------+
@endditaa
```
