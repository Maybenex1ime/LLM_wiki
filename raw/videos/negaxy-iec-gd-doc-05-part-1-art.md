---
title: "GD Doc 5 Part 1 — Art: Định Nghĩa Art Style, Brief & Workflow Với Art Team (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 5 Part 1 - Art.MOV"
date_added: 2026-05-19
date_updated: 2026-05-19
tags: [video, course-transcript, game-design, art, art-style, art-brief, art-direction, asset-pipeline, vector-bitmap, level-detail, vietnamese]
aliases: ["GD Doc 5 Part 1", "Buổi 5 Phần 1 Art", "Art Style Brief Vũ"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-04-level-data-and-iap]]"
  - "[[negaxy-iec-gd-doc-06-part-1-ui]]"
  - "[[negaxy-iec-gd-doc-07-ui-ux-monetize]]"
summary: "Buổi 5 Part 1 (Vũ + Đức + Minh + học viên): cách GD viết art brief cho team art — phân loại art style (chibi 1/2, 1/3, 1/4), level detail, naming convention, vector vs bitmap + outline, size card 5×6 trên 1080×1920, define palette per đối tượng, contrast giữa địch và mình. Toy Odyssey case study về art quá nhiều layer làm tách hình bị dính. Workflow: chốt con đầu tiên rồi giữ form, đổi quần áo. Anti-pattern: paste reference rồi đẩy hết cho art."
---

# GD Doc 5 Part 1 — Art: Định Nghĩa Art Style, Brief & Workflow

**Speakers:**
- **Vũ** — Lecturer chính. Chia sẻ kinh nghiệm 2Cơ Game (Tam Quốc, Kiếm Hiệp, Mộng Võ Lâm), Ritga, IEC.
- **Đức** — Học viên có game thẻ bài, ý tưởng "tông tím đen huyền bí," 32 thẻ trên bàn đấu.
- **Minh** — Học viên từng làm con NFT (Toy Odyssey-related), từng làm việc với anh Nhất (art lead Ritga).
- **Giang** — Học viên (lurker session này).

**Format:** Buổi học trao đổi, ~45 phút, tiếng Việt. Tập trung vào câu hỏi "GD đưa cho team art cái gì?" — chuyển trọng tâm từ gameplay sang art pipeline.

