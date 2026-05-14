---
title: "GD Doc 2 — Level Design & Feeling Game (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 2.mp3"
date_added: 2026-05-13
tags: [video, course-transcript, game-design, level-design, match-3, monetization, liveops, mobile-games, vietnamese]
aliases: ["GD Doc 2", "Buổi 2 Game Design Course", "Level Design Vũ Hiệp"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-01]]"
  - "[[gamerefinery-match-3-code-part-2]]"
  - "[[linkedin-tandon-match-3-code-part-1]]"
summary: "Buổi 2 khóa Game Design (Vũ + Hiệp): bóc tách solution tạo độ khó level Match-3, thuật toán spawn chip, file ý đồ, giới hạn phần cứng cho asset, depth vs breadth, inter:reward ratio, phương pháp test A/B từng biến cho LiveOps."
---

# GD Doc 2 — Level Design & Feeling Game

**Speakers:**
- **Vũ** — Lecturer chính (xưng "mình"/"anh", người dẫn buổi)
- **Hiệp** — Co-lecturer (được mời chia sẻ thêm cuối buổi)
- **Giang** — Học viên có dự án thực tế đang vận hành (nhiều dòng game level-base, hỏi nhiều)
- **Quân** — Học viên (con full spin / merchandise puzzle)

**Format:** Buổi học trao đổi 2 chiều, ~150 phút, tiếng Việt. Có nhắc lại nội dung Doc 1 (tài sản — assets) và đặt nợ một số câu hỏi cho Doc 6 (Level data) và Doc 7 (Style/UX).

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 2.mp3.txt` (~3,417 dòng, 19k từ; chunks 000-008 đã ghép, head/tail hallucination đã trim).

---

## Tiếp Nối Doc 1: Đánh Vào Feeling Của Tài Sản

Vũ chốt phần tài sản (asset) của Doc 1 bằng cách dịch chuyển từ "đặc tính tài sản" sang **cách đánh vào feeling của tài sản**:

- **Số lượng** — ai cũng muốn nhiều. Quyết định: reward cho nhiều hay ít, gói IAP bán nhiều hay ít?
- **Chất lượng / Phân cấp** — game có Legendary đến Common thì bán cấp nào?
- **Khan hiếm**:
  - **Tự nhiên** (cap cứng).
  - **Theo progress** ("level 50 nó không hiếm nữa") — có thể bán cho người mua sớm để leapfrog.
- **Achievement** — bày ra home, hoặc nhét trong "trên mình riêng".
- **Khoe tài sản** — game farm bày tài sản (tượng lợn vàng, nhà tráng tác dụng) lên đất để khi người chơi khác thăm thì thấy "mức độ giàu có, mức độ cống hiến cho game".
- **Giá trị tăng theo thời gian** — đặc tính nhóm game đặc thù, ít dùng nên bỏ qua.

Quote khoe tài sản: *"Vì sao đánh vào yếu tố tài sản? Nên lúc trước mình nói: khi các bạn list hết tất cả yếu tố liên quan con game ra, thì các bạn sẽ làm được cái này."*

---

## Solution Tạo Độ Khó Level — 5 Yếu Tố Cốt Lõi

Vũ yêu cầu học viên liệt kê *"có bao nhiêu cách để làm tắc một level"*. Kết quả tổng hợp (cho Match-3 / Candy Crush style):

1. **Giới hạn tài nguyên** — time, số mu (moves).
2. **Obstacle / mật độ chướng ngại** — số lượng và phân bố vật cản trên board.
3. **Bài trí ban đầu** — cách xếp object ở thời điểm start level.
4. **Mục tiêu** — số lượng goal cần đạt.
5. **"Tắc ẩn"** — thông qua thuật toán sinh chip + drop rate + logic reveal key object (tắc không thông qua 4 yếu tố trên mà thông qua RNG có chủ đích).

Quote: *"Tại sao trong vòng lần 1, lần 2, lần 3 các bạn chơi không qua, lần 4 các bạn lại qua? Vì bước đi nó khác. Khi mà set up ban đầu, tất cả các đoạn chip — các viên nhỏ nhỏ — bản thân các chip đấy sẽ chỉ được sinh ra theo tỉ lệ và sinh ra theo bố cục."*

---

## Thuật Toán Spawn Chip Trong Match-3

Khi quy đổi "user view" sang "game design view", học viên đề xuất:

- **Limit màu** — mỗi level chỉ dùng 1 subset màu của full palette.
- **Bias ô liền kề** — muốn dễ thì cho ô trên (tầng XI+1) khác màu với ô dưới (XI), tăng khả năng combine.
- **Tỷ lệ drop từng màu**:
  - 5 màu đều 20% → khó nhất (xác suất match đều thấp).
  - Lệch tỷ lệ → dễ hơn.
- **Thay tỷ lệ trong cùng một level** — khi user mua thêm moves (bằng tiền/quảng cáo) phải đảm bảo cho thắng, nếu không user bỏ. *"Phải cho nó thắng, không nó bỏ mẹ em đi."*

Logic adaptive key object (case Candy Crush):
> *"Có 5 object cần thu. Object thứ 5 chỉ xuất hiện khi còn 10 nước đi. Nếu lần 1 fail dưới 10 mu, lần sau cộng 5 mu (15). Nếu lần 2 vẫn fail, lần 3 cộng tiếp 5 mu. Bao giờ người ta thắng được thì xuất hiện sớm hơn nữa."*

Vũ note: viết logic spawn riêng chỉ phần đó cần "4-6 trang" cho code làm.

---

## Giới Hạn Phần Cứng — Trade-off Cho Asset

Vũ kể bài học từ game chiến thuật 3D ngày xưa:

- Thiết bị tham chiếu: ~200k chip giới hạn (iPhone đời cũ).
- Yêu cầu level design: 100 vs 100 quân.
- Art làm chi tiết: mỗi con ~15k chip.
- Math: 200 con × 15k = 3M chip → vượt giới hạn 15 lần → game crash.

Pattern fix:
- Cắt khớp ít hơn (slider zombie 20 đốt → 6 đốt).
- Thay đổi logic ăn point: trước 5 điểm = 1 đốt mới. Sau: 5 điểm → 10 → 50 (ăn theo lộ trình tăng dần).
- Giữ first impression: lúc onboard hiển thị "fill 20 con" nhưng late-game cắt khớp dần.

Quote bộ giáp Wukong: *"Ảnh tản nó cũng sướng, mẩn cho đôi tuần một cái. Xong lên nó mặc, mặc được cái áo để game còn chạy được. Mặc thêm cái quần là game đứt — crack luôn."*

**Nguyên tắc**: GD phải set giới hạn ngay từ đầu (target device: iPhone 7 vs 15), không phải để team art tự định.

- 10 vs 10 → level design theo **chiều sâu**.
- 30 vs 30 → level design theo **chiều rộng**.

Bài học giảng viên rút ra: *"Các bạn đã đè một cái nhà 10 tầng lên trên một cái móng chỉ có 3 tầng thôi. Bây giờ ông code làm thế nào?"*

Bonus: 2D cũng dính — quá nhiều khớp trong một màn hình → lag không optimize được.

---

## Game Ngắn Hạn vs Dài Hạn

LifeTV đo bằng CPI ở thời điểm khác nhau:

- **Ngắn hạn**: D1, D2, D3. *"Vẽ thoải mái — tăng/bằng/giảm gì cũng được, miễn không giảm đi."*
- **Dài hạn**: D7, D14, D30, D60. Phải nghĩ rất rõ về 2 chiều mở rộng:

### Chiều Sâu (Depth)

Cùng core mechanic, chỉ tăng độ khó:
- Match-3: 1000 level, tăng độ khó bằng cách thêm màu / giảm số move / giảm time.
- RPG: combat → win → upgrade hero → next map. Không có PvP, không bang hội, không event.

### Chiều Rộng (Breadth)

Thêm modes / systems:
- PvP, Arena, bang hội.
- Mode đánh boss riêng.
- Mode đảo mới với skill mới hoàn toàn.

Quy tắc Vũ đưa ra: *"Định nghĩa MTV thì chỉ thiết kế đến đó thôi. Không thêm gì cả, không nghĩ đến tính năng gì cả. Hãy làm tốt nhất để nó ra cái này."*

---

## File Ý Đồ — Thiếu Sót Phổ Biến Của Designer

Phần Vũ nhấn mạnh nhiều nhất trong buổi. File ý đồ là cái "mọi người rất hay thiếu khi làm data."

### Lộ Trình Content

```
CT1: object {1, 2}
CT2: object {1, 2, 3, 4}  // 1,2 carry over, 3,4 mới
CT2.1: focus trọng tâm object 3
CT2.2: focus 1,2
CT2.3: 3,1,2 mix
```

### Tiêu Chí Thời Gian Mục Tiêu

Đặt mục tiêu time-to-complete trước khi thiết kế:
- Đầu chapter: 20s.
- Chapter 2: 35s.
- Chapter 3: 80s.

Khi design xong test thực tế, đối chiếu — nếu lệch quá thì biết hướng để sửa.

### Tiêu Chí Số Mu Hiển Thị vs Hardcore

Pattern hệ thống "ép" độ khó dần qua replay:
- Level đầu: hardcore = 10 mu, hiển thị = 40 mu → 100% win, build trust.
- Mid: hardcore = 15, hiển thị = 20 → tỷ lệ thắng/thua bắt đầu thay đổi.
- Late: hardcore = 18, hiển thị = 20 → tỷ lệ reward / draw thay đổi mạnh, ép user vào funnel.

Quote: *"Khi em fix lúc ban đầu, em cần 10 mu để qua, em để thực tế là 40 mu — 100% sẽ thắng. Đến level tiếp theo, cần 15 mu thì cho 20. Đoạn sau nữa, hardcore là 18 mà hiển thị 20, lúc này tỷ lệ reward thay đổi rất nhiều."*

### Lý Do Pick Level Cho Event

Khi Quân nói "đặt yes ở level 8, 18, 28...", Vũ hỏi *"vì sao"* — đáp án phải đến từ phân bổ ad density / engagement time, không phải đoán:

```
Ad target = 10 ads/day
Time engagement = 20 phút
Level time = 1 phút → ~20 trận/session
Density inter:reward = X:Y
→ Suy ra placement của từng "yes" trên trục level.
```

---

## Inter : Reward Ratio (Y:R)

Vũ và Hiệp đồng quan điểm fix tổng số ad/day để giữ retention ban đầu:

- Target inter:reward ratio (ví dụ): 7:3.
- Thực tế đo được: 8:2 (nhiều inter, ít reward).

**Hai cách phản ứng (không có đúng/sai, là A/B test):**
1. Duy trì 8:2 nếu metrics OK.
2. Điều chỉnh về 7:3 bằng cách *"làm level khó hơn lên và yêu cầu ép vào reward"* — buộc user xem reward để qua.

Lỗi pattern: *"Em nói là để cho user nó chơi nhiều hơn thì em muốn làm nó dễ đi. Tức là nếu em làm khó lên thì thời gian chơi sẽ tụt xuống, nhưng reward sẽ tăng lên — không chắc làm tăng R tầm."*

---

## Test Methodology — Một Biến Tại Một Lần

Vũ cảnh báo anti-pattern thay đổi nhiều biến cùng lúc:

- Đừng cào cả 20 level lên cùng một lúc.
- Pick 1 level (e.g., level 5), tạo 2 phiên bản: dễ hơn + khó hơn. Phần còn lại giữ nguyên.
- Sau khi pick được nhánh thắng → bắt đầu test biến tiếp theo từ từ.

Quote: *"Ông nào máu phát sữa khó tất cả cái level này lên cùng với nhau thì không ra kết quả. Phần còn lại các bạn để nguyên, test senpai thì không dơ là thay đổi nguyên."*

Tách thay đổi UI và level design ra 2 product khác nhau nếu cần — không mix trong 1 game (vì khi user học UI mới + level mới cùng lúc thì không phân tích được nguyên nhân drop).

---

## Tower Defense Case — Khó Hơn Có Thể Tốt Hơn

Câu chuyện Vũ kể (counter-intuitive):

**Triệu chứng**: Tỷ lệ reward/inter rất cao, nhưng tổng số inter thấp → user chơi ít.

**Diagnosis sai (intuitive)**: Khó quá không chơi được → làm dễ đi.

**Hậu quả khi làm dễ**:
- User xem reward để lấy tài sản.
- Tài sản dùng không thấy tác dụng (vì level đã dễ rồi).
- Mất mục tiêu phấn đấu → bỏ game.

**Fix thực tế**: Tăng độ khó → tài sản trở nên hữu dụng → revenue tăng.

Quote: *"Mình không hề khẳng định với các bạn là sẽ làm khó lên hay là dễ đi thì sẽ ra tiền. Mình chỉ nói là các bạn nên thử test khó lên hoặc dễ đi, sau đó đưa ra định hướng."*

---

## Phân Tập User: User Giá Rẻ vs Giá Cao

Hiệp bổ sung: tăng/giảm độ khó tùy vào tập user UA đang convert:

- **User giá rẻ** (low-difficulty preference) → giảm khó → đúng.
- **User giá cao** (high-difficulty preference) → tạo level khó là điểm phát sinh IAP / keyword tìm kiếm → giảm khó là sai hướng.

Trao đổi với marketing/UA: GD phải biết tập user mình đang convert là loại nào trước khi balance level.

---

## Replay Rate Distribution — Phân Cực Nguy Hiểm

Phân tích sâu hơn metric "replay rate trung bình":

- Average = 1.3 lần/người không đủ thông tin.
- Cần biết phân bổ:
  - **Tập trung (1.2-1.4 là nhiều nhất)** → 1.3 đại diện được, sửa 1 hướng OK.
  - **Phân cực (1.1 và 1.5 nhiều nhất)** → game đang phục vụ 2 loại user khác nhau:
    - Sửa khó lên → đội 1.5 vất vả → tụt cao.
    - Sửa dễ đi → đội 1.1 chán → bỏ.
  - Giải pháp: **tách thành 2 sản phẩm**, không mix.

---

## Tách User → Tách Sản Phẩm

Anti-pattern: gắn "mode khó" thứ 2 trong cùng một con game dễ.

> *"Mấy con dễ đấy có riêng 1 mode chơi khó, 2 mode luôn. Nhưng khá là ít người chơi sang mode 2 đấy."*

Vũ note: sẽ explain ở Doc 7 (UX) tại sao user không chuyển mode.

Approach Giang đang làm:
- Tách core system giống nhau thành 2 con game: một UI ratio 0.18, một 0.13.
- Cả 2 đều cho metric tốt riêng.
- Trước đây mix 2 vào 1 (kéo 0.13 lên 0.18 trong cùng game) → user "học UI cũ rồi học UI mới → sai" → fail.
- *"Vì anh chỉ thay đổi phần level design thôi mà — đừng thay đổi cái gì khác, nếu không thì anh sẽ không đánh giá đúng."*

Một hướng IAP-leaning (~50% IAP), một hướng IAA-leaning (~20% IAP) — không phải đen-trắng.

---

## Whale Content Burn — "Bố Chơi 5 Ngày Hết Sạch"

Case Giang chia sẻ cuối buổi:

- Lượng content thiết kế: cần ~30 ngày cho user trung bình.
- Whale ngày D2 nạp 400$ → burn hết content trong 5 ngày.
- Đến D7: *"Bố biết hết rồi. Mày để content cho ta đi. Khó chịu."* → metric tệ.
- Vấn đề muốn giải: gating content theo time-pacing kể cả khi user willing-to-pay cao.

---

## Difficulty Curve Cổ Điển Đã Lỗi Thời

Hiệp chia sẻ về **difficulty curve** (khái niệm 2015):

- Định nghĩa lý thuyết cho game art truyền thống.
- Bị các dòng game mới (ASMR, no-fail games với 10M+ downloads) phá bỏ — *"Bạn có thể chơi những con game không thua bao giờ, vẫn vui."*
- Approach thực dụng (Hiệp đề xuất):
  1. Vẽ một kế hoạch ban đầu (biểu đồ + tiêu chí).
  2. Đo magic / chỉ số.
  3. Nắm chỉnh từ data, không tranh luận giáo điều.

Quote: *"Mấy ông làm game 3A trong nhà chỉ vật nhau ra để đấm nhau, không có gì đo đạt đâu. Ôm một quả bom 7-8 năm xong các ông ra nổ — nổ giòn thì các ông giỏi, xịt thì chui vào hang."*

---

## Level Content vs Level Data

Hai trục thiết kế level cần tách:

- **Level Content** — thêm element mới, đa dạng câu đố, tạo feel mới mẻ (không cần skill).
- **Level Data** — tăng/giảm số mu, scale up độ khó.

Game có thể mix cả 2 (vd. con "Vulnerability" của Giang — content + data trong cùng 1 level).

Mix → control khó hơn nhiều: *"Không biết thời điểm này nên thêm content mới vào, hay là tăng độ khó với content hiện có. Cùng lượng content giải cứu 2 công chúa thì giảm số mu để khó hơn, hay tăng từ 2 lên 3 công chúa?"*

---

## Bài Toán Của Giang — IAA → IAP Migration

Case study chính của buổi:

- Dòng game level-base, ngày xưa làm IAA → cố làm dễ + đắp content → revenue OK qua quảng cáo.
- Hiện tại cộng đồng/team muốn chuyển hướng "chất lượng hơn" → làm khó → user drop → kinh doanh kém.
- Vũ & Hiệp đáp: cần data + biết tập user UA → không thể mentor mà không xem context.

Câu chuyện Vũ kể đối chiếu: con Dogo (k×k game) — level 1 cực dễ 3 bấm, level 2 cho 300 mu nhưng dùng không hết. Chỉ thua bằng cách bắt user xem reward để mở slot mới. *"Đang trong một vùng bị mờ — không hiểu tư duy nào ở giữa mà ông ấy nghĩ ra như thế."*

Giang đang test: detect user pattern → server-side push (hết 10 reward thì đẩy sang tech 2 — thay vị trí reward bằng vị trí IAP) → vừa khai thác IAP vừa không lậu.

---

## Art Direction — Giới Hạn Của Game Designer

Trả lời câu hỏi của Giang về "feeling theo team" (Candy Crush fun-fun vs Harry Potter dùng giận, huyền bí):

- Đây là **Feeling theo team** — văn hóa, hợp gu user khác nhau.
- Việt Nam: game Tam Quốc / Võ Lâm OK; game Manga không OK — văn hóa tiếp cận.
- Wonka case: cùng IP "Wonka of Candy" (Zynga 84k rating) nhưng nhiều style art khác nhau cho thị trường khác nhau.

**GD ≠ Art Director:**
- GD chỉ cần mô tả ở mức "màu triangle vs màu quang" (triangle color scheme vs analogous color scheme).
- GD chỉ cần biết từ khóa feeling (cartoon, kinh dị) và đưa cho AD.
- Đừng làm thay AD — *"Phân tích sơ xài và phân tích sơ xài là không đúng như bạn tự chịu. Bạn phân tích được ở mức độ đủ hoặc sâu để họ tiếp tục được."*

Sẽ deep-dive ở Doc 7 (Style).

---

## Câu Hỏi Còn Nợ (Tham Chiếu Buổi Khác)

- **Cắt khớp & chất lượng đồ họa** — khi nào cắt được, khi nào không → Doc 7 (UX).
- **Tại sao user không chuyển sang mode 2 trong cùng game** → Doc 7 (UX).
- **Style / Art direction sâu** → Doc 7 (Style).
- **Level data deep-dive** → Doc 6.

---

## Thuật Ngữ Buổi Này

- **MTV** — metric mục tiêu của sản phẩm (ROI / monetization target validated by CPI).
- **CPI** — Cost Per Install (chi phí thuê 1 user). Là barometer để chia game ngắn vs dài hạn.
- **LTV / LifeTV** — Lifetime Value, đo theo CPI từng mốc D1-D60.
- **File ý đồ** — design intent doc kèm lộ trình + tiêu chí kiểm thử.
- **Inter / Reward (Y:R)** — inter-ad vs rewarded-ad ratio.
- **Tắc ẩn** — pattern block level qua RNG có chủ đích, không phải qua moves/time/obstacle hiển nhiên.
- **Tech 2** — pattern detect user state rồi server-side push UI/UX khác (Giang dùng).
- **Magic** — Vũ dùng theo nghĩa "metric đo đạt được" (cancel với "bay bổng" / cảm tính).

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Transcript thô: `GD Doc 2.mp3.txt`
- Timestamp chunks: `doc2_chunks/chunk_000..008.wav.srt`
- Audio gốc: `GD Doc 2.mp3`
- Khóa học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
