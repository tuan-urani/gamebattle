# Character Monster Stat Master

## Mục tiêu tài liệu

File này là bảng tổng hợp trung tâm cho character, monster, boss, level và chỉ số chiến đấu.

Các file khác có thể mô tả lore, skill, wave hoặc progression chi tiết hơn. Khi cần trả lời nhanh các câu hỏi sau thì dùng file này trước:

- tổng có bao nhiêu playable character
- tổng có bao nhiêu monster và boss
- hero, monster, boss có level ra sao
- HP, ATK, DEF của hero, monster, boss nằm ở đâu
- world/map nào dùng monster nào

## Quy mô roster V0.1

| Nhóm | Số lượng | Ghi chú |
| ---- | -------: | ------- |
| Playable hero | 6 | character chiến đấu người chơi có thể dùng |
| NPC hậu phương | 2 | không trực tiếp ra trận trong V0.1 |
| Monster thường/elite | 14 | enemy spawn trong stage thường và wave phụ boss |
| Boss world | 10 | mỗi world có 1 boss riêng |
| Tổng enemy type tính cả boss | 24 | 14 monster + 10 boss |

Không thêm hero, monster hoặc boss mới nếu chưa có vai trò gameplay riêng. Nếu chỉ cần tăng độ khó, ưu tiên tăng level, wave composition, objective sao hoặc modifier của stage.

## Công thức chung

### Sát thương

```text
Sát thương thực nhận = ATK * 100 / (100 + DEF mục tiêu)
```

### Hero stat theo level

Hero có level từ **1 đến 50**.

```text
Chỉ số hero level N = chỉ số level 1 + tăng mỗi level * (N - 1)
```

### Monster level theo stage

Monster thường và elite đi theo level của stage:

```text
Monster level stage thường = (world - 1) * 5 + ceil(stage / 2)
Monster level boss stage = world * 5
```

### Monster stat theo level

```text
HP  = HP level 1  * (1 + 0.09 * (monster level - 1))
ATK = ATK level 1 * (1 + 0.08 * (monster level - 1))
DEF = DEF level 1 * (1 + 0.07 * (monster level - 1))
```

Làm tròn số sau khi tính.

### Boss stat theo level

Boss có level riêng bằng `world * 5`.

```text
Boss HP  = HP gốc  * (1 + 0.12 * (boss level - 1))
Boss ATK = ATK gốc * (1 + 0.09 * (boss level - 1))
Boss DEF = DEF gốc * (1 + 0.08 * (boss level - 1))
```

Làm tròn số sau khi tính.

## Level theo world

| World | Hero level kỳ vọng | Monster level stage 1-2 | Stage 3-4 | Stage 5-6 | Stage 7-8 | Stage 9-10 | Boss level |
| ----- | -----------------: | ----------------------: | --------: | --------: | --------: | ---------: | ---------: |
| 1 | 1-5 | 1 | 2 | 3 | 4 | 5 | 5 |
| 2 | 6-10 | 6 | 7 | 8 | 9 | 10 | 10 |
| 3 | 11-15 | 11 | 12 | 13 | 14 | 15 | 15 |
| 4 | 16-20 | 16 | 17 | 18 | 19 | 20 | 20 |
| 5 | 21-25 | 21 | 22 | 23 | 24 | 25 | 25 |
| 6 | 26-30 | 26 | 27 | 28 | 29 | 30 | 30 |
| 7 | 31-35 | 31 | 32 | 33 | 34 | 35 | 35 |
| 8 | 36-40 | 36 | 37 | 38 | 39 | 40 | 40 |
| 9 | 41-45 | 41 | 42 | 43 | 44 | 45 | 45 |
| 10 | 46-50 | 46 | 47 | 48 | 49 | 50 | 50 |

## Hero theo world

