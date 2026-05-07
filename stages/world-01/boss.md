# World 01 Boss - Patient Zero Escort

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 1 - Trại Sơ Tán Thất Thủ |
| Loại màn | Boss stage |
| Boss | Patient Zero Escort |
| Boss level | 5 |
| Level hero kỳ vọng | 5 |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Slot đội hình | 4 |
| Hệ thống đã mở | deploy cơ bản, Aegis Energy, EXP tướng, nâng cấp hero level |
| Enemy/Boss pool | Patient Zero Escort, Blank Walker, Static Carrier |
| Điều kiện mở boss | Hoàn thành đủ 30/30 sao của 10 stage thường trong World 1 |
| Mục tiêu thắng | Giết boss |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 170 giây |
| Stamina cost | 10 |
| First clear EXP | 290 |
| Repeat clear EXP | 140 |

## Ý đồ thiết kế

Boss stage là bài kiểm tra cuối của World 1: **tutorial, giữ cổng, xử lý runner và Static Carrier**.

Độ khó chính: độ khó tăng từ số lượng walker, sang runner tốc độ cao, rồi Static Carrier gây Signal Drain.

Boss không chỉ có nhiều máu hơn stage thường. Màn này ép người chơi xử lý đúng mechanic trước khi cố gắng kết thúc trận.

Điều kiện mở khóa boss:

- phải thắng đủ 10 stage thường của world
- phải đạt đủ **30/30 sao** từ 10 stage thường đó

Luật thắng/thua của boss stage:

- Người chơi thắng khi boss chết.
- Boss chết là kết thúc màn, không cần phá thêm ổ infected/cổng brainrot.
- Enemy, wave phụ và boss đều tạo áp lực lên cổng Aegis.
- Người chơi thua nếu cổng Aegis bị phá.

## Trạng thái người chơi

| Hero | Class | Deploy cost | Cooldown | Vai trò |
| ---- | ----- | ----------: | -------- | ------- |
| Kael Voss | Vanguard Breaker | 20 | 18 giây | tanker tuyến trước, giữ cổng |
| Mira Sane | Pulse Ranger | 15 | 14 giây | bắn xa, xử lý runner/support |

## Enemy và boss trong màn

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Patient Zero Escort | boss | cơ chế riêng của boss stage |
| Blank Walker | 1 | enemy nền, đông và chậm, dùng để ép tuyến |
| Static Carrier | 3 | chết phát nổ Signal Drain, nguy hiểm nếu nổ sát cổng |

## Boss mechanic

- boss có hộ vệ đi cùng
- boss hồi máu khi còn hộ vệ
- boss summon Blank Walker theo chu kỳ
- phase sau gọi Static Carrier

## Timeline V0.1

| Thời điểm | Sự kiện | Mục đích |
| --------: | ------- | -------- |
| 0s | Boss xuất hiện cùng 4 Blank Walker | mở trận, buộc người chơi dựng tuyến ngay |
| 25s | 5 Blank Walker | tăng áp lực tuyến trước |
| 50s | Boss kích hoạt mechanic 1 | giới thiệu cơ chế boss chính |
| 70s | 3 Static Carrier, 3 Blank Walker | trộn enemy để kéo người chơi khỏi việc chỉ focus boss |
| 60% HP | Boss chuyển phase 2 | tăng cường cơ chế chính của world |
| 105s | Boss gọi wave phụ lớn | kiểm tra khả năng clear wave |
| 30% HP | Boss chuyển phase cuối | tạo spike cuối trận |
| 150s | Finale wave: 5 Blank Walker, 3 Static Carrier | ép kết thúc trước khi cổng vỡ |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng boss stage |
| 2 sao | Hạ toàn bộ hộ vệ trước khi boss hồi máu quá 2 lần |
| 3 sao | Cổng Aegis còn trên 50% HP |

## Vì sao boss này khó

- Boss gom toàn bộ cơ chế chính của world vào một trận dài hơn stage thường.
- Người chơi phải chia sát thương giữa boss, wave phụ và mục tiêu mechanic.
- Objective sao phụ yêu cầu xử lý mechanic tốt, không chỉ thắng bằng level cao.
- Nếu kéo dài trận, wave phụ và mechanic boss sẽ bào cổng Aegis hoặc làm đội hình mất nhịp.

## Cách vượt qua

- deploy Kael trước để khóa tuyến
- đặt Mira sau Kael để bắn runner và Static Carrier
- không để Static Carrier chết quá gần cổng
- Không dồn toàn bộ Aegis Energy vào damage nếu tuyến trước chưa ổn định.
- Khi boss chuyển phase, giữ tài nguyên để phản ứng với wave hoặc mechanic mới.
- Ưu tiên objective 2 sao trước nếu muốn perfect clear, vì boss thường phạt người chơi bỏ qua mechanic.

## Dấu hiệu boss đang quá khó

- Người chơi đúng level kỳ vọng nhưng không qua được phase 2.
- Mechanic boss xảy ra quá sớm trước khi người chơi có đủ tài nguyên phản ứng.
- Wave phụ khiến cổng vỡ dù người chơi đã hạ đúng mục tiêu mechanic.

## Dấu hiệu boss đang quá dễ

- Người chơi có thể bỏ qua mechanic và chỉ focus boss vẫn thắng.
- Boss không ép thay đổi target priority.
- Phase cuối không tạo khác biệt so với nửa đầu trận.

