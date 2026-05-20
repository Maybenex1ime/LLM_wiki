---
title: "Blend Animation Pattern — Combo & Wall Collision"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-2-animation]]"
date_added: 2026-05-20
tags: [concept, animation, transition, combo, blend, polish]
aliases: [blend animation, anim transition, combo blend, wall collision blend]
status: draft
related:
  - "[[animation-brief-essentials]]"
  - "[[hit-reaction-3-approaches]]"
summary: "Blend = fade-out anim 1 + fade-in anim 2 trong 0.1-0.2s. Tránh anti-pattern vẽ tất cả tổ hợp transition (N² files). 2 use cases: combo chain (đá cao → đá thấp không về idle) và wall collision (run → blend idle khi va tường). Brief: artist vẽ anim độc lập, code làm blend."
---

## Định Nghĩa

Blend Animation = transition technique giữa 2 animation states thông qua fade-out + fade-in trong 0.1-0.2s.

Khác với hard cut (instant switch) — blend smoothes visual.

Khác với connecting anim (vẽ frames between A và B) — blend là code-driven, không cần artist vẽ extra frames.

> *"Blend là một cái khoảng hiệu ứng để tiếp nối — đây là anim 1, đây là anim 2. Bình thường nó sẽ về idle sau diễn hay. Nhưng làm mờ trong đoạn này và nó đi sang anim 2 ngay lập tức."*

## Use Case 1 — Combo Chain

Game tiết tấu nhanh (song đấu) cần animation **chuyển trực tiếp** không về idle:
- **Đá cao → đá thấp** không về idle giữa.
- **Đá cao → skin 2** không về idle.
- **Punch → Kick → Skill** continuous flow.

### Anti-Pattern: Vẽ Tất Cả Tổ Hợp

Bùng nổ tổ hợp:
- Đá cao → idle, đá thấp → idle, đấm → idle.
- Đá cao → đá thấp, đá cao → đấm, đá thấp → đá cao...
- N action × N transition = **N² anim files**. Không quản lý được.

3 actions = 9 transitions. 5 actions = 25 transitions. Không scale.

### Solution: Blend Hiệu Ứng

Code:
```pseudo
on_combo_chain(unit, action1, action2):
  unit.fade_out(action1, duration=0.1)
  unit.fade_in(action2, duration=0.1)
  // anim 1 và anim 2 đều là files độc lập
```

Artist vẽ:
- Anim 1: đá cao (full).
- Anim 2: đá thấp (full).
- → 2 files thay vì 1 file transition + 2 base.

Yêu cầu artist:
- Vẽ anim độc lập (anim 1 + anim 2).
- Define "đoạn nào cần blend lên hay không" trong brief.

## Use Case 2 — Wall Collision

Tình huống: nhân vật chạy → va tường → vẫn cứ chạy "dũi thẳng" vào tường. Đa phần game accept hành vi này.

### Solution 1 — Kệ (Accept)

> *"Nếu chấp nhận thì thôi nha ông bạn nha."*

Phù hợp cho game không yêu cầu polish cao.

### Solution 2 — Anim Có Tương Tác (Blend)

- Khi va tường → sinh ra anim transition.
- **Blend** từ "run" sang "idle" để cử động không bị cứng.

> *"Nó blend lại với cả idle. Nó blend idle để cho phạm vi của hành động nó nhẹ nhàng lại."*

Phù hợp polish cao, đặc biệt 3D adventure / open world.

Code:
```pseudo
on_wall_collision(unit):
  unit.fade_out("run", duration=0.2)
  unit.fade_in("idle", duration=0.2)
  // smoothly transition instead of frozen run
```

## Blend Duration Guide

| Duration | Use Case |
|----------|----------|
| **0.05s** | Snappy / fighting game | Quick reaction |
| **0.1s** | Default combo / general | Standard polish |
| **0.2s** | Smooth transition (wall, idle return) | Cinematic |
| **0.3s+** | Cutscene / slow | Hide cut |

## Implementation In Engine

### Unity

```csharp
Animator.CrossFade(stateName, normalizedTransitionTime: 0.1f);
```

### Unreal

```cpp
PlayAnimation(NewAnim, BlendTime=0.1f);
```

### Custom Engine

```pseudo
blend_animation(current_anim, new_anim, duration):
  for t in 0..duration:
    weight = t / duration
    render(current_anim, opacity=1-weight) + render(new_anim, opacity=weight)
```

## Brief For Animator

Document trong animation brief:
- **Combo entries** — list các action có thể combo (e.g., punch → kick).
- **Blend duration default** — 0.1s for combat, 0.2s for movement.
- **No-blend rules** — actions phải về idle giữa (ví dụ: hit reaction phải finish trước action mới).
- **Combo blend exception** — combo có thể bypass blend nếu muốn snap feeling.

Sample brief:
```
ACTION TRANSITIONS:
- punch → kick: blend 0.1s
- punch → block: blend 0.05s (snappy)
- attack → hit_reaction: NO BLEND (instant)
- hit_reaction → idle: blend 0.2s
- run → wall_idle: blend 0.2s
```

## Anti-Pattern

- **Hard cut everywhere** — visual jarring, low polish feel.
- **Blend quá lâu** (>0.3s combat) — slow combat feel.
- **Vẽ transition anim** thay vì code blend — N² file explosion.
- **Blend without docs** — code random switch, debugging khó.
- **Blend cho mọi transition** — performance cost, lose snap feel where needed.

## Liên Hệ Wiki

[[animation-brief-essentials]] cho brief tổng quát — blend là phần trong brief. [[hit-reaction-3-approaches]] cho cách 3 (anim kêu lại) — speed-up + blend OK cùng nhau.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-2-animation.md` § "Va Vào Tương Tác — Wall Collision", "Combo Animation — Blend Giữa Anim 1 → Anim 2"
