# Cách Chơi

## Thể loại

Game thuộc thể loại **side-scrolling auto-battle base defense**.

Người chơi không điều khiển từng nhân vật di chuyển thủ công. Người chơi đóng vai chỉ huy, triển khai hero/unit đúng thời điểm để:

- giữ cổng căn cứ
- chống các wave infected
- đẩy đội hình tiến lên
- phá cổng hoặc lõi của enemy
- đánh bại boss cuối stage

Người chơi là chỉ huy Quân Đoàn Aegis, sử dụng **Aegis Energy** để triển khai các chiến binh đã sống sót qua quá trình **Aegis Resonance** ra chiến trường.

## Vòng lặp chính

1. Chọn world và stage.
2. Chọn đội hình hero Aegis.
3. Vào trận.
4. Tích tài nguyên chiến đấu theo thời gian.
5. Triển khai hero hoặc unit.
6. Unit tự đánh, tự tích nộ và tự dùng skill nộ khi đầy nộ.
7. Phá tuyến infected hoặc đánh bại boss.
8. Nhận thưởng.
9. Nâng cấp hero.
10. Mở stage tiếp theo.

## Mục tiêu trong trận

Mỗi trận có hai phe:

- bên trái: căn cứ hoặc cổng Aegis của người chơi
- bên phải: ổ infected, cổng brainrot hoặc boss

Điều kiện thắng:

- phá cổng enemy
- hoặc tiêu diệt boss
- hoặc sống sót qua toàn bộ wave tùy loại stage

Điều kiện thua:

- cổng Aegis bị phá
- toàn bộ đội hình bị quét sạch
- hết thời gian trong một số stage đặc biệt

## Tài nguyên trong trận

### Aegis Energy

Tài nguyên dùng để triển khai unit.

Nguồn nhận chính:

- **Aegis Reactor**: căn cứ tự tạo năng lượng theo thời gian
- **Kill Burst**: nhận thêm năng lượng khi tiêu diệt enemy
- **Core Engineer**: tạo năng lượng theo chu kỳ nhờ cột năng lượng gắn liền

Thông số gợi ý ban đầu:

- bắt đầu trận với 20 Aegis Energy
- giới hạn tối đa 100 Aegis Energy
- Aegis Reactor tự hồi 1 energy mỗi 2 giây
- Kill Burst: enemy thường cho 1 đến 2 energy khi chết

Điểm thiết kế:

- tự hồi theo thời gian chỉ là nguồn nền
- kill enemy giúp người chơi snowball nhẹ khi đánh tốt
- Core Engineer là cách build đội hình thiên về kiểm soát tài nguyên

### Core Engineer tạo Aegis Energy như thế nào?

Core Engineer là unit hậu phương, không tấn công. Khi được triển khai, nhân vật mang theo một cột năng lượng gắn liền với bản thân.

Cách tạo năng lượng:

- Core Engineer tự tạo Aegis Energy theo chu kỳ
- Cột năng lượng cũng tạo Aegis Energy theo chu kỳ
- Cột không tách rời, di chuyển theo Core Engineer
- Khi Core Engineer bị hạ, cột cũng biến mất

Nhược điểm:

- không gây sát thương trực tiếp
- cần thời gian mới tạo đủ giá trị
- nếu trận quá ngắn, hiệu quả kém hơn unit sát thương

### Item đặc biệt tạo Aegis Energy là gì?

Item đặc biệt là các item có dòng hiệu ứng liên quan đến năng lượng triển khai, thường nằm ở slot **Core Module**, **Accessory** hoặc **Tactical Chip**. Các item này được mua trong shop.

Ví dụ:

- **Starter Capacitor**  
  Bắt đầu trận với thêm 10 Aegis Energy.

- **Resonance Battery**  
  Tăng giới hạn Aegis Energy tối đa thêm 20.

- **Kill Converter Chip**  
  Mỗi 10 enemy bị tiêu diệt sẽ nhận thêm 8 Aegis Energy.

- **Boss Siphon Module**  
  Mỗi khi gây mất 10% máu boss, nhận 5 Aegis Energy.

- **Perfect Hold Badge**  
  Nếu cổng Aegis không mất máu trong 30 giây đầu, nhận 15 Aegis Energy.

- **Heavy Deploy Refund Cell**  
  Sau khi triển khai unit giá cao, hoàn lại 15% chi phí nếu unit sống quá 20 giây.

### Nộ

Mỗi chiến binh có một thanh nộ riêng. Người chơi không bấm skill thủ công.

Cách hoạt động:

- chiến binh tự dùng đòn đánh cơ bản
- mỗi đòn đánh cơ bản sẽ tích nộ
- một số unit cũng nhận thêm nộ khi bị đánh hoặc khi hồi máu
- khi thanh nộ đầy, chiến binh tự động dùng skill nộ
- sau khi dùng skill nộ, thanh nộ trở về 0 và bắt đầu tích lại

Thông số gợi ý:

- mỗi chiến binh cần 100 nộ để dùng skill nộ
- đòn đánh thường tạo 8 đến 15 nộ tùy class
- tanker có thể nhận thêm nộ khi bị đánh
- healer có thể nhận thêm nộ khi hồi máu
- item có thể tăng tốc độ tích nộ hoặc lượng nộ khởi đầu

Điểm thiết kế:

- người chơi không phải micro skill
- sức mạnh của unit đến từ đội hình, thời điểm triển khai và nâng cấp
- skill nộ vẫn tạo khoảnh khắc bùng nổ tự nhiên trong trận

## Triển khai unit

Mỗi hero có chi phí triển khai và cooldown riêng.

Ví dụ:

- Vanguard Breaker: giá trung bình, cooldown ngắn
- Pulse Ranger: giá thấp, cần bảo vệ
- Resonance Blade: giá trung bình, cooldown vừa
- Aegis Medic: giá cao hơn, không nên spam
- Core Engineer: giá cao, ảnh hưởng chiến trường lâu dài
- Overdrive Titan: giá rất cao, cooldown dài

## Đội hình

Mặc định có 4 slot đội hình. Mở slot thứ 5 khi đạt World 8.

Một đội hình cơ bản nên có:

- 1 tanker
- 1 sát thương tầm xa
- 1 sát thương cận chiến hoặc sát thủ
- 1 hỗ trợ hoặc hồi phục
- 1 slot linh hoạt

Gợi ý formation:

- **Balanced Squad**: Vanguard Breaker, Pulse Ranger, Resonance Blade, Aegis Medic
- **Defense Squad**: Vanguard Breaker, Core Engineer, Aegis Medic, Pulse Ranger
- **Boss Killer Squad**: Vanguard Breaker, Resonance Blade, Pulse Ranger, Overdrive Titan
- **Wave Clear Squad**: Core Engineer, Pulse Ranger, Overdrive Titan, Aegis Medic

## Loại stage

Mỗi world có 10 stage thường và 1 stage boss.

### Stage thường

Độ khó tăng dần qua từng stage, giúp người chơi farm EXP để nâng cấp hero trước khi vào boss.

### Stage boss

Trận cuối world, xuất hiện boss với cơ chế riêng.

## Cơ chế sao

Mỗi stage có tối đa 3 sao.

Điều kiện gợi ý:

- thắng trận
- cổng Aegis còn trên 50% máu
- hoàn thành trong thời gian yêu cầu

Sao dùng để:

- mở rương world
- mở hard mode
- nhận vật liệu nâng cấp

## Nhịp chơi mong muốn

- mỗi trận thường: 1 đến 3 phút
- boss stage: 3 đến 5 phút
- người chơi nên ra quyết định liên tục nhưng vẫn dễ theo dõi
