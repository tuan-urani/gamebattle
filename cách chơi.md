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
8. Nhận thưởng và EXP vào kho EXP tướng.
9. Vào kho tướng để dùng EXP nâng hero level hoặc nâng skill nộ khi đủ điều kiện.
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

Item đặc biệt là item được trang bị trực tiếp lên hero, không phải buff chung mơ hồ của cả tài khoản.

Mỗi hero có 3 slot item:

- **Weapon Module**
- **Armor Module**
- **Tactical Chip**

Các item tạo Aegis Energy thường nằm ở slot **Tactical Chip** hoặc một số **Weapon Module** đặc biệt. Chúng có thể mua trong shop hoặc nhận từ boss.

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
- đòn đánh thường tạo khoảng 8 đến 15 nộ ở level thấp, sau đó tăng theo hero level và item
- tanker có thể nhận thêm nộ khi bị đánh
- healer có thể nhận thêm nộ khi hồi máu
- item có thể tăng tốc độ tích nộ hoặc lượng nộ khởi đầu

### Nâng cấp skill nộ

Skill nộ vẫn được kích hoạt tự động khi đầy nộ, nhưng hiệu ứng của skill có thể được nâng cấp.

Quy tắc:

- hero đạt level 10, 15, 20 sẽ mở quyền nâng skill nộ lên bậc cao hơn
- level chỉ mở điều kiện nâng, không tự động nâng skill
- người chơi nâng skill nộ trong UI nâng cấp hero
- mỗi bậc skill nên tăng hiệu ứng gameplay rõ ràng

Ví dụ:

- skill đánh 1 mục tiêu nâng thành đánh 2 mục tiêu
- skill hồi 1 đồng minh nâng thành hồi 2 đồng minh
- skill tạo khiên tăng thêm phạm vi hoặc thời gian
- skill giải debuff có thể giải thêm debuff hoặc thêm kháng debuff ngắn hạn

Điểm thiết kế:

- người chơi không phải micro skill
- sức mạnh của unit đến từ đội hình, thời điểm triển khai và nâng cấp
- skill nộ vẫn tạo khoảnh khắc bùng nổ tự nhiên trong trận

### Debuff trong trận

Debuff là hiệu ứng xấu có thời gian tồn tại, do enemy hoặc boss gây lên hero Aegis.

Quy tắc:

- debuff có icon và thời gian còn lại trên hero
- debuff cùng loại không cộng dồn, chỉ refresh thời gian
- Aegis Medic có thể xóa debuff bằng skill nộ
- item kháng debuff làm giảm thời gian hoặc mức ảnh hưởng của debuff
- hiệu ứng vị trí như bị đẩy lùi hoặc bị enemy lao vào tuyến sau không được xóa bằng giải debuff thông thường

Debuff status hiện tại gồm:

- **Signal Drain**: giảm tốc độ tích nộ
- **Rage Leech**: rút nộ hiện có
- **Desync**: có khả năng đánh hụt
- **Rage Lock**: không thể tích nộ
- **Ultimate Lock**: không thể dùng skill nộ
- **Toxic Suppression**: giảm hồi máu và mất máu theo thời gian

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

Replay stage thường là nguồn farm EXP chính, nhưng mỗi lần vào stage đều tốn stamina dù thắng hay thua.

Khi thắng stage, EXP được cộng vào kho EXP tướng. Người chơi không nhận level tự động sau trận; cần vào kho tướng và dùng EXP để nâng hero mong muốn.

### Stage boss

Trận cuối world, xuất hiện boss với cơ chế riêng.

## Cơ chế sao

Mỗi stage có tối đa 3 sao.

Quy tắc chung:

- **1 sao**: thắng stage
- **2 sao**: hoàn thành objective phụ thứ nhất của stage
- **3 sao**: hoàn thành objective phụ thứ hai của stage

Objective phụ phải thay đổi theo world, stage type hoặc boss mechanic. Không dùng cùng một bộ điều kiện cho toàn bộ game.

Chi tiết điều kiện sao của toàn bộ 110 stage được thống kê trong file **cơ chế sao theo từng stage.md**.

Sao không phải tiền tệ tiêu hao. Sao được ghi nhận vào **Thành tựu sao World**.

Khi tổng sao trong một world đạt mốc nhất định, người chơi nhận được rương thành tựu của world đó. Rương mở ra **EXP tướng** để đưa vào kho EXP tướng.

### Nhóm objective sao

Objective phụ có thể thuộc các nhóm sau:

- **Giữ cổng**: cổng Aegis còn trên một mức HP nhất định.
- **Tốc độ**: hoàn thành stage trước mốc thời gian.
- **Kiểm soát enemy**: không để enemy đặc biệt chạm cổng hoặc vượt tuyến.
- **Chống debuff**: giới hạn số lần hero bị debuff như Signal Drain, Desync, Toxic Suppression.
- **Ưu tiên mục tiêu**: hạ elite, node phụ, healer hoặc support enemy trước mốc thời gian.
- **Bảo vệ đội hình**: không để hero tuyến sau chết, không để quá nhiều unit bị hạ.
- **Boss mechanic**: xử lý đúng cơ chế riêng của boss.

### Quy tắc hiển thị

- Màn chọn stage phải hiển thị rõ 3 điều kiện sao.
- Khi vào trận, objective sao phụ nên có tracker ngắn gọn.
- Sau trận, UI phải cho biết sao nào đạt, sao nào không đạt và lý do thất bại.
- Nếu stage đã đạt 3 sao, replay stage vẫn cho EXP repeat nhưng không tăng thêm tiến độ thành tựu sao.

### Thành tựu sao World

Mỗi world có 11 stage, tối đa 33 sao.

Rương thành tựu chỉ nhận một lần theo từng world.

| Mốc sao world | Thành tựu | Thưởng |
| ------------: | --------- | ------ |
| 10 sao | World Star I | rương EXP nhỏ |
| 20 sao | World Star II | rương EXP vừa |
| 30 sao | World Star III | rương EXP lớn |
| 33 sao | Perfect World Clear | rương EXP hoàn hảo |

### EXP từ rương thành tựu

Lượng EXP trong rương tăng theo world để khớp với progression level.

```text
Rương EXP nhỏ = 150 + world * 40
Rương EXP vừa = 300 + world * 80
Rương EXP lớn = 500 + world * 120
Rương EXP hoàn hảo = 800 + world * 160
```

Ví dụ:

| World | 10 sao | 20 sao | 30 sao | 33 sao |
| ----- | -----: | -----: | -----: | -----: |
| 1 | 190 EXP | 380 EXP | 620 EXP | 960 EXP |
| 5 | 350 EXP | 700 EXP | 1100 EXP | 1600 EXP |
| 10 | 550 EXP | 1100 EXP | 1700 EXP | 2400 EXP |

EXP từ rương thành tựu được cộng vào kho EXP tướng. Người chơi tự chọn hero để nâng level.

## Nhịp chơi mong muốn

- mỗi trận thường: 1 đến 3 phút
- boss stage: 3 đến 5 phút
- người chơi nên ra quyết định liên tục nhưng vẫn dễ theo dõi
