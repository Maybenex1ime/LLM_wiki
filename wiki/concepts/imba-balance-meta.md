---
title: "Imba Balance — Cân Bằng MTV vs Power Tại Checkpoint"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [concept, balance, progression, iap, meta]
aliases: [imba balance, balance gói tướng, tường mới, MTV vs power]
status: draft
related:
  - "[[balance-scale]]"
  - "[[iap-pricing-user-value]]"
  - "[[rpg-unit-weakness-principle]]"
  - "[[first-iap-strategy]]"
summary: "Khi bán gói tướng/meta, GD phải balance MTV (EV/EAV — material target value) với power tại từng checkpoint. Imba có chủ ý ngắn hạn ok, mất cân bằng dài hạn → game mất giá trị progression"
---

## Định Nghĩa

Học viên có game có gói tướng (bán theo cấu trúc 10$/5$/7$). Vấn đề: nếu user mua được gói cuối → sở hữu hết toàn bộ tướng meta → game **mất giá trị progression**. Vũ phân tích đây là bài toán **imba balance** (imbalance balance) — cân bằng giữa giá trị tài sản và yêu cầu content tại các checkpoint.

> *"Anh bán cho người ta đến đây không đúng — người ta đã đủ khả năng sở hữu toàn bộ cái thời gian cho cái con game này của anh rồi. Thế dẫn đến xong nó sẽ không còn giá trị nữa."*

## Nguyên Tắc Cân Bằng

Vũ vẽ nguyên tắc:

> *"Em phải luôn luôn balancing được cái MTV (có thể là EV, có thể là EAV) tại một checkpoint, bằng với power của nó tại checkpoint này — hoặc lớn hơn nhỏ hơn cộng trừ một con số nào đó. Chứ đừng để mất cân bằng."*

Diễn giải:
- **Tại mỗi checkpoint** (mốc content, mốc level), tính:
  - **MTV** (Material Target Value): tổng giá trị tài sản user đang có (gói đã mua + farm tích lũy).
  - **Power user**: chỉ số combat / progress yêu cầu để pass checkpoint.
- MTV ≈ Power user (cộng trừ một biên độ chấp nhận được).
- Cấm: MTV >> Power (user vượt quá xa) hoặc MTV << Power (user mua tiền vẫn không qua).

## 2 Dạng Mất Cân Bằng

### Imba Cao Quá Sớm

User mua xong tới checkpoint mới mà power vẫn vượt yêu cầu → không cần grind, content tiếp theo vô nghĩa. Hậu quả:
- User thấy không có thử thách → bỏ.
- Game không còn cơ hội bán gói tiếp theo (user đã có sẵn power).

Đây chính là vấn đề ban đầu — bán gói cuối quá xa, user sở hữu toàn bộ.

### Yếu Một Cái Đáy Ra

User trả tiền xong rồi power vẫn không đủ → cảm thấy bị lừa, refund hoặc bỏ. Hậu quả:
- Lòng tin tụt → không nạp tiếp.
- Review tiêu cực.

Đây là pattern nhiều studio mắc khi *"đánh giá sai user power"* — bán gói thấp giá trị ở checkpoint cao.

## Imba Có Mục Đích — Tường Mới

Có lúc cố ý cho imba ngắn hạn để thúc đẩy mua thêm:

> *"Em phải cần để cho nó imba một thời gian. Chứ nó nạp tiền xong rồi nó không imba thì dở rồi."*

Pattern imba có chủ ý:
- User nạp tiền → cảm giác mạnh mẽ ngắn hạn (MTV > Power một chút).
- Designer plan **tường mới** (content/độ-khó mới) ở khoảng 1-2 ngày sau.
- Khi đụng tường mới → cân bằng lại MTV vs Power → user cần mua gói tiếp.

Tường mới làm đằng sau, không phải đẩy thẳng ngay từ đầu — phải cho user "tận hưởng" power vừa mua một thời gian, sau đó mới ép. Đây là kỹ thuật giữ momentum mua hàng mà không gãy progression.

## Liên Hệ Wiki

[[balance-scale]] là khung tổng thể cho phân tỷ trọng module — imba balance là instance cụ thể tại từng checkpoint. [[iap-pricing-user-value]] cho khung định giá để tránh "cất bằng sai đồng tiền" (bán $10 cho hero unlock $300 worth journey). [[rpg-unit-weakness-principle]] là cơ chế giúp giải imba — mỗi unit có weakness → user phải mua unit khác cho map khác → không có gói duy nhất sở hữu toàn bộ. [[first-iap-strategy]] (comparison) cho 2 trường phái pricing gói đầu — first-IAP rất rẻ có thể tạo imba ngắn hạn dễ.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Imba/Balance Gói Meta — Bài Toán Của Game Có Tướng"
