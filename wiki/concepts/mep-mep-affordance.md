---
title: "Mép Mép Affordance — Visual Cue Cho Vuốt"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-1-art]]"
date_added: 2026-05-20
tags: [concept, ux, ui, affordance, layout, mobile-design]
aliases: [mép mép, edge affordance, swipe cue, 5x6 grid layout, visible swipe hint]
status: draft
related:
  - "[[inherited-habit-conventions]]"
  - "[[thumb-zone-design]]"
  - "[[icon-vs-text-framework]]"
summary: "Layout trick: thay vì grid 6×5 trọn (30 card), dùng grid 5 × 6 + 'mép mép' phía dưới — user thấy rìa thừa → reflex vuốt → biết có thể scroll mà không cần tutorial. Hide affordance trong layout, không qua text/text/arrow."
---

## Định Nghĩa

Mép Mép Affordance = layout pattern hiển thị **rìa của row tiếp theo** (visual cue partial) → user reflex hiểu có thể scroll / vuốt.

> *"Phân bổ UI cũng đừng phân bổ kiểu 3 × 5 = 30. Mà nên phân bổ 30 × 5 — ở đây nó có một tí tí mép mép dưới để mọi người có behavior vuốt. Thì user nó biết là có thể vuốt được, mà không cần chèn ninh, không cần dạy dỗ gì cả."*

## Cơ Chế

### Pattern Đúng — Grid Mép Mép

Layout 30 cards (5 col × 6 row) trên màn:
- Visible row: 5 (cố định trên màn).
- Show: 4 full rows + 1 row "mép" (chỉ thấy 30-40% chiều cao).
- User reflex: "có thêm row dưới, scroll xuống."

```
[card][card][card][card][card]   ← row 1
[card][card][card][card][card]   ← row 2
[card][card][card][card][card]   ← row 3
[card][card][card][card][card]   ← row 4
[card][card][card][card][card]   ← row 5 (full)
[░░░][░░░][░░░][░░░][░░░]        ← row 6 (mép, 40%)
```

### Pattern Sai — Grid Trọn

Layout 30 cards (6 col × 5 row) trên màn:
- All 30 visible cùng lúc, fit grid 6×5.
- No mép → no cue cho scroll.
- User assume "đã xong" → không biết có gì thêm.

```
[c][c][c][c][c][c]
[c][c][c][c][c][c]
[c][c][c][c][c][c]
[c][c][c][c][c][c]
[c][c][c][c][c][c]
```

## Hide Affordance Trong Layout

Vũ key insight: **affordance hide trong layout chứ không expose qua text/arrow/tutorial**.

Pattern affordance:
- **Mép mép** = scroll affordance (vuốt up/down).
- **Edge fade** = scroll affordance (vuốt horizontal).
- **Card peeking** = pagination (vuốt left/right).
- **Bottom shadow** = "more content below."

User reflex hiểu mà không cần guide. Visual cue = silent communication.

## Áp Dụng Mép Mép

### Inventory Page

| Approach | Mép | UX |
|----------|-----|-----|
| 5 × 4 grid trọn | Không | User không biết scroll |
| 5 × 4 + mép row 5 | Có | User reflex scroll |
| 4 × 5 grid trọn | Không | User không biết scroll |
| 4 × 5 + mép col 5 | Có (horizontal) | User reflex scroll ngang |

Recommendation: chọn grid orientation theo gameplay context. Inventory = vertical scroll (mép dưới). Shop carousel = horizontal scroll (mép phải).

### Card Selection

Game thẻ bài: hiện 5-6 thẻ "có mép" thay vì 7-8 thẻ trọn. User scroll thấy thêm thẻ.

### Level Selection

Mobile puzzle game: hiện 4-5 levels + level tiếp theo có **mép** thấy 30%. User know "có level chưa unlock phía trước."

## Khi Nào Pattern Không Phù Hợp

Mép mép không phù hợp khi:
- **Fixed content** — chỉ có 4 elements, không có gì thêm. Hiển thị trọn.
- **Modal popup** — content tự contained, không scroll.
- **Tutorial overlay** — user đang được guide, mép cue confusing.
- **Whale UI** — premium feel, mọi thứ visible (không hide).

## Implementation Notes

### CSS / Game UI Spec

Cho row mép:
- Height: 30-40% của row chuẩn.
- Opacity: full (không fade — fade là pattern khác).
- Position: sticky bottom of visible area.

### Touch Target

- Tap được vào mép row → scroll snap to next row.
- Long-press không trigger action (vì user expect scroll).

### Animation

- Row mép có thể subtle bounce khi page load (cue motion).
- Sau bounce xong → static.
- Re-bounce khi user idle 10s.

## Anti-Pattern

- **Arrow icon "swipe down"** — text/arrow workaround thay vì silent design.
- **Tutorial popup "vuốt để xem thêm"** — friction, modal break flow.
- **Mép cho fixed content** — confusing (user vuốt không có gì).
- **Mép quá nhỏ** (<20%) — user không thấy → no cue.
- **Mép quá lớn** (>50%) — user nhầm là full row.

## Liên Hệ Wiki

[[inherited-habit-conventions]] cho universal patterns user đã biết — mép mép là 1 affordance pattern phổ thông. [[thumb-zone-design]] cho khoảng cách vùng tay với mép — mép phải reachable. [[icon-vs-text-framework]] cho rule không dùng text/arrow guide khi có thể silent.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-1-art.md` § "Size Card Cho Bàn Đấu — 32 Thẻ Trên 1080×1920", "UX Cue: Mép Mép Phía Dưới"
