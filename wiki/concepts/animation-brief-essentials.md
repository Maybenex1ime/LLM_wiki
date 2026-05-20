---
title: "Animation Brief Essentials — Frame Rate, Transition, Cast Time"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-2-animation]]"
date_added: 2026-05-20
tags: [concept, animation, art, art-brief, gd-craft]
aliases: [animation brief, mô tả anim, frame rate brief, form anim biên độ]
status: draft
related:
  - "[[art-brief-3-parts]]"
  - "[[cast-time-cao-bang-vs-per-con]]"
  - "[[gd-reverse-skin-time]]"
summary: "GD mô tả 'tim rap, idle, walk' = too generic. Brief đầy đủ cần: detail per action, transition giữa anim (idle→walk→run), frame count per anim, frame rate (đặc biệt fast actions), tương tác môi trường, biên độ theo form (to/béo vs nhỏ/gầy)."
---

## Định Nghĩa

Animation Brief Essentials = các yếu tố GD phải define trong brief cho team animation. Khác với art static brief — animation có thêm dimension time.

> *"Bạn GD mô tả animation cho team art như thế nào?" Học viên trả lời: "Tim rap, idle, walk..." → quá generic.*

## 5 Elements Cần Define

### 1. Detail Per Action

Không chỉ "idle" — idle như thế nào:
- Idle với chân đứng yên + tay vung nhẹ?
- Idle với hơi thở (chest rise/fall)?
- Idle với fidget (đặt tay lên hông, look around)?

Tương tự "walk":
- Walk casual?
- Walk cautious (game stealth)?
- Walk angry?

### 2. Transition Giữa Anim

Không có anim đứng độc lập — phải nối chuỗi:
- Idle → Walk → Run → Walk → Idle.
- Idle → Attack → Idle.
- Attack → Hit (defender) → Idle.

Brief phải define **transition logic**:
- Default: về idle giữa các action.
- Combo: chuyển trực tiếp giữa action (xem [[blend-animation-pattern]]).

### 3. Frame Count Per Anim

> *"Mình hỏi các bạn có yêu cầu thời gian trong một anim trong lúc đầu không, hay chỉ mô tả nó là nhanh chậm trên đất? Đúng cách mọi người thông thường là như thế."*

Brief phải có:
- Frame count cụ thể (12 frames cho attack, 24 frames cho skill).
- Frame rate (12 FPS hoặc 24 FPS).
- Total duration (1s cho attack, 2s cho skill).

Skip → code không biết tính cast time → balance hệ thống gãy.

### 4. Frame Rate (Đặc Biệt Fast Action)

- **Idle / Walk**: 12 FPS sufficient.
- **Attack / Skill**: 24+ FPS để smooth.
- **Hit reaction**: 30 FPS để impact nặng.
- **Slow action** (sleep, eat): 6 FPS đủ.

Đầu tư FPS theo **frequency of view**:
- Anim xuất hiện nhiều → invest FPS cao.
- Anim ít xuất hiện → giảm FPS, save asset budget.

### 5. Tương Tác Môi Trường

- Có nhấn nút, có cúi xuống nhặt đồ không?
- Wall collision (xem [[blend-animation-pattern]]).
- Terrain variant (chạy trên cỏ vs chạy trên băng — chân run run?).

## Form Ảnh Hưởng Biên Độ Anim

Quy tắc đầu tiên Vũ chốt: animation phải khớp với form, không cào bằng.

### To Béo vs Nhỏ Gầy

Cùng 1 action A→B trong 1 giây:
- **Nhân vật nhỏ**: rơ tay rất rõ ràng, nhìn hợp lý.
- **Nhân vật to béo**: rơ tay nhanh quá → ảnh bị vô lý.

> *"Cái việc này diễn ra ngay từ thời điểm đầu tiên. Một người béo tay từ vị trí A lên vị trí B của vợ, và một người gầy rơ tay từ A lên B — không thể coi cùng được."*

