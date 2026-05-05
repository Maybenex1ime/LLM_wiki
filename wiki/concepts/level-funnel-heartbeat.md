---
title: "Level Funnel Heartbeat"
source: "compiled"
date_added: 2026-05-05
tags: [concept, level-design, funnel, puzzle]
aliases: [heartbeat pattern, difficulty pattern, nhịp tim funnel]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[easy-level-design]]"
  - "[[ftue-curve]]"
  - "[[lion-studios]]"
summary: "Pattern bố trí hard/mid/easy levels trong daily loop — 20-25% hard levels, gap 4-6 giữa 2 hard"
---

## Định Nghĩa

Heartbeat pattern là cách phân bố levels theo difficulty trong daily loop để tạo nhịp tension/relief — tương tự nhịp tim. [[lion-studios]] khuyến nghị 20-25% levels trong loop hằng ngày là hard, phân bố đều, và không bao giờ back-to-back.

Phân biệt với heartbeat within a level (xem [[hard-level-design]]) — bài này nói về heartbeat giữa các levels trong funnel, không phải bên trong 1 level.

## Phân Loại Level Theo Difficulty

Đo bằng average attempts to complete:

| Loại | Avg attempts | Fail rate (tham khảo) |
|---|---|---|
| Easy | 1-1.3 | 10-15% |
| Mid | 1.3-1.7 | 15-30% |
| Hard | >1.7 | 30-50%+ |

Tuy nhiên, Playbook nhấn mạnh: nên định nghĩa hard/easy bằng inflection point của churn vs fail rate trong dữ liệu game cụ thể, không phải số tuyệt đối. Ví dụ một game cụ thể trong Playbook: churn tăng đột biến (triples) khi fail rate vượt 55% → đó là ngưỡng hard cho game này. Easy là dưới 10-15% fail rate. Medium là khoảng 20-35%.

## Pattern Sau D0

Lion Studios trình bày mẫu pattern điển hình sau D0:

```
Easy → Mid → Mid → Hard → Easy (cooldown) → Warm-up → ...→ Hard
```

Ba thành phần đặc biệt cần lưu ý.

**Cooldown Level** đặt ngay sau hard level. Lion Studios mô tả: "Use easy level to take the pressure out of the player before increase the heat up".

**Warm-up Level** re-increase difficulty từ từ. "Don't cause much fails but players must be careful while playing".

**New Feature Introductions** đặt trước hoặc trong hard level. "New features like boosters and new level elements are introduced prior to or within the hard levels".

Gap giữa 2 hard levels dao động 4-6 levels — không quá gần để tránh churn, không quá xa để giữ pacing.

## Pacing Theo Tenure

Mật độ và difficulty thay đổi theo ngày:

| | D0 | D1 | D2 |
|---|---|---|---|
| Mix | Easy + Mid (chủ yếu) | Mid + Hard | Ít Easy, nhiều Hard + "Harder" |
| Duration | Ngắn | Dài hơn | Peak |
| Hard level đầu | ~Lvl 19-20 | Lvl ~35 | — |
| Interstitial | Sau Lvl 20 + no-ads offer | Sau mỗi level | Sau mỗi level |
| Mục đích | Hook, build expertise | Gradually challenge | Test expertise |

Avg level duration tăng dần theo tenure để match với expertise đang xây.

## Heartbeat Logic

Quote Playbook: "General approach is to let players play 20-25% hard levels out of the levels they play daily. So, if average level per day is 10 for your game, there should be 2 hard levels in your loop of 10 levels. These hard levels should be uniformly distributed."

Ví dụ "Basic Loop" cho 10 levels:

```
Easy → Medium → Medium → Medium → Hard → Easy → Medium → Medium → Medium → Hard
```

Hoặc biến thể có "SuperHard":

```
Easy → Medium → Medium → Medium → Hard → Easy → Medium → Easy → Medium → SuperHard
```

## Nguồn Tham Khảo

- `raw/papers/Lion Studios MVP Guide.pptx.pdf` (slides 11-13)
- `raw/papers/Lion.pdf` (Level Design Playbook, slides 12-13)
