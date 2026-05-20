---
title: "Form Base Art Template — Con Đầu Tiên Là 10 Điểm"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-1-art]]"
date_added: 2026-05-20
tags: [concept, art, art-workflow, production-line, asset-pipeline, scaling]
aliases: [form base, con đầu tiên template, production line art, asset scale workflow]
status: draft
related:
  - "[[art-brief-3-parts]]"
  - "[[mep-mep-affordance]]"
  - "[[file-y-do-design-intent]]"
summary: "Workflow Vũ chốt khi studio nhỏ không có art director: vẽ con đầu (form base) kỹ → fix tỷ lệ chân tay/mắt → giữ nguyên cho các con sau, chỉ thay quần áo/đầu. 3 form base: trung bình / béo / gầy. Production line-able, giảm dependency 1 artist cứng."
---

## Định Nghĩa

Form Base Art Template = workflow scale team art bằng cách **fix tỷ lệ thân thể** (form base) cho 1 con đầu tiên, các con sau follow form đó (chỉ thay outfit, head, accessory).

Phù hợp khi studio nhỏ không có art director cứng — GD phải gánh role half-art-director.

> *"Đấy là một cách để cho các bạn bớt phải gãy nhau. Và các bạn art khác — khi 1 người đã vẽ rồi — thì những người khác còn lại cũng có thể xuất công nghiệp. Cứ thế vẽ đè lên."*

## 3 Bước Workflow

### Bước 1 — Vẽ Con Đầu Theo Form

- Vẽ con base: tỷ lệ đầu, mắt, chân tay, hand.
- Iterate cho đến khi GD chấp nhận: *"Tôi thấy cũng được."*
- **Chốt con đầu tiên là 10 điểm** — không sửa nữa từ moment này.

Anchor metaphor: con đầu = ruler. Sau này tất cả compare against ruler.

### Bước 2 — Cứ Theo Form Vẽ Tiếp

> *"Từ giờ anh em làm cách này nhá: cứ theo form này mà phải. Mắt giữ nguyên size, chân tay giữ nguyên size. Tóc, quần, đắp áo vào thôi. Đừng vẽ lại nữa."*

3 form base recommended:
- **Trung bình** — default proportion.
- **Béo** — thicker torso, wider hips.
- **Gầy** — thinner torso, longer limbs.

Mỗi form vẽ kỹ chỉ 1 con. Tất cả con khác trong form đó:
- Thay đầu (face, hair).
- Thay outfit (clothing, armor).
- Thay accessory (weapon, hat).
- **KHÔNG thay** chân tay tỷ lệ.

### Bước 3 — Document Edge Cases

Define preemptively để art không tưởng tượng:
- **Tóc cao nhất đến đâu** (max hair height).
- **Mũ cao nhất đến đâu** (max hat height).
- **Bụng to** → vẽ con bụng to ra trước, đừng ép artist tưởng tượng.
- **Cao và lùn** → nếu khác form, vẽ riêng từ đầu (không squeeze form base).

## Lợi Production Line

### Giảm Dependency

> *"Việc đòi tuyển art director là một câu chuyện mà mình nghĩ các bạn sẽ không giải quyết được. Volume của công ty + quy mô dự án không đủ để cho 1 director có đất dụng võ."*

Studio nhỏ không có director full-time:
- GD gánh half-vai (knowing style + detail + color + workflow).
- Artist mới onboard nhanh — chỉ cần follow form base + brief.
- Một artist rời đi không phá pipeline (form base là template, không phải gu cá nhân).

### Tăng Throughput

| Approach | Asset/Week | Quality |
|----------|-----------|---------|
| Mỗi artist vẽ tự do | 5-8 | Inconsistent |
| Form base + outfit swap | 15-20 | Consistent |

Form base ~3-4× throughput vì:
- Skip "vẽ chân tay" phase per asset.
- Reuse rig/skeleton.
- Auto-merge body parts với head parts (xem dưới).

## Auto-Merge Tools

Khi form base + naming convention consistent, có thể script auto-merge:

### Conditions

- Tất cả nhân vật cùng pose set (idle, attack, dead, skin1).
- Body parts ghép được với nhau (cùng skeleton).
- Có hoặc không có body pass — cả 2 đều ghép được.

### Process

- Artist vẽ separate: bodies, heads, outfits, accessories.
- Script combine: pick body type → pick head → pick outfit → pick accessory.
- Output: 1 combined character với pose set hoàn chỉnh.

### Naming Convention Example

Đức propose: `men_strength_1`, `men_strength_2`.

Vũ improvement:
- **Đổi tiền tố trước**: `m_strength_1` thay vì `men_strength_1`.
- Lý do: sort file → phần nào của anh nào (m_ = men, w_ = women, e_ = enemy).
- Compact prefix giúp script parse easier.

## Process Ritga (Reference)

Minh share kinh nghiệm Ritga: anh Nhất (art lead) áp **process 7-9 bước** cho 1 bức ảnh nhân vật.

- Mỗi bước là 1 stage hoàn thiện (sketch → line → flat color → shading → details → review).
- Duyệt xong stage → mới chuyển sang stage tiếp.
- Bước nào sai → refactor stage đó, không phá toàn bộ.

Vũ comment: process Ritga "trùng cầy" cho team nhỏ, phù hợp studio mid-size làm sản phẩm dài hạn. Studio nhỏ + prototype → skip → use form base.

## When To Re-Visit Form Base

Form base không sacred — re-visit khi:
- **New character archetype** (e.g., dragon-type, robot) → cần form mới.
- **Game pivot** đổi style — abandon form cũ, draft form mới.
- **Quality issue** sau ship — user complain form awkward → redesign.

Khi re-design: drop old form + freeze new form. Don't try to "evolve" form gradually (creates inconsistency).

## Anti-Pattern

- **Mỗi artist vẽ tự do** — inconsistency, không scale.
- **Form base không document** — new artist không biết, vẽ tự do.
- **GD ép artist tưởng tượng edge case** — bụng to / tóc cao → artist guess → sai.
- **Có art director full-time ở studio nhỏ** — không đủ work, conflict.
- **Squeeze form base cho mọi character** — cao và lùn không fit form base trung bình → awkward.

## Liên Hệ Wiki

[[art-brief-3-parts]] cho 3-part brief — form base implement Part 1 (Art Style). [[mep-mep-affordance]] cho cụ thể về layout — form base ảnh hưởng layout calculation. [[file-y-do-design-intent]] cho design intent file — form base belongs trong design intent.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-1-art.md` § "Workflow Chốt Form — Con Đầu Tiên Là Template", "Naming Convention Cho File List", "Process Ritga"
