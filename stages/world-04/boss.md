# World 04 Boss - Bombardiro Crocodilo

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 4 - Nhà Máy Gãy Xương |
| Loại màn | Boss stage |
| Boss | Bombardiro Crocodilo |
| Boss level | 20 |
| Level hero kỳ vọng | 20 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal |
| Slot đội hình | 4 |
| Hệ thống đã mở | formation preset, enemy giáp dày |
| Enemy/Boss pool | Bombardiro Crocodilo, Meat Shield Host |
| Điều kiện mở boss | Hoàn thành đủ 30/30 sao của 10 stage thường trong World 4 |
| Mục tiêu thắng | Giết boss |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 200 giây |
| Stamina cost | 12 |
| First clear EXP | 410 |
| Repeat clear EXP | 200 |

## Ý đồ thiết kế

Boss stage là bài kiểm tra cuối của World 4: **enemy tanker, giáp dày, pháo kích tuyến sau**.

Độ khó chính: enemy trâu che chắn cho sát thương tuyến sau, kéo dài trận và làm backline nguy hiểm.

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
| Mason Rook | Core Engineer | 30 | 24 giây | tạo Aegis Energy, mạnh trong trận dài |
| Riven Hal | Resonance Blade | 25 | 20 giây | áp sát elite/support/boss phụ |

## Enemy và boss trong màn

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Bombardiro Crocodilo | boss | cơ chế riêng của boss stage |
| Meat Shield Host | 5 | tanker infected, che chắn cho enemy phía sau |

## Boss mechanic

- boss pháo kích tuyến sau
- kích hoạt giáp dày trong thời gian ngắn
- cần áp sát hoặc tập trung damage đúng thời điểm

## Timeline V0.1

| Thời điểm | Sự kiện | Mục đích |
| --------: | ------- | -------- |
| 0s | Boss xuất hiện cùng 4 Meat Shield Host | mở trận, buộc người chơi dựng tuyến ngay |
| 25s | 5 Meat Shield Host | tăng áp lực tuyến trước |
| 50s | Boss kích hoạt mechanic 1 | giới thiệu cơ chế boss chính |
| 70s | 3 Patch Beast, 3 Meat Shield Host | trộn enemy để kéo người chơi khỏi việc chỉ focus boss |
| 60% HP | Boss chuyển phase 2 | tăng cường cơ chế chính của world |
| 105s | Boss gọi wave phụ lớn | kiểm tra khả năng clear wave |
| 30% HP | Boss chuyển phase cuối | tạo spike cuối trận |
| 150s | Finale wave: 5 Meat Shield Host, 3 Patch Beast | ép kết thúc trước khi cổng vỡ |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng boss stage |
| 2 sao | Phá giáp Bombardiro Crocodilo trước mốc 150 giây |
| 3 sao | Không để hero backline bị hạ |

## Vì sao boss này khó

- Boss gom toàn bộ cơ chế chính của world vào một trận dài hơn stage thường.
- Người chơi phải chia sát thương giữa boss, wave phụ và mục tiêu mechanic.
- Objective sao phụ yêu cầu xử lý mechanic tốt, không chỉ thắng bằng level cao.
- Nếu kéo dài trận, wave phụ và mechanic boss sẽ bào cổng Aegis hoặc làm đội hình mất nhịp.

## Cách vượt qua

- dùng Riven để áp sát mục tiêu giáp dày/support
- Mira cần ưu tiên Scream Spitter
- Kael giữ tuyến để Patch Beast không chạm cổng
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

