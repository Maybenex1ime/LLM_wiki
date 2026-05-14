---
title: "GD Doc 3 — Phase Dự Án: Prototype, MVP & Fueling (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 3 - Phase du an.MOV"
date_added: 2026-05-14
tags: [video, course-transcript, game-design, prototype, mvp, fueling, monetization, mobile-games, hyper-casual, vietnamese]
aliases: ["GD Doc 3", "Buổi 3 Phase Dự Án", "Prototype vs MVP Vũ Hiệp"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-02-level-design]]"
  - "[[negaxy-iec-gd-doc-04-level-data-and-iap]]"
summary: "Buổi 3 (Vũ + Hiệp + Giang): phase dự án từ Prototype → MVP → vận hành. Phân biệt Prototype vs MVP, mục tiêu test ở từng phase, fueling và base game, balance scale tài nguyên giữa các module, lý do test bản không quảng cáo, định nghĩa lại Inter, và vì sao day 7 hoà dễ scale hơn day 3 hoà."
---

# GD Doc 3 — Phase Dự Án: Prototype, MVP & Fueling

**Speakers:**
- **Vũ** — Lecturer chính (xưng "mình"/"anh", người dẫn buổi).
- **Hiệp** — Co-lecturer (chia sẻ về test prototype không quảng cáo, case giãn inter, day 7 hoà).
- **Giang** — Học viên có dự án thực tế đang vận hành (đưa quan điểm về day 7 hoà dễ scale).
- **Thiên** — Học viên (đặt câu hỏi về tham chơi vs CPI khi target hyper/bitcoin).
- Một số học viên khác đặt câu hỏi về D3/D7, CTR baseline, cách tính level cần cho retention.

**Format:** Buổi học trao đổi 2 chiều, ~120 phút, tiếng Việt. Tiếp nối "feeling của game" từ Doc 1 và đặt nền cho Doc 4 (Level Data, vào sâu phần level design số). Có nhắc lại Inter:Reward ratio đã giảng ở Doc 2.

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 3 - Phase du an.MOV` (video gốc) + `GD Doc 3 - Part 1.cleaned.txt` (transcript đã cleaned, 1,100 dòng).

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

## Fueling Trong Prototype — Vì Sao Test Khó

Fueling (kỹ thuật giả lập trận đấu / battle simulation để verify gameplay loop) là phần test hơi đặc thù trong prototype. Vũ lấy ví dụ con game đá bóng — codename "S3":

- 11 cục tròn (cầu thủ) bên này, 10 cục bên kia.
- Phân loại bằng chỉ số + màu (xanh — bình thường, đỏ — Legend, tím — Epic).
- Bấm auto cho 2 đội đánh nhau → xem có tự generate được một trận bóng không.
- Có tự ghi bàn, kết thúc trận, đá penalty — *"là đủ xong được một cái nghi thức của Prototype."*

Tại sao fueling khó test trong prototype:

> *"Fueling đoạn này test sẽ hơi khó. Không phải đơn giản — bởi vì fueling này chỉ fueling đúng mức độ của gameplay thôi. Các bạn chưa nhìn thấy level design trông mặt mũi nó ra làm sao, các bạn cũng chưa nhìn thấy hình ảnh của con game nó chạy mức độ mượt mà như thế nào cả."*

Performance đo qua prototype cũng hạn chế — bản chất performance còn phụ thuộc rất nhiều thứ bên ngoài bổ trợ (animation, asset 2D vs 3D, va chạm vật lý). Prototype chỉ cho biết logic gameplay có đúng không, không kết luận được performance cuối.

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

## Anti-Pattern Phổ Biến — Lái Theo User

Một số anti-pattern xuất hiện trong buổi:

- **Định lượng resource bằng "user thiếu rồi bù"** — Vũ note: không sai nhưng là loop đuổi theo user. Nên vẽ đồ thị trọng số trước.
- **Test prototype có quảng cáo** — không tách được chất lượng idea và mũ nét.
- **Spam inter sau mỗi level** — *"đây tôi không hề đúng đường luôn, nhưng bài toán để làm thì người ta lại ở đây."*
- **Target D0/D1 hoà cao** — UA không scale được, *"các bạn không chạy được dụng chạy luôn."*
- **Chứng minh 1 cái với nhiều biến số** — không biết đúng/sai do biến nào.

---

## Câu Hỏi / Chủ Đề Còn Nợ

- **Level design góc nhìn prototype** — đã chạm nhẹ, deep-dive vào Doc 4 (Level Data).
- **Mũ nét sâu hơn** — kiến trúc đặt mũ nét trong game lãi ở D7+.
- **Phân biệt CPI vs LowWatt vs LTV** trong UA workflow — phụ thuộc UA team, GD chỉ supply số.

---

## Thuật Ngữ Buổi Này

- **Prototype** — bản thử nghiệm sơ khai, mục tiêu chứng minh idea + truyền đạt gameplay nội bộ. Không có animation/asset đầy đủ.
- **MVP** (Minimum Value Product) — bản nhỏ nhất có thể cho user thật chơi, đẩy ra thị trường để thu data.
- **Fueling** — kỹ thuật giả lập trận đấu/battle để verify gameplay loop (vd auto cho 2 đội đánh nhau xem có ra trận hoàn chỉnh).
- **Base game** — định hướng triển khai cốt lõi (auto / auto có skill / auto có chỉ đạo) sau prototype.
- **Balance Scale** — bảng phân tỷ trọng tài nguyên giữa các module (core, phụ bản, PvP, sự kiện).
- **CPI** — Cost Per Install, proxy cho "tập user".
- **CTR** — Click Through Rate, metric đầu tiên đánh giá prototype có được chấp nhận không.
- **CVI** — Cost Video Install, kết hợp với CTR để ra MPV nhưng tốn thời gian hơn.
- **MPV** — metric mục tiêu của sản phẩm (sau khi qua CTR + CVI).
- **Inter** — quảng cáo phích thời gian, cho user nghỉ tích giữa 2 session. Không phải spam mỗi level.
- **Mũ Nét** (money knot) — điểm tiêu tiền của user trong game, nơi designer set monetization point.
- **Lãi Ở Đây vs Lãi Ở Đây Mũ** — lãi sớm (D0-D1) khó scale; lãi muộn (D3-D7+) dễ scale qua UA.
- **D3 / D7 Hoà** — break-even ở ngày 3 / ngày 7 (tổng doanh thu = chi phí UA).
- **LowWatt** — phần trăm doanh thu thu hồi giai đoạn đầu (D1-D2). Game lãi D7 thường LowWatt thấp (~20-25%).
- **LTV** — Lifetime Value tổng user. Giãn inter có thể nâng LTV 60-70%.
- **Điểm Hoà** — ngày break-even. Càng đẩy sâu thì vùng khai thác phần dư càng rộng.
- **SQI** — chỉ số chiếu (channel quality index) dùng so sánh 2 sản phẩm trên cùng hệ thống chiếu.
- **ROAS / GPA** — metric UA thường target để decide scale.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Video gốc: `GD Doc 3 - Phase du an.MOV`
- Transcript cleaned: `GD Doc 3 - Part 1.cleaned.txt` (1,100 dòng — duy nhất 1 Part)
- Khóa học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
- Vị trí trong khóa: **Buổi 3 — Phase Dự Án** (nằm giữa Doc 2 Level Design và Doc 4 Level Data).
