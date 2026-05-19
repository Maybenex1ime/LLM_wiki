---
title: "GD Doc 5 Part 2 — Animation: Mô Tả Animation, Frame Chuẩn, Hit Reaction & Tương Tác (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 5 Part 2 - Animation.MOV"
date_added: 2026-05-19
date_updated: 2026-05-19
tags: [video, course-transcript, game-design, animation, frame-rate, hit-reaction, combat, projectile, blend, vietnamese]
aliases: ["GD Doc 5 Part 2", "Buổi 5 Phần 2 Animation", "Animation Brief Vũ"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-05-part-1-art]]"
  - "[[negaxy-iec-gd-doc-06-part-1-ui]]"
  - "[[negaxy-iec-gd-doc-03-phase-du-an]]"
summary: "Buổi 5 Part 2 (Vũ + học viên): cách GD mô tả animation cho team art — frame chuẩn cho action cơ bản, biên độ theo form (to/béo vs nhỏ/gầy), cast time và cooldown approach (cào bằng vs per-con), projectile speed strategies, va vào tường blend animation, hit reaction 3 cách xử lý dồn (kệ mẹ / block time / anim kêu lại), combo blend giữa anim 1 → anim 2, biểu cảm tùy case, quần áo va vào người (Mộng Bốn Lầm 2013 case). GD reverse: fix skin time trước rồi thiết kế gì trong khoảng đó."
---

# GD Doc 5 Part 2 — Animation: Mô Tả & Brief

**Speakers:**
- **Vũ** — Lecturer chính. Chia sẻ kinh nghiệm Mộng Bốn Lầm (2013), các con song đấu, RPG.
- **Học viên** (không rõ tên) — đặt câu hỏi về combo, biểu cảm, projectile, quần áo va người.

**Format:** Buổi học trao đổi, ~45 phút, tiếng Việt. Tiếp nối Doc 5 Part 1 — chuyển từ art static sang motion/animation. Topic dạy GD cách viết animation brief cho team art.

