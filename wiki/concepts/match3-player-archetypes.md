---
title: "Match-3 Player Archetypes — 3 Nhóm User"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [concept, level-design, match-3, user-segmentation, game-theory]
aliases: [3 nhóm user Match-3, First-Look user, Logic user, Scattered user]
status: draft
related:
  - "[[match3-difficulty-levers]]"
  - "[[user-segmentation-3-axes]]"
  - "[[pattern-habit-break]]"
  - "[[hidden-variable-difficulty]]"
summary: "3 archetype user khi đứng trước Match-3 board có 2 combo: First-Look (chọn combo to nhất), Logic (tính cascade), Scattered (đi không theo logic — win rate thấp nhất). Designer dùng bài trí để nudge user về combo mình muốn"
---

## Định Nghĩa

Vũ vẽ 1 board Match-3 có 2 combo (Combo 1 dọc cascade cao; Combo 2 ngang to hơn nhìn) và hỏi học viên: "Em chọn nước nào trước?". Nhận được 4 cách lý giải khác nhau → phân thành 3 archetype.

> *"Các con game thì người chơi là những cỗ máy có cách tính toán khác nhau, nhưng tựu trung có một số nhóm. Khi mình bắt được action của người ta, mình hãy dùng thói quen đi của người ta để lấy cái thắng."*

## 3 Archetype

### First-Look User

*"To lạ và nhìn thấy cái đùi gà to thì ăn trước, không cần phải gì cả."*

Hành vi: chọn combo to nhất hoặc rõ nhất trước, không tính cascade. Logic kiểu *"2 → 1 nếu 2 không liên quan tới 1"*. Đây là nhóm impulse-driven, dựa vào visual saliency.

### Logic User

Hành vi: tính cascade, đi từ combo 1 → combo 2 để tối ưu chain. Đo lường khả năng chain reaction trước khi click. Có analysis ngắn (1-2 giây) trước mỗi nước đi.

### Scattered User ("Mắc Kém")

*"Cái nhóm này gần như là cái nhóm có tỷ lệ win thấp nhất, thấp tịch luôn."*

Hành vi: đi chỗ quái nào không theo logic, tìm combo 3 ở chỗ khác hẳn. Có thể do thiếu kinh nghiệm, mất tập trung, hoặc đang chơi nhanh không suy nghĩ.

## Design Intent — Nudge User

Khi designer muốn ép 75-80% user pick một combo cụ thể (vd combo 2 thay vì combo 1), kỹ thuật là **modify visual saliency**:

> *"Anh kéo cái 2 này dọc ra một cái — nó vừa to, nó vừa dài, nó vừa sâu ở phía dưới."*

Sau khi modify:
- First-Look user converge sang combo 2 (vì to hơn).
- Logic user cũng có thể converge (vì cascade từ dưới lên dài hơn).
- Scattered user vẫn random, nhưng tỷ lệ pick combo 2 tăng theo prominence.

Tỷ lệ user pick combo mong muốn từ ~33% (random 3 cách) lên ~75-80% (nudged).

## Quy Tắc Dùng Archetype

Mỗi level Match-3 có 1 *intended path* mà designer thiết kế. Để intended path win:
- **Bài trí** (lever 3 trong [[match3-difficulty-levers]]) phải nudge first-look + logic về cùng path.
- **Random fill** (ball nut) phải back up path bằng favorable drops.
- **Adaptive logic** sau fail phải tăng favorability nếu user tiếp tục đi sai path.

Scattered user là **outlier** không phục được — chấp nhận họ có tỷ lệ win thấp hơn. Trong [[user-segmentation-3-axes]], Scattered tương ứng nhóm thấp tay nhẹ skill (S1T thấp) — bù bằng booster/help.

## Bot Test Archetype

Vũ kể: làm Match-3 ngày xưa từng viết bot test level — bot không biết design — đi nước theo % để ra kết quả phân nhóm user. *"Cùng với một logic test, kết quả khác nhau như thế nào."* Bot mô phỏng 3 archetype:
- Bot first-look: pick combo có visual area lớn nhất.
- Bot logic: pick combo có expected cascade cao nhất.
- Bot random: pick uniformly.

Win rate của 3 bot trên cùng 1 level cho biết level có "intended path" rõ chưa, hay đang random về kết quả.

## Liên Hệ Wiki

[[match3-difficulty-levers]] cho 5 levers thiết kế khó — archetype là khung user-side để hiểu hệ quả của mỗi lever. [[user-segmentation-3-axes]] là khung tổng quát hơn (3 trục: sở thích, tư chất, tài chính) — Match-3 archetype là chuyên đề về tư chất user trong cùng dòng casual puzzle. [[pattern-habit-break]] khai thác cả 3 archetype theo cách khác nhau — First-Look bị break nhanh nhất, Logic adapt nhanh hơn, Scattered không thay đổi. [[hidden-variable-difficulty]] dùng biến ẩn để balance giữa các archetype mà user không nhận ra.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "Game Theory Optimization — 3 Nhóm User Match-3", "Bài Toán Của Giang"
