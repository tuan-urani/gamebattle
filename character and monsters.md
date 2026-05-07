# Character And Monsters

## Mục tiêu tài liệu

Tài liệu này định nghĩa phe người chơi, phe phản diện, các lớp chiến binh, quái thường và boss chính của game **The Last Front of Brainrot**.

File này là nguồn chính cho toàn bộ thông tin character và monster:

- lore, vai trò, class, skill và debuff
- roster, unlock, level, stat, deploy cost
- monster, boss, công thức scale và phân bổ theo world

Trục chính:

- phe người chơi là **Quân Đoàn Aegis**, những chiến binh đã tiêm huyết thanh Aegis, cấy lõi Aegis và vượt qua Aegis Resonance
- phe phản diện là các cá thể con người đã bị brainrot hóa, mất nhận thức và bị điều khiển bởi **Tần Số Mẹ**
- mỗi world có một boss infected riêng, đại diện cho một biến thể brainrot mạnh hơn

## Phe Người Chơi: Quân Đoàn Aegis

Quân Đoàn Aegis là lực lượng phản công cuối cùng của nhân loại. Họ không chỉ là người sống sót. Họ là những người đã tiêm huyết thanh Aegis, cấy lõi Aegis và sống sót qua quá trình **Aegis Resonance**.

Quy tắc rất đơn giản:

- **Huyết thanh Aegis**: chống đồng hóa
- **Lõi Aegis**: chuyển tín hiệu brainrot thành sức mạnh
- **Aegis Resonance**: quá trình biến người sống sót thành chiến binh

Aegis biến tín hiệu brainrot thành năng lượng chiến đấu có kiểm soát:

- tăng sức mạnh thể chất
- tăng phản xạ
- tăng khả năng chịu đòn
- cho phép dùng vũ khí cộng hưởng
- giữ ý thức không bị Tần Số Mẹ chiếm lấy

## Vai trò người chơi

Người chơi là chỉ huy Quân Đoàn Aegis. Người chơi không trực tiếp ra trận, mà điều phối:

- đội hình chiến binh
- thời điểm triển khai unit
- nâng cấp hero
- chiến thuật vượt từng world để tiến tới lõi Tần Số Mẹ

Người chơi là chỉ huy Quân Đoàn Aegis, sử dụng **Aegis Energy** để triển khai các chiến binh đã sống sót qua quá trình **Aegis Resonance** ra chiến trường.

## Quy Mô Roster V0.1

Phiên bản thiết kế ban đầu dùng quy mô rõ ràng để dễ cân bằng:

| Nhóm | Số lượng | Ghi chú |
| ---- | -------: | ------- |
| Playable hero | 6 | character chiến đấu người chơi có thể dùng |
| NPC hậu phương | 2 | không trực tiếp ra trận trong V0.1 |
| Monster thường/elite | 14 | enemy spawn trong stage thường và wave phụ boss |
| Boss world | 10 | mỗi world có 1 boss riêng |
| Tổng enemy type tính cả boss | 24 | 14 monster + 10 boss |

Không thêm hero hoặc monster mới nếu chưa có vai trò gameplay riêng. Nếu chỉ cần tăng độ khó, ưu tiên tăng level, wave composition hoặc modifier của map.

## Cấp Độ Và Chỉ Số Hero

Hero có level từ **1 đến 50**.

Công thức chỉ số:

```text
Chỉ số ở level N = chỉ số level 1 + tăng mỗi level * (N - 1)
```

Các chỉ số chính:

- **HP**: máu tối đa.
- **ATK**: sát thương hoặc hiệu quả chính của hero. Với Core Engineer, ATK là hiệu quả pylon, không phải sát thương trực tiếp.
- **DEF**: giảm sát thương nhận vào.
- **Nộ/đòn**: lượng nộ nhận được từ một đòn đánh cơ bản hoặc một chu kỳ hành động.

Công thức sát thương đề xuất:

```text
Sát thương thực nhận = ATK * 100 / (100 + DEF mục tiêu)
```

### Level theo world

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

### Hero theo world

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

### Bảng chỉ số hero level 1

