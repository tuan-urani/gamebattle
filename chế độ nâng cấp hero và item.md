# Chế Độ Nâng Cấp Hero Và Item

## Mục tiêu thiết kế
Hệ nâng cấp cần tạo cảm giác:
- hero mạnh lên rõ ràng
- item có giá trị sưu tầm
- người chơi có lý do quay lại farm mỗi ngày
- mỗi lớp chiến binh Aegis có hướng build riêng

## Vai trò NPC hậu phương
Đội Nghiên Cứu Kháng Não không phải đơn vị chiến đấu. Họ là nhóm NPC hậu phương, phụ trách shop, nâng cấp hero, nâng cấp item, nghiên cứu Aegis và phân tích dữ liệu sau mỗi world. Người chơi không triển khai họ ra trận, nhưng mọi sức mạnh của Quân Đoàn Aegis đều được duy trì nhờ họ.

Trong UI nâng cấp:
- **Dr. Lena Oris** phụ trách hero upgrade, Aegis Core và nghiên cứu kháng não
- **Bruno Vale** phụ trách item upgrade, shop, vũ khí, giáp, bẫy và blueprint

## Nâng cấp hero

### 1. Level
Level tăng chỉ số cơ bản.

Chỉ số tăng theo level:
- HP
- ATK
- DEF
- tốc độ tích nộ
- hiệu quả chiến đấu tổng thể

Nguồn EXP:
- clear stage
- dùng Hero EXP Chip
- nhiệm vụ ngày
- Supply Run

### 2. Star
Star thể hiện cấp tiến hóa của hero.

Quy tắc đề xuất:
- hero bắt đầu từ 1 đến 3 sao tùy độ hiếm
- tối đa 6 sao
- cần mảnh hero để tăng sao

Tác dụng:
- tăng mạnh chỉ số nền
- tăng sức mạnh đòn đánh cơ bản và skill nộ
- nâng giới hạn level

Ví dụ:
- 1 sao: level tối đa 20
- 2 sao: level tối đa 40
- 3 sao: level tối đa 60
- 4 sao: level tối đa 80
- 5 sao: level tối đa 100
- 6 sao: mở Awakening

### 3. Skill
Mỗi hero có:
- 1 đòn đánh thường
- 1 skill nộ tự động

Nâng skill cần:
- coin
- Skill Manual
- Aegis Core Fragment

Skill nộ tự kích hoạt khi thanh nộ đầy. Người chơi không bấm skill thủ công.

Nâng skill nên thay đổi rõ, không chỉ tăng phần trăm nhỏ.

Ví dụ:
- level 1: bắn 1 mục tiêu
- level 3: bắn xuyên 2 mục tiêu
- level 5: thêm hiệu ứng Desync
- level 7: giảm lượng nộ cần để kích hoạt

### 4. Aegis Core
Aegis Core là lõi riêng của từng hero.

Chỉ số có thể nâng:
- Core Stability: tăng độ ổn định sức mạnh
- Resonance Output: tăng sát thương hoặc hồi phục
- Signal Resistance: kháng debuff brainrot
- Rage Output: tăng tốc độ tích nộ hoặc hiệu quả skill nộ

Core có thể chia theo loại:
- **Guard Core**: hợp tanker
- **Pulse Core**: hợp xạ thủ
- **Blade Core**: hợp sát thủ
- **Medic Core**: hợp healer
- **Engineer Core**: hợp công sự
- **Titan Core**: hợp unit hạng nặng

### 5. Awakening
Awakening là nâng cấp cuối của hero, mở khi đạt:
- 6 sao
- level tối đa
- skill nộ đạt mốc yêu cầu
- hoàn thành nhiệm vụ cá nhân hoặc boss challenge

Tác dụng:
- đổi ngoại hình
- nâng cấp hiệu ứng đòn đánh cơ bản
- nâng cấp hiệu ứng skill nộ
- có thể thêm voice line hoặc cutscene ngắn

## Nâng cấp item

## Loại item
Mỗi hero có thể trang bị:
- Weapon
- Armor
- Core Module
- Accessory
- Tactical Chip

### Weapon
Tăng sát thương.

Ví dụ:
- kiếm nghịch pha
- súng lọc âm
- pháo Aegis
- găng cộng hưởng

### Armor
Tăng sống sót.

Ví dụ:
- giáp phản xung
- áo chống nhiễu
- khung ổn định cơ bắp

### Core Module
Tăng hiệu suất lõi Aegis.

Ví dụ:
- tăng tốc độ tích nộ
- tăng hồi năng lượng
- tăng độ ổn định kỹ năng
- tăng giới hạn Aegis Energy
- nhận Aegis Energy khi phá phase boss

### Accessory
Item phụ tạo hiệu ứng đặc biệt.

Ví dụ:
- vòng lọc âm
- mặt nạ chống brainrot
- pin cộng hưởng dự phòng
- tụ năng lượng khởi trận
- huy hiệu giữ cổng

### Tactical Chip
Chip chiến thuật thay đổi lối chơi.

Ví dụ:
- tăng sát thương lên boss
- tăng sát thương lên infected tốc độ cao
- hồi máu khi giết enemy
- tăng coin sau trận
- nhận Aegis Energy theo số enemy bị tiêu diệt
- hoàn lại một phần chi phí khi triển khai unit giá cao

