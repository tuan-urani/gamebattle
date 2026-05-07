# World 01 Stage 07 - Trại Sơ Tán Thất Thủ

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 1 - Trại Sơ Tán Thất Thủ |
| Stage | 7 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 4 |
| Monster level | 4 |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Slot đội hình | 4 |
| Hệ thống đã mở | deploy cơ bản, Aegis Energy, EXP tướng, nâng cấp hero level |
| Enemy pool | Blank Walker, Twitch Runner, Static Carrier |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 110 giây |
| Wave budget mục tiêu | 58 |
| Stamina cost | 6 |
| First clear EXP | 110 |
| Repeat clear EXP | 57 |

## Ý đồ thiết kế

Stage này dùng vai trò: **tăng mật độ hoặc đưa elite/support xuất hiện rõ hơn**.

Trọng tâm world: tutorial, giữ cổng, xử lý runner và Static Carrier.

Độ khó chính: độ khó tăng từ số lượng walker, sang runner tốc độ cao, rồi Static Carrier gây Signal Drain.

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

Gợi ý đội hình:

- Luôn cần một tuyến trước ổn định trước khi deploy damage/support.
- Nếu stage có enemy support, ưu tiên damage dealer hoặc assassin xử lý mục tiêu đó sớm.
- Nếu stage có nhiều enemy tốc độ cao, giữ Aegis Energy dự phòng để deploy chặn nhịp.

## Enemy trong stage

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Blank Walker | 1 | enemy nền, đông và chậm, dùng để ép tuyến |
| Twitch Runner | 2 | chạy nhanh, kiểm tra khả năng giữ cổng và deploy đúng nhịp |
| Static Carrier | 3 | chết phát nổ Signal Drain, nguy hiểm nếu nổ sát cổng |

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 1 Twitch Runner, 3 Blank Walker | 5 | mở đầu, cho người chơi setup tuyến |
| 13s | 1 Twitch Runner, 5 Blank Walker | 7 | giới thiệu áp lực chính với số lượng vừa |
| 28s | 1 Twitch Runner, 1 Static Carrier, 3 Blank Walker | 8 | tăng overlap và buộc deploy đúng nhịp |
| 44s | 1 Twitch Runner, 1 Static Carrier, 4 Blank Walker | 9 | tăng overlap và buộc deploy đúng nhịp |
| 64s | 1 Twitch Runner, 1 Static Carrier, 4 Blank Walker | 9 | tăng overlap và buộc deploy đúng nhịp |
| 82s | 1 Twitch Runner, 1 Static Carrier, 5 Blank Walker | 10 | tăng overlap và buộc deploy đúng nhịp |
| 99s | 1 Static Carrier, 1 Twitch Runner, 5 Blank Walker | 10 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Hạ 2 Twitch Runner đầu tiên trong 10 giây kể từ lúc spawn |
| 3 sao | Cổng Aegis còn trên 65% HP |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 1: tutorial, giữ cổng, xử lý runner và Static Carrier.
- Enemy pool hiện tại là **Blank Walker, Twitch Runner, Static Carrier**, nên người chơi phải xử lý nhiều vai trò cùng lúc thay vì chỉ đánh enemy nền.
- Objective sao phụ tạo thêm áp lực: **Hạ 2 Twitch Runner đầu tiên trong 10 giây kể từ lúc spawn** và **Cổng Aegis còn trên 65% HP**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Blank Walker chậm nhưng đông, dùng damage tầm xa để bào dần thay vì deploy quá nhiều tanker.
- Giữ một lượt deploy hoặc cooldown để chặn Twitch Runner khi chúng spawn theo cặp.
- Focus Static Carrier từ xa, tránh để nó chết trong khu vực sát cổng.
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

