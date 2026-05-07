# Stage Difficulty And Wave Design

## Mục tiêu tài liệu

Tài liệu này bổ sung lớp thiết kế còn thiếu giữa campaign map và trận đánh thực tế.

Các file hiện tại đã trả lời:

- game có world nào
- world có enemy và boss nào
- stage có objective sao gì
- hero và monster scale chỉ số thế nào

Tài liệu này trả lời thêm:

- tại từng stage người chơi đang có hero nào
- level kỳ vọng của hero là bao nhiêu
- stage đó đang dạy hoặc kiểm tra kỹ năng gì
- quái ra theo wave như thế nào
- bao nhiêu con là vừa
- điểm khó của màn đến từ đâu
- làm sao tăng độ khó có kiểm soát thay vì chỉ tăng số lượng

## Quyết định V0.1 để giảm mơ hồ

Các quyết định dưới đây dùng làm base cho thiết kế stage. Nếu các file khác khác với phần này thì nên cập nhật lại cho thống nhất.

File tổng hợp nhanh về character, monster, boss, level và stat nằm ở **character_monster_stat_master.md**.

- Formation mặc định có **4 slot** từ đầu game, nhưng World 1 chỉ có 2 hero để chọn.
- Formation slot thứ 5 mở ở **World 8**.
- World 4 mở **formation preset**, không mở thêm slot đội hình.
- World 1 bắt đầu với **Kael Voss** và **Mira Sane**.
- World 2 mở **Mason Rook** sau khi hạ boss World 1.
- World 3 mở **Riven Hal** sau khi hạ boss World 2.
- World 5 mở **Iris Venn** sau khi hạ boss World 4.
- World 7 mở **Atlas-09** sau khi hạ boss World 6.
- Skill nộ tự kích hoạt khi đủ 100 nộ. Người chơi không bấm skill thủ công.
- Stage thường thắng bằng cách đẩy lane và phá **ổ infected/cổng brainrot** bên phải.
- Boss stage thắng bằng cách giết **boss**. Boss chết là kết thúc màn.
- Cổng Aegis bên trái là base của người chơi. Nếu bị phá thì thua.
- Enemy luôn có mục tiêu cuối là tấn công cổng Aegis.
- Boss của mỗi world chỉ mở khi người chơi đã đạt đủ **30/30 sao** của 10 stage thường trong world đó.
- Stage thường World 1 nên dài 75 đến 120 giây.
- Boss World 1 nên dài 150 đến 210 giây.

## Stage Blueprint

Mỗi stage nên được thiết kế theo công thức:

```text
Stage = Player State + Enemy Pool + Wave Budget + Teaching Goal + Star Pressure
```

Trong đó:

- **Player State**: hero đã mở, level kỳ vọng, số slot đội hình, hệ thống đã mở.
- **Enemy Pool**: danh sách enemy được phép spawn trong stage.
- **Wave Budget**: tổng độ nặng của enemy được phép dùng trong stage.
- **Teaching Goal**: stage này dạy hoặc kiểm tra điều gì.
- **Star Pressure**: objective sao phụ ép người chơi chơi tốt hơn ở đúng trọng tâm của stage.

Không nên viết stage bằng cảm giác kiểu "cho nhiều quái hơn". Mỗi stage phải có một câu trả lời rõ:

```text
Stage này khó vì điều gì?
```

Ví dụ:

- khó vì runner chạy nhanh
- khó vì static carrier nổ gần cổng
- khó vì enemy support làm chậm nộ
- khó vì backline bị dive
- khó vì boss hồi máu khi hộ vệ còn sống

## Player State Theo World

