---
title: "FTUE Curve"
source: "compiled"
date_added: 2026-05-05
tags: [concept, level-design, onboarding, ftue, puzzle]
aliases: [first time user experience, onboarding curve, đường cong onboarding]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[easy-level-design]]"
  - "[[level-funnel-heartbeat]]"
  - "[[new-mechanic-introduction]]"
  - "[[booster-design-puzzle]]"
  - "[[lion-studios]]"
summary: "Curve fail rate cho 20-25 levels đầu của puzzle game theo Lion Studios — 0-5% → 8-10% → 15% → 20%"
---

## Định Nghĩa

FTUE (First Time User Experience) curve là chuỗi level đầu (~20-25 levels) được calibrate fail rate tăng dần để hook người chơi qua D0 session, build expertise, và set expectations cho thử thách lớn hơn. Curve này được [[lion-studios]] benchmark cho puzzle game có level duration 1-2 phút.

## Curve Fail Rate Chuẩn

| Range | Mục đích | Fail rate target |
|---|---|---|
| Lvl 1-5 | Super easy start | 0-5% |
| Lvl 6-8 | First little challenge | 8-10% |
| Lvl 11-14 | First hard level | ~15% |
| Lvl 16-20 | Second hard level | ~20% |

Trần an toàn: "If you don't have an exceptional sticky game, you shouldn't have fail rate above 25% in your first 20-25 levels for a game about 1 min average level duration".

Levels giữa các hard ones phải là mix easy + medium. First hard level (Lvl 11-14) phải đặt next to first mechanic's tutorial level — để người chơi vừa học mechanic xong có cơ hội áp dụng ngay.

## Ba Lớp Đan Xen

FTUE curve không chỉ là curve difficulty — nó là 3 curve song song.

Lớp difficulty theo bảng trên. Lớp mechanic introduction trong D0-D1 introduce 2-3 core mechanics (exploratory phase), mechanic đầu dạy ngay từ Lvl 1 — xem [[new-mechanic-introduction]]. Lớp booster introduction theo thứ tự tăng dần power, mỗi booster đặt ngay trước challenge spike — xem [[booster-design-puzzle]].

Ví dụ rollout cho game 8-10 min/3 levels đầu: Lvl 4 introduce 1st booster, Lvl 5 1st little challenge (lý do dùng booster vừa học), Lvl 6 2nd booster, Lvl 9 3rd booster, Lvl 12 1st real challenge.

## Anatomy D0 Session

Theo MVP Guide, một D0 session điển hình có cấu trúc:

```
Lvl 1 ── Lvl 5 ── Lvl 12 ── Lvl 19/20 ── Lvl 35
Onboard  First    Learning  First         End of
         longer   reinforce hard level    session
         level
```

Lvl 1 là onboarding — không challenging, dễ qua. Lvl 5 là first longer level — hơi lâu hơn bình thường, người chơi thường fail vì lỗi nhỏ và fix ở attempt 2. Lvl 12 là learning reinforcement — dùng những gì đã học ở onboarding. Lvl 19-20 là first real challenge, takes 2-3 fails. Sau khi hoàn thành Lvl 20, first interstitial xuất hiện kèm no-ads offer popup ngay sau. Lvl 35 thường là điểm kết thúc D0 session — trên hoặc sau một hard level.

## Vai Trò Của First Hard Level

Hard level đầu tiên trong FTUE không để monetize. Mục tiêu là introduce upcoming challenges của further levels. Quote MVP Guide: "The goal for the hard levels in D0 is to introduce the upcoming challenges at the further levels not monetizing users at first."

Kết thúc D0 session ở/sau hard level tạo cliffhanger cho D1 — người chơi muốn quay lại để vượt qua.

## Anti-Patterns

| Đừng | Lý do |
|---|---|
| Hard level ở Lvl 1-10 | Churn cao, chưa đủ expertise |
| Fail rate >25% trong 20 levels đầu | Vượt sticky threshold |
| Visual đơn giản ở levels đầu | "Easy = boring", xem [[easy-level-design]] |
| Introduce >3 mechanic trong D0 | Quá tải mental model |
| Hard level mà không có mechanic mới đi kèm | Mất cơ hội teach by challenge |

## Nguồn Tham Khảo

- `raw/papers/Lion Studios MVP Guide.pptx.pdf` (slides 10-11, 15)
- `raw/papers/Lion.pdf` (Level Design Playbook, slide 11)
