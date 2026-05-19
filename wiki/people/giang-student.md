---
title: "Giang — Học Viên Case Study Lặp Lại"
source: "compiled"
date_added: 2026-05-15
tags: [person, student, case-study, game-designer, vietnam]
aliases: [Giang IAA IAP, Giang Pull-the-Pin]
status: draft
related:
  - "[[vu-negaxy]]"
  - "[[hiep-iec]]"
  - "[[negaxy-iec-gd-course]]"
  - "[[replay-rate-distribution]]"
  - "[[imba-balance-meta]]"
summary: "Học viên có nhiều dự án dài hạn đang vận hành — case study lặp lại qua nhiều buổi (Whale Content Burn, IAA→IAP migration, Pull-the-Pin multivariable, gói tướng meta, music game subscription)"
---

## Tiểu Sử

Giang là học viên có nhiều dự án thực tế đang vận hành trong khóa Game Design Course by Negaxy + IEC. Case study của Giang xuất hiện ở Doc 1, Doc 2, Doc 3, Doc 4, Doc 7, Doc 8 — gần như mọi buổi.

Background tiết lộ qua case:
- **Đã làm hyper sang hybrid** (model 2 studio "GAC-like" được Vũ và Giang trao đổi trong Doc 1).
- **Đang vận hành dòng game level-base** với IAA-leaning revenue (Doc 2).
- **Đã tách core system thành 2 con game** với UI ratio khác nhau (0.18 vs 0.13, IAP-leaning ~50% vs IAA-leaning ~20%).
- **Có game với hero/unit tower-base** (Halo / tower-base RPG units, Doc 4 — case RPG unit weakness).
- **Có game nhạc** đang phát triển mix IAP + sub (Doc 7).
- **Có game ERP có content tốt** (Doc 3 — chia sẻ về D7 hoà bền hơn D3 hoà).

Phong cách trong lớp: hỏi sâu, đưa case cụ thể, sẵn sàng phản biện Vũ và Hiệp. Vũ và Hiệp thường tương tác trực tiếp với Giang để bóc tách giả thiết.

## Đóng Góp Case Study

Các framework wiki được build từ case Giang:

- **Whale Content Burn** (Doc 2) — case whale ngày D2 nạp $400 burn 30-day content trong 5 ngày → bài toán content gating cho pay user. Liên quan [[imba-balance-meta]].
- **IAA → IAP Migration** (Doc 2, Doc 3) — case dòng level-base hyper → hybrid. Tech 2 server-side detect user pattern. Liên quan [[iaa-iap-migration]].
- **Replay Rate Distribution** (Doc 2) — tách thành 2 sản phẩm với UI ratio khác nhau thay vì mix 2 vào 1. Liên quan [[replay-rate-distribution]].
- **Pull-the-Pin Multivariable** (Doc 4) — case difficulty không tính được bằng công thức, phải test thực tế. Liên quan [[level-data-vs-handcrafted]].
- **Gói Tướng Meta Imbalance** (Doc 3) — case bán gói cuối sở hữu toàn bộ tướng meta → mất giá trị progression. Liên quan [[imba-balance-meta]].
- **Music Game Subscription** (Doc 7) — case Amanote-style, hỏi khi nào dùng sub. Liên quan [[subscription-pack-design]].
- **D7 Hoà Bền Hơn D3** (Doc 3) — phản biện Vũ, được Vũ xác nhận đúng. Liên quan [[d7-vs-d3-breakeven]].

## Quan Điểm Nổi Bật

- **Damage tiềm năng của GD cao nhất trong team** (Doc 1): *"Các bạn art hay dev nếu làm sai thì chỉ một mình các bạn đi làm lại. Nhưng GD làm sai thì tất cả các bộ phận khác phải đi sửa lại."* Insight rút từ kinh nghiệm tuyển GD.
- **Tách 2 sản phẩm thay vì mode khó trong cùng game** (Doc 2): đã thử mix 2 UX ratio trong cùng game và fail.
- **D7 hoà bền hơn D3 hoà** — đối nghịch quan điểm tối ưu sớm.
- **Quay quảng cáo không cần là game thật** (Doc 1): chia sẻ technique level đặc biệt kỳ cục chỉ để quay video.

## Phong Cách

Giang khác đa số học viên khác ở chỗ:
- Đưa case có **số liệu cụ thể** (whale $400 D2, ratio 0.18 vs 0.13, content gating timeline 30 ngày).
- **Sẵn sàng phản biện** lecturer — D7 vs D3 case là điển hình.
- Đặt câu hỏi từ **multi-product perspective** (kế hoạch tách 2 game), không chỉ single-game tuning.

## Liên Hệ Wiki

[[vu-negaxy]] và [[hiep-iec]] là lecturer khóa. [[negaxy-iec-gd-course]] là context. Phần lớn case Giang được Vũ/Hiệp gọi tên trong khi giảng → các concept wiki có "Case Giang" subsection.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Bài Toán Của Giang — IAA → IAP Migration", "Whale Content Burn"
- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Day 7 Hoà Dễ Scale Hơn Day 3 Hoà", "Imba/Balance Gói Meta"
- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "Bài Toán Của Giang — Multivariable Không Tính Được", "RPG Unit Design"
- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Subscription Pack — Case Study Game Nhạc (Amanote)"