| World | Hero có thể dùng khi bắt đầu world | Slot đội hình | Ghi chú unlock |
| ----- | ---------------------------------- | ------------: | -------------- |
| 1 | Kael Voss, Mira Sane | 4 | roster khởi đầu |
| 2 | Kael Voss, Mira Sane, Mason Rook | 4 | mở Mason Rook sau boss World 1 |
| 3 | Kael Voss, Mira Sane, Mason Rook, Riven Hal | 4 | mở Riven Hal sau boss World 2 |
| 4 | Kael Voss, Mira Sane, Mason Rook, Riven Hal | 4 | không mở hero mới |
| 5 | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn | 4 | mở Iris Venn sau boss World 4 |
| 6 | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn | 4 | không mở hero mới |
| 7 | Kael Voss, Mira Sane, Mason Rook, Riven Hal, Iris Venn, Atlas-09 | 4 | mở Atlas-09 sau boss World 6 |
| 8 | Toàn bộ 6 hero | 5 | mở formation slot thứ 5 |
| 9 | Toàn bộ 6 hero | 5 | full roster |
| 10 | Toàn bộ 6 hero | 5 | full roster |

## Playable hero stat level 1

| Hero | Class | Mở khóa | HP | ATK | DEF | Nộ/đòn | Tăng HP/level | Tăng ATK/level | Tăng DEF/level | Tăng nộ/level |
| ---- | ----- | ------: | -: | --: | --: | -----: | -------------: | --------------: | --------------: | ------------: |
| Kael Voss | Vanguard Breaker | World 1 | 760 | 52 | 26 | 8.5 | 65 | 4 | 2 | 0.15 |
| Mira Sane | Pulse Ranger | World 1 | 430 | 72 | 10 | 11.0 | 34 | 6 | 1 | 0.20 |
| Mason Rook | Core Engineer | World 2 | 500 | 20 | 14 | 10.0 | 38 | 3 | 1 | 0.20 |
| Riven Hal | Resonance Blade | World 3 | 520 | 88 | 14 | 12.0 | 42 | 7 | 1 | 0.18 |
| Iris Venn | Aegis Medic | World 5 | 460 | 38 | 12 | 13.0 | 36 | 4 | 1 | 0.25 |
| Atlas-09 | Overdrive Titan | World 7 | 1050 | 140 | 34 | 7.0 | 90 | 10 | 3 | 0.10 |

## Playable hero stat level 50

| Hero | HP | ATK | DEF | Nộ/đòn |
| ---- | -: | --: | --: | -----: |
| Kael Voss | 3945 | 248 | 124 | 15.9 |
| Mira Sane | 2096 | 366 | 59 | 20.8 |
| Mason Rook | 2362 | 167 | 63 | 19.8 |
| Riven Hal | 2578 | 431 | 63 | 20.8 |
| Iris Venn | 2224 | 234 | 61 | 25.3 |
| Atlas-09 | 5460 | 630 | 181 | 11.9 |

## Deploy cost hero V0.1

| Hero | Cost Aegis Energy | Cooldown deploy | Vai trò chính |
| ---- | ----------------: | --------------: | ------------- |
| Kael Voss | 20 | 18 giây | chặn tuyến, bảo vệ cổng |
| Mira Sane | 15 | 14 giây | sát thương tầm xa, xử lý runner và support |
| Mason Rook | 30 | 24 giây | tăng kinh tế energy, trận dài |
| Riven Hal | 25 | 20 giây | xử lý elite, support, boss phụ |
| Iris Venn | 35 | 26 giây | hồi máu, giải debuff |
| Atlas-09 | 60 | 45 giây | xoay trận, phá wave lớn, đánh boss |

## Monster thường và elite stat level 1

