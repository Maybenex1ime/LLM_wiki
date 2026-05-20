---
title: "UI Button 3 Spawn Types — Popup / State / Luồng Lên Đới"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ui, button-states, flow, popup, gd-craft]
aliases: [3 nảy sinh khi bấm, popup state luồng lên đới, button trigger types, UI case]
status: draft
related:
  - "[[ui-wireframe-workflow]]"
  - "[[ui-rule-max-2-levels]]"
  - "[[equip-flow-hero-vs-weapon]]"
summary: "Mỗi nút khi bấm có thể trigger 1 trong 3 loại: (1) Popup — báo cứng không sinh flow phụ, (2) State — thay đổi state của button, (3) Luồng Lên Đới — sinh flow phụ. Designer phải list tất cả case trước khi vẽ UI để không discover later."
---

## Định Nghĩa

3 Spawn Types = framework Vũ chốt để list mọi case có thể xảy ra khi user tap button. Mỗi button trong wireframe phải xác định trigger trong 3 loại này.

> *"Tại sao mình tách popup này và popup này nó ra khác nhau? Cái luồng này là luồng cứng — mình không thể làm gì khác được. Còn thế này là nó có một luồng lên đới phụ xảy ra theo trường hợp đấy."*

## 3 Loại

### 1. Popup (Báo Cứng)

Popup không sinh flow phụ. User chỉ có option Close.

Examples:
- **Thông báo kết quả** — "Level 20 hoàn thành, +500 gold."
- **Error message** — "Không có kết nối internet."
- **Confirmation** — "Bạn có muốn thoát game?"

Action options trong popup:
- Close / Cancel → tắt popup, không thay đổi state.
- Confirm → execute action, tắt popup.

Đặc điểm: **luồng cứng**. Không thể go elsewhere.

### 2. State Của Button

State thay đổi thuộc button gốc.

Các state phổ biến:

| State | Trigger | Visual |
|-------|---------|--------|
| **Active** | Default | Solid color, glow |
| **Inactive (xám)** | Disabled / not available | Grayscale |
| **Locked** | Level chưa đủ | Padlock icon + text "Mở khi level 50" |
| **Loading** | Đang fetch data | Spinner icon |
| **Loading Fail** | Network error | Text "Tải lại?" |
| **Watch Ad** | Sau khi dùng free, available qua ad | Icon video |
| **Count-Down** | Sau action, cooldown | Timer text |

Đặc điểm: button visual + interaction thay đổi, không trigger flow mới.

### 3. Luồng Lên Đới (Flow-Up)

Bấm button sinh **flow phụ** khác (không phải popup đơn).

Examples:
- **Bấm Mua** → thiếu tiền → popup mua vàng → store → flow IAP.
- **Bấm Equip** → flow chọn vũ khí → flow chọn nhân vật → flow confirm.
- **Bấm Battle** → flow chọn team → flow chọn skill → battle screen.

Đặc điểm: flow lồng nhau, mỗi step có thể quay lại hoặc forward.

## Case Study Lucky Spin (4 States)

Vũ test 3 spawn types qua Lucky Spin button (logic: 1 lần free / 1 tiếng + 1 lần watch ad cộng dụng).

| State # | Icon | Màu | Trigger |
|---------|------|-----|---------|
| 1 | "Lucky Spin" text + icon | Vàng | Sẵn sàng quay free |
| 2 | "Turn back after X min" count-down | Xám | Đang cooldown |
| 3 | "Spin" + icon video | Xanh | Sau khi dùng free, xem ad để quay tiếp |
| 4 | "Level 20" + khóa | Xám-locked | Chưa đủ level |

Mỗi state là 1 case Type 2 (State của button). Transition giữa các state:

- State 1 → State 2 (sau quay)
- State 2 → State 1 (sau cooldown)
- State 1 → State 3 (sau dùng free, có ad available)
- State 4 → State 1 (sau lên level 20)

> *"Đề nghị các bạn vẽ như sau: nút này ở đây trạng thái 1, 2, 3, 4. Làm 1 thích nút ở bên cạnh: 1 là gì, 2 là gì, 3 là gì. Trường hợp nào từ 1 sang 2 hay 2 sang 3. File này thì sẽ là art và code dùng chung."*

State table = **single source of truth** cho cả art + code.

## Process Áp Dụng

Khi vẽ draft UI (Bước 2 của [[ui-wireframe-workflow]]):

1. List tất cả button trong màn.
2. Per button, đặt 3 câu hỏi:
   - Bấm → có popup không? Popup làm gì?
   - Bấm → state thay đổi không? Bao nhiêu state? Transition?
   - Bấm → flow phụ nào sinh ra? Map flow đó.
3. Document trong UI brief.

Nếu skip step này → discover case during dev → fix tốn time + bug.

## Anti-Pattern

- **Vẽ pixel mà không list case** — designer focus visual, dev hỏi "click vào thì làm gì?" → ad-hoc decision.
- **State thiếu** — không define disabled state → user thấy nút active mà bấm không có response → bug.
- **Flow Up không terminate** — flow phụ không có exit path → user stuck.
- **Popup gọi popup** — vi phạm [[ui-rule-max-2-levels]] (max 2 tầng).

## Liên Hệ Wiki

[[ui-wireframe-workflow]] cho workflow tổng thể (Bước 2 áp dụng framework này). [[ui-rule-max-2-levels]] cho rule tối đa 2 tầng flow lên đới. [[equip-flow-hero-vs-weapon]] cho case study flow lên đới phức tạp.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "3 Nảy Sinh Khi Bấm Nút", "Case Study: Lucky Spin — 4 Trạng Thái"
