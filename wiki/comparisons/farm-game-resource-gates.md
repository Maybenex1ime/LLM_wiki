---
title: "Farm Game Resource Gates — Facebook Farm vs Hay Day vs Township"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [comparison, ux, monetization, farm-game, resource-gate, retention]
aliases: [farm game evolution, Facebook Farm vs Hay Day, Township resource gate, farm UX]
status: draft
related:
  - "[[ux-yeu-ich-definition]]"
  - "[[material-count-decision-paralysis]]"
  - "[[heart-system-design]]"
summary: "3 thế hệ farm game cùng core 'trồng cây' nhưng resource gate khác nhau → UX hoàn toàn khác. Facebook Farm (theft + seed hard cap), Hay Day (seed soft cap), Township (tiền thay seed, batch unlimited). Bài học: phân tích mechanic ở level resource-gate, không ở surface."
---

## Bối Cảnh

3 game farm trên timeline khác nhau, cùng core mechanic "trồng cây - thu hoạch - bán." Vũ kể qua Doc 6 Part 2 như case study về vì sao "cùng mechanic không = cùng UX."

> *"Trồng cây của 3 con này khác gì nhau? Mình phân tích cho các bạn xem là mọi người đã nói là đều trồng cây nhưng mà cái đấy nó không đủ. Trồng cây bằng cái gì và vì sao ta làm cái đó? Đấy mới là vấn đề."*

## Bảng So Sánh

| Aspect | Farm (Facebook ~2009) | Hay Day (2012+) | Township (2013+) |
|--------|------------------------|------------------|-------------------|
| **Trồng từ gì** | Hạt giống | Hạt giống | Tiền (gold) |
| **Hard cap** | Hạt giống có hạn + thằng vặt trộm | Hạt giống có hạn | Không có (chỉ giới hạn theo tiền) |
| **Trộm cây từ người khác** | Có (Farmville) | Không | Không |
| **Cây héo** | Có (nếu không thu) | Có | Không (cây giữ vĩnh viễn cho đến khi thu) |
| **Batch planting** | 1 hạt 1 lần | 1 hạt 1 lần | 50+ hạt 1 lần |
| **Trải nghiệm chính** | Stress (lo bị trộm) | Quản lý ngày 1-2 lần | "Vè vè vè vè" |
| **Habit driver** | Đăng nhập canh giờ | Đăng nhập hai lần/day | Đăng nhập tự do |
| **Monetization gate** | Mua hạt giống premium | Mua hạt giống / accelerator | Mua gem để accelerate |

## Phân Tích Theo Trục

### Facebook Farm (Farmville) — Punishment Model

User behavior:
- Trồng cây → đi ngủ.
- Sáng hôm sau: cây bị trộm bởi bạn bè trong network.
- Stress + FOMO → log in thường xuyên để defend.

UX:
- **Negative emotion** drive engagement.
- High retention ngắn hạn (D1-D7 thấp churn).
- Low long-term retention — user burnout vì stress.

Punishment-driven design = đời đầu social farming. Phase out qua thời gian (xem [[clash-of-clans-punishment-evolution]] cho pattern tương đương trong combat game).

### Hay Day — Punishment Soft

User behavior:
- Trồng cây từ hạt giống (limit).
- Không có trộm → bớt stress.
- Cây héo nếu không thu → soft penalty (retention pressure mild).

UX:
- Removed theft, kept seed scarcity.
- Mass-market casual friendly.
- Monetize qua: mua hạt + accelerate growth.

Hay Day là **bước trung gian** — phase out trộm, keep seed gate.

### Township — Frictionless Batch

User behavior:
- Có nhiều tiền → tap "plant 50" → batch plant 1 màn ruộng.
- *"Em bán vè vè vè vè, hôm hôm phát 4 50 cái luôn."*
- Không có hạt limit, không có héo.

UX:
- **Positive emotion** — cảm giác "ăn được" liên tục.
- Habit formation qua repetition không có friction.
- Monetize: gem để accelerate growth time, gem để mua bằng tiền tài nguyên.

> *"Cứ vào vẹt cái quẹt cái xong đi chỗ khác chơi thôi. Cảm giác rất sướng."*

Township là **frictionless** evolution. Resource gate chuyển từ scarcity (hạt) → time (chờ cây mọc) → money (accelerate).

## Phân Tích

### Cùng Mechanic, Khác Resource Gate → Khác UX

Surface mechanic giống nhau: trồng cây.

Resource gate khác nhau:
- Farm: hạt giống + theft.
- Hay Day: hạt giống.
- Township: tiền.

UX khác hoàn toàn:
- Farm: stress + social pressure.
- Hay Day: management routine.
- Township: dopamine batch reward.

Bài học: **không design ở level mechanic, design ở level resource gate**.

### Trend: Bỏ Hard Punishment, Tăng Frictionless

Trajectory rõ ràng từ 2009 → 2013:
1. Theft → Heo cây → No penalty.
2. Hạt limit → Tiền limit → Unlimited (bounded only by money).
3. 1-hạt/lần → Batch.

Pattern same với [[clash-of-clans-punishment-evolution]]: mature studios phase out punishment qua iterations.

### Monetization Implication

Punishment-driven (Farm): user mua hạt premium để defend cây / replant.

Frictionless (Township): user mua gem để **accelerate** progression — không phải để defend.

**Tăng convert rate** vì user mua trong trạng thái sướng (accelerate sướng tiếp), không mua trong trạng thái stress (defend khỏi loss).

## Kết Luận

Phân tích mechanic ở surface level (như nhau, cùng "trồng cây") = useless. Phải dissect ở:
- **Resource gate**: cái gì limit user action?
- **Penalty model**: lose gì khi fail?
- **Reward delivery**: batch hay incremental?

Township là example tối ưu **frictionless casual** trong genre farm. Modern farm games (FarmVille 3, FarmCity) đều adopt Township pattern.

Designer làm farm new → start với Township pattern, không Farm pattern.

## Liên Hệ Wiki

[[ux-yeu-ich-definition]] cho khung UX dual-goal. [[material-count-decision-paralysis]] cho cùng logic (simpler resource = better UX). [[heart-system-design]] cho monetize qua time-gate (similar trade-off). [[clash-of-clans-punishment-evolution]] cho parallel pattern phase out punishment.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Farm Games — 3 Generations"