| Monster | Loại | HP | ATK | DEF | Vai trò |
| ------- | ---- | -: | --: | --: | ------- |
| Blank Walker | thường | 140 | 18 | 4 | đông, chậm, ép tuyến |
| Twitch Runner | thường | 95 | 24 | 2 | chạy nhanh, xuyên tuyến |
| Jaw Crawler | thường | 115 | 21 | 3 | bò thấp, khó bị một số unit bắn trúng |
| Static Carrier | thường | 180 | 28 | 5 | chết phát nổ nhiễu nhỏ |
| Meat Shield Host | elite | 420 | 34 | 16 | tanker che chắn đàn |
| Scream Spitter | elite | 160 | 30 | 3 | bắn xa vào tuyến trước |
| Bone Drummer | elite | 220 | 22 | 6 | buff tốc đánh hoặc tốc chạy cho enemy gần đó |
| Mute Leech | elite | 190 | 20 | 5 | gây Rage Leech và Signal Drain |
| Patch Beast | elite | 560 | 55 | 18 | chậm, rất trâu, đánh đau |
| Regrowth Host | elite | 250 | 18 | 8 | hồi máu hoặc tái kích hoạt enemy |
| Phase Stalker | elite | 260 | 65 | 7 | áp sát tuyến sau |
| Signal Host | elite | 300 | 28 | 10 | phát Signal Drain diện rộng |
| Red Host | elite | 480 | 70 | 14 | tiến hóa trong trận |
| Core Guardian | elite | 900 | 95 | 25 | bảo vệ lõi, xuất hiện cuối game |

## Monster behavior summary

| Monster | Di chuyển | Tầm đánh | Cơ chế chính |
| ------- | --------- | -------- | ------------ |
| Blank Walker | chậm | cận chiến | enemy nền, tạo số lượng |
| Twitch Runner | nhanh | cận chiến | chạy xuyên tuyến, ép deploy đúng nhịp |
| Jaw Crawler | bò thấp | cận chiến | khó bị một số unit bắn trúng |
| Static Carrier | chậm | cận chiến | chết phát nổ gây Signal Drain gần điểm nổ |
| Meat Shield Host | chậm | cận chiến | tanker che chắn enemy phía sau |
| Scream Spitter | chậm | tầm xa | bắn sóng âm, có cơ hội gây Desync |
| Bone Drummer | vừa | cận chiến | buff tốc độ/tốc đánh cho enemy gần đó |
| Mute Leech | vừa | cận chiến | gây Rage Leech và Signal Drain |
| Patch Beast | chậm | cận chiến | rất trâu, đánh đau, ép phá giáp/burst |
| Regrowth Host | chậm | hỗ trợ tầm trung | hồi máu hoặc tái kích hoạt enemy |
| Phase Stalker | nhanh | cận chiến | lướt vào backline nếu có khoảng trống |
| Signal Host | vừa | hỗ trợ toàn bản đồ | phát Signal Drain theo chu kỳ |
| Red Host | nhanh | cận chiến | tiến hóa/tăng sức mạnh nếu sống lâu |
| Core Guardian | chậm | cận chiến diện rộng | elite cuối game, gây áp lực lên cổng |

## Boss stat sau scale

| World | Boss | Level | HP | ATK | DEF | Vai trò |
| ----- | ---- | ----: | -: | --: | --: | ------- |
| 1 | Patient Zero Escort | 5 | 2664 | 57 | 13 | nhiều hộ vệ, dạy focus target |
| 2 | Trippo Motorico | 10 | 4992 | 105 | 21 | boss lao nhanh, gây thủng tuyến |
| 3 | Tralalero Tralala Prime | 15 | 7772 | 145 | 32 | Signal Drain, Desync |
| 4 | Bombardiro Crocodilo | 20 | 13776 | 211 | 60 | pháo kích, giáp dày |
| 5 | Tung Tung Tung Sahur | 25 | 15520 | 228 | 58 | buff wave, tạo áp lực liên tục |
| 6 | Dottore Mozzarella | 30 | 20608 | 245 | 73 | hồi máu, hồi sinh, Toxic Suppression |
| 7 | Ballerino Cappuccino | 35 | 21844 | 357 | 67 | lao vào tuyến sau, chí mạng |
| 8 | La Torre Frequenza | 40 | 31808 | 415 | 115 | Rage Lock, Ultimate Lock, node phụ |
| 9 | Chimpanzini Bananini Red Host | 45 | 38936 | 526 | 136 | học skill nộ, scale theo thời gian |
| 10 | The Mother Frequency | 50 | 58480 | 649 | 177 | boss cuối nhiều phase |

