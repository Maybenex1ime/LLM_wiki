---
title: "Fueling — Pacing Khai Thác Value"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [concept, monetization, pacing, fueling, mu-net, mobile-games]
aliases: [fueling pacing, mũ nét, money knot, pacing khai thác value]
status: draft
related:
  - "[[d7-vs-d3-breakeven]]"
  - "[[ltv-cpi-formula]]"
  - "[[iaa-iap-migration]]"
  - "[[inter-ad-redefinition]]"
summary: "Fueling = tốc độ/phân bổ khai thác value từ user qua thời gian. Game 'lãi ở đây mũ' (mũ nét xa, lãi D7+) khó làm hơn nhưng dễ scale hơn game 'lãi ở đây' (lãi D0/D1)"
---

## Định Nghĩa

**Fueling** (theo cách Vũ dùng trong Doc 3) là **tốc độ/phân bổ khai thác value từ user qua thời gian** — không phải "battle simulation" như một số bản transcript cũ phiên âm sai. Khái niệm gắn liền với *điểm hòa* (break-even point) trong UA economics.

Quote định nghĩa:

> *"Mà về mặt fueling, thì khi mà các bạn dồn dậm quá nhiều các thứ để chúng ta kiếm tiền từ 1 user trong lần ra đầu — có nghĩa là người ta sẽ bỏ rất là nhanh. Có khi chúng ta cũng không nhận được cái gì đó."*

Analogy Vũ dùng: như mua nhà — *"người ta phải dàn trả ra trả nợ, không bắt bạn trả nợ ngay được. Mình phải dàn trải ra, sau đó người ta thanh toán lại."*

## Mũ Nét — Money Knot

Vũ phân biệt 2 trục thiết kế game theo vị trí mũ nét (money knot — điểm tiêu tiền của user):

- **Game "lãi ở đây"** (đầu game) — spam art / sản phẩm chỉ ăn user ở ngay đầu, không scale được sâu. Mũ nét đặt ngay D0/D1.
- **Game "lãi ở đây mũ"** — mũ nét đặt ở giữa và sâu trong game, user phải đi đoạn dài mới đến.

> *"Game lãi ở đây không, lãi ở đây mũ. Và game lãi ở đây mũ thì game nào dễ scale cơ? Lãi ở đây mũ sẽ là game rất dễ scale. Và đây là cách làm game — chứ không phải làm game như này."*

Game "lãi ở đây mũ" khó hơn — cần kiến thức làm cả hệ thống mũ nét, quảng cáo phải phát đúng tác dụng. Đổi lại scale được. Xem [[inter-ad-redefinition]] — đặt inter đúng nghĩa là điều kiện tiên quyết.

## Hyper vs Hybrid/ERP Fueling

### Hyper — Ép D0/D1

Game hyper buộc fueling dồn sớm:
- Phải khai thác cực kỳ vào D0/D1 để hoà.
- Khai thác quá nhiều → user mệt mỏi, khó chịu, retention D1 thấp.
- Phù hợp dòng hyper vì lifecycle ngắn (~3-6 tháng) và CPI rẻ; không scale được lâu dài.

### Hybrid / ERP — Trải Dài D3-D7+

Game hybrid hoặc ERP cho phép fueling dàn trải:
- D3, D7 (hoặc D14, D30) là điểm hoà.
- Mỗi ngày khai thác một phần, user không cảm thấy bị ép.
- Pool user tiếp cận lớn hơn vì spam ad/IAP nhẹ tay → cả non-IAP user lẫn pay user cùng giữ được.

Quote so sánh: *"Mình cứ hiểu đơn giản là một con nó hoà ngay từ đầu thì cái đường dốc nó đâm xuống nhanh hơn. Còn con kia tuy nó dốc hơn nhưng mà sau một ngày D7 vậy thì nó vẫn còn kiếm được tiền — nó sẽ kiếm được nhiều tiền hơn."*

## Điều Kiện Tiền Đề Chuyển D3 → D7

Vũ nhấn: chuyển từ D3 hoà sang D7 hoà **không phải chỉ là chuyển target**. Tiền đề bắt buộc:

- **Content kéo dài tới ít nhất D7** — không chỉ đủ hấp dẫn vài ngày đầu.
- **Quảng cáo + IAP có cấu trúc dàn trải** — không chỉ frontload ngay D0.
- **Pool sản phẩm chất lượng** — *"không tự nhiên chúng ta mang một cái món hà hay là một cái quả dưa bị thối ra bắt người ta mua."*

Case study Vũ kể: con Múc Càn Trô — ngày trước chạy theo cách hoà D3 → chỉ scale được ~30 triệu downloads. Sau khi chuyển sang hoà D30 → scale lên gần 200 triệu downloads.

## Case Hiệp — Giãn Inter Tăng LTV 60-70%

Hiệp chia sẻ case giảm density inter, kéo lãi sang day xa hơn:

| Phiên bản | Logic | LTV tổng |
|-----------|-------|----------|
| Approach cũ | 1 level → 1 inter | Baseline |
| Logic 1 | Sau 2 level → 1 inter | Tăng 1 chút |
| Logic 2 | Sau khi xem 1 inter → phải 1 phút sau mới hiện inter tiếp | LTV tổng kéo ~160-170% (tăng 60-70%) |

> *"Cái bản giảm là xem 1 inter thì 1 phút sau nguyên inter, thì cái chỉ số nó tăng lên tương đối là vượt. Và bọn mình kéo cái mức độ hoà xuống ngày 3 — nhưng bù lại thì tăng lên khá là tốt."*

Bài học: giảm doanh thu D1-D2 để kéo dài user → tổng LTV tăng vượt. Áp pattern này sang các con sau làm baseline cho team.

## Liên Hệ Wiki

[[d7-vs-d3-breakeven]] (comparison) là chi tiết về 2 mốc break-even. [[ltv-cpi-formula]] là khung số xa hơn — fueling phải làm LTV vượt CPI. [[iaa-iap-migration]] là context lớn — migration sang hybrid mở chỗ cho fueling dàn trải. [[inter-ad-redefinition]] giải thích cách đặt inter đúng tác dụng (không spam) — điều kiện tiên quyết cho fueling.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Mũ Nét — Lãi Ở Đâu Trên Game", "Fueling — Pacing Khai Thác Value", "Giãn Inter — Case Tăng LTV 60-70%"
