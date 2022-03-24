- Transaction - Gộp một nhóm các Statement vào một Transaction Block. Các thay đổi được tạo ra trong một Transaction Session chỉ được lưu trong Memory cho tới khi Transaction Session kết thúc, có thể quyết định Undo Changes hoặc Commit Changes

- Rollback - Trở về trạng thái trước khi start Transaction (Undo Changes) và kết thúc Transaction Session

- Commit - Cập nhật thay đổi vào Database (Commit Changes) và kết thúc Transaction Session

- Start một Transaction Session mới khi chưa kết thúc Transaction Session hiện tại (Rollback hoặc Commit) sẽ dẫn tới Implicit Commit (thay đổi của Transaction Session hiện tại sẽ tự động được Commit vào Database)

- Save Point - Đóng vai trò như một điểm đánh dấu cho các thay đổi được tạo ra trong một Transaction Session. Khi Rollback về một Save Point, các thay đổi trở về trạng thái trước Save Point. Rollback về một Save Point không kết thúc Transaction Session hiện tại
