---
title: "Art Brief 3 Parts — Art Style, Level Detail, Color"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-1-art]]"
date_added: 2026-05-20
tags: [concept, art, art-brief, gd-craft, asset-pipeline, chibi]
aliases: [art brief, 3 thành phần art brief, art style level detail color, define art spec]
status: draft
related:
  - "[[form-base-art-template]]"
  - "[[vector-vs-bitmap-game-art]]"
  - "[[file-y-do-design-intent]]"
summary: "Khung 3 thành phần GD đưa cho team art: (1) Art Style — cách thức vẽ (chibi 1/3, joint count, eye/mouth ratio), (2) Level Detail — mật độ chi tiết (đường thẳng/hoa văn trong diện tích), (3) Color — tông + palette per đối tượng + contrast. Skip = team art vẽ tự do, GD chỉnh hoài không xong."
---

## Định Nghĩa

Art Brief 3 Parts = framework Vũ chốt khi GD đưa requirements cho team art. 3 thành phần bắt buộc đầy đủ trước khi team art bắt đầu work.

Lý do: skip → team art vẽ tự do theo gu cá nhân → cãi vã "xấu vs đẹp" không có spec để so → quay round không kết thúc.

> *"Cách làm như thế là giao hết cho bên art rồi. Vậy thì trong những dự án mà các bạn buộc phải mô tả art style cho đội art — không theo cái cách bê nguyên con gốc vào — thì mình sẽ mô tả như thế nào?"*

## Part 1 — Art Style (Cách Thức Vẽ)

Define **HOW** to draw.

### Form (Tỷ Lệ)

- **Chibi 1/2, 1/3, 1/4** — đầu/thân ratio.
- **Chibi chân to vs chibi chân teo** — subtype phân biệt.
- **Realistic 1/7** — adult proportions.

> *"Tên + đặc điểm style: chibi 1/3, chibi 1/2, chibi 1/4 (đầu/thân ratio). Đặc điểm riêng: chibi chân to, chibi chân teo. Phân biệt subtype để art không vẽ tự do."*

### Joint Count

- Bao nhiêu joint cho animation.
- Limit nếu zoom nhỏ (vector outline thay vì bitmap multi-layer).
- Standard: 16 joints cho 2D rig (head, torso, 2 arms × 2 segments, 2 hands, hips, 2 legs × 2 segments).

### Facial Proportions

- Tỷ lệ mắt / mũi / miệng trong khuôn mặt (%).
- E.g., mắt 35% width, miệng 20% width.
- Đảm bảo expression consistency across characters.

## Part 2 — Level Detail (Mật Độ Chi Tiết)

Define **HOW MUCH** detail.

### Density Metric

> *"Mật độ chi tiết: bao nhiêu đường thẳng / hoa văn trong một diện tích nhất định."*

- Đếm số visible line per square inch.
- Đếm số distinct color region.
- Đếm number of pattern element.

### Anti-Pattern Example

> *"Mặt từ đầu chibi rõ rồi, tròn xoe tròn ủng. Xong ở dưới bắt đầu là cổ áo, nó cứ dồng phượng hết cả lên — chấm chấm chấm chấm tí tí. Liệu nó có ra art style của bạn hay không? Hay là bạn phải define xem trên một cái hình ảnh như thế, mật độ chi tiết của bạn có bao nhiêu?"*

Mật độ không define → art tự "chấm chấm tí tí" → mật độ phá art style.

### Character Density vs Screen Density

- Số nhân vật / màn hình ảnh hưởng level detail.
- 5 nhân vật trên màn → mỗi nhân vật có thể detailed.
- 30 nhân vật trên màn → giảm detail per nhân vật để render efficient.

## Part 3 — Color & Tone

Define **WHAT COLORS**.

### Emotion Mapping

- **Vui tươi** → bright primary colors (đỏ, vàng, xanh).
- **Huyền bí** → tone trầm + neon accent (tím đen, đen rượu vang).
- **Thư giãn** → pastel.
- **Hành động** → bold high-contrast.

### Tông Chính

Define 1-2 màu chủ đạo:
- Game của Đức: tím đen, huyền bí.
- Game farm: xanh lá pastel.
- Game cyberpunk: tím + neon hồng.

### Palette Per Đối Tượng

> *"Palette per đối tượng: Quân mình: xanh dương → xanh lá gradient. Quân địch: cam → đỏ gradient. Background: nâu → xám gradient."*

Mỗi nhóm có palette riêng → user phân biệt visual ngay.

### Contrast

- **Quân địch vs quân mình** — high contrast (warm vs cool color).
- **Object interactive vs background** — saturation + brightness contrast.
- **HUD vs gameplay** — strong outline / shadow.

Thiếu contrast → user không phân biệt được trong combat → drop rate.

## Case Study Đức (Game Thẻ Bài)

Vũ test bằng Đức mô tả game của mình:

| Aspect | Đức's Input | Vũ's Improvement |
|--------|-------------|------------------|
| Tông màu | Tím đen, huyền bí | OK |
| Form nhân vật chính | Chibi 1/3, nam, châu Âu | OK + add "quần áo rách, áo choàng, có cánh" |
| Bối cảnh | Tách tiền cảnh / hậu cảnh / object | OK |
| Gameplay arena | Trên bot, không phải map | OK |
| Bot màu | Nâu đỏ, vàng (cát) | OK |
| Phân cấp | Theo style Hearthstone: trắng = cao nhất + effect | Add: hierarchy không bắt buộc qua màu, có thể qua effect + name |

Sau khi Đức mô tả → Vũ chỉ thêm gaps:
- Visual hierarchy đảm bảo IAP feel rõ ràng.
- Effect khác biệt cho rarity (nếu skip color).

## Process Flow

1. **GD draft brief** — fill 3 parts với details cụ thể.
2. **Review với team art** — confirm understanding + capacity.
3. **Art produces 1 sample** — first character / first asset.
4. **GD review sample** — match brief? if yes → continue, if no → refine brief.
5. **Production line up** — apply brief cho các asset còn lại.

Xem [[form-base-art-template]] cho production line technique.

## Anti-Pattern: "Paste Reference Đẩy Hết Cho Art"

> *"Học viên trả lời ngắn: 'Lấy reference, lúc luộc nguyên art style của nó.' Vũ chỉ ra vấn đề..."*

Skip brief → paste game reference → đẩy hết cho art:
- Không có tiêu chí để đánh giá đúng yêu cầu hay không.
- Team art không leader cứng + nhiều member → mỗi người vẽ một kiểu → quay round không kết thúc.
- Trượt vào cãi vã "xấu vs đẹp" thay vì so với spec.

Brief = **measurable spec**. So sánh art output với spec, không so với gu.

## Liên Hệ Wiki

[[form-base-art-template]] cho production line — sau khi brief có 3 parts, dùng form base để scale team. [[vector-vs-bitmap-game-art]] cho cụ thể về Part 1 (vector vs bitmap choice). [[file-y-do-design-intent]] cho design intent file — context cho art brief.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-1-art.md` § "3 Thành Phần Của Art Brief — Style, Level Detail, Color", "Anti-Pattern Mở Đầu"