## Item tạo Aegis Energy

Các item này dùng cho build thiên về triển khai unit nhanh, giữ tempo hoặc gọi unit đắt sớm hơn.

### Starter Capacitor
Slot: Accessory.

Hiệu ứng:
- bắt đầu trận với thêm Aegis Energy
- phù hợp stage có wave đầu mạnh

### Resonance Battery
Slot: Core Module.

Hiệu ứng:
- tăng giới hạn Aegis Energy tối đa
- phù hợp đội hình dùng nhiều unit đắt

### Kill Converter Chip
Slot: Tactical Chip.

Hiệu ứng:
- sau mỗi số lượng enemy bị tiêu diệt, nhận thêm Aegis Energy
- phù hợp stage wave đông

### Boss Siphon Module
Slot: Core Module.

Hiệu ứng:
- gây mất một mốc máu boss sẽ nhận Aegis Energy
- phù hợp boss stage và boss rush

### Perfect Hold Badge
Slot: Accessory.

Hiệu ứng:
- nếu cổng Aegis không mất máu trong một khoảng thời gian đầu trận, nhận Aegis Energy
- phù hợp đội hình phòng thủ chắc

### Heavy Deploy Refund Cell
Slot: Tactical Chip.

Hiệu ứng:
- hoàn lại một phần chi phí triển khai nếu unit giá cao sống đủ lâu
- phù hợp Overdrive Titan hoặc đội hình late-game

## Độ hiếm item
Đề xuất rarity:
- Common
- Rare
- Epic
- Legendary
- Mythic

Khác biệt:
- item càng hiếm càng có nhiều dòng chỉ số phụ
- Legendary trở lên có hiệu ứng riêng
- Mythic có thể gắn với boss hoặc world đặc biệt

## Nâng cấp item

### Level item
Dùng Item EXP và coin.

Tăng:
- chỉ số chính
- một phần chỉ số phụ

### Rank item
Dùng blueprint và vật liệu world.

Tác dụng:
- tăng giới hạn level
- mở thêm dòng chỉ số phụ
- nâng hiệu ứng đặc biệt

### Merge item
Ghép nhiều item cùng loại để tăng bậc.

Quy tắc gợi ý:
- 3 item cùng rarity có thể ghép thành 1 item rarity cao hơn
- item đã nâng cấp có thể hoàn lại một phần tài nguyên khi dùng làm nguyên liệu

## Item set
Item set giúp người chơi build theo vai trò.

### Set Bastion
Hợp Vanguard Breaker.

Bonus:
- 2 món: tăng HP
- 4 món: giảm sát thương khi đứng gần cổng Aegis

### Set Pulse Hunter
Hợp Pulse Ranger.

Bonus:
- 2 món: tăng ATK
- 4 món: đòn đánh có tỉ lệ gây Desync

### Set Phase Reaper
Hợp Resonance Blade.

Bonus:
- 2 món: tăng chí mạng
- 4 món: tăng sát thương lên enemy hỗ trợ và boss

### Set White Signal
Hợp Aegis Medic.

Bonus:
- 2 món: tăng hồi máu
- 4 món: khi hồi máu sẽ xóa một debuff cho mục tiêu

### Set Core Architect
Hợp Core Engineer.

Bonus:
- 2 món: giảm chi phí đặt trụ
- 4 món: trụ tồn tại lâu hơn

### Set Titan Frame
Hợp Overdrive Titan.

Bonus:
- 2 món: tăng sát thương diện rộng
- 4 món: skill nộ gây thêm hiệu ứng đẩy lùi

## Nguyên liệu nâng cấp

### Coin
Dùng cho hầu hết nâng cấp cơ bản.

Nguồn:
- campaign
- nhiệm vụ ngày
- Supply Run

### Hero Fragment
Dùng để tăng sao hero.

Nguồn:
- elite stage
- boss stage
- rương world

### Aegis Core Fragment
Dùng nâng lõi Aegis và skill nộ cao cấp.

Nguồn:
- Core Defense
- boss stage
- nhiệm vụ tuần

### Blueprint
Dùng nâng rank item.

Nguồn:
- elite stage
- world boss
- map hard mode

### Mutation Sample
Dùng nghiên cứu kháng infected.

Nguồn:
- boss
- enemy elite
- event world

## Quy tắc cân bằng
- Hero level tạo sức mạnh nền.
- Star tạo mục tiêu dài hạn.
- Đòn đánh cơ bản và skill nộ tạo khác biệt gameplay.
- Aegis Core tạo hướng build.
- Item tạo độ sâu và khả năng tùy biến.

Không nên để một hệ nâng cấp duy nhất quyết định toàn bộ sức mạnh. Người chơi cần có nhiều hướng cải thiện đội hình.

## Gợi ý mở khóa theo tiến trình
- World 1: level hero
- World 2: item cơ bản
- World 3: nâng skill
- World 4: item rank
- World 5: Aegis Core
- World 6: item set
- World 7: tăng sao hero
- World 8: legendary item
- World 9: nâng cấp skill nộ cao cấp
- World 10: awakening
