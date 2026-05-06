# Chế Độ Nâng Cấp Hero Và Item

## Mục tiêu thiết kế

Hệ nâng cấp hero tập trung vào hai phần:

- **Hero level**: tăng trực tiếp chỉ số nền để người chơi thấy hero mạnh lên rõ ràng sau mỗi cấp.
- **Skill nộ**: chỉ được mở quyền nâng cấp ở các mốc level nhất định, giúp hero có bước nhảy sức mạnh theo giai đoạn.

## Vai trò NPC hậu phương

Đội Nghiên Cứu Kháng Não là nhóm NPC hậu phương phụ trách nâng cấp hero và phân tích dữ liệu sau mỗi world.

Trong UI nâng cấp:

- **Dr. Lena Oris** phụ trách hero level và nâng cấp skill nộ

## Nâng cấp hero

### Thuộc tính hero

Mỗi hero chỉ có các chỉ số:

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

Nguồn EXP:

- hoàn thành stage của world
- thưởng lớn khi hạ boss stage
- chơi lại stage để farm EXP cơ bản, có giới hạn bằng stamina để tránh farm vô hạn

EXP không tự động cộng thẳng vào hero sau trận. Khi thắng stage, EXP được đưa vào **kho EXP tướng** của người chơi. Người chơi vào kho tướng, chọn hero muốn nâng, rồi dùng EXP trong kho để nâng level cho hero đó.

### Mục tiêu level theo world

Để tránh người chơi bị out trình hoặc vượt quá xa độ khó, mỗi world có một mốc level khuyến nghị:

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

### EXP cần để lên cấp

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

### Tổng EXP mốc quan trọng

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

### EXP nhận từ stage

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

Ví dụ:

| Stage | First Clear EXP | Repeat Clear EXP |
| ----- | --------------: | ---------------: |
| World 1 Stage 1 | 80 | 45 |
| World 1 Stage 10 | 125 | 63 |
| World 2 Stage 1 | 95 | 53 |
| World 5 Stage 5 | 160 | 85 |
| World 10 Stage 10 | 260 | 135 |
| World 1 Boss | 290 | 140 |
| World 5 Boss | 450 | 220 |
| World 10 Boss | 650 | 320 |

### Cơ chế farm EXP

Farm EXP diễn ra bằng cách replay stage đã clear. Không phải map nào cũng cho hiệu quả như nhau.

Quy tắc farm:

- stage thường là nguồn farm chính
- boss cho nhiều EXP nhưng tốn thời gian hơn, không phải nơi farm hiệu quả nhất theo stamina
- stage càng cao trong world thì EXP càng tốt
- replay stage vẫn tiêu tốn stamina như bình thường
- chỉ khi thắng stage mới nhận EXP
- thua hoặc thoát giữa chừng không nhận EXP để tránh lạm dụng
- EXP thắng trận đi vào kho EXP tướng
- người chơi tự quyết định dùng EXP đó cho hero nào

Khuyến nghị cho người chơi:

- nếu đang thiếu ít EXP để chạm mốc skill level 10, 15, 20: farm stage 8 đến 10 của world hiện tại
- nếu vừa mở world mới nhưng bị hụt sức mạnh: quay lại stage 9, 10 và boss của world trước
- nếu muốn lên nhanh hero mới mở khóa: farm EXP bằng đội hình mạnh, sau đó vào kho tướng để dùng EXP nâng hero mới

### Kho EXP tướng

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

### Tăng chỉ số mỗi lần lên cấp

Mỗi lần lên level, hero tăng chỉ số theo bảng tăng trưởng cố định của class.

Ví dụ:

- Kael từ level 1 lên 2: `+65 HP`, `+4 ATK`, `+2 DEF`, `+0.15 nộ/đòn`
- Mira từ level 1 lên 2: `+34 HP`, `+6 ATK`, `+1 DEF`, `+0.20 nộ/đòn`
- Iris từ level 1 lên 2: `+36 HP`, `+4 ATK`, `+1 DEF`, `+0.25 nộ/đòn`

Tăng trưởng này nên giữ cố định để người chơi dễ hiểu và đội dev dễ cân bằng.

### Nâng cấp skill nộ

Skill nộ không tăng theo từng level. Hero cần đạt các mốc level nhất định để mở quyền nâng cấp skill nộ.

Mốc đề xuất:

- level 10: mở nâng skill nộ lên bậc 2
- level 15: mở nâng skill nộ lên bậc 3
- level 20: mở nâng skill nộ lên bậc 4

Khi đạt mốc level, người chơi vẫn cần chủ động nâng skill trong UI nâng cấp. Level chỉ là điều kiện mở khóa, không tự động nâng skill.

Mỗi bậc skill nộ nên tăng hiệu ứng rõ ràng, không chỉ tăng sát thương theo phần trăm.

Ví dụ hướng nâng:

