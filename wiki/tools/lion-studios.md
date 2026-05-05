---
title: "Lion Studios"
source: "compiled"
date_added: 2026-05-05
tags: [tool, publisher, mobile-games, casual]
aliases: [Lion Studios by AppLovin]
status: draft
related:
  - "[[hard-level-design]]"
  - "[[ftue-curve]]"
  - "[[level-funnel-heartbeat]]"
summary: "Publisher mobile casual games (subsidiary của AppLovin), nổi tiếng với Level Design Playbook và MVP Guidelines cho puzzle game"
---

## Tổng Quan

Lion Studios là publisher mobile casual game, một nhánh của AppLovin. Studio tập trung vào hyper-casual và casual puzzle, với portfolio gồm các tựa như Match Factory, Twisted Tangle, Collect'em All, Unpuzzle, Block Puzzle, Tap Away, Hexa Sort, All in Hole, Car Jam, Screw It Out, Bus Escape: Traffic Jam.

## Vai Trò Trong Wiki

Lion Studios xuất bản hai tài liệu nội bộ định hướng partners thiết kế puzzle game cho monetization dài hạn:

- **MVP Guidelines for Future Hits** (17 trang) — phân loại level difficulty, near-miss, foreseeable failure, và pattern bố trí level theo D0/D1/D2.
- **Level Design Playbook** (32 trang) — playbook đầy đủ về level design, funnel design, mechanic introduction, booster design, iteration testing, và toolkit.

Hai tài liệu này là nguồn chính cho các bài [[hard-level-design]], [[easy-level-design]], [[ftue-curve]], [[level-funnel-heartbeat]], [[booster-design-puzzle]], [[new-mechanic-introduction]], [[timer-design]], [[level-iteration-testing]], [[rv-placement-strategy]].

## Triết Lý Thiết Kế

Lion Studios mô tả sự dịch chuyển chiến lược: từ "tối đa hóa ad revenue trong khi cố giữ retention" sang "monetize users dài hạn qua progressive learning curve và challenging their skills". Hard levels không phải để chặn người chơi mà là currency sink trigger booster/revive usage. Triết lý này khác biệt với hyper-casual truyền thống vốn ưu tiên retention ngắn hạn.

## Lợi Thế / Hạn Chế

Tài liệu Lion Studios mạnh ở số liệu cụ thể (fail rate %, level number, attempt count) thay vì nguyên tắc trừu tượng, kèm reference đến game thực tế trong portfolio để minh họa. Quy trình iteration data-driven (S1-S4 testing phases) bắt buộc cần level database và Looker dashboard.

Hạn chế: benchmark được chuẩn hóa cho level duration 1-2 phút — game khác phải tự calibrate. Targeted vào partners của AppLovin nên một số insight mang tính monetization-first.

## Nguồn Tham Khảo

- `raw/papers/Lion Studios MVP Guide.pptx.pdf`
- `raw/papers/Lion.pdf` (Level Design Playbook)
