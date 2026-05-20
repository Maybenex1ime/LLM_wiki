---
title: "Clash Royale Percent Stat Display — Base × (1 + % × level)"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ui, stat-display, balance-design, level-design]
aliases: [percent per level, base stat × level, Clash Royale stat innovation, simplification stat]
status: draft
related:
  - "[[skin-bridging-comparison]]"
  - "[[value-perception-techniques]]"
  - "[[ux-3-criteria]]"
summary: "Clash Royale thay đổi pattern stat: HP per level absolute (con A level 7 = 1450, level 8 = 1620) sang HP = Base × (1 + 10% × level). User chỉ nhớ base + level multiplier thay vì table absolute. Simpler stat = simpler UI = mass-market friendly."
---

## Định Nghĩa

Pattern stat display dạng **multiplicative** thay vì **absolute table**:

```
HP_final = Base_HP × (1 + percent_per_level × current_level)
ATK_final = Base_ATK × (1 + percent_per_level × current_level)
```

Vũ cite Clash Royale là pioneer pattern này trong mobile card games.

## Trước Clash Royale — Absolute Per Level

Pattern legacy:

| Card | Level 1 | Level 2 | ... | Level 10 |
|------|---------|---------|-----|----------|
| Knight | 700 | 770 | ... | 1330 |
| Wizard | 600 | 660 | ... | 1140 |

Designer phải define **stat absolute per level** trong Excel/Google Sheet. Mỗi card × mỗi level = 1 row.

Vấn đề:
- **Designer**: maintenance table phức tạp, balance change = update N rows.
- **User**: phải nhớ stat absolute để compare cross-level (con A level 7 vs con B level 8 — không có common base).
- **UI**: phải display full stat, không có shortcut.

## Sau Clash Royale — Multiplier Per Level

Pattern mới:

```
Knight base HP = 700, ATK = 70
Per level: +10%
Level 7 Knight: HP = 700 × (1 + 10% × 7) = 1190
Level 8 Knight: HP = 700 × (1 + 10% × 8) = 1260
```

Designer chỉ define **1 base stat + 1 multiplier**. Levels auto-compute.

Lợi:
- **Designer**: tweak base hoặc multiplier → tất cả levels recompute.
- **User**: nhớ base stat → biết all levels (math trong đầu hoặc UI hiển thị multiplier).
- **UI**: show base + level + computed final stat.

## UI Implication

### Display Pattern

UI hiển thị stat:
```
HP: 700 (base) × 1.7 (level 7) = 1190
```

User parse:
- Base 700 (đặc trưng card).
- 1.7 (level multiplier, scale theo level).
- 1190 (final value).

So sánh 2 card cùng level:
- Knight level 7: 1190 HP.
- Wizard level 7: 1020 HP.
- → User biết Knight strong hơn 17% vì cùng multiplier 1.7.

### Card Card Comparison

User scan card list:
- Card A base 700, card B base 600 → A 17% strong hơn.
- Apply multiplier theo level user current → biết relative strength.

Decision-making nhanh (1-2 giây) thay vì parse table.

## Tính Chất "Con Nào Tốt Từ Đầu = Tốt Mãi"

Theo Vũ:
> *"Con nào tốt từ đầu = tốt mãi mãi."*

Multiplier không scaling differently giữa các card → base stat hierarchy preserved across all levels.

Trade-off:
- **Lợi**: balance đơn giản, không có "comeback" mechanic.
- **Bất lợi**: user "ốc đảo" khi card đã tier thấp — không có upgrade path để bridge.

Fix: introduce **rare cards mới** hoặc **rebalance base stat** thay vì non-linear multiplier.

## Generalization Beyond Card Games

Pattern áp dụng cho mọi game có stat:
- **RPG**: hero base + level (Genshin Impact, đa số gacha).
- **Tower defense**: tower base + upgrade tier.
- **Idle game**: business base + multiplier (Adventure Capitalist).
- **MOBA**: champion base + level.

Đa số mobile game post-2017 dùng pattern này. Legacy game (pre-2014) hay còn table absolute.

## Math-Friendly cho User

Multiplier dễ tưởng tượng:
- +10% per level → level 10 = 2× base.
- +20% per level → level 5 = 2× base.

User mental model: "level 10 strong gấp đôi level 1." So với absolute table: "level 10 = 1620, level 1 = 700, ratio ... wait, calculate ..."

Cross-reference [[value-perception-techniques]] cho big numbers + fraction-friendly — multiplier là pattern fraction-friendly cho stat.

## Anti-Pattern: Mixed Pattern

Nhầm lẫn:
- Một số stat dùng absolute (HP), số khác dùng multiplier (ATK).
- Card này dùng pattern A, card khác dùng pattern B.
- → User confusion, không build mental model.

Stick với 1 pattern cho mọi card. Nếu cần exception (1-2 card legendary có scaling khác), document rõ.

## Anti-Pattern: Multiplier Quá Cao

> *"Bài học UI: simplification logic → simplification stat display → UI gọn hơn (chỉ cần show base stat + level multiplier)."*

Tuy nhiên nếu multiplier quá cao (+30% per level) → late game stat huge → cảm xúc không kéo dài.

Sweet spot: +5% đến +15% per level. Đảm bảo level 50 stat khoảng 3-5× level 1.

## Liên Hệ Wiki

[[skin-bridging-comparison]] cho A+ pattern (same skill set, stat khác) — multiplier là dạng A+ cho stat. [[value-perception-techniques]] cho big numbers + fraction-friendly — multiplier hỗ trợ cảm xúc. [[ux-3-criteria]] tiêu chí 2 (giảm thông tin) — multiplier display nhỏ hơn table absolute.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "Clash Royale Innovation — Tăng % Per Level"
