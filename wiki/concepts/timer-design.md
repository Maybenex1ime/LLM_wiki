---
title: "Timer Design (Puzzle)"
source: "compiled"
date_added: 2026-05-05
tags: [concept, level-design, timer, puzzle]
aliases: [thiết kế timer, time-based puzzle]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[level-iteration-testing]]"
  - "[[lion-studios]]"
summary: "Quy trình set timer cho puzzle level — before/after first test methodology của Lion Studios"
---

## Định Nghĩa

Timer là cơ chế giới hạn thời gian hoàn thành level (khác với move count limit). [[lion-studios]] khuyến nghị thêm timer khi game không có fail condition khác hoặc core game quá straightforward (chơi bằng reflex thuần túy).

Quote Playbook: "If your game doesn't have another fail condition or the core game is very straightforward to play (with reflexes), [add timer]."

## Before The First Test (Setup Without Data)

Cho game có 2-3 phút level duration, quy trình 5 bước.

Đầu tiên, playtest với dummy playing và record durations. First 5 levels add ít nhất 2-3 phút vào play data. Lvl 5-20 add khoảng 1 phút vào play data. Lvl 20+ add 30-45 sec vào play data. Cuối cùng, để tự động hoá levels khác, tính proportion of play time vs số moves to clear hoặc goal amount, multiply theo số đó cho mỗi level.

Ví dụ: nếu trung bình 20 items per level cho 120 sec → coefficient 6. Sau đó multiply level's number of items × 6 để guess timer cho new levels. Coefficient có thể tính riêng cho hard, medium, easy levels.

## After The First Test (Calibrate With Data)

Quy trình 4 bước với data thực tế:

1. Add another fail condition — keep eye on `fail by time %`
2. Nếu players churn khi % này tăng → cần decrease nó
3. Coefficient mới có thể tính từ data cho new levels sẽ add
4. Keep below 10% — dùng timer như gatekeeper, để players biết có timer nhưng fail vì condition khác

Quote Playbook: "You see something like: for hard levels, when the fail by time % is above 20%, the churn increases compared to the levels with similar fail rate. Then for these levels increase the time."

## Metrics To Track Cho Timer Levels

Khi dùng timer, theo dõi thêm:
- `avg time to fail`
- `avg time to win`
- `fail by time %` — nên giữ < 10%

Xem [[level-iteration-testing]] cho metrics đầy đủ.

## Triết Lý

Timer là gatekeeper, không phải primary fail condition. Người chơi nên fail vì decision (move count, blockers, strategy) — timer chỉ tồn tại để ngăn họ stall. Tỉ lệ "fail by time" cao báo hiệu timer quá tight hoặc level design có vấn đề. Đây là logic khác với reflex-based games (vd. cooking game) nơi timer là core mechanic.

Trong [[hard-level-design]], timer có thể dùng để tăng perceived difficulty mà không thay đổi actual difficulty — tức là level vẫn pass được, nhưng cảm giác urgency cao hơn → trigger booster usage.

## Nguồn Tham Khảo

- `raw/papers/Lion.pdf` (Level Design Playbook, slides 19-20)
