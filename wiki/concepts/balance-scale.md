---
title: "Balance Scale — Phân Trọng Số Module"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [concept, game-design, planning, scope, resource-allocation]
aliases: [balance scale, phân tỷ trọng module, trọng số module game]
status: draft
related:
  - "[[prototype-vs-mvp]]"
  - "[[gd-role-as-machine-link]]"
  - "[[imba-balance-meta]]"
summary: "Bảng phân tỷ trọng tài nguyên giữa các module game (core, phụ bản, PvP, sự kiện) tổng = 100%. Khi thêm module mới phải lấy bớt từ module khác, không 'thêm vào trên'"
---

## Định Nghĩa

Balance scale là **sơ đồ phân tỷ trọng tài nguyên** giữa các module game mà Vũ giới thiệu trong Doc 3 để giải quyết bài toán scope. Mỗi module được gán % và tổng phải đúng 100%.

Cấu trúc ví dụ:

```
Core gameplay:         50%
Phụ bản:               10%
PvP:                   20%
Sự kiện / đặc thù:     20%
─────────────────────
Tổng:                 100%
```

Quy tắc: **tổng phải đúng 100%, không có module được "thêm vào trên" mà không lấy chỗ từ module khác**.

## Mục Đích

Balance scale dùng cho 2 quyết định:

1. **Resource development** — bao nhiêu phần trăm thời gian/người dồn vào core vs vào mode phụ.
2. **Lock priority khi feature creep** — nếu mode mới đề xuất > 10% trọng số phụ bản, phải cắt bớt thứ khác. Không có *"chúng ta sẽ làm thêm cái này"* — phải hỏi *"chúng ta sẽ bớt cái nào"*.

Đây là một công cụ cụ thể cho [[gd-role-as-machine-link]] — GD phải define trước thay vì để các nhóm tự thêm ý tưởng vào.

## Vẽ Đồ Thị Trọng Số Theo Level

Vũ phản hồi anti-pattern "thiếu tiền bù tiền" (designer chờ user thiếu rồi thêm reward 1.000V) bằng đề xuất proactive:

- Mỗi module có trọng số riêng (50%, 10%, 20%, 20%).
- Vẽ đồ thị theo level — level 20 mở module mới, level 25 đo tham trạng user trong main → đẩy lượng resource phân cực sang module phụ.

> *"Thay vì cái việc là mình cứ đi tới đâu rồi mình bắt đầu thêm — mình sẽ làm cái số này có một cái tương quan nhất định để mình biết là mình nên đẩy vào đây là khoảng bao nhiêu."*

Khác biệt cốt lõi: reactive ("user thiếu thì thêm") vs proactive ("vẽ trọng số theo level trước, theo đó allocate reward"). Reactive khiến designer chạy theo user; proactive cho designer kiểm soát expectation.

## Anti-Pattern — Lái Theo User

Quote phân tích case học viên:

> *"Cách này khiến cho bọn em đang chạy một cái vòng mà suốt ngày phải đuổi theo với việc là user đang làm cái gì."*

Khi không có balance scale, designer luôn ở thế bị động — thiếu tiền vào thì cắm thêm, sự kiện thấp ngày thì bù event, mode chính chậm thì gấp gáp. Balance scale fix bằng cách **lock priority** trước khi nhìn data.

## Liên Hệ Wiki

[[prototype-vs-mvp]] là context: balance scale là sản phẩm cuối của quá trình scope sau khi prototype confirm direction. [[imba-balance-meta]] là instance cụ thể của balance scale — phải giữ MTV (Material Target Value) tại checkpoint cân bằng với power user. [[gd-role-as-machine-link]] là triết lý — define trước, không reactive.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Balance Scale — Phân Trọng Số Module", "Thêm Tính Năng Mới — Có Ảnh Hưởng Gameplay Không?"