| Hero      | Class            | Mở khóa | HP  | ATK | DEF | Nộ/đòn | Tăng HP/level | Tăng ATK/level | Tăng DEF/level | Tăng nộ/level |
| --------- | ---------------- | ------: | --: | --: | --: | -----: | -------------: | --------------: | --------------: | ------------: |
| Kael Voss | Vanguard Breaker | World 1 | 760 |  52 |  26 |    8.5 |             65 |               4 |               2 |          0.15 |
| Mira Sane | Pulse Ranger     | World 1 | 430 |  72 |  10 |   11.0 |             34 |               6 |               1 |          0.20 |
| Riven Hal | Resonance Blade  | World 3 | 520 |  88 |  14 |   12.0 |             42 |               7 |               1 |          0.18 |
| Iris Venn | Aegis Medic      | World 5 | 460 |  38 |  12 |   13.0 |             36 |               4 |               1 |          0.25 |
| Mason Rook | Core Engineer   | World 2 | 500 |  20 |  14 |   10.0 |             38 |               3 |               1 |          0.20 |
| Atlas-09  | Overdrive Titan  | World 7 | 1050 | 140 |  34 |    7.0 |             90 |              10 |               3 |          0.10 |

### Bảng chỉ số hero level 50

| Hero       | HP   | ATK | DEF | Nộ/đòn |
| ---------- | ---: | --: | --: | -----: |
| Kael Voss  | 3945 | 248 | 124 |   15.9 |
| Mira Sane  | 2096 | 366 |  59 |   20.8 |
| Riven Hal  | 2578 | 431 |  63 |   20.8 |
| Iris Venn  | 2224 | 234 |  61 |   25.3 |
| Mason Rook | 2362 | 167 |  63 |   19.8 |
| Atlas-09   | 5460 | 630 | 181 |   11.9 |

### Deploy cost hero V0.1

| Hero | Cost Aegis Energy | Cooldown deploy | Vai trò chính |
| ---- | ----------------: | --------------: | ------------- |
| Kael Voss | 20 | 18 giây | chặn tuyến, bảo vệ cổng |
| Mira Sane | 15 | 14 giây | sát thương tầm xa, xử lý runner và support |
| Mason Rook | 30 | 24 giây | tăng kinh tế energy, trận dài |
| Riven Hal | 25 | 20 giây | xử lý elite, support, boss phụ |
| Iris Venn | 35 | 26 giây | hồi máu, giải debuff |
| Atlas-09 | 60 | 45 giây | xoay trận, phá wave lớn, đánh boss |

## Các Lớp Chiến Binh Aegis

Mỗi chiến binh Aegis chỉ có 2 loại hành động:

- **Đòn đánh cơ bản**: tự động đánh theo vai trò của class
- **Skill nộ**: đánh thường sẽ tích nộ, khi đầy nộ thì chiến binh tự động dùng skill nộ

Skill nộ có thể được nâng cấp theo bậc. Hero đạt các mốc level 15, 30 và 45 sẽ tự mở bậc skill nộ cao hơn.

Nguyên tắc nâng skill nộ:

- bậc skill nộ tự mở theo mốc level, không dùng tài nguyên riêng
- mỗi bậc skill nên tăng hiệu ứng rõ ràng
- ưu tiên tăng số mục tiêu, phạm vi, thời gian hiệu lực, số debuff được giải hoặc lượng tài nguyên tạo ra
- tránh chỉ tăng sát thương theo phần trăm nếu không tạo khác biệt trong cách chơi

### Bảng nâng cấp skill nộ

