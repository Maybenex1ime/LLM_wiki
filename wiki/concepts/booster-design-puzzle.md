---
title: "Booster Design (Puzzle)"
source: "compiled"
date_added: 2026-05-05
tags: [concept, monetization, booster, puzzle]
aliases: [thiết kế booster, booster combo, booster rollout]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[ftue-curve]]"
  - "[[rv-placement-strategy]]"
  - "[[lion-studios]]"
summary: "Booster design theo Lion Studios — 3 function types (PA/SE/RD), combo composition, rollout schedule"
---

## Định Nghĩa

Booster trong puzzle game là power-up người chơi dùng để vượt qua thử thách. [[lion-studios]] phân loại booster theo 3 function types và đề xuất combo composition cùng rollout schedule cụ thể.

## Booster Function Types

| Loại | Ví dụ | Vai trò |
|---|---|---|
| **Progression Accelerator (PA)** | Hammer, rocket | Clears blockers, helps stuck players |
| **Strategic Enhancer (SE)** | Swap, color bomb | Adds tactical choices, has strategic depth |
| **Revenue Driver (RD)** | Premium tool | Powerful but costly — great for monetization layers |

Quy tắc Lion Studios: "Don't add them just to have many boosters, add them if they really have different function and use".

## Booster Combo Composition

Combo là tập hợp booster game của bạn nên có. Lion Studios khuyến nghị 1 trong 3 mức:

| Combo | Thành phần | Khi dùng |
|---|---|---|
| `1PA + 1SE` | 1 PA + 1 SE | Game đơn giản, ít depth |
| `1PA + 1SE + 1RD` | + 1 Revenue Driver | Game muốn monetize tốt hơn |
| `2PA + 1SE + 1RD` | 2 PA (vd. hammer + rocket) | Game có nhiều loại blocker khác nhau |

Sự khác biệt giữa "combo" (composition) và "rollout" (timing) là quan trọng. Combo trả lời câu hỏi "có những booster gì". Rollout trả lời câu hỏi "khi nào introduce mỗi cái".

## Rollout Schedule

5 quy tắc rollout của Lion Studios:

1. Tránh introduce tất cả booster cùng lúc / back-to-back
2. Tutorial booster chỉ sau khi đã dạy core gameplay (vài levels đầu)
3. Introduce booster ngay trước challenge spike đầu tiên — để có lý do dùng
4. Roll out theo thứ tự tăng dần power — match với độ khó tăng dần
5. Tutorial booster không bắt người chơi làm quá 2 steps of action

### Ví Dụ Schedule

Game 8-10 min/3 levels đầu:

```
Lvl 4:  1st booster (PA)
Lvl 5:  1st little challenge       ← lý do dùng booster vừa học
Lvl 6:  2nd booster (SE)
Lvl 9:  3rd booster (RD)
Lvl 12: 1st real challenge
```

Game ngắn hơn (5 min × 5 levels đầu):

```
Lvl 6:  1st booster
Lvl 7:  1st little challenge
Lvl 8:  2nd booster
Lvl 11: 3rd booster
Lvl 14: 1st challenge
```

## Liên Hệ Với Hard Level

Booster là cơ chế monetization cốt lõi của [[hard-level-design]]. Foreseeable failure trong hard level tạo window bán booster (trước khi fail). Revive sau khi fail là một dạng RD đặc biệt. Booster placement không nên cannibalize RV revenue — xem [[rv-placement-strategy]] để hiểu cách balance giữa booster và rewarded video.

Trong [[ftue-curve]], booster đầu tiên introduce ở Lvl 4-6 (tùy độ dài level), ngay trước first little challenge.

## Nguồn Tham Khảo

- `raw/papers/Lion.pdf` (Level Design Playbook, slides 21-22)
