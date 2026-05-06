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
9. Nâng cấp hero, item, lõi Aegis.
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
- **Wave Break**: nhận một lượng năng lượng khi dọn sạch một wave
- **Elite Break**: nhận năng lượng lớn hơn khi hạ elite hoặc phá giáp boss
- **Defense Bonus**: nhận thêm nếu chặn được enemy trước khi chúng chạm cổng Aegis
- **Core Engineer**: dựng công trình tạo hoặc tái chế năng lượng
- **Item đặc biệt**: biến kill, block, crit hoặc boss damage thành năng lượng

Thông số gợi ý ban đầu:
- bắt đầu trận với 20 Aegis Energy
- giới hạn tối đa 100 Aegis Energy
- tự hồi 1 energy mỗi 2 giây
- enemy thường cho 1 đến 2 energy khi chết
- elite cho 8 đến 12 energy khi chết
- dọn sạch wave cho 10 energy
- phá một phase boss cho 15 đến 25 energy

Điểm thiết kế:
- tự hồi theo thời gian chỉ là nguồn nền
- kill enemy giúp người chơi snowball nhẹ khi đánh tốt
- wave clear tạo nhịp bung unit sau mỗi đợt
- Core Engineer và item là cách build đội hình thiên về kiểm soát tài nguyên

### Core Engineer tạo Aegis Energy như thế nào?
Core Engineer không chỉ “tăng hồi năng lượng” chung chung. Đây là class chuyên biến chiến trường thành nhà máy năng lượng tạm thời.

Công trình gợi ý:

- **Resonance Pylon**  
  Mỗi 8 giây tạo 5 Aegis Energy. Nếu bị enemy phá thì mất hiệu lực. Phù hợp cho trận dài hoặc stage phòng thủ.

- **Scrap Converter**  
  Khi enemy chết trong vùng ảnh hưởng, có tỉ lệ chuyển xác nhiễm thành 1 Aegis Energy. Phù hợp với wave đông như World 5.

- **Emergency Battery**  
  Kích hoạt một lần để nhận ngay 20 Aegis Energy. Cooldown dài. Dùng khi cần gọi tanker hoặc Overdrive Titan khẩn cấp.

- **Gate Dynamo**  
  Khi cổng Aegis bị đánh, chuyển một phần sát thương chặn được thành năng lượng. Phù hợp lối chơi thủ chắc.

Nhược điểm:
- công trình tốn Aegis Energy ban đầu để đặt
- cần thời gian mới hoàn vốn
- dễ bị boss hoặc enemy áp sát phá
- nếu trận quá ngắn, Core Engineer không hiệu quả bằng unit sát thương trực tiếp

### Item đặc biệt tạo Aegis Energy là gì?
Item đặc biệt là các item có dòng hiệu ứng liên quan đến năng lượng triển khai, thường nằm ở slot **Core Module**, **Accessory** hoặc **Tactical Chip**.

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

### Campaign Stage
Stage chính để mở map và theo cốt truyện.

### Elite Stage
Stage khó hơn, có mini-boss và rơi nguyên liệu hiếm.

### Boss Stage
Stage cuối world. Boss có cơ chế riêng.

### Supply Run
Stage farm tài nguyên hằng ngày.

### Core Defense
Stage phòng thủ căn cứ trong một số phút.

### Boss Rush
Chế độ mở sau khi hoàn thành campaign hoặc một mốc world nhất định.

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

## Trạng thái trong trận

### Desync
Enemy bị lệch nhịp, giảm tốc độ di chuyển và tốc độ đánh.

### Mutate
Enemy tiến hóa trong trận, tăng chỉ số hoặc mở kỹ năng mới.

### Silence Signal
Hero không tích nộ và không dùng được skill nộ trong vài giây.

### Clean Pulse
Xóa debuff brainrot khỏi đồng minh.

## Nhịp chơi mong muốn
- mỗi trận thường: 1 đến 3 phút
- stage elite: 2 đến 4 phút
- boss stage: 3 đến 5 phút
- người chơi nên ra quyết định liên tục nhưng vẫn dễ theo dõi

## Hướng dẫn người chơi mới
World 1 nên dạy theo thứ tự:
- cách triển khai unit
- cách giữ cổng
- cách đánh thường, tích nộ và tự dùng skill nộ
- cách đọc thanh máu boss
- cách nâng cấp hero sau trận
- cách chọn đội hình trước stage

World 2 bắt đầu dạy:
- enemy chạy nhanh
- cần tanker giữ tuyến
- cần bẫy hoặc làm chậm

World 3 bắt đầu dạy:
- enemy debuff
- cần item kháng nhiễu
- cần ưu tiên mục tiêu hỗ trợ
