- Index - Các giá trị được lưu trữ trong một bảng phụ đã được sắp xếp. Một liên kết với Row gốc được lưu trữ cùng với Index Value
- Index có thể nâng cao hiệu suất truy vấn
- Mặc định chỉ có Primary Key được tạo Index

- Không sử dụng quá nhiều Index!

- Các loại Index

* Standard single-column index
* Unique index
* Multi-column index
* Partial index (Not In MySQL)

- EXPLAIN - Không thực thi mà giải thích cách thực thi Statement sau nó (Plan)
- EXPLAIN ANALYZE - Vừa đưa ra Plan, vừa thực thi để trả về kết quả thực tế sau khi thực thi Statement sau nó

- Khi thêm ràng buộc UNIQUE cho một Column, một Unique Index tương ứng với Column sẽ được tạo tự động

- Multi-column index tối ưu cho câu lệnh WHERE chứa điều kiện AND (kết hợp các Column)
- Thứ tự khi định nghĩa Multi-column index quan trọng
- Vẫn tận dụng được Multi-column index khi WHERE không chứa đủ giá trị mà chỉ chứa các giá trị tại định nghĩa Multi-column index theo thứ tự từ trái sang
