---
title: "Level Iteration Testing"
source: "compiled"
date_added: 2026-05-05
tags: [concept, level-design, testing, analytics, puzzle]
aliases: [iteration testing, S1-S4 testing, quick funnel fix]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[level-funnel-heartbeat]]"
  - "[[rv-placement-strategy]]"
  - "[[lion-studios]]"
summary: "4 phases test (S1-S4) và quick funnel/level fix techniques theo Lion Studios"
---

## Định Nghĩa

Iteration testing là quy trình test và fix level funnel theo từng giai đoạn (S1-S4) trong vòng đời development, kết hợp với techniques quick fix dựa trên data churn / fail rate / RV per user. [[lion-studios]] đặt iteration testing là layer optimization phía trên các nguyên tắc design tĩnh.

## 4 Phases Testing

| Phase | Focus | Lưu ý |
|---|---|---|
| **S1** | Basic, 1-2 mechanics | Đừng tạo difficult levels — playtester có skill cao hơn average player |
| **S2** | Initial data | Check make sure early levels không quá khó, see how new players react khi difficulty tăng |
| **S3** | Optimize heartbeat pattern + see churn | Implement 4-5 mechanics |
| **S4** | More levels, more mechanics, further optimization | Focus on level ARPU, coin sinks |

Sub-rule từ Playbook: nếu D1 retention có vấn đề → check data, fix và reorder levels. Consider adding một couple of new mechanic.

## Quick Funnel Analysis

Phương pháp data-driven để identify levels cần action.

**Best monetized levels (nhân bản).** Sort theo `RV Shows Per User` cao nhất, filter levels có level churn thấp (good signal). Tell design team analyze và create more similar ones.

**Worst engaging hard levels (priority fix).** Sort theo level churn rate cao nhất, filter levels có high fail rate. Tell design team analyze và fix.

**Easy levels có monetization problem.** Filter ra first 10 levels (very early), filter ra fail rate < 8% (too easy). Còn lại sort theo `RV Shows Per User` thấp nhất → đây là levels có thể make harder để improve monetization. Liên kết trực tiếp với chiến thuật trong [[easy-level-design]].

**Critical issue: churn without difficulty.** Filter levels có churn cao nhưng fail rate thấp. Đây là dấu hiệu technical / UX problem, không phải difficulty.

## Quick Level Fix

Khi identify level cần fix, dùng playtest data:

- Check `move to fail` hoặc `time to fail` variable — compare proportionally với level goal
- Quan sát noob play để tìm frustration moment

Ví dụ Playbook: nếu data cho thấy players failing ở ~3 phút trên level có timer 3:12 → thử fix timer trong level. Xem [[timer-design]] cho timer-specific tuning.

## Quick Funnel Fix

Keypoints: release tension của back-to-back hard levels; achieve bằng reorder where possible (rẻ hơn redesign); fix otherwise.

Ví dụ actions trong Playbook:
- "Back to back hard levels, replace with level X"
- "Decrease difficulty make it easy level"
- "Replace with [easier level ID]"
- "Decrease difficulty"

## Toolkit

Lion Studios khuyến nghị toolkit cơ bản:

- Level Editor in Unity (cho S4+ games)
- Level Database with level visuals (Figma không practical for analysis — dùng Google Sheet với heartbeat pattern)
- Level Catalogs của mỗi release including Looker data
- Level Fix Backlog có resulting data từ Looker
- Level Files dạng JSON/CSV (thay vì separate scenes trong Unity editor)
- Looker Level Funnel dashboard

## Metrics Cốt Lõi

Level Funnel Data: avg stacks placed to complete, avg stacks placed to fail, avg goal complete %, attempts (7+ days), funnel %, level churn %, level fail %, retry ratio, avg coin sink, unique level fail, avg play used, avg pre-up used, RV shows per user (unique), RV shows per user.

Level ARPU Data: ARPU, cum ARPU, % RV revenue, % inter revenue, % banner revenue, % IAP revenue.

Cho timer levels add thêm: avg time to fail, avg time to win, fail by time %.

## Nguồn Tham Khảo

- `raw/papers/Lion.pdf` (Level Design Playbook, slides 24-29, 30-32)
