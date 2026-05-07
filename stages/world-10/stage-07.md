# World 10 Stage 07 - Lõi Phát Xạ

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 10 - Lõi Phát Xạ |
| Stage | 7 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 49 |
| Monster level | 49 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn, Atlas-09 |
| Slot đội hình | 5 |
| Hệ thống đã mở | full system, xung nghịch pha, boss cuối nhiều phase |
| Enemy pool | Core Guardian, Red Host, Signal Host, Phase Stalker, Patch Beast |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 155 giây |
| Wave budget mục tiêu | 58 |
| Stamina cost | 10 |
| First clear EXP | 245 |
| Repeat clear EXP | 129 |

## Ý đồ thiết kế

Stage này dùng vai trò: **tăng mật độ hoặc đưa elite/support xuất hiện rõ hơn**.

Trọng tâm world: tổng hợp toàn bộ cơ chế cũ, boss cuối nhiều phase.

Độ khó chính: Core Guardian ép tuyến, debuff diện rộng làm trễ skill nộ, elite cũ xuất hiện cùng lúc.

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
| Core Guardian | 10 | elite cuối game, chậm nhưng ép tuyến cực mạnh |
| Red Host | 8 | tiến hóa trong trận, càng để lâu càng nguy hiểm |
| Signal Host | 6 | phát Signal Drain diện rộng, buộc người chơi ưu tiên focus |
| Phase Stalker | 6 | áp sát backline nếu tuyến trước có khoảng trống |
| Patch Beast | 7 | enemy giáp dày, chậm nhưng rất trâu và đánh đau |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Phase Stalker | 12 | mở đầu, cho người chơi setup tuyến |
| 19s | 1 Signal Host, 2 Phase Stalker | 18 | giới thiệu áp lực chính với số lượng vừa |
| 39s | 1 Signal Host, 2 Phase Stalker | 18 | tăng overlap và buộc deploy đúng nhịp |
| 62s | 1 Signal Host, 2 Phase Stalker | 18 | tăng overlap và buộc deploy đúng nhịp |
| 90s | 1 Signal Host, 2 Phase Stalker | 18 | tăng overlap và buộc deploy đúng nhịp |
| 116s | 1 Signal Host, 2 Phase Stalker | 18 | tăng overlap và buộc deploy đúng nhịp |
| 140s | 1 Core Guardian, 1 Signal Host, 2 Phase Stalker | 28 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Cổng Aegis còn trên 40% HP |
| 3 sao | Không để quá 1 hero bị hạ |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 10: tổng hợp toàn bộ cơ chế cũ, boss cuối nhiều phase.
- Enemy pool hiện tại là **Core Guardian, Red Host, Signal Host, Phase Stalker, Patch Beast**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Cổng Aegis còn trên 40% HP** và **Không để quá 1 hero bị hạ**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Patch Beast nên bị giữ xa cổng; nếu nó chạm tuyến cuối, sát thương mỗi đòn rất khó hồi lại.
- Giữ tanker đúng vị trí để Phase Stalker không có khoảng trống lao vào backline.
- Signal Host là mục tiêu ưu tiên cao; nếu để pulse nhiều lần, đội hình sẽ mất nhịp nộ.
- Red Host phải bị burst trước khi evolve, đặc biệt ở các wave giữa và cuối.
- Core Guardian cần bị giữ từ xa bằng tanker khỏe và burst damage; không để nó chạm cổng.
- Nếu objective yêu cầu giữ HP cổng, ưu tiên chặn wave hơn là greed damage lên mục tiêu xa.
- Muốn lấy 3 sao thì phải chơi theo objective, không chỉ thắng bằng cách kéo dài trận.

## Dấu hiệu stage đang quá khó

- Người chơi đúng level kỳ vọng nhưng thua trước 50% thời lượng stage.
- Enemy đặc biệt chạm cổng trước khi người chơi có cơ hội phản ứng.
- Objective 2 sao thất bại gần như chắc chắn dù người chơi deploy đúng.

## Dấu hiệu stage đang quá dễ

- Người chơi không cần đổi thứ tự deploy vẫn thắng ổn định.
- Wave cuối không gây thêm áp lực so với wave giữa.
- Người chơi đạt 3 sao dù bỏ qua enemy đặc biệt hoặc cơ chế chính.

