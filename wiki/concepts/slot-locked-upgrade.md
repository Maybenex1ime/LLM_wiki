---
title: "Slot-Locked Upgrade — Level Gắn Slot Không Gắn Con"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, equipment, upgrade-system, refund]
aliases: [slot-locked, slot upgrade, level gắn slot, refund-free upgrade]
status: draft
related:
  - "[[skin-bridging-comparison]]"
  - "[[match3-player-archetypes]]"
  - "[[ux-3-criteria]]"
  - "[[file-y-do-design-intent]]"
summary: "Trong equipment system, upgrade gắn vào slot (không gắn con/áo). User nâng slot 1 lên level 9 → bất kỳ áo nào mua sau cũng auto level 9. Phá cơ chế trừng phạt khi swap → user thoải mái experiment, không tiếc tài nguyên đã invest."
---

## Định Nghĩa

Slot-Locked Upgrade = pattern equipment system trong đó level/stat upgrade gắn với **vị trí (slot)** trên nhân vật, không gắn với **cái áo cụ thể**.

Ví dụ con Acero của HB (Vũ kể):
- Slot vị trí "áo giáp" có level 9.
- User mua áo giáp mới (rare hơn) → áo mới auto level 9 (cùng slot, cùng level).
- Không cần trả lại tài nguyên cũ, không lose progress.

## Đối Lập: Equipment-Bound Upgrade

Pattern thông thường: level gắn với **cái áo** cụ thể.

- User nâng áo basic level 9 → tiêu nhiều material.
- Mua áo rare mới → áo rare ở level 1.
- Muốn dùng áo rare → phải nâng lại từ level 1 → tiếc tài nguyên đã invest vào áo basic.

User behavior: *"Khởi đầu trận nó hay dí dòng mấy cái đấy. Tiết kiệm tiền để thằng Legend."* User không dám nâng cấp các con không legendary vì sợ waste.

## So Sánh

| Aspect | Equipment-Bound | Slot-Locked |
|--------|-----------------|-------------|
| Khi swap áo | Mất level, phải nâng lại | Giữ nguyên level |
| Tâm lý user | Tiếc, dí dòng, holding tài nguyên | Thoải mái experiment |
| Khi acquire item mới | Hesitate, weigh cost | Tap-and-go |
| Habit formation | Phá (mỗi swap = decision) | Hỗ trợ (swap = free) |
| IAP/IAA flow | Chậm (user save tài nguyên) | Nhanh (user chi tiêu liên tục) |

> *"Đỗ cơ chế trừng phạt cũng như thế là sướng hơn. Nó gắn với con tướng luôn. Nó gắn với cả cái slot, cái áo, cái quần. Nâng cấp bao nhiêu thì nó ở nâng cấp đấy."*

## Tâm Lý Skill-Player

Slot-locked đặc biệt phù hợp với **skill-driven user** (xem [[match3-player-archetypes]]). Đặc tính:

- Giữ tiền cho legendary, không nâng con thường.
- Chỉ nâng con khi bàn khó.
- Sẵn sàng swap deck/build nếu phù hợp.

Equipment-bound punish behavior này (nâng con thường thì lose tiền khi có legendary). Slot-locked support: user nâng slot → giá trị giữ vĩnh viễn → comfort nâng sớm.

> *"Đấy là cái tâm lý của những ông chơi theo kiểu dạng là xác định là chơi kỹ thuật đấy. Từ lúc đầu có rất nhiều tiền nhưng mà không dám nâng con nào hết. Cứ giữ lại. Đến bàn nào mà khó quá thì chọn cái con khỏe nhất nâng lên tí cho nó vừa đủ khoa xong thì thôi."*

## Implementation Notes

Khi build slot-locked system:
- **Schema**: hero có N slots (helmet, armor, weapon, boots). Mỗi slot có level + stat. Equipment instance chỉ reference cosmetic + multiplier.
- **Upgrade UI**: cho user upgrade slot, không upgrade equipment.
- **Cosmetic swap**: drag equipment vào slot → swap free, không trigger upgrade flow.
- **Display**: hero card show slot levels, không show per-item levels.

## Khi Skip Pattern

Slot-locked không phù hợp khi:
- **Equipment có unique passive** — áo rare có ability đặc biệt → đặc tính gắn equipment, không gắn slot. Pattern slot-locked làm mất feel rare.
- **Crafting/forging game** — gameplay là craft + upgrade item từng cái → user expect item-bound progression.
- **Hardcore RPG** với deep gear (Diablo-like) — user invest vào từng món gear, expect lose progress khi swap.

## Cross-Pattern Examples

| Game | Pattern | Outcome |
|------|---------|---------|
| Diablo / Path of Exile | Equipment-bound | Hardcore, deep gear meta |
| Acero (HB) | Slot-locked | Casual-friendly, fast iteration |
| Genshin Impact | Hybrid (artifact-bound for slot, hero-bound for char) | Compromise |
| Clash Royale | Card-bound (no slot) | Different model entirely |

## Refund Mechanic

Một số game implement **refund** thay cho slot-locked:
- User nâng áo basic level 9.
- Khi swap áo rare → trả lại 80% tài nguyên đã invest.
- User chấp nhận lose 20% as friction.

Trade-off: refund đơn giản hơn slot rebuild, nhưng vẫn có lose → user vẫn tiếc. Slot-locked > refund cho casual UX.

## Liên Hệ Wiki

[[skin-bridging-comparison]] cho cùng logic UX comfort (giảm decision regret). [[match3-player-archetypes]] cho skill-player tâm lý hold tài nguyên. [[ux-3-criteria]] tiêu chí 3 — slot-locked giảm decision count per upgrade. [[file-y-do-design-intent]] — design intent của slot-locked phải document, không phải config invisible.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Resource Refund — Slot-Locked Upgrade"
