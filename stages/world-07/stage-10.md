# World 07 Stage 10 - Thành Phố Méo Giọng

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 7 - Thành Phố Méo Giọng |
| Stage | 10 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 35 |
| Monster level | 35 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn, Atlas-09 |
| Slot đội hình | 4 |
| Hệ thống đã mở | Overdrive Titan, challenge world cũ, replay farm EXP world cũ |
| Enemy pool | Phase Stalker, Mute Leech, Bone Drummer |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 155 giây |
| Wave budget mục tiêu | 78 |
| Stamina cost | 10 |
| First clear EXP | 215 |
| Repeat clear EXP | 111 |

## Ý đồ thiết kế

Stage này dùng vai trò: **bài kiểm tra tổng hợp trước boss**.

Trọng tâm world: backline dive, elite nhiều, áp lực tuyến sau.

Độ khó chính: Phase Stalker và boss đánh vào backline, buộc người chơi giữ formation kín.

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
| Phase Stalker | 6 | áp sát backline nếu tuyến trước có khoảng trống |
| Mute Leech | 4 | rút nộ và gây Signal Drain, khắc chế đội hình phụ thuộc skill nộ |
| Bone Drummer | 4 | buff tốc độ cho enemy, làm wave trở nên dày hơn |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Bone Drummer | 8 | mở đầu, cho người chơi setup tuyến |
| 19s | 1 Mute Leech, 2 Bone Drummer | 12 | giới thiệu áp lực chính với số lượng vừa |
| 39s | 1 Mute Leech, 1 Phase Stalker, 2 Bone Drummer | 18 | tăng overlap và buộc deploy đúng nhịp |
| 62s | 1 Mute Leech, 1 Phase Stalker, 2 Bone Drummer | 18 | tăng overlap và buộc deploy đúng nhịp |
| 90s | 1 Mute Leech, 1 Phase Stalker, 2 Bone Drummer | 18 | tăng overlap và buộc deploy đúng nhịp |
| 116s | 1 Mute Leech, 1 Phase Stalker, 2 Bone Drummer | 18 | tăng overlap và buộc deploy đúng nhịp |
| 140s | 1 Phase Stalker, 1 Mute Leech, 2 Bone Drummer | 18 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Hoàn thành trong 130 giây |
| 3 sao | Không để quá 1 hero bị hạ |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 7: backline dive, elite nhiều, áp lực tuyến sau.
- Enemy pool hiện tại là **Phase Stalker, Mute Leech, Bone Drummer**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Hoàn thành trong 130 giây** và **Không để quá 1 hero bị hạ**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Hạ Bone Drummer sớm; nếu để buff nhiều lần, wave sau sẽ vượt budget thực tế.
- Không để Mute Leech sống lâu cạnh tanker hoặc damage chính vì Rage Leech làm trễ skill nộ.
- Giữ tanker đúng vị trí để Phase Stalker không có khoảng trống lao vào backline.
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

