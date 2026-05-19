---
title: "Pattern Habit Break — Tạo Thói Quen Rồi Phá Vỡ"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [concept, level-design, difficulty, habit, ux]
aliases: [phá thói quen người chơi, 3 level tạo 1 level phá, habit break]
status: draft
related:
  - "[[match3-difficulty-levers]]"
  - "[[hidden-variable-difficulty]]"
  - "[[file-y-do-design-intent]]"
  - "[[match3-player-archetypes]]"
summary: "Kỹ thuật tạo độ khó bằng cách build thói quen người chơi trong 3 level rồi phá ở level 4. User chết 1 lần → đạt tỷ lệ replay đã set trong file ý đồ"
---

## Định Nghĩa

Pattern habit break là kỹ thuật tạo độ khó level không thông qua tăng resource/obstacle, mà thông qua **build thói quen trong 3 level → phá ở level 4**. Vũ định nghĩa qua analogy bình nước:

> *"Ngày đầu tiên bạn đến bạn nhìn, bạn cầm nó lên. Ngày thứ 2 bạn đi đến gần lại nó chủ động lấy. Đến ngày thứ 3 bạn có thể vừa bấm điện thoại vừa đi qua vẫn lấy được. Ngày thứ 4 có ông nào đấy rời cái bình nước từ bên trái sang bên phải — các bạn đi qua, cua tay theo thói quen, và không tìm thấy bình nước. Bạn đâu có phải ngó nghiêng đi tìm bình nước này, đi bộ sang một hai bước cầm nó lên — như vậy là các bạn đã phải tăng phí mu cho người chơi rồi."*

Quy tắc Vũ chốt: *"Các bạn làm thế giới này để 3 level chỉ chuẩn bị cho một lần user chết."*

## 3 Case Áp Dụng

### Case 1 — Lưỡi Cưa (Saw Blade)

3 bài đầu: lưỡi cưa chỉ chạy thẳng A → B → A. *"Bài 1 nó giòn giả, bài 2 nó quen, và bài thứ 3 là không cần ngắm xem nó quỹ đạo nó dễ chạy như thế nào — nó nhảy phọt phát qua luôn, không cần để nghĩ."*

Bài 4 phá thói quen — 2 cách:
- Thêm vật cản mới trên đường.
- Đổi logic jump-point: thay vì A → B → A, đổi thành A → B → C → B → A. User đã quen pattern cũ sẽ nhảy sai vị trí.

### Case 2 — Tower Defense 2 Cọp

4 level đầu thả quân ở 1 cọp. *"User đã xây dựng hết chú bên này thì bọn nó đi vào cái chỗ đường chống — như thế nó bị thua và nó phải chơi lại."* Level 5 spawn quân bên cọp đối diện.

Đây là pattern Vũ đã giới thiệu sớm từ Doc 1 dưới tên "rainbow design" — chặn user bằng nhiều hướng khác nhau (entrance, hệ quân, data ẩn) chứ không chỉ tăng chỉ số tuyến tính.

### Case 3 — Bắn Máy Bay Theo Quỹ Đạo

*"Trước khi nhìn thấy sự việc, user sẽ action. Lần 1 nó cứ bay ngang, lần 2 bay ngang, lần 3 bay ngang — dù trong đám có 1 con cáo thẳng dưới mặt mình, thì nó là một cái mồng, và có thể là to luôn."*

User đã quen pattern bay ngang → ngầm trust rằng pattern này không đổi. Level phá: đột nhiên có con bay dọc/khác hướng. User shot lệch.

## Cơ Chế Tâm Lý

Pattern habit break khai thác 2 hiện tượng:

1. **Automation** — sau 3 lần lặp, user chuyển hành vi từ chú ý sang tự động. Phản ứng nhanh hơn nhưng kém adapt.
2. **Loss aversion + foreseeable failure** — khi user chết vì pattern break, cảm xúc "lừa tôi rồi" trigger replay (muốn báo thù) thay vì bỏ. Khác với chết vì "khó", chết vì "lừa" gây tò mò.

Quy tắc: *"3 level tạo thói quen → 1 level phá → user chết 1 lần → đạt tỷ lệ replay đã đặt trong [[file-y-do-design-intent]]"*. Designer kiểm soát replay rate qua cường độ phá.

## Khi Nào KHÔNG Dùng

- **Game ASMR / no-fail** — không có concept "chết". Pattern habit break không áp.
- **Tutorial / early FTUE** — user chưa build trust với game, một lần "lừa" có thể làm user bỏ ngay. Đợi đến sau D1 mới dùng.
- **Game competitive PvP** — phá thói quen của bot không có ý nghĩa, vì opponent là user khác cũng phá.

## Liên Hệ Wiki

[[match3-difficulty-levers]] cho 5 levers cụ thể, trong đó pattern habit break dùng lever 3 (bài trí ban đầu) và lever 5 (tắc ẩn). [[hidden-variable-difficulty]] là technique paired — tăng khó qua biến ẩn cũng là một dạng phá expectation. [[file-y-do-design-intent]] là tài liệu chốt designer set tỷ lệ replay target — pattern habit break là technique để đạt target đó. [[match3-player-archetypes]] giải thích vì sao 3 nhóm user phản ứng khác nhau với pattern break: First-Look bị lừa nhanh nhất, Logic adaptive nhanh hơn.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "Pattern Habit — Tạo Thói Quen Rồi Phá Vỡ"