Tiếp nối Doc 5 Part 1 (Art) và đặt nền cho Doc 6 (UI/UX). Có nhắc lại "feeling của game" từ Doc 1 và bài cân bằng từ Buổi 1.

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 5 Part 2 - Animation.MOV` (802 MB, ~45 phút) + `GD Doc 5 Part 2 - Animation.MOV.txt` (737 dòng, faster-whisper large-v3 chunked 5×10-phút qua `doc5_anim_chunks/`).

---

## Đặt Vấn Đề — GD Mô Tả Animation Như Thế Nào?

Vũ mở đầu hỏi: "Bạn GD mô tả animation cho team art như thế nào?" Học viên trả lời: "Tim rap, idle, walk..." → quá generic.

Vũ chỉ ra các yếu tố thiếu trong brief thông thường:

- **Detail hơn từng action** — không chỉ "idle" mà idle như thế nào.
- **Tiếp nối từ anim khác** — không có anim đứng độc lập, phải nối idle → walk → run.
- **Thời gian per anim** — bao nhiêu giây thì chuyển frame nào.
- **Tương tác với môi trường** — có nhấn nút, có cúi xuống nhặt đồ không.
- **Frame rate** — đặc biệt với hành động fast (nhân doanh, chạy).

> *"Mình hỏi các bạn có yêu cầu thời gian trong một anim trong lúc đầu không, hay chỉ mô tả nó là nhanh chậm trên đất? Đúng cách mọi người thông thường là như thế."*

Đây là baseline — phần lớn GD mô tả "nhanh / chậm" thay vì cụ thể frame count, frame rate, transition.

---

## Tính Cách + Đặc Trưng Quyết Định Animation

Vũ chốt nguyên tắc đầu tiên: animation phải khớp với **form của nhân vật**, không cào bằng.

### Form To Béo vs Nhỏ Gầy

Cùng 1 action A→B trong 1 giây:
- **Nhân vật nhỏ**: rơ tay rất rõ ràng, nhìn hợp lý.
- **Nhân vật to béo**: rơ tay nhanh quá → nhìn ảnh bị vô lý.

> *"Cái việc này diễn ra ngay từ thời điểm đầu tiên. Một người béo tay từ vị trí A lên vị trí B của vợ, và một người gầy rơ tay từ A lên B — không thể coi cùng được."*

### Sức Nặng & Sức Đập

- **Nhảy**: nhân vật nhỏ nhảy phát lên bàn — ok. Nhân vật to béo nhảy phát lên bàn — không hợp lý → biên độ jump phải giới hạn.
- **Sức đập** (impact, từ trên xuống): nhân vật to → impact phải nặng, ít động tác. Nhân vật nhỏ → impact nhẹ, có thể múa.

### Quy Tắc Động Tác

- **Người to** → động tác **ít, rõ ràng, gọn gàng**.
- **Người nhỏ** → có thể **múa may rồng phượng** mà nhìn vẫn hợp lý.

Nếu vẽ 2 con giống hệt rồi kéo cao thấp → form to béo bị "dối" (động tác bị kêu quá nhiều) → anim không khớp với hình ảnh.

---

## Frame Chuẩn Cho Action Cơ Bản

Vũ đề xuất define **frame chuẩn cho 1 action tham chiếu**, sau đó từng con tính biên độ relative:

- **Frame rate chuẩn** (ví dụ 24 FPS hoặc 30 FPS) cho 1 action cơ bản — gọi là frame tham chiếu.
- Action cho mỗi con tính theo biên độ relative (con to chậm hơn 1.2×, con nhỏ nhanh hơn 0.8×).

Nếu không define từ đầu → mỗi action tự do → code không tính được cast time → balance system gãy.

---

## Cast Time & Cooldown — 2 Approach

Vũ phân biệt 2 cách xử lý skill timing:

### Approach 1: Cào Bằng (Recommended)

- Cooldown tính từ **thời điểm 0** (lúc bấm skill).
- Projectile bắn ra từ **thời điểm 0 + C1** (constant cast delay).
- Tất cả con dùng C1 giống nhau.

→ Code logic đơn giản. Skill timer = số học.

### Approach 2: Cast Time Per Con

- Mỗi con animation cast time khác nhau (con A 0.8s, con B 1.2s).
- Code phải tính cast time per con khi tính DPS, projectile spawn.

> *"Cái này nó sẽ bị khác nhau và code sẽ bị đi xử lý từng việc một. Đấy là lý do vì sao mình mới nói cố gắng đẩy từ sớm nhất có thể."*

Hậu quả không define từ sớm:
- Battle RPG 6-7 skin → mỗi skin tính riêng → workload bùng nổ.
- Số học DPS không match thực tế (con A đáng lý mạnh hơn con B nhưng anim chậm hơn → thực tế ngang nhau).

> *"Cuối cùng cái kết quả cân bằng thực tế không giống với kết quả cân bằng lý thuyết của các bạn — ít nhất là về mặt số học. Mình chưa nói về fueling."*

---

## Projectile Speed — Đa Phần Là "Cắt Ra Là Chúng"

Vũ phân loại projectile theo logic:

### Loại 1: Logic "Cắt Ra Là Chúng" (Đa Số)

- Skill bắn ra → mặc định trúng target.
- Bạn không cần tính physics — chỉ vẽ animation projectile đi từ vị trí A → vị trí B (target lúc bắn).
- Tốc độ projectile **nhanh** để khỏa lấp gap di chuyển của target.

### Loại 2: Platformer / Có Chạm

- Chỉ skin Platformer mới cần tính chạm thật.
- Có chạm → gây dam. Không chạm → miss.

### Anti-Pattern: Box Projectile To

Một số GD dùng trick "làm box projectile to hơn" → "cảm giác chưa chạm đã gây dam":

> *"Trường hợp nó rất là ngu ở chỗ này — kiểu cảm giác nó chưa chạm vào nó đã gây dam rồi. Tester bắt đầu kiểu âm lên."*

Tester sẽ flag inconsistency → fail QA.

### Loại 3: 3D Real-Position Skill

- Bắn theo vị trí thật target → target chạy bố → miss.
- Solution:
  - **Bay vòng rả** — tracking projectile (homing missile).
  - **Predict** — đoán vị trí sau X giây dựa vào hướng di chuyển → bắn thẳng đến đó.

---

## GD Reverse — Fix Skin Time Trước

Vũ đề xuất tư duy ngược chiều:

> *"Tôi đã fix cái skin này trong khoảng gian bao lâu, và bây giờ tôi nghĩ xem nên làm gì trong khoảng gian đấy. Tức là nghĩ từ không cân bằng đi xuống."*

Pattern:
1. **Chốt time fix** (ví dụ 1s cho cast skill).
2. **Tính lượng action có thể nhồi trong 1s** đó (animation, projectile, hit effect).
3. **Cân bằng** dựa trên số học.

Lợi ích:
- Skin không phải scale ngắn/dài → không trông "vèo vèo" hay "múa quá."
- Project time và cast time match với calculation.
- Result thực tế = lý thuyết.

Vũ nhắc lại bài cân bằng từ Buổi 1: *"Các bạn phải để ý vấn đề cân bằng ngay từ đầu."*

---

## Va Vào Tương Tác — Wall Collision

Tình huống: nhân vật chạy → va tường → vẫn cứ chạy "dũi thẳng" vào tường. Đa phần game accept hành vi này.

### Solution 1: Kệ (Accept)

> *"Nếu chấp nhận thì thôi nha ông bạn nha."*

Phù hợp cho game không yêu cầu polish cao.

### Solution 2: Anim Có Tương Tác (Blend)

- Khi va tường → sinh ra anim transition.
- **Blend** từ "run" sang "idle" để cử động không bị cứng.

> *"Nó blend lại với cả idle. Nó blend idle để cho phạm vi của hành động nó nhẹ nhàng lại."*

Phù hợp polish cao, đặc biệt 3D adventure / open world.

---

## Hit Reaction — Bài Toán Dồn

Combat 2 player chém nhau có 2 mode:

### Mode 1: Không Hit Reaction (Phần Phật Phật)

- Cả 2 không có anim bị thương.
- Cùng action attack → trade damage qua DPS.

### Mode 2: Có Hit Reaction (Ngửa Người Ra Sau)

- Khi bị chém → anim "ngửa người" (~0.2s) + "giật về idle" (~0.2s) = 0.4s freeze.

#### Bài Toán Dồn

- Attacker action = 1s.
- Defender hit reaction = 0.4s.
- Tổng defender chờ trước khi đánh lại = 1.4s (ngửa + giật về + bắt đầu attack mới).
- Trong gap 0.4s đó → attacker đánh tiếp → defender ngửa tiếp → **bị dồn vô tận**.

> *"Trong thời gian 1.2 giây — tôi đứng nghiêm cho bạn chém hay tôi lại vã cho cái nữa? Bạn lại ngửa ra đằng sau và có nghĩa là rồn — chết toang luôn."*

### 3 Cách Xử Lý

| Cách | Mô tả | Phù hợp |
|------|-------|---------|
| **Kệ mẹ** | Người dồn được, kẻ bị dồn không có cửa bật lại | Hardcore brawler, intentional combo |
| **Block Time** | Sau 1 hit, có cooldown trước hit tiếp (skill này không block tham) | Song đấu (1v1) cần tương tác cao |
| **Anim Kêu Lại** | Anim của attacker bị speed-up để match thời gian recovery của defender | Game chiến thuật / RPG cào bằng |

### Theo Dòng Game

- **Game chiến thuật, số đông, auto** → chọn cách **Anim Kêu Lại** (block tham). Calculation = thực tế.
- **Song đấu / tương tác cao** → chọn **Kệ Mẹ** hoặc **Block Time**. Player feel responsive.
- **Combo skill có chủ ý** → cho dồn thoải mái (block tham mặc định nhưng combo skill đặc biệt được dồn).

> *"Khi nghĩ ra anim, các bạn cần phải đưa ra cái logic cho anim đấy để code thực hiện thôi. Còn nếu không nói về logic ngã ngửa giật sau, họ sẽ không biết tính toán như thế nào."*

---

## Combo Animation — Blend Giữa Anim 1 → Anim 2

Game tiết tấu nhanh (song đấu) cần animation **chuyển trực tiếp** không về idle:

- **Đá cao → đá thấp** không về idle giữa.
- **Đá cao → skin 2** không về idle.

### Anti-Pattern: Vẽ Tất Cả Tổ Hợp

Bùng nổ tổ hợp:
- Đá cao → idle, đá thấp → idle, đấm → idle.
- Đá cao → đá thấp, đá cao → đấm, đá thấp → đá cao...
- N action × N transition = N² anim files. Không quản lý được.

### Solution: Blend Hiệu Ứng

> *"Blend là một cái khoảng hiệu ứng để tiếp nối — đây là anim 1, đây là anim 2. Bình thường nó sẽ về idle sau diễn hay. Nhưng làm mờ trong đoạn này và nó đi sang anim 2 ngay lập tức."*

Code làm transition:
- Tắt anim 1 (fade out).
- Mở anim 2 (fade in).
- Khoảng blend ngắn (~0.1-0.2s).

Yêu cầu artist:
- Vẽ anim độc lập (anim 1 + anim 2).
- Định nghĩa "đoạn nào cần blend lên hay không" trong brief.

---

## Biểu Cảm — Tùy Case

Vũ admit không nhiều trải nghiệm phần này:

> *"Mình chưa có trải nghiệm làm tới game mà sử dụng anime — sử dụng biểu cảm. Ngoại trừ trailer thì mình không nói nhé."*

Trong game của Vũ chỉ làm:
- **Nhăn mặt / nhăn mũi** khi bị hit (đi kèm hit reaction).
- **Mô tả** biểu cảm bằng text trong brief, không animate.

### Biểu Cảm Theo Case Trạng Thái

Phù hợp khi game có state machine rõ:
- **HP thấp** → nhăn mặt, thở hổn hển.
- **Thua** → gục mặt xuống.
- **Bị thương** → chân đi cà thọt, cà nhắc.
- **Thắng** → nhảy múa, dơ tay chúc mừng.

Theo style là **anim đặc biệt cho case** thay vì biểu cảm liên tục.

---

## Mức Độ Chi Tiết Anim — Theo Tần Suất

Vũ chốt nguyên tắc invest:

- **Anim xuất hiện nhiều** (idle, walk, run, attack basic) → đầu tư chi tiết.
- **Anim xuất hiện ít** (case đặc biệt, victory pose) → giảm chi tiết, save thời gian.

Ngoài ra còn liên quan đến **tương tác bối cảnh** — chạy trên cỏ vs chạy trên băng:
- Trên băng: chân run run, tốc độ chậm lại, chân vẫn khua như đang chạy → không hợp lý.
- Cần anim variant theo bối cảnh nếu game có nhiều terrain.

---

## Quần Áo Va Vào Người — Mộng Bốn Lầm Case 2013

Vũ kể trải nghiệm: con Mộng Bốn Lầm (2013) gặp vấn đề quần áo (váy) va vào đùi.

### Constraint Kỹ Thuật

- Stitch points trên vải dính vào skin nhân vật → tốn memory.
- 4×4 nhân vật trên màn → lượng stitch nhiều → máy 2013 không đủ resource.

### Workaround Vũ Dùng

- Chọn quần áo **bó sát**, ôm gọn vào thân.
- Tránh chi tiết rườm rà (váy dài, áo choàng phồng).
- Style "thực dụng" — giảm complexity asset.

### Modern Solution

- Dòng máy cao → stitch points cao.
- Có thể dán vải vào đùi với cloth simulation.
- Tuy nhiên với mobile (target rộng) → vẫn có cấu hình thấp → cần optimization.

---

## Naming Convention Cho Trang Phục Thay Thế

Khi GD yêu cầu skin system (quần áo thay thế được) — cả 2D và 3D — Vũ note nguyên tắc:

- Chia phần body parts (head, torso, legs, hand) thành component.
- Mỗi component có pose set chuẩn (idle, attack, idle, dead).
- Naming convention nhất quán để swap được.
- Body skeleton chung cho mọi outfit.

Topic này Vũ defer chi tiết — sẽ deeper trong buổi Animation Tools nếu có.

---

## Anti-Pattern Tổng Hợp

- **Mô tả anim chỉ "nhanh chậm"** — không có frame count, không có FPS.
- **Cào bằng anim cho mọi form** — to/nhỏ cùng animation → form to nhìn "dối."
- **Cast time per con tự do** — code phải xử lý từng case → workload bùng nổ.
- **Box projectile to** để fake hit — tester phát hiện ngay.
- **Ép vẽ mọi tổ hợp transition** — N² files, không scale.
- **Không define hit reaction logic** — code không biết tính ngược, dẫn đến dồn vô tận hoặc trade dam sai.
- **Quần áo rườm rà** trên hardware yếu — lag + memory issue.
- **Skin scale ngắn/dài** để fit time → trông như múa hoặc vèo vèo (skin time không fix từ đầu).
- **GD không nói về frame rate khi anim ít/nhiều** — artist invest đều mọi anim, lãng phí.

---

## Thuật Ngữ Buổi Này

### Animation Basics
- **Frame Chuẩn** — frame rate (FPS) baseline cho 1 action cơ bản. Các action khác tính relative.
- **Biên Độ Anim** — phạm vi chuyển động cho phép theo form (to béo / nhỏ gầy).
- **Cast Time** — thời gian từ lúc bấm skill đến lúc skill phát.
- **Cooldown** — thời gian giữa 2 lần dùng skill.
- **Cào Bằng** — approach 1: tất cả con dùng cùng cast time / cooldown. Code đơn giản.
- **Per Con** — approach 2: mỗi con khác. Code phải tính per case.

### Projectile
- **Cắt Ra Là Chúng** — projectile mặc định trúng target, không tính physics. Đa số game.
- **Platformer Skill** — projectile cần chạm thật mới gây dam.
- **Predict Position** — đoán vị trí target sau X giây để bắn trúng (3D real-position).
- **Bay Vòng Rả** — tracking/homing projectile.
- **Box Projectile** — hitbox của projectile. Làm to để "fake hit" là anti-pattern.

### Combat
- **Hit Reaction** — anim phản ứng khi bị tấn công (ngửa người, nhăn mặt).
- **Block Tham** — skill block lẫn nhau, không thể spam dồn.
- **Dồn** — combo vô tận khi defender chưa kịp recover.
- **Phần Phật Phật** — không hit reaction, 2 bên trade dam qua DPS.

### Animation Transition
- **Blend** — hiệu ứng nối anim 1 → anim 2, fade out + fade in. Khoảng 0.1-0.2s.
- **Idle Return** — về idle giữa các action (default).
- **Combo Chain** — chuyển trực tiếp giữa các action, không về idle.

### Expression / State
- **Anim Case Đặc Biệt** — anim cho HP thấp, thua, thắng, bị thương — không phải biểu cảm liên tục.
- **State Machine** — quản lý anim theo state (idle / attack / hit / dead / victory).

### Asset Optimization
- **Stitch Points** — điểm dính vải vào skeleton/skin. Càng nhiều càng tốn memory.
- **Tần Suất Anim** — anim xuất hiện nhiều → invest chi tiết. Anim ít → giảm chi tiết.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Video gốc: `GD Doc 5 Part 2 - Animation.MOV` (802 MB, ~45 phút).
- Transcript đầy đủ: `GD Doc 5 Part 2 - Animation.MOV.txt` (737 dòng, faster-whisper large-v3 chunked 5×10-phút qua `doc5_anim_chunks/`).
- Chunks: `doc5_anim_chunks/chunk_000.wav.txt` ... `chunk_004.wav.txt`.
- Khoá học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
- Vị trí trong khoá: **Buổi 5 Phần 2 — Animation** (nằm sau Doc 5 Part 1 Art; đặt nền cho Doc 6 UI/UX).
- Date updated 2026-05-19: compile lần đầu sau khi chunked transcription hoàn thành.
