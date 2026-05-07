# Giới Hạn Số Lần Chơi Trong 1 Ngày

## Mục tiêu thiết kế

Hệ stamina tồn tại để:

- kiểm soát tốc độ farm EXP
- tránh người chơi vượt progression quá nhanh
- tạo nhịp quay lại trong ngày
- giữ cân bằng giữa người chơi miễn phí và người chơi nạp

## Tài nguyên giới hạn chính: Aegis Stamina

**Aegis Stamina** là năng lượng dùng để vào stage.

Tên cũ là Aegis Charge. Trong tài liệu vận hành nên dùng thống nhất là **stamina** để người chơi dễ hiểu.

## Quy tắc cơ bản

- tối đa: **120 stamina**
- mỗi lần vào stage sẽ **trừ stamina ngay khi bắt đầu trận**
- thắng, thua hay thoát giữa chừng đều **không hoàn stamina**
- stamina tự hồi theo thời gian

## Hồi stamina theo thời gian

Đề xuất:

- hồi **1 stamina mỗi 6 phút**
- hồi đầy từ 0 đến 120 mất **12 giờ**

Nhịp này đủ để:

- người chơi casual chơi vài lần mỗi ngày
- người chơi chăm quay lại nhiều phiên ngắn
- vẫn giữ giới hạn farm EXP

## Chi phí stamina vào stage

| Loại stage | Chi phí stamina |
| ---------- | --------------: |
| Stage thường world 1-3 | 6 |
| Stage thường world 4-6 | 8 |
| Stage thường world 7-10 | 10 |
| Stage thử thách elite | 12 |
| Boss world 1-3 | 10 |
| Boss world 4-6 | 12 |
| Boss world 7-10 | 15 |

## Thua trận có mất lượt không?

Có.

Quy tắc thống nhất:

- thắng stage: mất stamina
- thua stage: mất stamina
- thoát giữa chừng: mất stamina

Lý do:

- tránh việc người chơi thoát ra vào liên tục để dò wave miễn phí
- khiến quyết định vào stage và chọn đội hình có giá trị hơn
- kiểm soát farm EXP ổn định hơn

## Mua hoặc xem quảng cáo để lấy stamina

### Quảng cáo

- xem quảng cáo nhận **20 stamina**
- tối đa **3 lần mỗi ngày**
- tổng cộng nhận thêm tối đa **60 stamina/ngày**

### Mua bằng gem

- mua **60 stamina** mỗi lần
- tối đa **5 lần mỗi ngày**
- giá tăng dần theo lượt mua trong ngày

Gợi ý giá:

| Lần mua | Gem |
| ------: | --: |
| 1 | 50 |
| 2 | 75 |
| 3 | 100 |
| 4 | 150 |
| 5 | 200 |

## Liên hệ với EXP farm

Stamina là giới hạn chính của việc farm EXP.

Vì mọi lần vào map đều tốn stamina, người chơi phải cân nhắc:

- farm stage cuối world cũ để lên level an toàn
- hay đẩy tiếp stage mới với độ rủi ro cao hơn

Điều này giúp progression ổn định hơn và tránh việc người chơi farm vô hạn trong một phiên chơi.

## Lý do trong lore

Aegis Stamina đại diện cho khả năng vận hành ổn định của lõi Aegis và thể trạng chiến binh sau mỗi lần triển khai.

Mỗi lần ra trận:

- lõi Aegis sinh nhiệt
- hệ đồng bộ thần kinh bị nhiễu
- huyết thanh Aegis bị tiêu hao
- căn cứ phải tái đồng bộ hệ chiến đấu

Vì vậy stamina vừa là cơ chế game, vừa khớp với bối cảnh thế giới.

## Khuyến nghị cân bằng ban đầu

Với 120 stamina và nhịp hồi 1 stamina mỗi 6 phút:

- người chơi casual có thể chơi 10 đến 15 stage thường mỗi ngày
- người chơi chăm có thể dùng thêm quảng cáo hoặc gem để farm tiếp
- boss stage vẫn có giá trị nhưng không phải nơi farm rẻ nhất