| Hero       | Bậc 1 | Bậc 2 - level 15 | Bậc 3 - level 30 | Bậc 4 - level 45 |
| ---------- | ----- | ---------------- | ---------------- | ---------------- |
| Kael Voss | Khiên cho tuyến trước gần nhất, đẩy lùi enemy gần nhất | Khiên ảnh hưởng 2 đồng minh tuyến trước | Tăng thời gian khiên và lực đẩy lùi | Khiên nhận thêm kháng debuff ngắn hạn |
| Mira Sane | Bắn xuyên một đường thẳng | Thêm một phát phụ vào enemy máu thấp | Đòn xuyên làm chậm enemy trúng đạn | Đòn xuyên gây thêm sát thương lên enemy bị giáp hoặc khiên |
| Riven Hal | Lướt chém enemy nguy hiểm nhất trong tầm | Chém thêm 1 mục tiêu gần đó | Nếu hạ mục tiêu, nhận lại một phần nộ | Ưu tiên elite hoặc boss phụ, tăng sát thương kết liễu |
| Iris Venn | Hồi mạnh 1 đồng minh nguy cấp và xóa 1 debuff | Hồi thêm 1 đồng minh nữa | Xóa tối đa 2 debuff | Đồng minh được hồi nhận kháng debuff ngắn hạn |
| Mason Rook | Tăng nhịp tạo Aegis Energy của pylon | Tạo ngay một lượng Aegis Energy khi kích hoạt | Đồng minh gần pylon tăng tốc độ tích nộ | Tăng thời gian hiệu lực và tạm tăng giới hạn Aegis Energy |
| Atlas-09 | Gây nổ diện rộng và đẩy lùi enemy | Tăng phạm vi nổ | Thêm hiệu ứng choáng ngắn lên enemy thường | Gây thêm sát thương lên elite và boss |

## Hệ Thống Debuff

Debuff là hiệu ứng xấu có thời gian tồn tại, gắn lên hero hoặc toàn đội hình Aegis.

Quy tắc chung:

- debuff có thể bị giảm thời gian bởi chỉ số kháng debuff
- Aegis Medic có thể xóa debuff bằng skill nộ
- hiệu ứng tức thời như rút nộ sẽ không có thời gian tồn tại, nhưng vẫn được tính là debuff để hệ thống objective và UI có thể theo dõi

### Debuff status v0.1

Hiện tại game có **6 debuff status chính**.

| Debuff | Tác dụng | Thời gian gốc | Stack | Nguồn gây ra |
| ------ | -------- | ------------: | ----- | ------------ |
| **Signal Drain** | giảm 40% tốc độ tích nộ | 6 giây | refresh thời gian, không cộng dồn | Static Carrier, Mute Leech, Signal Host, Tralalero Tralala Prime, La Torre Frequenza, The Mother Frequency |
| **Rage Leech** | rút ngay 15 nộ hiện có của mục tiêu | tức thời | không stack | Mute Leech |
| **Desync** | 25% khả năng đánh hụt đòn đánh cơ bản | 5 giây | refresh thời gian, không cộng dồn | Scream Spitter, Tralalero Tralala Prime, The Mother Frequency |
| **Rage Lock** | không thể tích thêm nộ | 4 giây | refresh thời gian, không cộng dồn | La Torre Frequenza, The Mother Frequency |
| **Ultimate Lock** | có đủ nộ nhưng không thể dùng skill nộ | 4 giây | refresh thời gian, không cộng dồn | La Torre Frequenza, The Mother Frequency |
| **Toxic Suppression** | giảm 50% hồi máu nhận vào và mất 2% HP tối đa mỗi giây | 6 giây | refresh thời gian, không cộng dồn | Dottore Mozzarella |

### Nguồn debuff theo enemy

| Enemy/Boss | Debuff gây ra | Ghi chú |
| ---------- | ------------- | ------- |
| Static Carrier | Signal Drain | kích hoạt khi chết, phạm vi nhỏ quanh điểm nổ |
| Scream Spitter | Desync | đòn bắn sóng âm có cơ hội gây lạc nhịp |
| Mute Leech | Rage Leech, Signal Drain | chuyên khắc chế hero phụ thuộc skill nộ |
| Signal Host | Signal Drain | phát nhiễu theo chu kỳ, phạm vi rộng hoặc toàn map tùy stage |
| Tralalero Tralala Prime | Signal Drain, Desync | boss World 3, trọng tâm là rối nhịp và làm chậm nộ |
| Dottore Mozzarella | Toxic Suppression | boss World 6, giảm hiệu quả hồi máu của người chơi |
| La Torre Frequenza | Rage Lock, Ultimate Lock, Signal Drain | boss World 8, khóa nhịp nộ và skill nộ |
| The Mother Frequency | Signal Drain, Desync, Rage Lock, Ultimate Lock | boss cuối, dùng lại các debuff trọng yếu của game |

### Hiệu ứng xấu không tính là debuff status