| World | Level kỳ vọng | Hero có thể dùng khi bắt đầu world | Slot đội hình | Hệ thống chính đã mở |
| ----- | ------------: | ---------------------------------- | ------------: | -------------------- |
| 1 | 1-5 | Kael Voss, Mira Sane | 4 | deploy cơ bản, Aegis Energy, EXP tướng |
| 2 | 6-10 | Kael, Mira, Mason Rook | 4 | Core Engineer, bẫy làm chậm, stage thử thách elite |
| 3 | 11-15 | Kael, Mira, Mason, Riven Hal | 4 | debuff, nâng skill nộ bậc 2, objective chống debuff |
| 4 | 16-20 | Kael, Mira, Mason, Riven | 4 | formation preset, enemy giáp dày |
| 5 | 21-25 | Kael, Mira, Mason, Riven, Iris Venn | 4 | Aegis Medic, thanh nộ hiển thị rõ |
| 6 | 26-30 | Kael, Mira, Mason, Riven, Iris | 4 | counter hồi máu, chống Toxic Suppression, nâng skill nộ bậc 3 |
| 7 | 31-35 | Kael, Mira, Mason, Riven, Iris, Atlas-09 | 4 | Overdrive Titan, challenge world cũ |
| 8 | 36-40 | toàn bộ 6 hero | 5 | formation slot thứ 5, node phụ, khóa nộ nâng cao |
| 9 | 41-45 | toàn bộ 6 hero | 5 | xung nghịch pha Aegis, nâng skill nộ bậc 4 |
| 10 | 46-50 | toàn bộ 6 hero | 5 | full system, boss cuối nhiều phase |

## Cost Triển Khai Hero V0.1

Bảng này giúp stage designer ước lượng người chơi có thể deploy gì ở từng thời điểm. Đây là thông số tạm để thiết kế wave, chưa phải số balance cuối.

| Hero | Cost Aegis Energy | Cooldown deploy | Vai trò trong stage design |
| ---- | ----------------: | --------------: | -------------------------- |
| Kael Voss | 20 | 18 giây | chặn tuyến, bảo vệ cổng |
| Mira Sane | 15 | 14 giây | sát thương tầm xa, xử lý runner và support |
| Mason Rook | 30 | 24 giây | tăng kinh tế energy, trận dài |
| Riven Hal | 25 | 20 giây | xử lý elite, support, boss phụ |
| Iris Venn | 35 | 26 giây | hồi máu, giải debuff |
| Atlas-09 | 60 | 45 giây | xoay trận, phá wave lớn, đánh boss |

Thông số Aegis Energy nền đang dùng:

- bắt đầu trận với 20 energy
- giới hạn mặc định 100 energy
- Aegis Reactor tạo 1 energy mỗi 2 giây
- enemy thường chết cho 1 đến 2 energy tùy loại

## Enemy Threat Cost

Threat Cost là điểm độ khó dùng để xây wave. Nó không thay thế chỉ số HP/ATK/DEF. Cùng một enemy ở World 1 và World 5 vẫn scale chỉ số theo level, nhưng Threat Cost giúp kiểm soát mật độ và nhịp spawn.

| Enemy | Threat Cost | Lý do |
| ----- | ----------: | ----- |
| Blank Walker | 1 | enemy nền, tạo áp lực số lượng |
| Jaw Crawler | 2 | thấp, khó bắn trúng, ép kiểm soát tuyến |
| Twitch Runner | 2 | nhanh, dễ chạm cổng nếu thiếu tanker |
| Static Carrier | 3 | chết gây Signal Drain, nguy hiểm nếu nổ gần cổng |
| Scream Spitter | 4 | bắn xa, gây Desync |
| Bone Drummer | 4 | buff tốc độ cho đàn |
| Mute Leech | 4 | rút nộ và gây Signal Drain |
| Meat Shield Host | 5 | tanker che chắn |
| Regrowth Host | 5 | hồi máu, kéo dài wave |
| Signal Host | 6 | phát Signal Drain diện rộng |
| Phase Stalker | 6 | dive tuyến sau |
| Patch Beast | 7 | trâu, đánh đau |
| Red Host | 8 | scale trong trận |
| Core Guardian | 10 | elite cuối game, ép tuyến cực mạnh |

## Wave Budget

Wave Budget là tổng Threat Cost mục tiêu của một stage.

Quy tắc mềm:

```text
Stage Budget = tổng Threat Cost của toàn bộ enemy spawn trong stage
```

Ví dụ:

```text
10 Blank Walker = 10 budget
4 Twitch Runner = 8 budget
2 Static Carrier = 6 budget
Tổng = 24 budget
```

Budget có thể lệch khoảng 10% nếu stage cần dạy cơ chế mới hoặc có objective sao khó.

