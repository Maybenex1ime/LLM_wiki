---
title: "Multi-Start Design — 3 Use Cases, 3 Risks, Element Regret"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, onboarding, ftue, multi-start, role-design]
aliases: [multi-start, đa khởi đầu, chọn role đầu game, class selection, customize start]
status: draft
related:
  - "[[ftue-curve]]"
  - "[[user-segmentation-3-axes]]"
  - "[[rpg-unit-weakness-principle]]"
  - "[[defending-design-decisions]]"
summary: "Multi-start = chọn class/role đầu game. 3 use cases: mạnh đầu/yếu đầu/phụ trợ. 3 risks: non-linear progression, balance mess, no restart path. Anti-pattern: element rock-paper-scissors tạo regret. Fix: encounter design bám lựa chọn để user luôn cảm thấy 'may quá chọn đúng'."
---

## Định Nghĩa

Multi-Start = onboarding pattern cho user chọn **role/class/nhân vật khởi đầu** ảnh hưởng gameplay. Khác customize-start (chọn nam/nữ, skin — cosmetic only).

> *"Trong multi-start thì nó có hai loại. Một là em chọn những các cái role nhất định. Hoặc là em tự build — em có tổng 100 điểm, em vào em tự bấm."*

Khi cần:
- **Game phân role** (Empire/Rise of Kingdom — chọn quốc gia).
- **MMO class** (RPG team-based với rotation system).
- **Single-player branching** (Diablo/Pokemon — chọn nhân vật đầu).

Không cần:
- **Hành trình độc lập** không tương tác giữa user → multi-start "hơi quá sức."
- **Game casual** (Match-3, Idle) → no role → no multi-start.

## 3 Use Cases Per Role

Hiệp & Đồng (học viên) muốn đưa multi-start vào game của họ. Vũ phân tích 3 archetype role:

| # | Role Pattern | Tâm lý User | % User Chọn |
|---|--------------|-------------|--------------|
| 1 | **Mạnh đầu yếu sau** (Early Power) | Sướng được ngày nào là sướng | Đa số |
| 2 | **Yếu đầu mạnh sau** (Late Bloomer) | Khổ trước sướng sâu mới giàu | Trung bình — risk fall-off |
| 3 | **Phụ Trợ** (Support) | Buff cho team, không chém | Rất ít |

> *"Đa phần các bên sẽ chọn cái loại đầu — sướng được ngày nào là sướng. Khi nào hết sướng thì ta bỏ."*

> *"Nhiều ông là không trụ được. Bởi vì bị thọt ra."* — về Pattern 2 (yếu đầu).

> *"Ta thích người ta là phải lên, tướng dẫn đầu lên để chém giết."* — vì sao support roles unpopular.

Hệ quả design: design 3 role nhưng **expect 80%+ user chọn Pattern 1**. Balance per role là khó vì user distribution bias.

## 3 Risks Của Multi-Start

### Risk 1 — Non-Linear Progression

> *"Multi-start nó sẽ không tuyến tính với tất cả các người chơi... Có người nó sẽ tốt hơn mặt bằng chung thị trường, và có người sẽ bị yếu hơn mặt bằng chung."*

User class yếu → cảm thấy bị punish → quit trước **monetization threshold** (level user thường in-app đầu tiên) → mất doanh thu.

### Risk 2 — Balance Mess

Trong game đế chế (Rise of Kingdom):

> *"Tóm lại nó sẽ gom hết vào một nùi những cái bọn khỏe."*

Toàn bộ user dồn vào 1 class → 2 class còn lại die. YouTube reviewer phải explicit hướng dẫn *"start với nation X"* → bypass tự do chọn → multi-start trở thành "fake choice."

### Risk 3 — No Restart Path

Mobile user không biết clear data:

> *"Rất nhiều user không biết clear cách. Clear data để chơi lại đâu. Họ không biết cách clear data. Và gần như là họ sẽ bị mắc định — chỉ có là xóa dữ liệu đi, tải lại một con game mới thôi."*

User stuck level 15 với class sai → uninstall thay vì restart → mất user vĩnh viễn.

## Anti-Pattern: Element Rock-Paper-Scissors → Regret

