---
title: "Thumb Zone Design — Bố Cục Tầm Tay"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [concept, ux, ui, layout, mobile-games]
aliases: [thumb zone, bố cục tầm tay, phá UI]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[notification-management]]"
  - "[[dark-ux-techniques]]"
summary: "Thumb zone là vùng ngón cái user dễ với tới trên màn hình điện thoại. Nút quan trọng (đặc biệt IAP) phải nằm trong vùng này. Phá UI = cố tình thiết kế lệch grid để hút mắt"
---

## Định Nghĩa

Thumb zone là **vùng ngón tay user (đặc biệt ngón cái) dễ với tới** trên màn hình điện thoại khi cầm 1 tay. Nút quan trọng phải nằm trong vùng này, đặc biệt là IAP và CTA chính.

Vũ phản hồi layout home của Darwin (Đồng):
- 2 hàng button ở **trên cao** → người dùng phải vươn ngón tay lên.
- Phần dưới màn hình **rất trống**.
- *"Sao trả tiền quá khổ thế. Rơi điện thoại là nó bỏ game luôn đấy."*

Quy tắc: **kéo các nút quan trọng (đặc biệt là IAP) vào vị trí ngón tay người ta dễ bấm**.

## So Sánh Với Game Tham Chiếu

| Layout | Vùng Top (xa) | Vùng Bottom (thumb zone) |
|--------|---------------|---------------------------|
| Game gốc (tham chiếu) | Setting / Noti (ít quan trọng) | Nút trả tiền + Play |
| Darwin (Đồng) | Tất cả nút compress | Trống |

Darwin tham chiếu game gốc nhưng đảo ngược cấu trúc → fail UX. Game gốc đã design thumb zone đúng — Darwin copy visual nhưng không copy logic.

## Pattern Phân Tay

- **Tay phải**: đa số user → bố cục lệch phải. Đức (học viên có publisher background): tay trái rất hiếm trong số liệu.
- **Tay trái + Tay phải đều**: cần "vương" (compromise) layout center-symmetric. Số lượng case này ít.

Hệ quả thiết kế: bố cục lệch phải là default. Test edge case user tay trái nhưng không design layout chính cho họ.

## Phá UI — Đập Vỡ Grid Để Hút Mắt

Bình thường thiết kế UI theo grid để cân đều. **Phá UI** là cố tình làm lệch grid.

2 trường hợp thường phá UI:
1. **IAP** — nút to hơn bình thường, đẹp hơn, có effect (animation, glow).
2. **Giới thiệu content mới** — nút lệch hẳn khỏi grid để user nhận ra ngay.

Phá UI là kỹ thuật **monetization-aware**: designer chấp nhận UI không cân đối nếu nó tăng click rate cho element quan trọng. Khi grid hoàn hảo, user scan đều — không có gì nổi bật → IAP bị ignore.

## Tip Visibility Cho Nút

Yếu tố nhận diện nút (từ Doc 3):
- **To, rõ ràng, sạch sẽ, không phải sót** — đặt ở chỗ trung tâm, màu rực rỡ.
- **Quen thuộc** — *"thói quen của hành vi như chồng mình luôn ám"*. Button mua sắm thường xanh — user đã quen từ các game khác, nếu dùng màu khác → user không tìm được.
- **Tách bạch khỏi giả-nút** — *"các tách xong gạch nhịp giống kiểu game Hyper hay để cái chữ nồng thanh thì người ta cũng rất khó tìm. Người ta luôn sẽ ấn vào cái đầu tiên hiện lên."*

Anti-pattern Hyper UI (chữ nồng thanh, gạch nhịp) — user khó tìm đúng button, mặc định bấm cái đầu tiên hiện lên. Designer dòng casual nên tránh.

## Edge Case Vật Lý — Tay Trái vs Tay Phải, Ngón Dài/Ngắn

Vũ kể case con survival có nút multimedia thiết kế ban đầu cho user tay phải. Feedback từ user tay trái: *"tao phải đánh nhầm."*

Bài học: UX phải tính cả thằng tay trái, thằng tay phải, thằng ngón dài, thằng ngón ngắn — không thể design 1 layout phục vụ mọi cách cầm. Designer chọn primary case (tay phải) và accept secondary case bị compromise một chút.

## Liên Hệ Wiki

[[ux-3-criteria]] là khung 3 tiêu chí; thumb zone phần lớn liên quan đến tiêu chí 1 (số bước thao tác — bao gồm khoảng cách di chuyển). [[notification-management]] cho thứ tự noti — noti quan trọng cũng nên nằm trong thumb zone. [[dark-ux-techniques]] tận dụng thumb zone để đặt nút "lừa" (đảo X3, pop-up nâng cấp ở chỗ nút "back").

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Phá UI — Đập Vỡ Grid Để Hút Mắt", "Bố Cục Tầm Tay"
- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Visibility & Familiarity", "Edge Case — Thằng Tay Trái vs Tay Phải"