### Budget gợi ý cho stage thường

| Vị trí stage trong world | Vai trò | Budget gợi ý |
| ------------------------ | ------- | ------------: |
| Stage 1 | giới thiệu world | 18-24 |
| Stage 2 | củng cố cơ bản | 24-30 |
| Stage 3 | giới thiệu enemy/cơ chế mới | 28-36 |
| Stage 4 | phối hợp enemy mới với enemy cũ | 34-42 |
| Stage 5 | thêm áp lực giữa world | 38-48 |
| Stage 6 | kiểm tra nhịp deploy | 44-54 |
| Stage 7 | tăng mật độ hoặc elite nhẹ | 50-60 |
| Stage 8 | stress test cơ chế world | 56-66 |
| Stage 9 | endurance trước stage cuối | 62-74 |
| Stage 10 | bài kiểm tra trước boss | 68-82 |

World càng cao thì enemy đã scale level, nên không cần tăng budget quá mạnh. Độ khó nên tăng bằng composition, mechanic và objective sao.

## Nhịp Wave Chuẩn

Stage thường nên có 3 pha:

| Pha | Thời lượng tương đối | Vai trò |
| --- | -------------------: | ------- |
| Mở đầu | 0-25% stage | cho người chơi deploy tuyến đầu và đọc enemy chính |
| Giữa trận | 25-70% stage | trộn enemy, tạo áp lực thật |
| Cuối trận | 70-100% stage | spike cuối, kiểm tra đội hình |

Quy tắc:

- không dùng quá 25% tổng budget trong 15 giây đầu
- enemy mới nên xuất hiện lần đầu với số lượng nhỏ
- finale wave không nên vượt quá 35% tổng budget nếu stage không phải survival
- nếu stage có objective tốc độ, tổng thời lượng nên ngắn hơn nhưng spawn dày hơn
- nếu stage có objective giữ cổng, spawn nên có nhiều đợt ép tuyến thay vì một spike duy nhất
- nếu stage có objective chống debuff, enemy gây debuff phải xuất hiện đủ rõ để người chơi hiểu đang bị kiểm tra

## Cách Tăng Độ Khó Theo Stage

Thứ tự ưu tiên tăng độ khó:

1. Tăng số enemy nền.
2. Thêm enemy tốc độ hoặc enemy đặc biệt số lượng ít.
3. Trộn enemy đặc biệt với enemy nền để che chắn.
4. Tăng overlap giữa các wave.
5. Thêm elite hoặc support enemy.
6. Thêm objective sao khó hơn.
7. Tăng level hoặc modifier map.

Không nên tăng tất cả cùng lúc. Một stage chỉ nên có 1 hoặc 2 nguồn khó chính.

## World 1 Stage Design

World 1 là tutorial world. Trọng tâm là:

- dạy deploy tanker trước
- dạy ranger đứng sau gây sát thương ổn định
- dạy giữ cổng Aegis
- giới thiệu enemy chạy nhanh
- giới thiệu Static Carrier nổ gây Signal Drain
- boss dạy focus target và xử lý hộ vệ

Hero có thể dùng trong toàn bộ World 1:

- **Kael Voss**
- **Mira Sane**

Formation:

- UI có 4 slot, nhưng roster chỉ có 2 hero.
- Stage 1 có thể dùng tutorial prompt để yêu cầu deploy Kael trước, Mira sau.

Level kỳ vọng:

| Stage | Level hero kỳ vọng |
| ----- | -----------------: |
| Stage 1 | 1 |
| Stage 2 | 1 |
| Stage 3 | 2 |
| Stage 4 | 2 |
| Stage 5 | 3 |
| Stage 6 | 3 |
| Stage 7 | 4 |
| Stage 8 | 4 |
| Stage 9 | 5 |
| Stage 10 | 5 |
| Boss | 5 |

### World 1 Stage 1

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | dạy deploy Kael để chặn tuyến, sau đó deploy Mira để bắn sau lưng tanker |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 1 |
| Enemy pool | Blank Walker |
| Thời lượng mục tiêu | 80 giây |
| Budget mục tiêu | 20 |
| Điểm khó | số lượng Blank Walker tăng dần |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 2 Blank Walker | 2 | wave mở đầu, đủ thời gian deploy Kael |
| 12s | 3 Blank Walker | 3 | dạy giữ tuyến |
| 25s | 4 Blank Walker | 4 | người chơi nên deploy Mira |
| 42s | 5 Blank Walker | 5 | bắt đầu ép cổng nhẹ |
| 60s | 6 Blank Walker | 6 | finale wave |

