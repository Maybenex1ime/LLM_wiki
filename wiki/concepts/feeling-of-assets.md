---
title: "Feeling Of Assets — 6 Đặc Tính Đánh Vào Tâm Lý Tài Sản"
source: "[[raw/videos/negaxy-iec-gd-doc-02-level-design]]"
date_added: 2026-05-15
tags: [concept, monetization, psychology, asset, iap]
aliases: [đặc tính tài sản, 6 đặc tính tài sản, đánh feeling tài sản]
status: draft
related:
  - "[[iap-purchase-drivers]]"
  - "[[iap-pricing-user-value]]"
  - "[[user-archetype-asset-vs-self-expression]]"
  - "[[user-segmentation-3-axes]]"
summary: "6 đặc tính tài sản (số lượng, chất lượng, khan hiếm, achievement, khoe tài sản, giá trị tăng theo thời gian) — designer dùng để define cách monetize tài sản trong game"
---

## Định Nghĩa

Vũ chốt phần "tài sản" của Doc 1 bằng cách dịch chuyển từ "có tài sản nào" sang **cách đánh vào feeling của tài sản**. Đây là 6 đặc tính tâm lý mà tài sản trong game (hero, skin, item, currency, decoration...) khai thác:

## 6 Đặc Tính

### 1. Số Lượng

Ai cũng muốn nhiều. Quyết định mà GD phải trả lời:
- Reward cho nhiều hay ít?
- Gói IAP bán nhiều hay ít?
- Số lượng tài sản hiển thị trên home (1 hero hay 50 hero)?

Đặc tính này gắn với [[asset-hardware-tradeoff]] — không thể bán "100 hero hiển thị cùng lúc" trên iPhone đời cũ.

### 2. Chất Lượng / Phân Cấp

Khi game có nhiều tier (Legendary → Epic → Rare → Common), designer phải chọn bán cấp nào.
- Bán Common pack → ai cũng mua được, giá trị cảm nhận thấp.
- Bán Legendary pack → ít người mua, giá cao, mỗi gói là sự kiện.

Một số game pin chất lượng ngay từ ô đại diện (avatar khung Legendary phát sáng) để khai thác cảm xúc.

### 3. Khan Hiếm

Có 2 dạng:
- **Khan hiếm tự nhiên** (cap cứng) — số lượng giới hạn vĩnh viễn.
- **Khan hiếm theo progress** — *"level 50 nó không hiếm nữa"*. Bán cho người mua sớm để leapfrog đến level 50 trước.

Khan hiếm theo progress là vũ khí mạnh nhất — designer kiểm soát timeline khan hiếm bằng cách điều chỉnh tốc độ progression.

### 4. Achievement

Bày ra home, hoặc *"nhét trong trên mình riêng"* (achievement page riêng). Khi user xem lại được những gì đã đạt → motivate tiếp.

Achievement có thể là tài sản ảo (badge, title) — không tốn server resource nhưng có giá trị tâm lý.

### 5. Khoe Tài Sản

Game farm là ví dụ điển hình: bày tài sản (tượng lợn vàng, nhà tráng tác dụng) lên đất để khi người chơi khác thăm thì thấy *"mức độ giàu có, mức độ cống hiến cho game"*.

Quote Vũ về lý do đặt: *"Vì sao đánh vào yếu tố tài sản? Nên lúc trước mình nói: khi các bạn list hết tất cả yếu tố liên quan con game ra, thì các bạn sẽ làm được cái này."*

Khoe tài sản đòi hỏi 2 yếu tố cùng có:
- Cơ chế **show off** (visit friend, leaderboard, public profile).
- **Asymmetric visibility** — user A thấy tài sản user B nhưng B không buộc thấy A. Tạo cảm giác *"phải khoe để được nhìn"*.

### 6. Giá Trị Tăng Theo Thời Gian

Đặc tính nhóm game đặc thù — Vũ note ít dùng nên bỏ qua. Ví dụ: hero level càng cao càng quý (vì khó level up lại nếu mất), pet age càng lâu càng đắt.

Phần lớn game mobile không tận dụng đặc tính này vì player turnover cao. Phù hợp game social/sandbox có lifetime dài.

## Áp Dụng Vào Design

Khi GD list tài sản trong game, mỗi tài sản phải được hỏi: **6 đặc tính nào đặc tính nào áp được?** Tài sản không có đặc tính nào → có thể không cần tồn tại.

Ví dụ matrix cho 1 hero card RPG:
| Đặc Tính | Áp Vào Hero Card? | Cách Triển Khai |
|----------|----|------------------|
| Số lượng | Có | Collection page, *"đã thu thập 12/50"* |
| Chất lượng | Có | Rarity tier (SSR/SR/R) |
| Khan hiếm | Có | Limited banner, time-gated |
| Achievement | Có | Hero milestone badge |
| Khoe tài sản | Có | Show on friend list, PvP avatar |
| Giá trị tăng theo thời gian | Tùy | Hero level rare reset |

## Liên Hệ Wiki

[[iap-purchase-drivers]] cho 12 driver chi tiết tại sao user IAP — phần lớn drivers map về 6 đặc tính này. [[iap-pricing-user-value]] cho khung định giá theo content-value gói mở ra. [[user-archetype-asset-vs-self-expression]] (comparison) cho 2 archetype trong [[user-segmentation-3-axes]] — nhóm tài sản chính là nhóm primary cho monetization các đặc tính này.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Tiếp Nối Doc 1: Đánh Vào Feeling Của Tài Sản"
