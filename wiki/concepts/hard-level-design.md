---
title: "Hard Level Design"
source: "compiled"
date_added: 2026-05-05
tags: [concept, level-design, puzzle, monetization]
aliases: [thiết kế level khó, hard level]
status: draft
related:
  - "[[easy-level-design]]"
  - "[[level-funnel-heartbeat]]"
  - "[[rv-placement-strategy]]"
  - "[[booster-design-puzzle]]"
  - "[[lion-studios]]"
summary: "Hard level trong puzzle game là currency sink để trigger booster/revive — không phải để chặn người chơi"
---

## Định Nghĩa

Hard level là level có average attempts to complete trên 1.7 lần (theo phân loại của [[lion-studios]]). Mục tiêu thiết kế hard level không phải tạo rào cản mà tạo currency sink: trigger usage của booster (trước khi fail) và revive (sau khi fail). Lion Studios mô tả: "These levels aim to create currency sink by triggering revive and booster usage. It's also likely these levels to be the ones that usually end the sessions."

Quy tắc cốt lõi: average attempts to complete nên trong khoảng 2-3 attempts — không bao giờ "impossible to pass".

## Ba Nền Tảng Của Hard Level

Lion Studios Level Design Playbook đặt ra 3 nền tảng phải có cùng lúc.

**Replayability.** Level phải có nhiều paths/strategies để người chơi muốn thử lại sau khi fail. Quote Playbook: "If you have multiple paths in your gameplay, players tend to give more attempts to try these possibilities". Ví dụ Bus Escape: Traffic Jam dùng 3 blue buses cho phép start với 3 directions khác nhau trong cùng 1 level.

**Heartbeat Within A Level.** Trong một level, độ căng phải có flow tension/relief. Ví dụ Playbook: level bắt đầu khó sẽ release tension sau ~10 moves; level bắt đầu dễ sẽ intensify tension sau ~10 moves. Pattern này khác với heartbeat của funnel — xem [[level-funnel-heartbeat]] cho heartbeat giữa các levels.

**Perceived Difficulty.** Cùng fail rate, level có perceived difficulty cao hơn sẽ tạo 2.5x RV watch. Playbook chỉ ra ví dụ: 2% fail rate + 1 RV cell với perceived high → 2.5x RV watch so với 4% fail rate + 2 RV cells với perceived low. Cảnh báo: với early levels, perceived high difficulty có thể dẫn đến churn vì người chơi chưa có resistance.

## Cơ Chế Monetization

**Near-Miss.** Đặt blocker để fail xảy ra sau khi đã hoàn thành ~60-80% level. Quote: "The closer failure moment to level end, more you get booster sink and revive adoption". Lý do: cảm xúc "suýt nữa thì xong" trigger revive.

**Foreseeable Failure.** Cho người chơi thấy trước fail đang đến, có khoảng thời gian giữa "stuck" và "fail triggered". Quote: "Player is aware that placing any tiles will trigger a fail. This provides a room for them to consider booster usage". Đây là window để bán booster — xem [[booster-design-puzzle]].

Hai cơ chế này phải dùng đồng thời. Near-miss tạo cảm xúc revive sau fail. Foreseeable failure tạo cơ hội booster trước fail. Thiếu foreseeable → mất window booster. Thiếu near-miss → cảm xúc đáng tiếc thấp, ít ai bấm revive.

## Adaptive Difficulty

Sau fail thứ 2-3, có thể nới lỏng difficulty để giảm churn — nhưng không quá mạnh, vì sẽ hại revenue. Match Factory giảm relevance của items sau lần fail thứ 2. Collect'em All tặng +1 move mỗi lần fail từ lần thứ 2 trở đi. Quote MVP Guide: "Be aware that significantly lowering the difficulty may also harm your revenue".

## Vị Trí Hard Level Đầu Tiên

Trong [[ftue-curve]], hard level đầu tiên xuất hiện khoảng Lvl 11-14 (fail rate 15%) với mục đích introduce upcoming challenges, không phải monetize. Hard level thực sự để monetize bắt đầu từ D1 trở đi với mật độ 20-25% trong loop hằng ngày.

## Nguồn Tham Khảo

- `raw/papers/Lion Studios MVP Guide.pptx.pdf` (slides 5-9)
- `raw/papers/Lion.pdf` (Level Design Playbook, slides 6-10)
