---
title: "Value Perception — 4 Kỹ Thuật Design Cho Cảm Xúc"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, monetization, psychology, anchor-effect]
aliases: [value perception, big numbers, skill probability friendly, gift anchor, Highland upsell, cảm nhận giá trị]
status: draft
related:
  - "[[behavior-vs-stated-preference]]"
  - "[[iap-purchase-drivers]]"
  - "[[first-iap-strategy]]"
  - "[[feeling-of-assets]]"
summary: "4 kỹ thuật khai thác perceived value khác intrinsic value: big numbers (100 gold > 1 gold cùng tỷ lệ), skill probability fraction-friendly (33% > 7%), gift-on-package anchor (2M trên 4M total), Highland upsell (size M→L +2-3k). Design cho cảm xúc, không cho math."
---

## Định Nghĩa

Value perception = giá trị mà user **cảm nhận**, khác giá trị **thực** (intrinsic / mathematical). Vũ dạy 4 kỹ thuật khai thác chênh lệch này.

Tiền đề: design cho cảm xúc — xem [[behavior-vs-stated-preference]].

## Kỹ Thuật 1 — Big Numbers

Cùng tỷ lệ kinh tế, số to hơn = sướng hơn.

| Setup A | Setup B |
|---------|---------|
| Drop 1 gold | Drop 100 gold |
| Upgrade cost 1 gold | Upgrade cost 100 gold |
| Tỷ lệ purchasing power | Giống hệt |

User cảm thấy Setup B có giá trị cao hơn.

> *"Họ không biết được cái giá trị này và cái giá trị này nó tương quan với nhau như thế nào. Nhưng họ chỉ nhìn vào cái giá trị này cứ nhiều hơn là sướng."*

**Khi áp dụng**: chọn currency scale ngay từ ban đầu. 100/1000 cho gold, không phải 1/10. Tỷ lệ sau scale lên rồi không downscale được.

**Reference thực tế**: giá nhà VN tăng "danh nghĩa" nhưng tương quan purchasing-power không tăng. Người ta vẫn thấy "giá tăng" → vẫn tham gia thị trường. Same psychology.

## Kỹ Thuật 2 — Skill Probability Fraction-Friendly

Designer hay viết quyết tích **7%** hoặc **7.5%**. Anti-pattern.

> *"Đánh đời nào ra được 7%? Nhìn vào con số này nó có tưởng tượng đánh bao lâu ra không?"*

User parse decimal → không tưởng tượng được.

**Convert sang fraction**:

| Decimal | Fraction-Friendly | Cảm Xúc User |
|---------|-------------------|--------------|
| 7% | ~1/14 | Hên xui, đánh nhiều mới được |
| 33% | 1/3 | Đánh 3 phát chắc được |
| 50% | 1/2 | Coin flip, đánh 2 phát |
| 25% | 1/4 | Đánh 4 phát |

> *"Bây giờ đưa ra con số giống như 33% — à nó 10 tượng trong đầu rồi. Đánh 3 phát chắc được phải."*

Trận ~40 hit × 33% ≈ 13 lần proc → user thấy "đạt được." Trận ~40 hit × 7% ≈ 3 lần proc → user thấy "không bao giờ."

**Khi áp dụng**: skill chance, drop rate, crit rate. Chọn 1/2, 1/3, 1/4, 1/5 thay vì decimal lẻ.

## Kỹ Thuật 3 — Gift-on-Package Anchor

Cold-call sales script analogy. So sánh 2 pitch:

### Pitch Không Anchor (Failed)

- *"Tặng anh gói bao trời 2 triệu."*
- Câu hỏi: gói tổng giá bao nhiêu? — *"Gói đấy là 2 triệu anh ạ."*
- User cảm nhận: tặng 100% giá → không phải gift, chỉ là sale → không hấp dẫn.

### Pitch Có Anchor (Won)

