---
title: "GD Doc 1 — Vai Trò GD, Thuyết Phục Sếp & Tư Duy Số Liệu (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 1.mp3"
date_added: 2026-05-14
tags: [video, course-transcript, game-design, mindset, gd-role, monetization, ua, ecpm, vietnamese, mobile-games]
aliases: ["GD Doc 1", "Buổi 1 Game Design Course", "Vai Trò Game Design Vũ Hiệp"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-02-level-design]]"
  - "[[negaxy-iec-gd-doc-04-level-data-and-iap]]"
summary: "Buổi 1 khóa Game Design (Vũ + Hiệp): định nghĩa vai trò GD trong cỗ máy sản xuất, kỹ năng define cho code/art, tip phỏng vấn GD, 5 level idea để thuyết phục sếp, công thức LTV > CPI, balance khó/booster/ad đặt từ trước, chuyển đổi IAA → IAP, ECPM là biến không kiểm soát được."
---

# GD Doc 1 — Vai Trò GD, Thuyết Phục Sếp & Tư Duy Số Liệu

**Speakers:**
- **Vũ** — Lecturer chính (xưng "mình"/"anh", người dẫn buổi)
- **Hiệp** — Co-lecturer & host (mở buổi, đặt vấn đề, bổ sung góc UA/UX/ECPM cuối buổi)
- **Giang** — Học viên có nhiều dự án dài hạn đang vận hành (chia sẻ kinh nghiệm hyper → hybrid, mô hình hai studio GAC)
- **Đạt** — Học viên, sản phẩm RedBone của Lyng Mobi (hỏi nhiều về xếp deadline, daily login)
- **Đảng / Nam / Lâm / Trúc / Quân** — Các học viên khác (hỏi creative-first vs gameplay-first, chase trend, low-CPI vs low-LTV)

