---
title: "eCPM — Biến Hộp Đen Designer Không Kiểm Soát"
source: "[[raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset]]"
date_added: 2026-05-15
tags: [concept, monetization, ecpm, ads, ua]
aliases: [eCPM blackbox, eCPM phụ thuộc cái gì, app quality]
status: draft
related:
  - "[[ltv-cpi-formula]]"
  - "[[iaa-iap-migration]]"
  - "[[user-cannibalism]]"
summary: "eCPM là biến doanh thu quảng cáo mà designer không trực tiếp kiểm soát — phụ thuộc CTR, tệp UA, style game, performance Play Store, dẫn đến 2 game giống hệt nhau có thể eCPM gấp 3 lần nhau"
---

## Định Nghĩa

eCPM (effective Cost Per Mille — doanh thu trung bình quảng cáo trên mỗi 1000 lượt hiển thị) là một biến mà Vũ gọi là **hộp đen** vì designer không kiểm soát trực tiếp được. Tổng quát: `Earnings = eCPM × impressions / 1000` — designer có thể tăng impressions qua thiết kế ad placement, nhưng eCPM gần như là output của ad-network thị trường.

Case Vũ kể: anh và Giang từng có **2 con game giống hệt nhau** mọi mặt (cơ chế, art, balance, retention) nhưng **eCPM một con gấp 3 lần con kia**. *"Tất cả những thứ về tiệm khách hàng — là năng chen, là ad-network, là buy-back, organic, v.v. — nó cũng 1% mà mẹ nó sinh ra. Cũng có 2 con giống hệt nhau mà chỉ số nó không đúng nhau."*

## eCPM Phụ Thuộc Cái Gì

Hiệp breakdown các yếu tố ảnh hưởng:

- **CTR (Click-Through Rate)** — tương tác của user trong app với ad. CTR cao → ad-network trả eCPM cao hơn.
- **Tệp khách hàng đầu vào** — tuổi, giới tính, sức mua, khu vực. *"Tệp khách hàng này UA Quick có thể đổ về CPI cao hay thấp, chọc vào người già hay người trẻ — UA Quick CVL này chỉ biết được cái này."*
- **Mức độ đồ họa** — game art tâm linh hơn hyper tay nhẹ thì eCPM trên user trẻ khác.
- **Style game** — Vũ note đây là **biến quyết định cuối cùng**.
- **Performance trên Play Store** — *"hiện trạng bây giờ chính là cái app quality. Khi performance đủ tốt, bản thân Play sẽ trả vào những user chất lượng — và khi user chất lượng thì eCPM tất cả sẽ tốt."*

## Pattern Counter-Intuitive

Có sản phẩm chỉ số *"rất tuyệt vời nhưng eCPM không gì cả — chịu"*. Có sản phẩm chỉ số bình thường, CPI cũng cao, nhưng eCPM trên rời, vẫn win. Đây là lý do [[ltv-cpi-formula]] không phải công cụ forecast doanh thu chính xác — chỉ là công cụ decide go/no-go.

Vũ kết: *"Bí ẩn thật. Đúng không? Đó là giải thích được không? Đó không có câu trả lời."*

## Clone Scale Không Được — User Cannibalism

Đạt hỏi: nếu mô hình tốt, có thể clone 100 con cùng lúc để scale không? Vũ + Hiệp đồng quan điểm **không được vì user cannibalism**.

> *"Phân bổ user thì có thể anh biết — chính là user anh đã chạy ở quán tốt rồi. Bây giờ anh chạy với cái tệp đấy, có thể anh sẽ đi rớt lại chính như user đấy — mà cái giá trị đấy là giá trị thấp hơn. Và 2 con đấy của anh đang cạnh tranh, chứng kiến với nhau."*

Khi 2 con cùng studio target cùng tệp user, eCPM của con sau giảm vì user đã quen UI/UX/style của con trước → ít click ad hơn. Hiệp note ngoại lệ: bên app (không phải game) — *"có những sản phẩm 100 con nhưng có khi chỉ 10 con ngon cười và 5 con ngồi khóc"* — vẫn có spread, không phải đều. Xem [[user-cannibalism]].

## Hệ Quả Cho Designer

Vì eCPM không control được, designer chỉ có 2 hướng:
1. **Tăng impressions** qua ad placement (xem [[inter-ad-redefinition]], [[rv-placement-strategy]]).
2. **Migrate sang IAP** để giảm phụ thuộc eCPM thị trường — xem [[iaa-iap-migration]].

Vũ không khuyên cố tối ưu eCPM trực tiếp — *"đó không có câu trả lời"* — mà thiết kế sao cho game vẫn lãi ngay cả khi eCPM thấp hơn baseline.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset.md` § "eCPM — Biến Hộp Đen Designer Không Kiểm Soát Được", "Clone 100 Bản Có Được Không"
