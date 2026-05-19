---
title: "Hidden Variable Difficulty — Điều Chỉnh Khó Sau IAP"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [concept, level-design, difficulty, iap, adaptive]
aliases: [biến ẩn điều chỉnh khó, hidden variable, distract variable]
status: draft
related:
  - "[[match3-difficulty-levers]]"
  - "[[chip-spawn-algorithm]]"
  - "[[pattern-habit-break]]"
  - "[[iap-pricing-user-value]]"
summary: "Sau khi user IAP làm level dễ đi, designer cần tăng khó lại nhưng user không nhận ra. 3 loại biến: trên mặt (rủi ro), biến ẩn (khuyến cáo: freestyle ratio, drop rate, mix density), distract (đổi tông màu, palette)"
---

## Định Nghĩa

Bài toán Vũ giới thiệu: user IAP → level dễ đi → user hardcore mất challenge → bỏ. Làm sao tăng khó lại sau IAP **mà user không nhận ra**? Vũ phân thành 3 loại biến điều chỉnh.

## 3 Loại Biến

### Loại 1 — Biến Trên Mặt (Không Khuyến Cáo)

Biến hiển thị trực tiếp: số mu hiển thị, thời gian limit. Nếu giảm xuống sau IAP, user sẽ phản ánh *"tại sao có 20 mu tao có 18 mu?"*. Risky.

OK với game không có video quay leo top (user không so sánh tay-trong-tay với streamer). Vẫn risky vì user có thể chụp screenshot để complain.

### Loại 2 — Biến Ẩn (Khuyến Cáo)

Biến không hiển thị trực tiếp trên UI:

- **Freestyle ratio** — phần random fill (Match-3 ball nut) → giảm tỷ lệ favorable. User không biết tỷ lệ drop, chỉ thấy "không có match hay".
- **Drop rate** — tỷ lệ hạt khác nhau (5 màu đều 20% là khó nhất; lệch là dễ hơn). Sau IAP, designer điều chỉnh về 20% đều.
- **Mix density** — pattern phân tán màu/chip xen kẽ nhau như thế nào. Cluster (A,A,A,B,B) thì dễ; intersperse (A,B,A,B,A) thì khó.

3 biến này là layer ẩn sâu trong [[chip-spawn-algorithm]] — user chơi 10 ván vẫn không nhận ra. Đây là công cụ phổ biến nhất trong Match-3 commercial.

### Loại 3 — Distract Variable (Cẩn Trọng)

Không phải tăng khó thật mà tăng **cognitive load**:

- **Đổi tông màu** — level 6 day → level 7 night (hoặc đảo). Effect dễ/khó nhìn hơn.
- **Đổi color palette** — từ basic (xanh đỏ tím vàng) → same-tone (các màu sang sang nhau, khó phân biệt). User phải dồn focus → perceived difficulty tăng dù level data không đổi.

Quote Vũ:

> *"Lúc đấy cái độ khó của level chơi nó không được quyết định bởi level design bằng data, mà nó tăng độ khó lên bởi vì độ phân biệt về màu sắc của mọi người. Cái này là hoàn toàn cá nhân — có người sẽ thấy khó lên, có người vẫn cảm thấy nó xịn hơi khó lắm chút thôi."*

Distract phụ thuộc từng user — không control được như biến ẩn. Cảnh báo: nếu lạm dụng (tất cả level đều dùng distract), user mệt mỏi visual → bỏ.

## Game Reveal-Map vs Hidden-Map

Khả năng dùng hidden variable phụ thuộc thông tin user nhìn thấy:

- **Platformer / hidden map** (user không nhìn thấy toàn map) → nhồi khó vào freestyle section. User không có baseline để so sánh.
- **Match-3 / fully revealed board** (state show hết) → khó hơn vì user thấy hết → ưu tiên biến ẩn / distract.

Hệ quả: game càng cho user nhiều thông tin, càng khó hidden variable. Phải bù bằng distract hoặc accept risk khi dùng biến trên mặt.

## Liên Hệ Với IAP Strategy

Hidden variable là công cụ giữ challenge cho user paying sau khi họ mua boost/power. Không có nó, IAP biến game thành too easy → user paying bỏ trước user non-paying. Đây là instance cụ thể của [[imba-balance-meta]] — phải re-balance power vs difficulty sau gói IAP.

Pattern Match-3 commercial:
1. User mua moves pack ($1.99 → +5 moves).
2. Server-side: giảm freestyle ratio favorable 5-10%.
3. User vẫn thắng vì +5 moves, nhưng vẫn cảm thấy *"hơi khó"* → continue dùng moves.

## Liên Hệ Wiki

[[match3-difficulty-levers]] — hidden variable là lever 5 (tắc ẩn). [[chip-spawn-algorithm]] là implementation chi tiết. [[pattern-habit-break]] là technique paired — tăng khó qua phá expectation, không qua tăng số. [[iap-pricing-user-value]] cho khung pricing — hidden variable giữ challenge để IAP tiếp theo có lý do. [[imba-balance-meta]] là context lớn — không có hidden variable, IAP tạo imba bất kiểm soát.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "Hidden Variables — Điều Chỉnh Khó Sau IAP"
