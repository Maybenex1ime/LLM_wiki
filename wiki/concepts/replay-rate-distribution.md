---
title: "Replay Rate Distribution — Phân Cực Hay Tập Trung"
source: "[[raw/videos/negaxy-iec-gd-doc-02-level-design]]"
date_added: 2026-05-15
tags: [concept, level-design, replay, user-segmentation, analytics]
aliases: [phân cực replay rate, replay distribution, average không đủ]
status: draft
related:
  - "[[match3-difficulty-levers]]"
  - "[[user-segmentation-3-axes]]"
  - "[[metric-diagnosis-4-methods]]"
  - "[[level-iteration-testing]]"
summary: "Average replay rate (vd 1.3) không đủ thông tin — phải xem phân bổ. Nếu phân cực 1.1 vs 1.5 nghĩa là game đang phục vụ 2 tập user khác nhau, nên tách thành 2 sản phẩm"
---

## Định Nghĩa

Replay rate là metric đo số lần trung bình user chơi lại 1 level. Vũ chỉ ra **average replay rate không đủ thông tin** — phải xem **phân bổ** (distribution) mới biết game đang phục vụ user thế nào.

Cùng một average = 1.3 lần/người, có thể đến từ 2 distribution khác hẳn nhau:

- **Tập trung** (concentrated): phần lớn user ở 1.2-1.4 → 1.3 đại diện được.
- **Phân cực** (bimodal): hai cụm 1.1 và 1.5 lớn nhất → 1.3 không đại diện cho ai.

## Hệ Quả Thiết Kế

### Distribution Tập Trung

Khi replay rate cluster quanh trung bình, game đang phục vụ một tập user khá đồng nhất. Designer fix theo 1 hướng (làm khó hơn, hoặc làm dễ hơn) sẽ ảnh hưởng cả tập một cách đoán được. Quy trình A/B đơn nhánh hợp lý.

### Distribution Phân Cực

Khi có 2 cụm rõ rệt, game đang phục vụ **2 loại user khác nhau** trong cùng 1 sản phẩm:

- Cụm 1.1 = user thấy dễ, không cần thử lại nhiều.
- Cụm 1.5 = user thấy khó, phải thử lại nhiều.

Hậu quả: bất kỳ thay đổi nào cũng hại một nửa user.

- **Sửa khó lên** → cụm 1.5 vất vả → tụt cao.
- **Sửa dễ đi** → cụm 1.1 chán → bỏ.

> *"Sửa khó lên → đội 1.5 vất vả → tụt cao. Sửa dễ đi → đội 1.1 chán → bỏ."*

Giải pháp Vũ đề xuất: **tách thành 2 sản phẩm**, không mix.

## Case Giang — Tách Thành 2 Game

Giang đang triển khai approach này:
- Tách core system giống nhau thành 2 con game: một UI ratio 0.18, một 0.13.
- Cả 2 đều cho metric tốt riêng.
- Trước đây mix 2 vào 1 (kéo 0.13 lên 0.18 trong cùng game) → user *"học UI cũ rồi học UI mới → sai"* → fail.

Vũ nhấn nguyên tắc test methodology: *"Vì anh chỉ thay đổi phần level design thôi mà — đừng thay đổi cái gì khác, nếu không thì anh sẽ không đánh giá đúng."* Một hướng IAP-leaning (~50% IAP), một hướng IAA-leaning (~20% IAP) — không phải đen-trắng.

## Anti-Pattern — Mode Khó Trong Game Dễ

Một số game cố giải bài "phục vụ 2 cụm" bằng cách thêm **mode khó thứ 2** trong cùng 1 con game dễ. Vũ note pattern này failed:

> *"Mấy con dễ đấy có riêng 1 mode chơi khó, 2 mode luôn. Nhưng khá là ít người chơi sang mode 2 đấy."*

Vũ defer lý do user không chuyển mode sang Doc 7 (UX). Tổng quát: user đã *"vào ngữ cảnh dễ"* không tự chuyển sang ngữ cảnh khó — vì gameplay đã set expectation. Tách sản phẩm = cho 2 expectation khác nhau từ trang download.

## Liên Hệ Wiki

Replay rate distribution là một input cho [[user-segmentation-3-axes]] (khung 3 trục phân tập user). [[metric-diagnosis-4-methods]] có method "dimension" tương tự — không tin average, tách theo segment. [[level-iteration-testing]] sử dụng replay rate cùng với churn để identify levels cần action — nhưng trước khi action phải hỏi: distribution thế nào? [[match3-difficulty-levers]] cho các lever cụ thể nếu quyết định fix theo 1 hướng.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Replay Rate Distribution — Phân Cực Nguy Hiểm", "Tách User → Tách Sản Phẩm"
