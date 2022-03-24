- Foreign Key Naming Convention - entityName_columnName

- Inner Join - Kết nối 2 Table dựa trên các giá trị giống nhau xuất hiện trên 2 Column tại 2 Table
- Left Join - Lấy tất cả các giá trị trên Column tại Table bên trái (Table trước câu lệnh LEFT JOIN) và chỉ lấy các giá trị trên Column tại Table bên phải (Table sau câu lệnh LEFT JOIN) xuất hiện trên Column tại Table bên trái
- Right Join - ...
- Cross Join - Mỗi Row tại Table này sẽ được kết hợp với tất cả các Row tại Table kia

- Union - Kết hợp nhiều Result Set thành 1 Result Set bằng cách nối thêm Row (chỉ có thể thực hiện khi các Result Set có cùng số Column)
- Join - Gộp nhiều Table vào một Result Set bằng cách nối thêm Column

- Có thể sử dụng giá trị của bất kì Column nào làm Foreign Key (kể cả các non-Primary Key Column)

- ... REFERENCES <table_name> (<column_name>) ON DELETE [RESTRICT|NO ACTION (default)|CASCADE|SET NULL|SET DEFAULT] ON UPDATE ...
- Nếu sử dụng Primary Key làm khóa ngoại, có thể bỏ qua <column_name>

- 1:1 - Có thể đặt Foreign Key ở bất kì Table nào trong 2 Table (nên đặt sao cho tối ưu (ví dụ, ON DELETE, ON UPDATE được thuận tiện))
- 1:n - Đặt Foreign Key ở Table phía n

- n:n - Tạo một "Intermediate Table" lưu trữ quan hệ giữa 2 "Main Table". "One row per relation"
- "Intermediate Table" Naming Convention: mainTableX_mainTableY