Các hiệu ứng dưới đây vẫn gây bất lợi, nhưng không bị xóa bởi skill giải debuff thông thường.

| Hiệu ứng | Tác dụng | Nguồn gây ra | Cách khắc chế |
| -------- | -------- | ------------ | ------------- |
| **Knockback** | đẩy lùi tuyến trước, làm đội hình mất vị trí | Tung Tung Tung Sahur | dùng tanker cứng, khiên, kháng đẩy lùi |
| **Backline Dive** | áp sát hoặc tấn công hero tuyến sau | Phase Stalker, Ballerino Cappuccino | giữ tanker đúng vị trí, dùng unit chặn đường, ưu tiên focus sát thủ |
| **Enemy Haste** | tăng tốc độ di chuyển hoặc tấn công cho enemy | Bone Drummer, Tung Tung Tung Sahur | hạ enemy buff trước, dùng làm chậm hoặc sát thương diện rộng |
| **Enemy Regrowth** | hồi máu hoặc tái kích hoạt enemy | Regrowth Host, Dottore Mozzarella | dùng burst damage, phá hồi máu, ưu tiên giết support |

### Vanguard Breaker

Vai trò: tanker tuyến đầu.

Đặc điểm:

- máu cao
- giáp cao
- tốc độ chậm
- dùng khiên cộng hưởng để chặn wave infected

Đòn đánh cơ bản:

- đánh cận chiến bằng khiên hoặc búa cộng hưởng

Skill nộ:

- **Resonance Guard**: dựng lá chắn lớn, giảm sát thương cho tuyến trước và đẩy lùi enemy gần nhất

### Pulse Ranger

Vai trò: xạ thủ tầm xa.

Đặc điểm:

- sát thương ổn định
- bắn từ tuyến sau
- khắc chế quái bay, quái hỗ trợ và quái phát nhịp

Đòn đánh cơ bản:

- bắn một mục tiêu từ xa bằng súng lọc âm

Skill nộ:

- **Noise Piercer**: bắn một phát xuyên hàng, gây sát thương nhiều enemy trên cùng đường đạn

### Resonance Blade

Vai trò: sát thủ cận chiến.

Đặc điểm:

- tốc độ cao
- sát thương mạnh vào mục tiêu đơn
- dễ chết nếu không có tanker giữ tuyến

Đòn đánh cơ bản:

- chém nhanh mục tiêu gần nhất bằng kiếm nghịch pha

Skill nộ:

- **Phase Slash**: lướt tới enemy nguy hiểm nhất trong tầm và chém một chuỗi sát thương cao

### Aegis Medic

Vai trò: hồi phục và hỗ trợ đội hình.

Đặc điểm:

- không gây nhiều sát thương
- giữ đội hình sống lâu hơn
- giải debuff và giữ nhịp đội hình

Đòn đánh cơ bản:

- bắn xung hồi phục vào đồng minh thấp máu nhất

Skill nộ:

- **Emergency Sync**: hồi máu mạnh cho đồng minh nguy cấp nhất và xóa một debuff brainrot

### Core Engineer

Vai trò: hậu phương tạo năng lượng.

Đặc điểm:

- không tấn công
- mang cột năng lượng gắn liền với bản thân
- Core Engineer và cột đều tạo Aegis Energy theo chu kỳ
- khi Core Engineer bị hạ, cột cũng biến mất

Đòn đánh cơ bản:

- không có, chỉ duy trì cột năng lượng

Skill nộ:

- **Resonance Pylon**: kích hoạt cột năng lượng, tăng nhịp tạo Aegis Energy trong thời gian ngắn

### Overdrive Titan

Vai trò: unit hạng nặng, giá cao, cooldown lâu.

Đặc điểm:

- sức mạnh ngang mini-boss
- sát thương diện rộng
- chịu đòn cực tốt

Đòn đánh cơ bản:

- đấm hoặc quét cận chiến, gây sát thương diện nhỏ trước mặt

Skill nộ:

- **Aegis Burst**: phát nổ xung cộng hưởng diện rộng, gây sát thương lớn và đẩy lùi enemy

## Hero Chính Gợi Ý

### Kael Voss - Vanguard Breaker

Vai trò truyện: cựu đội trưởng phòng thủ tại trại sơ tán đầu tiên.

