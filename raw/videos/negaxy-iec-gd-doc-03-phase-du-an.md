---
title: "GD Doc 3 — Phase Dự Án: Prototype, MVP & Vận Hành (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 3 - Phase du an.MOV"
date_added: 2026-05-14
date_updated: 2026-05-19
tags: [video, course-transcript, game-design, prototype, mvp, monetization, retention, ux, arpu, iap-packages, habit-formation, mobile-games, hyper-casual, vietnamese]
aliases: ["GD Doc 3", "Buổi 3 Phase Dự Án", "Prototype vs MVP Vũ Hiệp"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-02-level-design]]"
  - "[[negaxy-iec-gd-doc-04-level-data-and-iap]]"
  - "[[negaxy-iec-gd-doc-07-ui-ux-monetize]]"
summary: "Buổi 3 (Vũ + Hiệp + Giang + học viên): phase dự án từ Prototype → MVP → vận hành (Part 1), Q&A UX/retention/ARPU/imba (Part 2), và khung Improve Chỉ Số chi tiết (Part 3) — retention improvement, stack types, 4-phase habit formation, ngắt mềm/cứng, hierarchy reward theo dòng game, win-screen ad tricks, IAP package structure (Basic/Đất bạc/Super/Mắc/Chặn). Phân biệt Prototype vs MVP, test feelings prototype, balance scale, test bản không quảng cáo, định nghĩa lại Inter, D7 hoà dễ scale hơn D3, fueling = pacing khai thác value, ad timing vs skill unlock, trade-off ARPU vs ARPPU cho ERP."
---

# GD Doc 3 — Phase Dự Án: Prototype, MVP & Vận Hành

**Speakers:**
- **Vũ** — Lecturer chính (xưng "mình"/"anh", người dẫn buổi).
- **Hiệp** — Co-lecturer (chia sẻ test prototype không quảng cáo, case giãn inter, D7 hoà, case Tiny Battle/Tiny Kingdom).
- **Giang** — Học viên có dự án thực tế đang vận hành (đưa quan điểm về D7 hoà bền hơn D3; sản phẩm ERP có content tốt).
- **Thiên** — Học viên (đặt câu hỏi về tham chơi vs CPI khi target hyper/bitcoin).
- **Linh** — Học viên (đặt câu hỏi về mục tiêu test ở giai đoạn đầu).
- Một số học viên khác đặt câu hỏi về D3/D7, CTR baseline, level cần cho retention, UX, balance gói tướng.

**Format:** Buổi học trao đổi 2 chiều, ~190 phút, tiếng Việt. Gồm 3 phần:
- **Part 1 (~100 phút)** — Phase dự án: Prototype, MVP, monetization pacing, D7 scale.
- **Part 2 (~45 phút)** — Q&A mở rộng: UX vs UI, hierarchy reward quảng cáo, retention curves, ARPU/ARPPU, imba balance gói meta.
- **Part 3 (~45 phút)** — Improve chỉ số: framework cải thiện retention, stack types, 4-phase habit formation, ngắt mềm/cứng, ad timing, IAP package structure, revenue chart shape cho ERP.

