# Chế Độ Nâng Cấp Hero

## Mục tiêu thiết kế

Hệ nâng cấp hiện tại chỉ tập trung vào **EXP tướng**, **hero level** và **skill nộ**.

Phiên bản hiện tại không dùng thêm hệ progression phụ nào khác.

Khi thắng stage, người chơi nhận **EXP tướng**. EXP này đi vào kho EXP tướng và được dùng để nâng level hero.

## Vai trò NPC hậu phương

Đội Nghiên Cứu Kháng Não là nhóm NPC hậu phương phụ trách nâng cấp hero và phân tích dữ liệu sau mỗi world.

Trong UI nâng cấp:

- **Dr. Lena Oris** phụ trách hero level và nâng cấp skill nộ

## Nâng cấp hero

### Thuộc tính hero

Mỗi hero chỉ có các chỉ số chính:

- HP
- ATK
- DEF
- tốc độ tích nộ

### Level

Hero level tăng trực tiếp các chỉ số trên.

Ví dụ:

- level 1 lên level 2: tăng một lượng HP, ATK, DEF và tốc độ tích nộ theo bảng chỉ số của hero đó
- mỗi hero có thể có tốc độ tăng chỉ số khác nhau tùy vai trò
- tanker ưu tiên tăng HP và DEF
- damage dealer ưu tiên tăng ATK
- support có thể tăng tốc độ tích nộ tốt hơn để dùng skill nộ thường xuyên hơn

Hero level tối đa: **50**.

Hero mới mở khóa bắt đầu ở **level 1**. Vì EXP nằm trong kho chung, người chơi có thể dùng EXP đã farm trước đó để nâng hero mới mà không cần bắt hero đó tham gia trận.

Nguồn EXP:

- hoàn thành stage thường
- thưởng lớn khi hạ boss stage
- chơi lại stage để farm EXP cơ bản, có giới hạn bằng stamina để tránh farm vô hạn

EXP không tự động cộng thẳng vào hero sau trận. Khi thắng stage, EXP được đưa vào **kho EXP tướng** của người chơi. Người chơi vào kho tướng, chọn hero muốn nâng, rồi dùng EXP trong kho để nâng level hero đó.

## Mục tiêu level theo world

| World | Level khuyến nghị khi bắt đầu | Level khuyến nghị trước boss |
| ----- | ----------------------------: | ---------------------------: |
| 1 | 1 | 5 |
| 2 | 6 | 10 |
| 3 | 11 | 15 |
| 4 | 16 | 20 |
| 5 | 21 | 25 |
| 6 | 26 | 30 |
| 7 | 31 | 35 |
| 8 | 36 | 40 |
| 9 | 41 | 45 |
| 10 | 46 | 50 |

## EXP cần để lên cấp

EXP để nâng từ level `N` lên `N+1`:

```text
EXP cần = 100 + (N - 1) * 20
```

Ví dụ:

| Từ level | Lên level | EXP cần |
| -------: | --------: | ------: |
| 1 | 2 | 100 |
| 2 | 3 | 120 |
| 3 | 4 | 140 |
| 4 | 5 | 160 |
| 5 | 6 | 180 |
| 9 | 10 | 260 |
| 14 | 15 | 360 |
| 19 | 20 | 460 |
| 29 | 30 | 660 |
| 49 | 50 | 1060 |

## Tổng EXP mốc quan trọng

| Mốc level đạt được | Tổng EXP cộng dồn |
| -----------------: | ----------------: |
| 5 | 520 |
| 10 | 1620 |
| 15 | 3220 |
| 20 | 5320 |
| 25 | 7920 |
| 30 | 11020 |
| 35 | 14620 |
| 40 | 18720 |
| 45 | 23320 |
| 50 | 28420 |

## EXP nhận từ stage

Mỗi stage cho 2 phần EXP:

- **First Clear EXP**: thưởng lần đầu để đẩy progression chính
- **Repeat Clear EXP**: thưởng khi farm lại map

EXP này là tài nguyên chung trong kho tướng, không phải EXP riêng của từng hero.

Quy tắc:

```text
First Clear EXP stage thường = 60 + world * 15 + stage * 5
Repeat Clear EXP stage thường = 35 + world * 8 + stage * 2
Boss First Clear EXP = 250 + world * 40
Boss Repeat Clear EXP = 120 + world * 20
```

Ô trong bảng dưới dùng format:

```text
First Clear EXP / Repeat Clear EXP
```