**Format:** Buổi học mở khóa ~150 phút, tiếng Việt. Vũ + Hiệp đặt mindset cho 7 buổi tiếp theo. Buổi này KHÔNG đi sâu vào "tài sản" (asset characteristics) như Doc 2 reference lại — phần đó có thể đã được nhắc trong slide khung mà Hiệp dùng để mở Doc 2, hoặc nằm trong segment audio không capture được. Doc 1 (audio) tập trung vào **vai trò game designer**, **thuyết phục sếp ra quyết định dự án**, và **dòng tiền IAA/IAP/eCPM** theo góc nhìn business.

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 1.mp3.txt` (~4,921 dòng whisper transcript; head/tail có hallucination chào hỏi/setup mic, đã trim).

---

## Đặt Rule Cho Khóa Học

Vũ mở đầu bằng 3 rule giao kết cho cả 8 buổi:

1. **Hai buổi nội dung + nghỉ giữa giờ ngắn** — học liên tục một mạch quá căng, "10 phút với nhau".
2. **Push back ngay nếu thấy không đúng** — *"Mọi người cảm thấy không đúng, không phù hợp — mọi người nói luôn. Chúng ta sẽ tìm một phương án tiếp cận khác."* Tránh để học viên mất tiền + thời gian rồi mới phát hiện không hợp.
3. **Sẽ có recording sau buổi** — Vũ gửi lại link, dùng cho bạn mới của VNP onboard.

Hiệp nhắc lý do tổ chức khóa: chất lượng GD năm nay (theo cảm nhận từ các studio Stay-at-home) tụt đi, các công ty đều thấy "vẫn còn giới hạn về kiến thức GD". Vũ và Teddy (anh đồng hành xây nội dung) muốn dạy *"kiến thức thực tế nhất, chứ không phải những thứ xa xôi"* — học viên đều là người đã làm game, mỗi buổi sẽ đối chiếu trực tiếp với sản phẩm của họ.

---

## Vai Trò Của Game Designer — Mắt Xích Trong Cỗ Máy

Đoạn này Vũ dành thời gian nhiều nhất. Mở luận điểm bằng việc thẳng thắn chỉ ra một anti-pattern phổ biến:

> *"Các bạn nói cái gì thì cốt phải làm cho. Các bạn nói cái gì là phải làm thế nào với đấy. Thực ra thì góc nhìn của mình hơi khác. Mình nghĩ cái design nó là một mắt xích trong cả một cỗ máy."*

Designer **không phải vị trí ra lệnh** mà là một component trong dây chuyền. Vai trò "đúng" là **define đủ thông tin để các mắt xích khác làm việc được**. Nếu code không làm nổi, nếu art kêu deadline không đủ — *"vậy các bạn đã hoàn thành vai trò của mình hay chưa?"*

### Define Cho Code

Code làm việc bằng *"đúng sai, là luồng, là hàm, là logic"* — designer cứ mô tả "lượn văn" thì code không hiểu. Vũ ví dụ:

- Game 2 nhân vật, một skill lửa, một skill băng. Khi 2 effect đè lên một mục tiêu → **kết quả là gì?** Băng đông cứng nhưng bị rã đông? Cả hai cancel nhau? Sinh ra một effect mới (steam)? *"Đó là quyền của các bạn — nhưng bạn phải define được cái đầu ra."*
- Game vật lý (RedBone của Đạt): GD cần define **trước** các tham số (kích thước, khối lượng, chất liệu cho ma sát), **sau đó** mới đến phần tuning bằng cảm giác. Đạt thừa nhận team không define rõ ngay từ đầu, chủ yếu "cảm giác và điều chỉnh lại".
- Khi user nhấn nút gia tốc: đồ thị gia tốc thế nào? Lên đến mức nào thì plateau? Khi nhả tay thì rơi xuống 0 hay giảm dần? Booster có ảnh hưởng tốc độ không?

Quote về dây chuyền hỏi-đáp:

> *"Game design là người tưởng tượng ra game, vì thế cho nên là cái sự tưởng tượng đấy đôi lúc nó vớ vẩn, thiếu logic và nó chưa nghĩ được kỹ cạnh kẽ. Trong khi dev thì họ lại là những người hoàn toàn ngược lại — họ là người làm việc thực tế. Cứ liên tục là quá trình vấn đáp như thế. Nếu người nào define nhiều thứ ngay từ lúc đầu, quá trình này sẽ giảm bớt — nó không hết đâu."*

Nguyên tắc: *"Hãy giảm bớt thời gian từ cái đoạn làm đúng, để tăng cái đoạn làm hay lên."* — Vũ chia dự án thành 2 đoạn: làm đúng (function works) và làm hay (polish). Define tốt → đoạn 1 ngắn → có chỗ cho đoạn 2.

### Define Cho Art

Vấn đề điển hình: *"Các bạn art sẽ có xu hướng vẽ từng chi tiết đẹp, thay vì đưa ra một tầm bố cục đẹp."* Art thường không biết hết về ràng buộc kỹ thuật hay quy chuẩn timeline dự án => Cần đưa ra giới hạn, khung để art vẽ và sáng tạo theo

Tower Defense 3D: thiết bị xử lý max ~100k tris, 80 mob cùng màn chơi → mỗi mob chỉ được ~3k tris. Nếu art vẽ con boss 15k tris vì "đẹp" → vỡ trận. GD phải đưa tham số trước.

Color clash ví dụ: red boom đỏ. Một effect biến nó thành golden → bỗng dưng cùng màu vàng với toàn bộ quân đồng minh khác, lẫn vào nhau. Designer phải nghĩ trước những combo color như vậy.

### Daily Login — Case Study Define Trước

Đạt hỏi sâu về Daily Login. Vũ liệt kê 3 mô hình:

1. **7-day loop, lặp lại** — reward ô to dễ vẽ art (1 ngày 2-3 quà cũng ok).
2. **28-30 day no-loop, miss thì bỏ qua hôm đó** — phải design state "disabled icon".
3. **28-30 day no-loop, miss thì tiếp tục hôm sau (rồi 1 hôm sau nữa)** — không ép user vào nhịp.

Bài học không phải "loại nào đúng" mà là **GD phải define ngay từ đầu** mục đích Daily Login để làm gì. Sau đó cân bằng reward sao cho UI/UX truyền tải đủ tầm quan trọng → user dù bận thế nào cũng vào 1 phút lấy reward.

Hiệp bổ sung:

> *"Em mất đậm trong cái Daily Login — nó không hề quan trọng như việc đấy, thì người ta mới không còn muốn ngày hôm sau. Nhưng nếu ngày D3 đã làm cho người ta hiểu rằng tôi sẽ phải đăng nhập liên tục D4, D5, D6, D7 để nhận cái này, thì hôm sau bỏ ra 1 phút thôi log in, xong rồi đi chơi với bạn gái — chuyện rất bình thường."*

Anti-pattern Daily Login: design xong reward → đến cuối thấy không còn quà gì để cho → ngày 28 phải bỏ legendary item vào → user thấy *"từng ngày bình thường không có sức nặng, không thấy quý giá"* → cãi nhau giữa GD/art/operations để dồn quà ra đầu.

---

## Tip Phỏng Vấn Game Designer

Câu chuyện này lúc đầu là chia sẻ "nỗi đau" tuyển GD, nhưng Vũ + Hiệp đào sâu thành playbook cho người tuyển.

### Tại Sao GD Khó Tuyển

- **Không có bằng cấp** — art có portfolio, dev có chứng chỉ, GD chả có căn cứ gì.
- **Damage tiềm năng cao nhất trong team** — Giang note: *"Các bạn art hay dev nếu làm sai thì chỉ một mình các bạn đi làm lại. Nhưng GD làm sai thì tất cả các bộ phận khác phải đi sửa lại."*
-> Role nhạy cảm, khó chưng minh.

### Test Phỏng Vấn (Vũ)

1. **Bắt mở điện thoại** — xem ứng viên đang chơi game nào, bắt phân tích. *"Cho mình xem điện thoại, bỏ ra, trời ơi — bên trong toàn clan, class, liên minh thoại mấy cái — có vẻ không phù hợp lắm nhỉ. Anh em chưa từng chơi dòng game này không có trải nghiệm, bây giờ vào đây đưa toàn chức năng cao siêu này phải gói."*
2. **Pick GD có background kỹ thuật** — Vũ thiên chọn ~1 nửa GD có background dev: *"Họ sẽ không có ấy bậc, họ sẽ rất sắc đến mặt kỹ thuật. Họ sẽ sắc một chỗ — nếu họ giải quyết không đúng thì rất ok."*
3. **Yêu cầu chơi nhiều game cùng dòng** — không chỉ cài và lướt qua game play, mà phân tích cấu trúc bên trong. *"Cái việc chọn người vào một vị trí GD nó khó hơn — không có bằng cấp, và khi phân tích một game các bạn bảo em chưa chơi game này, hoặc bạn phân tích một game cùng mình mà mình cũng chưa chơi — thế là vô cùng."*
4. **Chỉ định một game cụ thể, yêu cầu phân tích** — để xem góc nhìn của bạn. Hoặc đưa con game của công ty mình, để bạn ấy chơi như user mới và so sánh với game khác bạn đã chơi.
5. **Cẩn thận hyper casual 10 phút onboarding** — trong 10 phút đầu hay nhất đã được dồn vào. Nhưng level 40-50 mới ép gating IAP thì chơi 10 phút trong phỏng vấn chưa tới được → góc nhìn ngắn.
6. Đo khả năng cải thiện game 

### Hiệp's Tip — Đo Khả Năng Cải Thiện

Round 1: hỏi *"thời điểm con game đó hot lên, các chỉ số như thế nào?"* — test xem ứng viên có quan tâm số liệu để tối ưu hay không. *"Không để ý cái đấy → loại đúng luôn thời điểm đấy. GD không chỉ làm phát triển, mà còn quá trình tối ưu nữa."*

Round 2: *"Bạn đã tối ưu nó như thế nào?"* — bao gồm play time, retention. Bạn ấy có chỉ ra điểm yếu của bản đầu tiên không, có rút kinh nghiệm cho con sau không. *"Những bạn nào mà tôi yêu được thì là bạn có khả năng cải thiện được trong tương lai."*

Trường hợp ứng viên từ chối tiết lộ chỉ số công ty cũ → **đánh giá cao** (đạo đức bảo mật) chứ không loại.

---

## GD Phải Cover Cái Gì — Tranh Cãi Về Scope

Giang đặt câu hỏi: training fresher / intern lên thì các bạn OK với việc làm breakdown, vẽ flow chart, dataflow. Nhưng có bạn năm kinh nghiệm bảo *"đấy không phải phần việc của em, em thuần làm GD, em chỉ mô tả chức năng công năng thôi"*. Hỏi mọi người chia công việc thế nào.

Vũ trả lời: bên ngoài nước (Vũ làm với Trung Quốc) thì cycle là **doc → break down → flow chart → dataflow diagram**. Đến đoạn dataflow, *"cốt gần như là đoạn đọc phía trên chỉ để hiểu cái này làm cái gì thôi — đa phần nó xem dataflow chạy dữ liệu từ đâu sang, mỗi chức năng nó nhận cái gì, trả cái gì, trả về chỗ nào."*

Lập luận của Vũ:
- Người **nghĩ ra** function là người hiểu sâu nhất. Bộ phận khác có thể làm, nhưng không thể tốt bằng. => Cần phải cover được nhiều trường hợp để giảm thời gian của quá trính làm đúng
- Chỉ một vài role đặc thù (script writer, environment artist) tách riêng được vì *"công việc của ông ấy chỉ có viết chuyện thôi"*.
- Còn lại — concept, function, balance — *"đâu liên quan gì việc không làm? Tắc anh em cũng thỏa mãn hết rồi."*
- **Mọi con game đều có giới hạn của nó**

Với dòng game mobile, GD cần phải có thêm kiến thức về marketing, nhân khẩu học -> GD ở Việt nam ko có trường lớp nào quy chuẩn

---

## Setup Buổi 1 — 5 Việc Phải Nghĩ Khi Start Dự Án

Vũ liệt kê sơ bộ, hứa đào sâu ở các buổi sau:

1. **Xây base — version đầu** — Anti-pattern: version đầu một kiểu, version 2 phát triển 180 độ vì *"không tư duy sâu với con game, sau cứ thích cái gì phát triển cái đó"*. Ví dụ một bạn được làm idle puzzle, thêm vài function, đến một hồi *"chuyển từ puzzle thao tác đơn giản sang một con tay chân miệng cuồng luôn"*. Vũ vẫn để bạn làm rồi đo data tự thất bại — *"3 tuần"* — để bạn học bằng kết quả.
2. **Quan tâm tới giá** ngay từ đầu (CPI ballpark, target LTV).
3. **Phân tích data** — define ngay những metric cần thiết: review rate, restart rate, booster usage rate. *"Ngày xưa làm code, anh code à? Ừ, OK. Thế phân tích data sẽ rõ đúng không? Trong chức năng này của ông cần data gì? Có chỉ số A, B, C của bản này, X, Y, Z cho bản sau."*
4. **Scope — thu hẹp dự án** xuống mức minimum để valid sản phẩm.
5. **Xác định loại sản phẩm** ngắn hạn (chase trend) vs dài hạn — quyết tâm rõ vì 2 hướng yêu cầu khác nhau hoàn toàn.

---

## Idea-First vs Creative-First — Hai Workflow Cùng Tồn Tại

Hiệp hỏi Giang và team Nam (Trúc) về việc khi start dự án mới, đi từ creative hay từ gameplay.

### Creative-First (Giang, Nam)

Team marketing nghiên cứu thị trường + creative trước. Win creative → feedback ngược cho GD viết kịch bản phục vụ creative đó. Nam mô tả: *"Đi từ phía là những ý tưởng game mới, bọn mình sẽ làm nhiệm vụ là nghĩ các kịch bản creative cho GD. Vì ý tưởng game mới nó chưa có tham chiếu gì ở bên ngoài — nó có thể là mix, có thể là tan trộn nhiều thứ."*

GD trong workflow này phải nghĩ luôn các tiêu chí phim creative kèm theo (chơi ngu, hack & slash để fake đã tay, cá tính tranh nhân vật). 70-80% copy từ game tham chiếu, 20-30% sáng tạo riêng — đào kỹ creative tham chiếu để biết giống/khác chỗ nào.

### Gameplay-First (Vũ trước đây)

Team xuất phát từ ý tưởng game → bộ phận marketing dựng creative để quảng cáo. *"Marketing thường có xu hướng nhìn vào sản phẩm để tạo ra creative, nhiều hơn là việc từ ý tưởng lên từ creative."*

### Quay Quảng Cáo Không Cần Là Game Thật

Giang chia sẻ thêm: có level "đặc biệt kỳ cục" được xếp tay riêng chỉ để quay video — *"Xếp hình trái tim, ngôi sao, mặt mèo, để cho vào game có thể không, nhưng họ vẫn cứ làm để chỉ quay creative thôi."* Thậm chí có thể *"phá cả cái core gameplay của con game"* để có shot đẹp. Test trên video chạy A/B trên Facebook ad nhanh hơn test trong game.

Nam thêm: bên anh GD dựng creative bằng phần mềm (timeline editor), không phải dựng trong engine game — *"các bạn ấy dễ kiểm soát hơn"*.

Hiệp đóng segment: cách Giang/Nam là *"góc nhìn em phải học. Lúc trước bọn em đi từ ý tưởng — và bọn em cũng chưa thường về đấy bao giờ."*

### Khi Nào Creative-First Win

Hiệp phân loại:
- **Game cơ chế đơn giản (hyper casual)** — creative thể hiện gameplay gần như toàn bộ → creative là yếu tố quan trọng nhất để start dự án.
- **Game phức tạp hơn (puzzle, hybrid)** — *"creative chỉ là một bộ phận chúng ta quyết định làm hay không"*. User nhìn creative chưa đủ ra toàn cảnh, GD vẫn phải build các cơ chế phụ trợ.

---

## Chase Trend — Sản Phẩm Ngắn Hạn Đừng Đối Xử Như Dài Hạn

Lâm hỏi: nếu mình bắt trend với một creative, đến lúc sản phẩm ra thì trend đã xuống, làm sao biết được?

Hiệp trả lời bằng cách lật ngược câu hỏi: *"Em hướng đến là cái gì? Một sản phẩm ngắn hạn bắt trend, hay một sản phẩm dài hạn mà em vô tình lấy trend làm UA nguồn?"*

Khung suy luận:

- **Chase trend = sản phẩm ngắn**: KPI là tốc độ ra hàng, *"em phải biết là cái sản phẩm em hướng đến là sản phẩm gì. Chúng ta không thể bắt một trend để làm sản phẩm dài hạn được"*. Trend chỉ kéo dài 1 tháng → cho phép 1-2 tuần làm sản phẩm.
- **Dài hạn**: không dựa vào trend. Dựa vào pool thị trường lớn — pool lớn → CPI giảm → eCPM, retention, monetization tốt hơn theo dây chuyền.

Anti-pattern Hiệp warn: *"Đừng giải quyết bài toán 'tôi làm xong thì mất trend'. Hãy tránh không rơi vào luồng suy nghĩ đó từ đầu — cộng trừ nhân chia các vị trí, chúng ta đừng có xáo trộn cố tình tạo ra nó thành câu cao lên nhưng không gãy nhẹn."*

Tài hỏi follow-up: nếu hết trend mà collect được lượng user đều, có thể tăng LTV cho nhóm đó được không. Vũ trả lời case Imposter Solo Queue: khi trend xuống, team đã thử 3 hướng:
1. Thay đổi tần suất quảng cáo (delay deeper, ngắt mạch giữa) → ổn.
2. Chuyển sang IAA + IAP — *"có một lượng user chuyển sang IAP"*.
3. Clone sang con trend mới (Fall Guys) — *"có sự thay đổi"*.

Bài học: phải biết **trend mang lại gì** (CPI thấp, FPV giữ, giá trị đầu vào) và **user mang lại gì** (LTV qua tương tác in-app, giá trị con game) — tách rạch ròi 2 đầu. Khi trend tắt, CPI tăng → phải tăng LTV bù lại bằng kéo dài core loop. Ví dụ Mob Control: hyper → hybrid bằng cách *"thay vì core loop từ 1 đến 2, người ta làm 1 → 1.5 → 1.8 → 1.9 → 2"* — kéo lifetime dài qua việc đi đường vòng nhưng vẫn satisfying.

---

## 5 Levels Of Idea — Thang Đo Thuyết Phục Sếp

Đạt hỏi: với game lớn (Vico-scale), điều gì thuyết phục được CEO/leader bỏ vốn vào idea của GD. Vũ trả lời bằng cách phân thành 5 level thuyết phục, đi từ kém nhất lên.

### Level 1 — "Anh em lấy game puzzle đi"

*"Làm gì sếp không nó? Đấy, thế là lúc nào lên đấy tưởng là em sẽ lấy game puzzle để nói cũng chưng — tóm lại là nó như không nó."* Mất giá trị bản thân. **Đừng đưa idea kiểu level 0.**

Mô tả game như một user có *"đánh nhau, có đi phụ bản, cầm cung cầm súng cầm dao"* — *"rất là sơ khai"*. CV / Ether Refresher đầy kiểu này. Không hiệu quả.

### Level 2 — Bóc Tách Element

Liệt kê những gì game có: vũ khí thì chỉ số gì, quái thì chỉ số gì, level cần chỉ số gì. *"Tóm lại là bắt đầu các bạn có những cái đường dòng các bạn bắt đầu làm."*

### Level 3 — Biết Cách Triển Khai

Biết các thứ vừa list được làm bằng cách nào: giao tiếp với code thế nào, với art ra sao, balance tính toán bên trong. Khảo sát timeline sơ bộ — *"xếp giao cho các bạn làm 6 tháng thôi, cuối cùng các bạn list lên một hồi khảo sát sơ bộ thấy dự án phải 8-10 tháng, 1 năm — khá khoai đúng không."*

### Level 4 — Biết Chỗ Cúng Tiền (Monetization Logic)

Không chỉ "em sẽ bán pack X, đặt booster Y, view ad Z" — mà phải biết **tại sao user phải chi trả hoặc xem ad chỗ đó**. Vũ ví dụ Match-3:

```
Level 5-7: 1 level cần dùng 1 booster
Level 8-9: 1 level cần dùng thêm 1 booster (hết free)
Level 10+: bắt đầu phải view ad / mua booster
```

Mỗi điểm bán/ad phải có hard reason gắn vào level design. *"Không phải là bạn nghĩ là có cái này nó sẽ booster nó phá hàng ngang, phá hàng dập."*

Cảnh báo: nếu game khó tới mức *"xem 2 cái quảng cáo rồi nó mới không thể qua được, đến khi nó chơi lại nó nghĩ — ồ bây giờ chơi level này, 3 quảng cáo nó không qua được, bây giờ xem 5 cái, nó mới phải"* → user ngán → bỏ.
-> **Phải có tiêu chí xác định độ khó level và cách cân bằng độ khó trong level, để tìm được điểm mà user hài lòng và sẵn sàng bỏ tiền**

Cùng level 4 này Vũ giới thiệu **2 case "chặn tài" để model monetization**:

#### Tower Defense — Chặn Bằng 2 Cọp

Map có 2 cọp (entrance). Các level trước thả quân chỉ vào 1 cọp → user quen xây dựng phòng thủ 1 bên. Đến level 10, wave thứ 2 (1920) **đột ngột thả vào cọp 2 trắng tinh** — user không có gì phòng thủ bên đó. Lúc này lựa chọn:
- Xem ad → nhận 1 quả tên lửa / 1000 tiền xây ngay 3 chỗ.
- Bỏ cuộc, replay từ đầu, biết lần sau wave 18-19 phải để dự phòng.

Vũ gọi đây là *"rainbow design"* — không chỉ tăng chỉ số mà đa hướng cách chặn.

#### Tower Defense — Khắc Hệ Quân

Game có hệ Red / Blue / Green. Wave đầu toàn red → user dồn gold nâng cấp blue (counter red). Hết gold → đột ngột thả green vào → quân của user khắc kiểu hết. *"Không cần tăng chỉ số, chỉ cần thay đổi sức lực quân thôi — bây giờ còn toàn quân lại level 1, làm gì? Xem ad, nhận tiền nâng cấp, hoặc mua."*

#### Match-3 — Biến Ẩn

Match-3 có 2 phần:
- **Hiển thị**: blocker, mục tiêu, board → user replay sẽ thấy ngay.
- **Ẩn**: tỷ lệ chip drop, digital random.

*"Cái yếu tố ẩn là các cái chip bên trong — các tỷ lệ chip bên trong. Phần level design lúc trước rất là dễ hoặc rất là khó. Nhưng chỉ cần bạn mua 1 cái booster thôi, tương ứng level bạn twit sang 1 cái data ẩn rồi sao đó dễ hơn — user sẽ dễ chịu hơn."*

Đây là điểm bán booster có lý do thực sự, không phải bừa.

### Level 5 — Idea Đặc Sắc / Original

Bạn không chỉ trả lời được "tôi monetize ở đâu", mà còn vượt ra khỏi vùng an toàn: *"con này CPI giữ được khoảng 2 đô — bài toán giải quyết là, một là có cách nào đặc sắc cho con chú giải quyết hạ CPI xuống. Hai là tính CPI, LTV ít nhất phải vượt qua được 2 đô."*

Vũ note pattern thuyết phục: *"Cái thứ mình thuyết phục nghe có vẻ có lý, làm gì mà chưa chắc thành công. Nhưng cái gì mà nghe đã khó vào rồi, khả năng thành công không cao."*

### Yếu Tố Sếp (Bonus, Vũ Tiếc Lộ Riêng)

Có 3 yếu tố ngoài kỹ năng:
1. **Sếp đang quan tâm dòng nào** — ấn tượng cá nhân. *"Khi mà mình thuyết phục anh Huy thì anh Huy thích — chính thôi."* Hoặc *"em nghe bảo anh Thơ ở bên Xuân Hát làm một Match 3 thành công lắm"* → thuyết phục dễ hơn.
2. **Ấn tượng về bản thân người nói** — fresher / intern thuyết phục 6-month project khó hơn người có 4 năm trong công ty + đồng thuận từ các vị trí khác.
3. **Bằng chứng (số liệu) — không ai bỏ qua được**, nhưng người mới hay collect không đủ, collect không trust được, hoặc *"collect thông tin lợi cho mình, không có lợi thì đọc qua"* (bias).

---

## Công Thức LTV > CPI — Khung Bảo Vệ Dự Án

Hiệp đặt ra workflow chi tiết để bảo vệ dự án với sếp bằng số. Đây là phần ông nhấn mạnh nhất.

### Bóp Bài Toán Thành Inputs/Outputs

```
Input vào con game ─→ CPI (cost per install)
                  ├─ pool thị trường
                  ├─ chen / trend
                  ├─ LTV reference
                  ├─ kim loại (kinh đô)
                  ├─ cơ chế đang viral
                  └─ chân phục creative
                  
