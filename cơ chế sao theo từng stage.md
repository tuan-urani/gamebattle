# Cơ Chế Sao Theo Từng Stage

## Mục tiêu tài liệu

Tài liệu này thống kê chi tiết điều kiện **1 sao, 2 sao, 3 sao** cho toàn bộ stage của game.

Tổng quy mô hiện tại:

- 10 world
- mỗi world có 10 stage thường và 1 boss stage
- tổng cộng **110 stage**
- tối đa **330 sao**

## Quy tắc chung

- **1 sao**: thắng stage
- **2 sao**: hoàn thành objective phụ thứ nhất
- **3 sao**: hoàn thành objective phụ thứ hai

## Quy tắc mở boss

Trong mỗi world:

- 10 stage thường tạo thành tổng tối đa **30 sao**
- boss stage chỉ mở khi người chơi đã đạt đủ **30/30 sao** của 10 stage thường
- 3 sao của boss không dùng để mở boss, mà chỉ dùng để hoàn tất mốc **33/33 sao** của world

Điều này có nghĩa là người chơi có thể thắng từng stage thường với 1 sao, nhưng nếu chưa hoàn thiện đủ toàn bộ 30 sao thì vẫn chưa được vào boss.

## Quy ước đo objective

- `chạm cổng`: enemy chạm hitbox cổng Aegis ít nhất 1 lần
- `khu vực sát cổng`: 25% đoạn đường gần cổng Aegis nhất
- `backline`: hero hoặc unit đứng sau tanker chính
- `spawn`: thời điểm enemy cụ thể xuất hiện trên map
- `pulse`: một lần phát hiệu ứng diện rộng của enemy support hoặc boss
- `buff`: một lần enemy hỗ trợ kích hoạt thành công hiệu ứng tăng tốc hoặc tăng sức mạnh
- `evolve`: Red Host chuyển sang trạng thái tiến hóa trong trận

## World 1: Trại Sơ Tán Thất Thủ

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Cổng Aegis còn trên 80% HP | Không để quá 8 enemy chạm cổng |
| Stage 2 | Thắng stage | Cổng Aegis còn trên 75% HP | Hoàn thành trong 120 giây |
| Stage 3 | Thắng stage | Hạ Twitch Runner đầu tiên trong 8 giây kể từ lúc spawn | Cổng Aegis còn trên 75% HP |
| Stage 4 | Thắng stage | Không để quá 6 enemy chạm cổng | Hoàn thành trong 115 giây |
| Stage 5 | Thắng stage | Không để Static Carrier nổ trong khu vực sát cổng | Cổng Aegis còn trên 70% HP |
| Stage 6 | Thắng stage | Không để quá 5 enemy chạm cổng | Hoàn thành trong 110 giây |
| Stage 7 | Thắng stage | Hạ 2 Twitch Runner đầu tiên trong 10 giây kể từ lúc spawn | Cổng Aegis còn trên 65% HP |
| Stage 8 | Thắng stage | Không để Static Carrier nổ trong khu vực sát cổng | Hoàn thành trong 105 giây |
| Stage 9 | Thắng stage | Không để quá 4 enemy chạm cổng | Cổng Aegis còn trên 60% HP |
| Stage 10 | Thắng stage | Hạ toàn bộ Static Carrier trước khi chạm cổng | Hoàn thành trong 100 giây |
| Boss | Thắng boss stage | Hạ toàn bộ hộ vệ trước khi boss hồi máu quá 2 lần | Cổng Aegis còn trên 50% HP |

## World 2: Xa Lộ Di Tản

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Không để quá 3 Twitch Runner chạm cổng | Hoàn thành trong 125 giây |
| Stage 2 | Thắng stage | Không để quá 2 Jaw Crawler chạm cổng | Cổng Aegis còn trên 70% HP |
| Stage 3 | Thắng stage | Hạ 3 enemy tốc độ cao đầu tiên trong 8 giây kể từ lúc spawn | Hoàn thành trong 120 giây |
| Stage 4 | Thắng stage | Không để Static Carrier nổ trong khu vực sát cổng | Không để quá 4 enemy tốc độ cao chạm cổng |
| Stage 5 | Thắng stage | Cổng Aegis còn trên 65% HP | Hoàn thành trong 115 giây |
| Stage 6 | Thắng stage | Không để quá 3 enemy tốc độ cao chạm cổng | Hạ đợt Jaw Crawler đầu tiên trong 10 giây kể từ lúc spawn |
| Stage 7 | Thắng stage | Không để quá 1 Jaw Crawler chạm cổng | Hoàn thành trong 110 giây |
| Stage 8 | Thắng stage | Không để Static Carrier nổ trong khu vực sát cổng | Cổng Aegis còn trên 60% HP |
| Stage 9 | Thắng stage | Không để quá 2 enemy tốc độ cao chạm cổng | Hoàn thành trong 105 giây |
| Stage 10 | Thắng stage | Cổng Aegis còn trên 55% HP | Hạ đợt enemy tốc độ cao cuối trong 12 giây kể từ lúc spawn |
| Boss | Thắng boss stage | Trippo Motorico không chạm cổng quá 1 lần | Hoàn thành trong 180 giây |

