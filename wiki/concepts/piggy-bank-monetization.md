---
title: "Piggy Bank Monetization"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [concept, monetization, iap, ads, dark-ux]
aliases: [Piggy Bank, hút máu user, lợn tích tiền]
status: draft
related:
  - "[[dark-ux-techniques]]"
  - "[[iap-purchase-drivers]]"
  - "[[fueling-pacing]]"
summary: "Cơ chế Piggy Bank: tiền user kiếm được tự động vào lợn, user phải xem ad/IAP để rút. Vũ áp dụng trên Tidy Battle với chu kỳ 9-15 phút, không dài hơn vì user chỉ chơi 40-50 phút/ngày"
---

## Định Nghĩa

Piggy Bank là cơ chế hút máu cho thiếu tài nguyên — pattern monetization mà tiền user kiếm được tự động vào "lợn" thay vì vào ví. User phải xem ad hoặc trả tiền để rút.

Vũ chia sẻ pattern triển khai trên game **Tidy Battle**:
- Bình thường xem ad được 1.000 tiền.
- Cho Piggy Bank tích thêm 500 nữa.
- Vào Piggy Bank xem 1 ad → được tầm 1.500.

Cơ chế thuần (game khác làm, hardcore hơn): tiền user kiếm được **tự động** vào Piggy Bank → user phải dùng tiền thật mua lại chính tiền mình kiếm. Vũ nhận: *"Của con anh áp dụng thử — anh thường nhận là nó cũng hút máu thật."*

## Quy Tắc Thời Gian

Piggy Bank phải có chu kỳ phù hợp với session length:

- **9-15 phút cho 1 lần xem**.
- Không đặt dài hơn vì user tầm chơi 40-50 phút/ngày, dài quá user không quay lại được.

Logic: trong session 40 phút, user có thể trigger Piggy Bank 2-3 lần. Nếu chu kỳ 30 phút thì chỉ 1 lần → ít cơ hội ad. Nếu chu kỳ 5 phút thì spam → user mệt.

## Lý Do Hiệu Quả

Quote Vũ về tâm lý user:

> *"Rõ ràng giá trị của 1 quảng cáo nếu xem thông thường là 1 con số x, nhưng xem ở 1 chỗ khác lại là giá trị x của y. Về lý người chơi gì tính toán thích cái x của y này hơn. Việc có x của y này nó đẩy nhanh quá trình giá của y — xo ra này nhiều hơn. Vì sao? Vì họ thấy ra có 1 cái lỡ."*

Diễn giải: cùng 1 ad = 1.000 tiền (xem thường) vs 1.500 tiền (Piggy Bank). User thấy số 1.500 > 1.000 → bias đi xem ad ở Piggy Bank. Designer kích hoạt loss aversion: user cảm thấy *"nếu không xem, mất 500 tích lũy"*.

## 2 Biến Thể

| Biến Thể | Cơ Chế | Mức Độ Aggressive |
|----------|--------|---------------------|
| Vũ (Tidy Battle) | Ad thường = 1000, Piggy Bank ad = 1500 (bonus 500) | Vừa phải, user vẫn lựa chọn |
| Hardcore | Tiền kiếm tự động vào lợn, phải trả tiền thật mua lại | Hút máu mạnh — dark UX |

Vũ ưu tiên biến thể vừa phải. Biến thể hardcore thuộc [[dark-ux-techniques]] — chỉ áp dụng khi conversion thấp dù đã làm hết các pattern lành mạnh.

## Liên Hệ Với Fueling

Piggy Bank là một lever cụ thể của [[fueling-pacing]]:
- Giữ ad density không quá dày (cảm giác user).
- Bù bằng "giá trị mỗi ad" cao hơn (bonus 500 tiền).
- Tổng impression có thể giảm nhẹ nhưng eCPM × volume tăng do user click chủ động.

## Khi Nào KHÔNG Dùng

- **Game không có session liên tục** (vd. game tournament 1 trận/ngày) — Piggy Bank không tích đủ.
- **Game UX cao cấp** không chấp nhận pattern *"giam tiền user"* — risk brand.
- **Game subscription-only** — Piggy Bank xung đột với mô hình sub. Xem [[subscription-pack-design]].

## Liên Hệ Wiki

[[dark-ux-techniques]] cho khung dark UX tổng thể — Piggy Bank ở biến thể mạnh là dark UX. [[iap-purchase-drivers]] driver "thiếu tài nguyên" và "FOMO" — Piggy Bank kích hoạt cả 2. [[fueling-pacing]] là context lớn — Piggy Bank giúp tăng giá trị mỗi ad mà không tăng frequency.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Piggy Bank — Cơ Chế Hút Máu Cho Thiếu Tài Nguyên"