Tính cách:

- lạnh
- kỷ luật
- luôn nhận phần nguy hiểm nhất

Lối chơi:

- tanker mở đầu game
- giữ tuyến tốt
- phù hợp cho người chơi mới

### Mira Sane - Pulse Ranger

Vai trò truyện: cựu kỹ thuật viên tín hiệu, người đầu tiên phát hiện nhịp nhiễm của Tần Số Mẹ.

Tính cách:

- tập trung
- ít nói
- rất ghét âm thanh brainrot

Lối chơi:

- bắn tầm xa
- làm chậm enemy
- mạnh khi đi cùng tanker

### Riven Hal - Resonance Blade

Vai trò truyện: chiến binh Aegis có chỉ số cộng hưởng cao bất thường.

Tính cách:

- liều lĩnh
- thích áp sát boss
- hay vượt lệnh nếu thấy cơ hội kết liễu

Lối chơi:

- sát thương đơn mục tiêu cao
- chuyên giết boss phụ và enemy hỗ trợ

### Iris Venn - Aegis Medic

Vai trò truyện: y sĩ chiến trường của Quân Đoàn Aegis.

Tính cách:

- tỉnh táo
- bình tĩnh dưới áp lực
- ưu tiên cứu đồng đội hơn truy đuổi kill

Lối chơi:

- hồi phục
- giải debuff
- giữ đội hình sống lâu hơn trong các trận dài

### Mason Rook - Core Engineer

Vai trò truyện: kỹ sư chiến trường chuyên đi cùng đội hình Aegis.

Tính cách:

- thực dụng
- nói ít làm nhiều
- tin rằng mọi trận chiến đều thắng bằng chuẩn bị tốt

Lối chơi:

- dựng trụ
- đặt bẫy
- tăng khả năng thủ cổng

### Atlas-09 - Overdrive Titan

Vai trò truyện: người đầu tiên sống sót sau liều Aegis Overdrive.

Tính cách:

- trầm
- trí nhớ bị rạn
- luôn nghe thấy tiếng Tần Số Mẹ nhưng vẫn chống lại nó

Lối chơi:

- unit hạng nặng
- dùng để xoay trận
- mạnh nhưng tốn tài nguyên

## NPC Hậu Phương: Đội Nghiên Cứu Kháng Não

Đội Nghiên Cứu Kháng Não không phải đơn vị chiến đấu. Họ là nhóm NPC hậu phương, phụ trách nâng cấp hero, nghiên cứu Aegis và phân tích dữ liệu sau mỗi world. Người chơi không triển khai họ ra trận, nhưng mọi sức mạnh của Quân Đoàn Aegis đều được duy trì nhờ họ.

### Dr. Lena Oris

Vai trò trong game:

- NPC chính ở Research Lab
- phụ trách hero level và nâng cấp skill nộ
- giải thích lore về Aegis Resonance, Tần Số Mẹ và khả năng hoàn nguyên infected
- xuất hiện trong báo cáo sau mỗi world boss

Tính cách:

- tỉnh táo
- mang mặc cảm vì công nghệ được tạo ra quá muộn
- xem mỗi infected là một bệnh nhân chưa cứu được

### Bruno Vale

Vai trò trong game:

- NPC kỹ thuật hậu phương
- phụ trách bẫy, công sự, blueprint và phân tích chiến trường
- giải thích các unlock kỹ thuật sau mỗi world
- đại diện cho phần thực dụng của căn cứ Aegis

Tính cách:

- thực dụng
- nói ít làm nhiều
- tin rằng mọi trận chiến đều thắng bằng chuẩn bị tốt

## Phe Phản Diện: Đàn Nhiễm Brainrot

Phe phản diện không phải một đội quân bình thường. Họ là những con người đã bị brainrot hóa, mất nhận thức và bị Tần Số Mẹ biến thành các hình thái quái dị.

Điểm quan trọng:

- enemy từng là con người
- phần lớn không còn ý thức
- chúng không ác theo nghĩa thông thường
- Tần Số Mẹ dùng chúng như cơ thể mở rộng của chính nó

## Cấu Trúc Phe Phản Diện

Quái thường chỉ có đòn đánh cơ bản, không có thanh nộ và không dùng skill.