Output từ con game ─→ LTV (lifetime value)
                   ├─ time chơi
                   ├─ retention (D1, D3, D7, D30)
                   ├─ A-B-B metric (qua tuần 2009 trước)
                   └─ Impression (số inter / time)

Điều kiện bán dự án: LTV > CPI
```

### Tính impression Từ Session

Hiệp đưa ví dụ tính cụ thể:

```
Time chơi target: 30 phút / session
Break down (đã thảo luận buổi trước): 10 inter ads
Retention chuỗi: D1 = 40%, D2 = 30%, D3 = 20%, D4 = 10%

Tổng impression đến D4 = 10 + 4 + 3 + 2 + 1 = 20 ads/user
```

Có thể nhân với eCPM tham chiếu thị trường → ra LTV ước lượng.

### Tránh Trường Hợp "Nói Mồm"

> *"Đây là cái mà các bạn cần để bảo vệ với sếp, không phải mồm. 2 cái này đúng là phải tự nhiên là có số ít. Còn cái việc làm như thế nào, cái quota này các bạn chính là các sếp dám bỏ thể lợi."*

Sếp dám bỏ 2 tuần — nếu LTV ước lượng > CPI nhưng không làm được — *"đây là dự án mới của lá. Đây biết là tôi đã sử dụng — tùy mỗi công ty và mỗi sếp của mình."*

### Ngoại Suy Cho Game Dài Hạn

Đảng phản biện: với game dài hạn, đến D60 mới hòa được CPI, mà test chỉ chốt số ở D3-D7. Hiệp trả lời:

- Phải có **kinh nghiệm ngoại suy** từ D7 → D30 → D60.
- *"Bên ngoài (Trung Quốc) thì nó hay dùng công thức ngoại suy nhiều hơn."*
- Áp dụng đúng công thức chỉ ~1% chốt quyết định — *"nó sẽ không 100% được, và về sau có rất nhiều biến số khác."*
- Phụ thuộc vào **năng lực của team** — nếu GD biết tối ưu D7 đến ngưỡng X, thì ngoại suy D60 đúng. Nếu chỉ làm được D3 đẹp mà D7 đã tụt thì công thức sai.

Vũ note: ngày xưa mua game Trung Quốc ở VDC, *"các anh đi mua game của Trung Quốc, game họ chạy rồi, tất cả mọi thứ chỉ số là retention, time engagement, chi tiêu chung bình. Rồi mình mua về — nhiều khi chỉ số ở nước ngoài và Việt Nam không đúng nhau."* Trust số thị trường khó.

### Sensor Tower? Không Trust

> *"Đến bây giờ ở nhà bắt đầu có một số công cụ như sensor tower hay là mock chỉ số ra — nhưng mà anh em hỏi thật, anh em nhìn vào chỉ số sensor tower anh em có tin không? Mình nhìn vào hồi xưa, có vẻ — chắc là hơi khói free thì không đúng, nhưng khói free thì chắc đúng. Cuối cùng mình xoay vào chỉ số bằng chính con game của mình mình cũng thấy không đúng."*

---

## Ngắn Hạn vs Dài Hạn — Quyết Định Đầu Hơn Cả Thiết Kế

Tổng kết các đoạn rải rác trong buổi:

| Trục | Ngắn Hạn (Chase Trend) | Dài Hạn |
|------|------------------------|---------|
| Timeline build | 1-2 tuần | 3-6 tháng |
| Pool thị trường | Nhỏ → CPI cao tạm thời | Lớn → CPI giảm |
| Test cycle | Chốt số sớm (D1-D3) | Ngoại suy D7 → D60 |
| Cơ chế | 1 cơ chế chính, ít hệ thống phụ | Mix nhiều cơ chế, phải tự coherent |
| Monetization model | IAA chủ lực | IAA + IAP, dần migrate sang IAP |
| Rủi ro | Hết trend = chết | Pool tắt = chết chậm hơn |

Quote Hiệp:
> *"Chúng ta đừng giải quyết bài toán 'tôi làm xong tôi đánh mất trend'. Tại sao chúng ta không nghĩ ra cách khác? Bằng cái việc đi giải quyết một bài toán vốn dĩ là không nên đề cập."*

---

## IAA → IAP Migration — Vì Sao Ai Cũng Muốn Chuyển

Vũ + Hiệp phân tích cấu trúc nguồn thu game mobile:

```
Game Revenue ─┬─ IAA (in-app ads)
              │   ├─ eCPM (impression rate × cost)
              │   └─ Cross-promo
              └─ IAP (in-app purchase)
