# World 05 Stage 05 - Chợ Đêm Không Ngủ

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 5 - Chợ Đêm Không Ngủ |
| Stage | 5 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 23 |
| Monster level | 23 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn |
| Slot đội hình | 4 |
| Hệ thống đã mở | Aegis Medic, thanh nộ hiển thị rõ |
| Enemy pool | Bone Drummer, Meat Shield Host |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 120 giây |
| Wave budget mục tiêu | 46 |
| Stamina cost | 8 |
| First clear EXP | 160 |
| Repeat clear EXP | 85 |

## Ý đồ thiết kế

Stage này dùng vai trò: **tăng áp lực giữa world bằng wave hỗn hợp**.

Trọng tâm world: wave đông, enemy haste, nhịp nhanh.

Độ khó chính: Bone Drummer tăng tốc đàn, runner tận dụng khoảng trống, tanker bị knockback.

Luật thắng/thua của stage thường:

- Người chơi thắng khi phá được ổ infected/cổng brainrot bên phải.
- Enemy luôn tiến về bên trái để tấn công cổng Aegis.
- Người chơi thua nếu cổng Aegis bị phá.

## Modifier riêng của stage

Nhịp xung môi trường gây lực đẩy lùi tuyến trước theo chu kỳ. Hiệu ứng này dùng để phục vụ objective liên quan tanker/knockback.
Stage có side wave phụ ngoài wave chính. Side wave cần được hạ nhanh để không chồng vào wave kế tiếp.

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
| Bone Drummer | 4 | buff tốc độ cho enemy, làm wave trở nên dày hơn |
| Meat Shield Host | 5 | tanker infected, che chắn cho enemy phía sau |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Bone Drummer | 8 | mở đầu, cho người chơi setup tuyến |
| 18s | 1 Meat Shield Host, 2 Bone Drummer | 13 | giới thiệu áp lực chính với số lượng vừa |
| 37s | 1 Meat Shield Host, 2 Bone Drummer | 13 | tăng overlap và buộc deploy đúng nhịp |
| 60s | 1 Meat Shield Host, 2 Bone Drummer | 13 | tăng overlap và buộc deploy đúng nhịp |
| 84s | 1 Meat Shield Host, 2 Bone Drummer | 13 | tăng overlap và buộc deploy đúng nhịp |
| 103s | 1 Meat Shield Host, 2 Bone Drummer | 13 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Hạ mỗi side wave trong 15 giây kể từ lúc spawn |
| 3 sao | Tanker bị knockback nặng không quá 2 lần |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 5: wave đông, enemy haste, nhịp nhanh.
- Enemy pool hiện tại là **Bone Drummer, Meat Shield Host**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Hạ mỗi side wave trong 15 giây kể từ lúc spawn** và **Tanker bị knockback nặng không quá 2 lần**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Hạ Bone Drummer sớm; nếu để buff nhiều lần, wave sau sẽ vượt budget thực tế.
- Dùng damage xuyên giáp hoặc Riven để phá Meat Shield Host, tránh để nó che support phía sau.
- Muốn lấy 3 sao thì phải chơi theo objective, không chỉ thắng bằng cách kéo dài trận.

## Dấu hiệu stage đang quá khó

- Người chơi đúng level kỳ vọng nhưng thua trước 50% thời lượng stage.
- Enemy đặc biệt chạm cổng trước khi người chơi có cơ hội phản ứng.
- Objective 2 sao thất bại gần như chắc chắn dù người chơi deploy đúng.

## Dấu hiệu stage đang quá dễ

- Người chơi không cần đổi thứ tự deploy vẫn thắng ổn định.
- Wave cuối không gây thêm áp lực so với wave giữa.
- Người chơi đạt 3 sao dù bỏ qua enemy đặc biệt hoặc cơ chế chính.