Monster thường và elite dùng level để scale chỉ số. Vì vậy cùng một enemy như **Twitch Runner** ở World 1 và World 2 sẽ không có chỉ số giống nhau.

### Cấp độ monster

Monster level đi theo stage:

```text
Monster level stage thường = (world - 1) * 5 + ceil(stage / 2)
Monster level boss stage = world * 5
```

Ví dụ:

- World 1 Stage 1-2: monster level 1
- World 1 Stage 9-10: monster level 5
- World 2 Stage 1-2: monster level 6
- World 10 boss: monster level 50

### Công thức scale monster thường và elite

```text
HP  = HP level 1  * (1 + 0.09 * (monster level - 1))
ATK = ATK level 1 * (1 + 0.08 * (monster level - 1))
DEF = DEF level 1 * (1 + 0.07 * (monster level - 1))
```

Làm tròn số sau khi tính.

Ví dụ **Twitch Runner**:

| Vị trí              | Level | HP | ATK | DEF |
| ------------------- | ----: | -: | --: | --: |
| World 1 Stage 3-4   |     2 | 104 |  26 |   2 |
| World 2 Stage 1-2   |     6 | 138 |  34 |   3 |
| World 5 Stage 9-10  |    25 | 300 |  70 |   5 |

### Bảng chỉ số monster level 1

| Monster          | Loại | HP | ATK | DEF | Vai trò |
| ---------------- | ---- | -: | --: | --: | ------- |
| Blank Walker     | thường | 140 | 18 |  4 | đông, chậm, ép tuyến |
| Twitch Runner    | thường |  95 | 24 |  2 | chạy nhanh, xuyên tuyến |
| Jaw Crawler      | thường | 115 | 21 |  3 | bò thấp, khó bị một số unit bắn trúng |
| Static Carrier   | thường | 180 | 28 |  5 | chết phát nổ nhiễu nhỏ |
| Meat Shield Host | elite | 420 | 34 | 16 | tanker che chắn đàn |
| Scream Spitter   | elite | 160 | 30 |  3 | bắn xa vào tuyến trước |
| Bone Drummer     | elite | 220 | 22 |  6 | buff tốc đánh hoặc tốc chạy cho enemy gần đó |
| Mute Leech       | elite | 190 | 20 |  5 | gây Rage Leech và Signal Drain |
| Patch Beast      | elite | 560 | 55 | 18 | chậm, rất trâu, đánh đau |
| Regrowth Host    | elite | 250 | 18 |  8 | hồi máu hoặc tái kích hoạt enemy |
| Phase Stalker    | elite | 260 | 65 |  7 | áp sát tuyến sau |
| Signal Host      | elite | 300 | 28 | 10 | phát Signal Drain diện rộng |
| Red Host         | elite | 480 | 70 | 14 | tiến hóa trong trận |
| Core Guardian    | elite | 900 | 95 | 25 | bảo vệ lõi, xuất hiện cuối game |

### Monster behavior summary

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

### Monster theo world/map

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

### 1. Đàn Nhiễm Cơ Bản

Là những người mới biến dạng hoặc biến dạng chưa hoàn chỉnh. Chúng tạo thành wave đông, ép người chơi phải giữ tuyến.

Loại thường gặp:

- **Blank Walker**
  - Di chuyển: đi bộ chậm
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: vung tay đập thẳng vào mục tiêu gần nhất

- **Twitch Runner**
  - Di chuyển: chạy nhanh
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: lao tới cào nhanh mục tiêu tuyến trước

- **Jaw Crawler**
  - Di chuyển: bò sát mặt đất
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: cắn vào chân mục tiêu gần nhất

- **Static Carrier**
  - Di chuyển: đi bộ chậm
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: đập mạnh bằng thân thể vào mục tiêu trước mặt
  - Debuff: khi chết phát nổ sóng nhiễu nhỏ, gây **Signal Drain** trong phạm vi gần

### 2. Dị Thể Chiến Đấu

Là infected đã phát triển chức năng chiến đấu rõ ràng.

Loại thường gặp:

- **Meat Shield Host**
  - Di chuyển: đi bộ chậm
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: húc vai hoặc đấm nặng vào mục tiêu trước mặt

