---
title: "New Mechanic Introduction"
source: "compiled"
date_added: 2026-05-05
tags: [concept, level-design, mechanic, puzzle]
aliases: [introduce mechanic mới, mechanic rollout]
status: draft
related:
  - "[[ftue-curve]]"
  - "[[hard-level-design]]"
  - "[[booster-design-puzzle]]"
  - "[[lion-studios]]"
summary: "Khi nào và cách introduce mechanic mới trong puzzle — D0/D1 explore (2-3), D2-D4 (1/day), D5+ every other day"
---

## Định Nghĩa

Mechanic là yếu tố gameplay mới (blocker, generator, helper, rescue tool, unlock target) thêm vào level để tạo depth. Theo [[lion-studios]], mục tiêu chính của introduce mechanic mới là avoid monotony, không phải tăng difficulty thuần túy.

Quote Playbook: "Very first mechanics should focus more on avoiding monotony to increase retention rather than increasing depth because players are already trying to understand the core game."

## Mechanic Categories

Playbook phân loại mechanic theo 8 categories:

| Category | Ví dụ | Mô tả |
|---|---|---|
| Unlock - Goal Based | Locked Slot | Tồn tại đến khi unlock |
| Unlock - Match Based | Wood, Safe | Hit để clear / build stack |
| Unlock - Color Based | Playpen | Hit khi cùng màu |
| Generator - Static | Camera | Hit để đạt goal |
| Generator - Disposable | Gem | Cân nhắc hit hay không |
| Helper | Firecracker | Clear neighbors |
| Rescue | Car | Color-based escape |
| Other | Jelly | Hit từ specific position |

## Onboarding Pace

Lion Studios benchmark onboarding pace cho 7 ngày đầu:

| Ngày | Số mechanic mới | Vai trò |
|---|---|---|
| D0-D1 | 2-3 core features | Exploratory experience |
| D2-D4 | 1 feature/ngày | Continued exploration |
| D5+ | Every other day | Reduced pace |

Quote: "D0 and D1 are an exploratory experience. Usually 2-3 core features, that'll be used frequently following days, are introduced."

## Benchmark Implementation Levels

Cho game có ≥2 phút level duration, Lion Studios đề xuất 4 mechanic đầu tại các lvl:

| # | Lvl | Đặc điểm |
|---|---|---|
| #1 | Lvl 11 | Extremely basic, no learning curve |
| #2 | Lvl 25 | First variety, very short learning curve |
| #3 | Lvl 45 | Different variety, short learning curve |
| #4 | Lvl 70 | Show some depth, có thể là helper |

## Validation: Compare With Similar Fail Rate Levels

Khi implement mechanic mới, validate bằng cách compare level chứa mechanic mới với no-mechanic levels có fail rate tương tự. Nếu mechanic mới gây churn cao hơn đáng kể → mechanic có vấn đề. Có thể fix bằng cách đặt mechanic ở lower fail rate level (sweet spot), hoặc remove mechanic.

## Best Practices

Do: use widely known objects và create ASMR effects; objects và mechanics nên có intuitive connection; keep coherence giữa mechanic art style và theme; focus on surprising players, giving more challenge, helping them, hoặc change the way they strategize.

Don't: don't change the core rules; don't overcomplicate it; don't neglect fundamental UX rules; don't use realistic looking animals like snake và frog.

## Liên Hệ Với Hard Level

Mechanic mới luôn introduce trước hoặc trong hard level (xem [[hard-level-design]]) — để người chơi có lý do thực tế để học. Trong [[ftue-curve]], first hard level (Lvl 11-14) phải đặt ngay sau first mechanic tutorial.

Mechanic introduction khác với booster introduction. Mechanic là yếu tố level-content (tile, blocker, target). Booster là power-up người chơi dùng — xem [[booster-design-puzzle]].

## Nguồn Tham Khảo

- `raw/papers/Lion.pdf` (Level Design Playbook, slides 16-18, 23)