| World | Stage 1 | Stage 2 | Stage 3 | Stage 4 | Stage 5 | Stage 6 | Stage 7 | Stage 8 | Stage 9 | Stage 10 |
| ----- | ------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- | -------- |
| 1 | 80/45 | 85/47 | 90/49 | 95/51 | 100/53 | 105/55 | 110/57 | 115/59 | 120/61 | 125/63 |
| 2 | 95/53 | 100/55 | 105/57 | 110/59 | 115/61 | 120/63 | 125/65 | 130/67 | 135/69 | 140/71 |
| 3 | 110/61 | 115/63 | 120/65 | 125/67 | 130/69 | 135/71 | 140/73 | 145/75 | 150/77 | 155/79 |
| 4 | 125/69 | 130/71 | 135/73 | 140/75 | 145/77 | 150/79 | 155/81 | 160/83 | 165/85 | 170/87 |
| 5 | 140/77 | 145/79 | 150/81 | 155/83 | 160/85 | 165/87 | 170/89 | 175/91 | 180/93 | 185/95 |
| 6 | 155/85 | 160/87 | 165/89 | 170/91 | 175/93 | 180/95 | 185/97 | 190/99 | 195/101 | 200/103 |
| 7 | 170/93 | 175/95 | 180/97 | 185/99 | 190/101 | 195/103 | 200/105 | 205/107 | 210/109 | 215/111 |
| 8 | 185/101 | 190/103 | 195/105 | 200/107 | 205/109 | 210/111 | 215/113 | 220/115 | 225/117 | 230/119 |
| 9 | 200/109 | 205/111 | 210/113 | 215/115 | 220/117 | 225/119 | 230/121 | 235/123 | 240/125 | 245/127 |
| 10 | 215/117 | 220/119 | 225/121 | 230/123 | 235/125 | 240/127 | 245/129 | 250/131 | 255/133 | 260/135 |

## EXP nhận từ boss

| World | Stamina boss | Boss First Clear EXP | Boss Repeat EXP | Repeat EXP / stamina |
| ----- | -----------: | -------------------: | --------------: | -------------------: |
| 1 | 10 | 290 | 140 | 14 |
| 2 | 10 | 330 | 160 | 16 |
| 3 | 10 | 370 | 180 | 18 |
| 4 | 12 | 410 | 200 | 16.67 |
| 5 | 12 | 450 | 220 | 18.33 |
| 6 | 12 | 490 | 240 | 20 |
| 7 | 15 | 530 | 260 | 17.33 |
| 8 | 15 | 570 | 280 | 18.67 |
| 9 | 15 | 610 | 300 | 20 |
| 10 | 15 | 650 | 320 | 21.33 |

Boss chỉ farm được sau khi đã mở boss. Mỗi boss của world yêu cầu người chơi đạt đủ **30/30 sao** từ 10 stage thường của world đó trước khi được vào đánh.

## Cơ chế farm EXP

Farm EXP là việc replay stage hoặc boss đã clear để nhận **Repeat Clear EXP**.

First Clear EXP chỉ nhận một lần. Sau đó, mọi lần thắng lại stage đó đều nhận Repeat Clear EXP.

Quy tắc farm:

- stage thường là nguồn farm ổn định nhất vì ngắn và dễ auto/replay
- boss cho EXP/stamina tốt hơn, nhưng tốn thời gian hơn, khó hơn và chỉ mở sau khi đã full 30/30 sao stage thường
- stage càng cao trong world thì EXP càng tốt
- replay stage vẫn tiêu tốn stamina như bình thường
- chỉ khi thắng stage mới nhận EXP
- thua hoặc thoát giữa chừng không nhận EXP để tránh lạm dụng
- EXP thắng trận đi vào kho EXP tướng
- người chơi tự quyết định dùng EXP đó cho hero nào

### Map farm khuyến nghị

Nếu xét stage thường, stage 10 của world đang farm thường là lựa chọn tốt nhất vì có Repeat EXP cao nhất trong world.

| World | Map farm nhanh | Stamina | First Clear EXP | Repeat EXP | Repeat EXP / stamina |
| ----- | -------------- | ------: | --------------: | ---------: | -------------------: |
| 1 | Stage 10 | 6 | 125 | 63 | 10.5 |
| 2 | Stage 10 | 6 | 140 | 71 | 11.83 |
| 3 | Stage 10 | 6 | 155 | 79 | 13.17 |
| 4 | Stage 10 | 8 | 170 | 87 | 10.88 |
| 5 | Stage 10 | 8 | 185 | 95 | 11.88 |
| 6 | Stage 10 | 8 | 200 | 103 | 12.88 |
| 7 | Stage 10 | 10 | 215 | 111 | 11.1 |
| 8 | Stage 10 | 10 | 230 | 119 | 11.9 |
| 9 | Stage 10 | 10 | 245 | 127 | 12.7 |
| 10 | Stage 10 | 10 | 260 | 135 | 13.5 |

Nếu xét tiết kiệm stamina, boss đã mở là lựa chọn tốt nhất. Nếu xét tốc độ clear và độ ổn định, stage 8 đến 10 của world hiện tại là lựa chọn an toàn hơn.

