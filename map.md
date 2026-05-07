# Map

## Mục tiêu tài liệu

Tài liệu này định nghĩa cấu trúc world map, progression, boss, enemy focus và phần thưởng chính của từng khu vực.

Game đi theo hành trình:
**Căn cứ Aegis -> vùng sơ tán -> khu dân cư -> khu công nghiệp -> chợ đêm -> bệnh viện -> thành phố -> đài phát -> vùng đỏ -> lõi Tần Số Mẹ**.

## Cấu trúc world map

Mỗi world gồm:

- 10 stage thường
- 1 stage boss

Gợi ý unlock:

- vượt 10 stage thường và đạt đủ **30/30 sao** của 10 stage thường để mở boss
- hạ boss để mở world kế tiếp

## Loại node trên bản đồ

### Stage thường

Mỗi world có 10 stage thường. Độ khó tăng dần qua từng stage để người chơi farm EXP, nâng cấp hero và chuẩn bị cho boss.

Mục tiêu thắng của stage thường là **đẩy lane và phá ổ infected/cổng brainrot bên phải**.

Điều kiện thua là **cổng Aegis bên trái bị phá**. Enemy trong stage thường luôn tiến về phía cổng Aegis để tấn công và gây thua nếu người chơi không giữ tuyến.

### Stage boss

Trận cuối world. Có boss riêng, cơ chế riêng và phần thưởng mở khóa world tiếp theo.

Boss stage không mở ngay khi chỉ thắng đủ 10 stage thường. Người chơi phải hoàn thành đủ **30/30 sao** của 10 stage thường trong world đó mới được mở khóa boss.

Mục tiêu thắng của stage boss là **giết boss**. Khi boss chết, màn kết thúc thắng ngay, không cần phá thêm ổ infected hoặc cổng brainrot.

Điều kiện thua vẫn là **cổng Aegis bên trái bị phá**. Boss có thể trực tiếp tấn công cổng hoặc dùng wave phụ, node phụ, debuff và mechanic riêng để tạo áp lực lên cổng Aegis.

### Stage thử thách elite

Stage thử thách elite là node phụ mở từ World 2, không nằm trong chuỗi bắt buộc 10 stage thường + 1 stage boss của mỗi world.

Mục tiêu thắng/thua vẫn dùng luật của stage thường hoặc boss stage tùy biến thể, nhưng có modifier khó hơn như wave dày hơn, enemy elite xuất hiện sớm hơn, giới hạn thời gian gắt hơn hoặc objective sao phụ khắt khe hơn.

Stage thử thách elite dùng để farm thêm EXP, kiểm tra đội hình và tạo nội dung optional cho người chơi đã nâng cấp tốt. Không dùng node này để khóa tiến trình campaign chính.

## Level Và EXP Theo World

Mỗi world tương ứng khoảng 5 level hero.

| World | Level monster stage thường | Level boss | First Clear EXP stage thường | Repeat EXP stage thường | Boss First Clear EXP | Boss Repeat EXP |
| ----- | -------------------------: | ---------: | ---------------------------: | ----------------------: | -------------------: | --------------: |
| 1 | 1-5 | 5 | 80-125 | 45-63 | 290 | 140 |
| 2 | 6-10 | 10 | 95-140 | 53-71 | 330 | 160 |
| 3 | 11-15 | 15 | 110-155 | 61-79 | 370 | 180 |
| 4 | 16-20 | 20 | 125-170 | 69-87 | 410 | 200 |
| 5 | 21-25 | 25 | 140-185 | 77-95 | 450 | 220 |
| 6 | 26-30 | 30 | 155-200 | 85-103 | 490 | 240 |
| 7 | 31-35 | 35 | 170-215 | 93-111 | 530 | 260 |
| 8 | 36-40 | 40 | 185-230 | 101-119 | 570 | 280 |
| 9 | 41-45 | 45 | 200-245 | 109-127 | 610 | 300 |
| 10 | 46-50 | 50 | 215-260 | 117-135 | 650 | 320 |

EXP trong bảng là EXP đưa vào kho EXP tướng sau khi thắng stage. Người chơi dùng EXP này trong kho tướng để nâng level hero mong muốn.

## Enemy Theo Stage

Cùng một monster có thể xuất hiện ở nhiều world, nhưng chỉ số sẽ khác nhau do monster level tăng theo world và stage.

File tổng hợp nhanh về roster, stat và monster theo world nằm ở **character_monster_stat_master.md**.

Ví dụ:

- Twitch Runner ở World 1 là level 2 đến 5
- Twitch Runner ở World 2 là level 6 đến 10
- Twitch Runner ở World 5 là level 21 đến 25

