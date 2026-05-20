---
title: "Hành Vi vs Lời Nói — Design Cho Cái User Làm, Không Phải Cái User Nói"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, user-research, mindset]
aliases: [hành vi vs lời nói, behavior vs stated, design cho hành vi, user nói khác làm]
status: draft
related:
  - "[[ux-yeu-ich-definition]]"
  - "[[playtest-protocol-designer]]"
  - "[[user-test-no-explanation]]"
summary: "User nói A, làm B — designer phải design cho B. Vũ test 3 học viên về quán ăn quen: tiêu chí khai báo (ngon/rẻ/sạch) khác tiêu chí thật (giá ceiling 50k, gu hương vị quê, tiện + được nhớ mặt). Cảm xúc ≠ sự thật — design cho cảm xúc."
---

## Định Nghĩa

Hành vi (behavior) là cái user **thực sự làm**. Lời nói (stated preference) là cái user **báo cáo họ thích**. Hai thứ khác nhau — designer phải bám hành vi, không bám lời nói.

> *"Đấy. Thưa các bạn đây là hành vi đấy. Không phải những cái gì các bạn nói ra là những thứ các bạn nghĩ. Cái thứ mà các bạn thực tế hành động ấy mới là cái thứ các bạn nghĩ."*

## Case Study — 3 Học Viên, 3 Tiêu Chí Quán Ăn Quen

Vũ test 3 học viên cùng câu hỏi *"Tiêu chí chọn quán ăn quen của em?"* → 3 kết quả khác nhau.

### Tài — Cơm Gà Gần Nhà

- **Khai báo**: ngon → rẻ → sạch (đặt sạch lên hàng đầu).
- **Test push**: *"Quán cơm sạch 100k/đĩa vs quán bình thường 50k/đĩa. Chọn quán nào?"* → chọn quán 50k.
- **Tiêu chí thật**: ceiling giá 50k. Sạch CHỈ KHI nằm trong giới hạn giá.

Lời nói: "sạch quan trọng." Hành vi: giá quan trọng hơn sạch trong điều kiện kinh tế cá nhân của Tài.

### Đồng — Mì Quảng Ở Đông Đa

- **Khai báo**: ngon + giá phải chăng.
- **Hành vi**: đi 10 km từ Mễ Trì → Đông Đa 2 lần/tháng để ăn quán mì Quảng.
- **Tiêu chí thật (sau khi Vũ moi ra)**:
  - Ngon theo gu Quảng Nam (cay/đậm) — *"có thể với người khác là không ngon."*
  - Chủ quán nói tiếng Quảng Nam → có tương tác gần gũi.
  - **Hành trình đi dạo phố** là 1 phần experience (*"em thích cả cái hành trình đi đến đấy chứ không phải thích mỗi cái chỗ đấy không"*).

Lời nói: "ngon, hợp lý." Hành vi: gu hương vị quê + emotional attachment + ritual đi dạo.

### Vũ — Bún Riêu Đội Cấn

- **Khai báo**: không (anh kể như case study).
- **Hành vi**: 2-3 bát/tuần ở 1 quán không quá ngon, không gần đường lớn, giá không rẻ.
- **Tiêu chí thật**: chủ quán nhớ gu (*"bún riêu thịt bò ít bún nhiều mắm tôm, một cốc trà đá"*), xuất ngay không phải gọi món, có hôm quên trả tiền cũng không vấn đề.

Lời nói có thể là "ngon, rẻ, gần." Hành vi cho thấy: **tiện + được nhớ mặt** > ngon + rẻ.

## Insight Cho Designer

> *"Vậy thì mình đừng đánh đồng vào một cái bất kỳ một cái gì cả... Nó có thể đến từ việc ăn ngon, gần giống với cái gu của bạn ấy ở quê bạn ấy ở Quảng Nam. Nó có thể là cái sự tiện lợn đối với anh. Nó có thể là cái thứ mà bạn này thích là cái món phụ, là cái mức tầm tiền giá của bạn ấy ok."*

3 người = 3 tiêu chí khác nhau. Không có "tiêu chí tốt universal." Designer phải **quan sát hành vi** từng tập user thay vì hỏi (survey).

## Cảm Xúc vs Sự Thật

Hành vi-bị-điều-khiển-bởi-cảm-xúc:
- User cảm thấy 100 gold > 1 gold dù tỷ lệ giống (xem [[value-perception-techniques]]).
- User cảm thấy giá nhà tăng dù purchasing-power-parity không thay đổi.
- User cảm thấy 33% skill "đánh được" dù 7% có thể proc nhanh hơn statistically.

> *"Cảm xúc và sự thật đôi lúc nó giống nhau, đôi lúc nó khác nhau. Vì thế cho nên có rất nhiều bạn ấy, khi mà đưa ra các con số ấy là mình thấy nó không phù hợp với cảm xúc của dân dân."*

Designer design cho **cảm xúc** (perceived value), không design cho **sự thật** (intrinsic value). Game không tối ưu math — game tối ưu **feel**.

## Phương Pháp Khai Thác

Lời nói rẻ — survey form, in-game poll. Không tin cậy.

Hành vi đắt nhưng đáng tin:
- **Analytics events** — funnel, session length, retention curve.
- **Playtest observation** — xem user chơi (không hỏi).
- **A/B test** — 2 variants, so KPI thật.
- **Push test** — hỏi đối lập (Vũ test Tài bằng câu *"sạch 100k vs bình thường 50k"*) để force lộ tiêu chí thật.

## Anti-Pattern: Hỏi Survey Rồi Build Theo Lời Nói

User nói "em muốn UI to + nhiều info" → designer build → user vẫn không tăng retention. Lý do: user nói cái "có vẻ đúng" (UI = dễ đọc), nhưng hành vi cho thấy user phớt UI và chỉ tap nút quen thuộc.

> *"Anh đang moi cái đấy của em ra để anh muốn xem cái hành vi của em trong việc lựa chọn là cái gì. Thì từ cái hành vi lựa chọn đấy, cái quán nào nó đạt được tất cả các tiêu chí của em, nó sẽ thành quán quen của em."*

Moi ra qua follow-up question. Push test khi user khai báo quá generic.

## Liên Hệ Wiki

[[ux-yeu-ich-definition]] cho khung UX dual-goal. [[user-test-no-explanation]] cho nguyên tắc khi test user không được giải thích — bảo vệ tính nguyên bản của hành vi. [[playtest-protocol-designer]] (skill) cho framework playtest. [[user-segmentation-3-axes]] phân tập theo trục — mỗi tập có hành vi đặc trưng.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Hành Vi vs Lời Nói — Câu Chuyện Quán Ăn"
