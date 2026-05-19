---
title: "Level Content vs Level Data — Hai Trục Thiết Kế Level"
source: "[[raw/videos/negaxy-iec-gd-doc-02-level-design]]"
date_added: 2026-05-15
tags: [concept, level-design, content, data]
aliases: [level content vs data, hai trục thiết kế level]
status: draft
related:
  - "[[level-data-vs-handcrafted]]"
  - "[[match3-difficulty-levers]]"
  - "[[file-y-do-design-intent]]"
  - "[[new-mechanic-introduction]]"
summary: "Hai trục thiết kế level cần tách bạch: Level Content (thêm element mới, không cần skill) và Level Data (tăng/giảm số mu, scale up độ khó). Mix cả 2 trong 1 level → khó control khi cần fix"
---

## Định Nghĩa

Vũ phân biệt **2 trục thiết kế level**:

- **Level Content** — thêm element mới, đa dạng câu đố, tạo feel mới mẻ. Không yêu cầu user tăng skill, chỉ là thử nghiệm cảm xúc.
- **Level Data** — tăng/giảm số mu (moves), scale up độ khó qua các biến quantitative. Yêu cầu user tăng skill hoặc dùng booster.

Một level Match-3 có thể chỉ thay đổi 1 trục, hoặc mix cả 2.

## Ví Dụ Cụ Thể

| Cách Triển Khai | Trục | Output User Trải Nghiệm |
|------------------|------|--------------------------|
| Thêm 1 blocker mới (ice cream cone) | Content | "Mới quá!" — học cách phá |
| Giảm số mu từ 25 xuống 20 | Data | "Khó quá!" — phải tối ưu nước đi |
| Đổi goal: thu 2 → 3 công chúa | Content + Data | "Vừa nhiều mới hơn vừa khó hơn" |
| Đổi tỷ lệ chip drop 5 màu | Data (ẩn) | "Sao không có match nào hay vậy" |

## Mix Khó Control

Khi mix cả 2 trục trong cùng 1 level, designer mất khả năng diagnose khi player bị stuck. Vũ minh họa qua case con "Vulnerability" của Giang:

> *"Không biết thời điểm này nên thêm content mới vào, hay là tăng độ khó với content hiện có. Cùng lượng content giải cứu 2 công chúa thì giảm số mu để khó hơn, hay tăng từ 2 lên 3 công chúa?"*

Nếu chỉ một level fail rate cao, không biết nguyên nhân là content mới (user chưa quen) hay data (số mu quá ít). Phải A/B 2 bản → tốn thời gian.

## Quy Tắc

1. **1 level fix 1-2 tiêu chí**, không nhồi nhiều cùng lúc. Lúc fix sẽ biết phải chỉnh biến nào.
2. **Content roll out có timing**, không spam. Xem [[new-mechanic-introduction]] (Lion Studios) cho schedule introduce mechanic.
3. **Data scale theo curve đã định trước** trong [[file-y-do-design-intent]] — không reactive.

## Interest Curve Bổ Sung

Designer có thể đồng thời tăng difficulty + tăng hứng thú tại các điểm cố định (level 10, 20...). Vũ ví dụ: *"Đến level đấy bình thường chỉ có 3 màu — nhưng đến đấy mình muốn tăng độ khó vừa muốn tăng sự hấp dẫn nữa, thì thêm 1 màu nữa, đạt được cả 2 tiêu chí."*

Đây là exception có chủ đích — designer chấp nhận mix tại điểm milestone (khoảng level 10, 20) để gây ấn tượng, biết trước rằng fail rate có thể spike. Còn các level thường thì giữ 1 trục.

## Liên Hệ Wiki

[[level-data-vs-handcrafted]] (comparison) là phân loại chi tiết của Level Data — Match-3 dùng số trên Excel/Grid, Pull-the-Pin dùng đặt object trong Unity. [[match3-difficulty-levers]] cho 5 levers Data chính của Match-3. [[file-y-do-design-intent]] là tài liệu chốt designer chọn 1 biến đầu ra. [[new-mechanic-introduction]] (từ Lion Studios) cho schedule introduce Content theo D0/D1/D2.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Level Content vs Level Data"
- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "Quy Đổi Biến Sang Một Difficulty Score", "Interest Curve Bổ Sung"