### Sức Nặng & Sức Đập

- **Nhảy**: nhân vật nhỏ → nhảy lên bàn OK. Nhân vật to béo → nhảy lên bàn không hợp lý → biên độ jump giới hạn.
- **Sức đập**: nhân vật to → impact nặng, ít động tác. Nhân vật nhỏ → impact nhẹ, có thể múa.

### Quy Tắc

- **Người to** → động tác **ít, rõ ràng, gọn gàng**.
- **Người nhỏ** → có thể **múa may rồng phượng** mà nhìn vẫn hợp lý.

Vẽ 2 con giống hệt rồi kéo cao thấp → form to béo bị "dối" → anim không khớp với hình ảnh.

## Frame Chuẩn Cho Action Cơ Bản

Define 1 action tham chiếu, các action khác tính relative:

- **Frame rate chuẩn** (ví dụ 24 FPS hoặc 30 FPS) cho 1 action cơ bản.
- Action cho mỗi con tính theo biên độ relative (con to chậm hơn 1.2×, con nhỏ nhanh hơn 0.8×).

Nếu không define từ đầu → mỗi action tự do → code không tính được cast time → balance gãy.

## Cast Time & Cooldown — 2 Approach

Đây là cross-reference với [[cast-time-cao-bang-vs-per-con]] (full comparison article).

Tóm tắt:
- **Cào bằng**: tất cả con dùng cùng cast time. Code đơn giản. Default.
- **Per Con**: mỗi con riêng. Code phải xử lý từng case. Battle RPG 6-7 skin → workload explode.

> *"Cuối cùng cái kết quả cân bằng thực tế không giống với kết quả cân bằng lý thuyết của các bạn — ít nhất là về mặt số học."*

## Mức Độ Chi Tiết Anim — Theo Tần Suất

Invest principle:
- **Anim xuất hiện nhiều** (idle, walk, run, attack basic) → đầu tư chi tiết.
- **Anim xuất hiện ít** (case đặc biệt, victory pose) → giảm chi tiết, save thời gian.

Ngoài ra liên quan **tương tác bối cảnh**:
- Trên băng: chân run run, tốc độ chậm, chân vẫn khua như đang chạy → không hợp lý.
- Cần anim variant theo bối cảnh nếu game có nhiều terrain.

## Quần Áo Va Vào Người — Mộng Bốn Lầm Case 2013

Constraint kỹ thuật:
- Stitch points trên vải dính vào skin nhân vật → tốn memory.
- 4×4 nhân vật trên màn → lượng stitch nhiều → máy 2013 không đủ.

Workaround Vũ:
- Chọn quần áo **bó sát**, ôm gọn vào thân.
- Tránh chi tiết rườm rà (váy dài, áo choàng phồng).
- Style "thực dụng" — giảm complexity asset.

Modern solution: dòng máy cao → có thể cloth simulation, nhưng mobile target rộng → vẫn cần optimization.

## Anti-Pattern

- **Mô tả anim chỉ "nhanh chậm"** — không có frame count, không có FPS.
- **Cào bằng anim cho mọi form** — to/nhỏ cùng animation → form to nhìn "dối."
- **Skin time scale ngắn/dài** để fit time → trông như múa hoặc vèo vèo.
- **GD không nói về frame rate** khi anim ít/nhiều → artist invest đều mọi anim, waste.
- **Skip transition logic** — anim không nối được, code phải custom.

## Liên Hệ Wiki

[[art-brief-3-parts]] cho static art brief — animation brief là extension. [[cast-time-cao-bang-vs-per-con]] cho cast time approach comparison. [[gd-reverse-skin-time]] cho approach "fix time first, design within." [[blend-animation-pattern]] cho transition technique chi tiết.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-2-animation.md` § "Đặt Vấn Đề", "Tính Cách + Đặc Trưng Quyết Định Animation", "Frame Chuẩn", "Mức Độ Chi Tiết Anim"
