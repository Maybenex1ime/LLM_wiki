---
title: "Match-3 Difficulty Levers — 5 Yếu Tố Tạo Độ Khó"
source: "[[raw/videos/negaxy-iec-gd-doc-02-level-design]]"
date_added: 2026-05-15
tags: [concept, level-design, match-3, difficulty]
aliases: [5 yếu tố tạo khó Match-3, difficulty levers Match-3, tắc ẩn]
status: draft
related:
  - "[[hidden-variable-difficulty]]"
  - "[[chip-spawn-algorithm]]"
  - "[[hard-level-design]]"
  - "[[match3-player-archetypes]]"
summary: "5 levers cốt lõi để tạo độ khó trong Match-3/Candy Crush style: giới hạn tài nguyên, obstacle, bài trí ban đầu, mục tiêu, và tắc ẩn (RNG có chủ đích)"
---

## Định Nghĩa

Vũ yêu cầu học viên liệt kê *"có bao nhiêu cách để làm tắc một level"* và tổng hợp được 5 yếu tố cốt lõi áp dụng cho Match-3 / Candy Crush style:

1. **Giới hạn tài nguyên** — time, số mu (moves).
2. **Obstacle / mật độ chướng ngại** — số lượng và phân bố vật cản trên board.
3. **Bài trí ban đầu** — cách xếp object ở thời điểm start level.
4. **Mục tiêu** — số lượng goal cần đạt.
5. **Tắc ẩn** — thông qua thuật toán sinh chip, drop rate, logic reveal key object. Tắc không thông qua 4 yếu tố trên mà thông qua RNG có chủ đích.

4 yếu tố đầu là **biến hiển thị** (user nhìn vào board sẽ thấy). Yếu tố thứ 5 là **biến ẩn** — user không nhận ra. Phân biệt này quan trọng cho monetization và adaptive difficulty.

## Tắc Ẩn — RNG Có Chủ Đích

Đây là lever đặc thù của Match-3 / puzzle có random fill. Vũ giải thích bằng quote điển hình:

> *"Tại sao trong vòng lần 1, lần 2, lần 3 các bạn chơi không qua, lần 4 các bạn lại qua? Vì bước đi nó khác. Khi mà set up ban đầu, tất cả các đoạn chip — các viên nhỏ nhỏ — bản thân các chip đấy sẽ chỉ được sinh ra theo tỉ lệ và sinh ra theo bố cục."*

Tắc ẩn bao gồm:
- **Tỷ lệ chip drop từng màu** (5 màu đều 20% là khó nhất; lệch tỷ lệ thì dễ hơn).
- **Bias ô liền kề** (muốn dễ thì cho ô trên khác màu với ô dưới, tăng khả năng combine).
- **Logic adaptive key object** (object thứ 5 chỉ xuất hiện khi còn 10 nước đi; fail thì cộng 5 mu lần sau).
- **Logic reveal sau khi user mua moves bằng tiền** — *"Phải cho nó thắng, không nó bỏ mẹ em đi."*

Xem [[chip-spawn-algorithm]] cho thuật toán cụ thể, và [[hidden-variable-difficulty]] cho cách dùng tắc ẩn để chỉnh khó sau khi user IAP.

## Quan Hệ Giữa Các Lever

5 lever không độc lập — chúng tác động lẫn nhau:

- Tăng số mu (lever 1) làm dễ → cần tăng obstacle (lever 2) hoặc lệch chip drop (lever 5) để giữ độ khó.
- Tăng số goal (lever 4) làm khó → có thể bù bằng tỷ lệ chip favorable (lever 5).
- Bài trí ban đầu (lever 3) quyết định *"distance to first combo"* — board mà 2 chip cùng màu gần nhau sẽ dễ.

Vũ cảnh báo anti-pattern: *"Cứ cộng vào liên tục để tạo ra độ khó thì không đúng nhé. Tới giờ làm thế là rất khó control."* Quy đổi nhiều lever về **1 biến cuối** (thường là số mu) để control — xem [[file-y-do-design-intent]] cho file ý đồ chốt 1 biến.

## Match-3 Có 3 Phần Trong 1 Level Fixed-Time

Khi cấu trúc level Match-3, designer chia board thành 3 phần (Vũ:

1. **Goal** (tượng gấu, vật cần thu) — fixed, hiển thị.
2. **Pattern combo prepared** — designer xếp sẵn 2 bomb + 1 rocket *"nhìn phát là thấy combo"*. Đây là quà cho user nhìn ra.
3. **Random fill (ball nut)** — phần còn lại random. Đây là chỗ áp tắc ẩn để control khó.

Khi user fail 4 ván liên tiếp, designer có thể bias phần random fill để cho thêm rocket → user qua mà không cảm thấy bị nới luật.

## Liên Hệ Wiki

5 levers cùng với [[hard-level-design]] (replayability, heartbeat, perceived difficulty) tạo nên đầy đủ toolkit thiết kế khó Match-3. [[chip-spawn-algorithm]] là deep-dive về lever 5. [[hidden-variable-difficulty]] giải thích cách dùng lever 5 để adapt khó sau IAP. [[match3-player-archetypes]] giải thích vì sao cùng 1 board, 3 nhóm user khác nhau pick combo khác nhau — designer dùng bài trí (lever 3) để nudge.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Solution Tạo Độ Khó Level — 5 Yếu Tố Cốt Lõi", "Thuật Toán Spawn Chip"
- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "Match-3 — 3 Phần Trong 1 Level Fixed-Time"