Tiếp nối Doc 4 (Level Data) và đặt nền cho Doc 5 Part 2 (Animation), Doc 6 (UI/UX). Lần đầu trong khoá đi sâu vào art workflow.

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 5 Part 1 - Art.MOV` (1.8 GB) + `GD Doc 5 Part 1 - Art.MOV.txt` (1,396 dòng, faster-whisper large-v3 chunked).

---

## Anti-Pattern Mở Đầu — "Lấy Reference, Đẩy Hết Cho Art"

Vũ hỏi mở đầu: *"Bình thường khi đề xuất một cái art, mọi người mô tả art style như thế nào?"* Học viên trả lời ngắn: "Lấy reference, lúc luộc nguyên art style của nó."

Vũ chỉ ra vấn đề:

> *"Cách làm như thế là giao hết cho bên art rồi. Vậy thì trong những dự án mà các bạn buộc phải mô tả art style cho đội art — không theo cái cách bê nguyên con gốc vào — thì mình sẽ mô tả như thế nào?"*

Vấn đề khi nhận hàng:
- Không có **tiêu chí** để đánh giá đúng yêu cầu hay không.
- Khi team art không có leader cứng + nhiều member → mỗi người vẽ một kiểu → quay round không kết thúc.
- Trượt vào cãi vã "xấu vs đẹp" thay vì so sánh với spec.

---

## Mô Tả Đầu Vào — Case Game Thẻ Bài Của Đức

Vũ test bằng cách yêu cầu Đức mô tả game của mình. Output:

- **Tông màu chủ đạo**: tím đen, huyền bí.
- **Nhân vật chính**: Chibi 1/3 (đầu/thân), nam, châu Âu, quần áo rách, áo choàng, có cánh.
- **Bối cảnh**: tách tiền cảnh / hậu cảnh / object có thể tương tác.
- **Gameplay**: tương tác trên bot (puzzle-like), không phải trên map.
- **Bot màu**: nâu đỏ, vàng (cát).
- **Nhân vật phụ**:
  - Tuyến đồng hành: 2-3 con, màu xanh dương.
  - Tuyến phản diện: đỏ và đen.
- **Phân cấp** (theo style Hearthstone): màu trắng = cao nhất + effect riêng.

Vũ chỉnh: phân cấp không bắt buộc qua màu — có thể qua tên + effect. Nhưng vấn đề bán IAP: *"Làm sao để biết con đó xịn thế nào? Làm sao để nó nổi bật trong đội hình khi ra trận?"* → cần visual hierarchy rõ ràng.

---

## Vector vs Bitmap — Phải Outline

Khi Đức đề cập "hạn chế dùng Guardian (Bitmap)," Vũ đào sâu lý do.

### Behavior Của Art Khi Vẽ

> *"Em có biết là art của họ có behavior phóng to lên để họ vẽ, sau đó họ sẽ zoom nhỏ lại không? Đấy chính là lý do mà vì sao cái level design này thường sẽ bị sai. Có cái ảnh sẽ rất nhìn to rất đẹp — nhưng khi zoom nhỏ lại rất khó."*

Art zoom in/out → bitmap zoom nhỏ thì bị vỡ. **Vector** giữ chất lượng ở mọi size.

### Outline 2-3 Pixel

> *"Em nên sử dụng vector và đẩy outline vào. Thì khi zoom nhỏ ảnh của em sẽ không bị vỡ. Outline em chỉ cần chỉnh lại theo đường bo của con đấy — ví dụ outline 3 pixel hay 2 pixel."*

Vũ confirm 2Cơ Game và IEC đều dùng **vector** cho card-based games (Tam Quốc, Kiếm Hiệp, Mộng Võ Lâm). Card hiển thị 3D trong battle, nhưng collection panel là 2D vector.

---

## Size Card Cho Bàn Đấu — 32 Thẻ Trên 1080×1920

Vũ truy vấn Đức về size: với 32 thẻ cùng màn hình, mỗi thẻ bao nhiêu pixel?

### Math

- Phone resolution: 1080 × 1920.
- 32 thẻ ≈ 5 × 6 + dư mép.
- Card size ≈ **120-180 pixel** (có thể lên 150-200 nếu chấp nhận lệch).

Vũ chốt: thẻ nhỏ như vậy + vẽ vector + outline 2-3 pixel → user nhìn rõ ngay cả khi 32 ô cùng màn.

### UX Cue: Mép Mép Phía Dưới

> *"Phân bổ UI cũng đừng phân bổ kiểu 3 × 5 = 30. Mà nên phân bổ 30 × 5 — ở đây nó có một tí tí mép mép dưới để mọi người có behavior vuốt. Thì user nó biết là có thể vuốt được, mà không cần chèn ninh, không cần dạy dỗ gì cả."*

Visual cue: phần "mép mép" thừa ở mép màn hình → user reflex vuốt dạp. Bài học UX: hide affordance trong layout, không phải qua text/tutorial.

---

## 3 Thành Phần Của Art Brief — Style, Level Detail, Color

Vũ chốt khung GD đưa cho team art:

### 1. Art Style — Cách Thức Vẽ

- **Tên + đặc điểm style**: chibi 1/3, chibi 1/2, chibi 1/4 (đầu/thân ratio).
- **Đặc điểm riêng**: chibi chân to, chibi chân teo. Phân biệt subtype để art không vẽ tự do.
- **Khớp (joints)**: bao nhiêu khớp, dùng để animation. Hạn chế Guardian nếu zoom nhỏ.
- **Chi tiết bổ sung**: tỷ lệ mắt, mũi, miệng trong khuôn mặt (%).

### 2. Level Detail — Mật Độ Chi Tiết

- **Định nghĩa**: bao nhiêu đường thẳng / hoa văn trong một diện tích nhất định.
- **Số lượng nhân vật / màn hình**: scale density.

Vũ minh hoạ anti-pattern: 

> *"Mặt từ đầu chibi rõ rồi, tròn xoe tròn ủng. Xong ở dưới bắt đầu là cổ áo, nó cứ dồng phượng hết cả lên — chấm chấm chấm chấm tí tí. Liệu nó có ra art style của bạn hay không? Hay là bạn phải define xem trên một cái hình ảnh như thế, mật độ chi tiết của bạn có bao nhiêu?"*

Không define mật độ → art tự "chấm chấm tí tí" → mật độ phá art style.

### 3. Màu Sắc & Tone

- **Cảm xúc mong muốn**: vui tươi → màu gì, huyền bí → màu gì.
- **Tông chính**: ví dụ tím đen.
- **Phân cấp màu** (nếu có): primary, secondary, accent.
- **Mức độ tương phản (contrast)** giữa các bên: quân địch vs quân mình.
- **Palette per đối tượng**:
  - Quân mình: xanh dương → xanh lá gradient.
  - Quân địch: cam → đỏ gradient.
  - Background: nâu → xám gradient.

---

## Naming Convention Cho File List

Đức mô tả naming: `men_strength_1`, `men_strength_2`. Vũ propose cải tiến:

- **Đổi tiền tố trước**: `m_strength_1` thay vì `men_strength_1`.
- Lý do: khi sort file, người ta nhìn thấy ngay phần nào là phần anh nào (m_ = men, w_ = women, e_ = enemy).
- **Auto-merge tools**: nếu mọi nhân vật theo cùng form (cùng pose set: attack, idle, dead, skin1), có thể script auto-ghép body parts với head parts → giảm 1 con từ work manual.

Điều kiện auto-merge:
- Tất cả nhân vật đi theo cùng pose body set.
- Body parts ghép được với nhau (cùng skeleton).
- Có hoặc không có body pass — cả 2 đều ghép được.

---

## Case Toy Odyssey — Anh Hiệu Và Bài Học Quá Nhiều Layer

Vũ kể câu chuyện dự án Toy Odyssey:

### Vấn Đề

Anh Hiệu là art cứng, style "cực kỳ đẹp." Trên 1 cái chân nhỏ (≈ ½ cây bút), anh chuyển **6-7 lớp màu** từ xám sang đen.

> *"Anh ấy chuyển được 6-7 lớp. Vấn đề là anh ấy chuyển được 6-7 lớp nhưng mà trên cái chân con nhân vật nó bé. Anh ấy làm rất là lâu, và các con nhân vật khác đều bị kiểu như thế."*

Hậu quả:
- Vẽ rất lâu.
- Khi 2 nhân vật va vào nhau → màu chuyển từ con A sang con B bị "nhờ nhờ," không có **độ tách biệt**.
- Lớp của con này dính vào lớp của con kia → user không phân biệt được địch vs mình.

### Game Design Thô Hơn Nhưng Hiệu Quả Hơn

> *"Nếu như theo kiểu game design gọi là thô nhất nhá — cái quần màu xanh, cái bóng nó màu đen. Có đoạn layer chuyển nhờ nhờ giữa là màu xanh đen. Thế là xong — vẽ 3 layer. Mà cái nào lâu hơn?"*

3 layer (xanh, xanh đen, đen) thay vì 7-8 layer:
- Nhanh hơn rất nhiều.
- Tách hình rõ ràng — nhân vật ra khỏi background, nhân vật vs nhân vật.
- User chơi nhận biết được object.

### Bài Học Cho GD

> *"Tới sau khi mình làm mình thấy kết quả: 'Anh ơi tại sao game này của mình nó cứ tối tối user chơi nó cứ khó nhìn rồi nó không phân biệt được con nào là địch con nào là bên mình. Em chơi rất hay bị chết.' Đầu tiên nghĩ là khó. Sửa level design rồi nó vẫn cứ không được. Mới phát hiện ra là cái style art này nó làm cho con game nó trở nên là một là tối, hai là dính hình."*

GD không can thiệp sớm → art "đẹp lẻ" nhưng không serve gameplay → fix tốn thời gian gấp nhiều lần.

---

## Workflow Chốt Form — Con Đầu Tiên Là Template

Vũ propose process khi không có art director:

### Bước 1: Vẽ Con Đầu Theo Form

- Vẽ con base: tỷ lệ đầu, kích thước mắt, kích thước chân tay.
- Iterate cho đến khi GD chấp nhận: "Tôi thấy cũng được."
- **Chốt con đầu tiên là 10 điểm**.

### Bước 2: Cứ Theo Form Vẽ Tiếp

> *"Từ giờ anh em làm cách này nhá: cứ theo form này mà phải. Mắt giữ nguyên size, chân tay giữ nguyên size. Tóc, quần, đắp áo vào thôi. Đừng vẽ lại nữa."*

3 form base: trung bình / béo / gầy.
- Mỗi form vẽ kỹ chỉ 1 con.
- Các con sau: thay đầu, tóc, quần áo, mặt → giữ chân tay tỷ lệ.

### Bước 3: Lưu Ý Edge Cases

- Tóc cao nhất đến đâu (định nghĩa max height).
- Mũ cao nhất đến đâu.
- Bụng to → vẽ con bụng to ra trước, **đừng ép artist tưởng tượng**.
- Cao và lùn → nếu khác form, vẽ riêng từ đầu.

### Lý Do

> *"Đấy là một cách để cho các bạn bớt phải gãy nhau. Và các bạn art khác — khi 1 người đã vẽ rồi — thì những người khác còn lại cũng có thể xuất công nghiệp. Cứ thế vẽ đè lên."*

Giảm dependency lên 1 artist cứng. Production line-able khi cần scale team.

---

## Process Ritga — 7-9 Bước Per Nhân Vật

Minh chia sẻ kinh nghiệm Ritga: anh Nhất (art lead) áp **process 7-9 bước** cho 1 bức ảnh nhân vật.

- Mỗi bước là 1 stage hoàn thiện (sketch → line → flat color → shading → details → review).
- Duyệt xong stage → mới chuyển sang stage tiếp.
- Bước nào sai → refactor stage đó, không phá toàn bộ.

Vũ comment: process Ritga rất "trùng cầy" cho team nhỏ, nhưng phù hợp với studio mid-size làm sản phẩm dài hạn. Studio nhỏ + prototype → process này có thể bị skip.

### Khi Studio Nhỏ Không Có Art Director

> *"Việc đòi tuyển art director là một câu chuyện mà mình nghĩ các bạn sẽ không giải quyết được. Volume của công ty + quy mô dự án không đủ để cho 1 director có đất dụng võ."*

Hệ quả: GD phải gánh vai trò half-art-director — biết style, biết detail, biết color, biết workflow. Đây là lý do Vũ dạy chủ đề này: *"Các bạn ở công ty nhỏ buộc sẽ phải chấp nhận có những vị trí phải làm nhiều việc."*

---

## GD Phải Định Nghĩa Đầu Vào — Không Chỉ Đầu Ra

Vũ phản biện học viên đề xuất "ta cứ làm, art vẽ ra, mình nói đẹp/xấu":

> *"Em là người đưa ra yêu cầu. Bây giờ người ta làm không đúng yêu cầu của em — em bảo phân tích, em bổ ra cái thứ nào không đúng. Thế thì sao em không bổ luôn từ đầu đi để lấy cái mà nói họ?"*

Analogy: nếu sếp bảo "ngày nào em cũng đi muộn" thì em hỏi "quy định nào trong giờ là đi muộn?" Phải có **spec rõ ràng** trước → mới có cơ sở chỉnh art.

### "Không Phải Người Yêu Dở Thuần"

> *"Bây giờ mình là một yêu dơ. Nếu mình nhìn thấy một cái gì đấy khó chịu, mình sẽ làm thế nào? Vậy chúng ta có phải là yêu dơ thuần đâu — ta là trong đồng hữu sản xuất. Bây giờ buộc phải bóc tách vấn đề để giải quyết cái sự tốt nhất."*

GD không thể chỉ "cảm thấy không đúng" — phải bóc tách thành spec cụ thể (style mismatch? level detail quá? màu lệch palette?).

### "Cái Lẩu Mắm" — Gu Cá Nhân vs Gu Thị Trường

> *"Anh em có thể thích ăn lẩu mắm tanh tanh khắm khắm. Nhưng anh em khác quen kiểu pizza đồ Tây rồi — cho đi vào hàng lẩu mắm thì khéo bịt mũi chạy từ đầu ngõ. Câu chuyện ở đây là ta đang mài sản phẩm trở thành sản phẩm mang thị hiếu chung cho nhiều người."*

GD không "vẽ game cho mình thích" — vẽ game cho **thị trường thích**. Pizza > lẩu mắm khi serve toàn cầu.

---

## GD Học Vẽ Layout — Vuông Tròn Tam Giác

Đặc biệt với studio nhỏ, GD phải vẽ được layout (không cần đẹp):

> *"Bên anh, các bạn GD sẽ còn được yêu cầu là 'Ông vẽ. Tôi không yêu cầu ông vẽ layout UI trông ra như thế nào — nhưng ít nhất ông phải layout được phần gameplay trông mặt mũi ra làm sao. Ông vẽ tay được thì họ vẽ. Vào video, dùng vuông tròn tam giác, bố tả xếp như thế nào — tùy quyền ông.'"*

Yêu cầu:
- **Layout gameplay** (không phải UI hoàn chỉnh).
- Camera góc nhìn — vẽ tay hoặc dùng shapes.
- Đủ cho artist hình dung **bố cục, kích thước tương đối, depth**.

3D case: nhân vật + camera nghiêng → nhân vật cúi mặt → artist phải biết để điều chỉnh cam/pose. GD cần draft sớm để art không vẽ off.

---

## Anti-Pattern Tổng Hợp

Vũ tổng kết:

- **Paste reference rồi đẩy hết cho art** — không có spec để đánh giá.
- **Không define art style từ đầu** — cãi xấu/đẹp thay vì so spec.
- **Không có level detail definition** — art tự "chấm chấm tí tí" phá style.
- **Không define palette per đối tượng** — địch và mình dính nhau visual.
- **Art quá nhiều layer trên đối tượng nhỏ** — chậm + dính hình (Toy Odyssey case).
- **GD "yêu dở thuần"** — chỉ "cảm thấy khó chịu" không bóc tách spec.
- **Vẽ game theo gu cá nhân** — lẩu mắm thay vì pizza, không serve thị trường.
- **Không học vẽ layout** — không communicate được bố cục cho artist.
- **Đòi tuyển art director ở studio nhỏ** — không đủ work cho 1 director full-time, mâu thuẫn quy mô.

---

## Thuật Ngữ Buổi Này

### Art Style
- **Art Style** — định nghĩa cách thức vẽ + màu cho sản phẩm. Bao gồm form, level detail, palette.
- **Chibi 1/3** — tỷ lệ đầu/thân = 1/3 (đầu chiếm 1/3 chiều cao). Cũng có 1/2, 1/4 etc.
- **Level Detail** — mật độ chi tiết hình ảnh (đường thẳng, hoa văn) trong một diện tích nhất định.
- **Khớp** — joints cho animation. Số khớp ảnh hưởng tới animation pipeline.

### Pipeline
- **Vector** — định dạng đồ hoạ scale được không vỡ. Pháp tuyến cho card-based games (Tam Quốc, Kiếm Hiệp style).
- **Bitmap / Guardian** — định dạng pixel-based. Zoom nhỏ bị vỡ.
- **Outline 2-3 pixel** — viền theo đường bo của object, giúp tách object khỏi background khi zoom nhỏ.
- **Auto-Merge** — script ghép body parts với head/clothing parts. Yêu cầu cùng pose set.
- **Process N Bước** — workflow art chia thành stages (sketch → line → flat → shading → details). Pattern Ritga: 7-9 bước.

### Color & Tone
- **Tông Chính** — màu chủ đạo (ví dụ tím đen).
- **Palette Per Đối Tượng** — màu riêng cho từng nhóm (địch cam-đỏ, mình xanh, BG nâu-xám).
- **Phân Cấp Màu** — primary/secondary/accent hierarchy.
- **Contrast** — độ tương phản giữa các nhóm. Thiếu contrast → user không phân biệt được object.

### Workflow
- **Form Base** — con đầu tiên đã chốt, các con sau giữ tỷ lệ chân tay, chỉ thay quần áo/đầu.
- **Art Director** — vị trí lead art. Studio nhỏ thường không đủ work cho full-time director → GD gánh half-vai.
- **Production Line** — nhiều artist cùng vẽ theo template chốt, giảm dependency 1 artist cứng.

### UX
- **Mép Mép Affordance** — visual cue trong layout (rìa thừa phía dưới) để user reflex vuốt mà không cần tutorial. Pattern: 5 × 6 + mép thay vì 6 × 5 trọn.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Video gốc: `GD Doc 5 Part 1 - Art.MOV` (1.8 GB, ~45 phút).
- Transcript đầy đủ: `GD Doc 5 Part 1 - Art.MOV.txt` (1,396 dòng, faster-whisper large-v3 chunked qua `doc5_art_chunks/`).
- Khoá học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
- Vị trí trong khoá: **Buổi 5 Phần 1 — Art** (nằm sau Doc 4 Level Data + IAP; đặt nền cho Doc 5 Part 2 Animation và Doc 6 UI/UX).
- Date updated 2026-05-19: compile lần đầu từ transcription có sẵn.
