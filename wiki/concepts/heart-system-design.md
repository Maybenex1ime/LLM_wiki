---
title: "Heart System Design — Khi Cần, Khi Không"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, monetization, retention, ux, puzzle-games]
aliases: [heart system, tim, lives system, mạng chơi, energy system]
status: draft
related:
  - "[[fueling-pacing]]"
  - "[[retention-curve-design]]"
  - "[[iaa-iap-migration]]"
  - "[[piggy-bank-monetization]]"
summary: "Heart system là dao hai lưỡi. Cần khi muốn tăng session/day + monetize bottleneck. Không cần khi gameplay đã gây nghiện. Anti-pattern: tim chỉ mua bằng tiền — replace by ad-for-heart. Case Nuts & Bolts (paywall annoy) vs Township → FarmCity (ad-funded 7× progression)."
---

## Định Nghĩa

Heart system (tim, mạng, lives) = bottleneck cho số phiên/lượt chơi. Mỗi lần thua = mất 1 tim. Hết tim = ngừng chơi đến khi hồi (real-time) hoặc trả tiền/ad.

Common trong puzzle games (Candy Crush, Match-3) — đại đa số 5 tim, hồi 30 phút/tim.

## 2 Mục Đích Đối Lập

Giang đặt câu hỏi *"em đang phân vân có nên đưa heart system vào game puzzle của em không."* Vũ chia thành 2 mục đích:

### Mục Đích A — Tăng Số Phiên/Day

Heart limit force user **ngừng chơi giữa session** → quay lại sau khi tim hồi. Hệ quả: tăng số phiên trong ngày, tăng touchpoint với app.

Phù hợp: game **mass-market** muốn user retention spread out across day.

### Mục Đích B — Tăng Thời Gian/Session

Không tim → user chơi liên tục đến khi chán. Hệ quả: tăng thời gian trên mỗi session.

Phù hợp: game **gây nghiện cao**, user sẽ bỏ điện thoại xuống và quay lại tự nhiên.

> *"Nếu bạn tự tin rằng cái gameplay của bạn là gây nghiện — chứ không như người đặt điện thoại nót báo lên làm hoàn thành xong thì đặt vào lại. Chứ sau khi làm việc xong họ sẽ không có lấy lưu khóa lâu."*

## Quy Tắc Quyết Định

| Game Property | Choose | Lý Do |
|---------------|--------|-------|
| **Gameplay gây nghiện** (user nhớ đến app) | Không tim | Bottleneck phá flow, lose retention |
| **Gameplay chỉ chơi khi rảnh** (passive) | Có tim | Force touchpoint, monetize bottleneck |
| **Cần monetize qua bottleneck** | Có tim | Tim = filter user (xem dưới) |
| **Cần increase ad impressions** | Có tim + ad refill | Tăng ad load qua replenish |

## Heart = Filter User (Monetization)

Vũ kể case Nuts & Bolts (OneShot):

> *"Sau khoảng 2 tới 3 lần chơi bị thua mình bắt đầu ngấm ngấm hiểu hiểu cái puzzle đấy. Thì lần cuối cùng mình chơi hết 4 tim... Mình phải để mua với một cái giá nó đắt đỏ so với cả cái behavior tập khách hàng của mình."*

Pattern dụ:
- Level 1-N: user mất ~3 tim để hiểu puzzle (replay rate ~3-4).
- Level cuối tim → user đã invest (sunk cost) → option: trả $1.99 mua tim hoặc lose progress.

Tim = filter sàng lọc whale vs casual:
- User casual → từ bỏ.
- User invested → trả tiền.

Designer chấp nhận **lose volume** để **tăng ARPPU** từ user còn lại.

## Anti-Pattern: Tim Bắt Buộc Mua Bằng Tiền

Vũ behavior cá nhân với Nuts & Bolts:
> *"Tóm lại là sao mình bỏ 1 đô 99, 2 đô 99 không có tài sản gì để quay về thì đối với mình mình không bỏ."*

User cảm nhận: bỏ tiền vào 1 game level mà không có gì để giữ lại → không value → không trả.

### Fix: Ad-For-Heart

> *"Nếu là đặt quảng cáo được tặng tim thì anh sẽ happy hơn."*

User chấp nhận **xem 30s ad** để đổi 1 tim — nhưng không chấp nhận trả $1.99.

Lý do tâm lý:
- Ad = "labor" trả time, không trả tiền túi.
- $1.99 = real money commitment.
- Ad-for-heart cũng tăng **ad load** → IAA revenue cho game ad-funded.

Recommended: heart refill có 3 path — wait (real-time), watch ad (free time), buy gem (real money). Cho user pick path phù hợp behavior.

## Case Township → FarmCity Conversion

Vũ kể trải nghiệm cá nhân — same farm genre, 2 monetization models:

| Game | Model | User Behavior Của Vũ |
|------|-------|----------------------|
| **Township** | Heavy IAP | 1 tháng để qua vùng 1 |
| **FarmCity** (iCame) | Ad-funded (xem ad accelerate) | 4-5 ngày qua vùng 1 |

> *"Có những cái ngày mà nói thật với mọi người là anh chơi đến cả 100 lượt quảng cáo... Anh được khám phá các content sau cũng cảm rất sướng."*

7× progression speed → 7× content discovery → user sướng hơn. Studio đổi **lower per-user revenue** lấy **larger volume + higher retention**.

Caveat: chỉ valid cho dòng game **ad-funded** đã establish. IAP-heavy game không dễ convert sang ad-funded mid-life.

## Khi Nào Skip Hoàn Toàn Heart System

Game không cần tim khi:
- **Single-player narrative** với progress save — user chơi đến khi xong story.
- **Idle/Tycoon** — gameplay đã require "ngừng chơi để wait." Tim redundant.
- **Match-3 với content lớn** + monetize qua booster/IAP — Royal Match dùng pattern này (tim có nhưng rất thừa thải, ít limit).
- **PvP** — cooldown match đã serve role của tim.

## Test Trước Khi Commit

> *"Mình nghĩ thời gian đầu không nên quá cứng về việc là phải có tim. Mà là nên để test cái vấn đề đó."*

Quy trình:
1. **Build prototype không tim** → measure session length + retention.
2. **A/B test** tim ở mid-game (sau khi user đã invest 3-5 levels).
3. **Compare**: ARPPU + retention + churn rate.
4. **Decide** dựa trên KPI thực tế cho game này, không dựa trên "best practice."

Vũ chốt: heart system không có "best practice universal." Decision = test.

## Liên Hệ Wiki

[[fueling-pacing]] cho framework pacing — tim là một dạng forcing pacing. [[retention-curve-design]] cho R1/R3/R7 — tim ảnh hưởng cross-day retention. [[iaa-iap-migration]] cho context tổng quát IAP vs IAA. [[piggy-bank-monetization]] khác monetization gate (tài sản tích lũy) — có thể kết hợp.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Heart System — Khi Nào Cần, Khi Nào Bỏ"
