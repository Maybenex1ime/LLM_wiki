---
title: "Subscription Pack Design"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [concept, monetization, subscription, iap]
aliases: [subscription pack, sub pack, Amanote case]
status: draft
related:
  - "[[iap-purchase-drivers]]"
  - "[[first-iap-strategy]]"
  - "[[fueling-pacing]]"
summary: "Subscription Pack phù hợp game content/view (nhạc, đọc, xem phim) — Amanote 80% revenue từ sub, pay rate 1.3-3%. KHÔNG phù hợp game RPG/Battle vì user không định lượng được $100/tháng giải quyết gì"
---

## Định Nghĩa

Subscription Pack là gói tự trừ tiền định kỳ (tuần / tháng). Giang hỏi Vũ về case **Amanote** (game piano) — game tập trung sub, không IAP.

## Số Liệu Amanote (Vũ 2019)

| Metric | Số Liệu |
|--------|---------|
| Doanh thu từ subscription | ~100% (gần như toàn bộ) |
| Pay rate (sub) | 1.3-1.5% |
| Gói tuần | $5 (giá Vũ biết) |
| Gói tháng | $5 (Vũ note) hoặc $20 (Giang biết) |

Vũ note: số liệu của anh là 2019, không update sau đó nên có thể thay đổi.

## Tâm Lý Mua Subscription

> *"Bản thân những trò chơi kiểu âm nhạc — anh có hỏi bên Amanote lúc trước, họ nói rằng game âm nhạc thì có cái đặc thù là chu kỳ tâm lý của họ khá dài. Yêu giữa có thể chơi 2-3 ngày, sau đó lại nghỉ. Lúc nào cũng quay lại chơi, rồi lại nghỉ. Họ không bỏ."*

Đặc tính game nhạc:
- UX rất tả mát, content không lặp lại được (không thể chơi 3 level cùng 1 bài nhạc).
- Số lượng content yêu cầu cao → bán gói $10-$20 cho 100 bài rất khó.
- Cơ chế sub: 80%+ user không tắt sub *"cho tới khi —"*. Yêu dơ không biết cách tắt. Khi nhận ra bị mất tiền vài lần thì mới tắt.
- *"Lượng tiền họ kiếm được trong cái quá trình kéo dài đấy nói nhiều hơn là việc giá trị họ có thể mua được 1 gói."*

Sub kéo dài vì 2 lý do: friction tắt + user lazy. Cả 2 đều benefit revenue.

## Khi Nào Nên Dùng Subscription

### Phù Hợp

- **Game content/view** (game nhạc, đọc truyện, xem phim, Netflix).
- *"Em đừng tự tưởng — chỉ cần 1 bài hát mới mà mình được chơi là họ đã đủ sướng rồi."*
- Giá trị mỗi ngày tương đương nhau, người ta thấy *"ngày nào cũng nhận được gì đó"*.

### KHÔNG Phù Hợp

- **Game RPG/Battle/AI Giang/Negamon** — *"Người ta không biết là $100 sẽ giải quyết được cái gì cho 1 tháng. Làm sao người ta dám xuống tiền?"*
- Vũ ví dụ: Negamon bán con thú, nhưng không ép subscribe. *"Bọn anh chưa đến mức phải ép người dùng. Mình sẽ chỉ kiểm tra khi con game thật sự tốt."*

### Battle Pass ≠ Sub Thật

Battle Pass / gói 30 ngày của RPG **không phải sub** — chỉ là chưa setup theo kiểu sub. Setup sub thật là khi hết 30 ngày tự trừ tiền, tự tặng lại quà.

Phân biệt:
| | Battle Pass | Subscription Thật |
|---|---|---|
| Trả tiền | 1 lần / 30 ngày | Auto-renew |
| Hết kỳ | User phải mua tiếp | Tự gia hạn |
| Friction tắt | Không có (không cần tắt) | Cần vào setting Apple/Google |
| Lifetime value | Bounded | Cao hơn nhiều |

## Sub Cho Cơ Hội Mua (Wukong)

Vũ kể case **Wukong**: mua skin được khoảng 100 gòn. Sau đó bán cái sub 100 gòn — user mua sub chỉ để được mua skin.

> *"Sub để mua skin đã là quá đáng, đây là sắp để mua cơ hội."*

Pattern này edge-case — sub không cung cấp value trực tiếp mà cung cấp **quyền tham gia** vào hệ thống mua khác. User chấp nhận vì cảm giác "VIP / privileged".

## Bài Học Cho Game Mix IAP + Sub

Giang chia sẻ: game nhạc Giang đang làm vẫn để IAP ngay từ đầu + sub. User chưa kịp trải nghiệm content thì bị show IAP/sub → drop nhiều.

Vũ note bài học từ Amanote 2019: bên Amanote yêu cầu *"game chỉ có sub thôi, cũng quảng cáo hẳn kiếp"*. Game nhạc có bộ phận user *"chỉ là cấm cái tay nghe nhạc"* — quảng cáo lên là khó chịu, rú hầm.

Quy tắc cho game nhạc: hoặc all-in vào sub (Amanote), hoặc tách bạch IAP-only và sub-only. Mix lẫn trong cùng 1 game khiến user paralysis ở moment ra quyết định.

## Liên Hệ Wiki

[[iap-purchase-drivers]] cho 12 driver — sub chủ yếu khai thác driver "content" và "phá giới hạn bản thân". [[first-iap-strategy]] cho 2 trường phái IAP — sub là biến thể của trường phái "giữ giá trị" vì giá đều mỗi tháng. [[fueling-pacing]] cho khung tổng thể — sub là một cách kéo break-even rất xa (D30+).

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Subscription Pack — Case Study Game Nhạc (Amanote)"