Tiếp nối "feeling của game" từ Doc 1 và đặt nền cho Doc 4 (Level Data) + Doc 7 (UI/UX & Monetize). Có nhắc lại Inter:Reward ratio đã giảng ở Doc 2.

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 3 - Phase du an.MOV` (video gốc, 3.3 GB) + `GD Doc 3 - Phase du an.MOV.txt` (transcript đầy đủ 4,318 dòng, faster-whisper large-v3 chunked, 20×10-phút chunks với beam=1 fallback, re-run 2026-05-18 — ~3× content so với run 2026-05-15).

---

## Tiếp Nối Doc 1: Xác Định Mục Tiêu Trước Khi Test

Vũ mở buổi bằng việc rà lại từ Doc 1 — "feeling của game" và những vấn đề có thể phát sinh trong vận hành. Trước khi nói về phase prototype, người dẫn yêu cầu liệt kê **những thứ cần xác định trước khi đẩy sản phẩm ra test**:

- **Performance** — game chạy mượt không, có vượt giới hạn phần cứng không.
- **Gameplay** — logic cốt lõi có hoạt động, có truyền đạt được không.
- **Tập user** — phân loại tập in-house và tập user thị trường, ai phù hợp với game này.
- **Tính năng chính** — feature list tối thiểu để chứng minh idea.

Vũ phân chia thị trường thành 2 nhóm theo cách test:

- **Bên làm game tập trung phi thẳng ra thị trường** — không qua xác định mục tiêu nội bộ, ship trước rồi sửa sau.
- **Bên làm game cẩn trọng** — phải xác định mục tiêu trước, *"thực tế mình có làm được nó không"*.

Trao đổi xoay quanh việc khi nào cần phase nào và biên độ chi phí mà công ty chấp nhận trả cho mỗi phase.

---

## Prototype vs MVP — 2 Bản Khác Nhau

Phần định nghĩa cốt lõi của buổi. Vũ nhấn rõ:

> *"Pro-time và MVP là 2 bản khác nhau nhé. MVP là gì? Minimum Value Product — tức là cái bản mà các bạn có thể cho user chơi được, nhưng mà nó nhỏ hết có thể. Còn bản pro-time chỉ là bản thử nghiệm thôi."*

### Prototype

Bản thử nghiệm phục vụ truyền đạt ý đồ trong nội bộ:

- Cho user hiểu mặt gameplay.
- Cho team, cho sếp hình dung được *"cái thứ ông nghĩ ra, ông nói ra, ông viết ra — trông mặt mũi nó ra làm sao"*.
- Bản chất còn rất sơ khai — graphics có thể chỉ là khối tròn, animation chưa hoàn thiện.

Mục tiêu duy nhất quan trọng nhất: *"Làm thế nào để hiểu, truyền đạt ý nghĩa của gameplay — để cho mọi người cùng nhau xem và đưa ra được comment ý kiến."*

### MVP

Bản đẩy ra thị trường để thu data thật:

- Đã đủ gameplay loop để chơi được.
- Đủ "hết có thể nhỏ" — vẫn là minimum, không full feature.
- Dùng để test trên tập user thật, không phải nội bộ.

Vũ note: nhiều nhóm Việt Nam đang lẫn lộn 2 bản này — đẩy prototype ra test thị trường (sai mục tiêu) hoặc làm MVP ôm quá nhiều feature (kéo dài thời gian).

---

## Feelings Trong Prototype — Vì Sao Test Khó

> [!info] Đính Chính Transcription
> Bản cleaned.txt cũ phiên âm là "Fueling" trong section này — bản large-v3 mới phiên âm 3 lần liên tiếp là **"Feelings"** ở cùng đoạn (dòng 45-47 transcript). Theo ngữ cảnh, Vũ đang nói về **cảm giác chơi game** (gameplay feel) — chứ không phải "fueling" theo nghĩa monetization. Từ "fueling" thật sự xuất hiện sau (dòng 576, context monetization pacing) — xem section *Fueling — Pacing Khai Thác Value* bên dưới.

Test feelings trong prototype hơi đặc thù — verify được gameplay feel ở mức độ core nhưng không xa hơn được. Vũ minh hoạ bằng battle simulation cho con game card battle đá bóng (codename "S3" cũ):

- 11 cục tròn (cầu thủ) bên này, 10 cục bên kia.
- Phân loại bằng chỉ số + màu (xanh — bình thường, đỏ — Legend, tím — Epic).
- Bấm auto cho 2 đội đánh nhau → xem có tự generate được một trận bóng không.
- Có tự ghi bàn, kết thúc trận, đá penalty — *"là đủ xong được một cái nghi thức của Prototype."*

Tại sao feelings khó test sâu trong prototype:

> *"Feelings đoạn này test sẽ hơi khó. Không phải đơn giản — bởi vì feelings này chỉ feelings đúng ngõ độc của cái gameplay thôi. Các bạn chưa nhìn thấy level design trông mặt mũi nó ra làm sao, các bạn cũng chưa nhìn thấy hình ảnh của con game nó chạy mức độ mượt mà như thế nào cả."*

Battle simulation chỉ test được **logic gameplay** + **feel cốt lõi** (có vào trận đấu được không, có kết thúc được không). Performance không kết luận được — bản chất performance phụ thuộc rất nhiều thứ bên ngoài bổ trợ (animation, asset 2D vs 3D, va chạm vật lý). Toàn cảnh feel (visual + audio + responsive) phải chờ MVP để đo trên user thật.

---

## Prototype Là "Cái Base" Cho Comment

Ý nghĩa thứ hai của prototype: làm base để team đập vào comment, từ đó hình thành scope và item list cho MVP.

Khi prototype lên kệ, các nhánh comment thường gặp:

- **Cách thức triển khai** — game theo hướng châu Âu vs châu Á, art style nào hợp gu user.
- **Scope** — 2D vs 3D, số lượng object, mức độ chi tiết per object.
- **Item mở** — game sẽ có những loại tài sản nào.

Ví dụ một battle bóng đá có thể có 3 hướng triển khai gameplay:

- **Auto hoàn toàn** — user chỉ xem.
- **Auto có skill** — auto vận hành, user bấm sẵn skill trước trận, chỉ số tăng theo skill picked.
- **Auto có chỉ đạo** — user can thiệp vào logic trận đấu: *"yêu cầu tất cả người thủ về rồi lên công đi, rồi lên thủ đi."*

Vũ phân biệt 2 nhánh:

- Auto có skill → can thiệp vào **chỉ số** cầu thủ.
- Auto có chỉ đạo → can thiệp vào **logic** trận đấu.

*"Đây chính là cái base mà mình nói tới."* Prototype giúp lock định hướng — sau đó MVP mới biết build theo nhánh nào.

---

## Scope — 2D vs 3D, Form & Tổ Hợp

Sau khi base định xong, scope mới được tính:

- **3D vs 2D** — quyết định toàn bộ pipeline asset.
- **Sự giống/khác giữa các con** — dùng chung form hay 3 form khác nhau, có con to/nhỏ/cao.
- **Tốc độ tháo lắp asset** — mức độ mix tổ hợp đầu/tóc/mặt/mũi/tay là bao nhiêu.
- **Số combo asset** — mỗi form ra bao nhiêu biến thể.

Khi scope rõ, designer mới tính được số chip 3D phải lo, độ phức tạp animation, và quay lại đối chiếu với giới hạn performance đã đặt trong Doc 2.

---

## Balance Scale — Phân Trọng Số Module

Vũ giới thiệu công cụ "balance scale" — sơ đồ phân tỷ trọng tài nguyên giữa các module game.

Cấu trúc:

```
Core gameplay:         50%
Phụ bản:               10%
PvP:                   20%
Sự kiện / đặc thù:     20%
─────────────────────
Tổng:                 100%
```

Mỗi module có trọng số khác nhau. Balance scale dùng để:

- Quyết định bao nhiêu phần trăm tài nguyên phát triển dồn vào core vs vào mode phụ.
- Lock priority khi feature creep — nếu mode mới > 10% trọng số phụ bản, phải cắt bớt thứ khác.

Quy tắc Vũ nhấn: tổng phải đúng 100%, không có module được "thêm vào trên" mà không lấy chỗ từ module khác.

---

## Thêm Tính Năng Mới — Có Ảnh Hưởng Gameplay Không?

Vũ đặt câu hỏi mở: thêm 1 chức năng mới (mode mới, phụ bản, kỳ cuộc) có ảnh hưởng tới core gameplay không?

Học viên trả lời: chỉ là chức năng thêm vào, mở mode mới, hoặc cách thức để cố lệnh kỳ cuộc — **không ảnh hưởng** core.

Vũ chuyển sang ví dụ con số: clear 1 cõi thác → reward 1.000V (currency in-game).

> *"Cho anh hỏi con số 1.000V này làm gì? — Mình sẽ tính toán dựa trên cái mốc để user nó đạt một cái mục tiêu ở đây, ví dụ như khi đến cái đoạn đấy user nó cần 1.000V để nâng cấp kéo. Thì mình sẽ để đoạn đấy thiếu thiếu một chút, xong rồi mình có thể kiểu cắm vào đấy."*

Vũ phản hồi: cách này **không sai nhưng đang chạy một vòng đuổi theo user**:

> *"Cách này khiến cho bọn em đang chạy một cái vòng mà suốt ngày phải đuổi theo với việc là user đang làm cái gì."*

### Giải Pháp — Vẽ Đồ Thị Trọng Số Theo Level

Thay vì reactive (chờ user thiếu rồi cắm vô), proactive bằng cách vẽ đồ thị:

- Mỗi module có trọng số riêng (50%, 10%, 20%, 20%).
- Vẽ đồ thị theo level — level 20 mở module mới, level 25 đo tham trạng user trong main → đẩy lượng resource phân cực sang module phụ.
- *"Thay vì cái việc là mình cứ đi tới đâu rồi mình bắt đầu thêm — mình sẽ làm cái số này có một cái tương quan nhất định để mình biết là mình nên đẩy vào đây là khoảng bao nhiêu."*

---

## MVP — Test Gì?

Đến phase MVP, Vũ liệt kê lại checklist:

- Gameplay — đã hiểu, đã pass prototype.
- Fueling — pass prototype.
- Tech — *"chắc cũng vừa vừa thôi, mình làm nhanh, đâu có quan tâm rất nhiều."*
- **Tập user** — phẩm đoán trước "AI này phù hợp với nhóm nào", có thể là tập trong công ty hoặc tập bên ngoài thị trường.

Vấn đề thực tế khi test MVP ở Việt Nam: data nhận về từ user chỉ biết quốc gia, *"chứ còn để phân tích là con số sâu hơn thì rất khó."*

### Truyền Tập User Thông Qua CPI

Vũ sửa lại approach: **tập user truyền qua CPI** chứ không phải qua phân tích demographics sâu:

> *"Phần test user và test tập user để có thể truyền thành tập user thông qua giá là cái CPI. Ví dụ mọi người sẽ nhìn xem cái CPI cao quá thì sẽ là một cái giảo cản rất lớn — làm phát triển rất nhiều thời gian để nó có lãi."*

CPI là proxy duy nhất cho việc xác định tập user khi data demographics yếu.

### Mục Tiêu Test Theo Dòng Game

Thiên đặt vấn đề:
- Game **hyper** → tập trung vào **test CPI** (ngắn hạn, ROI nhanh).
- Game **bitcoin / dài hạn** → tập trung vào **test time chơi, intention** (giữ user lâu).

Vũ xác nhận chính xác — bổ sung vào phần test user: time chơi và intention (ý định quay lại).

---

## D3 vs D7 — Tính Lượng Level Cần Cho Retention

Khi target retention, học viên đề xuất D3 hoặc D7. Vũ comment:

- **D7 thì căng đét** — đa phần không đạt được nếu không có content sâu.
- **D3 thì hợp lý hơn** cho prototype/MVP giai đoạn đầu.

Quy trình tính lượng level cần để đạt D3:

1. Tự chơi để đo thời gian/level.
2. Giả định: 1 level = 1 phút.
3. Đặt giả thiết user chơi bao nhiêu phút/ngày → ra số level cần.

Phản biện của học viên: *"Em nghĩ bao nhiêu phút nó không phải vấn đề ở đấy. Vấn đề là mình cần mục tiêu là bao nhiêu impression."* Nếu game có giới hạn resource (stamina, mạng) — user pham hết resource thì quay lại ngày sau lấy resource khác.

### Inter:Reward Ratio Trong D3 Planning

Học viên áp dụng công thức Inter:Reward đã học Doc 2:

- Ngày đầu: mỗi 5 level → 1 ad. Cần 4 ad/ngày → cho user 5-6 mạng.
- Thời gian hồi mạng quyết định pacing — ngắn để user quay lại nhiều lần, nhưng có giới hạn để không gây mệt mỏi.

Vũ lưu ý: tham chơi (engagement time) không thể không chế cứng được — chỉ không chế resource. *"Quan trọng là người ta có chơi thoải mái không, hay là người ta đã bỏ rồi."*

---

## Test Prototype Không Quảng Cáo — Quan Điểm Cốt Lõi

Phần Hiệp đẩy lên — quan điểm gây tranh luận. Cách các studio quốc tế (Voodoo, Lion, Cowally) test:

> *"Phố nó test là nó lạc đầu, thì thường không có quảng cáo luôn. Tại vì sao?"*

### Logic — Tách Chất Lượng Idea Khỏi Doanh Thu

Hiệp giải thích: nếu test có quảng cáo từ đầu, không phân biệt được:

- User bỏ vì game **không hay** (idea kém).
- User bỏ vì **quảng cáo phiền** (UX kém).
- Doanh thu tốt vì **idea giải trí** hay vì **mũ nét tốt**.

Bản không quảng cáo cho phép đo:
- User có thực sự **hứng thú** với game không (15-20 phút engagement thuần).
- Idea có được chấp nhận không.

Sau 3-5 ngày test bản không quảng cáo, đẩy bản có quảng cáo → so sánh 2 con với nhau để tách 2 biến.

Vũ bổ sung kinh nghiệm bên mình: 

> *"Bọn mình chỉ thường hay đút quảng cáo ở khoảng tầm sau level 3, level 4 — con số tương tự như thế. Và so sánh với cái bản không quảng cáo thì bọn mình thấy là về mặt tham chơi thì xem xem nhau, nhưng mà đi ra xe tù đài."*

Kết quả test khá dễ đoán trước — quảng cáo đẩy vào sớm sẽ kill tham chơi rõ rệt.

### Volume & Ngân Sách Test

Test bản không quảng cáo không cần volume lớn:
- Ngân sách ~$50-$100/ngày × 3-4 ngày.
- Đủ kết luận idea có được chấp nhận không.

---

## Mục Tiêu Prototype — Ít Biến Số Nhất

Sau case Giang (prototype test cụ thể 2 thứ: test idea + test khả thi kỹ thuật), Vũ chốt nguyên tắc:

> *"Về nguyên tắc nhé — khi chúng ta muốn chứng minh một cái gì thì tốt nhất là cái biến số của nó ít nhất. Thì nó sẽ biết nó đúng hay sai. Còn nếu chúng ta cho quá nhiều biến số vào đấy để chứng minh một cái là đúng, thì chúng ta sẽ không biết chúng ta đang đúng hay sai vào biến số nào."*

Prototype phải có mục tiêu **đơn lẻ và rõ**:
- Test 1 idea, hoặc test 1 vấn đề kỹ thuật.
- Không cố ép prototype kiêm luôn việc của MVP.

Nguyên tắc rút ra qua trao đổi với Giang:
1. **Đầu vào** — proline test được idea là quan trọng nhất; idea là 1.
2. Nếu prototype không pass → 2 lựa chọn: **bỏ luôn** (nếu thị trường đã có), hoặc **làm hẳn 1 sản phẩm thử** (nếu mình đánh giá là tiềm năng).
3. Không phun tiền vào hoàn thiện prototype quá sâu — vẽ vương thêm để chỉ trục ý đồ thị trường lên co len cho sản phẩm chính sau.

---

## CTR — Số Đầu Tiên Đánh Giá Prototype

Tiêu chí đo idea được chấp nhận hay không, ưu tiên dùng CTR (click-through rate):

- Chạy 10 user → CTR ~80% → idea được chấp nhận.
- Mất ~1 tuần để có câu trả lời CTR, quyết định tiếp tục hay stop.

Nếu cố ghép CTR với CVI (cost video install) hoặc kéo dài tới MPV → tốn thêm 2 phần thời gian và tiền.

### CTR Baseline Phụ Thuộc Volume

Câu hỏi: 0.3 là tốt không?

> *"0.3 chứ không phải tốt mà có khi tận 0.1, với volume nó rất là lớn. Đối với CTR chẳng hạn 80%, với volume nó rất lớn. Vậy thì cái volume của 0.3 này của anh nó không đại diện được, bắt vụ nó phải 0.1 thì nó mới là cái đúng."*

Quy tắc: baseline CTR/CVI không có con số tuyệt đối — phụ thuộc volume + ngân sách + vùng test. GD chỉ ra số liệu, UA chuyển con số sang kết luận market.

---

## Định Nghĩa Lại Inter — Không Phải Để Spam

Phần Vũ chỉnh lại tư duy phổ biến của developer Việt Nam:

> *"Inter, tại sao nó xin làm inter, chắc chắn nó không phải là cái để làm phiền. Chúng ta đang lạm dụng nó một cách xa, biến nó thành một cái làm phiền phải dùng."*

### Inter Đúng Nghĩa

Inter (interstitial ad) phải là:

- **Phích thời gian** cho người chơi dừng lại nghỉ tí và chuẩn bị cho session tiếp theo.
- Quảng cáo phải đúng tác dụng — **người ta xem mong muốn, xem để thư giãn**.
- Sau đó user quay lại tiếp tục với stress (challenge) tiếp theo.

Pattern sai phổ biến: spam inter mỗi cuối level, lạm dụng → user bỏ.

> *"Inter nó là quảng cáo, phích thời gian để cho người chơi họ dừng lãng quãng nghỉ tích và bắt đầu trong một chút kì mới."*

GD phải biết "mũ nét gì thì làm" — vị trí quảng cáo phải có thiết kế chủ ý, không chỉ là bộ đếm level.

---

## Mũ Nét — Lãi Ở Đâu Trên Game

Vũ phân biệt 2 trục thiết kế game:

- **Game "lãi ở đây"** (đầu game) — kiểu spam art / sản phẩm chỉ ăn user ở ngay từ đầu, không scale được sâu.
- **Game "lãi ở đây mũ"** — tạo mũ nét (money knot — điểm tiêu tiền của user) ở giữa và sâu trong game, user phải đi đoạn dài mới đến.

> *"Game lãi ở đây không, lãi ở đây mũ. Và game lãi ở đây mũ thì game nào dễ scale cơ? Lãi ở đây mũ sẽ là game rất dễ scale. Và đây là cách làm game — chứ không phải làm game như này."*

Game "lãi ở đây mũ" khó hơn nhiều — cần kiến thức làm cả hệ thống mũ nét, quảng cáo phải phát đúng tác dụng. Đổi lại scale được.

---

## Day 7 Hoà Dễ Scale Hơn Day 3 Hoà

Vũ đặt câu hỏi: tại sao test lãi ở D7 thì dễ scale hơn lãi ở D3? Giang phản biện đầu tiên:

- **Quan điểm Giang**: Lãi ở D3 dễ ra quyết định hơn — *"việc scale rất khó dễ ra quyết định, lãi ở D7 thì có thể là nó sẽ bền hơn."*

Vũ xác nhận quan điểm Giang đúng — với điều kiện coi đây là **một cách chơi game** (kinh doanh game phải ra lợi nhuận):

> *"Anh làm cho người ta đây một cách chơi game. Lãi ở D7 sẽ đúng khi mà chúng ta coi đây là một cách chơi game. Chơi game thì phải ra lợi nhuận mà. Nhưng nó không phải là chơi game."*

### Lý Do Kỹ Thuật

Vũ giải thích góc UA — game lãi sớm khó scale:

> *"Chạy tất cả con game các bạn đến thời điểm hiện tại. Với mặt UA các bạn có thể chạy ROAS, chạy GPA, các bạn nào target D0, D0-1 càng cao gần như cao của bạn không chạy được dụng chạy luôn. Cái này là thực tế nhất."*

### Mặt Feeling User

Vũ phân tích thêm góc trải nghiệm:

> *"Khi mà các bạn dồn dộng quá nhiều các thứ thì chúng ta kiếm tiền thôi user, cho người ta ra đầu — có nghĩa là người ta sẽ bỏ rất nhanh."*

Analogy bài học: như mua một căn nhà, *"người ta phải dàn trả ra trả nợ — nó không bắt bạn trả nợ ngay được. Chúng ta phải bỏ mặt tràn trải ra, sau đó người ta thanh toán."*

Hyper case ép D1 hoà:
- Phải khai thác cực kỳ trên đề ngay D1.
- Khai thác quá nhiều → user mệt mỏi, khó chịu, không quay lại.
- *"Cái tỷ lệ này không sao — người ta coi lại có không."*

### Quyết Định Theo Dòng Game

- **Hyper** → tỷ lệ ép sớm OK (anh em đã chạy quen).
- **Hybrid / partial** → nên target D3 hoà hoặc D7 hoà — dòng game cho phép pacing dài hơn.

---

## Fueling — Pacing Khai Thác Value

Fueling (theo cách Vũ dùng) không phải "battle simulation" mà là **tốc độ/phân bổ khai thác value từ user qua thời gian**. Đây là khái niệm gắn liền với điểm hoà:

> *"Mà về mặt fueling, thì khi mà các bạn dồn dậm quá nhiều các thứ để chúng ta kiếm tiền từ 1 user trong lần ra đầu — có nghĩa là người ta sẽ bỏ rất là nhanh. Có khi chúng ta cũng không nhận được cái gì đó."*

Analogy mà Vũ dùng: như mua nhà — *"người ta phải dàn trả ra trả nợ, không bắt bạn trả nợ ngay được. Mình phải dàn trải ra, sau đó người ta thanh toán lại."*

### Hyper Fueling — Ép D0/D1

Game hyper buộc fueling dồn sớm:
- Phải khai thác cực kỳ vào D0/D1 để hoà.
- Khai thác quá nhiều → user mệt mỏi, khó chịu, retention D1 thấp.
- Phù hợp dòng hyper vì lifecycle ngắn (~3-6 tháng) và CPI rẻ; không scale được lâu dài.

### Hybrid/ERP Fueling — Trải Dài D3-D7+

Game hybrid hoặc ERP cho phép fueling dàn trải:
- D3, D7 (hoặc D14, D30) là điểm hoà.
- Mỗi ngày khai thác một phần, user không cảm thấy bị ép.
- Pool user tiếp cận lớn hơn vì spam ad/IAP nhẹ tay → cả non-IAP user lẫn pay user cùng giữ được.

Khi Vũ trả lời câu của Hiệp "tại sao D7 dễ scale hơn cùng một con game": *"Mình cứ hiểu đơn giản là một con nó hoà ngay từ đầu thì cái đường dốc nó đâm xuống nhanh hơn. Còn con kia tuy nó dốc hơn nhưng mà sau một ngày D7 vậy thì nó vẫn còn kiếm được tiền — nó sẽ kiếm được nhiều tiền hơn."*

### Điều Kiện Tiền Đề

Vũ nhấn: chuyển từ D3 hoà sang D7 hoà **không phải chỉ là chuyển target**. Tiền đề bắt buộc:
- **Content kéo dài tới ít nhất D7** — không chỉ đủ hấp dẫn vài ngày đầu.
- **Quảng cáo + IAP có cấu trúc dàn trải** — không chỉ frontload ngay D0.
- **Pool sản phẩm chất lượng** — *"không tự nhiên chúng ta mang một cái món hà hay là một cái quả dưa bị thối ra bắt người ta mua."*

Case study Vũ kể: con Múc Càn Trô — ngày trước chạy theo cách hoà D3 → chỉ scale được ~30 triệu downloads. Sau khi chuyển sang hoà D30 → scale lên gần 200 triệu downloads.

---

## Giãn Inter — Case Tăng LTV 60-70%

Hiệp chia sẻ case thực tế giảm density inter, kéo lãi sang day xa hơn:

### Bài Toán

Approach cũ: cứ 1 level → 1 inter. User phàn nàn quảng cáo nhiều.

### 2 Logic Thử Nghiệm

1. **Logic 1**: Sau 2 level → mới đa 1 inter.
2. **Logic 2**: Sau khi xem 1 quảng cáo → phải khoảng 1 phút sau (hoặc thời gian tối thiểu) → mới hiện inter tiếp theo.

### Kết Quả

| Phiên bản | Chỉ số D2 | LTV tổng |
|-----------|-----------|----------|
| Logic 1 (giãn theo level) | Tăng 1 chút | — |
| Logic 2 (giãn theo time + level) | Tăng tương đối vượt | LTV tổng kéo ~160-170% |

> *"Cái bản giảm là xem 1 inter thì 1 phút sau nguyên inter, thì cái chỉ số nó tăng lên tương đối là vượt. Thứ 4 là vượt so với cả các bản khác. Và bọn mình kéo cái mức độ hoà xuống ngày 3 — nhưng bù lại thì tăng lên khá là tốt."*

### Bài Học

- Giảm doanh thu D1-D2 để kéo dài user → tổng LTV tăng vượt.
- Áp pattern này sang các con sau làm baseline cho team.

### Trade-off Day 7 Hoà

Hiệp note rủi ro: dồn hoà sang D7 → giai đoạn đầu **lượng LowWatt trả về thấp** (~20-25%). Yên tâm hơn khi LowWatt đầu game ~40-50%, sau đó giãn dần kéo LTV về sau:

> *"Nếu giá như với cách làm trước thì LTV chỉ là 120%, 130% thôi. Nhưng mà nếu các bạn giãn dần một chút — tùy cái này mình định lượng, mình đo test nữa — nó có thể kéo đến khoảng tầm 140%, 150%, 70%."*

---

## Điểm Hoà — Càng Muộn Thì Vùng Khai Thác Càng Dài

Vũ vẽ sơ đồ trên 2 con sản phẩm chất lượng tương đương trên cùng hệ thống chiếu SQI:

- **Sản phẩm A**: Điểm hoà = D2. CPI tăng thì D2 sẽ tụt → phần dư khai thác hẹp.
- **Sản phẩm B**: Điểm hoà = D7 (hoặc D6/D8). Phần dư khai thác kéo dài → giá trị về tiền keo ~15.

> *"Thay vào việc điểm hoà đây chúng ta cộng cái số nhỏ, và điểm hoà đây chúng ta cộng cái số lớn — thì cái nào sẽ mang lại giá trị? Cái này nó sẽ chỉ mang là chúng ta sẽ khó quất tích trong giai đoạn nặng."*

Các game điểm hoà kéo D30, D60 → vùng khai thác càng dài → scale càng tốt. Bài học chung: **chuyển điểm hoà từ D2 sang D7 là một bước scale lớn trong cùng cấu trúc game**.

---

# Part 2 — Q&A Mở Rộng: UX, Retention & Balance

Phần này tiếp ngay sau session Part 1, mở rộng từ giáo trình sang Q&A về UX, retention curve, và cách balance progression cho game ERP/RPG. Vũ chuyển topic bằng câu: *"Bây giờ đến phần thứ 2 — time play của session."*

---

## Phân Biệt UI vs UX

Học viên định nghĩa UX là *"một người chơi với các cái button — như mình hiện cái nút đấy lên thôi."* Vũ chỉnh lại:

> *"Vấn đề là kiểu cái nút đấy người dùng có cảm thấy tiện không? Người ta thấy kiểu quen thuộc không? Thì cái đấy gọi là user experience."*

UI = cấu trúc nút/màn hình; UX = trải nghiệm khi user thực sự tương tác với cấu trúc đó.

### Ví Dụ Cụ Thể — Màn Chọn Hệ Nhân Vật

Vũ minh hoạ bằng màn chọn nhân vật trong game (3 nhân vật trên, 3 nút hệ dưới, switch character theo hệ). Test với học viên:

- **Bạn 1**: bấm vào hệ ở thanh dưới → nhân vật switch theo.
- **Bạn 2**: bấm trực tiếp vào nhân vật trên màn hình.

Cả hai đều "đúng" về function nhưng phản ánh UX khác nhau. Vũ nhấn:

> *"Không phải user nào họ cũng tag vào đây, không phải user nào họ cũng thích tag vào đây. UX là làm sao để 10 thằng user nó đều trải nghiệm tốt nhất — mà 10 thằng user 10 tính cách hoàn toàn khác nhau."*

### Edge Case — Thằng Tay Trái vs Tay Phải

Vũ kể case con survival có nút multimedia thiết kế ban đầu cho user tay phải. Feedback từ user tay trái: *"tao phải đánh nhầm."* Bài học: UX phải tính cả thằng tay trái, thằng tay phải, thằng ngón dài, thằng ngón ngắn — không thể design 1 layout phục vụ mọi cách cầm.

### Visibility & Familiarity

Yếu tố nhận diện nút:
- **To, rõ ràng, sạch sẽ, không phải sót** — đặt ở chỗ trung tâm, màu rực rỡ.
- **Quen thuộc** — *"thói quen của hành vi như chồng mình luôn ám"* (button mua sắm thường xanh — user đã quen với màu này từ các game khác, nếu mình dùng màu khác → user không tìm được).
- **Tách bạch khỏi giả-nút** — *"các tách xong gạch nhịp giống kiểu game Hyper hay để cái chữ nồng thanh thì người ta cũng rất khó tìm. Người ta luôn sẽ ấn vào cái đầu tiên hiện lên."*

---

## Hierarchy Reward Quảng Cáo — WeTry > Hint > Booster

Vũ test học viên: trong 3 loại nút quảng cáo reward, cái nào được user bấm nhiều nhất?

1. **Hint** (gợi ý chơi).
2. **WeTry / Continue** (chơi lại sau khi thua, giữ progress).
3. **Booster** (vật phẩm hỗ trợ).

Học viên trả lời WeTry — lý do: *"Họ không muốn phải làm lại tất cả những cái từ trước đấy. Giữ lại thành quả từ trước và vẫn có thể phạm phá ra những cái lưu dụng sau."*

Vũ xác nhận. Hierarchy phản ánh **giá trị psychological** mà user gán cho reward:
- **Tránh mất progress** (WeTry) > **Tăng tiến độ** (Hint) > **Lợi ích phụ** (Booster).
- Loss aversion mạnh hơn gain pursuit.

GD đặt vị trí quảng cáo nên ưu tiên WeTry hoá hành vi user — vd lose-screen ad luôn ở vị trí dễ bấm nhất.

---

## Người Cao Tuổi & Tolerance Quảng Cáo

Học viên (Linh) share quan sát: *"Em rất hay chơi game với người già. Người già với trẻ nhỏ họ phản ánh rất thật luôn. Khi mà người già chơi lâu họ hay có xu hướng là xem một cái ạt — như kiểu là họ xem ạt họ được giải trí luôn. Họ không ngại khi xem ạt."*

Ứng dụng: với segment cao tuổi, có thể dí inter sớm hơn (vd level 4) — *"chứ không nhất thi là phải thẳng qua."* Tuy nhiên ad phải có **giá trị nội tại với user** (ngoài giải trí), không chỉ là chặn ngang gameplay.

---

## Retention Curves R1 → R7 — Bài Toán "Làm Sao Họ Quay Lại"

Vũ phân chia bài toán retention theo các mốc — *"R0 nó khác, R1 nó khác, R3, R5, R7 nó khác nhau"*:

- **R1 (Section 1 → Section 2)** — họ chơi xong section đầu, làm thế nào để họ chơi tiếp ngay session sau?
- **D1 → D2** — họ đóng game, ngày hôm sau làm thế nào kéo họ quay lại?
- **D3, D7 retention** — pacing content + reward cho từng ngày khác nhau.

Mỗi mốc cần một thiết kế khác: trong-session retention dùng momentum/curiosity hooks; cross-day retention dùng push noti, daily reward, gated progression.

GD là *"người thiết kế, họ muốn họ quay lại"* — Vũ nhấn đây là active design choice, không phải hệ quả.

---

## Trang Thái Visual & Brand Recognition

Học viên bổ sung yếu tố ảnh hưởng tỷ lệ bấm ad:
- **Xấu/đẹp & cực lý** — trạng thái visual có hấp dẫn không.
- **Nhận diện** — user đã nhìn thấy hình ảnh con game này từ quảng cáo trước đó. Nếu không thích, họ không bấm vào.

> *"Đôi khi thì cái credit mình tả ra ở quảng cáo gà thì nó biết — ví dụ là Mò và game, Mò và game..."*

Brand recognition cross-channel: art style + concept phải nhất quán giữa quảng cáo và game thật, không thì user click rồi bỏ vì kỳ vọng lệch.

---

## ARPU vs ARPPU — Trade-off Cho ERP

Vũ giải thích 2 chỉ số doanh thu user:

- **ARPU** (Average Revenue Per User) — tổng doanh thu / tổng số user (kể cả không trả tiền).
- **ARPPU** (Average Revenue Per Paying User) — doanh thu / chỉ số user đã trả tiền.

> *"Em thấy ARPPU làm gì khi mà tỷ lệ nó lại thấp? Đúng rồi — ARPU cao."*

Quy luật trade-off thường gặp:
- **ARPPU cao + Pay rate thấp** → một số ít whale đóng góp đại đa số doanh thu. ARPU đi ngang.
- **ARPPU cân bằng + Pay rate cao** → nhiều user cùng trả ít. ARPU đi lên.

Cho game ERP, Vũ khuyên ưu tiên đẩy ARPU lên qua pay rate, không chỉ đẩy ARPPU:

> *"Đối với ERP nhé — hãy cố gắng biến user free thành user trả tiền. Khi user đã trả tiền rồi hãy cứ dừng với họ. Cứ dừng càng kéo thì em sẽ kéo cái credit này càng cao."*

"Cứ dừng càng kéo" = giữ user trả tiền lâu dài thay vì ép họ trả thật nhiều ngay lần đầu.

---

## Imba/Balance Gói Meta — Bài Toán Của Game Có Tướng

Học viên có game có gói tướng — bán theo cấu trúc (10 đô, 5 đô, 7 đô...). Vấn đề: nếu user mua được gói cuối → sở hữu hết toàn bộ tướng meta → game **mất giá trị progression**.

> *"Anh bán cho người ta đến đây không đúng — người ta đã đủ khả năng sở hữu toàn bộ cái thời gian cho cái con game này của anh rồi. Thế dẫn đến xong nó sẽ không còn giá trị nữa."*

### Giải Pháp — Balance Power vs Resource Tại Checkpoint

Vũ vẽ nguyên tắc:

> *"Em phải luôn luôn balancing được cái MTV (có thể là EV, có thể là EAV) tại một checkpoint, bằng với power của nó tại checkpoint này — hoặc lớn hơn nhỏ hơn cộng trừ một con số nào đó. Chứ đừng để mất cân bằng."*

2 dạng mất cân bằng (imba) phổ biến:
1. **Imba cao quá sớm** — user mua xong tới checkpoint mới mà power vẫn vượt yêu cầu → không cần grind, content tiếp theo vô nghĩa.
2. **Yếu một cái đáy ra** — user trả tiền xong rồi power vẫn không đủ → cảm thấy bị lừa.

### Khi Nên Cho Imba Có Mục Đích

Có lúc cố ý cho imba ngắn hạn để thúc đẩy mua thêm:

> *"Em phải cần để cho nó imba một thời gian. Chứ nó nạp tiền xong rồi nó không imba thì dở rồi."*

Imba có chủ ý + thời lượng giới hạn:
- User nạp tiền → cảm giác mạnh mẽ ngắn hạn.
- Khi ra "tường mới" (content mới, độ khó mới) → cân bằng lại.
- Tường mới làm đằng sau, không phải đẩy thẳng ngay từ đầu.

Vũ note: bài toán này phức tạp, cần một buổi riêng để giải sâu — chỉ định hướng nguyên tắc tại đây.

---

## Anti-Pattern Phổ Biến — Lái Theo User

Anti-pattern xuất hiện trong buổi (cả Part 1 + Part 2):

- **Định lượng resource bằng "user thiếu rồi bù"** — Vũ note: không sai nhưng là loop đuổi theo user. Nên vẽ đồ thị trọng số trước.
- **Test prototype có quảng cáo** — không tách được chất lượng idea và mũ nét.
- **Spam inter sau mỗi level** — *"đây tôi không hề đúng đường luôn, nhưng bài toán để làm thì người ta lại ở đây."*
- **Target D0/D1 hoà cao** — UA không scale được, *"các bạn không chạy được dụng chạy luôn."*
- **Chứng minh 1 cái với nhiều biến số** — không biết đúng/sai do biến nào.
- **Bán gói cho phép sở hữu toàn bộ meta tướng** — phá progression, game mất giá trị sau gói cuối.
- **UI giả-nút theo style Hyper** (chữ nồng thanh, gạch nhịp) — user khó tìm đúng button, mặc định bấm cái đầu tiên hiện lên.
- **Design layout chỉ cho 1 cách cầm** — bỏ qua user tay trái, ngón dài/ngắn → UX fail edge cases.

---

# Part 3 — Improve Chỉ Số: Khung Cải Thiện Retention, Stack, Content, UX

Sau Part 2, Vũ chuyển sang câu hỏi mở: *"Bây giờ cần improve chỉ số. Mọi người thường được yêu cầu improve những chỉ số gì?"* Học viên kể: Retention, Time Play (Session/Tổng), Impression, Last Game (tech), Stuck, Tutorial, Server, Event, Cộng đồng, Trending, Giới hạn lý suộc. Vũ phân ra GD can thiệp được và phần ngoài tầm GD.

---

## Phân Loại Chỉ Số Theo Tầm GD Can Thiệp

Vũ liệt kê và đánh dấu:

| Chỉ số | GD can thiệp? | Ghi chú |
|--------|:-------------:|---------|
| Retention | ✅ | Cốt lõi của GD |
| Time Play (Session) | ✅ | Habit hình thành trong ngày |
| Time Play (Tổng) | ✅ | = Session × Số session |
| Impression | ✅ | Số session tăng → impression tăng |
| Last Game (tech) | ❌ | "Bên nào tech khoẻ thì sản phẩm tốt sẵn rồi" |
| Stuck | ✅ | UX/level pacing |
| Content | ✅ | Trọng tâm |
| Server | ❌ | Ngoài GD |
| Event | ✅ | Mode mới, daily challenge |
| Cộng đồng | ⚠️ | Định hướng community, không trực tiếp |
| Trending | ❌ | Ngoài khả năng GD |
| Giới hạn tài nguyên | ✅ | Lý suộc, stamina, mạng |
| Quảng cáo | ✅ | Vị trí, timing, mật độ |
| Notification | ✅ | Must-have nhưng impact thấp |

Vũ chốt nguyên tắc tránh suy nghĩ chủ quan:

> *"Không có cái gì càng càng càng đâu nhá. Càng càng là chỉ có càng khua thôi đấy."*

Cải thiện 1 chỉ số không tự động kéo retention. Phải biết chỉ số nào ảnh hưởng chỉ số nào.

---

## Critique Độ Tuổi & Văn Hoá — Không Design Theo Demographics

Học viên đề xuất: chỉnh game theo độ tuổi user. Vũ phản biện ngay — đây là chung chung và **chưa chắc chính xác**:

> *"Em lấy tách ra được 18 đến 25 đi. Với anh là một thằng hơn 30 tuổi, thì chắc chắn anh sẽ không biết nó hành động như thế nào. Anh là người Việt Nam — anh không biết 18, 25 tuổi của thằng Mỹ là như thế nào. Chắc chắn anh sẽ không biết."*

Ví dụ cụ thể về văn hoá cầm điện thoại:

- **Việt Nam** — cầm 2 tay, để màn hình ngang được, chơi thoải mái.
- **Nhật** — cầm 1 tay (vì đi xe điện, xe bus phải bám 1 tay) → màn hình ngang phải bỏ.

> *"Thằng Nhật, một tay nó phải bám vào bệ tàu, một tay nó chơi mà làm màn hình ngang thì phải bỏ — làm sao nó chơi được."*

Bài học: design layout/control phải hiểu **văn hoá target market**, không phải demographic chung. Trừ khi UA "rất giỏi" và đã tách khẩu học theo chiều sâu, segmentation theo độ tuổi là "trung trung và chưa chắc chính xác."

---

## Content vs Theme — Phân Biệt Quan Trọng

Vũ thử học viên: "Block puzzle 50M+ downloads thì có content gì?" Học viên: "Theme nó cũ, không có gì mới." Vũ chỉnh:

> *"Block puzzle là level của nó là content mà. Cái theme của nó không phải là mới — nhưng cái mới là cái câu đố của người ta. Cái câu đố ở mỗi level của nó là content."*

Phân biệt:
- **Theme** — concept tổng thể (đua xe, nông trại, puzzle).
- **Content** — biến thể trong từng level, từng session (câu đố, layout, đối thủ).

Anti-pattern: định nghĩa content quá rộng → không biết làm gì → thấy gì cũng muốn thêm. Phải **fix nội hàm content** trước (level layout? object mới? mode mới?) rồi mới mở rộng.

---

## UX Không Phải Nút Bấm — Trải Nghiệm Trên Sản Phẩm

Vũ mở rộng định nghĩa UX từ Part 2:

> *"UX không phải là cái việc trải nghiệm trên nút bấm. Mà UX là trải nghiệm về sản phẩm. Đây ví dụ: một sản phẩm em làm cần 3 bước, một sản phẩm em làm cần 2 bước — cái nào sướng? Nó có liên quan đến nút không?"*

### Case iPhone — Bật Hết Phone Có Phím

> *"Tại sao thằng iPhone đánh bật hết tất cả các loại O2? Bởi vì nó không có phím, nó không dùng bút. UX đấy — không phải nút đâu, không phải đồ hoạ đâu."*

iPhone thắng vì **giảm số bước** + **flow thuận** với suy nghĩ user, không phải vì button đẹp.

### Case Úc — Nhà Vệ Sinh Không Vòi Xịt

Trải nghiệm rủi ro cao về UX khi đi nước ngoài:

> *"Anh đi vào nhà vệ sinh — không có cái quả xí đít, rất khó chịu. Cái đấy không liên quan đến đồ hoạ cả, không liên quan đẹp gì cả."*

UX = expectation match. Khi flow lệch khỏi habit cũ → khó chịu, dù UI không sai.

### Case Nhà Hàng Nhật — Spend Tiền Vì Bowing

> *"Mình đi vào nhà hàng Nhật, tại sao mình spend tiền rất nhiều? Vào nó đứng, 2 thằng bên cúi gập người xuống chào. Nó đưa cho cái menu, một cái đĩa, mấy miếng cá sống cắt lên — 5-700 nghìn — theo mình gật đầu dễ lắm luôn. UX ở đấy — chứ không phải là nút xanh, nút đỏ, nút to, nút vàng đâu."*

UX dẫn dắt expectation và willingness-to-pay. Service flow > UI aesthetics.

### Áp Dụng Cho Game

GD nguyên tắc:
- **Game cũ làm 3 bước → mình làm 2 bước.**
- **Game cũ cần text giải thích → mình design intuitive, không cần text.**
- **UI chỉ là phần hiển thị (button to bao nhiêu, màu gì) — UX bao gồm UI nhưng còn flow, expectation, habit.**

> *"UI chỉ là cái hiển thị thôi. UX có UI nằm trong đó — nhưng nó còn rất nhiều thứ khác."*

### Customize Cho Tay Trái / Tay Phải

Anh ra mở rộng case con survival multimedia button của Vũ:

> *"Tại sao không cho chúng nó customize được? Thằng tay phải chuyển sang tay trái chơi, thằng tay trái chuyển sang phải. Mày tay trái — mày vào đây nó xếp lại."*

Khi không thể design 1 layout phục vụ mọi cách cầm → **cho user customize** thay vì cố "tối ưu cho 2 đứa cùng lúc."

---

## Stack — 3 Loại Khác Nhau, Cách Sửa Khác Nhau

Vũ phân loại stack (stuck) theo 3 nguyên nhân:

1. **Stack khó hiểu** — user bấm vào không biết bấm vào đâu, không hiểu phải làm gì.
2. **Stack khó thực hiện** — user hiểu rồi nhưng bấm hụt, button nhỏ hơn chuẩn Google.
3. **Stack khó hình thành thói quen** — user vào lần thứ 3, 4 vẫn quên flow.

Cách sửa từng loại:

- **Khó hiểu** → tăng visibility nút (to, rõ, sáng, ở trung tâm, không phải search), thêm hint, tutorial inline.
- **Khó thực hiện** → tăng kích thước nút, đảm bảo touch target ≥ Google standard.
- **Khó hình thành thói quen** → đặt nút ở vị trí familiar, dùng màu quen thuộc.

### Visibility & Familiarity Của Nút

Vũ liệt kê yếu tố giúp nút "dễ tìm":

- **To, rõ ràng, sạch sẽ** — đặt ở chỗ trung tâm, màu rực rỡ, không phải search.
- **Quen thuộc — màu "shop xanh"**:
  > *"Thói quen của hành vi như Shopee Mall luôn ám. Nó là màu xanh để ta đã quen với những cái nút đấy. Nếu mà ví dụ như Shopee mà làm cái nút kia cam thì nó không bị mình bị mất."*
  
  Buy buttons thường xanh — user đã quen từ các app khác. Đổi màu khác → user mất reflex.
- **Tách bạch khỏi giả-nút** — *"các Hyper hay để cái chữ nồng thanh thì người ta cũng rất khó tìm. Người ta luôn sẽ ấn vào cái đầu tiên hiện lên."*

### Khi Drop 40% Sau 2 Level — Là Khó Hay Là Gì?

Học viên Vũ kể case con game của bọn anh từng drop 40% sau 2 level đầu → còn 6%. Vũ nguyên tắc đặt câu hỏi:

> *"Em không nhận định là khó quá. Bắt đầu phải lăn vào để xử lý cho em vấn đề đấy. Chúng ta có thể đi detect — chứ không phải là cứ chốt là khó quá. Đặc sử em bảo cái level đấy của em nó chết quá nhiều — thì lúc đấy em sẽ suy nghĩ trong đầu là level này của mình khó quá."*

Drop có thể vì:
- **Khó** — không tìm ra cách giải.
- **Không thích game** — drop ngay từ đầu, không stuck.
- **Khó hình thành thói quen** — vẫn không quen flow sau lần thứ 3.

Phải detect bằng số (last action, time-to-quit, last_down từ boss hay obstacle) — không jump kết luận.

---

## 4 Mức Hành Vi: Học → Rèn Luyện → Thử Thách → Làm Chủ

Vũ giảng nguyên lý habit formation áp dụng vào level pacing:

> *"Hành vi user thì chắc chắn là có 4 bước: học, rèn luyện, có một cái thử thách, và cuối cùng là master nó rồi. Chúng ta thường viết là ít nhất chúng ta có 4 level."*

Cấu trúc:

| Mức | Số level tối thiểu | Vấn đề / Chốt |
|-----|:------------------:|---------------|
| Học | 1 | 3 chốt 2 vấn đề |
| Rèn luyện | 1 | 3 chốt 3 vấn đề |
| Thử thách | 1 | 3 chốt 4 vấn đề |
| Làm chủ | 1-2 | 3 chốt 5 vấn đề |

Người chơi đi qua 4 cái này trong một "project" (1 motif/biome), sau đó:
- **Điểm chốt master** = thời điểm chuyển content mới (đổi map, mở mode mới).
- Content mới phải **kế thừa** kỹ năng cũ — đừng làm "skill cũ vô nghĩa, skill mới lại học từ đầu."

### Analogy Pavlov

Vũ dùng phản xạ có điều kiện làm metaphor:

> *"Giống như ngày xưa mọi người học cái bài học gì mà bật đèn là chó chảy nước rãi. Phải làm những cái đấy đều, và những hành vi bên trong na ná giống nhau, thì user nó mới thành phản xạ. Còn em bây giờ vừa mới bật đèn — sau này tới lẽ làm cái khác hẳn luôn, tới lẽ làm cái khác hẳn nữa — thì user nó liên tục xoay xoay xoay, gần như nó không có khả năng control được game của em."*

Phải **lặp đủ** trong cùng motif (3-4 level) để user form reflex, **sau đó mới break** sang motif mới.

### Anti-Pattern — Mỗi Level Một Mechanic Khác

Vũ chỉ ra mistake phổ biến của GD:

> *"Cái này các bạn game design thường hơi không để ý. Tức là luôn luôn muốn làm level sau với level trước khác nhau rất nhiều — để mình cảm giác thoải mái, không bị nhàm chán công việc."*

Designer "vui vì content đa dạng" nhưng user "loạn vì không có pattern." Phải design **cho user, không cho designer**.

### Đo Khi Nào User "Chán" / "Master"

Vũ chia sẻ kinh nghiệm dòng puzzle: chán xuất hiện sau **7-10 phút** làm cùng motif. Trong session ngắn: lần 1 lạ, lần 2 quen, lần 3 chán → **lần thứ 3-4 nên thay** content.

---

## Sướng vs Khổ — Habit Formation Có Biên Độ

Vũ đặt câu hỏi: sướng và khổ, cái nào hình thành habit dễ hơn?

> *"Không ai có sở thích húc đầu vào đá cả. Đúng không? Làm một việc thuận lợi dễ hình thành thói quen hơn là một việc khó khăn. Nhưng tới một độ liều lượng, sướng quá ngược lại bỏ nhanh."*

### Analogy Ăn Sập Chợ

- **50 triệu, ngày hôm nay ăn sập chợ**:
  > *"Chắc chắn buổi sau ngán đúng không?"* — sướng quá → một lần là xong.
- **50 nghìn, 2 món/ngày, một tuần ăn sập chợ**:
  > *"Thử thách là sập chợ. Ngày hôm nay ăn được 2 món. Một tuần các bạn mới ăn xong cái chợ đấy."* — vừa đủ thử thách → habit dài hạn.

### Biên Độ Playtime — Không Pump Quá Cao

Vũ phản biện reflex "tăng playtime càng cao càng tốt":

> *"Mọi người hãy ý những cái con game mà có retention cao nhất — là những con game nào? Là những con mà có chỉ đo retention thang cao nhất, lại thường có những section chơi rất là ngắn."*

Pattern thực tế:
- 1 minute action (thu hoạch cây, đặt máy quả) → tắt điện thoại → ngày mai mở lại.
- **Session ngắn** → habit dễ hình thành.
- Session dài nhất thời → user expect mai cũng dài → mai không đáp ứng được → drop.

Analogy: đá bóng 1 trận sướng. Đá tiếp 3 tiếng → ngán, không muốn chơi.

---

## Ngắt Mềm vs Ngắt Cứng — Thiết Kế Để User Tự Dừng

Khác biệt giữa **active disengagement** (ngắt mềm) và **forced break** (ngắt cứng):

> *"User sẽ chủ động ngắt. Nó khác với việc bạn làm cái quà gọi là online liên tục."*

### Ngắt Mềm — Mồi Câu Theo Phút

Cơ chế:
- User chơi 10 phút → thấy có "món quà sau 1 phút nữa" → dừng lại, sẽ quay lại.
- Lucky Spin: chơi xong nhận quà nhỏ → "10-15 phút sau quay lại lấy free spin."
- Mục đích: **tạo nhiều session ngắn** thay vì 1 session dài.

> *"Cái việc ngắt chủ động này dẫn tới session chơi của bạn sẽ nhiều, nhưng playtime thì không cao. Nhưng nó hình thành được một thói quen — liên tục tạo ra mồi câu, mồi câu trong ngày, mồi câu sang ngày hôm sau."*

### Anti-Pattern — Win Streak Hung Hăng

Candy Crush style win streak:

> *"Thắng được 3 cuộc trận, được một mớ quà. Nếu thua quách phát, mất hết cả đống này luôn. Nó sẽ ngại."*

Win streak làm **tăng playtime** nhưng là con dao 2 lưỡi:
- User cực kỳ engaged → tốt cho whales (in-app payers).
- User không in-app → cảm thấy bị ép, mất win streak xong **không quay lại**.

> *"Khi user bị mất win streak, gần như họ không còn muốn chơi tiếp game đấy khi quay lại nữa, bởi vì nó khó khăn."*

GD phải biết target segment: high-payer thì hook strong, casual thì pacing nhẹ.

---

## Online Liên Tục vs Online Thời Điểm Cố Định

Vũ phân biệt 2 cách tạo session:

- **Online liên tục** — quà mỗi 1 phút, user phải mở liên tục → fatigue.
- **Online thời điểm cố định** — quà sau 10-15 phút, sau X giờ, daily login → user dừng nghỉ giữa, hình thành nhịp.

> *"Không phải online liên tục nhé. Mà là online vào thời điểm cố định. Thậm chí bạn có thể làm bằng cách là Lucky Spin — phút nữa sẽ có một lần free. User sẽ nghỉ luôn ở đó. Khoảng 10-15 phút sau nó quay lại."*

User pop in/out, nhận quà → "thích là việc nhận quà sau đó trân tiếp." Pattern này áp dụng cho mọi reward-on-timer mechanic.

---

## Case Block Puzzle 50M — Daily Challenge 28 Ngày

Vũ kể case một game block puzzle (~50M users) có **Daily Challenge 28 ngày**:

- 1 level/ngày, level rất khó — "khó khủng khiếp."
- Mỗi ngày chơi 1 lần.
- **Kích thích** vì độ khó cao trong khung 1 lần/ngày.
- Cuối 28 ngày → reward khủng (in-game) + retention D28 (game-side).

> *"Bởi vì một ngày chơi có một lần thôi. Một ngày có một lần và cuối cùng nó là một cái rì-quần khủng khiếp. Tức là nếu hoàn thành đống đấy thì về phía user được một mớ quả; còn về game của mình là được user đến tận ngày 28."*

Khác với "online liên tục" — đây là **hard challenge in fixed window** → vừa khó vừa habit-forming.

---

## Notification — Must-Have Nhưng Đừng Expect Cao

Vũ trả lời thẳng về push notification:

> *"Nó là một trong những tính năng must-have. Nhưng thực sự, theo kinh nghiệm của anh, nó không tăng được được bằng nhiều. Bạn tưởng tượng như các bạn thích làm cái gì bằng từ noti của mình thì nó chủ động rất nhiều."*

Generic push ("bao nhiêu nghìn người chơi đang chơi", "game đang cần sự hỗ trợ") — **có ý nghĩa nhưng đừng đặt expectation lớn**. Thứ tự ưu tiên cải thiện chỉ số:

1. **Stack** (sửa flow user kẹt).
2. **Content** (thêm/sửa biome, daily mission, daily reward).
3. **Giới hạn tài nguyên** (lý suộc, stamina).
4. **Quảng cáo** (vị trí, timing, density).
5. **Notification** (cuối cùng, low-impact).

---

## Ad Timing vs Skill Unlock — Đưa Ad Sau Khi Tặng

Nhân tiện về Black Block (đan ad), học viên hỏi:

> *"Nên đưa ad trước hay sau khi gai một kỹ năng mới?"*

Vũ trả lời rõ ràng — **đưa ad SAU**:

> *"Khi em đưa ra một kỹ năng mới thì cái expect — kỳ vọng — của họ về vấn đề đấy nó sẽ cao hơn. Và việc khi em xem quảng cáo xong nó đỡ bị drop hơn."*

Pattern triển khai:
- Cuối level → tặng user quả bom / mảnh khẩu súng.
- User mong unlock món tiếp → **đây là thời điểm tốt nhất để chen ad**.
- Drop rate khi ad xuất hiện thấp hơn vì user "tò mò với món quà sắp tới."

> *"Lúc thời điểm đẹp nhất để show quảng cáo là thời điểm mà trước đấy em phải tặng cho nó một cái gì đó, hoặc unlock một tính năng nào đó."*

Trừ khi có áp lực spam ad đẩy doanh thu → không tận dụng thời điểm này → drop rate cao hơn.

### Case Người Già + Ad Tại Level Core

Linh share thêm: người già "rất hay xem ạt" → có thể chen ad vào level core (boss). Nhưng:

> *"Cái ạt đấy của em nó phải có giá trị lớn hơn họ."*

Ad mid-gameplay phải có **reward đáng giá** (boost, revive) — không thể chỉ là interruption.

---

## Hierarchy Reward Quảng Cáo — Theo Dòng Game

Vũ mở rộng từ Part 2: bấm rate **không cố định** theo loại reward, mà phụ thuộc **dòng game**.

### Phân Loại Theo Cảm Xúc User

- **Hint** — *"Mày ngu để tao dạy."* User cảm giác chính mình ngu, cần hướng dẫn.
- **Booster** — *"Loạn này mày bị bí, cần một cái kỳ diệu."* User cảm giác mình ổn, chỉ là tình huống bí.
- **Revive** — *"Sắp thua rồi, không muốn bỏ phí."* User cảm giác tiếc công sức.

### Matching Theo Dòng Game

| Loại game | Reward cao nhất | Lý do |
|-----------|-----------------|-------|
| Logic + session ngắn (Candy Crush) | Hint + Revive | Giải ngược logic được, chỉ thiếu hint |
| Logic + session dài | Hint + Revive | Tương tự, nhưng Revive cao hơn |
| Random + session dài (Midcore) | Booster + Revive | Không thể giải ngược; sống lâu = giữ progress |
| Burst Mania-style | Revive | Midcore, session dài |

> *"Thằng Candy Crush không thể gắn Hint vào được. Logic giải ngược thì Hint luôn luôn có. Random thì Booster."*

### Bấm Rate Phụ Thuộc Tình Huống Cụ Thể

Cùng 1 game có thể bấm Booster hay Revive khác nhau theo **số mục tiêu còn lại trong trận**:

- Còn 1 mục tiêu → **Booster** (1 viên nổ, win ngay).
- Còn 2-3 mục tiêu → **Revive** (cần thêm move/turn).

Vũ chốt:

> *"Cái này không phụ thuộc vào mặc định nó tốt hay xấu, mà phụ thuộc tình huống. Là cái lúc đấy còn bao nhiêu mục tiêu."*

### Lưu Trả Là Tệ Nhất

Vũ note **Save / Try Again from Beginning** = loại bấm ít nhất:

> *"Lưu trả là tệ nhất — có nghĩa là gì? Hành trình ấy phải đi lại từ đầu. Ngu lại từ đầu. Đen lại từ đầu."*

Tập hardcore khắc kỷ thì OK, mass user thì không.

---

## Win-Screen Ad Tricks — 18 Versions, Mỗi Version Tăng Vài %

Hiệp/Vũ chia sẻ case tăng ad rate trên màn end-of-battle với cặp nút "Continue" + "x3":

### 3 Phương Án Đã Thử

1. **Tệ nhất** — Đổi vị trí 2 nút Continue/x3 ngẫu nhiên. *"Rất là tồi tàn hàn dịp"* — user tag nhầm vài lần thì học, không bền.
2. **Vòng quay x2/x3/x5** trên đầu — Số nó quay liên tục, user bấm dừng → ra số → nhận quà x số.
   > *"Trên này nó đọc số bao nhiêu kệ nó không quan tâm. Nhưng bấm vào đây thì cái này dừng lại — dừng đâu nhân đấy. Bét tí nhất cũng là nhân 1."*
3. **Pop-up có glow** — Chuyển win/lose từ full screen → pop-up. Nút "x3" với glow effect, kèm tia sáng → cảm giác urgency.

### Kết Quả 18 Tuần × 18 Phiên Bản

Mỗi phương án tăng vài % ad rate. Triển khai theo nhịp:
- Phương án 1: nhồi 1 lần / 5 levels (4 levels còn lại dùng phương án khác).
- Phương án 2: baseline.
- Phương án 3: replace phương án 1 sau khi confirm rate ổn.

> *"Trong cái trận hành trình đấy mình sẽ có nghĩ ra những trò — kể cả mưu hèn kế bẩn. Tăng nó lên, nhưng vấn đề là làm rồi quan sát số. Nếu tia sáng/đầu giảm — đoạn sau dừng lại."*

Đạo đức: tăng đến lúc user "cảm thấy bị lừa" → dừng. Đo qua tia sáng (overall engagement) — không chỉ ad rate.

### Bổ Sung Content Song Song

Cùng 18 tuần đó: bổ sung daily mission, daily reward (D3 rồng, D5 rồng cấp 3, D7 boss thoải mái). Combo win-screen tricks + content → con game scale "lên chỉ số để vững lãi, chạy được lần chục triệu user dân."

---

## Case Imposter Solo Queue — Bài Học Spam Inter

Vũ kể case **Imposter Solo Queue** thời 2021:

- Spend được, có lãi → QA team đẩy nhanh, scale lên **~20 triệu users**.
- **ROAS sụn xuống "bất mé"** — sản xuất content không kịp tốc độ tăng CPI.
- Spam Inter nặng → user feedback "rất nhiều quảng cáo" → drop.

> *"Hết ngưỡng luôn. Thú thật là thời điểm đấy mình cũng chưa nghĩ đến việc đẩy ROAS ra lùi hơn một chút — để FTP nó cũng được an toàn hơn."*

Hindsight: lẽ ra nên **giãn quảng cáo từ sớm** thay vì khai thác max. Hôm nay Vũ áp dụng tư duy đó cho các con sau:

> *"Bây giờ mình thấy là các mô hình mới của Lion Studios thời điểm này đang giãn dần ra về vấn đề quảng cáo — do user có chỉ số tốt hơn và đẩy thêm phần sang Việt Nam."*

---

## Hyper vs Hybrid — 2 Đường Cong Vòng Đời

Vũ vẽ 2 curve khác nhau:

### Hyper (3-6 Tháng)

- Doanh thu peak nhanh, giảm liên tục.
- CPI tăng dần → margin co lại.
- Khi sản xuất content không theo kịp → drop, không scale được.
- Đặc trưng: target D0-D1 hoà.

### Hybrid / Long-Tail (5-7 Năm)

- Doanh thu có "đường lên" sau giai đoạn đầu — khi user happy + CPI stable.
- Mỗi tháng up ~2 triệu user (con block puzzle case) → organic + paid mix.
- Đặc trưng: target D7-D60 hoà.

> *"FPV không đổi. CPI khi chúng ta target càng dài thì cực kỳ ổn định. Mà target đến D60 — cả một năm CPI nó không tăng được. Đây là lý do tại sao target càng dài hẳn dễ scale."*

Target D ngắn → CPI biến động liên tục → khó scale. Target D dài → CPI fix (anchor by long break-even target) → ổn định scale.

---

## Game Là Game, Không Phải Chỉ Kinh Doanh

Vũ phân biệt philosophy 2 cách approach:

> *"Anh làm cho người ta đem vào là một cách chơi game — chứ không phải là cách kinh doanh. Lãi ở D7 sẽ đúng khi chúng ta coi đây là kinh doanh game. Chơi game thì phải ra lợi nhuận mà. Nhưng nó không phải là chơi game."*

Khi coi là **kinh doanh**:
- D ngắn (D3) → lãi sớm, dễ ra quyết định scale/stop.
- Tối ưu ARPU/ARPPU/Pay rate.

Khi coi là **game thật**:
- D dài (D7+) → trải nghiệm user lên đầu.
- Khai thác monetize theo nhịp natural, không cưỡng ép.

> *"Em đừng bao giờ quan tâm đến chuyện làm người chơi họ — khi nó có hoà lưng, sau đó họ thất vọng em. Đấy là cách mà em làm mục tiêu của người ta bị sai."*

Khai thác đúng "progress" của user — đừng show skill đẹp nhất ngay D0 rồi sau đó không có gì để tăng.

---

## Diagnosis Drop Rate Trong Level — Đo Time-in-Level

Vũ chia sẻ kinh nghiệm puzzle: lưu **2 tham số per level**:

1. **Tham (time) in level** khi user **thắng**.
2. **Tham in level** khi user **thua**.

### Đọc Số

| Kịch bản | Diagnosis |
|----------|-----------|
| Tham thua ngắn | User không tìm ra cách giải. "Một quả tên lửa nó bay quỵch phát vào mặt, chết luôn." |
| Tham thua dài | User hiểu cách giải nhưng không xử lý được. 3 lý do: (a) nhiều vấn đề quá; (b) các vấn đề đan vào nhau bị dối; (c) chơi mệt đến mức không đủ khả năng. |
| Tham thắng ngắn | Quá dễ. |
| Tham thắng dài | Khó nhưng giải được. Đo thêm số "move" cần để win — confirm. |

### Last_down Analysis

Nếu game có thể trace action: đo **cái gì gây last_down**.

- Last_down từ boss → balance boss.
- Last_down từ obstacle → balance level layout.

> *"Last_down từ boss nó khác mà last_down từ obstacle nó khác. Em check được cái đấy thì bắt đầu ngồi suy luận."*

---

## Bán Song Song vs Bán Có Lựa Chọn — Gói Tướng Meta

Tình huống Giang: có gói tướng thứ 2 sau khi user mua gói 1. 2 chiến lược:

### Bán Song Song

- Hôm A bán con tướng 1, hôm B bán con tướng 2.
- Tất cả user đều tiếp cận được cả 2 gói.
- Tốt khi: user base lớn, cần improve ARPU broad.

### Bán Có Lựa Chọn (Gated)

- Chỉ user đã mua con 1 mới được mua con 2.
- "Improve trong tập đã pay" — squeeze whales.
- Tốt khi: user pay rate thấp, muốn deepen vertical revenue per whale.

### Anti-Pattern — Ép Sở Hữu Mới Được Mua

Vũ cảnh báo:

> *"Nếu mình ra 1 con tướng nữa thì phải thoả mãn cho những thằng chưa có con kia cũng mua thôi. Nếu mà nó phải mua con này thì lát con cuối thì chả ai mua. Nhiều điều kiện quá."*

Càng nhiều gate → càng ít user qualify → revenue thấp hơn.

---

## IAP Package Structure — 4-5 Tier Pricing

Vũ vẽ framework gói IAP cho game có tướng meta:

| Tier | Tên | Nội dung | Đặc điểm |
|------|-----|----------|---------|
| 1 | **Basic** | Reward nhỏ vùng thấp | 2 gói basic |
| 2 | **Đất bạc** | Reward cao + chỉ suất (mức value cao hơn) | Có thể đẩy đấu ảnh xuống đây |
| 3 | **Super** | Reward mắc + bắt đầu unique items | Còn 1 phần reward |
| 4 | **Mắc** | Chỉ unique cuối game | Không còn reward |
| 5 | **Chặn** | $1.5 / $2.5 — tạo so sánh | User chọn gói 2 vs gói 2.5 |

### Behaviour Cap Trên Value Discount

> *"Đến mức độ này thôi. Tức là tậm chí gói mắc của em có tỉ lệ giảm giá rất tốt — nhưng trên cơ bản nó không phải behavior của user. Chi trả tầm 5 đô. Thì dù em có khuyến mại đến ít 10 ở gói 10 đô — không mua."*

User có **mức chi trả mặc định cho thể loại game đó**. Discount không vượt cap được.

### Sau Khi User Đạt Gói Mắc → Mất Reason To Stay

> *"Họ đã mua đến mắc rồi — em còn muốn họ mua cái gì nữa? Game của em không còn có cái thứ để mà họ tiếp tục có thể spend nữa."*

Nếu meta tướng đã max → không có "vertical extension" → whale bỏ. Phải build **tướng meta mới + tường mới** sau khi user max gói cuối.

---

## Revenue Chart Shape — ERP vs Hyper

Giang chia sẻ con ERP của mình:

- D1: $5K | D2: $9K | D3: $4K

Shape: gồm về D2 → giảm D3 → bất thường.

Vũ phản biện: ERP **không nên trồi sụt** theo ngày như vậy. Đúng shape của ERP là:

- Tăng đều lên những ngày sau (D7, D14, D30).
- Không có "đỉnh sớm rồi giảm."

> *"Đối với dòng game thiên về ERP nhiều hơn — chắc chắn rồi biểu đồ web của nó sẽ đi như thế này, chứ không phải đánh như thế này."*

Diagnosis của Giang case:
- **Tỉ lệ revenue split**: 3 phần IAP / 3 phần reward (Ad).
- Vì user đạt gói cuối nhanh → mất reason để spend tiếp → revenue drop D3.

### Bài Toán Giang — Imba vào Đáy Ra

Vũ phân tích case Giang sâu thêm:

> *"Em phải luôn luôn balancing được MTV (có thể là EV, có thể là EAV) tại một checkpoint, bằng với power của nó tại checkpoint này — hoặc lớn hơn nhỏ hơn cộng trừ một con số nào đó. Chứ đừng để mất cân bằng."*

2 dạng imba:
1. **Imba xuống trong khi nạp** — user mua xong nhưng power vẫn không đủ → cảm giác bị lừa.
2. **Imba lên sau khi nạp** — user mua xong power vượt yêu cầu → không cần grind, không có reason để spend tiếp.

Giải:
- Imba có chủ ý + thời lượng giới hạn (1-2 ngày user mạnh sau khi pay).
- Tạo **tường mới** (challenge mode, content khó hơn) đặt sau gói mắc → user nạp xong cần tướng mới để vượt.
- "Khi em ra tướng mới chắc chắn rồi — lúc đó em sẽ lại cân tiếp."

### ARPU vs Pay Rate — ERP Pick

Vũ nguyên tắc cho ERP:

> *"Đối với ERP nhé — hãy cố gắng biến user free thành user nạp tiền. Khi user đã nạp tiền rồi hãy cứ dừng với họ. Cứ dừng càng kéo thì em sẽ kéo cái credit này càng cao."*

- ARPPU cao + Pay rate thấp → vài whale gánh; ARPU đi ngang.
- ARPPU cân bằng + Pay rate cao → đông user trả ít; ARPU đi lên + ổn định hơn.

ERP nên **ưu tiên Pay rate** (broad payer base) hơn ARPPU (whale-heavy). Khi user pay rồi → "cứ dùng với họ" → kéo dài relationship → LTV bền.

---

## Câu Hỏi / Chủ Đề Còn Nợ

- **Level design góc nhìn prototype** — đã chạm nhẹ, deep-dive vào Doc 4 (Level Data).
- **Mũ nét sâu hơn** — kiến trúc đặt mũ nét trong game lãi ở D7+.
- **Phân biệt CPI vs LowWatt vs LTV** trong UA workflow — phụ thuộc UA team, GD chỉ supply số.
- **Balance gói tướng meta + tường mới** — Vũ defer thành "một buổi riêng" vì độ phức tạp cao (logic gói nâng cấp, EV/EAV balancing per checkpoint, content gating sau khi user pay).
- **Revenue chart shape Giang case** — Vũ defer cũng buổi riêng.
- **UI/UX sâu hơn** — chuyển vào Doc 7 (UI/UX & Monetize).
- **Detection per chỉ số (R1/R3/R7)** — Vũ chốt cần "một buổi riêng" vì mỗi mốc retention cần thiết kế khác nhau.

---

## Thuật Ngữ Buổi Này

### Phase Dự Án
- **Prototype** — bản thử nghiệm sơ khai, mục tiêu chứng minh idea + truyền đạt gameplay nội bộ. Không có animation/asset đầy đủ.
- **MVP** (Minimum Value Product) — bản nhỏ nhất có thể cho user thật chơi, đẩy ra thị trường để thu data.
- **Feelings** — cảm giác gameplay (gameplay feel), thứ test được trong prototype qua battle simulation. Phân biệt với "Fueling".
- **Fueling** (theo Vũ) — pacing/phân bổ khai thác value qua thời gian (D0 → D7+). Khác với feelings; không phải battle simulation.
- **Base game** — định hướng triển khai cốt lõi (auto / auto có skill / auto có chỉ đạo) sau prototype.
- **Balance Scale** — bảng phân tỷ trọng tài nguyên giữa các module (core, phụ bản, PvP, sự kiện).

### Metrics & UA
- **CPI** — Cost Per Install, proxy cho "tập user".
- **CTR** — Click Through Rate, metric đầu tiên đánh giá prototype có được chấp nhận không.
- **CVI** — Cost Video Install, kết hợp với CTR để ra MPV nhưng tốn thời gian hơn.
- **MPV** — metric mục tiêu của sản phẩm (sau khi qua CTR + CVI).
- **ARPU** — Average Revenue Per User. Doanh thu / tổng user (kể cả free).
- **ARPPU** — Average Revenue Per Paying User. Doanh thu / số user trả tiền.
- **Pay rate** — tỷ lệ user trả tiền / tổng user. Cao = đông user trả ít; thấp = whale-heavy.
- **LowWatt** — phần trăm doanh thu thu hồi giai đoạn đầu (D1-D2). Game lãi D7 thường LowWatt thấp (~20-25%).
- **LTV** — Lifetime Value tổng user. Giãn inter có thể nâng LTV 60-70%.
- **ROAS / GPA** — metric UA thường target để decide scale.
- **SQI** — chỉ số chiếu (channel quality index) dùng so sánh 2 sản phẩm trên cùng hệ thống chiếu.

### Monetization
- **Inter** — quảng cáo phích thời gian, cho user nghỉ tích giữa 2 session. Không phải spam mỗi level.
- **Mũ Nét** (money knot) — điểm tiêu tiền của user trong game, nơi designer set monetization point.
- **Lãi Ở Đây vs Lãi Ở Đây Mũ** — lãi sớm (D0-D1) khó scale; lãi muộn (D3-D7+) dễ scale qua UA.
- **D3 / D7 Hoà** — break-even ở ngày 3 / ngày 7 (tổng doanh thu = chi phí UA).
- **Điểm Hoà** — ngày break-even. Càng đẩy sâu thì vùng khai thác phần dư càng rộng.

### Reward Quảng Cáo
- **WeTry / Continue** — ad reward cho phép chơi lại sau khi thua, giữ progress. Loại được bấm nhiều nhất.
- **Hint** — ad reward cho gợi ý chơi. Trung gian.
- **Booster** — ad reward cho vật phẩm hỗ trợ. Bấm ít nhất.

### Progression & Balance
- **Retention R1/R3/R7** — % user quay lại sau 1/3/7 ngày. Mỗi mốc cần thiết kế riêng (in-session vs cross-day).
- **Imba** — imbalance (mất cân bằng) giữa power user và yêu cầu content tại checkpoint.
- **MTV / EV / EAV** — metric balance dùng so sánh giá trị-tại-checkpoint với power-tại-checkpoint.
- **Tường Mới** — content/độ-khó mới ở giai đoạn sau, dùng để cân lại imba ngắn hạn sau khi user pay.

### UX
- **UI** — cấu trúc nút/màn hình (thứ designer vẽ). Hiển thị: kích thước, màu, vị trí.
- **UX** — trải nghiệm khi user thực sự tương tác với sản phẩm. **Không phải nút bấm, không phải đồ hoạ** — UX là flow/luồng thuận với suy nghĩ, expectation match, số bước thực hiện. Phải tính 10 thằng user 10 tính cách.
- **Brand Recognition** — sự nhất quán visual giữa ad creative và game thật.
- **Customize Layout** — cho user tự đổi bố cục (tay trái/tay phải) thay vì cố "tối ưu cho 2 đứa cùng lúc."

### Habit Formation & Improve Chỉ Số
- **Stack (Stuck)** — trạng thái user kẹt. 3 loại: khó hiểu, khó thực hiện, khó hình thành thói quen.
- **4 Mức Hành Vi** — Học → Rèn luyện → Thử thách → Làm chủ. Tối thiểu 4 level cho 1 motif (3 chốt 2/3/4/5 vấn đề).
- **Master Checkpoint** — điểm chuyển content mới sau khi user "làm chủ" motif cũ. Content mới phải kế thừa kỹ năng cũ.
- **Biên Độ Thói Quen** — khoảng playtime/độ khó phù hợp để form habit. Sướng quá → bỏ nhanh; khổ quá → không hình thành.
- **Ngắt Mềm (Active Disengagement)** — thiết kế để user **tự dừng** giữa session (mồi câu 1 phút, lucky spin) → tạo nhiều session ngắn thay vì 1 session dài.
- **Ngắt Cứng (Forced Break)** — user bị mất resource/win streak → bị ép dừng → khả năng cao không quay lại.
- **Mồi Câu** — quà ngắn hạn (1-15 phút) hoặc daily reward sang ngày sau, để user form thói quen quay lại.
- **Online Thời Điểm Cố Định** — quà/event vào giờ cố định, khác với online liên tục (fatigue).
- **Daily Challenge** — challenge khó 1 lần/ngày, kéo retention D28 (block puzzle 50M case).

### IAP Package Structure
- **Gói Basic** — reward nhỏ vùng thấp. 2 gói entry-level.
- **Gói Đất Bạc** — reward cao + chỉ suất, mức value vượt Basic.
- **Gói Super** — reward mắc + bắt đầu unique items. Cầu nối sang gói cuối.
- **Gói Mắc** — chỉ unique cuối game, không còn reward.
- **Gói Chặn** — $1.5/$2.5 tạo so sánh cho user chọn gói trên.
- **Behavior Cap** — mức chi trả mặc định của user cho thể loại game đó. Discount không vượt cap được.
- **Bán Song Song** — bán nhiều gói tướng cùng lúc, broad reach.
- **Bán Có Lựa Chọn (Gated)** — chỉ user đã pay gói trước được mua gói sau, deepen whale revenue.

### Diagnosis Metrics
- **Tham In Level** — time per level. Đo khi thắng và khi thua riêng — diagnose khó vs dễ vs not-engaged.
- **Last_down** — hành động cuối gây fail. Phân biệt từ boss vs obstacle.
- **CVR / PAY Rate** — % user trả tiền / tổng user.
- **MTV / EV / EAV** — metric balance giá trị-tại-checkpoint với power-tại-checkpoint.
- **FPV** — Forecast Per View. Stable hơn khi target D dài.
- **SQI** — chỉ số chiếu (channel quality index) dùng so sánh 2 sản phẩm trên cùng hệ thống chiếu.

### Ad Tricks
- **Win-Screen Pop-Up** — chuyển win/lose từ full screen → pop-up có glow. Tăng ad rate vài %.
- **Vòng Quay x2/x3/x5** — vòng quay dừng-đâu-nhân-đấy thay nút "x3" cố định.
- **Ad Sau Skill Unlock** — chen ad sau khi tặng item/skill mới để user expect cao → drop thấp.

### Triết Lý
- **Game vs Kinh Doanh** — coi là kinh doanh thì target D ngắn. Coi là game thì target D dài, khai thác natural.
- **Lý Quật Công Bằng** — ad reward không được tạo unfair với người trả tiền. Reward cho user xem ad ≤ reward cho user pay.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Video gốc: `GD Doc 3 - Phase du an.MOV` (3.3 GB, ~190 phút).
- Transcript đầy đủ: `GD Doc 3 - Phase du an.MOV.txt` (4,318 dòng, faster-whisper large-v3 chunked 20×10-phút với beam=1 fallback, re-run 2026-05-18).
- Transcript backup (run 2026-05-15 cũ, 1,500 dòng): `GD Doc 3 - Phase du an.MOV.txt.bak.20260518-090832`.
- Transcript timestamped: `GD Doc 3 - Phase du an.MOV.srt` (SRT chia theo chunk, timestamps relative trong từng chunk).
- Khóa học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
- Vị trí trong khóa: **Buổi 3 — Phase Dự Án** (nằm giữa Doc 2 Level Design và Doc 4 Level Data; Part 2 + Part 3 mở rộng sang chủ đề của Doc 7 UI/UX & Monetize).
- **Date updated 2026-05-19** — re-compile từ transcription 4,318 dòng (~3× content so với 1,500 dòng cũ): thêm Part 3 (Improve Chỉ Số framework với 17 sections mới — content vs theme, UX deep dive với case iPhone/Úc/Nhật, 4-phase habit formation, ngắt mềm/cứng, Daily Challenge 28-day, ad timing vs skill unlock, hierarchy reward theo dòng game, win-screen ad tricks 18 versions, IAP package structure 5 tier, revenue chart shape cho ERP). Tham khảo entries cũ:
  - 2026-05-15 — bổ sung Part 2 sau khi re-transcribe đầy đủ; fix label "Fueling/Feelings" theo audio gốc.
