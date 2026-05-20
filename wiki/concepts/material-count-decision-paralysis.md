---
title: "Material Count — Quá Nhiều Loại Gây Decision Paralysis"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, economy, resource-design]
aliases: [material count, số loại tài nguyên, decision paralysis, 2 vs 4 material]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[economy-progression-designer]]"
  - "[[feeling-of-assets]]"
  - "[[skin-bridging-comparison]]"
summary: "Game design hay làm nhiều loại material để 'rich.' Sai. 2 loại = user tap-tap-hold habit-driven. 4 loại = decision paralysis, dừng tay, tính toán mệt. Quy tắc: ưu tiên simple resource pool, chỉ thêm khi có lý do bóng tách (rare boss material, faction-locked etc)."
---

## Định Nghĩa

Material count = số loại tài nguyên upgrade cần dùng đồng thời cho 1 hành động (nâng cấp nhân vật, craft item).

Vũ chỉ ra anti-pattern phổ biến: GD đưa 4+ loại material → user bị decision paralysis → kill habit formation.

> *"Cha mẹ bây giờ sao không nhiều thế? 2 cái được không, có đến mức độ cần phải nhiều đến 4 cái?"*

## So Sánh 2 vs 4 Material

### 2 Material — Habit-Driven

User flow:
> *"Có 1 con legendary, có 1 lượng tài nguyên nhất định. Mình cứ tác thậm chí là tệ hết là hold cho tới khi hết tiền. Và sau đó từ con đấy xuống đến con thứ 2 là con epic. Mình lại làm cái việc đó tiếp tục."*

Pattern: tap-tap-hold cho đến khi hết tài nguyên → switch sang con tiếp theo. Không cần tính toán → habit-driven → repetition cao.

### 4 Material — Decision Paralysis

User phải:
- So 4 con số (tài nguyên A, B, C, D).
- So nhu cầu của 5+ con nhân vật.
- So priority: nâng legendary trước hay rare?
- Khi material mix-match (con X dùng A+B, con Y dùng C+D), càng khó.

> *"Càng suy nghĩ càng tính toán nhiều thì nó càng khó tạo thành thái quen. Dừng lại nhiều hơn."*

Hậu quả:
- User dừng tay giữa session → engagement drop.
- User cần guide ngoài game (YouTube, wiki) → cho thấy UX fail.
- IAP convert thấp — user không quyết định mua resource pack nào.

## Vì Sao GD Thường Sai

> *"Có một cái tệ của GoWinDesign trong cái đoạn này. Các bạn rất thích làm những cái lượng thú, các bạn rất thích những cái skill kiểu khác nhau rõ ràng."*

GD nghĩ:
- 4 loại = "phong phú" = "hay" = "thử thách."
- 4 loại tạo "depth" cho economy.
- User thích thinking puzzle.

Thực tế:
- User chỉ thích thinking puzzle ở **gameplay layer** (combat, level solving).
- User KHÔNG thích thinking ở **meta layer** (upgrade, craft).
- 4 loại "phong phú" giai đoạn đầu — sau đó kill habit → drop retention D7+.

> *"Thực sự việc đấy nó khiến cho user có thể cảm thấy thích thú ở giai đoạn đầu. Nhưng việc hiểu được, dùng được nó sẽ rất khó. Thậm chí là so sánh nó còn khó hơn."*

## Quy Tắc Quyết Định

| Số material | Khi Dùng |
|-------------|----------|
| **1** | Hyper-casual, single currency (coin) |
| **2** | Default cho casual/mid-core (soft + hard currency) |
| **3** | Cần khi có economy split (gold + gem + faction token, mỗi loại có nguồn riêng) |
| **4+** | Chỉ khi có lý do design rõ rệt (đa hệ class, raid-locked material) |

Test: nếu user không thể giải thích "tài nguyên này dùng để làm gì" trong 1 câu → quá phức tạp.

## Material Mix-Match Anti-Pattern

Tệ hơn 4 loại đơn lẻ: material mix-match.

Ví dụ: con A cần material 1+2, con B cần 3+4, con C cần 1+3.

User phải:
- Nâng con A → tiêu material 1+2.
- Sau đó nhận đầu cờ nâng con C → cần material 1 nhưng đã hết.
- Tính ngược: "nếu lúc nãy không nâng con A thì giờ nâng được con C."

Decision paralysis cấp 2. *"Mệt quá thì cái đấy bạn thử xem lại xem liệu có nhiều tài nguyên như thế có cần thiết hay không."*

## Lien Hệ Với [[skin-bridging-comparison]]

Same logic cho skin variety: 5 con với skin disjoint (ABC vs DEF) → không so sánh được. 5 con với skin bridging (ABC/BCD/ACD) → user so sánh được, decision dễ. Material count cũng vậy — overlap đủ để bridging.

## Khi Nào Multi-Material Đáng Cost

Multi-material defensible khi:
- **Faction-locked resource** — material gắn với specific class/faction.
- **Time-gated resource** — material chỉ drop từ weekly raid → tạo retention loop.
- **Trade-able resource** — user trade material giữa nhau (social layer).
- **Skill tree branching** — material xác định build (path A vs path B).

Tất cả các case này: material count tăng ALONG WITH economy depth. Không phải tăng để "phong phú."

## Liên Hệ Wiki

[[ux-3-criteria]] tiêu chí 3 (giảm lượng quyết định) trực tiếp áp dụng. [[economy-progression-designer]] (skill) cho framework economy. [[feeling-of-assets]] cho cảm xúc tài sản — nhiều material = nhiều tài sản nhưng nếu user không phân biệt được → tài sản cảm giác hỗn loạn. [[skin-bridging-comparison]] cho cùng logic ở skin/skill design.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Material Variety — Quá Nhiều Loại Tạo Decision Paralysis"
