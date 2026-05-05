---
title: "Easy Level Design"
source: "compiled"
date_added: 2026-05-05
tags: [concept, level-design, puzzle]
aliases: [thiết kế level dễ, easy level]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[ftue-curve]]"
  - "[[level-funnel-heartbeat]]"
  - "[[rv-placement-strategy]]"
  - "[[lion-studios]]"
summary: "Easy level <1.3 attempts — chứa monetization potential lớn nếu làm khó hơn 1 chút và ngắn hơn 20%"
---

## Định Nghĩa

Easy level là level có average attempts to complete dưới 1.3 lần (theo [[lion-studios]]). Theo dữ liệu Playbook, easy levels có level fail rate khoảng 10-15%, churn cực thấp, và coin sink vẫn mạnh.

## Triết Lý "Easy = Boring"

Lion Studios chỉ ra: easy không có nghĩa là levels trông đơn giản. A/B test giữa "Old Funnel" và "New Funnel" cho game Unpuzzle - Block Puzzle Tap Away cho thấy "new version with crowded early levels outperformed". Tức là levels đầu trông phức tạp (nhiều objects, dense visual) nhưng mechanic dễ vượt qua.

Quote MVP Guide: "Focus on hooking users and creating the expertise. Early levels can look challenging but actually be easy to complete."

## Visual Variety

Theo Playbook, ~25-30% của level mix nên là "visual levels" — levels có symmetry, visual patterns, casual figures. Avoid monotony bằng cách segment levels theo chủ đề khác nhau và loop chúng trong level mix:

- **Theme-based** (ví dụ music objects)
- **Color-based** (ví dụ pink objects)
- **Shape-based** (ví dụ cylindrical objects)

Playbook bổ sung ASMR effects: chain reactions, unlocks, surprises để tăng engagement của level dễ.

## Monetization Trong Easy Level

Easy level thường bị bỏ qua khi tối ưu monetization vì designer focus vào hard levels. Lion Studios cho rằng đây là sai lầm: "There is a big potential in easy levels as well".

Hai chiến thuật cụ thể. Một là làm easy levels khó hơn 1 chút — slightly tăng fail rate để tạo "easy win sink", người chơi vẫn hoàn thành nhưng dùng coin/booster. Hai là giảm thời lượng easy levels khoảng 20% so với mid/hard levels — tăng playtime của user qua nhiều levels nhanh hơn, nhiều inter ad impressions hơn.

## RV Placement Trong Easy Level

Easy levels có thể maximize RV power (về amount hoặc placement) vì người chơi ít có khả năng monetize qua các elements khác trong level dễ. Ví dụ Playbook: 3 RVs trong một easy level. Xem [[rv-placement-strategy]] để chi tiết.

## Vai Trò Trong Funnel

Easy levels là cooldown sau hard level — "Use easy level to take the pressure out of the player before increase the heat up!". Pattern điển hình sau D0:

```
Hard → Easy (cooldown) → Warm-up → Mid → Mid → Hard
```

Xem [[level-funnel-heartbeat]] để hiểu cách bố trí easy levels trong loop 10 levels hằng ngày.

## Nguồn Tham Khảo

- `raw/papers/Lion Studios MVP Guide.pptx.pdf` (slide 10)
- `raw/papers/Lion.pdf` (Level Design Playbook, slides 4-5, 14-15)
