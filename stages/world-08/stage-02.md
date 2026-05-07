# World 08 Stage 02 - Đài Phát Tín Hiệu

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 8 - Đài Phát Tín Hiệu |
| Stage | 2 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 36 |
| Monster level | 36 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn, Atlas-09 |
| Slot đội hình | 5 |
| Hệ thống đã mở | formation slot thứ 5, node phụ, khóa nộ nâng cao |
| Enemy pool | Signal Host, Scream Spitter |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 120 giây |
| Wave budget mục tiêu | 28 |
| Stamina cost | 10 |
| First clear EXP | 190 |
| Repeat clear EXP | 103 |

## Ý đồ thiết kế

Stage này dùng vai trò: **củng cố theme với áp lực giữ cổng hoặc tốc độ**.

Trọng tâm world: node phát sóng, khóa nộ, Signal Drain toàn bản đồ.

Độ khó chính: Signal Host và boss khóa nhịp nộ, làm skill nộ bị trễ hoặc không dùng được.

Luật thắng/thua của stage thường:

- Người chơi thắng khi phá được ổ infected/cổng brainrot bên phải.
- Enemy luôn tiến về bên trái để tấn công cổng Aegis.
- Người chơi thua nếu cổng Aegis bị phá.

## Modifier riêng của stage

Stage có pulse nhiễu diện rộng theo chu kỳ. Pulse được tính cho objective chống debuff.

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

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Scream Spitter | 8 | mở đầu, cho người chơi setup tuyến |
| 22s | 1 Signal Host, 2 Scream Spitter | 14 | giới thiệu áp lực chính với số lượng vừa |
| 46s | 1 Signal Host, 2 Scream Spitter | 14 | tăng overlap và buộc deploy đúng nhịp |
| 74s | 1 Signal Host, 2 Scream Spitter | 14 | tăng overlap và buộc deploy đúng nhịp |
| 98s | 1 Signal Host, 2 Scream Spitter | 14 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Signal Drain toàn đội không quá 5 lần |
| 3 sao | Hoàn thành trong 155 giây |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 8: node phát sóng, khóa nộ, Signal Drain toàn bản đồ.
- Enemy pool hiện tại là **Signal Host, Scream Spitter**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Signal Drain toàn đội không quá 5 lần** và **Hoàn thành trong 155 giây**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Ưu tiên hạ Scream Spitter trước khi Desync làm đội hình đánh hụt quá nhiều.
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

