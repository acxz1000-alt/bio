## Release TienThinh.Com V5 Tester

## Mô Tả V5.0.0

* Giao diện thân thiện, được tối ưu hoá để không gây ra tuột khung hình (lag)
* Panel Setting đã được thêm vào, tuỳ chỉnh các cài đặt nho nhỏ của trang.
* Đã thay đổi tất cả hình ảnh thành biểu tượng, loại bỏ kiểu chuột, tối ưu hóa chi tiết, sửa đổi tất cả các đường dẫn thành đường dẫn tương đối và khắc phục các vấn đề khác.
* Thêm animation màn hình khoá, thêm chế độ chuyển sang love day responsive, Tối ưu hóa hiệu ứng chuyển động.
* Vá lỗi nhỏ khi chọn nhạc & tự động chuyển nhạc trong panel setting.
* Đã tích hợp xoá cache bằng js kèm vào đó nhân bản class fake ở DOM. Loại bỏ nền gradient và tối ưu hóa animation cũng như độ trễ.
* Loader Screen thông minh tự động hiện khi trang chưa tải xong, tự động ẩn khi trang đã tải xong hoàn toàn, khi trang tải tới đâu thanh % sẽ hiện tới đó, sửa lỗi loader chồng lên pace-active.


## Tải Xuống

_(Sài termux hoặc Command)_

```sh
git clone https://github.com/WusThanhDieu/Profile-ThanhDieu.Com-V5-Tester.git
```

## Hướng Dẫn

Chỉnh sửa chung ở đường dẫn {domain}/res/config/option.php

Chỉnh sửa tài nguyên ở: {domain}/res/v5/*

## Demo
![TienThinh.Com](https://i.imgur.com/urmLd6H.png)
![TienThinh.Com](https://i.imgur.com/tOWfTBQ.png)
![TienThinh.Com](https://i.imgur.com/jjvyIvG.png)

## 🎮 Khu Trò Chơi
Bấm nút 🎮 trên thanh header để mở menu chọn trò chơi (giống nút đếm ngày yêu ❤️).

- Danh sách game cấu hình trong `res/config/option.php` → class `ThanhDieuGameList` → mảng `$games`.
- Mỗi game là 1 file HTML độc lập trong `res/v5/games/` (có sẵn: `snake.html`, `xo.html`, `memory.html`, `mole.html`).
- **Thêm game**: tạo file `res/v5/games/ten-game.html`, rồi thêm 1 khối `title / icon / desc / url / enabled` vào `$games`.
- **Bớt game**: xóa khối đó hoặc đặt `"enabled" => false`.
- **Sửa game**: đổi thông tin trong `option.php`; chỉnh luật chơi/tốc độ ở phần `CẤU HÌNH GAME` đầu mỗi file game.


## THINH.OS GAME CENTER - NEON GOMOKU FULL
- Cờ Caro 15x15 với 4 mức AI, undo, lưu điểm AI cục bộ.
- Multiplayer online dùng Supabase Auth + PostgreSQL + Realtime: phòng riêng, mã phòng, ghép ngẫu nhiên, chat, lịch sử và bảng xếp hạng.
- Cấu hình Supabase trong `res/v5/games/supabase-config.js`.
- Chạy SQL trong `SETUP/supabase-schema.sql`; xem `SETUP/README-VI.txt`.
- Nếu chưa cấu hình Supabase, chế độ AI vẫn chơi bình thường; các chế độ online cần backend.
