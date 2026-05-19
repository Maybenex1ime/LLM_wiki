---
title: "Thuật Toán Spawn Chip Match-3"
source: "[[raw/videos/negaxy-iec-gd-doc-02-level-design]]"
date_added: 2026-05-15
tags: [concept, match-3, algorithm, level-design, rng]
aliases: [chip spawn algorithm, thuật toán sinh chip, adaptive key object Match-3]
status: draft
related:
  - "[[match3-difficulty-levers]]"
  - "[[hidden-variable-difficulty]]"
  - "[[match3-player-archetypes]]"
summary: "Logic spawn chip trong Match-3: limit màu per level, bias ô liền kề khác màu cho dễ, tỷ lệ drop 5 màu (đều 20% là khó nhất), adaptive key object xuất hiện theo số fail"
---

## Định Nghĩa

Thuật toán spawn chip là **layer ẩn** của level design Match-3, quyết định khi nào và màu nào sẽ xuất hiện trên board sau mỗi nước đi. Đây là lever 5 ("tắc ẩn") trong [[match3-difficulty-levers]] — user không nhìn thấy nhưng quyết định độ khó.

Vũ note: viết logic spawn riêng chỉ phần đó cần "4-6 trang" cho code làm. Đây không phải pseudo-code đơn giản mà là document chi tiết với mọi edge case.

## Các Tham Số Chính

### 1. Limit Màu

Mỗi level chỉ dùng 1 subset màu của full palette.
- Level 1-5: 3 màu → dễ match.
- Level 10-15: 4 màu.
- Level 20+: 5 màu (max).

Tăng số màu = tăng khó vì xác suất 3 chip cùng màu đứng cạnh nhau giảm.

### 2. Bias Ô Liền Kề

Muốn dễ thì cho ô trên (row i+1) khác màu với ô dưới (row i) → tăng khả năng vertical combine.

Logic: sau khi user match 1 cluster, chip mới rơi xuống. Nếu chip mới ngẫu nhiên match với chip cũ → cascade tự nhiên. Bias giảm xác suất cascade (cho hard level) hoặc tăng (cho easy level).

### 3. Tỷ Lệ Drop Từng Màu

- **5 màu đều 20%** → khó nhất. Xác suất 3 chip cùng màu đứng gần thấp uniform.
- **Lệch tỷ lệ** (vd 30%/25%/20%/15%/10%) → dễ hơn. Cluster của màu cao xuất hiện thường hơn.

Designer dùng cài đặt này khi muốn nudge user về chiến thuật cụ thể — ép user match màu A trước (vì A xuất hiện nhiều), giải phóng path cho chip B.

### 4. Thay Tỷ Lệ Trong Cùng Level

Khi user mua thêm moves (bằng tiền/quảng cáo) phải đảm bảo cho thắng, nếu không user bỏ.

> *"Phải cho nó thắng, không nó bỏ mẹ em đi."*

Implementation: sau khi user trigger "moves pack", server trả về tỷ lệ drop favorable trong N moves tiếp theo. User cảm thấy *"hên thật"* — không nhận ra là pre-determined.

## Logic Adaptive Key Object (Candy Crush)

Case Vũ kể về adaptive logic cho key object:

> *"Có 5 object cần thu. Object thứ 5 chỉ xuất hiện khi còn 10 nước đi. Nếu lần 1 fail dưới 10 mu, lần sau cộng 5 mu (15). Nếu lần 2 vẫn fail, lần 3 cộng tiếp 5 mu. Bao giờ người ta thắng được thì xuất hiện sớm hơn nữa."*

Tóm tắt logic:
- Object thứ 5 chỉ xuất hiện khi user còn N moves remaining (mặc định N = 10).
- Mỗi lần fail level, threshold N tăng 5 (làm dễ đi).
- Khi user thắng, threshold reset hoặc về mặc định.

Pattern này là instance cụ thể của [[hidden-variable-difficulty]] cho key object — thay vì giảm số mu hiển thị (rủi ro user phát hiện), điều chỉnh thời điểm spawn object quan trọng.

## Quan Hệ Với Player Archetype

Thuật toán spawn ảnh hưởng khác nhau lên [[match3-player-archetypes]]:

| Archetype | Phản ứng với chip spawn favorable | Phản ứng với chip spawn unfavorable |
|-----------|-------------------------------------|---------------------------------------|
| First-Look | Pick combo to nhất, win | Random pick, có thể fail |
| Logic | Cascade chain → big win | Plan path khác, vẫn có thể win |
| Scattered | Random, có thể bỏ qua combo tốt | Likely fail |

Designer ưu tiên Logic + First-Look qua adaptive spawn — sau fail, spawn thêm "cluster rõ ràng" mà First-Look pick được, hoặc combo chain rõ mà Logic tính được. Scattered player vẫn fail random nhưng tỷ lệ tổng thắng tăng.

## Lưu Ý Implementation

- Logic phải **deterministic per session** — không random thuần. Cùng level + cùng action = cùng kết quả. Lý do: nếu thuần random, user replay 10 lần có thể có 1 lần win thực sự nhờ luck.
- **Server-authoritative** cho commercial title — không trust client để tránh cheat.
- **Logging mỗi spawn decision** — debug khi user complain "thua oan".

## Liên Hệ Wiki

[[match3-difficulty-levers]] là khung lớn — chip spawn là lever 5. [[hidden-variable-difficulty]] cho deep dive về dùng spawn để adjust khó sau IAP. [[match3-player-archetypes]] cho user-side phản ứng.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Thuật Toán Spawn Chip Trong Match-3"