Objective sao:

- 1 sao: thắng stage
- 2 sao: cổng Aegis còn trên 80% HP
- 3 sao: không để quá 8 enemy chạm cổng

### World 1 Stage 2

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | củng cố deploy đúng thứ tự và giữ cổng lâu hơn |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 1 |
| Enemy pool | Blank Walker |
| Thời lượng mục tiêu | 95 giây |
| Budget mục tiêu | 27 |
| Điểm khó | stage dài hơn, nhiều đợt liên tiếp hơn |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 3 Blank Walker | 3 | kiểm tra deploy Kael |
| 15s | 4 Blank Walker | 4 | áp lực nhẹ |
| 32s | 5 Blank Walker | 5 | người chơi cần Mira |
| 50s | 6 Blank Walker | 6 | ép tuyến giữa trận |
| 72s | 9 Blank Walker | 9 | finale đông nhưng chậm |

Objective sao:

- 1 sao: thắng stage
- 2 sao: cổng Aegis còn trên 75% HP
- 3 sao: hoàn thành trong 120 giây

### World 1 Stage 3

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | giới thiệu Twitch Runner và khái niệm enemy tốc độ cao |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 2 |
| Enemy pool | Blank Walker, Twitch Runner |
| Thời lượng mục tiêu | 95 giây |
| Budget mục tiêu | 31 |
| Điểm khó | runner có thể lọt qua nếu Kael deploy muộn |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 3 Blank Walker | 3 | mở đầu quen thuộc |
| 15s | 2 Blank Walker, 1 Twitch Runner | 4 | runner đầu tiên để dạy phản ứng |
| 32s | 4 Blank Walker, 1 Twitch Runner | 6 | runner được che bởi walker |
| 52s | 3 Blank Walker, 2 Twitch Runner | 7 | kiểm tra tuyến trước |
| 74s | 5 Blank Walker, 3 Twitch Runner | 11 | finale runner pressure |

Objective sao:

- 1 sao: thắng stage
- 2 sao: hạ Twitch Runner đầu tiên trong 8 giây kể từ lúc spawn
- 3 sao: cổng Aegis còn trên 75% HP

### World 1 Stage 4

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | kiểm tra khả năng giữ cổng trước nhiều runner hơn |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 2 |
| Enemy pool | Blank Walker, Twitch Runner |
| Thời lượng mục tiêu | 105 giây |
| Budget mục tiêu | 36 |
| Điểm khó | wave runner tách khỏi walker, buộc người chơi deploy đúng nhịp |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 4 Blank Walker | 4 | tạo tuyến đầu |
| 14s | 2 Twitch Runner | 4 | kiểm tra phản ứng nhanh |
| 30s | 5 Blank Walker, 1 Twitch Runner | 7 | phối hợp chậm và nhanh |
| 50s | 3 Blank Walker, 3 Twitch Runner | 9 | áp lực chính của stage |
| 74s | 6 Blank Walker, 2 Twitch Runner | 10 | finale hỗn hợp |
| 92s | 2 Twitch Runner | 4 | đợt chốt để ép cổng |

Objective sao:

- 1 sao: thắng stage
- 2 sao: không để quá 6 enemy chạm cổng
- 3 sao: hoàn thành trong 115 giây

### World 1 Stage 5

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | giới thiệu Static Carrier và vùng nguy hiểm gần cổng |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 3 |
| Enemy pool | Blank Walker, Twitch Runner, Static Carrier |
| Thời lượng mục tiêu | 110 giây |
| Budget mục tiêu | 39 |
| Điểm khó | Static Carrier chết gần cổng sẽ gây Signal Drain và làm chậm nhịp clear |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 4 Blank Walker | 4 | mở đầu an toàn |
| 18s | 3 Blank Walker, 1 Static Carrier | 6 | Static đầu tiên, đi chậm |
| 36s | 2 Twitch Runner, 1 Static Carrier | 7 | runner ép người chơi không bỏ tuyến |
| 56s | 5 Blank Walker, 1 Static Carrier | 8 | Static được che bởi walker |
| 78s | 4 Blank Walker, 2 Twitch Runner, 1 Static Carrier | 11 | wave chính |
| 98s | 1 Static Carrier | 3 | kiểm tra dứt điểm trước cổng |

