---
title: "Hit Reaction — 3 Cách Xử Lý Bài Toán Dồn"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-2-animation]]"
date_added: 2026-05-20
tags: [concept, animation, combat-design, hit-reaction, block-time]
aliases: [hit reaction, ngửa người, kệ mẹ, block time, anim kêu lại, bài toán dồn]
status: draft
related:
  - "[[animation-brief-essentials]]"
  - "[[cast-time-cao-bang-vs-per-con]]"
  - "[[blend-animation-pattern]]"
summary: "Hit reaction tạo bài toán dồn: attacker hit → defender ngửa 0.4s → attacker hit tiếp → defender ngửa tiếp → vô tận. 3 cách xử lý: (1) Kệ mẹ — allow dồn, hardcore brawler; (2) Block Time — cooldown sau 1 hit, song đấu; (3) Anim Kêu Lại — speed-up attack match recovery, chiến thuật cào bằng."
---

## Định Nghĩa

Hit Reaction = animation defender phản ứng khi bị tấn công. Common forms:
- Ngửa người ra sau (~0.2s).
- Giật về idle (~0.2s).
- Total recovery: ~0.4s.

Khi attacker action ngắn hơn defender recovery → **dồn** xảy ra: attacker hit liên tiếp, defender không kịp bật lại.

## Bài Toán Dồn

> *"Trong thời gian 1.2 giây — tôi đứng nghiêm cho bạn chém hay tôi lại vã cho cái nữa? Bạn lại ngửa ra đằng sau và có nghĩa là rồn — chết toang luôn."*

Math example:
- Attacker action = 1s.
- Defender hit reaction = 0.4s.
- Tổng defender chờ trước khi đánh lại = 1.4s (ngửa + giật về + bắt đầu attack mới).
- Trong gap 0.4s đó → attacker đánh tiếp → defender ngửa tiếp → **bị dồn vô tận**.

## 2 Mode Đầu Vào

### Mode 1: Không Hit Reaction (Phần Phật Phật)

- Cả 2 không có anim bị thương.
- Cùng action attack → trade damage qua DPS.
- Không có dồn — both side attack đều.

Game ví dụ: Clash Royale, auto-battle RPG. Simple combat math.

### Mode 2: Có Hit Reaction (Ngửa Người)

- Khi bị chém → anim ngửa người.
- Game feel rich, impact rõ ràng.
- Tạo bài toán dồn cần solve.

## 3 Cách Xử Lý

### Cách 1: Kệ Mẹ

> *"Người dồn được, kẻ bị dồn không có cửa bật lại."*

- Allow dồn fully.
- Attacker spam combo, defender phải block / dodge proactively.
- Skill expression = avoid dồn ban đầu.

Phù hợp:
- **Hardcore brawler** (Tekken, Street Fighter).
- **Intentional combo system** — combo IS the gameplay.
- **PvP skill ceiling cao** — pro player avoid by spacing.

### Cách 2: Block Time

- Sau 1 hit, attacker có cooldown trước hit tiếp.
- Skill này "không block tham" (defender immune trong window cooldown).
- Defender chắc chắn có window để bật.

Pseudo timing:
- Attacker hits at t=0.
- Block window: t=0 to t=0.3s (defender immune).
- Attacker can hit again at t=0.3s+.

Phù hợp:
- **Song đấu 1v1** (anime fighter, Smash Bros).
- **Tương tác cao** — player feel responsive.
- **Game balance fairness** — không ai dominant dồn.

### Cách 3: Anim Kêu Lại (Speed-Up Attacker)

- Anim của attacker bị speed-up để match thời gian recovery của defender.
- Math: attacker action time = defender recovery time → no dồn, no block.

Pseudo:
- Defender recovery = 0.4s.
- Attacker anim = 1s normally.
- Force attacker anim → 0.4s (speed-up 2.5×).

Phù hợp:
- **Game chiến thuật, số đông, auto-battle**.
- **Cần balance đúng số học** (cào bằng đầu vào với [[cast-time-cao-bang-vs-per-con]]).
- **Calculation = thực tế**.

> *"Game chiến thuật, số đông, auto → chọn cách **Anim Kêu Lại** (block tham). Calculation = thực tế."*

## Bảng So Sánh

| Cách | Game Feel | Code Complexity | Balance Accuracy | Phù Hợp Genre |
|------|-----------|-----------------|-------------------|---------------|
| **Kệ Mẹ** | Skill ceiling cao | Simple (no block logic) | Approx (depends skill) | Brawler, Fighter |
| **Block Time** | Fair, responsive | Medium | High | Song đấu, action |
| **Anim Kêu Lại** | Uniform, cào bằng | Medium (animation rate var) | Pure number = thực tế | Strategy, Auto-battle RPG |

## Combo Skill Exception

Một số game cho phép **dồn cho combo skill có chủ ý**:
- Default: cách 2 hoặc 3 (no dồn).
- Combo skill: cách 1 (allow dồn) — designer cho phép vì combo IS the move.

Example: Bayonetta — combo punisher pattern. Default fight = balanced, combo string = dồn allowed cho show.

## Code Implementation

### Cách 1 — Kệ Mẹ

```pseudo
on_hit(defender, damage):
  defender.play_hit_reaction()
  defender.hp -= damage
  // no block logic, attacker can hit immediately again
```

### Cách 2 — Block Time

```pseudo
on_hit(defender, damage):
  defender.play_hit_reaction()
  defender.hp -= damage
  defender.invuln_until = now + 0.3
  // future attacks blocked until invuln_until
```

### Cách 3 — Anim Kêu Lại

```pseudo
on_hit(defender, damage):
  defender_recovery = 0.4
  attacker_anim_speed = defender_recovery / default_anim_time
  attacker.play_attack(speed_multiplier=attacker_anim_speed)
  defender.play_hit_reaction()
  defender.hp -= damage
```

## Brief Animation

GD phải document logic:

> *"Khi nghĩ ra anim, các bạn cần phải đưa ra cái logic cho anim đấy để code thực hiện thôi. Còn nếu không nói về logic ngã ngửa giật sau, họ sẽ không biết tính toán như thế nào."*

Brief format:
- Anim hit reaction: 0.4s.
- Block window: 0.3s (if block-time).
- Attacker anim speed: variable (if anim-kêu-lại).
- Combo override: list combo IDs that bypass block.

## Anti-Pattern

- **Skip define cách** — code default sang Kệ Mẹ → balance gãy nếu game không phải brawler.
- **Mix cách without docs** — 50% skill block-time, 50% kệ mẹ → confusion, bug.
- **Hit reaction quá dài** (>0.5s) — defender feel powerless.
- **Hit reaction quá ngắn** (<0.1s) — không có impact feel.

## Liên Hệ Wiki

[[animation-brief-essentials]] cho brief tổng quát. [[cast-time-cao-bang-vs-per-con]] cho cast time approach — hit reaction approach phải align. [[blend-animation-pattern]] cho transition giữa hit reaction → idle.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-2-animation.md` § "Hit Reaction — Bài Toán Dồn"
