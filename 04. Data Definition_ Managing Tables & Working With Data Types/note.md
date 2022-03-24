SQL Convention

- Identifier sử dụng lowercase
- Nối các từ trong 1 Identifier bằng \_
- Identifier trùng với Key Word => Sử dụng "" (PostgreSQL) hoặc `` (MySQL)

- Với MySQL có thể sử dụng CREATE SCHEMA ...
- Có thể thêm các tùy chọn trong câu lệnh tạo CSDL tương ứng với mỗi RDBMS

- Tên bảng có thể để dạng số ít hay số nhiều

- ENUM: Kiểu dữ liệu chỉ chứa một số giá trị nhất định cho trước

- INSERT INTO tables (... column names) VALUES (... giá trị tương ứng từng cột) - Có thể bỏ qua một số cột bằng cách bỏ qua tên cột và giá trị

- NUMERIC(precision, scale)
- precision - Tổng số chữ số được lưu trữ
- scale - Tổng số chữ số sau dấu . được lưu trữ
- Nếu tổng số chữ số vượt quá giới hạn => Error (Lỗi)
- Nếu tống số chữ số sau dấu . vượt qua giới hạn => Rounded (Làm tròn)

- Ràng buộc Column và ràng buộc Table (so sánh giá trị của 2 Column,...)
