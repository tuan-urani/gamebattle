# World 02 Boss - Trippo Motorico

## Tổng quan

| Trường | Giá trị |
| ------ | ------- |
| World | 2 - Xa Lộ Di Tản |
| Loại màn | Boss stage |
| Boss | Trippo Motorico |
| Boss level | 10 |
| Level hero kỳ vọng | 10 |
| Hero có thể dùng | Kael Voss, Mira Sane, Mason Rook |
| Slot đội hình | 4 |
| Hệ thống đã mở | Core Engineer, bẫy làm chậm, stage thử thách elite |
| Enemy/Boss pool | Trippo Motorico, Twitch Runner |
| Điều kiện mở boss | Hoàn thành đủ 30/30 sao của 10 stage thường trong World 2 |
| Mục tiêu thắng | Giết boss |
| Điều kiện thua | Cổng Aegis bên trái bị phá |
| Thời lượng mục tiêu | 180 giây |
| Stamina cost | 10 |
| First clear EXP | 330 |
| Repeat clear EXP | 160 |

## Ý đồ thiết kế

Boss stage là bài kiểm tra cuối của World 2: **enemy tốc độ cao, tuyến phòng thủ dễ bị xuyên**.

Độ khó chính: runner và crawler ép cổng liên tục, người chơi bị phạt nếu deploy tanker muộn.

Boss không chỉ có nhiều máu hơn stage thường. Màn này ép người chơi xử lý đúng mechanic trước khi cố gắng kết thúc trận.

Điều kiện mở khóa boss:

- phải thắng đủ 10 stage thường của world
- phải đạt đủ **30/30 sao** từ 10 stage thường đó

Luật thắng/thua của boss stage:

- Người chơi thắng khi boss chết.
- Boss chết là kết thúc màn, không cần phá thêm ổ infected/cổng brainrot.
- Enemy, wave phụ và boss đều tạo áp lực lên cổng Aegis.
- Người chơi thua nếu cổng Aegis bị phá.

## Trạng thái người chơi

| Hero | Class | Deploy cost | Cooldown | Vai trò |
| ---- | ----- | ----------: | -------- | ------- |
| Kael Voss | Vanguard Breaker | 20 | 18 giây | tanker tuyến trước, giữ cổng |
| Mira Sane | Pulse Ranger | 15 | 14 giây | bắn xa, xử lý runner/support |
| Mason Rook | Core Engineer | 30 | 24 giây | tạo Aegis Energy, mạnh trong trận dài |

## Enemy và boss trong màn

| Enemy | Threat cost | Ghi chú |
| ----- | ----------: | ------- |
| Trippo Motorico | boss | cơ chế riêng của boss stage |
| Twitch Runner | 2 | chạy nhanh, kiểm tra khả năng giữ cổng và deploy đúng nhịp |

## Boss mechanic

- boss lao nhanh theo nhịp
- càng ít máu càng tăng tốc
- mỗi pha lao kéo thêm Twitch Runner

## Timeline V0.1

| Thời điểm | Sự kiện | Mục đích |
| --------: | ------- | -------- |
| 0s | Boss xuất hiện cùng 4 Twitch Runner | mở trận, buộc người chơi dựng tuyến ngay |
| 25s | 5 Twitch Runner | tăng áp lực tuyến trước |
| 50s | Boss kích hoạt mechanic 1 | giới thiệu cơ chế boss chính |
| 70s | 3 Jaw Crawler, 3 Twitch Runner | trộn enemy để kéo người chơi khỏi việc chỉ focus boss |
| 60% HP | Boss chuyển phase 2 | tăng cường cơ chế chính của world |
| 105s | Boss gọi wave phụ lớn | kiểm tra khả năng clear wave |
| 30% HP | Boss chuyển phase cuối | tạo spike cuối trận |
| 150s | Finale wave: 5 Twitch Runner, 3 Jaw Crawler | ép kết thúc trước khi cổng vỡ |

## Objective sao

| Sao | Điều kiện |
| --- | --------- |
| 1 sao | Thắng boss stage |
| 2 sao | Trippo Motorico không chạm cổng quá 1 lần |
| 3 sao | Hoàn thành trong 180 giây |

## Vì sao boss này khó

- Boss gom toàn bộ cơ chế chính của world vào một trận dài hơn stage thường.
- Người chơi phải chia sát thương giữa boss, wave phụ và mục tiêu mechanic.
- Objective sao phụ yêu cầu xử lý mechanic tốt, không chỉ thắng bằng level cao.
- Nếu kéo dài trận, wave phụ và mechanic boss sẽ bào cổng Aegis hoặc làm đội hình mất nhịp.

## Cách vượt qua

- deploy Kael sớm để chặn pha lao
- dùng Mira để hạ runner trước khi chạm cổng
- Mason chỉ nên dùng khi tuyến đã ổn định
- Không dồn toàn bộ Aegis Energy vào damage nếu tuyến trước chưa ổn định.
- Khi boss chuyển phase, giữ tài nguyên để phản ứng với wave hoặc mechanic mới.
- Ưu tiên objective 2 sao trước nếu muốn perfect clear, vì boss thường phạt người chơi bỏ qua mechanic.

## Dấu hiệu boss đang quá khó

- Người chơi đúng level kỳ vọng nhưng không qua được phase 2.
- Mechanic boss xảy ra quá sớm trước khi người chơi có đủ tài nguyên phản ứng.
- Wave phụ khiến cổng vỡ dù người chơi đã hạ đúng mục tiêu mechanic.

## Dấu hiệu boss đang quá dễ

- Người chơi có thể bỏ qua mechanic và chỉ focus boss vẫn thắng.
- Boss không ép thay đổi target priority.
- Phase cuối không tạo khác biệt so với nửa đầu trận.