## World 3: Khu Dân Cư Im Lặng

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Hero bị Signal Drain không quá 6 lần | Hoàn thành trong 130 giây |
| Stage 2 | Thắng stage | Hero bị Desync không quá 4 lần | Cổng Aegis còn trên 70% HP |
| Stage 3 | Thắng stage | Hạ Scream Spitter đầu tiên trong 10 giây kể từ lúc spawn | Hero bị Signal Drain không quá 5 lần |
| Stage 4 | Thắng stage | Mute Leech gây Rage Leech không quá 4 lần | Hero bị Desync không quá 4 lần |
| Stage 5 | Thắng stage | Hero bị Signal Drain không quá 5 lần | Hoàn thành trong 125 giây |
| Stage 6 | Thắng stage | Hero bị Desync không quá 3 lần | Cổng Aegis còn trên 65% HP |
| Stage 7 | Thắng stage | Hạ mỗi Scream Spitter trong 12 giây kể từ lúc spawn | Hero bị Signal Drain không quá 4 lần |
| Stage 8 | Thắng stage | Mute Leech gây Rage Leech không quá 3 lần | Hero bị Desync không quá 3 lần |
| Stage 9 | Thắng stage | Hero bị Signal Drain không quá 4 lần | Hoàn thành trong 120 giây |
| Stage 10 | Thắng stage | Không để quá 2 hero cùng lúc bị Desync | Cổng Aegis còn trên 60% HP |
| Boss | Thắng boss stage | Phá toàn bộ bản sao âm thanh trong 10 giây kể từ khi xuất hiện | Không để quá 2 hero cùng lúc bị Desync |

## World 4: Nhà Máy Gãy Xương

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Hạ Meat Shield Host đầu tiên trong 15 giây kể từ lúc spawn | Cổng Aegis còn trên 70% HP |
| Stage 2 | Thắng stage | Scream Spitter bắn trúng backline không quá 4 lần | Hoàn thành trong 135 giây |
| Stage 3 | Thắng stage | Hạ Patch Beast đầu tiên trong 20 giây kể từ lúc spawn | Cổng Aegis còn trên 70% HP |
| Stage 4 | Thắng stage | Hạ 2 enemy giáp dày trong 18 giây kể từ mỗi lần spawn | Không để hero backline bị hạ |
| Stage 5 | Thắng stage | Scream Spitter bắn trúng backline không quá 3 lần | Hoàn thành trong 130 giây |
| Stage 6 | Thắng stage | Patch Beast dùng heavy swing không quá 4 lần | Cổng Aegis còn trên 65% HP |
| Stage 7 | Thắng stage | Hạ 3 enemy giáp dày trước khi chạm cổng | Không để hero backline bị hạ |
| Stage 8 | Thắng stage | Hoàn thành trong 125 giây | Không để hero backline bị hạ |
| Stage 9 | Thắng stage | Scream Spitter bắn trúng backline không quá 2 lần | Cổng Aegis còn trên 60% HP |
| Stage 10 | Thắng stage | Hạ mọi Patch Beast trong 18 giây kể từ lúc spawn | Hoàn thành trong 120 giây |
| Boss | Thắng boss stage | Phá giáp Bombardiro Crocodilo trước mốc 150 giây | Không để hero backline bị hạ |

