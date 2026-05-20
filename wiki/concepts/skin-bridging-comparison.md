---
title: "Skin Bridging — ABC/BCD/ACD Pattern Cho So Sánh"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, skin-design, skill-design, comparison-ux]
aliases: [skin bridging, ABC BCD ACD, skin overlap, skin disjoint, skill comparison]
status: draft
related:
  - "[[material-count-decision-paralysis]]"
  - "[[ux-3-criteria]]"
  - "[[clash-royale-percent-stat-display]]"
  - "[[rpg-unit-weakness-principle]]"
summary: "5 con với skill disjoint (ABC vs DEF) — user không có cơ sở so sánh. 5 con với skill bridging (ABC/BCD/ACD) — user dùng skill overlap làm cầu nối → loại dần. A+ pattern: same skill set, stat lớn hơn → quyết định mua nhanh."
---

## Định Nghĩa

Skin Bridging = thiết kế skill/skin sets có **overlap** giữa các nhân vật → user dùng skill chung làm anchor để so sánh.

Đối lập: Skin Disjoint — mỗi nhân vật có skill set độc lập → không có baseline so sánh → user không quyết định mua.

## So Sánh Pattern

### Pattern Disjoint (Xấu)

```
Con 1: A B C
Con 2: D E F
```

User nhìn 2 con: không biết con nào mạnh hơn. *"Yếu chỉ vì 1 cái skin thôi thì bạn không biết được."*

Hệ quả:
- Offer pack bán con mới → user không biết có nên mua → không mua.
- User chỉ chọn con "trông đẹp" → bias visual, không bias gameplay.
- Designer phải explicit explain → fail communication via UI.

### Pattern Bridging (Tốt)

```
Con 1: A B C
Con 2: B C D
Con 3: A C D
Con 4: A B D
```

Overlap skills: B, C đều xuất hiện ở nhiều con → user dùng B, C làm baseline.

> *"Tính chất bắt cầu chỉ còn lại là C và D. Bây giờ khi các bạn đã nhìn thấy C và D yếu hơn rồi thì các bạn sẽ lấy cái đấy là cơ sở so sánh tiếp cho cái đống đằng sau."*

User loại dần:
1. Compare con 1 với con 2 (chung B,C) → khác biệt ở A vs D → quyết định A vs D.
2. Compare con 2 với con 3 (chung C,D) → khác biệt ở B vs A.
3. Loại dần.

Tính bắc cầu giúp user xếp hạng skill (A > B > C > D) chỉ qua compare local. Quyết định mua nhanh.

## Pattern A+ (Tối Ưu) — Same Skill Set, Stat Khác

> *"Con kia là 30% kích cỡ tóm lại là đánh 3 phát đều 1 phát. Con này cũng thế nhưng mà 50% có nghĩa là 1 mít 1 được. Xong chưa? Dễ à? Có đồng nào nghĩ ra quả skin 100% như tựa A không?"*

Pattern A+:
- Con A: skill set X, proc rate 30%.
- Con A+: skill set X, proc rate 50%.
- Con A++: skill set X, proc rate 70%.

User chỉ cần nhìn **1 con số** (proc rate) → quyết định ngay. Không cần parse skill description.

### Lợi Thế Cho Art

> *"Đấy nó làm như thế này tối nhất nó vừa đỡ câu cho các bạn nhé... Thậm chí các bạn vẽ cái icon skin này nó cũng sướng lắm. Hình bên trong nó giống nhau khác nhau một cái vảnh bên ngoài là ok rồi. Công sức các bạn làm giảm rất nhiều."*

Art workload: vẽ 1 base + 3 variant viền. Vs vẽ 4 hoàn toàn khác → giảm 75% asset time.

### Lợi Thế Cho User

- Quyết định nhanh (1 con số).
- Tiers rõ ràng (legendary > epic > rare).
- IAP convert cao (user biết upgrade lên A+ là worth tiền).

## Anti-Pattern: Skill Khác Quá Nhiều

> *"Bây giờ ông nhìn 1 cái game 1 cái con skin mà ABC xong con kia là DEF, thì tóm lại là nó yếu là vì cái bộ skin của nó hay nó yếu chỉ vì 1 cái skin thôi thì bạn không biết được. Giống như VTEC ấy — làm 1 cái dấu khác thôi, game khác có thể so sánh."*

VTEC reference: cùng 1 brand xe (Honda) nhưng tên model khác → user không so sánh dễ. Game tương tự — đẩy quá nhiều khác biệt → user không build mental model.

## Khi Nào Disjoint Có Lý Do

Disjoint OK khi:
- **Genre meta** = sưu tầm (Hearthstone collectors) — user chấp nhận parse từng card.
- **High skill ceiling** (esports) — user invest time để học từng nhân vật.
- **Class system** (RPG MMO) — class disjoint by design, user pick path.

Cho game **mass-market casual**: luôn dùng bridging hoặc A+. Disjoint kill conversion.

## Reset/Refund Resource

Một cách dung hoà giữa disjoint và bridging: cho user **trả lại tài nguyên** khi nâng cấp con khác.

Pattern (Acero của HB):
- Slot system thay vì hero-bound stat.
- User nâng cấp slot lên level 9 → bất kỳ áo nào mua sau cũng auto level 9.
- *"Khỏi cần phải trả lại. Đỗ cơ chế trừng phạt cũng như thế là sướng hơn."*

User không bị punish khi đổi build → có thể experiment → giảm decision regret. Xem [[slot-locked-upgrade]] cho deep-dive.

## Liên Hệ Wiki

[[material-count-decision-paralysis]] cho cùng logic ở material variety. [[ux-3-criteria]] tiêu chí 3 (giảm quyết định) — bridging chính là pattern giảm quyết định mua. [[clash-royale-percent-stat-display]] cho stat display pattern (base × % per level) đồng tinh thần A+ pattern. [[rpg-unit-weakness-principle]] cho weakness design — không phải mọi con strong ở mọi hệ, phải có C/B rating somewhere → bridging với weakness anchor.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Skin Variety — ABC/BCD/ACD Bridging vs ABC/DEF"
