---
title: "Retention Curve Design — R1/R3/R7 Khác Nhau"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [concept, retention, design, mobile-games]
aliases: [retention curve, R1 R3 R7, in-session vs cross-day retention]
status: draft
related:
  - "[[fueling-pacing]]"
  - "[[daily-login-design]]"
  - "[[notification-management]]"
  - "[[retention-dashboard]]"
summary: "Mỗi mốc retention (R1 = trong session, D1 = ngày sau, D3, D7) cần thiết kế khác. In-session dùng momentum/curiosity hooks; cross-day dùng push noti, daily reward, gated progression"
---

## Định Nghĩa

Vũ phân chia bài toán retention theo các mốc thời gian — *"R0 nó khác, R1 nó khác, R3, R5, R7 nó khác nhau"*:

- **R1 (Section 1 → Section 2)** — trong session: họ chơi xong section đầu, làm thế nào để họ chơi tiếp ngay session sau?
- **D1 → D2** — họ đóng game, ngày hôm sau làm thế nào kéo họ quay lại?
- **D3, D7 retention** — pacing content + reward cho từng ngày khác nhau.

Mỗi mốc cần một thiết kế khác — không có "one strategy" cho toàn bộ retention.

> *"Người thiết kế, họ muốn họ quay lại."*

Vũ nhấn đây là **active design choice**, không phải hệ quả của *"game vui là user tự quay lại"*.

## Phân Loại 2 Tầng

### In-Session Retention (R0 → R1)

User đang trong session, làm sao giữ cho họ chơi tiếp sau khi vừa hoàn thành 1 section?

Techniques:
- **Momentum hooks** — kết thúc section ngay khi reward vừa đẹp → user muốn "thử section tiếp".
- **Curiosity gap** — show preview content section tiếp theo (vd "Boss đáng sợ ở phía trước").
- **Cliffhanger** — fail boss → "thử lại với booster?".

In-session đo bằng số section / session, time-on-task.

### Cross-Day Retention (D1, D3, D7)

User đã đóng game. Làm sao kéo họ mở lại ngày sau?

Techniques:
- **Push notification** — daily reminder, event start.
- **Daily reward / login** — [[daily-login-design]] với 3 mô hình.
- **Gated progression** — content unlock vào timezone cụ thể (vd Battle Pass weekly chapter).
- **Social proof** — "Bạn bè vừa đạt level X" (nếu có friend system).

Cross-day đo bằng D1/D3/D7 retention %, return rate.

## Pacing Content + Reward Theo Mốc

Cho game retention D7 target:

| Mốc | Content | Reward Strategy |
|-----|---------|------------------|
| R1 (in-session) | Section 2 sẵn sàng load nhanh | Reward end-section to make user feel "đáng" chơi tiếp |
| D1 | Có thêm 5-10% content mới so với D0 | Daily reward to *"đẹp lòng"* — đặc biệt với S1 user nhẹ |
| D3 | Mở mode mới, mini-event | Reward escalate so với D1 (xem [[daily-login-design]]) |
| D7 | Unlock content tier mới (PvP, bang hội) | Milestone reward — *"D7 hero unlock"* |

Pacing đúng làm break-even shift từ D3 sang D7 — xem [[fueling-pacing]] và [[d7-vs-d3-breakeven]].

## Liên Hệ Với Notification

[[notification-management]] cho 5 loại noti và priority. Trong context retention design:
- **D1 noti**: Reward (chiều ý user trước) → Mission.
- **D3-D7 noti**: Playable (event mode mới) + Mission (chapter progress).

Designer không spam noti — chỉ noti cái user **chưa biết là có**. Đây là instance cụ thể của *"chỉ noti playable khi user nó quên mất chức năng này thôi."*

## Anti-Pattern — One-Size Retention

Designer mới hay dùng 1 strategy cho mọi mốc retention (vd. "tặng pack daily" cho cả D1, D3, D7). Hệ quả:
- D1 user chưa quen → pack value cao không hiểu.
- D7 user đã quen → pack value vừa thấy bình thường.

Pattern fix: **escalate reward + content theo mốc**. D1 dễ, D3 vừa, D7 hardcore — match với skill và investment user.

## Liên Hệ Wiki

[[fueling-pacing]] cho khung lớn — retention curve là một aspect của fueling. [[daily-login-design]] cho 3 mô hình cụ thể login bonus. [[notification-management]] cho noti strategy. [[retention-dashboard]] (XGAME analytics) cho metric tracking.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Retention Curves R1 → R7 — Bài Toán 'Làm Sao Họ Quay Lại'"
