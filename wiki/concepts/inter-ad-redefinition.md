---
title: "Inter Ad Redefinition — Không Phải Để Spam"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [concept, monetization, ads, interstitial, ux]
aliases: [định nghĩa lại inter, inter là phích thời gian, inter không spam]
status: draft
related:
  - "[[inter-reward-ratio]]"
  - "[[rv-placement-strategy]]"
  - "[[fueling-pacing]]"
  - "[[notification-management]]"
summary: "Inter (interstitial ad) là phích thời gian giữa 2 session căng thẳng, không phải bộ đếm level để spam. Đặt inter sai làm user mệt và bỏ; đặt đúng làm user xem mong muốn"
---

## Định Nghĩa

Vũ chỉnh lại tư duy phổ biến của developer Việt Nam về interstitial ads:

> *"Inter, tại sao nó xin làm inter, chắc chắn nó không phải là cái để làm phiền. Chúng ta đang lạm dụng nó một cách xa, biến nó thành một cái làm phiền phải dùng."*

Inter đúng nghĩa phải là:

- **Phích thời gian** cho người chơi dừng lại nghỉ tí và chuẩn bị cho session tiếp theo.
- Quảng cáo phải đúng tác dụng — **người ta xem mong muốn, xem để thư giãn**.
- Sau đó user quay lại tiếp tục với stress (challenge) tiếp theo.

Quote rõ định nghĩa:

> *"Inter nó là quảng cáo, phích thời gian để cho người chơi họ dừng lãng quãng nghỉ tích và bắt đầu trong một chút kì mới."*

## Anti-Pattern — Inter Mỗi Cuối Level

Pattern sai phổ biến: spam inter mỗi cuối level, lạm dụng → user bỏ. Khi inter trở thành *"bộ đếm level"* (level 5 → inter, level 6 → inter, level 7 → inter), user nhận ra mỗi level đều bị quảng cáo → cảm giác bị bóc lột.

GD phải biết "mũ nét gì thì làm" (xem [[fueling-pacing]]) — vị trí quảng cáo phải có thiết kế chủ ý, không chỉ là bộ đếm level. Mỗi inter phải có lý do thiết kế (cuối session căng thẳng, chuyển giữa 2 mode, sau khi user vừa thắng một thử thách lớn).

## Case Hiệp — Logic Giãn Inter

Hiệp test 2 logic giảm density inter:

1. **Logic 1**: Sau 2 level → mới đa 1 inter.
2. **Logic 2**: Sau khi xem 1 quảng cáo → phải khoảng 1 phút sau (hoặc thời gian tối thiểu) → mới hiện inter tiếp theo.

| Phiên bản | Chỉ số D2 | LTV tổng |
|-----------|-----------|----------|
| Logic 1 (giãn theo level) | Tăng 1 chút | — |
| Logic 2 (giãn theo time + level) | Tăng tương đối vượt | LTV tổng kéo ~160-170% |

Logic 2 win vì kết hợp 2 ràng buộc: cách level + cách thời gian. User không thể *"chơi tốc độ cao bù qua"* để bị inter dày đặc. Inter chỉ xuất hiện khi đủ cả 2 điều kiện — tạo cảm giác *"đến giờ giải lao"* hơn là *"bị chặn"*.

## Đặc Biệt Quan Trọng Cho Người Cao Tuổi

Học viên Linh share: *"Em rất hay chơi game với người già. Người già với trẻ nhỏ họ phản ánh rất thật luôn. Khi mà người già chơi lâu họ hay có xu hướng là xem một cái ạt — như kiểu là họ xem ạt họ được giải trí luôn. Họ không ngại khi xem ạt."*

Hệ quả: với segment cao tuổi, có thể dí inter sớm hơn (vd level 4) — nhưng ad phải có **giá trị nội tại với user** (ngoài giải trí), không chỉ chặn ngang gameplay. Đây là một dạng tinh chỉnh inter theo audience — vẫn giữ nguyên tắc "đúng tác dụng" nhưng adjust frequency.

## Liên Hệ Wiki

[[inter-reward-ratio]] là metric đo tỷ lệ inter:reward — quyết định bao nhiêu inter trong tổng ad budget. [[rv-placement-strategy]] (Lion Studios) là tương tự cho rewarded video. [[fueling-pacing]] cho khung lớn — inter chỉ là một lever trong fueling. [[notification-management]] cho thứ tự ưu tiên 5 loại noti, trong đó Ads có vị trí khác Inter.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Định Nghĩa Lại Inter", "Người Cao Tuổi & Tolerance Quảng Cáo"
