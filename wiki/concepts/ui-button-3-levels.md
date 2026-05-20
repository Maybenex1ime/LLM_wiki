---
title: "UI Button 3 Levels — Key / Blue / Hidden"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ui, button-hierarchy, priority, thumb-zone]
aliases: [3 level nút, Key Blue Hidden, button hierarchy, levels of priority UI]
status: draft
related:
  - "[[thumb-zone-design]]"
  - "[[ui-wireframe-workflow]]"
  - "[[ui-5-color-brief]]"
  - "[[notification-management]]"
summary: "Vũ phân 3 level button theo priority. Key (gameplay) — thumb zone bottom. Blue (optional) — side panel. Hidden — trong tab/menu. Mỗi level cho phép user prioritize visually. Tùy game: event có thể Key (event-driven) hoặc Blue (optional)."
---

## Định Nghĩa

3 Level Button = framework Vũ chốt để layout UI theo priority. Mỗi level có:
- **Đặc điểm**: functional vs optional vs decorative.
- **Vị trí gợi ý**: thumb zone vs side panel vs collapsed tab.

> *"Cái nào quan trọng thì mình để ra ngoài. Cái nào không quan trọng mình có thể 2 bớt nó đi."*

## Bảng 3 Level

| Level | Tên | Đặc Điểm | Vị Trí Gợi Ý |
|-------|-----|----------|---------------|
| 1 | **Key (Gameplay)** | Không có thì không chơi được | Thanh dưới, 2 lề trái-phải, thumb zone |
| 2 | **Blue (Optional)** | Có thì chơi tốt hơn, không có vẫn được. VD: achievement, event, lucky spin | Vị trí ít quan trọng, side panel |
| 3 | **Hidden (Không Quyết Định)** | Không cần thiết. Có thể giấu / cất vào tab khác | Trong setting menu / collapsed tab |

## Level 1 — Key Button

Button **must-have** để gameplay loop hoạt động.

Examples:
- **Play / Battle** — start match.
- **Home** — quay về main menu.
- **Skill cast** — combat skill button.
- **IAP shop** — monetization-critical.

Vị trí: **thumb zone** (xem [[thumb-zone-design]]).

Visibility: luôn visible trong context relevant. Không giấu, không nhỏ.

## Level 2 — Blue Button

Button **optional** — game vẫn chơi được nếu user skip.

Examples:
- **Achievement** — bonus reward tracking.
- **Daily login** — optional bonus.
- **Lucky Spin** — optional reward.
- **Event banner** — optional content.

Vị trí: side panel (left/right edge), HUD top.

Visibility: visible nhưng không chiếm thumb zone. Có thể có notification badge để thu hút attention.

## Level 3 — Hidden Button

Button **không quyết định** gameplay flow.

Examples:
- **Settings** — language, sound, save.
- **About / Credits**.
- **Help / FAQ**.
- **Privacy policy / Terms**.

Vị trí: ⚙ icon góc top-right hoặc trong setting menu.

Visibility: collapsed by default, expand on demand.

## Game-Specific Re-Classification

Một số button thay đổi level tùy game:

### Event Button

- **Event-driven game** (Coin Master, Royal Match): event = Key Button (event drives daily monetization).
- **Casual game** (Match-3 generic): event = Blue Button (optional).

### Daily Login

- **Game heavy onboarding**: daily login = Key (retention loop).
- **Game F2P deep**: daily login = Blue (nice-to-have).

### IAP Shop

- **F2P game**: Shop = Key (monetization gate).
- **Premium game** (paid up-front): Shop = Hidden hoặc absent.

Designer phải re-classify per game. Default không universal.

## Implementation: Visual Cue

Level cần visual differentiate:

| Level | Size | Color | Animation |
|-------|------|-------|-----------|
| Key | Large | Bold (vàng / xanh dương) | Idle pulse |
| Blue | Medium | Soft (xanh lá / cam) | Static |
| Hidden | Small | Mờ (xám) | None |

Xem [[ui-5-color-brief]] cho convention màu chi tiết.

## Anti-Pattern

- **Key button ở góc trên** — user phải vươn tay → friction → low engagement.
- **Blue button to bằng Key** — user không biết priority → bấm random → wasted action.
- **Hidden button visible always** — clutter UI, dilute attention.
- **Event không classify** — không biết cho event đi đâu trong UI.
- **Levels không update theo game phase** — D0 vs D7 user có khác needs, levels nên switch.

## Re-Classification Theo Game Phase

| Phase | Key Adjustment |
|-------|----------------|
| D0-D3 (onboarding) | Tutorial button = Key |
| D3-D7 (habit forming) | Daily login = Key |
| D7+ (committed) | Event + IAP = Key |
| D30+ (whale) | VIP / sub = Key |

Designer có thể switch levels dynamically theo cohort.

## Liên Hệ Wiki

[[thumb-zone-design]] cho vị trí thumb zone — Key buttons phải nằm trong. [[ui-wireframe-workflow]] cho workflow vẽ UI — apply 3 levels ở Bước 3. [[ui-5-color-brief]] cho convention màu giúp visualize 3 levels. [[notification-management]] cho 5 loại noti — Blue buttons hay có noti badge.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "3 Level Nút Trong UI"
