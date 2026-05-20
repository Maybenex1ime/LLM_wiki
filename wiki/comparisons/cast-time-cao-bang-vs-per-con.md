---
title: "Cast Time — Cào Bằng vs Per Con"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-2-animation]]"
date_added: 2026-05-20
tags: [comparison, animation, balance-design, code-design, skill-design]
aliases: [cast time cao bang, cast time per con, skill timing approach, balance vs anim time]
status: draft
related:
  - "[[animation-brief-essentials]]"
  - "[[gd-reverse-skin-time]]"
  - "[[balance-scale]]"
summary: "Approach 1 cào bằng: tất cả con dùng cùng C1 cast delay. Code đơn giản, balance dễ. Approach 2 per con: mỗi con riêng cast time. Battle RPG 6-7 skin → workload bùng nổ. Quan trọng: define từ sớm. Skip = balance lý thuyết không match thực tế."
---

## Bối Cảnh

Vũ phân biệt 2 approach xử lý skill timing trong combat animation. Liên quan trực tiếp đến balance system — chọn approach từ Day 1 ảnh hưởng workload code + balance đúng-sai-thực-tế.

> *"Cái này nó sẽ bị khác nhau và code sẽ bị đi xử lý từng việc một. Đấy là lý do vì sao mình mới nói cố gắng đẩy từ sớm nhất có thể."*

## Bảng So Sánh

| Aspect | Cào Bằng | Per Con |
|--------|----------|---------|
| **Cast time per skill** | Constant C1 cho mọi con | Khác cho mỗi con |
| **Code complexity** | Đơn giản | Cao (per-case logic) |
| **Balance dễ tính** | ✅ Số học = thực tế | ❌ Số học ≠ thực tế |
| **Asset budget** | Nhỏ (1 base timing) | Lớn (mỗi con khác) |
| **Anim workload** | Constant per skill | Bùng nổ với 6-7 skin |
| **Game feel** | Predictable, fair | Varied, characterful |
| **Phù hợp** | Strategy / RPG cào bằng | Song đấu / fighting game |

## Approach 1 — Cào Bằng

Pattern:
- **Cooldown** tính từ thời điểm 0 (lúc bấm skill).
- **Projectile** bắn ra từ thời điểm 0 + C1 (constant cast delay).
- Tất cả con dùng C1 giống nhau.

Code:
```pseudo
on_skill_cast(unit):
  wait(C1)  // cào bằng cho mọi unit
  spawn_projectile(unit.skill)
  unit.cooldown_started = now
```

→ Logic đơn giản. Skill timer = số học pure.

### Lợi

- **Balance simple**: DPS = damage / cooldown. Plug-and-play.
- **Bug-free**: ít edge case.
- **Onboarding nhanh**: dev mới hiểu trong 5 phút.
- **Đúng số học**: nếu con A "đáng lý" mạnh hơn con B 30%, thì thực tế cũng 30%.

### Bất Lợi

- **Game feel uniform**: tất cả con cast giống → không có "personality."
- **Khó differentiate animation**: anim phải fit chung 1 timing → constraint cao.

## Approach 2 — Cast Time Per Con

Pattern:
- Mỗi con animation cast time khác nhau (con A 0.8s, con B 1.2s).
- Code phải tính cast time per con khi compute DPS, projectile spawn.

Code:
```pseudo
on_skill_cast(unit):
  wait(unit.cast_time)  // per-unit
  spawn_projectile(unit.skill)
  unit.cooldown_started = now
  unit.next_cast_at = now + unit.cooldown
```

→ Tăng exception count theo số con.

### Lợi

- **Game feel rich**: con to chậm, con nhỏ nhanh → personality.
- **Animation tự do**: artist không bị fit constraint chung.
- **Tactical depth**: user chọn con cast nhanh vs damage cao.

### Bất Lợi

- **Số học ≠ thực tế**: con A theo paper mạnh hơn 30% — thực tế chỉ 10% vì cast time chậm hơn.
- **Balance khó**: phải tính DPS thực tế per con, không phải straight number.
- **Workload bùng nổ**: 6-7 skin × N skill = N×7 cast times để maintain.

> *"Cuối cùng cái kết quả cân bằng thực tế không giống với kết quả cân bằng lý thuyết của các bạn — ít nhất là về mặt số học. Mình chưa nói về fueling."*

## Quyết Định Approach

| Game Type | Recommended |
|-----------|-------------|
| **Strategy game cào bằng** (Clash Royale, RTS) | Cào bằng |
| **Auto-battle RPG** (Idle RPG) | Cào bằng |
| **Tower defense** | Cào bằng |
| **Song đấu 1v1** (Mortal Kombat, fighter) | Per Con |
| **Action combat** (Devil May Cry, Bayonetta) | Per Con |
| **MOBA** | Hybrid (per hero base + cào bằng item delay) |

## Hybrid Approach

Some games combine:
- **Base cast time per skill** (defined globally).
- **Modifier per character** (haste/slow buff).
- **Effective cast time** = base × (1 - haste%).

Pattern này khắc phục both downsides:
- Số học predictable (base + modifier).
- Game feel varied (modifier per character).

Pattern phổ biến trong gacha RPG hiện đại (Genshin, Honkai).

## Khi Late-Detect Approach 2 Là Sai

Symptom: balance team complain con A "trên paper mạnh nhưng thua trận con B."

Fix:
1. Audit cast time per con.
2. Identify outlier (con quá chậm / quá nhanh).
3. Choose:
   - **Switch sang cào bằng** (cost: redo anim).
   - **Compensate damage** (con cast chậm → damage cao hơn để equalize DPS).

Option 2 ít cost asset, but tăng complexity balance.

## Anti-Pattern: Không Define Từ Đầu

GD assume team art sẽ tự lo timing → mỗi con vẽ tự do → cast time random per con → balance theory fail.

Quote:
> *"Đấy là lý do vì sao mình mới nói cố gắng đẩy từ sớm nhất có thể."*

Define Day 1: cào bằng hay per con. Sau khi anim done, switch approach = redo all anim.

## Liên Hệ Wiki

[[animation-brief-essentials]] cho overview brief. [[gd-reverse-skin-time]] cho approach "fix time first" — implements cào bằng. [[balance-scale]] cho balance framework — approach quyết định độ accuracy của balance.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-2-animation.md` § "Cast Time & Cooldown — 2 Approach"
