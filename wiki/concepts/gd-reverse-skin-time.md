---
title: "GD Reverse — Fix Skin Time Trước, Design Within"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-2-animation]]"
date_added: 2026-05-20
tags: [concept, animation, balance-design, methodology, gd-craft]
aliases: [GD reverse, fix skin time, design within time, cân bằng từ không cân bằng]
status: draft
related:
  - "[[balance-scale]]"
  - "[[animation-brief-essentials]]"
  - "[[cast-time-cao-bang-vs-per-con]]"
summary: "Tư duy ngược chiều: thay vì design action rồi tính time, fix time trước (1s cast) → tính lượng action có thể nhồi trong time đó → cân bằng theo số học. Kết quả thực tế = lý thuyết. Vũ reference: 'nghĩ từ không cân bằng đi xuống.'"
---

## Định Nghĩa

GD Reverse Skin Time = methodology design ngược chiều thông thường:

**Pattern thông thường (Wrong)**:
1. Design action (skill, attack, ability).
2. Animator vẽ → tính time.
3. Code apply time → balance theo time đó.
4. → Time variant per skin, balance khó.

**Pattern Reverse (Right)**:
1. **Fix time** (e.g., 1s cast cho mọi skill).
2. Tính lượng action có thể nhồi trong 1s.
3. **Cân bằng** dựa trên số học (DPS = damage/time).
4. Animator phải fit anim vào 1s window.
5. → Time consistent, balance accurate.

> *"Tôi đã fix cái skin này trong khoảng gian bao lâu, và bây giờ tôi nghĩ xem nên làm gì trong khoảng gian đấy. Tức là nghĩ từ không cân bằng đi xuống."*

## 3 Bước Reverse

### Bước 1 — Chốt Time Fix

Define đơn vị time chuẩn cho hệ skill:
- **Cast time** = 1s cho mọi skill chính.
- **Attack basic** = 0.5s.
- **Skill ulti** = 2s.
- **Hit reaction** = 0.4s.

Fix Day 1, không tweak sau khi anim done.

### Bước 2 — Tính Action Trong Window

Trong 1s window có thể nhồi:
- Animation (12-24 frames at 24 FPS).
- Visual effect (start, mid, end keyframes).
- Damage application timing (when to apply).
- Sound effect cues.

Map từng element vào time fragment trong window:
```
0.0s: cast start, anim begin
0.3s: charge visual (mid keyframe)
0.6s: projectile spawn, damage applied
1.0s: anim end, return to idle
```

### Bước 3 — Cân Bằng Số Học

Now DPS = damage / cast_time:
- Skill A: 1000 damage / 1.0s = 1000 DPS.
- Skill B: 1500 damage / 1.5s = 1000 DPS.
- → Equal in math, anim cùng time window.

Balance accurate vì time fixed across skills.

## Lợi Pattern Reverse

> *"Lợi ích: Skin không phải scale ngắn/dài → không trông 'vèo vèo' hay 'múa quá.' Project time và cast time match với calculation. Result thực tế = lý thuyết."*

| Lợi | Ngược (Pattern Wrong) |
|-----|------------------------|
| Time consistent | Time variant per skin |
| Anim fit time | Time fit anim → tweak DPS messy |
| Balance accurate | Theory ≠ practice |
| Animator constraint clear | Animator free → designer lo balance |

## Liên Quan Bài Cân Bằng Buổi 1

Vũ nhắc lại bài cân bằng từ Buổi 1:

> *"Các bạn phải để ý vấn đề cân bằng ngay từ đầu."*

Reverse pattern implements directly — balance từ Day 1 trong animation brief, không phải post-hoc fix.

## Anti-Pattern Khi Skip Reverse

Designer skip step 1 (fix time):
- Animator vẽ skill A trong 0.8s, skill B trong 1.3s.
- Balance team tính DPS:
  - Skill A: 800 damage / 0.8s = 1000 DPS.
  - Skill B: 1200 damage / 1.3s = 923 DPS.
- → Theory says equal, practice says A wins.
- Fix attempt: tweak damage → tweak again → cycle.

Cycle tốn:
- Animation rework (time stretch / squeeze).
- Code rework (per-skill timing).
- Balance rework (numbers chase animation).

Reverse từ Day 1 = avoid cycle.

## Khi Pattern Reverse Không Phù Hợp

- **Fighting game** với skill personality (slow uppercut vs quick jab) — time per skill quan trọng feel.
- **Visual novel** với cutscene timing — story-driven, không gameplay timing.
- **Hand-crafted boss fight** — each ability designed individually.

Phù hợp cho:
- **Auto-battle RPG**.
- **Strategy game cào bằng**.
- **Tower defense**.
- **Mid-core mobile RPG**.

## Concrete Example

### Game RPG Battle với 6 Skill Per Hero

**Wrong way**:
1. Animator vẽ skill 1: 0.7s.
2. Animator vẽ skill 2: 1.2s.
3. ... skill 6: 0.9s.
4. Designer tính DPS per skill — variant.
5. Hero balance: hero A có 6 skill DPS [1000, 800, 900, 1100, 950, 1050]. Plus skill 2 nó 1.2s slow, kém play.
6. Iterate damage → đụng đến anim.

**Right way (Reverse)**:
1. Designer fix: mọi skill = 1.0s cast.
2. Animator vẽ skill 1, 2, 3, ... fit 1.0s exact.
3. Designer balance damage: skill 1 = 800, skill 2 = 1200, ... reflective of intended power.
4. Test: DPS = damage / 1s = damage directly. Easy.

## Document For Animator

Brief format:
```
SKILL TIMING (Fixed Day 1):
- Basic attack: 0.5s
- Skill 1-5 (active): 1.0s
- Ultimate: 2.0s
- Hit reaction: 0.4s
- Idle loop: 2.0s

CONSTRAINT: All anim must fit window exact. No tweaking timing later.
DAMAGE APPLICATION: At skill cast time × 0.6 (e.g., 0.6s for 1.0s skill)
```

## Liên Hệ Wiki

[[balance-scale]] cho balance framework — reverse implement balance accurate. [[animation-brief-essentials]] cho overall brief — reverse là sub-pattern trong brief. [[cast-time-cao-bang-vs-per-con]] — reverse là cách enforce cào bằng.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-2-animation.md` § "GD Reverse — Fix Skin Time Trước"
