# World 07 Boss - Ballerino Cappuccino

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 7 - Thành Phố Méo Giọng |
| Loại màn | Boss stage |
| Boss | Ballerino Cappuccino |
| Boss level | 35 |
| Level hero kỳ vọng | 35 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn, Atlas-09 |
| Slot đội hình | 4 |
| Hệ thống đã mở | Overdrive Titan, challenge world cũ, replay farm EXP world cũ |
| Enemy/Boss pool | Ballerino Cappuccino, Phase Stalker |
| Điều kiện mở boss | Hoàn thành đủ 30/30 sao của 10 stage thường trong World 7 |
| Mục tiêu thắng | Giết boss |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 230 giây |
| Stamina cost | 15 |
| First clear EXP | 530 |
| Repeat clear EXP | 260 |

## Ý đồ thiết kế

Boss stage là bài kiểm tra cuối của World 7: **backline dive, elite nhiều, áp lực tuyến sau**.

Độ khó chính: Phase Stalker và boss đánh vào backline, buộc người chơi giữ formation kín.

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
| Atlas-09 | Overdrive Titan | 60 | 45 giây | unit hạng nặng, phá wave lớn và boss |

## Enemy và boss trong màn

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Ballerino Cappuccino | boss | cơ chế riêng của boss stage |
| Phase Stalker | 6 | áp sát backline nếu tuyến trước có khoảng trống |

## Boss mechanic

- né đòn liên tục
- lao vào tuyến sau
- chuỗi chí mạng vào hero yếu máu

## Timeline V0.1

| Thời điểm | Sự kiện | Mục đích |
| --------: | ------- | -------- |
| 0s | Boss xuất hiện cùng 4 Phase Stalker | mở trận, buộc người chơi dựng tuyến ngay |
| 25s | 5 Phase Stalker | tăng áp lực tuyến trước |
| 50s | Boss kích hoạt mechanic 1 | giới thiệu cơ chế boss chính |
| 70s | 3 Mute Leech, 3 Phase Stalker | trộn enemy để kéo người chơi khỏi việc chỉ focus boss |
| 60% HP | Boss chuyển phase 2 | tăng cường cơ chế chính của world |
| 105s | Boss gọi wave phụ lớn | kiểm tra khả năng clear wave |
| 30% HP | Boss chuyển phase cuối | tạo spike cuối trận |
| 150s | Finale wave: 5 Phase Stalker, 3 Mute Leech | ép kết thúc trước khi cổng vỡ |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng boss stage |
| 2 sao | Không để Ballerino Cappuccino hạ bất kỳ hero nào |
| 3 sao | Thắng trước khi boss dùng đủ 3 chuỗi chí mạng |

## Vì sao boss này khó

- Boss gom toàn bộ cơ chế chính của world vào một trận dài hơn stage thường.
- Người chơi phải chia sát thương giữa boss, wave phụ và mục tiêu mechanic.
- Objective sao phụ yêu cầu xử lý mechanic tốt, không chỉ thắng bằng level cao.
- Nếu kéo dài trận, wave phụ và mechanic boss sẽ bào cổng Aegis hoặc làm đội hình mất nhịp.

## Cách vượt qua

- không deploy backline khi tuyến trước chưa ổn định
- Kael phải chặn đường dive
- Atlas dùng để xoay trận khi elite quá dày
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