Objective sao:

- 1 sao: thắng stage
- 2 sao: không để Static Carrier nổ trong khu vực sát cổng
- 3 sao: cổng Aegis còn trên 70% HP

### World 1 Stage 6

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | phối hợp runner và Static Carrier để kiểm tra nhịp deploy |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 3 |
| Enemy pool | Blank Walker, Twitch Runner, Static Carrier |
| Thời lượng mục tiêu | 110 giây |
| Budget mục tiêu | 45 |
| Điểm khó | runner kéo tuyến mỏng trong khi Static Carrier tạo vùng nổ |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 5 Blank Walker | 5 | ép deploy tanker |
| 15s | 3 Twitch Runner | 6 | kiểm tra phản ứng |
| 32s | 4 Blank Walker, 1 Static Carrier | 7 | dạy focus Static từ xa |
| 52s | 4 Blank Walker, 2 Twitch Runner | 8 | pressure hỗn hợp |
| 72s | 2 Static Carrier, 2 Twitch Runner | 10 | nguy hiểm nếu tuyến bị thủng |
| 92s | 6 Blank Walker, 1 Static Carrier | 9 | finale giữ cổng |

Objective sao:

- 1 sao: thắng stage
- 2 sao: không để quá 5 enemy chạm cổng
- 3 sao: hoàn thành trong 110 giây

### World 1 Stage 7

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | bài kiểm tra runner rõ ràng hơn trước khi tăng mật độ cuối world |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 4 |
| Enemy pool | Blank Walker, Twitch Runner, Static Carrier |
| Thời lượng mục tiêu | 115 giây |
| Budget mục tiêu | 51 |
| Điểm khó | runner xuất hiện theo cặp và có walker che chắn |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 4 Blank Walker | 4 | mở đầu ngắn |
| 12s | 2 Twitch Runner | 4 | objective 2 sao bắt đầu ở đây |
| 28s | 5 Blank Walker, 2 Twitch Runner | 9 | runner có cover |
| 48s | 1 Static Carrier, 3 Twitch Runner | 9 | áp lực tốc độ và debuff |
| 70s | 7 Blank Walker, 2 Twitch Runner | 11 | wave đông |
| 92s | 5 Blank Walker, 4 Twitch Runner, 1 Static Carrier | 14 | finale |

Objective sao:

- 1 sao: thắng stage
- 2 sao: hạ 2 Twitch Runner đầu tiên trong 10 giây kể từ lúc spawn
- 3 sao: cổng Aegis còn trên 65% HP

### World 1 Stage 8

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | stress test Static Carrier, buộc người chơi hạ nó trước khi tới sát cổng |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 4 |
| Enemy pool | Blank Walker, Twitch Runner, Static Carrier |
| Thời lượng mục tiêu | 115 giây |
| Budget mục tiêu | 58 |
| Điểm khó | nhiều Static Carrier đi trong các đợt khác nhau, gây rối nhịp clear |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 5 Blank Walker | 5 | setup |
| 14s | 2 Static Carrier | 6 | dạy focus Static sớm |
| 32s | 4 Blank Walker, 2 Twitch Runner | 8 | ép tuyến |
| 50s | 5 Blank Walker, 2 Static Carrier | 11 | Static có cover |
| 70s | 4 Twitch Runner, 1 Static Carrier | 11 | áp lực nhanh |
| 92s | 8 Blank Walker, 3 Static Carrier | 17 | finale Static convoy |

Objective sao:

- 1 sao: thắng stage
- 2 sao: không để Static Carrier nổ trong khu vực sát cổng
- 3 sao: hoàn thành trong 105 giây

