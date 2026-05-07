# World 03 Stage 08 - Khu Dân Cư Im Lặng

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 3 - Khu Dân Cư Im Lặng |
| Stage | 8 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 14 |
| Monster level | 14 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal |
| Slot đội hình | 4 |
| Hệ thống đã mở | debuff, nâng skill nộ bậc 2, objective chống debuff |
| Enemy pool | Scream Spitter, Mute Leech, Blank Walker |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 125 giây |
| Wave budget mục tiêu | 64 |
| Stamina cost | 6 |
| First clear EXP | 145 |
| Repeat clear EXP | 75 |

## Ý đồ thiết kế

Stage này dùng vai trò: **stress test cơ chế chính của world**.

Trọng tâm world: nhiễu âm, Signal Drain, Desync.

Độ khó chính: enemy làm chậm tích nộ, gây đánh hụt và rút nộ, khiến skill nộ không ra đúng nhịp.

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

Gợi ý đội hình:

- Luôn cần một tuyến trước ổn định trước khi deploy damage/support.
- Nếu stage có enemy support, ưu tiên damage dealer hoặc assassin xử lý mục tiêu đó sớm.
- Nếu stage có nhiều enemy tốc độ cao, giữ Aegis Energy dự phòng để deploy chặn nhịp.

## Enemy trong stage

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Scream Spitter | 4 | bắn xa và gây Desync, ép người chơi xử lý support |
| Mute Leech | 4 | rút nộ và gây Signal Drain, khắc chế đội hình phụ thuộc skill nộ |
| Blank Walker | 1 | enemy nền, đông và chậm, dùng để ép tuyến |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 5 Blank Walker | 5 | mở đầu, cho người chơi setup tuyến |
| 15s | 1 Scream Spitter, 4 Blank Walker | 8 | giới thiệu áp lực chính với số lượng vừa |
| 31s | 1 Scream Spitter, 1 Mute Leech, 2 Blank Walker | 10 | tăng overlap và buộc deploy đúng nhịp |
| 50s | 1 Scream Spitter, 1 Mute Leech, 2 Blank Walker | 10 | tăng overlap và buộc deploy đúng nhịp |
| 72s | 1 Scream Spitter, 1 Mute Leech, 2 Blank Walker | 10 | tăng overlap và buộc deploy đúng nhịp |
| 94s | 1 Scream Spitter, 1 Mute Leech, 3 Blank Walker | 11 | tăng overlap và buộc deploy đúng nhịp |
| 112s | 1 Mute Leech, 1 Scream Spitter, 4 Blank Walker | 12 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Mute Leech gây Rage Leech không quá 3 lần |
| 3 sao | Hero bị Desync không quá 3 lần |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 3: nhiễu âm, Signal Drain, Desync.
- Enemy pool hiện tại là **Scream Spitter, Mute Leech, Blank Walker**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Mute Leech gây Rage Leech không quá 3 lần** và **Hero bị Desync không quá 3 lần**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Blank Walker chậm nhưng đông, dùng damage tầm xa để bào dần thay vì deploy quá nhiều tanker.
- Ưu tiên hạ Scream Spitter trước khi Desync làm đội hình đánh hụt quá nhiều.
- Không để Mute Leech sống lâu cạnh tanker hoặc damage chính vì Rage Leech làm trễ skill nộ.
- Muốn lấy 3 sao thì phải chơi theo objective, không chỉ thắng bằng cách kéo dài trận.

## Dấu hiệu stage đang quá khó

- Người chơi đúng level kỳ vọng nhưng thua trước 50% thời lượng stage.
- Enemy đặc biệt chạm cổng trước khi người chơi có cơ hội phản ứng.
- Objective 2 sao thất bại gần như chắc chắn dù người chơi deploy đúng.

## Dấu hiệu stage đang quá dễ

- Người chơi không cần đổi thứ tự deploy vẫn thắng ổn định.
- Wave cuối không gây thêm áp lực so với wave giữa.
- Người chơi đạt 3 sao dù bỏ qua enemy đặc biệt hoặc cơ chế chính.

