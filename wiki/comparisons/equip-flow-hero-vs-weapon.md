---
title: "Equip Flow — Từ Hero vs Từ Weapon"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [comparison, ui, ux, equip-flow, hero-design, weapon-design]
aliases: [equip flow, từ nhân vật vs từ vũ khí, hero-first vs weapon-first equipment]
status: draft
related:
  - "[[ui-wireframe-workflow]]"
  - "[[auto-equip-design]]"
  - "[[ux-3-criteria]]"
summary: "2 approach equip: từ Hero (bấm hero → list weapon available) vs từ Weapon (bấm weapon → chọn hero). Hero-first dễ ở 1-equip lần đầu, weapon-first dễ khi switch nhiều con + xem tổng quan rare hierarchy. Vũ chốt: phải có 2-3 drafts để compare, không pick 1 phương án rồi tự bảo 'tốt nhất'."
---

## Bối Cảnh

Đức (học viên có game thẻ bài) hỏi Vũ về approach equip vũ khí cho nhân vật. Vũ teach qua case study chi tiết, chốt: GD phải vẽ **multiple drafts** rồi compare bằng số bước / dễ hiểu.

> *"Phải có 2 phương án mới so sánh được. Yêu thì yêu 2-3 cô — yêu mỗi 1 đứa rồi bảo là tốt nhất trần đời xem chừng nó bốc phép."*

## Bảng So Sánh

| Tình Huống | Approach A (Từ Hero) | Approach B (Từ Weapon) |
|------------|----------------------|------------------------|
| **Equip lần đầu** | 3 bước | 3 bước |
| **Switch giữa nhiều con nhanh** | Nhiều bước (mỗi con select riêng) | Ít hơn (chỉ bấm hero icon) |
| **Upgrade vũ khí** | Phải vào info ngược | Trực tiếp từ inventory |
| **Biết owner hiện tại của vũ khí** | Phải dò | Hiện icon owner ngay |
| **Tổng quan rare hierarchy** | Khó (phải chuyển qua từng hero) | Dễ (xem inventory list) |
| **User decision driver** | Bám theo hero (con này dùng gì) | Bám theo weapon (vũ khí này cho con nào) |

## Approach A — Từ Hero

Flow:
1. User bấm **hero**.
2. Popup vũ khí available cho hero này (2/3 màn hình).
3. Tap weapon → equip ngay.

Total: 3 bước (tap hero, tap weapon, action equip).

### Lợi

- **Hero-first thinking** — user nghĩ "con này dùng vũ khí gì hợp?" → decision driven by hero.
- **Tutorial dễ** — fresh user hiểu ngay (đại đa số RPG dùng pattern này).
- **Implicit filter** — hero level / rarity quyết định weapon nào show → giảm choice paralysis.

### Hạn Chế

- Switch nhiều hero → multi-step.
- Không tổng quan inventory weapon — user không biết weapon nào rare nhất.
- Upgrade weapon phải dive vào hero info → quay vòng tốn.

### Phù Hợp

- Game **few hero** (1-5 hero) — switch ít.
- Game **simple equipment** — không có rare hierarchy phức tạp.
- Game **tutorial-heavy** — guide flow theo hero progression.

## Approach B — Từ Weapon

Flow:
1. User mở **inventory weapon**.
2. Tap weapon → popup info.
3. Tap "Equip" → chọn hero từ list.

Total: 3 bước (open inventory, tap weapon, choose hero).

### Lợi

- **Tổng quan inventory** — user nhìn rare hierarchy ngay từ list.
- **Switch fast** — biết hero nào owning weapon nào, swap dễ.
- **Upgrade direct** — weapon info có nâng cấp button.
- **Trade-up thinking** — user nghĩ "weapon này cho con nào tốt hơn?"

### Hạn Chế

- **First-time user** confusion — không quen pattern.
- **Decision overhead** — user phải compare hero compatibility.
- **Hidden info** — không tab tap hero không thấy weapon owned.

### Phù Hợp

- Game **many hero** (10+ hero) — switch nhiều.
- Game **deep equipment** với rare hierarchy.
- Game **post-tutorial** — committed user.

## Hybrid Approach — Icon Owner

Vũ đề xuất improvement:

> *"Hiển thị icon owner trên vũ khí trong inventory: Icon màu vàng = đang cầm bởi tướng legendary. Icon màu xanh = đang cầm bởi tướng rare. Vũ khí không có icon = available."*

Apply cho cả 2 approach:
- Approach A: trong popup weapon list, show icon owner (helpful when weapon equipped by another hero).
- Approach B: trong inventory list, show icon owner default.

User nhìn ngay biết phải tháo của ai → reduce decision time.

## So Sánh Số Bước Cụ Thể (Hiệp's Game)

Hiệp (case Doc 7) đã quên nút Swap → original Approach A là **6 bước** thay vì 3. Sau optimize:

| Iteration | Flow | Bước |
|-----------|------|------|
| Original Approach A | Hero → list → ?  → swap → confirm → done | 6 |
| Optimized Approach A | Hero → tap weapon → done | 3 |
| Approach B | Weapon → tap equip → choose hero | 3 |
| Approach C (Auto-Equip) | Hero → auto-equip best | 2 |

Xem [[auto-equip-design]] cho Approach C — phù hợp game 1-hero hoặc 10+ hero, fail ở 1-5 hero không có fun role.

## Phương Án Số Hiển Thị Inventory

Có 3 strategy hiển thị inventory khi user bấm hero (Approach A):

| Strategy | Mô Tả | Phù Hợp |
|----------|-------|---------|
| **Hiện Tất Cả** | Including weapons đang cầm bởi hero khác | Tổng quan rare hierarchy + Vũ recommend |
| **Chỉ Phù Hợp Slot** | Kiếm thì không hiện cung | Giảm choice paralysis |
| **Chỉ Available** (exclude cầm) | User không cần tháo của hero khác | Friction-free flow |

> *"Hiện tất cả những con đang còn, đang có, kể cả con khác. Thằng này có thể nhìn tổng quan tất cả vũ khí — bạn có thể thấy biết được cái nào đa hơn cái nào luôn mà không cần phải so sánh."*

Vũ recommend **Strategy 1 + Icon Owner** cho game tướng meta:
- User nhìn tổng quan rarity ngay.
- Biết owner → quyết định tháo của ai để equip cho new hero.
- Reduce friction trong meta-decision making.

## Kết Luận

Không có "best approach universal." Decision dựa trên:
- **Số hero**: few (Approach A) vs many (Approach B).
- **Equipment depth**: simple (A) vs deep (B).
- **Game phase**: tutorial (A) vs post-tutorial (B).
- **User archetype**: skill (A, hero-first thinking) vs asset (B, inventory thinking).

Designer phải **draft both**, test với users, pick winner. Không pick 1 phương án rồi tự bảo "best."

## Liên Hệ Wiki

[[ui-wireframe-workflow]] cho workflow draft 2-3 phương án. [[auto-equip-design]] cho Approach C (auto-equip) — case study mở rộng. [[ux-3-criteria]] tiêu chí 1 (giảm bước) — basis cho compare 2 approach.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "Case Equip Vũ Khí — Bài Toán Khó Nhất", "Hiển Thị Inventory — 3 Strategies"
