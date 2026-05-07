# World 06 Boss - Dottore Mozzarella

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 6 - Bệnh Viện Đen |
| Loại màn | Boss stage |
| Boss | Dottore Mozzarella |
| Boss level | 30 |
| Level hero kỳ vọng | 30 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn |
| Slot đội hình | 4 |
| Hệ thống đã mở | counter hồi máu, chống Toxic Suppression, nâng skill nộ bậc 3 |
| Enemy/Boss pool | Dottore Mozzarella, Regrowth Host |
| Điều kiện mở boss | Hoàn thành đủ 30/30 sao của 10 stage thường trong World 6 |
| Mục tiêu thắng | Giết boss |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 220 giây |
| Stamina cost | 12 |
| First clear EXP | 490 |
| Repeat clear EXP | 240 |

## Ý đồ thiết kế

Boss stage là bài kiểm tra cuối của World 6: **hồi máu enemy, hồi sinh, Toxic Suppression**.

Độ khó chính: Regrowth Host và boss kéo dài wave, Toxic Suppression làm Iris hồi kém hiệu quả.

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
| Iris Venn | Aegis Medic | 35 | 26 giây | hồi máu, giải debuff |

## Enemy và boss trong màn

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Dottore Mozzarella | boss | cơ chế riêng của boss stage |
| Regrowth Host | 5 | hồi máu hoặc tái kích hoạt enemy, kéo dài wave |

## Boss mechanic

- hồi máu cho enemy
- hồi sinh quái đã chết
- tạo vùng Toxic Suppression

## Timeline V0.1

| Thời điểm | Sự kiện | Mục đích |
| --------: | ------- | -------- |
| 0s | Boss xuất hiện cùng 4 Regrowth Host | mở trận, buộc người chơi dựng tuyến ngay |
| 25s | 5 Regrowth Host | tăng áp lực tuyến trước |
| 50s | Boss kích hoạt mechanic 1 | giới thiệu cơ chế boss chính |
| 70s | 3 Scream Spitter, 3 Regrowth Host | trộn enemy để kéo người chơi khỏi việc chỉ focus boss |
| 60% HP | Boss chuyển phase 2 | tăng cường cơ chế chính của world |
| 105s | Boss gọi wave phụ lớn | kiểm tra khả năng clear wave |
| 30% HP | Boss chuyển phase cuối | tạo spike cuối trận |
| 150s | Finale wave: 5 Regrowth Host, 3 Scream Spitter | ép kết thúc trước khi cổng vỡ |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng boss stage |
| 2 sao | Dottore Mozzarella làm enemy hồi sinh không quá 6 lần |
| 3 sao | Hero bị Toxic Suppression không quá 5 lần |

## Vì sao boss này khó

- Boss gom toàn bộ cơ chế chính của world vào một trận dài hơn stage thường.
- Người chơi phải chia sát thương giữa boss, wave phụ và mục tiêu mechanic.
- Objective sao phụ yêu cầu xử lý mechanic tốt, không chỉ thắng bằng level cao.
- Nếu kéo dài trận, wave phụ và mechanic boss sẽ bào cổng Aegis hoặc làm đội hình mất nhịp.

## Cách vượt qua

- focus Regrowth Host ngay khi spawn
- Riven dùng để cắt healer/support
- Iris cần giữ tuyến sống nhưng không thể bỏ qua Toxic Suppression
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

