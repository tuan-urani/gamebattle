# World 02 Stage 05 - Xa Lộ Di Tản

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 2 - Xa Lộ Di Tản |
| Stage | 5 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 8 |
| Monster level | 8 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook |
| Slot đội hình | 4 |
| Hệ thống đã mở | Core Engineer, bẫy làm chậm, stage thử thách elite |
| Enemy pool | Twitch Runner, Jaw Crawler |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 105 giây |
| Wave budget mục tiêu | 46 |
| Stamina cost | 6 |
| First clear EXP | 115 |
| Repeat clear EXP | 61 |

## Ý đồ thiết kế

Stage này dùng vai trò: **tăng áp lực giữa world bằng wave hỗn hợp**.

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

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 1 Twitch Runner, 2 Jaw Crawler | 6 | mở đầu, cho người chơi setup tuyến |
| 16s | 1 Twitch Runner, 2 Jaw Crawler | 6 | giới thiệu áp lực chính với số lượng vừa |
| 33s | 1 Twitch Runner, 2 Jaw Crawler | 6 | tăng overlap và buộc deploy đúng nhịp |
| 52s | 1 Twitch Runner, 3 Jaw Crawler | 8 | tăng overlap và buộc deploy đúng nhịp |
| 74s | 1 Twitch Runner, 4 Jaw Crawler | 10 | tăng overlap và buộc deploy đúng nhịp |
| 90s | 1 Twitch Runner, 4 Jaw Crawler | 10 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Cổng Aegis còn trên 65% HP |
| 3 sao | Hoàn thành trong 115 giây |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 2: enemy tốc độ cao, tuyến phòng thủ dễ bị xuyên.
- Enemy pool hiện tại là **Twitch Runner, Jaw Crawler**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Cổng Aegis còn trên 65% HP** và **Hoàn thành trong 115 giây**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Giữ một lượt deploy hoặc cooldown để chặn Twitch Runner khi chúng spawn theo cặp.
- Jaw Crawler dễ lọt tuyến nếu chỉ dựa vào bắn xa; cần có unit giữ đường ở phía trước.
- Nếu muốn lấy sao tốc độ, deploy damage sớm hơn và không kéo trận bằng đội hình quá thủ.
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