## Boss base stat

| World | Boss | Boss level | HP gốc | ATK gốc | DEF gốc |
| ----- | ---- | ---------: | -----: | ------: | ------: |
| 1 | Patient Zero Escort | 5 | 1800 | 42 | 10 |
| 2 | Trippo Motorico | 10 | 2400 | 58 | 12 |
| 3 | Tralalero Tralala Prime | 15 | 2900 | 64 | 15 |
| 4 | Bombardiro Crocodilo | 20 | 4200 | 78 | 24 |
| 5 | Tung Tung Tung Sahur | 25 | 4000 | 72 | 20 |
| 6 | Dottore Mozzarella | 30 | 4600 | 68 | 22 |
| 7 | Ballerino Cappuccino | 35 | 4300 | 88 | 18 |
| 8 | La Torre Frequenza | 40 | 5600 | 92 | 28 |
| 9 | Chimpanzini Bananini Red Host | 45 | 6200 | 106 | 30 |
| 10 | The Mother Frequency | 50 | 8500 | 120 | 36 |

## Monster theo world/map

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

## Boss theo world/map

| World | Map | Boss | Cơ chế boss chính | Counter chính |
| ----- | --- | ---- | ----------------- | ------------- |
| 1 | Trại Sơ Tán Thất Thủ | Patient Zero Escort | hộ vệ, hồi máu khi còn hộ vệ, summon Blank Walker | Pulse Ranger |
| 2 | Xa Lộ Di Tản | Trippo Motorico | lao nhanh, tăng tốc theo HP thấp, gọi runner | Vanguard Breaker |
| 3 | Khu Dân Cư Im Lặng | Tralalero Tralala Prime | Signal Drain, Desync, bản sao âm thanh | Resonance Blade, Aegis Medic khi đã mở |
| 4 | Nhà Máy Gãy Xương | Bombardiro Crocodilo | pháo kích, giáp dày | Resonance Blade, focus giáp dày |
| 5 | Chợ Đêm Không Ngủ | Tung Tung Tung Sahur | buff tốc độ enemy, wave phụ, knockback tuyến trước | Vanguard Breaker |
| 6 | Bệnh Viện Đen | Dottore Mozzarella | hồi máu, hồi sinh, Toxic Suppression | Resonance Blade |
| 7 | Thành Phố Méo Giọng | Ballerino Cappuccino | lao tuyến sau, né đòn, chí mạng | Vanguard Breaker |
| 8 | Đài Phát Tín Hiệu | La Torre Frequenza | Rage Lock, Ultimate Lock, Signal Drain, node phụ | Resonance Blade |
| 9 | Vùng Đỏ Trung Tâm | Chimpanzini Bananini Red Host | đổi phase, học skill nộ hero | Overdrive Titan |
| 10 | Lõi Phát Xạ | The Mother Frequency | nhiều phase, tổng hợp debuff cuối game | Overdrive Titan |

## Thông số chưa chốt ở mức production

Các bảng trên đủ để làm base combat và stage design. Tuy nhiên nếu triển khai production combat, các thông số sau vẫn cần file riêng hoặc bổ sung thêm:

- tốc độ di chuyển dạng số của từng hero/enemy
- tốc đánh hoặc chu kỳ hành động dạng giây
- tầm đánh dạng unit/pixel/meters
- HP của cổng Aegis và ổ infected/cổng brainrot theo world
- damage enemy gây lên cổng Aegis
- target priority chi tiết khi có nhiều mục tiêu
- giới hạn số unit/enemy tối đa trên sân
