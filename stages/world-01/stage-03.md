# World 01 Stage 03 - Trại Sơ Tán Thất Thủ

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 1 - Trại Sơ Tán Thất Thủ |
| Stage | 3 |
| Loại màn | Stage thường |
| Level hero kỳ vọng | 2 |
| Monster level | 2 |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Slot đội hình | 4 |
| Hệ thống đã mở | deploy cơ bản, Aegis Energy, EXP tướng, nâng cấp hero level |
| Enemy pool | Blank Walker |
| Mục tiêu thắng | Đẩy lane sang phải và phá ổ infected/cổng brainrot bên phải |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 90 giây |
| Wave budget mục tiêu | 34 |
| Stamina cost | 6 |
| First clear EXP | 90 |
| Repeat clear EXP | 49 |

## Ý đồ thiết kế

Stage này dùng vai trò: **giới thiệu enemy hoặc cơ chế phụ đầu tiên**.

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

## Wave plan V0.1

| Thời điểm | Spawn | Budget | Mục đích |
| --------: | ----- | -----: | -------- |
| 0s | 3 Blank Walker | 3 | mở đầu, cho người chơi setup tuyến |
| 14s | 5 Blank Walker | 5 | giới thiệu áp lực chính với số lượng vừa |
| 28s | 5 Blank Walker | 5 | tăng overlap và buộc deploy đúng nhịp |
| 45s | 6 Blank Walker | 6 | tăng overlap và buộc deploy đúng nhịp |
| 63s | 7 Blank Walker | 7 | tăng overlap và buộc deploy đúng nhịp |
| 77s | 7 Blank Walker | 7 | finale, kiểm tra trọng tâm stage |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng stage |
| 2 sao | Hạ Twitch Runner đầu tiên trong 8 giây kể từ lúc spawn |
| 3 sao | Cổng Aegis còn trên 75% HP |

## Vì sao stage này khó

- Stage đặt áp lực đúng vào theme của World 1: tutorial, giữ cổng, xử lý runner và Static Carrier.
- Enemy pool hiện tại chỉ có **Blank Walker**, nên độ khó tập trung vào deploy đúng thứ tự, giữ cổng sạch và xử lý mật độ wave.
- Objective sao phụ tạo thêm áp lực: **Hạ Twitch Runner đầu tiên trong 8 giây kể từ lúc spawn** và **Cổng Aegis còn trên 75% HP**.
- Nếu người chơi deploy sai thứ tự, tuyến trước sẽ vỡ trước khi damage/support tạo đủ giá trị.

## Cách vượt qua

- Deploy tanker trước để tuyến không bị thủng trong 20 giây đầu.
- Không dùng hết Aegis Energy ngay khi wave đầu chưa lộ đủ enemy chính.
- Blank Walker chậm nhưng đông, dùng damage tầm xa để bào dần thay vì deploy quá nhiều tanker.
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