Vì vậy enemy cùng tên không được copy stat y nguyên giữa các map.

| World | Stage 1-3 | Stage 4-6 | Stage 7-10 | Boss stage |
| ----- | --------- | --------- | ---------- | ---------- |
| 1 | Blank Walker | Blank Walker, Twitch Runner | Blank Walker, Twitch Runner, Static Carrier | Patient Zero Escort, Blank Walker, Static Carrier |
| 2 | Twitch Runner, Blank Walker | Twitch Runner, Jaw Crawler | Twitch Runner, Jaw Crawler, Static Carrier | Trippo Motorico, Twitch Runner |
| 3 | Blank Walker, Scream Spitter | Scream Spitter, Mute Leech | Scream Spitter, Mute Leech, Blank Walker | Tralalero Tralala Prime, Mute Leech |
| 4 | Meat Shield Host, Scream Spitter | Meat Shield Host, Patch Beast | Meat Shield Host, Patch Beast, Scream Spitter | Bombardiro Crocodilo, Meat Shield Host |
| 5 | Twitch Runner, Bone Drummer | Bone Drummer, Meat Shield Host | Bone Drummer, Twitch Runner, Meat Shield Host | Tung Tung Tung Sahur, Twitch Runner, Bone Drummer |
| 6 | Mute Leech, Scream Spitter | Regrowth Host, Mute Leech | Regrowth Host, Scream Spitter, Mute Leech | Dottore Mozzarella, Regrowth Host |
| 7 | Phase Stalker, Mute Leech | Phase Stalker, Bone Drummer | Phase Stalker, Mute Leech, Bone Drummer | Ballerino Cappuccino, Phase Stalker |
| 8 | Signal Host, Scream Spitter | Signal Host, Mute Leech | Signal Host, Scream Spitter, Mute Leech | La Torre Frequenza, Signal Host |
| 9 | Red Host, Patch Beast | Red Host, Phase Stalker | Red Host, Patch Beast, Phase Stalker | Chimpanzini Bananini Red Host, Red Host |
| 10 | Red Host, Core Guardian | Core Guardian, Signal Host, Red Host | Core Guardian, Red Host, Signal Host, Phase Stalker, Patch Beast | The Mother Frequency, Core Guardian |

## Objective Sao Theo World

Mỗi stage tối đa 3 sao:

- 1 sao: thắng stage
- 2 sao và 3 sao: objective phụ theo world hoặc boss mechanic

Objective phụ trong bảng là mẫu cho stage thường của từng world. Stage boss dùng objective riêng ở cột cuối.

Bảng chi tiết cho từng stage cụ thể nằm trong file **cơ chế sao theo từng stage.md**.

Sao của từng stage được cộng vào **Thành tựu sao World**. Với mỗi world, **30 sao từ 10 stage thường** là điều kiện bắt buộc để mở boss. Sau khi hạ boss, người chơi có thể lấy sao boss để hoàn tất mốc **33 sao** và mở rương hoàn hảo của world.

| World | Objective phụ stage thường | Objective phụ boss stage |
| ----- | -------------------------- | ------------------------ |
| 1 | cổng Aegis còn trên 60% HP; không để quá 5 enemy chạm cổng | hạ toàn bộ hộ vệ trước khi boss hồi máu quá 2 lần; cổng còn trên 50% HP |
| 2 | không để quá 3 Twitch Runner hoặc Jaw Crawler vượt tuyến; thắng trước mốc thời gian | chặn đủ các pha lao của Trippo Motorico; không để runner được gọi chạm cổng |
| 3 | hero bị Signal Drain không quá 6 lần; hero bị Desync không quá 4 lần | phá bản sao âm thanh trong 10 giây; không để quá 2 hero cùng lúc bị Desync |
| 4 | hạ Meat Shield Host hoặc Patch Beast trong thời gian yêu cầu; không để Scream Spitter bắn tuyến sau quá 5 lần | phá giáp Bombardiro Crocodilo trước mốc thời gian; không để hero tuyến sau chết |
| 5 | diệt đủ số enemy trong chuỗi combo; không để Bone Drummer buff quá 3 wave | hạ wave phụ trong thời gian yêu cầu; tanker không bị đẩy lùi về sát cổng quá 2 lần |
| 6 | không để Regrowth Host hồi máu quá 4 lần; hero bị Toxic Suppression không quá 5 lần | ngắt hồi máu của Dottore Mozzarella; không để boss hồi sinh quá 6 enemy |
| 7 | không để Phase Stalker hạ hero tuyến sau; hạ elite trong thời gian yêu cầu | Ballerino Cappuccino không được hạ hero máu thấp; thắng trước khi boss dùng đủ 3 chuỗi chí mạng |
| 8 | phá Signal Host trước khi phát Signal Drain toàn bản đồ quá 3 lần; giữ ít nhất 2 skill nộ dùng được sau đợt khóa | phá 3 node phát sóng trước mốc thời gian; không để Rage Lock và Ultimate Lock trúng toàn đội quá 2 lần |
| 9 | hạ Red Host trước khi tiến hóa quá 2 lần; không để Phase Stalker xuyên tuyến sau | boss không copy cùng một skill nộ quá 2 lần; hạ phase cuối trước khi boss đạt stack tăng sức mạnh tối đa |
| 10 | sống sót qua elite wave với cổng trên 40% HP; không để Core Guardian chạm cổng quá 2 lần | hoàn thành phase The Choir với ít hơn 6 debuff diện rộng; kích hoạt xung nghịch pha trước mốc thời gian |

