---
title: "GD Doc 4 — Level Data, Phá Thói Quen & IAP Design (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 4  (IPhone).mp3"
date_added: 2026-05-14
tags: [video, course-transcript, game-design, level-design, level-data, iap, retention, rpg, vietnamese]
aliases: ["GD Doc 4", "Buổi 6 Level Data", "Level Design Data & IAP"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-02-level-design]]"
  - "[[gamerefinery-match-3-code-part-2]]"
  - "[[linkedin-tandon-match-3-code-part-1]]"
summary: "Buổi 4 (theo curriculum là Buổi 6, đảo lên dạy trước): phân biệt level data vs xếp tay, file tiêu chí + file ý đồ, kỹ thuật phá thói quen người chơi, biến ẩn để điều chỉnh khó sau IAP, định giá IAP theo user value, RPG unit weakness, retention vs session length tradeoff."
---

# GD Doc 4 — Level Data, Phá Thói Quen & IAP Design

**Speakers:**
- **Vũ** — Lecturer chính (xưng "anh"/"mình", người dẫn buổi).
- **Hiệp** — Co-lecturer (chia sẻ về difficulty curve lỗi thời, profile-based skill).
- **Giang** — Học viên có dự án thực tế (Halo / tower-base với RPG units, đang vận hành).
- **Hoàng** — Học viên hỏi về việc quy đổi biến độ khó thành 1 công thức.
- **Quân** — Học viên puzzle pin (game pin-pulling 10 level/chặng, element lava + nước).
- Một số học viên khác (con sort, con shooter, con survival, con đi vét tổng).