- skill đánh 1 mục tiêu có thể nâng thành đánh 2 mục tiêu
- skill hồi máu 1 đồng minh có thể nâng thành hồi 2 đồng minh
- skill tạo khiên có thể tăng thêm phạm vi hoặc thời gian tồn tại
- skill giải debuff có thể giải thêm số lượng debuff hoặc thêm kháng debuff ngắn hạn
- skill tạo Aegis Energy có thể tăng lượng energy hoặc tăng thời gian hiệu lực

### Giới hạn hệ progression

Game không dùng thêm một hệ tăng bậc riêng cho hero ngoài level và skill nộ.

Sức mạnh hero đến từ:

- level
- chỉ số nền tăng theo level
- nâng cấp skill nộ tại các mốc level
- item và lõi Aegis hỗ trợ build

## Hệ item cho hero

Item không dùng chung mơ hồ ở cấp đội hình. Mỗi hero mang bộ item riêng của chính mình.

Mỗi hero có **3 slot item**:

- **Weapon Module**: tăng sức mạnh vai trò chính của hero
- **Armor Module**: tăng sống sót hoặc kháng hiệu ứng
- **Tactical Chip**: thêm utility, năng lượng hoặc hiệu ứng chiến thuật

Ví dụ theo class:

- Vanguard Breaker: khiên cộng hưởng, giáp nặng, chip giữ tuyến
- Pulse Ranger: súng lọc âm, giáp nhẹ, chip xuyên giáp
- Resonance Blade: kiếm nghịch pha, giáp cơ động, chip kết liễu
- Aegis Medic: bộ khuếch đại hồi phục, áo kháng nhiễu, chip thanh tẩy
- Core Engineer: pylon core, áo kỹ sư, chip tối ưu năng lượng
- Overdrive Titan: lõi overdrive, giáp titan, chip bùng nổ

## Nhóm item chính

Item chia thành các nhóm:

- **ATK item**: tăng sát thương, xuyên giáp, sát thương boss
- **DEF item**: tăng HP, DEF, giảm sát thương nhận vào
- **Utility item**: tăng tốc độ tích nộ, kháng debuff, hồi năng lượng
- **Energy item**: tăng Aegis Energy đầu trận, giới hạn energy, hoàn energy
- **Set item**: kích hoạt bonus khi trang bị đủ số món

## Độ hiếm item

Đề xuất độ hiếm:

- Common
- Rare
- Epic
- Legendary

Item rarity chủ yếu tăng:

- chỉ số cộng thêm
- số dòng phụ
- chất lượng hiệu ứng đặc biệt

## Quy tắc trang bị item

- mỗi hero chỉ trang bị item của chính mình
- item có thể tháo lắp tự do ngoài trận
- một số item có thể dùng chung nhiều class
- một số item khóa theo class để tránh build phá cân bằng

## Ví dụ item theo hero

| Hero | Weapon Module | Armor Module | Tactical Chip |
| ---- | ------------- | ------------ | ------------- |
| Kael Voss | Bastion Hammer | Frontline Plating | Hold the Line Chip |
| Mira Sane | Noise Rail Rifle | Light Resonance Suit | Weakpoint Scope |
| Riven Hal | Phase Fang Blade | Kinetic Weave | Execute Protocol Chip |
| Iris Venn | Medical Pulse Staff | Sterile Guard Coat | Emergency Cleanse Chip |
| Mason Rook | Resonance Pylon Core | Engineer Field Vest | Grid Amplifier Chip |
| Atlas-09 | Overdrive Reactor Fist | Titan Shell Armor | Cataclysm Trigger Chip |

## Nâng cấp item

Item có level riêng, tách khỏi hero level.

Đề xuất:

| Rarity | Max item level | Số dòng phụ |
| ------ | -------------: | ----------: |
| Common | 10 | 1 |
| Rare | 15 | 2 |
| Epic | 20 | 3 |
| Legendary | 25 | 4 |

Mỗi lần nâng item:

- tăng chỉ số chính của item
- có thể tăng nhẹ chỉ số phụ ở một số mốc
- không mở skill mới cho hero

Vật liệu nâng item đến từ:

- stage thường
- boss world
- shop của Bruno Vale

## Ví dụ hiệu ứng item

- **Starter Capacitor**: hero bắt đầu trận giúp đội có thêm Aegis Energy.
- **Resonance Battery**: tăng giới hạn Aegis Energy tối đa.
- **Kill Converter Chip**: giết đủ số enemy sẽ tạo thêm Aegis Energy.
- **Perfect Hold Badge**: nếu cổng Aegis không mất máu trong đầu trận, nhận thêm Aegis Energy.
- **Anti-Debuff Insulator**: giảm thời gian bị Signal Drain hoặc Desync.
- **Armor Break Lens**: đòn đánh có cơ hội giảm DEF của enemy giáp dày.
- **Medic Relay Core**: tăng hiệu quả hồi máu và tốc độ tích nộ của Aegis Medic.

## Quy tắc cân bằng

- Hero level tạo sức mạnh nền.
- Skill nộ tạo bước nhảy sức mạnh theo mốc level.
- Tránh chồng quá nhiều hệ progression lên cùng một nhân vật.
