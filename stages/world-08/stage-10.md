# World 08 Stage 10 - Đài Phát Tín Hiệu

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 8 - Đài Phát Tín Hiệu |
| Stage | 10 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 40 |
| Monster level | 40 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn, Atlas-09 |
| Slot đội hình | 5 |
| Hệ thống đã mở | formation slot thứ 5, node phụ, khóa nộ nâng cao |
| Enemy pool | Signal Host, Scream Spitter, Mute Leech |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 160 giây |
| Wave budget mục tiêu | 78 |
| Stamina cost | 10 |
| First clear EXP | 230 |
| Repeat clear EXP | 119 |

## Ý đồ thiết kế

Stage này dùng vai trò: **bài kiểm tra tổng hợp trước boss**.

Trọng tâm world: node phát sóng, khóa nộ, Signal Drain toàn bản đồ.

Độ khó chính: Signal Host và boss khóa nhịp nộ, làm skill nộ bị trễ hoặc không dùng được.

Luật thắng/thua của stage thường:

- Người chơi thắng khi phá được ổ infected/cổng brainrot bên phải.
- Enemy luôn tiến về bên trái để tấn công cổng Aegis.
- Người chơi thua nếu cổng Aegis bị phá.

## Modifier riêng của stage

Không có modifier riêng ngoài enemy composition và objective sao.

## Trạng thái người chơi

| Hero | Class | Deploy cost | Cooldown | Vai trò |
| ---- | ----- | ----------: | -------- | ------- |
| Kael Voss | Vanguard Breaker | 20 | 18 giây | tanker tuyến trước, giữ cổng |
| Mira Sane | Pulse Ranger | 15 | 14 giây | bắn xa, xử lý runner/support |
| Mason Rook | Core Engineer | 30 | 24 giây | tạo Aegis Energy, mạnh trong trận dài |
| Riven Hal | Resonance Blade | 25 | 20 giây | áp sát elite/support/boss phụ |
| Iris Venn | Aegis Medic | 35 | 26 giây | hồi máu, giải debuff |
| Atlas-09 | Overdrive Titan | 60 | 45 giây | unit hạng nặng, phá wave lớn và boss |

Gợi ý đội hình:

- Luôn cần một tuyến trước ổn định trước khi deploy damage/support.
- Nếu stage có enemy support, ưu tiên damage dealer hoặc assassin xử lý mục tiêu đó sớm.
- Nếu stage có nhiều enemy tốc độ cao, giữ Aegis Energy dự phòng để deploy chặn nhịp.

## Enemy trong stage

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Signal Host | 6 | phát Signal Drain diện rộng, buộc người chơi ưu tiên focus |
| Scream Spitter | 4 | bắn xa và gây Desync, ép người chơi xử lý support |
| Mute Leech | 4 | rút nộ và gây Signal Drain, khắc chế đội hình phụ thuộc skill nộ |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Mute Leech | 8 | mở đầu, cho người chơi setup tuyến |
| 19s | 1 Scream Spitter, 2 Mute Leech | 12 | giới thiệu áp lực chính với số lượng vừa |
| 40s | 1 Scream Spitter, 1 Signal Host, 2 Mute Leech | 18 | tăng overlap và buộc deploy đúng nhịp |
| 64s | 1 Scream Spitter, 1 Signal Host, 2 Mute Leech | 18 | tăng overlap và buộc deploy đúng nhịp |
| 93s | 1 Scream Spitter, 1 Signal Host, 2 Mute Leech | 18 | tăng overlap và buộc deploy đúng nhịp |
| 120s | 1 Scream Spitter, 1 Signal Host, 2 Mute Leech | 18 | tăng overlap và buộc deploy đúng nhịp |
| 144s | 1 Signal Host, 1 Scream Spitter, 2 Mute Leech | 18 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Phá toàn bộ Signal Host trước khi wave cuối vào cổng |
| 3 sao | Hoàn thành trong 135 giây |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 8: node phát sóng, khóa nộ, Signal Drain toàn bản đồ.
- Enemy pool hiện tại là **Signal Host, Scream Spitter, Mute Leech**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Phá toàn bộ Signal Host trước khi wave cuối vào cổng** và **Hoàn thành trong 135 giây**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Ưu tiên hạ Scream Spitter trước khi Desync làm đội hình đánh hụt quá nhiều.
- Không để Mute Leech sống lâu cạnh tanker hoặc damage chính vì Rage Leech làm trễ skill nộ.
- Signal Host là mục tiêu ưu tiên cao; nếu để pulse nhiều lần, đội hình sẽ mất nhịp nộ.
- Nếu muốn lấy sao tốc độ, deploy damage sớm hơn và không kéo trận bằng đội hình quá thủ.
- Muốn lấy 3 sao thì phải chơi theo objective, không chỉ thắng bằng cách kéo dài trận.

## Dấu hiệu stage đang quá khó

- Người chơi đúng level kỳ vọng nhưng thua trước 50% thời lượng stage.
- Enemy đặc biệt chạm cổng trước khi người chơi có cơ hội phản ứng.
- Objective 2 sao thất bại gần như chắc chắn dù người chơi deploy đúng.

## Dấu hiệu stage đang quá dễ

- Người chơi không cần đổi thứ tự deploy vẫn thắng ổn định.
- Wave cuối không gây thêm áp lực so với wave giữa.
- Người chơi đạt 3 sao dù bỏ qua enemy đặc biệt hoặc cơ chế chính.