- *"Tặng anh gói 2 triệu trên tổng gói 4 triệu."*
- User cảm nhận: deal 50% off → giá trị thật tăng 2× → **phát sinh nhu cầu nghe.**

> *"Nghèo khác rồi. Nó mới phát sinh nhu cầu nghe. Sướng luôn."*

**Cơ chế tâm lý**: anchor effect. Não user so sánh **giảm/tăng giá vs giá gốc** thay vì giá tuyệt đối.

**Khi áp dụng trong game**:
- Starter pack: "$2.99 — gốc $14.99" (gạch ngang $14.99).
- IAP shop: luôn show "save 50%."
- Event offer: "limited time 70% off."

Xem [[first-iap-strategy]] cho x2/x8 ratio cho first-IAP.

## Kỹ Thuật 4 — Highland Upsell (Bypass Thinking)

Cà phê Highlands:
> *"Các bạn chỉ bỏ thêm khoảng 2000 đến 3000 nữa là bạn được một cốc cà phê từ size M lên size L. Thế là thôi bắt đầu cái máu tham nó nổ lên — còn chả biết là cái size L nó nhiều hơn size M bao nhiêu mà cứ mua cái cốc to nhất."*

### Cơ Chế

| Element | Vai Trò |
|---------|---------|
| **Delta nhỏ** (+2-3k) | Bypass decision cost |
| **Size to hơn rõ ràng** (M → L) | Cảm xúc "tham" |
| **Không có comparison value** | User không biết L hơn M bao nhiêu ml |

Quyết định = tham giá trị/ít cost → bypass thinking.

> *"Tức là mình đang không nói về vấn đề tính định lượng hay vấn đề về giá. Mình đang nói cái tư duy để họ đẩy cho mình này — giảm bớt số lượng suy nghĩ ra để quyết định."*

### Khi Áp Dụng Trong Game

- **IAP pack upsell**: pack $4.99 → pack $5.99 with 2× content. Delta nhỏ, content rõ ràng to hơn.
- **Bundle**: 1000 gold for $0.99, 2200 gold for $1.99. User cảm thấy "thêm 1 đô được nhiều hơn."
- **Subscription tier**: monthly $4.99, yearly $39.99 (3 tháng free). Delta tạo cảm giác lời.

Common pattern: 3 tier (small/medium/large), middle tier có "best value" badge — phần lớn user pick middle.

## Value-For-User AND Value-For-Studio

Tất cả 4 kỹ thuật chỉ có ích khi serve cả 2:

> *"Bây giờ các bạn tặng cho nó cái gì mà nó không có nhu cầu phát sinh mua bán nữa thì là cái không tốt với mình. Nhưng bạn tặng cái gì đó mà để cho nó phát sinh nhu cầu mua bán thì là cái đấy tốt với mình."*

Gift không sinh nhu cầu mua = waste. Big number drop không lead vào upgrade cost = waste. Mọi reward phải đẩy user vào loop chi tiêu tiếp theo.

## Anti-Pattern Tổng Hợp

- **Currency scale 1/10** thay vì 100/1000 — số không cảm xúc, không upgradable.
- **Decimal skill % (7%, 7.5%)** — user không tưởng tượng được.
- **Offer không có anchor giá gốc** — user không thấy deal.
- **Pack tier có delta to** ($0.99 → $9.99) — bypass thinking fail, user dừng cân nhắc.
- **Gift to không tied vào upgrade need** — sướng nhưng không chi tiêu.

## Liên Hệ Wiki

[[behavior-vs-stated-preference]] tiền đề "design cho cảm xúc." [[iap-purchase-drivers]] cho 12 drivers IAP — value perception thuộc category emotional drivers. [[first-iap-strategy]] cho x2/x8 first-IAP ratio áp dụng anchor. [[feeling-of-assets]] cho 6 đặc tính tài sản — số lượng (big numbers) là 1 trong 6. [[piggy-bank-monetization]] dùng kỹ thuật accumulation để tăng perceived value rút lợn.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "4 Ví Dụ về Value Perception"