### World 1 Stage 9

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | endurance cuối world, kiểm tra giữ cổng ổn định |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 5 |
| Enemy pool | Blank Walker, Twitch Runner, Static Carrier |
| Thời lượng mục tiêu | 120 giây |
| Budget mục tiêu | 64 |
| Điểm khó | wave overlap, không có khoảng nghỉ dài |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 6 Blank Walker | 6 | mở đầu đông hơn |
| 16s | 3 Twitch Runner | 6 | ép giữ tuyến |
| 32s | 5 Blank Walker, 1 Static Carrier | 8 | static có cover |
| 50s | 5 Blank Walker, 3 Twitch Runner | 11 | pressure chính |
| 70s | 2 Static Carrier, 2 Twitch Runner | 10 | nguy hiểm nếu cổng đã mất máu |
| 90s | 8 Blank Walker, 2 Twitch Runner | 12 | wave đông |
| 108s | 5 Blank Walker, 2 Static Carrier | 11 | finale |

Objective sao:

- 1 sao: thắng stage
- 2 sao: không để quá 4 enemy chạm cổng
- 3 sao: cổng Aegis còn trên 60% HP

### World 1 Stage 10

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | bài kiểm tra tổng hợp trước boss |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 5 |
| Enemy pool | Blank Walker, Twitch Runner, Static Carrier |
| Thời lượng mục tiêu | 120 giây |
| Budget mục tiêu | 72 |
| Điểm khó | Static Carrier xuất hiện ở finale, runner ép người chơi không thể chỉ focus một loại enemy |

Wave:

| Thời điểm | Spawn | Budget | Ghi chú |
| --------: | ----- | -----: | ------- |
| 0s | 6 Blank Walker | 6 | setup |
| 14s | 4 Twitch Runner | 8 | runner spike |
| 30s | 6 Blank Walker, 1 Static Carrier | 9 | static đầu |
| 48s | 5 Blank Walker, 3 Twitch Runner | 11 | mixed pressure |
| 68s | 3 Static Carrier | 9 | objective 2 sao bắt đầu nặng |
| 84s | 8 Blank Walker, 3 Twitch Runner | 14 | wave đông |
| 102s | 6 Blank Walker, 3 Static Carrier | 15 | finale Static convoy |

Objective sao:

- 1 sao: thắng stage
- 2 sao: hạ toàn bộ Static Carrier trước khi chạm cổng
- 3 sao: hoàn thành trong 100 giây

## World 1 Boss Stage

Boss: **Patient Zero Escort**

Thông tin chính:

| Trường | Giá trị |
| ------ | ------- |
| Mục tiêu thiết kế | dạy focus target, hạ hộ vệ để ngắt hồi máu boss |
| Hero có thể dùng | Kael Voss, Mira Sane |
| Level kỳ vọng | 5 |
| Enemy pool | Patient Zero Escort, Blank Walker, Static Carrier |
| Thời lượng mục tiêu | 170-210 giây |
| Điểm khó | boss hồi máu khi còn hộ vệ, summon thêm wave nhỏ |

Chỉ số boss ở level 5 theo công thức hiện tại:

| Chỉ số | Giá trị |
| ------ | ------: |
| HP | 2664 |
| ATK | 57 |
| DEF | 13 |

Mechanic:

- Boss đi chậm từ bên phải vào tuyến.
- Boss bắt đầu trận với 4 Blank Walker hộ vệ.
- Khi còn ít nhất 1 hộ vệ, boss hồi 1.5% HP tối đa mỗi 8 giây.
- Mỗi lần boss hồi máu được tính là 1 lần cho objective sao.
- Mỗi 35 giây, boss triệu hồi thêm Blank Walker.
- Ở 60% HP, boss gọi thêm 2 Static Carrier.
- Ở 30% HP, boss gọi thêm 3 Static Carrier theo hàng sau.
- Static Carrier trong boss stage chủ yếu buộc người chơi không chỉ focus boss.

Wave và boss timeline:

