# World 04 Stage 08 - Nhà Máy Gãy Xương

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 4 - Nhà Máy Gãy Xương |
| Stage | 8 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 19 |
| Monster level | 19 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook, Riven Hal |
| Slot đội hình | 4 |
| Hệ thống đã mở | formation preset, enemy giáp dày |
| Enemy pool | Meat Shield Host, Patch Beast, Scream Spitter |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 130 giây |
| Wave budget mục tiêu | 64 |
| Stamina cost | 8 |
| First clear EXP | 160 |
| Repeat clear EXP | 83 |

## Ý đồ thiết kế

Stage này dùng vai trò: **stress test cơ chế chính của world**.

Trọng tâm world: enemy tanker, giáp dày, pháo kích tuyến sau.

Độ khó chính: enemy trâu che chắn cho sát thương tuyến sau, kéo dài trận và làm backline nguy hiểm.

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
| Meat Shield Host | 5 | tanker infected, che chắn cho enemy phía sau |
| Patch Beast | 7 | enemy giáp dày, chậm nhưng rất trâu và đánh đau |
| Scream Spitter | 4 | bắn xa và gây Desync, ép người chơi xử lý support |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 2 Scream Spitter | 8 | mở đầu, cho người chơi setup tuyến |
| 16s | 1 Meat Shield Host, 2 Scream Spitter | 13 | giới thiệu áp lực chính với số lượng vừa |
| 32s | 1 Meat Shield Host, 2 Scream Spitter | 13 | tăng overlap và buộc deploy đúng nhịp |
| 52s | 1 Meat Shield Host, 2 Scream Spitter | 13 | tăng overlap và buộc deploy đúng nhịp |
| 75s | 1 Meat Shield Host, 2 Scream Spitter | 13 | tăng overlap và buộc deploy đúng nhịp |
| 98s | 1 Meat Shield Host, 1 Patch Beast, 2 Scream Spitter | 20 | tăng overlap và buộc deploy đúng nhịp |
| 117s | 1 Patch Beast, 1 Meat Shield Host, 2 Scream Spitter | 20 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Hoàn thành trong 125 giây |
| 3 sao | Không để hero backline bị hạ |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 4: enemy tanker, giáp dày, pháo kích tuyến sau.
- Enemy pool hiện tại là **Meat Shield Host, Patch Beast, Scream Spitter**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Hoàn thành trong 125 giây** và **Không để hero backline bị hạ**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Ưu tiên hạ Scream Spitter trước khi Desync làm đội hình đánh hụt quá nhiều.
- Dùng damage xuyên giáp hoặc Riven để phá Meat Shield Host, tránh để nó che support phía sau.
- Patch Beast nên bị giữ xa cổng; nếu nó chạm tuyến cuối, sát thương mỗi đòn rất khó hồi lại.
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

