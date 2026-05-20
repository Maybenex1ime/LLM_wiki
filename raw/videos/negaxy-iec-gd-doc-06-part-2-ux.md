---
title: "GD Doc 6 Part 2 — UX: Định Nghĩa Yêu Ích, Value Perception, Multi-Start & 3 Giảm Thiểu (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 6 Part 2 - UX.mp4"
date_added: 2026-05-20
date_updated: 2026-05-20
tags: [video, course-transcript, game-design, ux, value-perception, big-numbers, multi-start, heart-system, ui-minimization, hearthstone, clash-royale, warcraft-rumble, vietnamese]
aliases: ["GD Doc 6 Part 2", "Buổi 6 Phần 2 UX", "UX Yêu Ích Vũ"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-06-part-1-ui]]"
  - "[[negaxy-iec-gd-doc-07-ui-ux-monetize]]"
  - "[[negaxy-iec-gd-doc-08-phan-tap-user]]"
summary: "Buổi 6 Part 2 (Vũ + Tài + Đồng + Hiệp + Giang + học viên): định nghĩa UX = tối ưu trải nghiệm × tối đa hoá lợi ích nhà sản xuất (book Pháp nguồn Apple-inspire). Hành vi vs lời nói qua câu chuyện bún riêu/cơm gà/mì Quảng. 4 ví dụ value perception: big numbers (100 gold > 1 gold), skill probability 7% vs 33%, gift trên total package (2M/4M vs 2M/2M). Tổng quan gameplay UX: Negabon single-button, Clash of Clans phá trừng phạt qua 3 versions, Farm Facebook vs Hay Day vs Township, Clash Royale (skill-gated) vs Warcraft Rumble (asset-friendly). Heart system: lọc user vs tăng session — case Nuts & Bolts paywall vs FarmCity ad-funded. 3 nguyên tắc UI minimization (số bước, lượng info, lượng quyết định) với Hearthstone keyword vs uvo dense card. Multi-Start 3 use cases (mạnh đầu/yếu đầu/phụ trợ), 3 risk patterns, element regret anti-pattern. Buổi kết thúc 10:20 do hết sức — phần 2 UI/Dark UI dời sang buổi sau."
---

# GD Doc 6 Part 2 — UX: Yêu Ích, Value Perception, Multi-Start

**Speakers:**
- **Vũ** — Lecturer chính. Reference 2Cơ Game, IEC, Tiny Battle, ngoại sử Highland coffee.
- **Tài** — Học viên ăn cơm gà gần nhà, ưu tiên sạch/giá.
- **Đồng** — Học viên Quảng Nam, mì Quảng + interaction với chủ quán + đi dạo phố. Anh thiết kế "đồng chí" muốn làm Multi-Start.
- **Hiệp** — Reference con NegaMod, single-button skill mechanic; bảo vệ multi-start cho game Pokemon-style 3 hệ.
- **Đức** — Học viên thẻ bài (continue từ Doc 5/Doc 6 Part 1).
- **Giang** — Lurker, ngoài hỏi cuối buổi về tập user → Vũ "nợ câu trả lời sang buổi sau."

**Format:** Buổi học trao đổi, **~87 phút** (audio 5206s — short hơn các buổi khác vì kết thúc sớm 10:20pm), tiếng Việt. Phần 2 của Doc 6 — chỉ về **UX**, sau khi Part 1 đã chốt UI. Vũ chủ động tách hai phần để không trộn.

Buổi này **dừng giữa chừng** — Vũ nói còn một nửa nội dung UI/Dark UI/Upstreet thinking, dời sang buổi sau.