### Quy tắc biến thể theo stage

Trong cùng một world, không cần tất cả stage dùng y nguyên cùng một objective.

Gợi ý:

- Stage 1-3: objective dễ, tập trung dạy cơ chế world.
- Stage 4-6: objective vừa, bắt đầu yêu cầu người chơi counter enemy chính.
- Stage 7-10: objective khó, yêu cầu đội hình và nâng cấp hợp lý.
- Boss stage: objective gắn trực tiếp với boss mechanic.

## World 1: Trại Sơ Tán Thất Thủ

Bối cảnh: khu ngoại ô từng là nơi sơ tán dân thường.

Chủ đề:

- tutorial
- phòng tuyến đầu tiên
- người chơi đối mặt với infected từng là dân thường

Enemy chính:

- Blank Walker
- Twitch Runner
- Static Carrier

Boss: **Patient Zero Escort**

Cơ chế boss:

- có nhiều hộ vệ
- boss hồi máu khi hộ vệ còn sống
- dạy người chơi ưu tiên mục tiêu

Mở khóa:

- Vanguard Breaker
- Pulse Ranger
- hệ thống nâng cấp hero level

## World 2: Xa Lộ Di Tản

Bối cảnh: cao tốc kẹt xe, đoàn di tản bị nhiễm, trạm xăng và xe buýt cháy.

Chủ đề:

- enemy tốc độ cao
- tuyến phòng thủ dễ bị xuyên qua

Enemy chính:

- Twitch Runner
- Jaw Crawler
- Static Carrier

Boss: **Trippo Motorico**

Cơ chế boss:

- lao nhanh theo từng nhịp
- càng ít máu càng tăng tốc
- gọi thêm runner sau mỗi lần lao

Mở khóa:

- Core Engineer
- bẫy làm chậm
- stage thử thách elite

## World 3: Khu Dân Cư Im Lặng

Bối cảnh: khu phố đóng kín, loa trong nhà phát âm thanh lặp, đường phố không còn tiếng người.

Chủ đề:

- nhiễu âm
- Signal Drain và Desync
- enemy làm rối đội hình

Enemy chính:

- Scream Spitter
- Mute Leech
- Blank Walker

Boss: **Tralalero Tralala Prime**

Cơ chế boss:

- gây Signal Drain làm chậm tốc độ tích nộ
- gây Desync khiến unit đánh hụt
- tạo bản sao âm thanh

Mở khóa:

- Resonance Blade
- objective chống debuff
- hệ thống nâng cấp skill nộ theo mốc level, bậc 2 ở level 15

## World 4: Nhà Máy Gãy Xương

Bối cảnh: khu công nghiệp biến dạng, dây chuyền sản xuất lẫn với mô infected.

Chủ đề:

- enemy tanker
- pháo kích tuyến sau
- áp lực giáp dày

Enemy chính:

- Meat Shield Host
- Patch Beast
- Scream Spitter

Boss: **Bombardiro Crocodilo**

Cơ chế boss:

- bắn đạn hữu cơ vào tuyến sau
- có giáp dày
- cần unit áp sát hoặc focus đúng mục tiêu giáp dày

Mở khóa:

- formation preset
- counter enemy giáp dày

## World 5: Chợ Đêm Không Ngủ

Bối cảnh: khu chợ đêm đầy đèn, biển hiệu, nhạc lặp và infected tụ tập theo nhịp.

Chủ đề:

- wave đông
- enemy được buff tốc độ
- trận đấu có nhịp nhanh

Enemy chính:

- Bone Drummer
- Twitch Runner
- Meat Shield Host

