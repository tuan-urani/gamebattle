# World 06 Stage 06 - Bệnh Viện Đen

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 6 - Bệnh Viện Đen |
| Stage | 6 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 28 |
| Monster level | 28 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn |
| Slot đội hình | 4 |
| Hệ thống đã mở | counter hồi máu, chống Toxic Suppression, nâng skill nộ bậc 3 |
| Enemy pool | Regrowth Host, Mute Leech |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 130 giây |
| Wave budget mục tiêu | 52 |
| Stamina cost | 8 |
| First clear EXP | 180 |
| Repeat clear EXP | 95 |

## Ý đồ thiết kế

Stage này dùng vai trò: **kiểm tra nhịp deploy và counter bằng đội hình hợp lý**.

Trọng tâm world: hồi máu enemy, hồi sinh, Toxic Suppression.

Độ khó chính: Regrowth Host và boss kéo dài wave, Toxic Suppression làm Iris hồi kém hiệu quả.

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

Gợi ý đội hình:

- Luôn cần một tuyến trước ổn định trước khi deploy damage/support.
- Nếu stage có enemy support, ưu tiên damage dealer hoặc assassin xử lý mục tiêu đó sớm.
- Nếu stage có nhiều enemy tốc độ cao, giữ Aegis Energy dự phòng để deploy chặn nhịp.

## Enemy trong stage

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Regrowth Host | 5 | hồi máu hoặc tái kích hoạt enemy, kéo dài wave |
| Mute Leech | 4 | rút nộ và gây Signal Drain, khắc chế đội hình phụ thuộc skill nộ |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Mute Leech | 8 | mở đầu, cho người chơi setup tuyến |
| 20s | 1 Regrowth Host, 2 Mute Leech | 13 | giới thiệu áp lực chính với số lượng vừa |
| 40s | 1 Regrowth Host, 2 Mute Leech | 13 | tăng overlap và buộc deploy đúng nhịp |
| 65s | 1 Regrowth Host, 2 Mute Leech | 13 | tăng overlap và buộc deploy đúng nhịp |
| 91s | 1 Regrowth Host, 2 Mute Leech | 13 | tăng overlap và buộc deploy đúng nhịp |
| 112s | 1 Regrowth Host, 2 Mute Leech | 13 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Mute Leech gây Rage Leech không quá 5 lần |
| 3 sao | Hero bị Toxic Suppression không quá 4 lần |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 6: hồi máu enemy, hồi sinh, Toxic Suppression.
- Enemy pool hiện tại là **Regrowth Host, Mute Leech**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Mute Leech gây Rage Leech không quá 5 lần** và **Hero bị Toxic Suppression không quá 4 lần**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Không để Mute Leech sống lâu cạnh tanker hoặc damage chính vì Rage Leech làm trễ skill nộ.
- Burst Regrowth Host ngay khi spawn, không để nó kéo dài wave bằng hồi máu.
- Muốn lấy 3 sao thì phải chơi theo objective, không chỉ thắng bằng cách kéo dài trận.

## Dấu hiệu stage đang quá khó

- Người chơi đúng level kỳ vọng nhưng thua trước 50% thời lượng stage.
- Enemy đặc biệt chạm cổng trước khi người chơi có cơ hội phản ứng.
- Objective 2 sao thất bại gần như chắc chắn dù người chơi deploy đúng.

## Dấu hiệu stage đang quá dễ

- Người chơi không cần đổi thứ tự deploy vẫn thắng ổn định.
- Wave cuối không gây thêm áp lực so với wave giữa.
- Người chơi đạt 3 sao dù bỏ qua enemy đặc biệt hoặc cơ chế chính.

