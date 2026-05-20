---
title: "UI Wireframe Workflow — 3 Bước Cho VN Studio"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ui, workflow, wireframe, gd-craft]
aliases: [wireframe 3 bước, UI workflow VN, Core vs Flow approach, draft case]
status: draft
related:
  - "[[ui-button-3-levels]]"
  - "[[ui-button-3-spawn-types]]"
  - "[[equip-flow-hero-vs-weapon]]"
  - "[[file-y-do-design-intent]]"
summary: "Vũ chốt simplified UI workflow cho VN studio: (1) chọn approach Core vs Flow, (2) vẽ draft vuông tròn tam giác + đắp case, (3) làm UI thật với levels of priority. Khác với workflow agency quốc tế (Minh share) — adapt cho volume VN."
---

## Định Nghĩa

UI Wireframe Workflow của Vũ = quy trình 3 bước cho GD tại VN studio làm UI từ scratch. Đối lập với workflow chi tiết kiểu agency quốc tế (Minh share — flowchart toàn bộ, mood board, color palette).

> *"Việt Nam thường không cần phức tạp đến mức đó. Vũ sẽ adapt sao cho phù hợp VN volume."*

## Bước 1 — Xác Định Cách Làm

2 approach để xuất phát:

### Đi Từ Core Đi Ra

Flow: **tính năng → button → case**.

- Start: list các tính năng (weapon, inventory, shop, settings).
- Mid: define button cho mỗi tính năng.
- End: list case (popup, state, flow) cho mỗi button.

Lợi:
- Flow nhiều tầng cho phép sâu (case lồng nhau).
- Dễ mở rộng tính năng mới sau.

Phù hợp: game có nhiều system (RPG, strategy, MMO).

### Đi Từ Flow Đi Vào

Flow: **user flow → màn → button**.

- Start: vẽ user journey end-to-end (start app → home → battle → reward).
- Mid: định nghĩa màn cho mỗi step.
- End: bố trí button per màn.

Lợi:
- Đơn giản, follow story user.
- Phù hợp linear game flow.

Hạn chế:
- Khó xử lý case lồng nhau sâu.
- Tính năng mới không follow flow → khó add.

Phù hợp: hyper-casual, single-loop game.

## Bước 2 — Triển Khai (Draft + Case)

### Vẽ Draft Vuông Tròn Tam Giác

Không vẽ pixel art. Dùng wireframe shapes:
- **Vuông** = button / panel.
- **Tròn** = icon / avatar.
- **Tam giác** = action indicator (arrow, play).

Output: layout rough trên giấy / Figma / Miro.

### Đắp Case Vào Draft

Mỗi button trong draft phải có case attached:
- Bấm → popup nào?
- Bấm → state thay đổi gì?
- Bấm → flow phụ nào sinh ra?

Xem [[ui-button-3-spawn-types]] cho 3 loại case.

### Vòng Lại Hoàn Thiện

- Re-check draft với case mới phát hiện.
- Bổ sung button còn thiếu.
- Lặp đến khi draft cover tất cả use case.

> *"Vẽ draft đầu tiên (vuông tròn tam giác). Đắp case vào draft. Vòng lại để hoàn thiện draft + bổ sung case mới phát hiện. Lặp đến khi draft cho ra cái UI hợp lý."*

## Bước 3 — Làm UI Thật

Sau khi draft hoàn thiện:

### Phân Levels of Priority

| Level | Vị Trí |
|-------|--------|
| **Key (Must)** | Thumb zone (xem [[thumb-zone-design]]) |
| **Blue (Optional)** | Side panel, ít quan trọng |
| **Hidden** | Trong tab / setting menu |

Xem [[ui-button-3-levels]] cho 3 level button đầy đủ.

### Dàn Vị Trí Pixel

- Cố định 5 màu code (xem [[ui-5-color-brief]]) cho priority.
- Đảm bảo button quan trọng nằm trong thumb zone.
- Apply rule tối đa 2 tầng (xem [[ui-rule-max-2-levels]]).

## So Sánh Với Workflow Agency (Minh Share)

Workflow Manny Noel / Soft Cache (hybrid VN-quốc tế):

1. **Flowchart toàn bộ trường hợp** — màn inventory: có item / full / thiếu tiền / no internet → all branches.
2. **Sketch màn gameplay + home trước** — 2 màn quan trọng nhất.
3. **Mood board + color palette** — đồng bộ UI / VFX / gameplay.
4. **Wireframe vuông tròn tam giác** — yes/no decision tree before pixel polish.
5. **Detail từng màn** — break down từng feature.
6. **Estimate theo breakdown** — 2D, 3D, VFX, environment riêng.

Vũ comment: workflow Minh chuẩn freelance / agency quốc tế. VN studio thường không cần phức tạp.

| Yếu Tố | Agency (Minh) | VN Studio (Vũ) |
|---------|---------------|-----------------|
| Flowchart đầy đủ | ✅ All branches | ⚠️ Chỉ key branches |
| Mood board | ✅ Required | ❌ Không bắt buộc |
| Wireframe shapes | ✅ Vuông tròn tam giác | ✅ Vuông tròn tam giác |
| Estimate breakdown | ✅ Detailed | ⚠️ Rough |
| Iteration count | 3-5 rounds | 1-2 rounds |

VN volume requires faster iteration → simplified workflow.

## Workflow Cường (Web UI/UX Background)

Cường share flow của bạn (background web UI/UX):

1. Chọn **tỷ lệ màn hình** (18:9, preset iPhone 14 Pro Max trong XD/Figma).
2. Bật **lưới căn** (Photoshop grid).
3. Vẽ **bố cục chính** dọc:
   - HUD top: setting, currency.
   - Nút chính ở 1/3 dưới (thumb zone).
4. **Data setup**: Excel song song cho mỗi tính năng.

Vũ note: Cường flow phù hợp khi **làm theo con game gốc** (đã có template). Khi làm game mới, flow Vũ đề xuất phù hợp hơn (start từ Core/Flow approach).

## Anti-Pattern

- **Skip Bước 1** (xác định approach) → vẽ draft không có ngữ cảnh → phải redo.
- **Polish pixel quá sớm** (skip draft) → khó iterate, mất time.
- **Không đắp case vào draft** → discover case sau khi polish → fix tốn kém.
- **Skip Bước 3 priority** → button quan trọng nằm ngoài thumb zone, button không quan trọng chiếm spotlight.

## Liên Hệ Wiki

[[ui-button-3-levels]] cho 3 level button. [[ui-button-3-spawn-types]] cho 3 loại case. [[equip-flow-hero-vs-weapon]] cho case study ứng dụng workflow. [[file-y-do-design-intent]] — design intent file bổ sung cho draft. [[ui-5-color-brief]] cho convention màu.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "3 Bước Làm UI Cho VN Studio", "Wireframe Workflow — Từ Cường", "Workflow Pro Của Minh"
