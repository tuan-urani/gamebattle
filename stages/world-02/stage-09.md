# World 02 Stage 09 - Xa Lộ Di Tản

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 2 - Xa Lộ Di Tản |
| Stage | 9 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 10 |
| Monster level | 10 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook |
| Slot đội hình | 4 |
| Hệ thống đã mở | Core Engineer, bẫy làm chậm, stage thử thách elite |
| Enemy pool | Twitch Runner, Jaw Crawler, Static Carrier |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 125 giây |
| Wave budget mục tiêu | 70 |
| Stamina cost | 6 |
| First clear EXP | 135 |
| Repeat clear EXP | 69 |

## Ý đồ thiết kế

Stage này dùng vai trò: **endurance trước màn cuối, ít khoảng nghỉ hơn**.

Trọng tâm world: enemy tốc độ cao, tuyến phòng thủ dễ bị xuyên.

Độ khó chính: runner và crawler ép cổng liên tục, người chơi bị phạt nếu deploy tanker muộn.

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

Gợi ý đội hình:

- Luôn cần một tuyến trước ổn định trước khi deploy damage/support.
- Nếu stage có enemy support, ưu tiên damage dealer hoặc assassin xử lý mục tiêu đó sớm.
- Nếu stage có nhiều enemy tốc độ cao, giữ Aegis Energy dự phòng để deploy chặn nhịp.

## Enemy trong stage

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Twitch Runner | 2 | chạy nhanh, kiểm tra khả năng giữ cổng và deploy đúng nhịp |
| Jaw Crawler | 2 | bò thấp, tạo áp lực nếu tuyến bắn xa xử lý chậm |
| Static Carrier | 3 | chết phát nổ Signal Drain, nguy hiểm nếu nổ sát cổng |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 1 Twitch Runner, 2 Jaw Crawler | 6 | mở đầu, cho người chơi setup tuyến |
| 15s | 1 Twitch Runner, 3 Jaw Crawler | 8 | giới thiệu áp lực chính với số lượng vừa |
| 31s | 1 Twitch Runner, 1 Static Carrier, 2 Jaw Crawler | 9 | tăng overlap và buộc deploy đúng nhịp |
| 50s | 1 Twitch Runner, 1 Static Carrier, 2 Jaw Crawler | 9 | tăng overlap và buộc deploy đúng nhịp |
| 72s | 1 Twitch Runner, 1 Static Carrier, 3 Jaw Crawler | 11 | tăng overlap và buộc deploy đúng nhịp |
| 94s | 1 Twitch Runner, 1 Static Carrier, 4 Jaw Crawler | 13 | tăng overlap và buộc deploy đúng nhịp |
| 112s | 1 Static Carrier, 1 Twitch Runner, 4 Jaw Crawler | 13 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Không để quá 2 enemy tốc độ cao chạm cổng |
| 3 sao | Hoàn thành trong 105 giây |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 2: enemy tốc độ cao, tuyến phòng thủ dễ bị xuyên.
- Enemy pool hiện tại là **Twitch Runner, Jaw Crawler, Static Carrier**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Không để quá 2 enemy tốc độ cao chạm cổng** và **Hoàn thành trong 105 giây**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Giữ một lượt deploy hoặc cooldown để chặn Twitch Runner khi chúng spawn theo cặp.
- Jaw Crawler dễ lọt tuyến nếu chỉ dựa vào bắn xa; cần có unit giữ đường ở phía trước.
- Focus Static Carrier từ xa, tránh để nó chết trong khu vực sát cổng.
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

