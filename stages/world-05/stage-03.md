# World 05 Stage 03 - Chợ Đêm Không Ngủ

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 5 - Chợ Đêm Không Ngủ |
| Stage | 3 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 22 |
| Monster level | 22 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn |
| Slot đội hình | 4 |
| Hệ thống đã mở | Aegis Medic, thanh nộ hiển thị rõ |
| Enemy pool | Twitch Runner, Bone Drummer |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 110 giây |
| Wave budget mục tiêu | 34 |
| Stamina cost | 8 |
| First clear EXP | 150 |
| Repeat clear EXP | 81 |

## Ý đồ thiết kế

Stage này dùng vai trò: **giới thiệu enemy hoặc cơ chế phụ đầu tiên**.

Trọng tâm world: wave đông, enemy haste, nhịp nhanh.

Độ khó chính: Bone Drummer tăng tốc đàn, runner tận dụng khoảng trống, tanker bị knockback.

Luật thắng/thua của stage thường:

- Người chơi thắng khi phá được ổ infected/cổng brainrot bên phải.
- Enemy luôn tiến về bên trái để tấn công cổng Aegis.
- Người chơi thua nếu cổng Aegis bị phá.

## Modifier riêng của stage

Nhịp xung môi trường gây lực đẩy lùi tuyến trước theo chu kỳ. Hiệu ứng này dùng để phục vụ objective liên quan tanker/knockback.

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
| Twitch Runner | 2 | chạy nhanh, kiểm tra khả năng giữ cổng và deploy đúng nhịp |
| Bone Drummer | 4 | buff tốc độ cho enemy, làm wave trở nên dày hơn |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Twitch Runner | 4 | mở đầu, cho người chơi setup tuyến |
| 16s | 1 Bone Drummer, 2 Twitch Runner | 8 | giới thiệu áp lực chính với số lượng vừa |
| 34s | 1 Bone Drummer, 2 Twitch Runner | 8 | tăng overlap và buộc deploy đúng nhịp |
| 55s | 1 Bone Drummer, 2 Twitch Runner | 8 | tăng overlap và buộc deploy đúng nhịp |
| 77s | 1 Bone Drummer, 2 Twitch Runner | 8 | tăng overlap và buộc deploy đúng nhịp |
| 95s | 1 Bone Drummer, 2 Twitch Runner | 8 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Tanker bị knockback nặng không quá 2 lần |
| 3 sao | Hoàn thành trong 135 giây |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 5: wave đông, enemy haste, nhịp nhanh.
- Enemy pool hiện tại là **Twitch Runner, Bone Drummer**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Tanker bị knockback nặng không quá 2 lần** và **Hoàn thành trong 135 giây**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Giữ một lượt deploy hoặc cooldown để chặn Twitch Runner khi chúng spawn theo cặp.
- Hạ Bone Drummer sớm; nếu để buff nhiều lần, wave sau sẽ vượt budget thực tế.
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

