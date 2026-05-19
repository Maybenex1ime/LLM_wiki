---
title: "IAP Purchase Drivers — Vì Sao User Pay"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [concept, monetization, iap, psychology, drivers]
aliases: [drivers IAP, vì sao user pay, 12 driver IAP, why people pay]
status: draft
related:
  - "[[iap-pricing-user-value]]"
  - "[[feeling-of-assets]]"
  - "[[hidden-variable-difficulty]]"
  - "[[user-segmentation-3-axes]]"
summary: "Các động cơ khiến user IAP: giải quyết vấn đề liên tục, time-starve solve, aesthetic, social validation, phá giới hạn bản thân, rich-user impulse. Doc 7 mở rộng thành 12 driver"
---

## Định Nghĩa

Vũ phân tích các động cơ IAP (in-app purchase) qua case study + driver list. Nguyên tắc cốt lõi:

> *"Làm thế nào để người ta giải quyết vấn đề liên tục — khi người ta giải quyết vấn đề liên tục thì người ta mới phát sinh IAP liên tục."*

IAP không phải hoạt động "chốt 1 lần lớn" mà là **chuỗi quyết định nhỏ liên tục**. Designer phải tạo ra **chuỗi vấn đề** để chuỗi IAP có lý do tồn tại.

## Drivers Cốt Lõi (Doc 4)

### 1. Giải Quyết Vấn Đề

Battle game: user stuck với boss → mua chỉ số ATK → vượt → next problem. Mỗi IAP giải 1 vấn đề cụ thể, sau đó vấn đề tiếp theo xuất hiện.

Continuous friction pattern (Buzo - con micro-pack): mỗi vấn đề nặng nhỏ nhưng liên tục → nạp liên tục, không nạp 1 cú lớn. *"Cái lượng nặng của nó rất nhỏ nhưng nó lại nặng nhiều — nó nặng liên tục nhiều."*

### 2. Time-Starve Solve

Idle game: user không có thời gian cày → mua hạt / tăng tốc. Đây là *"bán thời gian"* — user trả tiền để skip waiting.

### 3. Aesthetic / Skin

Mua vì đẹp, không cần solve gì. User trẻ và rich user driver chủ yếu. Skin pricing flexible vì không có baseline content value.

### 4. Social Validation / Leaderboard

> *"Trong leaderboard ai vượt qua nhiều level nhất, sâu về trước mặt tất cả mọi người. Con người luôn có tư duy là không có kém bất kỳ ai — đặc biệt là khi họ đã hòa vào con game của mình rồi."*

User trả tiền để giữ rank, không phải để chơi tốt hơn. Driver mạnh nhất ở game competitive.

### 5. Phá Giới Hạn Bản Thân

Buzo game, ASMR no-fail: *"Tôi luôn muốn vượt qua giới hạn của bản thân mình — phải nói chí tuệ về bất kỳ một cái gì."*

Driver intrinsic — user mua để chứng tỏ với chính mình. Không có social audience.

### 6. Rich User Mua Vô Tư

*"Cứ thích thì mua. Mục tiêu là quay tiktok."*

Whale driver. Không sensitive về pricing, không cần justification. Tỷ lệ user nhỏ nhưng revenue chiếm đại đa số ở nhiều game.

## 12 Driver Mở Rộng (Doc 7)

Doc 7 mở rộng thành 12 driver cụ thể hơn:

1. Thua + cần thắng (giải quyết tình huống).
2. Tiêu / thêm tài nguyên.
3. Rút ngắn thời gian chơi.
4. Gacha (sở hữu tài sản).
5. Buster (thua).
6. Content.
7. Sở hữu tài sản.
8. Đi tìm bóng (random reward).
9. Cạnh tranh.
10. Sợ lỡ cơ hội (FOMO).
11. Ganh đua → tăng sức mạnh.
12. Lợi ích / profit so sánh.

Phần lớn 12 driver này map về 6 đặc tính tài sản trong [[feeling-of-assets]] — đặc biệt là khan hiếm (FOMO), khoe tài sản (cạnh tranh, social), số lượng (sở hữu, gacha).

## Map Driver → IAP vs Ads

Doc 7 (UI/UX/Monetize) đưa ra quy tắc:

| Driver | Khuyến cáo |
|--------|------------|
| Thua + giải quyết tình huống tức thời | Ads > IAP |
| Thiếu tài nguyên ít | Ads |
| Thiếu tài nguyên nhiều | IAP |
| So sánh profit (gói tổ hợp) | IAP thuần |
| Sở hữu tài sản (sinh giá trị) | IAP |
| Rút ngắn thời gian chơi | Ads |
| No Ad | IAP only |
| Thêm content | IAP (có thể mix Ads để test demand) |

Lý do: Ads phù hợp khi cảm xúc *"không sinh giá trị tài sản tay cầm"* (rút ngắn, giải quyết tức thời). IAP phù hợp khi tạo ra *"tài sản tay cầm"* (sở hữu hero, gói tổ hợp).

## Liên Hệ Wiki

[[iap-pricing-user-value]] cho công thức định giá theo journey value. [[feeling-of-assets]] cho 6 đặc tính tài sản mà drivers khai thác. [[hidden-variable-difficulty]] giải thích cách giữ "vấn đề liên tục" sau IAP — không hide khó thì user mua xong dễ quá → bỏ. [[user-segmentation-3-axes]] cho khung phân tập user — mỗi tier (T2/T3/T4) có driver primary khác nhau.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "IAP Design — Why People Pay", "Continuous Friction Pattern"
- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "12 Driver Quyết Định Xem Ad / IAP", "Quy Tắc IAP vs Ads Theo Trường Hợp"
