# World 10 Stage 05 - Lõi Phát Xạ

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 10 - Lõi Phát Xạ |
| Stage | 5 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 48 |
| Monster level | 48 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn, Atlas-09 |
| Slot đội hình | 5 |
| Hệ thống đã mở | full system, xung nghịch pha, boss cuối nhiều phase |
| Enemy pool | Core Guardian, Signal Host, Red Host |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 145 giây |
| Wave budget mục tiêu | 46 |
| Stamina cost | 10 |
| First clear EXP | 235 |
| Repeat clear EXP | 125 |

## Ý đồ thiết kế

Stage này dùng vai trò: **tăng áp lực giữa world bằng wave hỗn hợp**.

Trọng tâm world: tổng hợp toàn bộ cơ chế cũ, boss cuối nhiều phase.

Độ khó chính: Core Guardian ép tuyến, debuff diện rộng làm trễ skill nộ, elite cũ xuất hiện cùng lúc.

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
| Core Guardian | 10 | elite cuối game, chậm nhưng ép tuyến cực mạnh |
| Signal Host | 6 | phát Signal Drain diện rộng, buộc người chơi ưu tiên focus |
| Red Host | 8 | tiến hóa trong trận, càng để lâu càng nguy hiểm |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Signal Host | 12 | mở đầu, cho người chơi setup tuyến |
| 22s | 1 Red Host, 2 Signal Host | 20 | giới thiệu áp lực chính với số lượng vừa |
| 45s | 1 Red Host, 2 Signal Host | 20 | tăng overlap và buộc deploy đúng nhịp |
| 72s | 1 Red Host, 2 Signal Host | 20 | tăng overlap và buộc deploy đúng nhịp |
| 102s | 1 Red Host, 2 Signal Host | 20 | tăng overlap và buộc deploy đúng nhịp |
| 125s | 1 Core Guardian, 1 Red Host, 2 Signal Host | 30 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Không để quá 2 hero bị hạ |
| 3 sao | Debuff diện rộng không quá 6 lần |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 10: tổng hợp toàn bộ cơ chế cũ, boss cuối nhiều phase.
- Enemy pool hiện tại là **Core Guardian, Signal Host, Red Host**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Không để quá 2 hero bị hạ** và **Debuff diện rộng không quá 6 lần**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Signal Host là mục tiêu ưu tiên cao; nếu để pulse nhiều lần, đội hình sẽ mất nhịp nộ.
- Red Host phải bị burst trước khi evolve, đặc biệt ở các wave giữa và cuối.
- Core Guardian cần bị giữ từ xa bằng tanker khỏe và burst damage; không để nó chạm cổng.
- Muốn lấy 3 sao thì phải chơi theo objective, không chỉ thắng bằng cách kéo dài trận.

## Dấu hiệu stage đang quá khó

- Người chơi đúng level kỳ vọng nhưng thua trước 50% thời lượng stage.
- Enemy đặc biệt chạm cổng trước khi người chơi có cơ hội phản ứng.
- Objective 2 sao thất bại gần như chắc chắn dù người chơi deploy đúng.

## Dấu hiệu stage đang quá dễ

- Người chơi không cần đổi thứ tự deploy vẫn thắng ổn định.
- Wave cuối không gây thêm áp lực so với wave giữa.
- Người chơi đạt 3 sao dù bỏ qua enemy đặc biệt hoặc cơ chế chính.

