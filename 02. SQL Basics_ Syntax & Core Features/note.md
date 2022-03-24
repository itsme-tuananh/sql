SELECT name, salary FROM employees WHERE salary > 8000;

Core SQL Syntax Rules

- SQL Command / Statement

- Câu lệnh kết thúc bằng ;
- Token
- Key word
- Identifier
- Clause
- Value / Expression
- Operator

- Câu lệnh SQL bắt buộc phải kết thúc bằng ; - nếu có nhiều hơn 1 câu lệnh SQL trong cùng một lệnh
- 1 câu lệnh SQL đơn trong 1 lệnh không cần ; ở cuối
- Câu lệnh SQL là case-insensitive - SELECT là giống như select
- Identifier (e.g. tên bảng, tên cột) có thể được bao quanh bằng "" (hoặc `` trong MySQL) để tránh xung đột với các từ khóa được tích hợp sẵn
- Câu lệnh có thể chứa 1 hoặc nhiều mệnh đề - nhưng thứ tự của các mệnh đề bắt buộc phải chính xác (e.g. SELECT trước FROM và WHERE)

Data Definition Statement vs Data Manipulation Statement

Data Definition

- Những câu lệnh truy vấn định nghĩa cơ sở dữ liệu, bảng & cấu trúc bảng
- Ràng buộc & quan hệ bảng
- Quản lý cơ sở dữ liệu & bảng (e.g. chỉnh sửa bảng, xóa bảng)

Data Manipulation

- Những câu lệnh truy vấn thao tác (chèn, cập nhật & xóa) hoặc fetch dữ liệu
- Có thể join, filter hoặc sort dữ liệu
- Sử dụng cơ sở dữ liệu & bảng được tạo thông qua "Data Definition Statement"
