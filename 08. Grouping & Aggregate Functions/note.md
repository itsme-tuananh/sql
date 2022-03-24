- Aggregate - Phép tính toán học trả về một (tổng hợp) kết quả
- Function - Hoạt động được định nghĩa từ trước, được thực thi theo yêu cầu
  => Aggregate Function - ...

- COUNT(\*) - Đếm tổng số bản ghi
- COUNT(column_name) - Không đếm giá trị NULL
- COUNT(DISTINCT column_name) - Chỉ đếm giá trị phân biệt (không trùng lặp)

- MAX(), MIN() - Đối với Text, so sánh thứ tự alphabet

- SUM()
- AVG() - Không xét giá trị NULL
- ROUND(..., x) - x: Số chữ số sau dấu .

- GROUP BY ... - Aggregated và Non-Aggregated trong cùng một Statement

- "Where" vs "Having"

* Filter Applied to: Raw Data | Aggregated Data (GROUP BY)
* Aggregate Function as Filter Condition Allowed: No | Yes
* Position: Before GROUP BY | After GROUP BY

- Window Function - Khá tương tự Aggregate Function, nhưng không gộp kết quả làm một cho toàn bộ Table (hoặc một nhóm), mà tạo thêm 1 Column chứa kết quả và không giảm bớt giá trị đầu vào về 1 Row hoặc 1 giá trị
- SUM(column_x) OVER()
- SUM(column_x) OVER(PARTITION BY column_y) - Các Row có cùng giá trị tại column_y sẽ được gộp chung tính toán và Column chứa kết quả tại các Row đó chứa cùng 1 giá trị
- SUM(column_x) OVER(PARTITION BY column_y ORDER BY column_z) - Các Row có cùng giá trị tại column_y sẽ được sắp xếp theo giá trị tại column_z, gộp chung tính toán và Column chứa kết quả tại các Row đó chứa cùng 1 giá trị

- RANK() - Rank các Row dựa trên giá trị của một Column cụ thể