## World 5: Chợ Đêm Không Ngủ

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Bone Drummer buff không quá 3 lần | Hoàn thành trong 140 giây |
| Stage 2 | Thắng stage | Hạ Bone Drummer đầu tiên trong 10 giây kể từ lúc spawn | Cổng Aegis còn trên 70% HP |
| Stage 3 | Thắng stage | Tanker bị knockback nặng không quá 2 lần | Hoàn thành trong 135 giây |
| Stage 4 | Thắng stage | Bone Drummer buff không quá 2 lần | Cổng Aegis còn trên 70% HP |
| Stage 5 | Thắng stage | Hạ mỗi side wave trong 15 giây kể từ lúc spawn | Tanker bị knockback nặng không quá 2 lần |
| Stage 6 | Thắng stage | Hoàn thành trong 130 giây | Không để quá 4 enemy chạm cổng |
| Stage 7 | Thắng stage | Hạ 25 enemy trong 60 giây đầu | Bone Drummer buff không quá 2 lần |
| Stage 8 | Thắng stage | Tanker không bị đẩy về khu vực sát cổng | Hoàn thành trong 125 giây |
| Stage 9 | Thắng stage | Hạ mỗi side wave trong 12 giây kể từ lúc spawn | Không để quá 3 enemy chạm cổng |
| Stage 10 | Thắng stage | Bone Drummer buff không quá 1 lần | Hoàn thành trong 120 giây |
| Boss | Thắng boss stage | Hạ mọi wave phụ trong 15 giây kể từ lúc spawn | Tanker bị đẩy về khu vực sát cổng không quá 2 lần |

## World 6: Bệnh Viện Đen

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Regrowth Host hồi máu không quá 4 lần | Cổng Aegis còn trên 70% HP |
| Stage 2 | Thắng stage | Hero bị Toxic Suppression không quá 5 lần | Hoàn thành trong 145 giây |
| Stage 3 | Thắng stage | Hạ Regrowth Host đầu tiên trong 10 giây kể từ lúc spawn | Không để hero bị hạ |
| Stage 4 | Thắng stage | Regrowth Host hồi máu không quá 3 lần | Hero bị Toxic Suppression không quá 4 lần |
| Stage 5 | Thắng stage | Hoàn thành trong 140 giây | Không để quá 1 hero bị hạ |
| Stage 6 | Thắng stage | Mute Leech gây Rage Leech không quá 5 lần | Hero bị Toxic Suppression không quá 4 lần |
| Stage 7 | Thắng stage | Hạ mỗi Regrowth Host trong 12 giây kể từ lúc spawn | Cổng Aegis còn trên 65% HP |
| Stage 8 | Thắng stage | Enemy được hồi sinh không quá 2 lần | Hero bị Toxic Suppression không quá 3 lần |
| Stage 9 | Thắng stage | Hoàn thành trong 135 giây | Hero bị Toxic Suppression không quá 3 lần |
| Stage 10 | Thắng stage | Regrowth Host hồi máu không quá 2 lần | Không để hero bị hạ |
| Boss | Thắng boss stage | Dottore Mozzarella làm enemy hồi sinh không quá 6 lần | Hero bị Toxic Suppression không quá 5 lần |

## World 7: Thành Phố Méo Giọng

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Không để hero backline bị hạ | Hoàn thành trong 150 giây |
| Stage 2 | Thắng stage | Hạ Phase Stalker đầu tiên trong 12 giây kể từ lúc spawn | Cổng Aegis còn trên 70% HP |
| Stage 3 | Thắng stage | Phase Stalker đánh trúng backline không quá 3 lần | Hoàn thành trong 145 giây |
| Stage 4 | Thắng stage | Hạ Bone Drummer trong 10 giây kể từ lúc spawn | Không để hero backline bị hạ |
| Stage 5 | Thắng stage | Phase Stalker đánh trúng backline không quá 2 lần | Cổng Aegis còn trên 65% HP |
| Stage 6 | Thắng stage | Hoàn thành trong 140 giây | Không để quá 1 hero bị hạ |
| Stage 7 | Thắng stage | Hạ 2 elite trong 15 giây kể từ mỗi lần spawn | Không để hero backline bị hạ |
| Stage 8 | Thắng stage | Phase Stalker đánh trúng backline không quá 2 lần | Hoàn thành trong 135 giây |
| Stage 9 | Thắng stage | Không để hero backline bị hạ | Bone Drummer buff không quá 2 lần |
| Stage 10 | Thắng stage | Hoàn thành trong 130 giây | Không để quá 1 hero bị hạ |
| Boss | Thắng boss stage | Không để Ballerino Cappuccino hạ bất kỳ hero nào | Thắng trước khi boss dùng đủ 3 chuỗi chí mạng |

