---
title: "RV Placement Strategy"
source: "compiled"
date_added: 2026-05-05
tags: [concept, monetization, rewarded-video, puzzle]
aliases: [rewarded video placement, RV slot]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[easy-level-design]]"
  - "[[booster-design-puzzle]]"
  - "[[level-iteration-testing]]"
  - "[[lion-studios]]"
  - "[[funnel-analysis]]"
  - "[[monetization-dashboard]]"
  - "[[inter-reward-ratio]]"
  - "[[inter-ad-redefinition]]"
summary: "Cách đặt RV slot trong level để monetize mà không cannibalize booster/IAP revenue"
---

## Định Nghĩa

RV (Rewarded Video) là ad format cho phép người chơi xem video để nhận reward trong game. RV placement là việc đặt RV slot ở vị trí và mức độ phù hợp trong level để tối ưu ad revenue mà không cannibalize các revenue stream khác (booster sales, IAP).

Nguyên tắc của [[lion-studios]]: "RV placements should not act as a 'watch-to-win' tool or perceived as a 'blocker'. They should be balanced in a way that makes players' experience easier but still they might need to buy boosters revive etc (no cannibalization!) to complete the level."

## Yếu Tố Quyết Định RV Power

RV power được quyết định bởi 2 yếu tố. Một là amount — bao nhiêu RV slot trong 1 level. Hai là placement — vị trí RV slot trên board, đặc biệt là số neighbor cells.

Ví dụ Playbook minh họa: RV slot central với 6 cells xung quanh là high power; RV slot với chỉ 3 neighbor cells là low power.

## Strategy Theo Level Difficulty

### Easy Levels

RV power có thể maximize (về amount và/hoặc placement). Lý do: trong easy levels, người chơi ít có khả năng monetize qua các elements khác (booster, IAP). RV là chính. Ví dụ Playbook: 3 RVs trong một easy level (max amount).

### Hard Levels — Strategy A: Avoid Churn

Nếu level super hard, RV power tăng để tránh churn. Người chơi có cảm giác có lối thoát, không bỏ cuộc.

### Hard Levels — Strategy B: Focus IAP/Booster

Nếu strategy là focus IAP và booster sales, RV power kept low. Ví dụ Playbook: 1 RV trong hard level với "far reach" (low power) → người chơi phải dùng booster/revive thay vì xem RV. Kết hợp với foreseeable failure trong [[hard-level-design]] để tối ưu booster sales.

## Decision Matrix

| Level Type | RV Strategy | Amount | Placement |
|---|---|---|---|
| Easy | Maximize | High (3+) | Central, high reach |
| Mid | Balanced | Medium (1-2) | Mixed |
| Hard, focus retention | High | High | Central |
| Hard, focus monetization | Low | Low (1) | Edge, far reach |

## Cannibalization Trap

Lion Studios cảnh báo: nếu RV quá powerful trong hard levels, người chơi sẽ luôn chọn "watch ad" thay vì mua booster hoặc IAP. ARPU giảm dù RV revenue tăng. Cần balance theo overall monetization strategy của game — đây là lý do [[booster-design-puzzle]] và RV placement phải thiết kế cùng nhau.

## Validation Qua Data

Trong [[level-iteration-testing]], `RV Shows Per User` là metric chính để identify levels cần action. Best monetized levels có RV cao + churn thấp → nhân bản. Easy levels có RV cực thấp → có thể make harder để cải thiện monetization.

## Nguồn Tham Khảo

- `raw/papers/Lion.pdf` (Level Design Playbook, slides 9-10, 14-15, 26)