Boss: **Tung Tung Tung Sahur**

Cơ chế boss:

- gõ nhịp tăng tốc toàn đàn
- gọi wave phụ
- tạo xung đẩy lùi tanker

Mở khóa:

- Aegis Medic
- hiển thị thanh nộ của unit
- đội hình hồi máu và giải debuff

## World 6: Bệnh Viện Đen

Bối cảnh: bệnh viện nghiên cứu nơi lưu hồ sơ giai đoạn đầu dịch.

Chủ đề:

- hồi máu enemy
- Toxic Suppression
- hé lộ khả năng hoàn nguyên người nhiễm

Enemy chính:

- Mute Leech
- Scream Spitter
- Regrowth Host

Boss: **Dottore Mozzarella**

Cơ chế boss:

- hồi máu cho enemy
- hồi sinh quái đã chết
- tạo vùng độc gây Toxic Suppression, giảm hồi máu của người chơi

Mở khóa:

- counter hồi máu
- tối ưu Aegis Medic bằng EXP và mở skill nộ bậc 3 ở level 30
- lore về cơ chế hoàn nguyên

## World 7: Thành Phố Méo Giọng

Bối cảnh: đô thị trung tâm, màn hình quảng cáo và loa công cộng phát tín hiệu brainrot.

Chủ đề:

- enemy elite nhiều
- sát thủ tuyến sau
- áp lực tinh thần lên Quân Đoàn Aegis

Enemy chính:

- Mute Leech
- Bone Drummer
- Phase Stalker

Boss: **Ballerino Cappuccino**

Cơ chế boss:

- né đòn
- lao vào tuyến sau
- gây chí mạng lên hero yếu máu

Mở khóa:

- Overdrive Titan
- chế độ thử thách world cũ
- replay farm EXP world cũ hiệu quả hơn

## World 8: Đài Phát Tín Hiệu

Bối cảnh: trạm phát sóng khổng lồ khuếch đại Tần Số Mẹ.

Chủ đề:

- phá node phụ
- Signal Drain toàn bản đồ
- trận boss có nhiều mục tiêu

Enemy chính:

- Scream Spitter
- Mute Leech
- Signal Host

Boss: **La Torre Frequenza**

Cơ chế boss:

- gây Rage Lock và Ultimate Lock trong thời gian ngắn
- buff infected toàn màn
- phải phá 3 node phát sóng trước khi boss nhận sát thương lớn

Mở khóa:

- nâng cấp formation slot thứ năm
- node phụ trong boss stage
- giảm chi phí một số stage cũ

## World 9: Vùng Đỏ Trung Tâm

Bối cảnh: vùng dịch đỏ, nơi mặt đất, không khí và âm thanh như một cơ thể sống.

Chủ đề:

- enemy tiến hóa trong trận
- boss học skill nộ của hero
- chuẩn bị cho world cuối

Enemy chính:

- Patch Beast
- Phase Stalker
- Red Host

Boss: **Chimpanzini Bananini Red Host**

Cơ chế boss:

- đổi phase theo máu
- bắt chước skill nộ của hero kích hoạt nhiều nhất
- càng kéo dài càng mạnh

Mở khóa:

- xung nghịch pha Aegis
- nâng skill nộ bậc 4 ở level 45
- cổng vào lõi mẹ

## World 10: Lõi Phát Xạ

Bối cảnh: tâm dịch, lõi phát xạ của Tần Số Mẹ.

Chủ đề:

- boss cuối nhiều phase
- toàn bộ cơ chế cũ quay lại
- mục tiêu cuối là phá lõi và hoàn nguyên nhân loại

Enemy chính:

- tất cả biến thể elite
- Red Host
- Core Guardian

Boss: **The Mother Frequency**

Phase:

- **The Choir of Tralala**: âm thanh hỗn loạn, gây Signal Drain, Desync, Rage Lock và Ultimate Lock diện rộng
- **Bombardiro Rex**: hình thái công thành, sát thương cực cao
- **Mother Frequency Core**: lõi thật, cần dùng xung nghịch pha Aegis

Mở khóa sau khi hoàn thành:

- ending chính
- chế độ New Game Plus hoặc Infinite Outbreak
- boss rush

## Quy tắc mở rộng map sau này

- Mỗi world mới cần có một biến thể brainrot trung tâm.
- Boss phải có cơ chế riêng, không chỉ tăng chỉ số.
- Mỗi world nên mở một hệ thống, hero hoặc dạng thử thách mới.
- Môi trường phải kể chuyện: càng gần lõi mẹ, thế giới càng ít giống thế giới con người.
