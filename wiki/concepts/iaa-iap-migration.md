---
title: "IAA → IAP Migration"
source: "[[raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset]]"
date_added: 2026-05-15
tags: [concept, monetization, iaa, iap, hybrid, mobile-games]
aliases: [IAA sang IAP, hybrid monetization, migrate IAA IAP]
status: draft
related:
  - "[[ecpm-blackbox]]"
  - "[[ltv-cpi-formula]]"
  - "[[fueling-pacing]]"
  - "[[first-iap-strategy]]"
summary: "Vì sao mọi studio mobile đang muốn chuyển từ IAA (in-app ads) sang IAP (in-app purchase) hoặc hybrid — eCPM hyper sụp, puzzle dominate, IAP độc lập với ad-network"
---

## Định Nghĩa

IAA → IAP migration là xu hướng các studio mobile (đặc biệt là hyper casual) chuyển dần cấu trúc doanh thu từ phụ thuộc quảng cáo (in-app ads) sang phụ thuộc mua trong app (in-app purchase). Vũ và Hiệp giải thích bối cảnh thị trường khoảng 2025-2026 đẩy migration này thành nhu cầu thực tế chứ không phải lựa chọn.

```
Game Revenue ─┬─ IAA (in-app ads)
              │   ├─ eCPM (impression rate × cost)
              │   └─ Cross-promo
              └─ IAP (in-app purchase)
```

## Tại Sao IAA Khó Lúc Này

Vũ phân tích:

- Khi market hyper casual yếu đi → các studio hyper không còn mua user nữa → eCPM dòng hyper tụt → *"anh có làm tốt tất cả đi sáng nữa cũng chẳng ai mua của anh"*. Studio hyper bán user cho studio hyper khác — khi cả ngành ngừng mua, network tê liệt.
- Top trend thị trường giờ là **puzzle** — chính dòng puzzle đang mua chéo user của nhau bằng giá cao hơn → eCPM puzzle ổn.
- Nhiều studio muốn migrate sang puzzle để hứng eCPM của hệ này.

Đây là một dạng cross-network dependency: eCPM của bạn phụ thuộc vào việc có bao nhiêu studio cùng dòng đang mua user. Xem [[ecpm-blackbox]] cho lý do tại sao đây là biến hộp đen.

## IAP Là Đường Riêng

IAP không phụ thuộc cross-network — user trả tiền trực tiếp cho studio, không qua ad-network. Nhưng IAP khó về mặt design: *"IAA thì dễ, nhưng khi chúng ta chuyển sang IAP thì không dễ thì cũng dễ — hy vọng các bộ này cũng sẽ giúp mọi người làm cái gì đó."*

Đạt đưa ra case cụ thể: eCPM thấp nhưng product quality OK → migrate sang IAP được không? Hiệp confirm được, nhưng *"phải tách bạch — không bị ảnh hưởng"*. Tức là design IAP phải đứng độc lập, không phụ thuộc rằng ad-network sẽ trả tốt.

## Hybrid — Bước Trung Gian

Vũ tiết lộ Doc 5-6 (khóa học) sẽ có *"chuyển mô hình từ một con IAA sang một con hybrid, mà chuyển từ một con hybrid sang một con IAA thuật."* Hybrid = vừa có ads vừa có IAP, từ từ giảm trọng số ads tăng trọng số IAP.

Case Mob Control Vũ kể: từ hyper sang hybrid bằng cách *"thay vì core loop từ 1 đến 2, người ta làm 1 → 1.5 → 1.8 → 1.9 → 2"* — kéo lifetime dài qua việc đi đường vòng nhưng vẫn satisfying. Lifetime dài hơn → có chỗ cho IAP gating mid/late-game. Liên quan đến [[fueling-pacing]] (kéo break-even từ D3 sang D7+).

## Bài Học Cho Studio Hyper

Khi trend hyper xuống, Vũ kể case Imposter Solo Queue đã thử 3 hướng:

1. **Thay đổi tần suất quảng cáo** (delay deeper, ngắt mạch giữa) → ổn.
2. **Chuyển sang IAA + IAP** (hybrid) → *"có một lượng user chuyển sang IAP"*.
3. **Clone sang con trend mới** (Fall Guys) → *"có sự thay đổi"*.

Hướng 2 là migration thực sự — không bỏ IAA, chỉ thêm IAP làm second revenue stream. Khi trend tắt, CPI tăng → phải tăng LTV bù lại bằng kéo dài core loop.

## Liên Hệ Wiki

[[ecpm-blackbox]] giải thích vì sao IAA đặt rủi ro vào tay ad-network. [[ltv-cpi-formula]] là khung số giúp quyết định khi nào migrate (LTV stagnate dù CPI ổn → cần IAP để break ceiling). [[fueling-pacing]] là kỹ thuật cụ thể để kéo dài lifetime, mở chỗ cho IAP late-game. [[first-iap-strategy]] là 2 trường phái pricing cho gói IAP đầu tiên khi mới migrate.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset.md` § "IAA → IAP Migration — Vì Sao Ai Cũng Muốn Chuyển", "Chase Trend"
