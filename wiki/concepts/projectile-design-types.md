---
title: "Projectile Design — 3 Types: Cắt Ra Là Chúng, Platformer, 3D Predict"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-2-animation]]"
date_added: 2026-05-20
tags: [concept, animation, combat-design, projectile, physics]
aliases: [projectile types, cắt ra là chúng, platformer skill, 3D predict, homing missile]
status: draft
related:
  - "[[animation-brief-essentials]]"
  - "[[hit-reaction-3-approaches]]"
summary: "3 loại projectile design: (1) Cắt ra là chúng — mặc định trúng, projectile chỉ là visual (đa số game), (2) Platformer — phải chạm thật mới gây dam, (3) 3D Real-Position — bắn vào vị trí target dynamic (bay vòng rả/predict). Anti-pattern: box projectile to để fake hit — tester sẽ phát hiện."
---

## Định Nghĩa

Projectile = bullet / missile / spell visual đi từ caster đến target. Có 3 loại design theo cách compute hit:

## Type 1 — Cắt Ra Là Chúng (Default Majority)

Pattern:
- Skill bắn ra → **mặc định trúng** target.
- Projectile chỉ là **visual effect** từ A → B, không tính physics.
- Tốc độ projectile **nhanh** để khỏa lấp gap di chuyển của target.

> *"Loại 1: Logic 'Cắt Ra Là Chúng' (Đa Số). Skill bắn ra → mặc định trúng target. Bạn không cần tính physics — chỉ vẽ animation projectile đi từ vị trí A → vị trí B (target lúc bắn). Tốc độ projectile nhanh để khỏa lấp gap di chuyển của target."*

Code:
```pseudo
on_skill_cast(caster, target):
  apply_damage(target, caster.damage)  // damage applied immediately
  spawn_visual(caster.position, target.position, speed=fast)  // visual only
```

### Phù Hợp

- **Auto-battle RPG** — combat math driven, không physics.
- **Tower defense** — bullet only visual.
- **Card-based game** — projectile decorative.
- **Strategy** — units fire visually but math runs background.

### Lợi

- Code simple.
- Performance light (no per-pixel check).
- Balance predictable (always hit).

### Bất Lợi

- Less skill expression — không có dodge mechanic.
- Visual fakeness — projectile có thể "miss" pixel-wise nhưng vẫn damage.

## Type 2 — Platformer / Có Chạm

Pattern:
- Projectile có **collision box thật**.
- Phải chạm mới gây damage.
- Không chạm = miss.

Code:
```pseudo
on_skill_cast(caster, direction):
  proj = spawn_projectile(caster.position, direction, speed=medium)
  proj.on_collide = (target) -> apply_damage(target, caster.damage)
```

### Phù Hợp

- **Platformer** (Mario, Sonic).
- **Side-scrolling shooter** (Contra, Metal Slug).
- **Top-down shooter** (Hotline Miami).
- **Twin-stick shooter**.

### Lợi

- Skill expression cao (aim + dodge).
- Visual = reality.
- Replayability cao.

### Bất Lợi

- Code complex (collision detection).
- Balance khó (skill cap affects damage output).
- Mobile-unfriendly (precise aim on touch).

## Type 3 — 3D Real-Position Skill

Pattern:
- Bắn theo vị trí **thật** target.
- Target chạy đi → projectile có 2 sub-types:

### Sub-Type 3a — Bay Vòng Rả (Homing)

- Projectile có tracking AI.
- Updates direction theo target real-time.
- Like a homing missile.

```pseudo
update_projectile(proj, target):
  direction = normalize(target.position - proj.position)
  proj.velocity = direction * proj.speed
```

Phù hợp: missile RPG, magic-tracking spell.

### Sub-Type 3b — Predict Position

- Đoán vị trí target sau X giây dựa vào hướng di chuyển.
- Bắn thẳng đến vị trí đó.

```pseudo
on_skill_cast(caster, target):
  predicted_pos = target.position + target.velocity * projectile_time
  spawn_projectile(caster.position, predicted_pos, ...)
```

Phù hợp: precision shooter, snipper game, baseball-like.

### Phù Hợp Cho Cả 2

- **3D RPG** (Genshin, Honkai).
- **Action RPG** (Diablo cho some skills).
- **Tactical shooter** với projectile-based weapon.

### Lợi

- Realistic combat feel.
- Skill expression (positioning matters).

### Bất Lợi

- Complex code (3D collision + prediction).
- Performance cost.
- Test/balance khó.

## Anti-Pattern: Box Projectile To Để Fake Hit

> *"Một số GD dùng trick 'làm box projectile to hơn' → 'cảm giác chưa chạm đã gây dam.' Trường hợp nó rất là ngu ở chỗ này — kiểu cảm giác nó chưa chạm vào nó đã gây dam rồi. Tester bắt đầu kiểu âm lên."*

Pattern xấu:
- Visual projectile size = 50 pixel.
- Hitbox size = 100 pixel.
- Animation cho thấy projectile cách target 30 pixel → damage applied.

User reaction: "what? It didn't hit me visually."

Tester catch ngay → flag inconsistency → fail QA.

Fix:
- Hitbox match visual (or slightly tighter, never larger).
- Use Type 1 if simplification needed (visual decorative, damage by logic).

## Decision Framework

| Game Genre | Recommended Type |
|-----------|-------------------|
| Auto-battle RPG | Type 1 (cắt ra là chúng) |
| Card-based combat | Type 1 |
| 2D platformer | Type 2 |
| Side-scrolling shooter | Type 2 |
| Mobile arcade | Type 1 (mass) hoặc Type 2 (skill-focused) |
| 3D RPG with combat | Type 3a (homing) hoặc Type 3b (predict) |
| FPS / shooter | Type 2 (hitscan) hoặc Type 3b (predict) |

## Liên Hệ Wiki

[[animation-brief-essentials]] cho brief tổng quát — projectile type quyết định anim length. [[hit-reaction-3-approaches]] cho receiving side — hit reaction phải match projectile type.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-2-animation.md` § "Projectile Speed — Đa Phần Là 'Cắt Ra Là Chúng'"
