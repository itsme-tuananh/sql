- Primary Key không nhất thiết phải là auto-incrementing integer

- Composite Primary Key - Primary Key gồm giá trị của nhiều hơn 1 Column
- PRIMARY KEY (column_x, column_y)

- Surrogate Key - Đóng vai trò như một định danh chính duy nhất nhưng không phải tiêu chí xác định duy nhất thực sự (ví dụ, id tại "Intermediate Table" trong n:n)
- Không có gì sai với việc sử dụng Surrogate Key! Surrogate Key thường rất hữu dụng

- Một Column là Foreign Key vẫn có thể trở thành (hoặc nằm trong) Primary Key

- Composite Foreign Key - Foreign Key gồm giá trị của nhiều hơn 1 Column
- FOREIGN KEY (column_x, column_y) REFERENCES table_x (column_x, column_y) ON DELETE ...

- Self-Referential Relationship - Một Data Entity có quan hệ với chính nó (internal relationship) => Thêm 1 Column tham chiếu tới chính nó
  CREATE TABLE employees (
  id SERIAL PRIMARY KEY,
  ...,
  supervisor_id INT REFERENCES employees ON DELETE SET NULL
  );

- 1 Table có thể INNER JOIN với chính nó (cần sử dụng 2 Alias phân biệt)
  SELECT \*
  FROM employees AS e1
  INNER JOIN employees AS e2 ON e1.supervisor_id = e2.id;

- Self-Referential Many-to-Many Relationship - Tương tự Self-Referential Relationship nhưng quan hệ n:n
  => Tạo "Intermediate Table", nhưng cần thêm ràng buộc để 1 quan hệ không xuất hiện 2 lần (do cùng tham chiếu tới 1 Table nên 1 quan hệ có 2 cách biểu diễn)
  CREATE TABLE users_friends (
  user_id INT REFERENCES users ON DELETE CASCADE,
  friend_id INT REFERENCES users ON DELETE CASCADE,
  CHECK (user_id < friend_id),
  PRIMARY KEY (user_id, friend_id)
  );
