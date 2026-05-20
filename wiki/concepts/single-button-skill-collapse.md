---
title: "Single-Button Skill Collapse — Negabon vs Pokemon"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, ui, combat-design, skill-design, simplification]
aliases: [single-button skill, Negabon attack, collapse skill flow, 1-tap skill]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[hiep-iec]]"
  - "[[mobile-vs-pc-console-skill]]"
summary: "Negabon (Hiệp) cải tiến UX combat của Pokemon original: thay vì menu skill → chọn target → bấm cast (3+ taps), gộp thành 1-tap trên thanh phong độ. Tap thanh giữa = skill, tap thanh bên = đánh thường. User mất kỹ thuật tay nhưng cảm xúc 'perfect timing' thay thế."
---

## Định Nghĩa

Single-Button Skill Collapse = pattern UX gộp nhiều tap thành 1 tap cho combat input. Skill và attack chia qua **vùng tap trong cùng 1 element** thay vì 2 nút riêng.

Vũ cite case Negabon của Hiệp như ví dụ tốt:

> *"Cái con Negabon của anh Hiệp này. Là cái lúc giai đoạn đầu ấy. Anh ấy đưa ra tôi một cái cây xe ấy để tôi đưa về hướng dối với công chế ấy. Đó là tap vào cái thanh phong độ để nó bắn ra bằng cái skill của bản chưởng ấy. Tôi rất là thích."*

## So Sánh Với Pokemon Original

Pokemon bản gốc (Game Boy / DS):

| Step | Action | Tap Count |
|------|--------|-----------|
| 1 | Mở menu Battle | 1 |
| 2 | Chọn skill từ list | 1 |
| 3 | Chọn target | 1 |
| 4 | Confirm | 1 |
| **Total** | | **4 taps** |

Plus optional: đổi nhân vật (thêm 2-3 taps).

> *"Nếu mà ai đã từng chơi Pokemon bản gốc ấy, thì mọi người thấy là để con nhân vật ra được một con skill ấy, nó rất nhiều thao tác."*

## Negabon Collapse

Negabon's mechanism:

| Element | Position | Action | Result |
|---------|----------|--------|--------|
| Thanh phong độ | Trên màn hình | (Auto-update theo time) | Stat hiển thị |
| Thanh giữa (vàng/xanh) | Bên dưới phong độ | Tap | Skill phát + 30% damage |
| Thanh bên cạnh | Bên cạnh thanh giữa | Tap | Đánh thường |

User chỉ cần: nhăm mắt vào 1 region → tap đúng zone → output là skill hoặc attack tùy zone.

> *"Bằng một chỉ duy nhất một nút, tức là nút Attack cũng chính là nút chọn skill luôn. Bởi vì cái skill nó sẽ nằm trên thanh ấy luôn. Đánh vào cái thanh giữa thì nó ra skill, còn nếu mà đánh vào cái thanh màu vàng vàng thanh xanh bên cạnh, phần thanh màu vàng thanh xanh, thì nó chỉ ra đánh thường thôi."*

Tap count: **1**. Skill flow rút từ 4 taps → 1 tap.

## Trade-Off

Mất:
- **Granular control** — không chọn skill cụ thể từ pool nhiều skill (giả định only 1 active skill).
- **Tactical depth** — Pokemon original cho user pick skill phù hợp situation.
- **Strategic complexity** — không có "long-term planning" trong skill choice.

Được:
- **Habit-driven combat** — user tap-tap-tap, không suy nghĩ skill choice.
- **Flow state** — focus on timing thanh phong độ, không break flow để chọn menu.
- **Mobile-friendly** — phù hợp casual mobile attention span.

> *"Khiến cho user nó rất dễ hiểu. Và từ đấy cái việc là user sẽ không để ý đến phần phía trên luôn, chỉ tập trung nhăm nhăm đánh vào cái thanh này."*

User mất kỹ thuật tay (chọn skill), nhận lại **cảm xúc timing perfect** (chờ phong độ đầy → tap đúng lúc → 30% bonus).

## Khi Nào Pattern Phù Hợp

- **Mobile game casual / mid-core** — touch input, attention span ngắn.
- **Auto-battle với skill cast manual** — gameplay cho phép user focus 1 skill.
- **Hyper / hybrid casual** — single mechanic dominant.

Không phù hợp:
- **Hardcore strategy** (XCOM, Civilization) — skill choice IS gameplay.
- **MOBA** (Clash Royale, Mobile Legends) — multiple skills phải accessible.
- **MMO RPG** với deep skill rotation — pattern này too shallow.

## Generalization: Zone-Based Tap

Pattern Negabon là special case của zone-based input. Generalize:
- 1 UI element → multiple regions → each region = different action.
- User memorize position → no menu cost.
- Visual cue (màu, animation) report current state.

Ví dụ khác:
- **Brawl Stars** — tap & hold để aim, release để fire. 2 actions trong 1 gesture.
- **Match-3** — tap select, swipe execute. 2 actions, single sequence.
- **Idle game** — long-press accelerate, tap collect. Zone gesture.

## Liên Hệ Wiki

[[ux-3-criteria]] tiêu chí 1 (giảm số bước) — Negabon là minimum case. [[hiep-iec]] cho profile of Hiệp + Negabon project. [[mobile-vs-pc-console-skill]] cho context: mobile cần dung sai input, tap zone-based là pattern tận dụng dung sai.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Negabon (Hiệp) — Single-Button Skill"