Tiếp nối Doc 6 Part 1 (UI) và đặt nền cho Doc 7 (UI/UX & Monetize). Reference qua lại Doc 8 (3 tập user).

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 6 Part 2 - UX.mp4` (1.15 GB, ~87 phút) + `GD Doc 6 Part 2 - UX.mp4.txt` (2,075 dòng, faster-whisper large-v3 chunked qua `doc6_ux_chunks/` — 9 chunks 10-phút; chunks 001/003/008 re-split thành 5-min sub-parts trong `sub5/` do hallucination loop).

---

## Định Nghĩa UX — Trích Sách Pháp

Vũ mở bài bằng quote từ cuốn sách của một nhà thiết kế đồ gia dụng Pháp — sách inspire cho nhà thiết kế chính của Apple:

> *"Yêu ích là việc tối ưu hoá trải nghiệm của người dùng mang lại tối đa hoá lợi ích cho nhà sản xuất."*

Bình luận tự nhiên của lớp: *"Đúng chất tư bản."* Vũ confirm — *"Tóm lại là làm cho người ta sướng nhưng mà người ta không suy tiền ra thì mất công quá nhỉ."*

UX không phải làm user happy phi vụ lợi. UX là **hành trình kéo user về dòng tiền** thông qua trải nghiệm tốt. Hai phần luôn đi cặp:

1. **Yêu ích là cái gì** (tính năng / trải nghiệm).
2. **Mang lại lợi ích nhà sản xuất như thế nào** (monetization path).

Bỏ phần 2 ra = UX research thuần. Game studio không làm research — phải đi cả 2 chiều.

---

## Hành Vi vs Lời Nói — Câu Chuyện Quán Ăn

Vũ test 3 học viên về quán ăn quen → khai thác tiêu chí thật của họ.

### Tài — Cơm Gà Gần Nhà

- Món thích: cơm gà.
- Tiêu chí khai báo: ngon → rẻ → sạch.
- Khi push: *"Quán cơm sạch bán trăm nghìn một đĩa. Quán cơm bình thường cũng ăn năm mươi nghìn một đĩa. Chọn quán nào?"* → Tài chọn rẻ.

> *"Đấy. Thưa các bạn đây là hành vi đấy. Không phải những cái gì các bạn nói ra là những thứ các bạn nghĩ. Cái thứ mà các bạn thực tế hành động ấy mới là cái thứ các bạn nghĩ."*

Tiêu chí thật của Tài: **giá 50k là ceiling, sạch trong giới hạn đó**.

### Đồng — Mì Quảng Đông Đa

- Quê Quảng Nam, đi Hà Nội tìm hết quán mì Quảng → chốt 1 quán Đông Đa.
- Sẵn sàng đi xa từ Mễ Trì → Đông Đa (~10 km, 2 lần/tháng).
- Tiêu chí: ngon theo gu gốc Quảng Nam (cay/đậm) + giá phải chăng + tương tác bằng tiếng Quảng Nam với chủ quán + **hành trình đi dạo phố** đến quán.

> *"Em thích cả cái hành trình đi đến đấy chứ không phải thích mỗi cái chỗ đấy không."*

Tiêu chí thật của Đồng: gu hương vị **không đại diện cho tập chung** + emotional attachment với quê hương + experience layer ngoài món ăn.

### Vũ — Bún Riêu Đội Cấn

- Quán không quá ngon, không gần đường lớn, không rẻ hơn.
- Lý do quay lại: **chủ quán nhớ gu**. Vũ đến — không phải gọi món — bún riêu thịt bò ít bún nhiều mắm tôm + trà đá xuất ra ngay.
- Có hôm quên trả tiền — lần sau trả bù — không vấn đề.

> *"Người ta biết cái gu anh thích cái gì. Và người ta luôn ưu tiên anh làm được trước việc đó. Đấy là lợi thế. Khiến cho cái việc anh không đi thích thì sang quán khác."*

Tiêu chí thật của Vũ: **tiện + được nhớ mặt** > ngon + rẻ.

### Insight Tổng Quát

3 người = 3 tiêu chí khác nhau. Không thể "đánh đồng vào một cái bất kỳ":

> *"Cái việc mà tạo hành trình một cái trải nghiệm tốt ở trong game cũng vậy. Nó không đến từ bất kỳ một yếu tố nào gọi là chỉ duy nhất nó. Mà nó đến từ yếu tố tổng hợp — gameplay, UI, social network, cái thứ mà người ta thích."*

UX = compound experience. Cả studio bóp công để chiều user → user phải suy tiền ra. Không phải user paying = studio không chiều.

---

## Building Block của UX

### Sướng → Repetition → Habit

1. **Sướng** (vui HOẶC tiện) là điều kiện cần để user lặp lại.
   > *"Muốn lặp lại thì nó phải sướng nó phải lặp lại. Khổ thì lặp lại ít."*
2. **Lặp lại** tạo habit. Habit có 2 nguồn:
   - **Mới tạo** (do game design).
   - **Kế thừa** từ habit có sẵn (icon Home, icon hotel — *"vậy thì làm ơn đừng làm cái gì khác cả. Nó cứ vậy đi."*).
3. **Phá bỏ habit** (Anti-Cramming pattern — referenced từ Doc 2 Level Design) → user phải quyết định: xem RV / trả tiền / từ bỏ. Đó là điểm kiếm tiền.

Conventions không reinvent: home icon, hotel icon, settings gear, video play. *"Nhìn cái này thì các bố nghĩ ra là cái gì? Là cái hotel. Đúng không? Vậy thì cái này chúng ta đã được kế thừa rồi — làm ơn đừng thay đổi nó."*

### Value — Cho User VÀ Cho Mình

Mọi hành động lặp đi lặp lại phải mang giá trị cho user. Đồng thời phải sinh nhu cầu chi tiêu cho studio:

> *"Bây giờ các bạn tặng cho nó cái gì mà nó không có nhu cầu phát sinh mua bán nữa thì là cái không tốt với mình. Nhưng bạn tặng cái gì đó mà để cho nó phát sinh nhu cầu mua bán thì là cái đấy tốt với mình."*

---

## 4 Ví Dụ về Value Perception

### 1. Big Numbers — 100 Gold > 1 Gold

So sánh hai cấu hình kinh tế cùng tỷ lệ:

| Setup A | Setup B |
|---------|---------|
| Drop 1 gold | Drop 100 gold |
| Upgrade cost 1 gold | Upgrade cost 100 gold |

User cảm thấy Setup B *"cảm xúc hơn"* dù purchasing power giống hệt.

> *"Họ không biết được cái giá trị này và cái giá trị này nó tương quan với nhau như thế nào. Nhưng họ chỉ nhìn vào cái giá trị này cứ nhiều hơn là sướng."*

Cảm xúc ≠ sự thật. Reference: giá nhà VN tăng "danh nghĩa" nhưng purchasing-power-parity không tăng — *"Cảm xúc và sự thật đôi lúc nó giống nhau, đôi lúc nó khác nhau."* Designer phải design cho **cảm xúc**, không phải cho sự thật.

### 2. Skill Probability — 7% vs 33%

Anti-pattern: thiết kế quyết tích **7%** hoặc **7.5%**.

> *"Đánh đời nào ra được 7%? Nhìn vào con số này nó có tưởng tượng đánh bao lâu ra không?"*

Với 33%: user *"ó nó 10 tượng trong đầu rồi — đánh 3 phát chắc được."* Một trận ~40 hit → 33% = ~13 lần proc → cảm thấy đạt được. 7% = ~3 lần → cảm thấy hên xui.

Rule: chuyển con số sang **fraction dễ tưởng tượng** (1/3, 1/2, 1/4) thay vì decimal precision.

### 3. Gift-on-Package — Anchor Effect

Cold-call sales:
- Pitch A: *"Tặng anh gói bao trời 2 triệu."* Nhưng *"gói đấy là 2 triệu anh ạ"* → no anchor → user không thấy giá trị.
- Pitch B: *"Tặng anh gói 2 triệu trên tổng gói 4 triệu."* → user thấy **deal hời 50%** → phát sinh nhu cầu nghe.

> *"Mày phải tặng tao 2 triệu trên tổng gói 4 triệu — nghĩa khác rồi. Nó mới phát sinh nhu cầu nghe."*

Ứng dụng: starter pack, IAP — luôn có **"giá gốc gạch ngang"** > giá bán. Compare-to-anchor effect.

### 4. Highland Upsell — Size M → L

> *"Thằng Highland các bạn chỉ bỏ thêm khoảng 2000 đến 3000 nữa là bạn được một cốc cà phê từ size M lên size L. Thế là thôi bắt đầu cái máu tham nó nổ lên — còn chả biết là cái size L nó nhiều hơn size M bao nhiêu mà cứ mua cái cốc to nhất."*

Tư duy: **giảm bớt số lượng suy nghĩ** để user quyết định nhanh. Mục tiêu của upsell không phải convince user về size — mà bypass thinking.

---

## Gameplay UX — Case Studies

### Negabon (Hiệp) — Single-Button Skill

Cải tiến so với Pokemon gốc:

| Pokemon gốc | Negabon |
|-------------|---------|
| Chọn skill từ menu phía dưới | Chỉ 1 nút Attack |
| Bấm lên trên chọn target | Cùng nút đó vừa attack vừa skill |
| Đổi nhân vật riêng | Skill nằm trên thanh phong độ |

Mechanic: tap thanh **giữa (vàng/xanh)** = skill; tap thanh **bên cạnh** = đánh thường. Tỷ lệ phong độ +30% damage.

> *"Khiến cho user nó rất dễ hiểu. Và từ đấy cái việc là user sẽ không để ý đến phần phía trên luôn, chỉ tập trung nhăm nhăm đánh vào cái thanh này."*

Bài học: collapse 3-tap interaction → 1-tap. Mất kỹ thuật tay nhưng cảm xúc "perfect timing" thay thế.

### Clash of Clans — 3 Versions Phá Trừng Phạt

| Version | Behavior khi attack | Hậu quả tâm lý |
|---------|---------------------|----------------|
| V1 (đầu) | Quân chết = mất luôn, phải mua lại | User sợ đánh, ít match — *"anh nhìn nhà đối phương thấy sợ rồi anh không muốn đánh"* |
| V2 | Quân chết → hồi sau 1 phút | User vẫn ngại nhưng đỡ |
| V3 (current) | Quân không chết trong battle | Match liên tục, retention cao |

> *"Vì thế cho nên các cái cơ chế mà mình hay xưa gọi là mình gọi là trừng phạt. Các game mix là càng ngày nó bỏ đi càng. Càng ngày nó càng bỏ đi nhiều."*

Bài học: punishment mechanics phá habit formation. Studios mature đều phase out.

### Farm Games — 3 Generations

| Game | Cơ chế trồng | Vấn đề |
|------|--------------|--------|
| Farm (Facebook) | Trồng từ hạt + có người vặt trộm | Heo, mất sound |
| Hay Day | Trồng từ hạt, không có trộm | Hạt giống = hard cap, héo nếu không trông |
| Township | Trồng **bằng tiền** (không hạt) | Free batch — *"Em bán vè vè vè vè, hôm hôm phát 50 cái luôn"* |

> *"Cảm giác rất sướng. Và đấy là cách mà tôi đang tìm để chỉ cho các bạn. Mọi người đã nói là đều trồng cây nhưng mà cái đấy nó không đủ. Trồng cây bằng cái gì và vì sao ta làm cái đó? Đấy mới là vấn đề."*

Bài học: cùng surface mechanic ("trồng cây") nhưng **resource gate** khác → UX khác hoàn toàn. Đừng analyse mechanic ở surface level.

### Clash Royale vs Warcraft Rumble — Skill vs Asset

Đồng (skill player) thích Clash Royale. Vũ (asset player) thích Warcraft Rumble. Cùng game thẻ bài chiến thuật.

| Trục so sánh | Clash Royale | Warcraft Rumble |
|--------------|--------------|-----------------|
| Game mode | PvP-only | PvE chính + PvP phụ |
| Tài sản gate by | Skill (rank-based pack) | PvE progress (player-paced) |
| Khi gặp đội mạnh | Stuck, đội hình mắc, *"thua liền 2-3 trận anh chán, không có đường nào để lên nữa cả"* | Switch sang deck khác / chuyển PvE |
| Pack quan trọng nhất | Lên rank (skill-gated) | Lên PvE level |
| Chest reward | Time-locked (4 chest cap) → ngại chơi | Pick 3 challenges trong slots |
| Behavior trigger | Mua skill | Mua tài sản |

> *"Anh là người chơi hệ ngạc. Và khi anh ra trận có nghĩa là lúc đó đội hình phải mắc. Mà khi đội hình đã mắc, kỹ năng tay của anh lại kém. Anh thua. Thua liền hai ba trận. Anh chán."*

Bài học: cùng genre, **target archetype** quyết định UX. Reference Doc 8 — 3 tập user: asset / intelligence / skill display.

Vũ thừa nhận: *"Anh chơi thì toàn bọn đã legend... Mặc đếch nó anh thua liều xỉu."* — không phù hợp tập của anh. Game không xấu, **mục tiêu khác.**

---

## Heart System — Khi Nào Cần, Khi Nào Bỏ

Giang đặt câu hỏi về cơ chế tim trong puzzle games. Vũ chia thành 2 mục đích:

### Mục Đích A: Tăng Session/Day

Heart limit → user chơi đến khi hết tim → đợi → quay lại. **Tăng số phiên trong ngày**.

### Mục Đích B: Tăng Thời Gian/Session

Không tim → user chơi liên tục đến khi chán. **Tăng thời gian trên mỗi phiên**.

### Trade-off

> *"Nếu bạn tự tin rằng cái gameplay của bạn là gây nghiện — chứ không như người đặt điện thoại nót báo lên làm hoàn thành xong thì đặt vào lại. Chứ sau khi làm việc xong họ sẽ không có lấy lưu khóa lâu."*

- Game **gây nghiện** (đặt phone xuống vẫn nhớ) → không cần tim.
- Game **chỉ chơi khi rảnh** → cần tim để force session.

Heart cũng là **monetization gate** + **filter user**. User chơi qua nhiều round không hết tim cũng là một dạng sướng.

### Anti-Pattern: Heart Tiền Mua Bắt Buộc (Case Nuts & Bolts)

Vũ chia sẻ behavior cá nhân với Nuts & Bolts (OneShot):

> *"Sau khoảng 2 tới 3 lần chơi bị thua mình bắt đầu ngấm ngấm hiểu hiểu cái puzzle đấy. Thì lần cuối cùng mình chơi hết 4 tim... Mình phải để mua với một cái giá nó đắt đỏ so với cả cái behavior tập khách hàng của mình. Tóm lại là sao mình bỏ 1 đô 99, 2 đô 99 không có tài sản gì để quay về thì đối với mình mình không bỏ."*

Improvement: thay vì **mua tim bằng tiền**, cho phép **xem ad đổi tim**:

> *"Nếu là đặt quảng cáo được tặng tim thì anh sẽ happy hơn."*

Caveat: behavior cá nhân của anh không đại diện cho all users. Test trước khi commit.

### Đối Tỉ: Township → FarmCity

Vũ ngày xưa chơi Township heavy IAP, đến 1 tháng mới qua content. Sau đó chuyển sang FarmCity (iCame) — game ad-funded:

> *"Có những cái ngày mà nói thật với mọi người là anh chơi đến cả 100 lượt quảng cáo... Trước kia anh chơi con Township 1 tháng thì bây giờ bằng anh chơi con Township chỉ 4 đến 5 ngày thôi. Anh được khám phá các content sau cũng cảm rất sướng."*

7× progression speed → 7× content discovery → user sướng hơn dù studio earnings không phải IAP. Yêu cầu: studio chấp nhận **giảm price-per-user** đổi lấy **tăng volume + retention**.

Caveat: chỉ valid cho **dòng game ad-funded** đã establish. IAP game không đơn giản convert sang ad-funded.

---

## UI Triết Lý — 3 Giảm Thiểu

Đây là phần mở đầu UX cho UI design. Triết lý: **giảm thiểu**.

| # | Giảm thiểu cái gì | Hiệu quả |
|---|-------------------|----------|
| 1 | **Số bước** để làm nhiệm vụ / nhận reward | User hành động **nhanh hơn** |
| 2 | **Lượng thông tin** user phải tiếp nhận | UI **gọn hơn**, dễ đọc |
| 3 | **Lượng quyết định/suy nghĩ** trước action | User trở thành **người hành động theo thói quen** — không cần suy nghĩ quá nhiều |

Đặt tên: **3 Giảm Thiểu** (3 Reductions).

> *"3 cái này nó hiển thị theo 3 bước, theo 3 cái tư duy này. Làm theo số bước là gì? Nhanh hơn. Theo số lượng thông tin gọn hơn. Và số lượng thứ 3 là biến user trở thành những người hành động theo thói quen, không cần phải suy nghĩ quá nhiều."*

---

## Case Hearthstone vs uvo — Keyword Compression

Vũ so sánh game thẻ bài:

### uvo

- Thẻ chữ rất dài.
- 10 con = 10 kiểu khác nhau.
- Yêu cầu user đọc kỹ từng thẻ.
- Audience **niche** (sưu tầm hardcore).

### Hearthstone

- Mỗi thẻ chỉ vài keyword: *"street"*, *"chat"* (taunt, charge).
- 10 con quy về ~2 kiểu.
- User parse keyword + icon → biết stat hierarchy ngay.
- Audience mass-market.

> *"Người dùng người ta hiểu ngay, người ta biết ngay vấn đề đó."*

Bài học **giảm thông tin** = **tăng audience**. Niche game = compact text, mass game = keyword compression.

> *"Bây giờ bạn cho 1 cái con mà nó viết khoảng tầm 2 dòng, 1 con khác viết khoảng tầm 3 dòng. Tóm lại con nào có 3 dòng theo góc độ của 1 thằng user — nếu như thế thì chắc là nên làm cả bản hình luôn. Mình sẽ nghĩ có cái mạnh nhất."*

Đơn vị heuristic: nhiều text dòng = mạnh hơn (user assume). Designer phải phá assumption này bằng visual hierarchy.

---

## Material Variety — Quá Nhiều Loại Tạo Decision Paralysis

Đức (game thẻ bài) có 4 loại material upgrade. Vũ critique:

> *"Cha mẹ bây giờ sao không nhiều thế? 2 cái được không, có đến mức độ cần phải nhiều đến 4 cái?"*

### 2 Materials

- User flow: *"có 1 con legendary, có 1 lượng tài nguyên nhất định, mình cứ tác thậm chí là tệ hết là hold cho tới khi hết tiền."*
- Không cần tính toán → habit-driven.

### 4 Materials

- User phải so 4 con số.
- Quyết định: nâng legendary hay rare hay epic?
- Khi tài nguyên mix-match (con A dùng material 1,2; con B dùng 3,4) → **càng phức tạp hơn nữa**.

> *"Càng suy nghĩ càng tính toán nhiều thì nó càng khó tạo thành thái quen. Dừng lại nhiều hơn."*

Anti-pattern GD: *"Các bạn rất thích làm những cái lượng thú, các bạn rất thích những cái skill kiểu khác nhau rõ ràng."* — thích thú giai đoạn đầu nhưng habit không hình thành.

---

## Skin Variety — ABC/BCD/ACD Bridging vs ABC/DEF

So sánh 5 con với hệ skill (mỗi con dùng 3 skills A-F):

### Pattern Tốt — Bridging

```
Con 1: A B C
Con 2: B C D
Con 3: A C D
Con 4: A B D
Con 5: ...
```

Có **skill overlap** → user so 2 con cùng skill chung → loại dần. *"Tính chất bắt cầu chỉ còn lại là C và D."*

### Pattern Xấu — Disjoint

```
Con 1: A B C
Con 2: D E F
```

User không có cơ sở so sánh. *"Yếu chỉ vì 1 cái skin thôi thì bạn không biết được."* Quyết định mua → không có baseline.

### A+ Pattern — Same Skill Set, Stronger Stat

> *"Con kia là 30% kích cỡ tóm lại là đánh 3 phát đều 1 phát. Con này cũng thế nhưng mà 50% có nghĩa là 1 mít 1 được. Xong chưa? Dễ à? Có đồng nào nghĩ ra quả skin 100% như tựa A không?"*

Cho phép user nhìn 1 skin → so sánh được. Vẽ icon cũng dễ — *"Hình bên trong nó giống nhau khác nhau một cái vảnh bên ngoài là ok rồi."* Công sức art giảm, decision speed tăng.

---

## Resource Refund — Slot-Locked Upgrade

Hiệp đưa ra giải pháp đã thấy: nâng cấp **gắn vào slot** thay vì gắn vào nhân vật.

### Anti-Pattern

- Nâng cấp gắn con → đổi áo mới → mất level → tiếc tiền.
- User dí dòng: *"Khởi đầu trận nó hay dí dòng mấy cái đấy — tiết kiệm tiền để thằng Legend."*

### Pattern Tốt (Con Acero của HB)

- Slot level 9 → bất kỳ áo nào mua cũng auto level 9.
- *"Khỏi cần phải trả lại. Đỗ cơ chế trừng phạt cũng như thế là sướng hơn."*

User skill-driven (giữ tiền cho legendary):
- Lúc đầu không dám nâng con nào → giữ tiền.
- Đến bàn khó → nâng vừa đủ qua → swap legendary sau.
- Slot-locked design support pattern này — không bị punish khi swap.

---

## Multi-Start — 3 Use Cases & Risk

Hiệp & Đồng đều muốn làm Multi-Start (chọn 1/3 nhân vật đầu game). Vũ phân tích.

### Khi Nào Cần Multi-Start

Bắt buộc cho **game phân role**:
- Empire / Rise of Kingdom (chọn quốc gia).
- Game team-based với class system.

Không cần cho **hành trình độc lập** (single-player narrative). Multi-start ở đây = "hơi quá sức."

### 3 Mục Đích Multi-Start (Per Role)

1. **Mạnh đầu yếu sau** (early game power) — đa số user chọn.
2. **Yếu đầu mạnh sau** (late bloomer) — *"nhiều ông không trụ được bởi vì bị thọt ra."*
3. **Phụ trợ** (support role) — *"rất ít người chơi thích chơi ở nhóm phụ trợ này."*

> *"Đa phần các bên sẽ chọn cái loại đầu — sướng được ngày nào là sướng. Khi nào hết sướng thì ta bỏ."*

### 3 Risks Of Multi-Start

#### Risk 1: Non-Linear Progression

> *"Multi-start nó sẽ không tuyến tính với tất cả các người chơi... Có người nó sẽ tốt hơn mặt bằng chung thị trường, và có người sẽ bị yếu hơn mặt bằng chung."*

User yếu hơn → cảm thấy bị punish → quit trước **monetization threshold** (level nó in-app cho mình) → mất doanh thu.

#### Risk 2: Balance Mess

Trong game đế chế / Rise of Kingdom: *"Tóm lại nó sẽ gom hết vào một nùi những cái bọn khỏe."* — toàn bộ user dồn vào 1 class → 2 class còn lại die. YouTube reviewer phải explicitly chỉ "start với nation X" → bypass tự do chọn.

#### Risk 3: No Restart Path

Mobile user không biết cách clear data:

> *"Rất nhiều user không biết clear cách. Clear data để chơi lại đâu. Họ không biết cách clear data. Và gần như là họ sẽ bị mắc định — chỉ có là xóa dữ liệu đi, tải lại một con game mới thôi. Xóa game đi thôi, tải lại."*

User stuck level 15 với class sai → quit thay vì restart. Hiệp's solution: *"unlock luôn 2 con còn lại"* sau checkpoint 1. Vũ improve: *"để hết check qua một, là người tem họ sẽ có được đủ 3 cái vật liệu"* — collect cả 3 con sau checkpoint 1 → no regret + circular balance.

### Anti-Pattern: Element Rock-Paper-Scissors → Regret

> *"Lúc đầu em chọn con lửa ở VN. Bị nó đẹp. Xong đánh, ồ chết rồi xong mình chọn sai rồi. Rồi đến con này mình sắp tắt ngay ở đây rồi gặp toàn con lửa. À con lửa chứ thì bị nước nó khắc."*

User chọn element → encounter toàn enemy khắc → cảm giác regret. Fix:

> *"Em làm cho người chơi, em phải vẽ cho người chơi cái chiều này. Ví dụ như là chọn lửa thì gặp nước, chọn nước thì gặp hỏa. Chứ không cho người ta cái cảm giác bị thất vọng."*

Encounter design **bám theo lựa chọn ban đầu**. User chọn lửa → đầu game gặp nước (lửa khắc nước → user thắng) → *"luôn luôn người chơi cảm thấy ôi may quá mình chọn con này."*

### Customize Start ≠ Multi-Start

- **Customize start** = chọn nam/nữ, skin → cosmetic, không ảnh hưởng gameplay.
- **Multi-start** = chọn role/class → ảnh hưởng gameplay balance.

Đừng nhầm.

### Multi-Start Strength

Khi đúng dòng game (RPG hệ Pokemon, MMO class):
- **Curiosity** (kỳ vọng + tò mò) — *"khơi gợi cho em được một cái kỳ vọng."*
- **Replay value** — chơi lại với class khác.

Hiệp's case: 3 hệ Pokemon, balance per checkpoint, user-friendly (chỉ cần 2-3 ngày để hiểu). Defensible.

Đồng's case: 2Cơ Game kingdom với 1 hero → switch sang 3 hero. *"Rất khó quay đầu."* Vũ cảnh báo high risk vì không có precedent + chỉ số hero hiện tại không ngon.

---

## Defending Decisions — "Bull Start Dự Án Phải Bảo Vệ Đồng Chí Em"

Cuối buổi Vũ chốt nguyên tắc:

> *"Bull start dự án là phải bảo vệ đồng chí em."*

Tức là: **document reasoning** cho mọi feature decision. Khi đưa lên sếp, các bên khác hỏi *"Tại sao anh nghĩ ra của cái này là cái gì? Giải quyết cái này như thế nào?"* — GD phải trả lời được.

> *"Tất cả các câu hỏi của mọi người nằm trong tất cả cái khuôn của mình. Và nếu mọi người hỏi những câu hỏi ngoài khuôn, hoàn toàn có thể đi bên lại."*

Common conflict: UA team hỏi *"Tại sao lại dùng vùng ảnh này, tại sao lại diễn cái action này trong khoảng thời gian này?"* → designer không trả lời được = đã fail communication.

Test fast → cheap; test risky → đắt. Phân biệt:
- Test rẻ → cứ thử.
- Test đắt (Đồng's 3-hero pivot) → bảo vệ logic chặt trước khi test.

> *"Cái việc chúng ta xuất phát một ý tưởng bằng một cách rất là chủ quan mà không được chuẩn bị đầy đủ tất cả các vụ hoặc là bảo vệ nó một cách tốt nhất, thì mọi người sẽ khó trong vấn đề mà thuyết phục hoặc là khó trong vấn đề mà kiểm soát được sản phẩm này."*

Sau khi test mà fail → không biết tại sao fail → không iterate được.

> *"Kể cả là thuyết phục được rồi sau lúc sau test chả biết nó đúng hay sai ở đâu. Khó nhất là cái việc đấy luôn."*

---

## Lecture Cut Off Early

Đến 10:20pm Vũ thông báo:

> *"Bây giờ hỏi mọi người là theo cái trải nghiệm, cái ưu ích của mọi người, bây giờ ta nên đi tiếp hay nên dừng lại?"*

Sau khi lớp đồng ý dừng:

> *"Cái phần còn lại nó nói rất nhiều... Về sau những cái thứ còn phần UI còn chưa xong, còn phần Dark UI nữa. Nó còn tương đối nhiều thứ. Và thậm chí là còn có cả cái phần mà liên quan tới cái tự duy sách Upstreet ban đầu nữa."*

Pending nội dung sang buổi sau:
- Phần còn lại UX về UI.
- Dark UX techniques (sẽ đầy đủ ở Doc 7).
- Sách Upstreet thinking (cách viết spec UX từ đầu).
- Giang's câu hỏi: **3 tập user** đặc trưng (sẽ trả lời ngay buổi sau — actually đã có trong Doc 8).

Self-aware closing: ngày hôm đó *"theo cái trải nghiệm, cái yêu ích"* nên dừng — tức là Vũ áp dụng ngay nguyên tắc UX tôn trọng năng lượng người dùng (lớp học).

---

## Anti-Pattern Tổng Hợp

- **Skill probability 7%** — user không tưởng tượng được → cảm giác hên xui.
- **1 gold drop + 1 gold upgrade** — đúng tỷ lệ nhưng không cảm xúc. Dùng 100/100.
- **Gift offer không có anchor** — *"tặng 2 triệu"* không thuyết phục bằng *"tặng 2 triệu trên gói 4 triệu."*
- **Reinvent home/hotel/settings icon** — vi phạm inherited habit.
- **Punishment mechanic** (quân chết hẳn) — phá habit formation, phase out.
- **Heart paywall không có ad option** — ad-for-life better cho ad-funded.
- **Card text dài 3 dòng** — user assume = mạnh, không thực sự đọc.
- **4 loại material** — decision paralysis, kill habit.
- **Skin disjoint** (ABC vs DEF) — không có cơ sở so sánh.
- **Slot upgrade gắn con** — user tiếc nâng cấp cho con không phải legendary.
- **Multi-start với element regret** — user chọn → encounter khắc → quit.
- **Multi-start không có restart path** — user stuck level 15 → uninstall không restart.
- **Customize start nhầm với multi-start** — male/female ≠ role choice.
- **Designer không document reasoning** — UA/sếp hỏi → fail, test fail → không iterate.
- **Test expensive feature không có backup plan** — Đồng's 3-hero pivot risk.

---

## Thuật Ngữ Buổi Này

### UX Definition
- **Yêu Ích** (UX) — tối ưu hoá trải nghiệm user + tối đa hoá lợi ích producer (def từ sách Pháp).
- **Hành Vi vs Lời Nói** — user nói A nhưng làm B, design cho B.
- **Cảm Xúc vs Sự Thật** — designer design cho cảm xúc (perceived value), không design cho sự thật (intrinsic value).

### Habit Formation
- **Sướng → Lặp Lại → Habit** — core loop UX.
- **Sướng** = vui HOẶC tiện. Hai pillar khác nhau.
- **Inherited Habit** — icon Home / Hotel / Setting đã universal — không reinvent.
- **Anti-Cramming Point** — điểm phá habit để monetize (referenced từ Doc 2).

### Value Perception
- **Big Numbers** — 100 gold > 1 gold dù tỷ lệ giống. Đơn vị cảm xúc.
- **Skill Probability** — chuyển 7% → 1/3, 33% → 1/3. Fraction-friendly.
- **Gift-on-Package Anchor** — *"tặng X trên tổng Y"* (Y > X) → user cảm thấy deal.
- **Highland Upsell** — *"+2k-3k để size L"* → bypass thinking.
- **Value-For-User AND Value-For-Studio** — gift mà không sinh nhu cầu mua = waste.

### Gameplay UX
- **Single-Button Skill** — collapse multi-tap → 1-tap (Negabon vs Pokemon).
- **Phá Trừng Phạt** — Clash of Clans 3 versions: quân chết → hồi → không chết.
- **Resource Gate** — Facebook Farm (theft) vs Hay Day (hạt) vs Township (tiền, no seed).
- **Skill vs Asset Player** — Clash Royale (skill-gated) vs Warcraft Rumble (asset-friendly).

### Heart System
- **Heart = Filter** — phương án monetize qua bottleneck.
- **Tăng Session/Day vs Tăng Phiên/Time** — 2 mục đích heart system.
- **Heart Ad Trade** — xem ad đổi tim > mua tim, cho game ad-friendly.
- **Township → FarmCity Conversion** — heavy IAP → ad-funded → 7× content speed.

### UI Triết Lý — 3 Reductions
- **Giảm Số Bước** — flow nhanh hơn.
- **Giảm Lượng Thông Tin** — UI gọn hơn (Hearthstone keyword vs uvo dense).
- **Giảm Lượng Quyết Định** — habit-driven action.

### Resource Design
- **Material Limit** — 2 max, 4 = decision paralysis.
- **Skin Bridging** (ABC/BCD/ACD) — overlap skill cho phép compare.
- **Skin A+** — same skill set, stat bigger → easy comparison.
- **Slot-Locked Upgrade** — level gắn slot không gắn con → no penalty khi swap.

### Multi-Start
- **3 Role Use Cases** — mạnh đầu / yếu đầu / phụ trợ.
- **3 Risks** — non-linear / balance mess / no restart path.
- **Customize Start** — cosmetic, không phải multi-start.
- **Encounter Friendly Element** — design enemy bám theo lựa chọn ban đầu, ngược lại với mặc định.
- **Circular Balance** — sau checkpoint 1, user unlock cả 3 con → no regret.

### Decision Defense
- **Bull Start Dự Án Phải Bảo Vệ** — GD document reasoning trước khi pitch.
- **Question Frame** — *"trong khuôn của mình"* vs *"ngoài khuôn"* (bị conflict, đi bên lại).
- **Test Cheap → Try; Test Expensive → Defend Logic** — cost-based test gate.
- **Fail Without Reason** — không document → fail không biết nguyên nhân → không iterate.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Video gốc: `GD Doc 6 Part 2 - UX.mp4` (1.15 GB, ~87 phút).
- Transcript đầy đủ: `GD Doc 6 Part 2 - UX.mp4.txt` (2,075 dòng, faster-whisper large-v3 chunked qua `doc6_ux_chunks/`).
  - 9 chunks 10-phút chính.
  - Chunks 001/003/008 re-split thành 5-min sub-parts trong `doc6_ux_chunks/sub5/` (hallucination loop trên 10-min chunks).
  - Chunk 008_part_1 (1.78 phút cuối) transcribe lại 2026-05-20 sau khi lỗi rỗng từ 2026-05-19.
- Khoá học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
- Vị trí trong khoá: **Buổi 6 Phần 2 — UX** (nằm sau Doc 6 Part 1 UI; đặt nền cho Doc 7 UI/UX & Monetize, Doc 8 Phân Tập User).
- Date updated 2026-05-20: compile lần đầu sau khi chunked transcription hoàn tất + final concat.
- **Lưu ý buổi dừng sớm:** Buổi này chỉ phủ ~50% nội dung dự kiến. Phần Dark UX + Upstreet thinking dời sang buổi sau (chưa có doc number rõ).
