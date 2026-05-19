---
title: "Mobile vs PC/Console — Hành Vi Kỹ Năng"
source: "[[raw/videos/negaxy-iec-gd-doc-08-phan-tap-user]]"
date_added: 2026-05-15
tags: [comparison, mobile, pc, console, platform, ux]
aliases: [mobile vs PC, dung sai input, mobile simplified]
status: draft
related:
  - "[[s-t-genre-grid]]"
  - "[[thumb-zone-design]]"
summary: "Mobile có phím ít, dung sai cao, bấm trượt thường xuyên. Phải tối đa hóa dung sai để user 'làm việc chưa đúng cũng phải cho người ta làm đủ'. PC/Console kỹ năng combo cao hơn"
---

## Bối Cảnh

Vũ note constraint của thiết bị di động ảnh hưởng đến archetype trong Doc 8. Mobile không thể đơn giản chuyển port game PC/Console — phải simplify input và tối ưu dung sai.

> *"Hành vi của người dùng trên điện thoại nó sẽ khác với hành vi mọi người chơi ở trên PC và Console."*

## Bảng So Sánh

| Tiêu Chí | Mobile | PC/Console |
|----------|--------|-------------|
| Input | Touch / swipe / virtual button | Bàn phím + chuột / gamepad |
| Phím | Ít (4-8 virtual button thường) | Nhiều (60+ phím + L2/R2/triggers) |
| Dung sai input | Cao — vuốt trượt, bấm lệch | Thấp — precise pointer/key |
| Combo skill | Đơn giản hóa — vuốt là đủ | Phức tạp — L2+R2+combo |
| Game S2T cao | Khó — phải reduce skill ceiling | Tự nhiên — APM cao OK |
| Genre suitable | Casual, RPG asset, Match-3 | MOBA, fighting, FPS, RTS |
| Session length | Ngắn (5-15 phút phổ biến) | Dài (1-3 tiếng phổ biến) |

## Phân Tích

### Mobile — Tối Đa Dung Sai

> *"Tất cả các game trên điện thoại này đều phải tìm cách... phải tối đa hóa dung sai — có nghĩa là người ta làm việc chưa đúng cũng phải cho người ta làm đủ."*

Designer mobile phải accept user *"làm chưa đúng"* và vẫn cho game chạy được. Ví dụ:
- Bắn súng: vuốt rộng quanh enemy → game auto-aim. User không cần precise tap.
- Đá bóng: vuốt theo direction chung → bóng đá theo trajectory cơ bản. Không cần kéo chính xác.

Combat trên mobile thường:
- Bỏ combo L2/R2 → chỉ còn vuốt + tap.
- Auto-attack default, skill là tap manual.
- Movement bằng joystick lớn (vùng vuốt rộng).

### Genre Cao Tay Cho Mobile

Ngoại trừ dòng đánh vào tập khách hàng kỹ năng cao (S2T3, S2T4 cho dòng "F1A2"), đa số game mobile **không gặp vấn đề về độ chính xác input**. Casual / Asset game không cần precision → mobile native suitable.

Game S2T cao trên mobile (case MOBA Hàn Quốc Vũ kể):
- Skill phân loại theo APM (Action Per Minute).
- Skill APM thấp: bắn đường thẳng, vòng cung quạt. Bắn thoải mái, trúng diện rộng không cần thăm binh.
- Skill APM cao — Chain Climbing: nhảy chain từ A → B → C → D với khoảng cách 40-50px trên màn full HD. Mobile rất khó.
- Skill AOE delay: bấm vào skill, giữ nút, hold lên trên, kéo skill ra các vị trí xung quanh.

Vũ note: *"Cân bằng khó là một phần, mà nó tưởng tượng là cái biên độ lệch nhau giữa kỹ năng của những người chơi nó cao kinh khủng luôn."*

### PC/Console — Combo Phức Tạp OK

PC/Console cho phép:
- Bàn phím 60+ phím + chuột tracking precise.
- Gamepad L2/R2/L1/R1 + bumpers cho combo system phức tạp.
- Game session dài → user invest skill learning curve.

Genre kết quả: MOBA (League of Legends desktop), fighting (Street Fighter), FPS (Counter-Strike), RTS (Starcraft).

Đem các genre này sang mobile cần simplify đáng kể. Wild Rift (LoL mobile) vs LoL desktop: skillset và pace khác hẳn.

## Hệ Quả Thiết Kế

Designer chọn platform phải pick:
- **Mobile-first**: thiết kế với dung sai cao, skill ceiling vừa phải, session ngắn.
- **PC/Console-first**: tận dụng combo, precision, session dài.
- **Cross-platform**: tách 2 build hoặc accept compromise — mobile build thường feel "đơn giản hơn" với fan của PC version.

Dead Cell và các con kỹ năng cao offline được Vũ map vào S2T2 hoặc S2T4 — phù hợp PC, khó port mobile đầy đủ.

## Liên Hệ Với Lưới S × T

Mobile constraint giới hạn ô (S2, T4) — *"siêu nhân"* không phải target chính. PC/Console mở rộng pool xuống tận T4 thoải mái.

[[s-t-genre-grid]]: Music game được Vũ map vào **S1T2** (không phải S2T2 như Guitar Hero) vì *"sẽ rất khó chơi mà chơi đại chúng ấy"* — đại chúng = giảm kỹ năng → mobile feasible.

## Kết Luận

Mobile và PC/Console không phải 2 platform cùng nội dung khác form factor — chúng đòi hỏi **thiết kế khác từ gốc**. Mobile native cần tối đa dung sai, simplify skill. PC native cho phép skill ceiling cao, session dài.

Designer port game cross-platform phải accept compromise hoặc tách build — không có *"one build for all"* cho game competitive S2T cao.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-08-phan-tap-user.md` § "Mobile vs PC/Console — Khác Biệt Kỹ Năng", "Case Study MOBA Hàn Quốc — APM Và Tập T2-T4"