Pokemon-style 3 hệ (lửa/nước/cỏ) với khắc chế cycle:
- Lửa khắc cỏ, cỏ khắc nước, nước khắc lửa.

User chọn lửa → encounter toàn quân nước → user "may xui."

> *"Lúc đầu em chọn con lửa ở VN. Bị nó đẹp. Xong đánh, ồ chết rồi xong mình chọn sai rồi. Rồi đến con này mình sắp tắt ngay ở đây rồi gặp toàn con lửa."*

Default behavior trong open-world / random encounter:
- Encounter random theo zone.
- 33% chance gặp counter element → user cảm thấy "thiệt thòi."
- Pattern recognition slow (3-5 level) → trễ feedback fix.

### Fix: Encounter Friendly To Choice

> *"Em làm cho người chơi, em phải vẽ cho người chơi cái chiều này. Ví dụ như là chọn lửa thì gặp nước, chọn nước thì gặp hỏa. Chứ không cho người ta cái cảm giác bị thất vọng."*

User chọn lửa → đầu game gặp nước (lửa khắc nước → user thắng) → *"luôn luôn người chơi cảm thấy ôi may quá mình chọn con này."*

Pattern: encounter design **biased theo lựa chọn ban đầu** trong early game (10-15 levels đầu). Sau threshold, mở fair encounter.

Trade-off: user reset class sẽ phát hiện bias → cảm thấy "fake difficulty." Acceptable trade nếu retention > truth.

### Fix Tiếp Theo: Circular Balance Post-Checkpoint

Vũ improve solution của Hiệp:

> *"Để hết check qua một, là người tem họ sẽ có được đủ 3 cái vật liệu. Cho họ không bị hối hận. Vì họ đã chọn con này. Và cái tiếp theo đó là cho họ được trải nghiệm cái việc là họ chọn con đầu tiên — họ sẽ bị con thứ hai. Bởi vì nó là hệ thống các cơ giới nhau."*

Sau checkpoint 1, user **unlock cả 3 con** (con mạnh nhất là con đã chọn + 2 con yếu hơn vào collect). Lợi:
- No regret cho user chọn lửa/nước/cỏ.
- Circular balance: 1 ngày user thấy lửa mạnh, ngày khác thấy nước mạnh → rotation.

## Customize Start ≠ Multi-Start

| Customize Start | Multi-Start |
|-----------------|-------------|
| Cosmetic (nam/nữ, skin) | Gameplay role |
| Không ảnh hưởng balance | Ảnh hưởng balance |
| Có thể đổi bất kỳ lúc nào | Hard để đổi sau commit |
| Mở vô tư | Cần protect bằng warning |

Nhầm lẫn: 1 số GD nghĩ chọn nam/nữ = multi-start → over-engineer. Nam/nữ thật ra chỉ là customize, không cần lo về balance/restart path.

## Multi-Start Strength (Khi Đúng Dòng)

- **Curiosity** + **kỳ vọng** — *"khơi gợi cho em được một cái kỳ vọng, một cái tính tò mò."*
- **Replay value** — chơi lại với class khác.
- **Pre-existing brand habit** — nếu game theo IP Pokemon, user đã có habit "chọn 3 nhân vật đầu" → multi-start là expected, không phải friction.

Hiệp's case (Pokemon-style 3 hệ): defensible vì:
- Genre familiar.
- Balance per checkpoint planned.
- Unlock cả 3 con sau checkpoint 1.

Đồng's case (2Cơ Game kingdom với 1 → 3 hero): **risky** vì:
- Genre không có precedent multi-start.
- Hero base stat chưa ngon (anh's words).
- "Rất khó quay đầu" sau khi commit.

## Liên Hệ Wiki

[[ftue-curve]] cho FTUE design tổng quát — multi-start là 1 yếu tố của FTUE. [[user-segmentation-3-axes]] giải thích vì sao majority user chọn Pattern 1. [[rpg-unit-weakness-principle]] cho concept "every S unit phải C ở hệ khác" — element design pattern. [[defending-design-decisions]] cho framework defend khi pitch multi-start risky.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Multi-Start — 3 Use Cases & Risk"