```

### Tại Sao IAA Khó Lúc Này

- Khi market hyper casual yếu đi → các studio hyper không còn mua user nữa → eCPM dòng hyper tụt → *"anh có làm tốt tất cả đi sáng nữa cũng chẳng ai mua của anh"*.
- Top trend thị trường giờ là **puzzle** — chính dòng puzzle đang mua chéo user của nhau bằng giá cao hơn → eCPM puzzle ổn.
- Nhiều studio muốn migrate sang puzzle để hứng eCPM của hệ này.

### IAP Là Đường Riêng

IAP không phụ thuộc cross-network. Nhưng IAP khó *"bị đậm quá"* — *"IAA thì dễ, nhưng khi chúng ta chuyển sang IAP thì không dễ thì cũng dễ — hy vọng các bộ này cũng sẽ giúp mọi người làm cái gì đó."*

Hiệp tiet lộ Doc 5-6 sẽ có *"chuyển mô hình từ một con IAA sang một con hybrid, mà chuyển từ một con hybrid sang một con IAA thuần."*

### Đạt's Migration Question

Đạt hỏi: ECPM thấp nhưng product quality OK → migrate sang IAP được không? Hiệp confirm: được, nhưng *"phải tách bạch — không bị ảnh hưởng [bởi eCPM thị trường]"*. Đây chính là lý do mọi người muốn IAP ngay cả khi đã có sản phẩm IAA chạy được.

---

## eCPM — Biến Hộp Đen Designer Không Kiểm Soát Được

Đoạn này Vũ chia sẻ cay đắng về limit của bài tính LTV > CPI:

**Case**: Vũ + Giang từng có **2 con game giống hệt nhau** mọi mặt (cơ chế, art, balance, retention) — nhưng eCPM một con gấp 3 lần con kia. *"Tất cả những thứ về tiệm khách hàng — là năng chen, là ad-network, là buy-back, organic, v.v. — nó cũng 1% mà mẹ nó sinh ra. Cũng có 2 con giống hệt nhau mà chỉ số nó không đúng nhau."*

### eCPM Phụ Thuộc Cái Gì

Hiệp đưa breakdown:

- **Tương tác của user trong app** (CTR — click-through rate vào ad).
- **Người dùng đầu vào** — ai cài đặt app: tuổi, giới tính, sức mua, khu vực. *"Tệp khách hàng này UA Quick có thể đổ về CPI cao hay thấp, chọc vào người già hay người trẻ — UA Quick CVL này chỉ biết được cái này."*
- **Mức độ đồ họa** — game art tâm linh hơn hyper tay nhẹ thì eCPM trên user trẻ khác.
- **Style game** — đây là **biến quyết định cuối cùng**.
- **Performance trên Play Store** — *"hiện trạng bây giờ chính là cái app quality. Khi performance đủ tốt, bản thân Play sẽ trả vào những user chất lượng — và khi user chất lượng thì eCPM tất cả sẽ tốt."*

### Pattern Counter-Intuitive

Có sản phẩm chỉ số kiểu *"rất tuyệt vời nhưng ECMP không gì cả — chịu"*. Có sản phẩm chỉ số bình thường, *"có chuyện CPI cũng đấy, nhưng eCPM trên rời, thành ra vẫn win"*.

Vũ kết: *"Bí ẩn thật. Đúng không? Đó là giải thích được không? Đó không có câu trả lời."*

### Clone 100 Bản Có Được Không?

Đạt hỏi: nếu mô hình tốt, có thể clone 100 con cùng lúc để scale không. Vũ + Hiệp đồng quan điểm: **không được vì user cannibalism**:

> *"Phân bổ user thì có thể anh biết — chính là user anh đã chạy ở quán tốt rồi. Bây giờ anh chạy với cái tệp đấy, có thể anh sẽ đi rớt lại chính như user đấy — mà cái giá trị đấy là giá trị thấp hơn. Và 2 con đấy của anh đang cạnh tranh, chứng kiến với nhau."*

Hiệp note ngoại lệ: bên app (không phải game) — *"có những sản phẩm 100 con nhưng có khi chỉ 10 con ngon cười và 5 con ngồi khóc"* — vẫn có spread, không phải đều.

---

## Vai Trò 2 Studio — Mô Hình GAC

Gần cuối buổi, Vũ chia sẻ bài học cấu trúc team từ thời ở GAC:

- **Studio 1 (Winter Wolf model)** — đi theo trend, copy game thành công, follow chỉ số. Người làm follow theo workflow, không phải người tự ra phương án.
- **Studio 2 (Original model)** — tự nghĩ ra sản phẩm. *"Anh em trong nhà thì không chọc bát cơm của nhau. Tóm lại bên Winter Wolf làm theo hướng như anh em đang làm."*

Vấn đề Studio 1 (follow):
> *"Khi mà người ta cần improve sản phẩm thì người ta lại không phát động từ đâu. Tại sao khi người ta làm cái hai này level 10 đi đến, em muốn cải thiện để improve lên — muốn cải thiện từ chỗ nào? Vì họ không phải là người gây ra phương án từ bắt đầu, họ follow theo và không kịp hiểu."*

Vấn đề Studio 2 (original): *"Phép thử cực nhiều, tỷ lệ sai cực cao. Nhưng khi làm được một cái thì đó là cái họ control ngay từ đầu."*

Bài học: hai mô hình đều có giới hạn riêng. Khóa học sẽ chỉ ra cách improve sản phẩm có sẵn **và** cách mix tạo ra cái mới. Không bắt phải chọn duy nhất một bên.

---

## Kết Luận Của Hiệp — Tất Cả Quy Về Con Số

Buổi đóng bằng monologue của Hiệp:

> *"Em rút lại một điều, em sẽ chỉ muốn mọi người hãy nhìn vào tất cả bằng những con số. Nó sẽ trả lời chúng ta là chúng ta đang làm tốt, chúng ta đang phải sửa ở đâu. Số đến cuối cùng số nó sẽ trả lời chúng ta."*

Hiệp khoe case: gần đây test 1 con theo mô hình ông đã share — *"1 lần 1 tuần, được khoảng 50% retention. 20k user/ngày — con số này em nghĩ là đúng. Đó là khi áp dụng được đúng mô hình và biết sửa ở đâu."*

Tiêu chí cuối cùng cho mọi quyết định GD:
- Bắt chước được — OK, miễn là **bằng chỉ số sản phẩm gốc**.
- Original — OK, miễn là **kiểm soát được biến nào tạo ra số**.

Phản đối anti-pattern: *"Một cái gì nó nói hay kiểu lý thuyết như thế nào, nó không lúc chả biết tối ưu ở đâu, nó fail tại một dự án dứa chừng."* GD không định nghĩa được biến nào ảnh hưởng số nào → vô dụng.

---

## Câu Hỏi Còn Nợ (Tham Chiếu Buổi Khác)

- **Đặc tính tài sản (asset characteristics)** — Doc 2 reference rõ ràng vào "Doc 1 đã nói về tài sản" với 6 đặc tính (số lượng, chất lượng/phân cấp, khan hiếm, achievement, khoe tài sản, giá trị tăng theo thời gian). Phần này KHÔNG xuất hiện trong transcript audio Doc 1 đã ingest. Có thể nằm trong slide / segment mà whisper không capture, hoặc Hiệp đã bonus thêm offline. Xem [[negaxy-iec-gd-doc-02-level-design]] § Tiếp Nối Doc 1.
- **Chuyển mô hình IAA → Hybrid → IAP sâu** → Doc 5-6 (Vũ note).
- **Phân tích style art / aesthetic direction** → Doc 7 (Vũ + Hiệp đồng nói).
- **Level data deep-dive + difficulty curve hiện đại** → Doc 4 / 6 (đã có ở [[negaxy-iec-gd-doc-04-level-data-and-iap]]).

---

## Thuật Ngữ Buổi Này

- **GD** — Game Designer / Game Design.
- **Define** — viết rõ thông số input/output cho mỗi function trước khi code build (kích thước, ma sát, công thức gia tốc, drop rate, v.v.). Đối lập với "designer cảm tính".
- **Dataflow Diagram** — sơ đồ chạy dữ liệu giữa các function/system, GD viết để code đọc trực tiếp.
- **5 Levels of Idea** — thang đo độ chín của ý tưởng khi thuyết phục sếp: 0 (mô tả như user), 1 (mô tả gameplay), 2 (bóc tách element), 3 (cách triển khai), 4 (logic monetization), 5 (original, đặc sắc).
- **Rainbow Design** — chặn user bằng nhiều hướng khác nhau (entrance, hệ quân, data ẩn), không chỉ tăng chỉ số tuyến tính.
- **Biến Hiển Thị vs Biến Ẩn** — trong Match-3, hiển thị (blocker, goal) user thấy ngay; ẩn (chip drop rate, RNG digital) user không kiểm soát được, dùng để bán booster có logic.
- **CPI** — Cost Per Install.
- **LTV** — Lifetime Value. Điều kiện bán dự án: LTV > CPI.
- **eCPM** — Effective Cost Per Mille (impression rate × cost). Biến hộp đen, GD không kiểm soát trực tiếp.
- **CTR** — Click-Through Rate, tương tác user với ad.
- **A-B-B** — metric ưu tiên số 1 của Hiệp (vẫn để mở từ Doc 4).
- **Investment** — số ad / time chơi (inter + reward count).
- **Pool Thị Trường** — số user tiềm năng của dòng game. Pool lớn → CPI giảm.
- **Chase Trend / Bắt Chen** — làm sản phẩm ngắn 1-2 tuần để hứng UA giá rẻ thời điểm cụ thể.
- **Ngoại Suy** — extrapolate metric từ D7 → D60 dựa trên kinh nghiệm tối ưu.
- **IAA / IAP / Hybrid** — In-App Ads / In-App Purchase / mix.
- **Cross-Promo (cross network)** — quảng cáo cho game khác từ ad-network.
- **App Quality (Play Store)** — performance metric trả về user chất lượng.
- **User Cannibalism** — 2 sản phẩm giống nhau của cùng studio ăn lại tệp user của nhau.
- **Winter Wolf model vs Original model** — 2 studio cùng nhà GAC, một follow trend, một tự ra ý tưởng. Vũ dùng làm framework so sánh trade-off.
- **Daily Login 7/28-30** — 3 mô hình daily login: 7-day loop, 28-day no-loop bỏ qua, 28-day no-loop tiếp tục.
- **File Define Sơ Bộ** — văn bản GD viết các "yếu tố ảnh hưởng liên quan" trước khi đi vào số cụ thể (gọi không xương). Bộ xương để code/art đắp tiếp.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Transcript thô: `GD Doc 1.mp3.txt` (~4,921 dòng whisper transcript)
- Audio gốc: `GD Doc 1.mp3`
- Vị trí trong khóa: **Buổi 1** (foundation / mindset), trước Doc 2 (Level Design).
- Khóa học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
- Note: Phần "tài sản (assets)" mà Doc 2 reference lại không xuất hiện trong audio Doc 1 — có khả năng là segment slide ngoài transcript, hoặc Hiệp/Vũ bonus offline. Reader cần Doc 2 § "Tiếp Nối Doc 1" để có khung 6 đặc tính tài sản.