Khuyến nghị cho người chơi:

- nếu đang thiếu ít EXP để chạm mốc skill level 15, 30, 45: farm stage 8 đến 10 của world hiện tại
- nếu vừa mở world mới nhưng bị hụt sức mạnh: quay lại stage 9, 10 và boss của world trước
- nếu muốn lên nhanh hero mới mở khóa: farm EXP bằng đội hình mạnh, sau đó vào kho tướng để dùng EXP nâng hero mới

## Kho EXP tướng

Kho EXP tướng là nơi lưu EXP nhận được từ stage.

Quy tắc:

- EXP trong kho là tài nguyên chung
- hero không cần tham gia trận vẫn có thể được nâng bằng EXP trong kho
- nâng level phải được người chơi xác nhận trong màn hình kho tướng
- nếu thiếu EXP, nút nâng level bị khóa hoặc hiển thị thiếu bao nhiêu EXP

Flow nâng level:

1. Thắng stage hoặc boss.
2. Nhận EXP vào kho EXP tướng.
3. Vào kho tướng.
4. Chọn hero.
5. Bấm nâng level.
6. Trừ EXP trong kho và tăng chỉ số hero.

## Tăng chỉ số mỗi lần lên cấp

Mỗi lần lên level, hero tăng chỉ số theo bảng tăng trưởng cố định của class.

| Hero | Mỗi level tăng HP | Mỗi level tăng ATK | Mỗi level tăng DEF | Mỗi level tăng nộ/đòn |
| ---- | ----------------: | -----------------: | -----------------: | --------------------: |
| Kael Voss | 65 | 4 | 2 | 0.15 |
| Mira Sane | 34 | 6 | 1 | 0.20 |
| Mason Rook | 38 | 3 | 1 | 0.20 |
| Riven Hal | 42 | 7 | 1 | 0.18 |
| Iris Venn | 36 | 4 | 1 | 0.25 |
| Atlas-09 | 90 | 10 | 3 | 0.10 |

Ví dụ:

- Kael level 1 lên level 2: `+65 HP`, `+4 ATK`, `+2 DEF`, `+0.15 nộ/đòn`
- Mira level 1 lên level 2: `+34 HP`, `+6 ATK`, `+1 DEF`, `+0.20 nộ/đòn`
- Iris level 1 lên level 2: `+36 HP`, `+4 ATK`, `+1 DEF`, `+0.25 nộ/đòn`

Tăng trưởng này nên giữ cố định để người chơi dễ hiểu và đội dev dễ cân bằng.

## Mốc skill nộ theo level

Skill nộ không tăng theo từng level. Skill nộ chỉ tăng bậc khi hero đạt các mốc level nhất định.

Mốc hiện tại được dãn theo max level 50 để late game vẫn còn mục tiêu nâng cấp rõ ràng:

- level 1: skill nộ bậc 1
- level 15: skill nộ lên bậc 2
- level 30: skill nộ lên bậc 3
- level 45: skill nộ lên bậc 4

Lý do chọn mốc này:

- bậc 2 rơi vào cuối World 3, sau khi người chơi đã quen với debuff và nhịp tích nộ
- bậc 3 rơi vào cuối World 6, khi game bắt đầu yêu cầu đội hình chống hồi máu và chống hiệu ứng kéo dài
- bậc 4 rơi vào cuối World 9, trước khi vào World 10 với full system và boss cuối nhiều phase

Ở phiên bản hiện tại, skill nộ **tự kích hoạt bậc mới khi hero đạt đủ level**. Không cần tài nguyên riêng và không cần farm gì ngoài EXP tướng.

Mỗi bậc skill nộ nên tăng hiệu ứng rõ ràng, không chỉ tăng sát thương theo phần trăm.

Ví dụ hướng nâng:

- skill đánh 1 mục tiêu có thể nâng thành đánh 2 mục tiêu
- skill hồi máu 1 đồng minh có thể nâng thành hồi 2 đồng minh
- skill tạo khiên có thể tăng thêm phạm vi hoặc thời gian tồn tại
- skill giải debuff có thể giải thêm số lượng debuff hoặc thêm kháng debuff ngắn hạn
- skill tạo Aegis Energy có thể tăng lượng energy hoặc tăng thời gian hiệu lực

## Giới hạn hệ progression

Game hiện tại không dùng thêm hệ tăng sức mạnh nào ngoài hero level và skill nộ.

Sức mạnh hero đến từ:

- level
- chỉ số nền tăng theo level
- nâng cấp skill nộ tại các mốc level

Reward sau trận hiện tại chỉ gồm:

- EXP tướng first clear
- EXP tướng repeat clear
- sao stage nếu đạt objective