## World 8: Đài Phát Tín Hiệu

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Phá Signal Host đầu tiên trước pulse thứ 3 | Cổng Aegis còn trên 65% HP |
| Stage 2 | Thắng stage | Signal Drain toàn đội không quá 5 lần | Hoàn thành trong 155 giây |
| Stage 3 | Thắng stage | Hạ Signal Host đầu tiên trong 12 giây kể từ lúc spawn | Không để hero backline bị hạ |
| Stage 4 | Thắng stage | Signal Host phát pulse không quá 3 lần | Hoàn thành trong 150 giây |
| Stage 5 | Thắng stage | Phá mọi Signal Host trước pulse thứ 2 của chúng | Cổng Aegis còn trên 60% HP |
| Stage 6 | Thắng stage | Hoàn thành trong 145 giây | Signal Drain toàn đội không quá 4 lần |
| Stage 7 | Thắng stage | Hạ mỗi Signal Host trong 10 giây kể từ lúc spawn | Mute Leech gây Rage Leech không quá 4 lần |
| Stage 8 | Thắng stage | Hoàn thành trong 140 giây | Không để hero backline bị hạ |
| Stage 9 | Thắng stage | Signal Host phát pulse không quá 3 lần | Cổng Aegis còn trên 55% HP |
| Stage 10 | Thắng stage | Phá toàn bộ Signal Host trước khi wave cuối vào cổng | Hoàn thành trong 135 giây |
| Boss | Thắng boss stage | Phá 3 node phát sóng trước mốc 150 giây | Rage Lock hoặc Ultimate Lock trúng toàn đội không quá 2 lần |

## World 9: Vùng Đỏ Trung Tâm

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Hạ Red Host đầu tiên trước khi evolve | Cổng Aegis còn trên 60% HP |
| Stage 2 | Thắng stage | Phase Stalker đánh trúng backline không quá 3 lần | Hoàn thành trong 160 giây |
| Stage 3 | Thắng stage | Red Host evolve không quá 1 lần | Không để hero backline bị hạ |
| Stage 4 | Thắng stage | Hạ Patch Beast đầu tiên trong 18 giây kể từ lúc spawn | Hoàn thành trong 155 giây |
| Stage 5 | Thắng stage | Red Host evolve không quá 1 lần | Phase Stalker đánh trúng backline không quá 2 lần |
| Stage 6 | Thắng stage | Hoàn thành trong 150 giây | Không để quá 1 hero bị hạ |
| Stage 7 | Thắng stage | Hạ 2 Red Host trước khi chúng evolve | Cổng Aegis còn trên 55% HP |
| Stage 8 | Thắng stage | Red Host evolve không quá 1 lần | Hoàn thành trong 145 giây |
| Stage 9 | Thắng stage | Phase Stalker đánh trúng backline không quá 2 lần | Không để quá 1 hero bị hạ |
| Stage 10 | Thắng stage | Red Host evolve không quá 1 lần | Hoàn thành trong 140 giây |
| Boss | Thắng boss stage | Boss không copy cùng một skill nộ quá 2 lần | Hạ phase cuối trước khi boss đạt max power stack |

## World 10: Lõi Phát Xạ

| Stage | 1 sao | 2 sao | 3 sao |
| ----- | ----- | ----- | ----- |
| Stage 1 | Thắng stage | Cổng Aegis còn trên 50% HP | Core Guardian chạm cổng không quá 2 lần |
| Stage 2 | Thắng stage | Hoàn thành trong 170 giây | Signal Drain diện rộng không quá 4 lần |
| Stage 3 | Thắng stage | Không để hero backline bị hạ | Core Guardian chạm cổng không quá 2 lần |
| Stage 4 | Thắng stage | Hạ elite wave trong 20 giây kể từ lúc spawn | Cổng Aegis còn trên 45% HP |
| Stage 5 | Thắng stage | Không để quá 2 hero bị hạ | Debuff diện rộng không quá 6 lần |
| Stage 6 | Thắng stage | Hạ support elite trong 12 giây kể từ lúc spawn | Core Guardian chạm cổng không quá 1 lần |
| Stage 7 | Thắng stage | Cổng Aegis còn trên 40% HP | Không để quá 1 hero bị hạ |
| Stage 8 | Thắng stage | Hoàn thành trong 160 giây | Debuff diện rộng không quá 5 lần |
| Stage 9 | Thắng stage | Core Guardian không được chạm cổng | Không để hero backline bị hạ |
| Stage 10 | Thắng stage | Cổng Aegis còn trên 40% HP | Hoàn thành trong 155 giây |
| Boss | Thắng boss stage | Hoàn thành phase The Choir với ít hơn 6 lần dính debuff diện rộng | Kích hoạt xung nghịch pha trước mốc 240 giây |
