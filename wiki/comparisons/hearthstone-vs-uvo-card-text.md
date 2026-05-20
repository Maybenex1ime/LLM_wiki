---
title: "Hearthstone vs uvo Card Text — Keyword Compression cho Mass Audience"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [comparison, ux, card-game, keyword-compression, information-density]
aliases: [Hearthstone keywords, uvo card text, card text length, keyword vs description]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[skin-bridging-comparison]]"
  - "[[user-test-no-explanation]]"
summary: "uvo card có description dài, 10 con = 10 kiểu khác nhau → niche audience (sưu tầm). Hearthstone dùng keyword (taunt, charge) → 10 con quy về ~2 kiểu → mass audience parse nhanh + so sánh ngay. Card text length trực tiếp ảnh hưởng audience scale."
---

## Bối Cảnh

Vũ minh hoạ tiêu chí "giảm lượng thông tin" (UX reduction #2) qua 2 game thẻ bài.

> *"Mọi người có biết con Hearthstone không? Con Hearthstone là con đại diện cho cái việc là tối giảm lực lượng thông tin. Những cái dòng rất dài ngoài của con Hearthstone nó chỉ viết bằng một cái gọi là keyword. Ví dụ như là street hoặc là chat. Đúng không ạ? Người dùng người ta hiểu ngay."*

## Bảng So Sánh

| Aspect | uvo | Hearthstone |
|--------|-----|-------------|
| **Card text length** | Dài, vài dòng full description | Vài keyword (1-3 từ) |
| **Skill expression** | Diễn giải verbose | Compressed keyword |
| **Reading time / card** | 10-20 giây | 1-2 giây |
| **Unique skill count** | 10 con = 10 kiểu | 10 con = ~2 kiểu (parametrized by stat) |
| **Card size** | Bé + dày | Vừa + ít text |
| **Audience** | Niche, sưu tầm hardcore | Mass-market |
| **Decision speed** | Slow (cần đọc kỹ) | Fast (icon + keyword + stat) |
| **Monetization potential** | Hardcore whale | Volume + mid-tier |

## Phân Tích

### uvo — Dense Description Pattern

User behavior:
- Mỗi card phải đọc text full.
- 10 cards trên bàn → 10× parsing time.
- Cần build mental model riêng cho mỗi card.

> *"Cái thẻ uvo này muốn mượn cái nút lắm rồi đấy. Chứ nó bé và nó dày. Xong lại đã thấy nó đọc không hiểu nữa. Chứ nó bé và nó dày."*

Audience implication:
- **Niche** — sưu tầm hardcore + reader fans.
- *"Sưu tầm thôi. Chứ các bạn mới chơi cái món đó nó khó lắm. 10 con là 10 kiểu khác nhau."*
- Đa số mass user dropped tại moment đầu vì không parse được.

### Hearthstone — Keyword Compression

User behavior:
- Scan keyword (taunt, charge, deathrattle, divine shield) → biết ngay archetype.
- Compare stat number → quyết định.
- Card duy nhất khác ở **stat** + **art**, không khác ở **skill description**.

> *"10 con nó chỉ quy về khoảng 2 kiểu thôi. Thì đấy chính là tối giản lượng thông tin. Tối giản lượng thông tin trong việc: 1 là phải đọc ít, 2 là nhiều nó phải lặp đi lặp lại."*

Audience implication:
- **Mass-market** — ai cũng parse được trong 2 giây.
- Onboarding nhanh — học 5-10 keyword là đủ.
- Monetize wide — F2P + casual đều convert.

## Khái Niệm — Keyword vs Description

| Keyword | Description |
|---------|-------------|
| Taunt | "Khi đối phương tấn công, phải tấn công minion có taunt trước" |
| Charge | "Có thể tấn công ngay lượt được ra" |
| Deathrattle | "Khi chết, kích hoạt effect bên dưới" |
| Divine Shield | "Block damage đầu tiên" |

Keyword compress description thành 1 từ. User memorize keyword = giải nén description tự động trong đầu.

Trade-off:
- Keyword cần repetition để dạy (in-game tutorial + tooltip).
- Sau khi user thuộc keyword → reading speed × 10.
- Description-based không cần dạy nhưng slow reading mãi mãi.

## Khi Card Text Dài Cho Phép

Trường hợp text dài justified:
- **Genre** = strategy hardcore (Magic the Gathering, original CCG).
- **Audience** = niche collectors expect deep mechanics.
- **Format** = physical card (text in hand, no time pressure).

Mass-market mobile card games (Hearthstone, Marvel Snap, Legends of Runeterra) đều adopt keyword compression. Pattern đã standardize.

## Visual Hierarchy Implication

> *"Nhiều con thì cái quyết định phía dưới nó mới dễ. À tóm lại 2 con có cái dòng giống hệt giống nhau, con nào có chỉ số to hơn — con nào có chỉ số to hơn nó có lấy mạnh hơn."*

Khi card có cùng keyword set:
- User compare **stat** (HP/ATK) — cao hơn = mạnh hơn.
- Quyết định mua / play deck nhanh.

Khi card có description khác nhau:
- User không biết compare gì.
- *"Bây giờ bạn cho 1 cái con mà nó viết khoảng tầm 2 dòng, 1 con khác viết khoảng tầm 3 dòng. Tóm lại con nào có 3 dòng theo góc độ của 1 thằng user — nếu như thế thì chắc là nên làm cả bản hình luôn. Mình sẽ nghĩ có cái mạnh nhất."*
- User assume dài = mạnh (heuristic) → bias decision.

## Recommended Pattern Cho Game Mass-Market

| Element | Hearthstone Pattern |
|---------|---------------------|
| Card text | ≤ 8-10 từ keyword (xem [[ux-3-criteria]] tiêu chí 2) |
| Icon | 2-3 icons phía dưới stat |
| Stat | Số to, position consistent (HP góc dưới phải, ATK góc dưới trái) |
| Rare indicator | Frame color + glow |
| Skill effect | Keyword + tooltip on long-press |

Avoid:
- Text > 3 lines.
- Multiple paragraphs.
- Tooltip needed cho mọi card.
- Custom skill cho mỗi card (use keyword library).

## Kết Luận

Card text length không phải design choice cosmetic — nó **define audience size**.

- Long text → niche (collectors, hardcore).
- Short keyword → mass (casual + competitive).

Designer choose target audience trước khi choose text density.

## Liên Hệ Wiki

[[ux-3-criteria]] tiêu chí 2 (giảm lượng thông tin) — keyword là pattern điển hình. [[skin-bridging-comparison]] cho cùng logic ở skin level (overlap để compare). [[user-test-no-explanation]] — test card text bằng cách show user mới không guide, đo "user hiểu trong X giây?"

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Case Hearthstone vs uvo — Keyword Compression"