- **Scream Spitter**
  - Di chuyển: đi bộ chậm
  - Tầm đánh: tầm xa
  - Đòn đánh cơ bản: bắn một luồng sóng âm vào tuyến trước
  - Debuff: có cơ hội gây **Desync**

- **Bone Drummer**
  - Di chuyển: đi bộ vừa
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: đập tay trống vào mục tiêu gần nhất

- **Mute Leech**
  - Di chuyển: đi bộ vừa
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: bám và cắn mục tiêu gần nhất
  - Debuff: gây **Rage Leech** và **Signal Drain**

- **Patch Beast**
  - Di chuyển: đi bộ chậm
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: quét tay nặng, gây sát thương cao lên mục tiêu trước mặt

- **Regrowth Host**
  - Di chuyển: đi bộ chậm
  - Tầm đánh: hỗ trợ tầm trung
  - Đòn đánh cơ bản: phát xung tái sinh, hồi máu nhẹ cho enemy thấp máu nhất gần đó

- **Phase Stalker**
  - Di chuyển: chạy nhanh, có pha lướt ngắn
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: lướt cắt vào mục tiêu tuyến sau nếu có khoảng trống

- **Signal Host**
  - Di chuyển: đi bộ vừa
  - Tầm đánh: hỗ trợ toàn bản đồ theo chu kỳ
  - Đòn đánh cơ bản: phát nhiễu làm chậm tốc độ tích nộ của hero trong thời gian ngắn
  - Debuff: gây **Signal Drain**

- **Red Host**
  - Di chuyển: đi bộ nhanh
  - Tầm đánh: cận chiến
  - Đòn đánh cơ bản: cào liên tục, tự tăng ATK nếu sống quá lâu

- **Core Guardian**
  - Di chuyển: đi bộ chậm
  - Tầm đánh: cận chiến diện rộng
  - Đòn đánh cơ bản: đập lõi gây sát thương diện nhỏ trước mặt

### 3. Cá Thể Brainrot Hóa

Đây là các biến thể đặc biệt được Tần Số Mẹ giữ lại và nuôi lớn. Chúng vẫn mang dấu vết danh tính cũ, nhưng bị bóp méo thành hình tượng brainrot.

Các cá thể này thường là:

- mini-boss
- boss world
- enemy elite xuất hiện ở màn cuối của mỗi world

### 4. Tần Số Mẹ

Tần Số Mẹ là lõi ý chí của đại dịch. Nó không cần tự di chuyển. Nó điều khiển infected qua nhịp, hình ảnh và tần số thần kinh.

Tần Số Mẹ có ba mục tiêu:

- giữ infected không hoàn nguyên thành người
- bảo vệ lõi phát xạ trung tâm khỏi bị phá
- mở rộng vùng phát xạ để đồng hóa những nhóm người sống sót còn lại

## Boss Theo World

Boss có **Boss Level** riêng bằng `world * 5`.

Công thức cơ sở:

```text
Boss HP  = HP gốc  * (1 + 0.12 * (boss level - 1))
Boss ATK = ATK gốc * (1 + 0.09 * (boss level - 1))
Boss DEF = DEF gốc * (1 + 0.08 * (boss level - 1))
```

Làm tròn số sau khi tính.

### Bảng chỉ số boss gốc

| Boss | World | Boss Level | HP gốc | ATK gốc | DEF gốc | Vai trò |
| ---- | ----: | ---------: | -----: | ------: | ------: | ------- |
| Patient Zero Escort | 1 | 5 | 1800 | 42 | 10 | nhiều hộ vệ, dạy focus target |
| Trippo Motorico | 2 | 10 | 2400 | 58 | 12 | boss lao nhanh, gây thủng tuyến |
| Tralalero Tralala Prime | 3 | 15 | 2900 | 64 | 15 | Signal Drain, Desync |
| Bombardiro Crocodilo | 4 | 20 | 4200 | 78 | 24 | pháo kích, giáp dày |
| Tung Tung Tung Sahur | 5 | 25 | 4000 | 72 | 20 | buff wave, tạo áp lực liên tục |
| Dottore Mozzarella | 6 | 30 | 4600 | 68 | 22 | hồi máu, hồi sinh, Toxic Suppression |
| Ballerino Cappuccino | 7 | 35 | 4300 | 88 | 18 | lao vào tuyến sau, chí mạng |
| La Torre Frequenza | 8 | 40 | 5600 | 92 | 28 | Rage Lock, Ultimate Lock, node phụ |
| Chimpanzini Bananini Red Host | 9 | 45 | 6200 | 106 | 30 | học skill nộ, scale theo thời gian |
| The Mother Frequency | 10 | 50 | 8500 | 120 | 36 | boss cuối nhiều phase |

