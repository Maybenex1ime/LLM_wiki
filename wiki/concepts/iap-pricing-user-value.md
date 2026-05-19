---
title: "IAP Pricing Theo User Value"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [concept, monetization, iap, pricing, user-value]
aliases: [định giá IAP, user value formula, cất bằng sai đồng tiền]
status: draft
related:
  - "[[iap-purchase-drivers]]"
  - "[[imba-balance-meta]]"
  - "[[first-iap-strategy]]"
  - "[[rpg-unit-weakness-principle]]"
summary: "Định giá IAP theo user value = thời gian chơi × giá phút theo quốc gia. Anti-pattern: 'cất bằng sai đồng tiền' — bán $10 cho hero pack mà mở ra $300 worth journey, user xài quá dài không có paywall tiếp"
---

## Định Nghĩa

Vũ đề xuất công thức định giá IAP dựa trên **user value** thay vì *"đoán giá thị trường"*:

```
User value (USD) = thời gian chơi (phút) × giá phút (USD/phút theo quốc gia)
```

Ví dụ:
- 100 phút × $0.1/phút = $10 → user balance = $10.
- Gói IAP nên định giá tương đương $10 = 1000V (V = currency in-game).

Đây là cách neutral để chốt gói "đáng giá" — không phải đắt hơn (user không mua) hay rẻ hơn (mất doanh thu).

## Anti-Pattern — Cất Bằng Sai Đồng Tiền

Case Giang bán hero pack $10:

- Hero pack thực ra unlock được **$300 giá trị journey** trước mặt (user mua hero này, đi qua $300 worth of content trước khi cần next pack).
- Bán $10 → user *"đi từ đây đến đây phải bỏ $300 thì em đang bán giá $10, tức em đang cất bằng sai đồng tiền."*
- Hậu quả: user mua xong đi dài quá → designer chưa kịp set next paywall → IAP velocity giảm.

Quote Vũ:

> *"Cái sỉ số của Halo nó phải tương đối với cái chuyện cho người ta đi một đoạn xong người ta mới phải đi tiếp content của em — chứ đừng để cho người ta đi một đoạn dài quá."*

Quy tắc: **giá gói IAP phải khớp với journey value mà gói mở ra**, không khớp với "giá cảm nhận" của tài sản. Bán hero $10 trông rẻ trước user, nhưng nếu hero mở ra $300 content thì designer mất chu kỳ IAP tiếp theo.

## Buy7 1.8% Cao — Nhưng Progress Mất Cân Bằng

Buy7 = % user mua IAP sau D7. 1.8% là rất cao (con bắn máy bay Inhalt cao nhất là 0.07%). Tuy vậy có thể signal *"em cân bằng progress người chơi chưa tốt — nó đang mua nhiều của T0, T1, T2 (gói tier thấp), chỉ trôi đến T5 là hết, dừng lại luôn."*

Hệ quả: Buy7 cao nhưng later-tier IAP không scale → game mỏng. Khi tier T0-T2 quá rẻ và pack lớn, user mua sạch tier thấp rồi không có lý do mua tier cao. Đây là dấu hiệu cần re-pricing — tăng giá T0-T2 hoặc giảm value để buộc user phải lên T5+.

## Drivers IAP Quyết Định Pricing

Vũ phân tích các động cơ IAP, ý chính: *"Làm thế nào để người ta giải quyết vấn đề liên tục — khi người ta giải quyết vấn đề liên tục thì người ta mới phát sinh IAP liên tục."*

Pricing strategy phải khớp với driver:

- **Giải quyết vấn đề** (battle): bán nhỏ liên tục — Buzo micro-pack pattern.
- **Time-starve solve** (idle): bán pack thời gian + tăng tốc, giá theo thời gian skip.
- **Aesthetic / Skin**: giá flexible, dựa trên "đẹp" và scarcity.
- **Social validation / Leaderboard**: bán power-ups gắn với top tier rankings.
- **Phá giới hạn bản thân**: bán content unlock (level mới, mode hard).
- **Rich user mua vô tư**: giá có thể cao thoải mái — nhóm này không sensitive.

Xem [[iap-purchase-drivers]] cho list 12 drivers chi tiết.

## Continuous Friction Pattern

Buzo (con micro-pack): mỗi vấn đề nặng nhỏ nhưng liên tục → nạp liên tục, không nạp 1 cú lớn. *"Cái lượng nặng của nó rất nhỏ nhưng nó lại nặng nhiều — nó nặng liên tục nhiều."*

Pricing implication: nhiều micro-pack $0.99-$2.99 thay vì pack lớn $19.99. Tổng revenue/user có thể cao hơn vì user dễ click $0.99 nhiều lần.

## Liên Hệ Wiki

[[iap-purchase-drivers]] cho list các động cơ IAP. [[imba-balance-meta]] cho khung "MTV vs Power" — IAP pricing phải đảm bảo MTV mua tăng tương ứng với checkpoint khó. [[first-iap-strategy]] (comparison) cho 2 trường phái cho gói đầu (x2 vs x8). [[rpg-unit-weakness-principle]] giải thích vì sao mỗi unit cần weakness — không có weakness thì gói $10 unlock toàn bộ meta → "cất bằng sai đồng tiền" theo định nghĩa lớn hơn.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "IAP Design — Why People Pay", "Định Giá IAP Theo User Value", "Buy7 1.8% Cao — Nhưng Progress Mất Cân Bằng"
