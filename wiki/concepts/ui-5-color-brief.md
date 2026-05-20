---
title: "UI 5-Color Brief — Convention Cho File UI"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ui, brief, color-convention, gd-craft, documentation]
aliases: [5 màu UI, color convention brief, đỏ cam vàng xanh-lá xanh-dương, file UI 5 colors]
status: draft
related:
  - "[[ui-button-3-levels]]"
  - "[[ui-wireframe-workflow]]"
  - "[[dark-ux-techniques]]"
summary: "Vũ chốt 5 màu code chuẩn cho file UI brief (art + code đều đọc): đỏ (chú ý cao, IAP), cam (monetize, ad), vàng (core gameplay), xanh lá (deemphasize, setting), xanh dương (rare, gây nhuận lận). Plus document color convention: đen/đỏ/xanh-lá cho text in doc."
---

## Định Nghĩa

5-Color Brief = convention màu Vũ chốt cho **file UI brief** — đảm bảo art và code đọc cùng ngôn ngữ về priority.

> *"File UI brief — 5 màu code (art + code đều đọc)."*

## Bảng 5 Màu

| Màu | Ý Nghĩa | Ví Dụ |
|-----|---------|-------|
| 🔴 **Đỏ** | Phải chú ý cao, làm đẹp nhất | Pop-up starter pack, event banner, IAP shop |
| 🟠 **Cam** | Liên quan monetize | Nút xem reward ad |
| 🟡 **Vàng** | Tính năng core, user phải đọc/hiểu | Battle button, gameplay HUD |
| 🟢 **Xanh Lá** | User bớt focus | Setting, refund button (cần có nhưng mờ đi) |
| 🔵 **Xanh Dương** | Gây nhuận lận (rare) | Icon video màu đỏ giả YouTube, asymmetric button size |

## Per Color

### 🔴 Đỏ — Maximum Attention

Reserve cho:
- **Pop-up starter pack** (D0-D3, highest LTV impact).
- **Event banner** (event-driven monetization).
- **IAP shop entry** (entry to monetization).
- **Limited-time offer** (FOMO trigger).

Art treatment:
- Glow / pulse animation.
- Bigger size than surrounding.
- Premium typography.
- Centered hoặc thumb zone.

### 🟠 Cam — Monetize Action

Reserve cho:
- **Reward ad button** ("xem ad +2x reward").
- **Continue with ad** (after fail level).
- **Double Down** (gambling ad pattern).
- **Skip with gem** (paid skip).

Art treatment:
- Video icon clearly visible.
- Distinct from organic Vàng (gameplay).
- Subtle animation (không over-the-top như Đỏ).

### 🟡 Vàng — Core Gameplay

Reserve cho:
- **Battle / Play button**.
- **Skill cast button**.
- **Move / Action button**.
- **Currency display** (gold, gem).

Art treatment:
- Always visible.
- Standard size, no animation unless critical.
- Position theo thumb zone for must-tap actions.

### 🟢 Xanh Lá — Deemphasize

Reserve cho:
- **Setting** (gear icon).
- **Refund** (rarely-used utility).
- **Mail / Inbox** (informational).
- **About / Credits**.

Art treatment:
- Smaller size.
- Less saturated color.
- Position góc top-right (out of thumb zone).
- Có thể collapse vào tab.

### 🔵 Xanh Dương — Confusion Trigger (Rare)

Reserve cho:
- **Icon video màu đỏ giả YouTube** — user reflex tab → drop ad.
- **Asymmetric button size** — break grid pattern.

⚠️ Sử dụng cẩn thận — nhiều dùng = lose trust.

> *"Các bạn art rất thích vẽ icon video màu đỏ giống YouTube. Tóm lại là cái icon màu đỏ nó sẽ rất là sợ — nguy hiểm."*

User reflex: thấy đỏ giống YouTube → tab ra → drop ad rate. GD phải explicitly require **small + side + mờ** cho ad icon.

Cross-reference [[dark-ux-techniques]] cho deeper dive vào "gây nhuận lận" tactics.

## Document Color Convention

Tương tự cho **text trong document** (UI brief / spec):

| Màu Text | Ý Nghĩa |
|----------|---------|
| **Đen** | Sẽ làm bản này, hoặc đã làm bản cũ |
| **Đỏ** | Update làm bản tới (highlight ưu tiên) |
| **Xanh Lá** | Ghi chú lung tung, đừng đọc vào (ghi cho bản sau) |

> *"GD viết note tương lai ngay trong doc chung → màu xanh lá → người khác auto skip."*

Lợi:
- Doc shared, không cần tách file per version.
- Reader nhanh chóng identify "what's in scope this sprint."
- Note long-term ý tưởng không lose, lưu vào doc cùng context.

## Implementation Notes

### File Format

Excel / Google Sheets / Notion với cell coloring. Mỗi row = UI element. Cột:
- Element name.
- Description.
- Priority color (background cell).
- State table reference.
- Owner (art / code / GD).

### Pixel Art Translation

Art không vẽ literally 5 màu vào game. Convention chỉ trong brief — game art có thể dùng palette riêng.

Translation:
- 🔴 → premium gold/red palette trong game.
- 🟠 → secondary action palette (video icons).
- 🟡 → core action palette.
- 🟢 → muted neutral palette.
- 🔵 → standout palette per use case.

### Code Translation

Code đọc brief để biết priority button → apply animation rules:
- Đỏ → enable pulse animation, glow shader.
- Cam → enable ad icon, video preview on hover.
- Vàng → standard render.
- Xanh lá → reduced opacity.
- Xanh dương → custom render per case.

## Anti-Pattern

- **Dùng convention khác giữa team** — art dùng 5 màu khác, code dùng 5 màu khác → confusion.
- **Đỏ ai cũng dùng** — Đỏ lose impact khi quá nhiều UI dùng.
- **Document text 5+ colors** — confusion. Stick với 3 colors (đen/đỏ/xanh lá).
- **Skin variant gắn vào convention màu** — convention là priority, không phải skin. Skin dùng palette khác.

## Liên Hệ Wiki

[[ui-button-3-levels]] cho 3 level button — convention màu map vào levels (Key = vàng/đỏ, Blue = cam/xanh lá, Hidden = xanh lá). [[ui-wireframe-workflow]] cho workflow apply convention. [[dark-ux-techniques]] cho deep-dive vào "gây nhuận lận" trong Xanh Dương category.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "File UI Brief — 5 Màu Code"