| Thời điểm | Sự kiện | Ghi chú |
| --------: | ------- | ------- |
| 0s | Boss + 4 Blank Walker hộ vệ | người chơi phải deploy Kael trước |
| 20s | 5 Blank Walker | tăng áp lực tuyến |
| 35s | Boss summon 4 Blank Walker | summon chu kỳ đầu |
| 55s | 2 Static Carrier, 3 Blank Walker | buộc Mira xử lý mục tiêu nguy hiểm |
| 70s | Boss summon 4 Blank Walker | summon chu kỳ |
| 60% HP | Boss gọi 2 Static Carrier | phase pressure |
| 105s | Boss summon 5 Blank Walker | nếu damage thấp, tuyến bị đông |
| 130s | 3 Static Carrier | kiểm tra focus target |
| 30% HP | Boss gọi 3 Static Carrier | phase cuối |
| 160s | 6 Blank Walker, 2 Static Carrier | finale nếu boss chưa chết |

Objective sao:

- 1 sao: thắng boss stage
- 2 sao: hạ toàn bộ hộ vệ trước khi boss hồi máu quá 2 lần
- 3 sao: cổng Aegis còn trên 50% HP

Ghi chú cân bằng:

- Nếu người chơi level 5 và deploy đúng, boss nên chết trước 180 giây.
- Nếu người chơi bỏ qua hộ vệ, boss hồi đủ lâu để trận kéo dài và mất sao 2.
- Nếu người chơi chỉ focus hộ vệ mà không xử lý Static Carrier, cổng dễ mất HP và mất sao 3.
- Boss stage không nên yêu cầu Riven hoặc Iris vì hai hero này chưa mở ở World 1.

## Template Viết Stage Mới

Khi viết stage mới, dùng template này:

```text
World X Stage Y

Player State:
- hero available:
- expected hero level:
- formation slots:
- systems unlocked:

Stage Intent:
- teaches/tests:
- main difficulty:
- star pressure:

Enemy Pool:
- enemy A:
- enemy B:
- enemy C:

Runtime:
- target duration:
- target budget:

Wave Plan:
- 0s:
- 15s:
- 30s:
- 50s:
- 75s:
- finale:

Failure Pattern:
- player fails if:

Balance Notes:
- too easy if:
- too hard if:
```

## Quy Tắc Nhân Rộng Sang World Khác

Mỗi world nên đi theo nhịp:

| Stage | Vai trò |
| ----- | ------- |
| 1 | giới thiệu theme world bằng enemy chính số lượng ít |
| 2 | củng cố theme với objective giữ cổng hoặc tốc độ |
| 3 | giới thiệu enemy/cơ chế phụ |
| 4 | trộn enemy mới và enemy cũ |
| 5 | thêm pressure giữa world |
| 6 | kiểm tra counter bằng đội hình hợp lý |
| 7 | tăng mật độ hoặc thêm elite nhiều hơn |
| 8 | stress test cơ chế world |
| 9 | endurance trước màn cuối |
| 10 | bài kiểm tra tổng hợp trước boss |
| Boss | boss dùng cơ chế world ở dạng rõ nhất |

Ví dụ:

- World 2: tăng độ khó bằng Twitch Runner, Jaw Crawler và các pha xuyên tuyến.
- World 3: tăng độ khó bằng Signal Drain, Desync và Mute Leech.
- World 4: tăng độ khó bằng giáp dày và pháo kích tuyến sau.
- World 5: tăng độ khó bằng enemy haste và wave đông.
- World 6: tăng độ khó bằng hồi máu enemy và Toxic Suppression.
- World 7: tăng độ khó bằng backline dive.
- World 8: tăng độ khó bằng node phụ và khóa nộ.
- World 9: tăng độ khó bằng enemy evolve và boss copy skill.
- World 10: tăng độ khó bằng tổng hợp toàn bộ cơ chế cũ.

## Checklist Trước Khi Chốt Một Stage

Một stage chỉ được xem là đủ rõ khi trả lời được:

- Người chơi có hero nào?
- Level kỳ vọng là bao nhiêu?
- Stage dài khoảng bao lâu?
- Enemy nào được phép xuất hiện?
- Tổng budget khoảng bao nhiêu?
- Wave đầu có đủ nhẹ để người chơi setup không?
- Enemy mới có được giới thiệu bằng số lượng nhỏ trước không?
- Finale có kiểm tra đúng cơ chế chính không?
- Objective 2 sao và 3 sao có bám vào điểm khó của stage không?
- Nếu người chơi thua, lý do có dễ hiểu không?