**Format:** ~150 phút, tiếng Việt. Buổi này theo lịch curriculum là **Buổi 6 (Level Data)** nhưng Vũ đảo lên dạy ngay sau Doc 2 — *"Đảo đến buổi số 6 đây làm trước nhé."*

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 4  (IPhone).mp3.txt` (3,559 dòng, ~19k từ).

---

## 2 Dạng Level Design Cơ Bản

Vũ mở đầu bằng việc nhóm tất cả các kiểu level design lại thành 2 trục, để học viên biết game của mình thuộc nhóm nào trước khi áp công cụ:

- **Level Data** — thiết kế bằng số trên Excel hoặc Grid (ô vuông, lục giác). Ví dụ: *"level 1 có con này bao nhiêu, level mấy số bao nhiêu"*. Áp dụng cho Match-3, sort, các game có ô lưới.
- **Level xếp tay (set time / handcrafted)** — Designer kéo thả vị trí trong Unity. Áp dụng cho Puzzle Pin (pull-the-pin), puzzle vật lý, Action Puzzle, RPG, environment shooter, game chiến thuật cần xếp map.

Một số game lai cả 2:
- 1 map dùng chung cho level 2 và level 7 (map không đổi) — nhưng đội quân spawn ở vị trí khác, số lượng khác, timing thả khác nhau. *"Bọn này đi thả theo thời gian, cách nhau là không phải — cách nhau 2 giây, con bạn này cách nhau 3 giây."*
- Map có boss → file config boss riêng (HP/damage/tốc độ chạy/vị trí spawn trong map).

Quy tắc Vũ nhấn: *"Nó thuộc nhóm nào thì mình bổ vào — nó mới dễ."* Trước khi học cách làm phải biết game thuộc nhóm nào.

---

## Trình Tự Xây Dựng Level Design — 2 File Indo + 1 File Output

Vũ chỉ ra anti-pattern phổ biến: *"Các bạn sẽ làm một file output luôn — level design xuất đầu ra luôn."* Designer skip 2 file đầu vào quan trọng:

### File 1 — File Tiêu Chí

Định nghĩa level cần đạt được cái gì TRƯỚC KHI thiết kế:
- **Content**: có bẫy số 1, bẫy số 2, đến cái thứ mấy.
- **Mức độ**: easy / hard / tutorial.
- **Chỉ tiêu validation**: same-art, tỷ lệ replay, các metric mong muốn.

### File 2 — File Ý Đồ (Design Intent)

Bao gồm cách triển khai từ tiêu chí → level cụ thể. Cấu trúc 1 ý đồ chuẩn (cho 1 lộ trình level 1-6):

```
Tutorial → Easy → Easy → Medium → Hard → Nightmare
100%     0%      0%      5%       8%      15%
win      thua    thua    replay   replay  replay
```

Sau khi pick ý đồ, dự án soát chéo: *"Eo, sao mày ác kê, mới vừa 16 mà mày cho người ta 15% chơi lại rồi — anh nghĩ là ít thôi, khoảng tầm 10% là vừa."* Có cuộc trao đổi cụ thể giữa người trong dự án để chốt con số.

### File Output — Level Design

Đến đoạn convert tiêu chí thành số mu (moves) cụ thể:
- Tutorial: 1-2 mu.
- Easy: tăng dần theo dòng game.
- Hard: hardcore = 20 mu thì thực để 23-25 mu cho user → ép tỷ lệ replay vào ~15%.
- Lý do gap: *"Kỹ năng của mình sẽ tốt hơn của user — tính cho user thoải mái hơn tí."*

Quote chốt phần file ý đồ:
> *"Anh gặp rất nhiều các bạn — khi mình chơi thử level design của bạn ấy và khi bạn ấy trình bày thì lúc đầu mình hiểu hiểu một tí, nhưng sau mình mới đổ không hiểu. Bởi vì là qua một level, hai level thì bạn ấy còn nhớ, đến level thứ ba bắt đầu quên — và bạn trình bày khác đi so với những gì bạn ấy đang thực làm."*

File ý đồ tồn tại để designer **không quên** ý định của chính mình giữa chừng.

---

## Pattern Habit — Tạo Thói Quen Rồi Phá Vỡ

Vũ định nghĩa kỹ thuật "tạo độ khó bằng cách phá thói quen". Analogy bình nước:

> *"Ngày đầu tiên bạn đến bạn nhìn, bạn cầm nó lên. Ngày thứ 2 bạn đi đến gần lại nó chủ động lấy. Đến ngày thứ 3 bạn có thể vừa bấm điện thoại vừa đi qua vẫn lấy được. Ngày thứ 4 có ông nào đấy rời cái bình nước từ bên trái sang bên phải — các bạn đi qua, cua tay theo thói quen, và không tìm thấy bình nước. Bạn đâu có phải ngó nghiêng đi tìm bình nước này, đi bộ sang một hai bước cầm nó lên — như vậy là các bạn đã phải tăng phí mu cho người chơi rồi."*

### Case 1 — Lưỡi Cưa (Saw Blade)

3 bài đầu: lưỡi cưa chỉ chạy thẳng A → B → A. *"Bài 1 nó giòn giả, bài 2 nó quen, và bài thứ 3 là không cần ngắm xem nó quỹ đạo nó dễ chạy như thế nào — nó nhảy phọt phát qua luôn, không cần để nghĩ."*

Bài 4 phá thói quen — 2 cách:
- Thêm vật cản mới trên đường.
- Đổi logic jump-point: thay vì A → B → A, đổi thành A → B → C → B → A. User đã quen pattern cũ sẽ nhảy sai vị trí.

### Case 2 — Tower Defense 2 Cọp

4 level đầu thả quân ở 1 cọp. *"User đã xây dựng hết chú bên này thì bọn nó đi vào cái chỗ đường chống — như thế nó bị thua và nó phải chơi lại."* Level 5 spawn quân bên cọp đối diện.

### Case 3 — Bắn Máy Bay Theo Quỹ Đạo

*"Trước khi nhìn thấy sự việc, user sẽ action. Lần 1 nó cứ bay ngang, lần 2 bay ngang, lần 3 bay ngang — dù trong đám có 1 con cáo thẳng dưới mặt mình, thì nó là một cái mồng, và có thể là to luôn."*

**Quy tắc**: 3 level tạo thói quen → 1 level phá → user chết 1 lần → đạt tỷ lệ replay đã đặt trong file tiêu chí. *"Các bạn làm thế giới này để 3 level chỉ chuẩn bị cho một lần user chết."*

---

## Quy Đổi Biến Sang Một Difficulty Score

Hoàng đặt câu hỏi: *"Có thể vẽ difficulty curve bằng cách quy đổi nhiều biến (thời gian, số move, obstacle, số màu) về 1 score không?"*

### Sort Game — 3 Biến Đo Khó

Vũ ví dụ con sort (không có move/time limit):
1. **Tổng số viên** — nhiều thì action nhiều.
2. **Số ô trống** — 3 ô = dễ, 2 ô = trung bình, 1 ô = khó, 0 ô = "bốc" (user bấm 1 viên xem, để lấy 1 slot trống trước khi move).
3. **Mật độ phân tán màu trong cùng 1 cổng** —
   - `A,A,A,B,B` (cụm) = dễ.
   - `A,B,A,B,A` (xen kẽ) = khó.

### Match-3 — 3 Phần Trong 1 Level Fixed-Time

1. **Goal** (tượng gấu, vật cần thu).
2. **Pattern combo prepared** — designer đã xếp sẵn 2 bomb + 1 rocket "nhìn phát là thấy combo".
3. **Random fill** (ball nut) — phần còn lại được random.

Pattern dùng để ép độ khó: *"User chơi đến 4 ván không qua được — làm ơn, hãy làm chỗ này [phần random] đi để cho user có thêm 1 quả rocket nữa, mà không phải thay level time khác."*

### Vấn Đề Multivariable

Vũ giải thích vì sao không thể tính "ngay" difficulty từ N biến:
- Cần quy về **1 biến cuối cùng** để control (số mu cho Match-3, win-rate cho Pull-the-Pin).
- Đừng cứ thêm biến để control khó — *"Cứ cộng vào liên tục để tạo ra độ khó thì không đúng nhé. Tới giờ làm thế là rất khó control."*
- Các biến phụ (mật độ, intersperse) tác động vào biến chính (số mu/drop rate), không thay thế nó.

### Interest Curve Bổ Sung

Designer thêm content mới tại các điểm cố định (level 10, 20...) để vừa tăng độ khó vừa tạo hứng thú. *"Đến level đấy bình thường chỉ có 3 màu — nhưng đến đấy mình muốn tăng độ khó vừa muốn tăng sự hấp dẫn nữa, thì thêm 1 màu nữa, đạt được cả 2 tiêu chí."*

Quy tắc: 1-2 tiêu chí / level, không nhồi nhiều cùng lúc, nếu không lúc fix không biết chỉnh biến nào.

---

## Game Theory Optimization — 3 Nhóm User Match-3

Câu chuyện điển hình của buổi. Vũ vẽ 1 board Match-3 có 2 combo:
- Combo 1: dọc, có khả năng nổ chain cao.
- Combo 2: ngang, nhìn to hơn.

Hỏi học viên: "Em chọn nước nào trước?" — nhận được 4 cách lý giải:
1. Chọn combo 1 vì là dọc → tạo cascade lớn hơn.
2. Chọn combo 2 vì combo to hơn.
3. Chọn cái thấy đầu tiên / trên tay quen.
4. Chọn dưới đáy → cascade lan từ dưới lên.

Vũ phân loại user:

- **Nhóm First-Look** — *"To lạ và nhìn thấy cái đùi gà to thì ăn trước, không cần phải gì cả."* Hành vi: 2 → 1 nếu 2 không liên quan tới 1.
- **Nhóm Logic Tính Toán** — tính cascade, đi từ 1 → 2 để tối ưu chain.
- **Nhóm "Mắc kém" / Scattered** — đi chỗ quái nào không theo logic, tìm combo 3 ở chỗ khác hẳn. *"Cái nhóm này gần như là cái nhóm có tỷ lệ win thấp nhất, thấp tịch luôn."*

### Design Intent — Nudge User

Khi muốn ép 75-80% user pick combo 2: *"Anh kéo cái 2 này dọc ra một cái — nó vừa to, nó vừa dài, nó vừa sâu ở phía dưới."* → first-look user và logic user đều converge sang combo 2.

Quote: *"Các con game thì người chơi là những cỗ máy có cách tính toán khác nhau, nhưng tựu trung có một số nhóm. Khi mình bắt được action của người ta, mình hãy dùng thói quen đi của người ta để lấy cái thắng."*

---

## Difficulty Curve Cổ Điển Lỗi Thời (Tiếp Doc 2)

Hiệp / Vũ giải thích vì sao biểu đồ độ khó tăng monotonic (kiểu học 2017) không còn đúng:

- **Game premium hiện đại** không "ăn tiền user trước" như game bán bằng/bán lĩa ngày xưa. Phải kéo user đi xa nhất có thể.
- Mục tiêu: drop sau mỗi level càng ít càng tốt (3% drop / level 1-10 là đã mừng).
- *"Ngày xưa em học GD và em được dạy thế này — em cũng bị tươi trải — là cứ thế này mà ra đồ khó, nó luôn luôn đi lên. Nó thực tế nhưng nó lại không phải thế này."*

### Profile-Based Skill — Difficulty Phẳng Thực Sự

Skill user tăng theo profile1 → profile2 → profile3, biểu đồ khó vẫn flat nhưng *perceived difficulty* gần như không đổi:

```
Difficulty (designer)  ──────────  (flat)
User skill profile     ──↗──↗──↗  (rises)
Perceived difficulty   ──────────  (flat or slightly easier)
```

Cho RPG / game có chỉ số: power gear (báo voi cấp 1 → cấp 2) bù trừ cho difficulty curve tăng → user vẫn cảm thấy cân bằng.

---

## Bài Toán Của Giang — Multivariable Không Tính Được

Giang phản biện: con Pull-the-Pin của ông không tính được difficulty bằng công thức — *"Cứ làm nó ướm ướm thôi. Chạy xong có user thì nhìn cái kết quả rồi mình chỉnh lại."*

Multivariable cụ thể (con Pull-the-Pin level 15 vs 16):
- Số lượng pin: bằng nhau.
- Khác biệt: **mật độ đan xen** giữa các pin trong layout — pin block lẫn nhau hay không.

Vũ và Hiệp thừa nhận:
- Một số game (Pull-the-Pin, MoSort/IQ optimization) **biến trong biến**, hàm chồng hàm → công thức không tính ra được.
- Vẫn cần file tiêu chí: target = 85% win-rate cho level 15 → chỉnh số pin / đan xen cho đến khi đạt target qua test.
- *"Đến cuối cùng vẫn là cái pin — cái pin sẽ là cái biến cuối. Các biến số bên trong (đan xen, vị trí) sẽ nằm vào trong đấy."*

Vũ kể: làm Match-3 ngày xưa từng viết bot test level — bot không biết design — đi nước theo % để ra kết quả phân nhóm user. *"Cùng với một logic test, kết quả khác nhau như thế nào."*

---

## Fake User Trong Internal Testing

Câu hỏi: làm sao tester nội bộ test được difficulty khi đã quá quen game?

### Sort Game — Fake Bằng Random

Sort là game decision tree rõ ràng: move cột 1 → 2 lộ ra viên red, move 2 → 1 lộ ra viên green. Người chơi quen sẽ tính trước. Cách fake: *"Mình chỉ có cách là mình giảm độ tinh của mình lại thôi — bấm ngẫu nhiên từ trái sang phải, một cách ngẫu nhiên và không để ý cái ở dưới."*

### Platformer — Chơi Ngược

*"Khi mình gen map xong, mình cho tester chơi ngược từ cuối lên. Sau đó tới lần thứ 3 mình bắt lại chơi xuôi từ dưới đó — lần chơi thứ 3, feeling của họ vẫn là như người mới từ đầu."*

### Số Lượng Level Test ≠ Số Level Design

Trong 20 level designed → chỉ 5 level đẩy cho test team. Lý do: thứ tự bị tráo, để habit không hình thành. *"Mình tráo ngược lại cái thứ tự của trước lần sau, để cho họ bị phá hết tất cả những cái thói quen cũ."*

### Giang's Approach — Outsource

Không dùng nội bộ test difficulty — *"Bên mình thì là tester thì không có vai trò test về độ khó."* Tester chỉ test bug/UI. Difficulty/content cảm nhận → đẩy quảng cáo trăm đô / nghìn đô, nhìn data từ user thật, rồi feedback ngược lại.

---

## Hidden Variables — Điều Chỉnh Khó Sau IAP

Bài toán: user IAP → level dễ đi → user hardcore mất challenge → bỏ. Làm sao tăng khó lại sau IAP **mà user không nhận ra**?

### Loại 1 — Biến Trên Mặt (Không Khuyến Cáo)

Số mu hiển thị, thời gian → user sẽ phản ánh "tại sao có 20 mu tao có 18 mu?". OK với game không có video quay leo top, nhưng risky.

### Loại 2 — Biến Ẩn (Khuyến Cáo)

- **Freestyle ratio** — phần random fill (Match-3) → giảm tỷ lệ favorable.
- **Drop rate** — tỷ lệ hạt khác nhau.
- **Mix density** — pattern phân tán màu/chip xen kẽ nhau như thế nào.

### Loại 3 — Distract (Cẩn Trọng)

Không phải tăng khó thật mà tăng cognitive load:
- **Đổi tông màu** — level 6 day → level 7 night (hoặc đảo). Effect dễ/khó nhìn hơn.
- **Đổi color palette** — từ basic (xanh đỏ tím vàng) → same-tone (các màu sang sang nhau, khó phân biệt). User phải dồn focus → perceived difficulty tăng dù level data không đổi.

Quote: *"Lúc đấy cái độ khó của level chơi nó không được quyết định bởi level design bằng data, mà nó tăng độ khó lên bởi vì độ phân biệt về màu sắc của mọi người. Cái này là hoàn toàn cá nhân — có người sẽ thấy khó lên, có người vẫn cảm thấy nó xịn hơi khó lắm chút thôi."*

### Game Reveal-Map vs Hidden-Map

- **Platformer / hidden map** → nhồi khó vào freestyle section (user không nhìn thấy trước).
- **Match-3 / fully revealed board** → khó hơn vì state show hết → ưu tiên biến ẩn / distract.

---

## IAP Design — Why People Pay

Vũ phân tích các động cơ IAP, ý chính: *"Làm thế nào để người ta giải quyết vấn đề liên tục — khi người ta giải quyết vấn đề liên tục thì người ta mới phát sinh IAP liên tục."*

### Drivers IAP

- **Giải quyết vấn đề** (battle game): user stuck với boss → mua chỉ số ATK → vượt → next problem.
- **Time-starve solve** (idle game): không có thời gian cày → mua hạt / tăng tốc.
- **Aesthetic / Skin** — mua vì đẹp, không cần solve gì.
- **Social validation / Leaderboard** — *"Trong leaderboard ai vượt qua nhiều level nhất, sâu về trước mặt tất cả mọi người. Con người luôn có tư duy là không có kém bất kỳ ai — đặc biệt là khi họ đã hòa vào con game của mình rồi."*
- **Phá giới hạn bản thân** — buzo game, ASMR no-fail: *"Tôi luôn muốn vượt qua giới hạn của bản thân mình — phải nói chí tuệ về bất kỳ một cái gì."*
- **Rich user mua vô tư** — *"Cứ thích thì mua. Mục tiêu là quay tiktok."*

### Continuous Friction Pattern

Buzo (con micro-pack): mỗi vấn đề nặng nhỏ nhưng liên tục → nạp liên tục, không nạp 1 cú lớn. *"Cái lượng nặng của nó rất nhỏ nhưng nó lại nặng nhiều — nó nặng liên tục nhiều."*

---

## Định Giá IAP Theo User Value

### User Value Formula

```
User value (USD) = thời gian chơi (phút) × giá phút (USD/phút theo quốc gia)
```

Ví dụ: 100 phút × 0.1 USD/phút = 10 USD → user "balance" = 10 USD. Gói IAP định giá tương đương 10 USD = 1000 V (V = currency in-game).

### Sai Lầm Định Giá — Bán Sai Đồng Tiền

Case Giang bán hero pack 10$:
- Hero pack thực ra đè được 300$ giá trị journey trước mặt (user mua hero này, đi qua 300$ worth of content trước khi cần next pack).
- Bán 10$ → user "đi từ đây đến đây phải bỏ 300$ thì em đang bán giá 10$, tức em đang cất bằng sai đồng tiền."
- Hậu quả: user mua xong đi dài quá → designer chưa kịp set next paywall → IAP velocity giảm.

Quote: *"Cái sỉ số của Halo nó phải tương đối với cái chuyện cho người ta đi một đoạn xong người ta mới phải đi tiếp content của em — chứ đừng để cho người ta đi một đoạn dài quá."*

### Buy7 1.8% Cao — Nhưng Progress Mất Cân Bằng

Buy7 = % user mua sau D7. 1.8% là rất cao (con bắn máy bay Inhalt cao nhất là 0.07%). Tuy vậy có thể signal *"em cân bằng progress người chơi chưa tốt — nó đang mua nhiều của T0, T1, T2 (gói tier thấp), chỉ trôi đến T5 là hết, dừng lại luôn."* Buy7 cao nhưng later-tier IAP không scale → game mỏng.

---

## RPG Unit Design — Nguyên Tắc "Phải Có Điểm Yếu"

Trả lời cho Giang về dòng tower-base có hero/unit:

> *"Trong nguyên tắc thiết kế RPG, tuyệt đối là con nào làm ra phải có điểm yếu. Bởi vì cái điểm yếu chính là cái mà khiến em mua con này rồi phải mua con khác. Và thiết kế level cũng phải theo điểm yếu và điểm mạnh của từng con — nó là cái khởi tạo ra đề bài tất cả mọi thứ."*

### Vũ Phân Tích Con Tướng Của Giang

- Đam to / AoE / tốc độ công nhanh.
- "Không có điểm yếu một câu."
- → unit này là $300 unit, không bán 10$ được.
- → designer phải làm next unit big-3 hơn → leo cảm xúc → fueling sai.

### Nguyên Tắc

- Mỗi unit S-tier ở 1 hệ (1 mode chơi), C/B ở các hệ khác.
- Bot vs quái là 2 hệ riêng → 1 unit không thể S cả 2.
- Multi-class system phải plan ngay từ đầu — *"Em đã phải tuning ngay từ đầu về các từng cái unit hoặc là từng cái hệ của từng class. Người ta mới có định hướng — tao sang map mới, con tướng này của tao sẽ bị counter, sẽ yếu đi, hoặc bị con khác counter lại."*

Hỗ trợ design level theo điểm yếu unit:
- Map A spawn quái mà tướng X mạnh → user dùng X.
- Map B spawn quái mà tướng X yếu → user phải mua tướng Y mới qua.

Quote bài học: *"Không phải đến lúc em có số liệu drop để em làm — phải tuning chôn ngay từ đầu."*

---

## Retention vs Session Length — Cắt Hay Không Cắt?

Câu hỏi từ học viên: *"Level design càng tốt → retention càng cao. Nhưng nếu user chơi lâu thì mệt → retention giảm. Có nên cắt session để user không kiệt sức?"*

### Case Study 1 — Idle Game (Thất Bại Cắt)

Tham số ban đầu:
- Session: 40 phút.
- Day retention: 1.5%.
- Tỷ lệ View ad: thấp.

Thử nghiệm:

| Lần | Action | Kết quả |
|-----|--------|---------|
| 1 | Cắt section → 2 phút mỗi đoạn, chặn paywall cứng, nhồi reward cho ngày sau | Session/đoạn 28% → 37%. Nhưng tổng thời gian/ngày 60 → 55 phút |
| 2 | Cắt nhỏ hơn nữa | Cùng pattern: section tăng, tổng giảm còn 56 phút |
| 3 | Bỏ cắt. Thêm level goal, level bonus, đổi hình ảnh trong level | Session 45 → 46 phút, tổng 65 phút |

Kết luận: idle game này không scale được retention bằng cắt. *"Một thí nghiệm là một thành công — không mang lại giá trị nhiều cho level design."*

### Case Study 2 — Tower Defense (Thành Công Cắt)

Con tay đi vét tổng:
- Trước: session 20 phút, 4.5 session/ngày.
- Cắt: 10 stage → 5 stage × 2 map, map thay đổi giữa các stage.
- Sau: session 17 phút, 7 session/ngày, tổng >100 phút.

### Quy Tắc Rút Ra

- **Game IAP-heavy** → muốn user chơi càng lâu càng tốt, càng nhiều friction càng nhiều IAP.
- **Game ad-heavy / survival** → cắt vs không cắt tùy đặc thù, không có công thức.
- **Build for max length trước, cắt sau** — *"Cứ làm con game chơi nhiều nhất, sau chúng ta sẽ bàn nhau cắt."*

Vũ priority metrics (thứ tự ưu tiên):
1. **A-B-B** (số 1, không bàn cãi).
2. **Investment** (xem quảng cáo / inter ratio).
3. Retention không phải metric quan trọng nhất — *"Anh không cảm thấy việc retention tăng được quá nhiều. Có những trường hợp mình làm retention tốt thì tăng lên được, có những trường hợp không."*

---

## Câu Hỏi / Chủ Đề Còn Nợ

- **Cách level design hợp với UX của IAP gating** → Doc 6 (UX).
- **Multi-class system trong RPG / unit tuning chi tiết** → không nằm trong khóa, Vũ note "khóa này không có phần RPG sâu".
- **Tower defense corner placement design intent** → mention but not deep-dive.

---

## Thuật Ngữ Buổi Này

- **Level Data** — design level bằng số trên Excel/Grid.
- **Level Set Time / Xếp Tay** — design level bằng cách đặt object thủ công trong Unity.
- **File Tiêu Chí** — định nghĩa content + target metrics của level trước khi thiết kế.
- **File Ý Đồ** — design intent doc kèm lộ trình và cách triển khai.
- **Ball Nut** — phần random fill trong board Match-3, không phải combo prepared.
- **Pattern Habit Break** — kỹ thuật tạo độ khó bằng cách phá thói quen user sau 3 level tạo pattern.
- **First-Look User** — user nhóm impulse, pick visual to nhất trước.
- **Logic User** — user nhóm tính toán cascade.
- **Mắc Kém User** — user nhóm scattered, không theo logic, win-rate thấp nhất.
- **Profile-Based Skill** — skill user tăng theo profile, bù vào difficulty curve.
- **Hidden Variable** — biến ẩn (drop rate, freestyle ratio, color palette) dùng tune khó mà user không nhận ra.
- **Distract Variable** — kỹ thuật tăng cognitive load bằng đổi theme/màu, không thực sự đổi data.
- **User Value** — định giá user theo (phút chơi × giá phút theo quốc gia).
- **Cất Bằng Sai Đồng Tiền** — IAP định giá sai so với journey-value mà gói mở ra.
- **Buy7** — % user mua IAP trong 7 ngày đầu.
- **A-B-B** — metric ưu tiên số 1 của Vũ (chưa giải nghĩa trong buổi, có thể là ad-based behavior metric).
- **Investment Metric** — số quảng cáo xem / thời gian.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Transcript thô: `GD Doc 4  (IPhone).mp3.txt` (3,559 dòng, ~125KB)
- Subtitle timestamp: `GD Doc 4  (IPhone).mp3.srt`
- Audio gốc: `GD Doc 4  (IPhone).mp3`
- Vị trí trong khóa: theo curriculum là **Buổi 6 (Level Data)**, ghi âm thứ 4 do được đảo lên dạy sớm sau Doc 2.
- Khóa học: Game Design Course by Negaxy + IEC (8 buổi).
