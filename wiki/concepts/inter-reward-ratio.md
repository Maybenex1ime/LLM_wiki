---
title: "Inter:Reward Ratio (Y:R)"
source: "[[raw/videos/negaxy-iec-gd-doc-02-level-design]]"
date_added: 2026-05-15
tags: [concept, monetization, ads, inter, rewarded-video]
aliases: [Y:R ratio, inter reward ratio, tỷ lệ inter reward]
status: draft
related:
  - "[[inter-ad-redefinition]]"
  - "[[rv-placement-strategy]]"
  - "[[ltv-cpi-formula]]"
  - "[[fueling-pacing]]"
summary: "Tỷ lệ giữa interstitial ads và rewarded video ads trong session — fix tổng ad/day rồi A/B tỷ lệ, 8:2 vs 7:3 không có đúng/sai mà phụ thuộc retention"
---

## Định Nghĩa

Inter:Reward ratio (ký hiệu Y:R) là tỷ lệ giữa **số interstitial ads** (ad chèn ngang, không có reward) và **số rewarded video ads** (RV — user xem để nhận thưởng) trong một session hoặc một ngày chơi.

Vũ và Hiệp đồng quan điểm: **fix tổng ad/day** trước để giữ retention, sau đó A/B tỷ lệ phân bổ giữa inter và reward. Ví dụ:

- Target ratio: 7:3 (7 inter + 3 reward = 10 ads/day).
- Thực tế đo được: 8:2 (8 inter + 2 reward).

## Hai Phản Ứng Khi Ratio Lệch

Vũ note **không có đúng/sai** — phải A/B:

1. **Duy trì 8:2** nếu metrics OK (retention không tụt, ARPDAU tăng).
2. **Điều chỉnh về 7:3** bằng cách *"làm level khó hơn lên và yêu cầu ép vào reward"* — buộc user xem reward để qua level. Tăng R bằng cách tăng demand cho reward, không phải tăng supply.

## Anti-Pattern — Làm Dễ Để Tăng Reward

Lỗi pattern phổ biến học viên mắc: *"Em nói là để cho user nó chơi nhiều hơn thì em muốn làm nó dễ đi. Tức là nếu em làm khó lên thì thời gian chơi sẽ tụt xuống, nhưng reward sẽ tăng lên — không chắc làm tăng R."*

Logic sai: làm dễ → user chơi nhiều level hơn → nhiều inter hơn. Nhưng reward không tăng vì user không cần reward khi level dễ. Kết quả: tổng ads tăng (nhiều inter spam), retention tụt vì user mệt inter — net negative.

Logic đúng: làm khó hơn ở một số điểm có chủ đích → user cần reward để qua → R tăng. Inter có thể giảm theo (vì user chơi ít level hơn) nhưng total ads/user giữ nguyên hoặc cao hơn về mặt giá trị (RV có eCPM cao hơn inter).

## Tower Defense Case — Khó Hơn Có Thể Tốt Hơn

Câu chuyện Vũ kể (counter-intuitive): một con TD có tỷ lệ reward/inter rất cao, nhưng tổng số inter thấp → user chơi ít.

**Diagnosis sai (intuitive)**: khó quá không chơi được → làm dễ đi.

**Hậu quả khi làm dễ**:
- User xem reward để lấy tài sản.
- Tài sản dùng không thấy tác dụng (vì level đã dễ rồi).
- Mất mục tiêu phấn đấu → bỏ game.

**Fix thực tế**: tăng độ khó → tài sản trở nên hữu dụng → revenue tăng.

Quote Vũ: *"Mình không hề khẳng định với các bạn là sẽ làm khó lên hay là dễ đi thì sẽ ra tiền. Mình chỉ nói là các bạn nên thử test khó lên hoặc dễ đi, sau đó đưa ra định hướng."*

## Tính Inter:Reward Trong D3 Planning

Học viên áp dụng Y:R vào tính lượng ad day target:
- Ngày đầu: mỗi 5 level → 1 ad. Cần 4 ad/ngày → cho user 5-6 mạng.
- Thời gian hồi mạng quyết định pacing — ngắn để user quay lại nhiều lần, nhưng có giới hạn để không gây mệt mỏi.

Y:R là một input của [[ltv-cpi-formula]] (tổng impression tính theo Y:R × retention chain).

## Liên Hệ Wiki

[[inter-ad-redefinition]] giải thích Inter không phải để spam mà là phích thời gian — phân biệt giữa "thêm inter spam" (sai) và "thêm inter có thiết kế" (đúng). [[rv-placement-strategy]] (Lion Studios) là tham chiếu cho cách đặt RV slot trong level. [[fueling-pacing]] là context lớn hơn — Y:R chỉ là một lever, fueling tổng thể bao gồm cả IAP pacing.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Inter : Reward Ratio (Y:R)", "Tower Defense Case"
- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Inter:Reward Ratio Trong D3 Planning"
