---
title: "RPG Unit Weakness Principle"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [concept, rpg, balance, unit-design, iap]
aliases: [unit weakness, mỗi unit phải có điểm yếu, tuning RPG]
status: draft
related:
  - "[[imba-balance-meta]]"
  - "[[iap-pricing-user-value]]"
  - "[[5-levels-of-idea]]"
summary: "Trong RPG/tower-base có hero, mỗi unit S-tier ở 1 hệ phải là C/B ở các hệ khác. Unit không weakness → game mỏng vì user mua xong 1 unit là đủ cho mọi map"
---

## Định Nghĩa

Trả lời case Giang (dòng tower-base có hero/unit), Vũ chốt nguyên tắc thiết kế RPG:

> *"Trong nguyên tắc thiết kế RPG, tuyệt đối là con nào làm ra phải có điểm yếu. Bởi vì cái điểm yếu chính là cái mà khiến em mua con này rồi phải mua con khác. Và thiết kế level cũng phải theo điểm yếu và điểm mạnh của từng con — nó là cái khởi tạo ra đề bài tất cả mọi thứ."*

Unit không weakness → một gói duy nhất unlock toàn bộ game → game mất giá trị progression. Đây là instance cụ thể của [[imba-balance-meta]] cho dòng game có unit.

## Phân Tích Con Tướng "Không Có Điểm Yếu"

Vũ phân tích một con tướng của Giang:
- Đam to / AoE / tốc độ công nhanh.
- *"Không có điểm yếu một câu."*

Hệ quả:
- Unit này là $300 unit theo [[iap-pricing-user-value]] — bán $10 là sai giá.
- Designer phải làm next unit big-3 hơn → leo cảm xúc → fueling sai.
- User mua xong dùng cho mọi map → không có lý do mua unit khác.

## Nguyên Tắc Tuning

- Mỗi unit **S-tier ở 1 hệ** (1 mode chơi), **C/B ở các hệ khác**.
- Bot vs quái là 2 hệ riêng → 1 unit không thể S cả 2.
- Multi-class system phải plan **ngay từ đầu** — không phải đợi có số liệu drop để tuning.

Quote bài học:

> *"Em đã phải tuning ngay từ đầu về các từng cái unit hoặc là từng cái hệ của từng class. Người ta mới có định hướng — tao sang map mới, con tướng này của tao sẽ bị counter, sẽ yếu đi, hoặc bị con khác counter lại."*

> *"Không phải đến lúc em có số liệu drop để em làm — phải tuning chôn ngay từ đầu."*

## Level Design Theo Weakness

Designer dùng weakness của unit để cấu trúc level/map:

- **Map A** spawn quái mà tướng X mạnh → user dùng X → cảm thấy *"mua đúng con"*.
- **Map B** spawn quái mà tướng X yếu → user phải mua tướng Y mới qua.

Pattern này tạo **chuỗi vấn đề liên tục** — driver IAP số 1 trong [[iap-purchase-drivers]]. User không thấy bị ép vì *"map mới, weakness mới, hợp lý thôi"*.

## Tower Defense Example

Doc 1 Vũ kể case Tower Defense khắc hệ quân: game có hệ Red / Blue / Green. Wave đầu toàn red → user dồn gold nâng cấp blue (counter red). Hết gold → đột ngột thả green vào → quân của user khắc kiểu hết.

*"Không cần tăng chỉ số, chỉ cần thay đổi sức lực quân thôi — bây giờ còn toàn quân lại level 1, làm gì? Xem ad, nhận tiền nâng cấp, hoặc mua."*

Đây là RPG unit weakness áp vào dạng simplified — không có hero, nhưng có "unit class" với weakness rõ.

## Anti-Pattern — Đợi Số Liệu Để Tuning

Designer mới hay làm: tạo nhiều unit, balance theo cảm tính, đợi data drop về rồi nerf/buff. Vũ note pattern này thất bại vì:

1. Tuning sau khi user đã mua unit → user phản ứng nặng (cảm thấy bị lừa).
2. Multi-class chỉ work khi designed-in từ đầu — patch không thể tạo weakness ngược.
3. Lost weeks/months trước khi có data đủ.

Vũ note: *"Khóa này không có phần RPG sâu"* — chỉ giới thiệu nguyên tắc, không deep-dive multi-class system.

## Liên Hệ Wiki

[[imba-balance-meta]] là context lớn — unit weakness là cơ chế cụ thể để balance MTV vs Power. [[iap-pricing-user-value]] cho khung định giá unit theo content value mà unit mở ra. [[5-levels-of-idea]] level 4: GD phải biết "tại sao user phải mua tướng Y" — RPG unit weakness chính là cơ chế đó.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "RPG Unit Design — Nguyên Tắc 'Phải Có Điểm Yếu'"
- `raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset.md` § "Tower Defense — Khắc Hệ Quân"