### Boss stat sau scale

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

### Boss theo world/map

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

### World 1: Patient Zero Escort

- Đòn đánh thường: cào hoặc đập cận chiến vào tuyến trước
- Skill nộ: triệu hồi Blank Walker, tự hồi máu nhẹ khi còn hộ vệ
- Khắc chế bởi hero: Pulse Ranger

### World 2: Trippo Motorico

- Đòn đánh thường: lao thẳng cận chiến vào mục tiêu trước mặt
- Skill nộ: tăng tốc lao liên tục, kéo theo Twitch Runner
- Khắc chế bởi hero: Vanguard Breaker

### World 3: Tralalero Tralala Prime

- Đòn đánh thường: phát xung âm tầm xa gây sát thương tuyến trước
- Skill nộ: gây **Signal Drain**, gây **Desync** khiến unit bắn trượt, tạo bản sao âm thanh
- Khắc chế bởi hero: Resonance Blade

### World 4: Bombardiro Crocodilo

- Đòn đánh thường: bắn đạn hữu cơ vào tuyến trước hoặc tuyến sau
- Skill nộ: dồn pháo kích tuyến sau, kích hoạt giáp dày trong thời gian ngắn
- Khắc chế bởi hero: Resonance Blade

### World 5: Tung Tung Tung Sahur

- Đòn đánh thường: đập trống cận chiến vào mục tiêu gần nhất
- Skill nộ: tăng tốc toàn bộ enemy, gọi wave phụ, tạo xung đẩy lùi tuyến trước
- Khắc chế bởi hero: Vanguard Breaker

### World 6: Dottore Mozzarella

- Đòn đánh thường: quật cận chiến bằng tay tái sinh
- Skill nộ: hồi máu cho enemy, hồi sinh quái đã chết, tạo vùng độc gây **Toxic Suppression**
- Khắc chế bởi hero: Resonance Blade

### World 7: Ballerino Cappuccino

- Đòn đánh thường: lao cắt nhanh vào tuyến sau
- Skill nộ: né đòn liên tục và tung chuỗi đánh chí mạng vào hero yếu máu
- Khắc chế bởi hero: Vanguard Breaker

### World 8: La Torre Frequenza

- Đòn đánh thường: quật dây cáp tầm xa vào tuyến trước
- Skill nộ: buff toàn bản đồ, gây **Rage Lock**, **Ultimate Lock** và **Signal Drain**, kích hoạt bảo vệ node phụ
- Khắc chế bởi hero: Resonance Blade

### World 9: Chimpanzini Bananini Red Host

- Đòn đánh thường: cào cận chiến tốc độ cao
- Skill nộ: đổi phase theo máu, học một phần skill nộ hero kích hoạt nhiều nhất
- Khắc chế bởi hero: Overdrive Titan

### World 10: The Mother Frequency

- Đòn đánh thường: xung nghịch pha quét diện rộng quanh lõi
- Skill nộ: chuyển phase theo thứ tự The Choir of Tralala, Bombardiro Rex, Mother Frequency Core; phase The Choir dùng **Signal Drain**, **Desync**, **Rage Lock** và **Ultimate Lock**
- Khắc chế bởi hero: Overdrive Titan

## Quy Tắc Thiết Kế Boss

- Mỗi boss phải đại diện cho một cơ chế riêng.
- Boss không chỉ nhiều máu hơn quái thường, mà phải buộc người chơi đổi chiến thuật.
- Boss nên có dấu vết con người cũ để tăng cảm giác bi kịch.
- Khi boss bị đánh bại, nên có một khoảnh khắc ngắn cho thấy họ từng là người.
- Boss càng gần lõi mẹ thì càng ít giống người và càng giống một phần của Tần Số Mẹ.
