---
title: "Lưới S × T — Map Genre Theo Archetype"
source: "[[raw/videos/negaxy-iec-gd-doc-08-phan-tap-user]]"
date_added: 2026-05-15
tags: [concept, user-segmentation, genre, archetype, mobile-games]
aliases: [lưới ST, S×T grid, S1T2, S2T2, S2T4, music game S1T2]
status: draft
related:
  - "[[user-segmentation-3-axes]]"
  - "[[mobile-vs-pc-console-skill]]"
  - "[[user-archetype-asset-vs-self-expression]]"
summary: "Lưới 2 chiều map genre game vào archetype user. S (sở thích trục dọc) × T (tư chất trục ngang). S1T2 = casual repeat. S2T2-T4 = challenge cao tay. Music game mix S1T2 + X1T2"
---

## Định Nghĩa

Vũ vẽ lưới 2 chiều để map genre vào user archetype trong Doc 8:

- **S (trục dọc)**: sở thích / skill type. S1 = nhẹ/lặp lại; S2 = challenge.
- **T (trục ngang)**: tư chất / kỹ năng. T1 (lóng ngóng) → T4 (siêu nhân).

Mỗi ô là một genre đặc thù. Khung này phục vụ designer: trước khi build game, xác định ô nào trên lưới → biết user là ai → biết IAP/UA strategy.

## Nhóm S1 — Sở Thích Nhẹ, Repeat

Game tham chiếu: Sudoku, Word, Word Cross, Sort, Match-3 lặp đi lặp lại.

Đặc trưng:
- Phổ user: từ trung lứa cho tới người già, kỹ năng tay yếu.
- Hành vi chơi: *"Từ level 10 tới level 20, từ level 30 có gì khác nhau không? Không khác nhau. Họ chỉ làm việc đấy theo thói quen theo phương thức thôi."*
- Vũ thừa nhận bản thân mình rơi vào nhóm này: *"Bây giờ mà chơi cái độ này xong rồi nó bảo anh ơi mình muốn giờ đêm đi bang chiến — anh đang làm việc khác rồi. Tha cho anh rồi và bắt đầu bị bỏ rồi đấy."*

### IAP Cho S1

- **Booster, Hint, Match Pad** — giải quyết vấn đề trong level.
- **Unlock màn chơi đặc biệt**.
- **Không** chi cho avatar/skin/đồ trang — *"Nó chơi cho riêng mình thôi nên là các cái thứ mà mua kiểu bán kiểu avatar nó tổng đồ trang thì khá là ít."*

Cảnh báo về tài chính: *"Cái đội này vấn đề là năng lực tài chính nó còn kém nữa. Nếu đẩy những thứ khó vào, nó không giải quyết được thì nó sẽ tắt, nó sẽ bỏ game."*

## Nhóm S2 — Challenge

Game tham chiếu: Chess, Tower Defense, Survival cao tay, dòng kỹ năng cao.

Đặc trưng:
- Phổ user trẻ, tính cạnh tranh cao, kỹ năng tốt.
- Mức chi tiêu khác — sẵn sàng chi giải quyết vấn đề "đáng".

S2T2-T4 là dòng kỹ năng cao như MOBA, Action RPG, Battle Royale. Xem [[mobile-vs-pc-console-skill]] cho constraint của mobile platform với S2 cao.

## Music Game — Mix Hai Trục

Vũ phân tích music game (Piano Time, Amanote) là một case **mix S1T2 + X1T2**:

- Core gameplay: S2T2 (đập theo beat — challenge).
- Mong muốn user: nghe trải nghiệm nhiều bài hát (X1T2).
- *"Có những thứ mà nó bị mix giữa 2 cái với nhau."*

Sudoku ngược lại: chỉ cần đổi puzzle, *"cái màn hình bên ngoài nó nào kệ"* — pure S1T-axis.

User Music game không trả tiền cho replay — *"Mình không bao giờ lặp tiền. Mình chơi chỉ đến 20% bài hát là hết. Mình đâu có thích nhiều bài đâu, mình chỉ thích tốt từng bài."* Tiền IAP chủ yếu là **gói nhạc + level mới**.

Lý do vì sao Music game được Vũ map vào S1T2 thay vì S2T2: nếu làm fast như Guitar Hero (S2T2) thì *"sẽ rất khó chơi mà chơi đại chúng ấy."* Đại chúng = giảm kỹ năng = S1T2.

## Ký Hiệu Phụ Vũ Dùng

Trong buổi, Vũ dùng một số ký hiệu chưa giải nghĩa rõ:

- **F1A2** — ghép cho dòng kỹ năng cao (Stickman, Fighting).
- **X1T2** — ghép với music game (content layer).

Đây là extension của lưới S×T sang chiều thứ 3 — có thể là loại tài sản (asset type) hoặc dòng content. Vũ không hệ thống hóa hoàn chỉnh trong buổi cuối; đề tài này có thể được phát triển sâu hơn trong khóa nâng cao tiếp theo.

## Ý Nghĩa Thiết Kế

Lưới S × T trả lời câu hỏi "user của tôi là ai?":

1. Designer chọn 1 ô (vd S2T2) trước khi thiết kế.
2. IAP/UA strategy align với ô đó.
3. Khi feature creep (đề xuất thêm mode mới), check xem có kéo game sang ô khác không. Nếu có, cân nhắc tách thành 2 sản phẩm (xem [[replay-rate-distribution]] — distribution phân cực → 2 sản phẩm).

## Liên Hệ Wiki

[[user-segmentation-3-axes]] là khung lý thuyết 3 trục — lưới S × T là cách visualize. [[mobile-vs-pc-console-skill]] cho constraint mobile với S2T cao. [[user-archetype-asset-vs-self-expression]] cho 2 nhóm S chính. [[replay-rate-distribution]] cho cảnh báo khi game mix 2 ô trên lưới.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-08-phan-tap-user.md` § "Lưới Phân Loại S × T", "Music Game — Mix Hai Trục"
