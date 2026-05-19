---
title: "Auto-Equip Design — 3 Loại Game"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [concept, ux, equipment, hero-management]
aliases: [auto-equip, tự động lắp đồ, fun role hero]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[rpg-unit-weakness-principle]]"
summary: "Auto-equip phù hợp game 1 hero (Loại 1) hoặc 10+ hero (Loại 3) — không phù hợp game 1-5 hero không có fun role (Loại 2b) vì hero tranh đồ lẫn nhau"
---

## Định Nghĩa

Auto-equip là pattern UX: click 1 hero → game tự động lắp toàn bộ trang bị tốt nhất, user không phải đi qua flow chọn từng slot. Tài (học viên) đề xuất làm option 3 cho case Equipment trong Doc 7 — giảm xuống còn 2 bước (chọn con + đeo).

Vũ phân tích auto-equip phù hợp hay không tùy số hero trong game.

## Cơ Chế 2 Biến Thể

Vũ "bẻ" để cả lớp thấy điểm yếu:

### Biến Thể A — "Tốt Nhất Cho Con Đang Bấm"

- Auto-equip lấy đồ tốt nhất ráp vào con đang bấm.
- Mỗi lần bấm con khác, bộ đồ "xịn số 1" lại bay sang con đó.
- Cuối cùng chỉ có 1 con luôn được bộ xịn nhất.
- Hậu quả: bộ đồ bị bounce qua lại, không ổn định.

### Biến Thể B — "Tốt Nhất Đang Chưa Mặc"

- Auto-equip *"lấy đồ tốt nhất đang chưa mặc cho ai cả"*.
- Con thứ nhất bộ xịn 1, con thứ 2 bộ xịn 2 — vẫn được.
- Nhưng khi user muốn *"chia niệm sức mạnh"* (con này áo xịn, con này kiếm xịn) thì thay rất khó.

Cả 2 biến thể đều có trade-off. Phải chọn theo context game.

## 3 Loại Game Theo Số Hero

Đức phản biện: *"Em chẳng thấy thốn, em thấy rất tiện. Khi em có một cái bun đến mười mấy con tướng, em không thể nào ngồi mặc từng quát một."* Ví dụ **One Punch Man The Strongest của VNG** — game thẻ bài, mỗi con 6 trang bị, auto-equip cứ lấy từ trang bị mạnh nhất ra mặc vào.

Vũ chốt 3 loại game:

| Loại | Số Hero | Auto-Equip Phù Hợp? |
|------|---------|---------------------|
| **Loại 1** | 1 con (Nyachero, Survival) | Rất tốt. *"Nhà có 1 đứa con, tất cả tinh túy nhất là dành cho nó."* |
| **Loại 2a** | 1-5 con + có fun role (kiếm/cung/giáo cố định) | OK. Mỗi con dùng class riêng, không tranh nhau. |
| **Loại 2b** | 1-5 con + KHÔNG fun role (mặc lẫn — game của Hiệp) | Không OK. Bắt đầu tranh. Phải phân bổ tay. |
| **Loại 3** | Mười mấy con (Lít-tờ-bíc GD) | Bắt buộc auto. *"Thời gian chơi gameplay không còn — chỉ mặc quần áo, nhặt đồ thì hết ngày."* |

Quy tắc Vũ chốt:

> *"Cái gì ít thì bao giờ cũng chất, cái gì nhiều thì sẽ bị giảm đi. Nhà bố mẹ thu nhập 1 tháng 50 triệu mà có 1 thằng con thì may ra được mặc giày Adidas, mặc quần Gucci. Chứ mà để 10 đứa thì mặc kiểu gì luôn."*

## Fun Role Là Gì

Fun role = vai trò class **cố định** cho mỗi hero (kiếm/cung/giáo). Khi hero có fun role, mỗi class có pool đồ riêng → không tranh đồ với class khác. Pool đồ phân tách: kiếm chỉ mặc đồ kiếm, không chia với cung.

Game loại 2b (1-5 hero không fun role) là edge case khó nhất:
- Số hero ít → user có thể manage tay.
- Nhưng không có class separation → đồ chia chung → auto-equip làm rối.

Solution Vũ đề xuất: pattern hỗn hợp — nhiều game cho cả 2 (menu thay từng slot + auto). *"Bởi vì không biết người ta thích cái gì."*

## Liên Hệ Với 3 Tiêu Chí UX

Auto-equip là case study cụ thể của [[ux-3-criteria]] tiêu chí 1 (số bước thao tác). Auto-equip 2 bước thắng option 1 (6 bước) và option 2 (3 bước) về số bước. **Nhưng** số bước ít không phải tiêu chí duy nhất — auto-equip vi phạm tiêu chí 2 (thông tin) cho game loại 2b: user mất khả năng "chia niệm sức mạnh".

Quy tắc tổng quát: **chọn UX option phải đối chiếu cả 3 tiêu chí**, không tối ưu 1 cái rồi bỏ 2 cái còn lại.

## Liên Hệ Wiki

[[ux-3-criteria]] cho khung 3 tiêu chí. [[rpg-unit-weakness-principle]] giải thích vì sao game loại 2b phải có weakness — nếu unit không weakness thì auto-equip càng nguy hiểm hơn (1 unit ăn hết bộ đồ tốt nhất, các unit khác useless).

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Option 3 — Auto-Equip", "3 Loại Game Phân Theo Số Hero — Auto-Equip Phù Hợp Khi Nào"
