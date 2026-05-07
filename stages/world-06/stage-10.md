# World 06 Stage 10 - Bệnh Viện Đen

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 6 - Bệnh Viện Đen |
| Stage | 10 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 30 |
| Monster level | 30 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn |
| Slot đội hình | 4 |
| Hệ thống đã mở | counter hồi máu, chống Toxic Suppression, nâng skill nộ bậc 3 |
| Enemy pool | Regrowth Host, Scream Spitter, Mute Leech |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 150 giây |
| Wave budget mục tiêu | 78 |
| Stamina cost | 8 |
| First clear EXP | 200 |
| Repeat clear EXP | 103 |

## Ý đồ thiết kế

Stage này dùng vai trò: **bài kiểm tra tổng hợp trước boss**.

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
| Scream Spitter | 4 | bắn xa và gây Desync, ép người chơi xử lý support |
| Mute Leech | 4 | rút nộ và gây Signal Drain, khắc chế đội hình phụ thuộc skill nộ |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Mute Leech | 8 | mở đầu, cho người chơi setup tuyến |
| 18s | 1 Scream Spitter, 2 Mute Leech | 12 | giới thiệu áp lực chính với số lượng vừa |
| 38s | 1 Scream Spitter, 1 Regrowth Host, 2 Mute Leech | 17 | tăng overlap và buộc deploy đúng nhịp |
| 60s | 1 Scream Spitter, 1 Regrowth Host, 2 Mute Leech | 17 | tăng overlap và buộc deploy đúng nhịp |
| 87s | 1 Scream Spitter, 1 Regrowth Host, 2 Mute Leech | 17 | tăng overlap và buộc deploy đúng nhịp |
| 112s | 1 Scream Spitter, 1 Regrowth Host, 2 Mute Leech | 17 | tăng overlap và buộc deploy đúng nhịp |
| 135s | 1 Regrowth Host, 1 Scream Spitter, 2 Mute Leech | 17 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Regrowth Host hồi máu không quá 2 lần |
| 3 sao | Không để hero bị hạ |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 6: hồi máu enemy, hồi sinh, Toxic Suppression.
- Enemy pool hiện tại là **Regrowth Host, Scream Spitter, Mute Leech**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Regrowth Host hồi máu không quá 2 lần** và **Không để hero bị hạ**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Ưu tiên hạ Scream Spitter trước khi Desync làm đội hình đánh hụt quá nhiều.
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

