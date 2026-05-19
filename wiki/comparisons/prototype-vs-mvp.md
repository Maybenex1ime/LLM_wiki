---
title: "Prototype vs MVP"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [comparison, prototype, mvp, phase, game-design]
aliases: [prototype vs MVP, phase dự án, base game vs MVP]
status: draft
related:
  - "[[balance-scale]]"
  - "[[fueling-pacing]]"
  - "[[ltv-cpi-formula]]"
summary: "Prototype phục vụ truyền đạt ý đồ nội bộ (test feelings, base cho comment, sơ khai); MVP đẩy ra thị trường để thu data (đủ loop, đủ minimum, test user thật)"
---

## Bối Cảnh

Học viên Việt Nam thường lẫn lộn 2 bản — đẩy prototype ra test thị trường (sai mục tiêu) hoặc làm MVP ôm quá nhiều feature (kéo dài thời gian). Vũ chốt rõ trong Doc 3:

> *"Pro-time và MVP là 2 bản khác nhau nhé. MVP là gì? Minimum Value Product — tức là cái bản mà các bạn có thể cho user chơi được, nhưng mà nó nhỏ hết có thể. Còn bản pro-time chỉ là bản thử nghiệm thôi."*

## Bảng So Sánh

| Tiêu Chí | Prototype | MVP |
|----------|-----------|-----|
| Mục tiêu | Test idea, truyền đạt ý đồ nội bộ | Đẩy ra thị trường thu data |
| Audience | Team, sếp, người trong công ty | User thực sự ngoài thị trường |
| Mức độ hoàn thiện | Sơ khai — khối tròn, animation chưa có | "Nhỏ hết có thể" nhưng đủ chơi |
| Test cái gì | Gameplay core, feel cốt lõi | CPI, retention, monetization, demographics |
| Budget | Thấp — battle simulation 11 cục tròn | ~$50-$100/ngày × 3-4 ngày test bản không quảng cáo |
| Biến số | **Ít nhất** (1 idea, 1 issue kỹ thuật) | Đủ feature minimum loop |
| Performance | Không kết luận được — phụ thuộc nhiều thứ ngoài | Test trên user thật |
| Output validation | CTR ~80% trong 10 user → idea OK | Retention chuỗi D1-D7, ARPU |

## Phân Tích

### Prototype — Battle Simulation

Vũ minh họa prototype cho game card battle đá bóng (codename "S3"):
- 11 cục tròn (cầu thủ) bên này, 10 cục bên kia.
- Phân loại bằng chỉ số + màu (xanh — bình thường, đỏ — Legend, tím — Epic).
- Bấm auto cho 2 đội đánh nhau → xem có tự generate được một trận bóng không.
- Có tự ghi bàn, kết thúc trận, đá penalty — *"là đủ xong được một cái nghi thức của Prototype."*

Prototype phải có **mục tiêu đơn lẻ và rõ**:

> *"Về nguyên tắc nhé — khi chúng ta muốn chứng minh một cái gì thì tốt nhất là cái biến số của nó ít nhất. Thì nó sẽ biết nó đúng hay sai."*

Nếu prototype không pass → 2 lựa chọn: **bỏ luôn** (nếu thị trường đã có), hoặc **làm hẳn 1 sản phẩm thử** (nếu mình đánh giá là tiềm năng).

### Prototype Là "Base" Cho Comment

Ý nghĩa thứ 2 của prototype: làm base để team đập vào comment, từ đó hình thành scope cho MVP. Comment nhánh:

- **Cách thức triển khai** — auto / auto có skill / auto có chỉ đạo.
- **Scope** — 2D vs 3D, số lượng object, mức độ chi tiết.
- **Item mở** — game sẽ có những loại tài sản nào.

Sau khi base định xong, mới tính được scope: số chip 3D, độ phức tạp animation, đối chiếu với giới hạn performance đã đặt (xem [[asset-hardware-tradeoff]]).

### MVP — Đẩy Ra Thị Trường

MVP phải đủ feature minimum để chơi được, nhưng *"nhỏ hết có thể"*. Khác với prototype:
- Đã có gameplay loop đầy đủ.
- Đã có monetization cơ bản (inter ads, basic IAP).
- Đã có FTUE để user mới onboarding.

Vấn đề thực tế khi test MVP ở Việt Nam: data nhận về từ user chỉ biết quốc gia. *"Chứ còn để phân tích là con số sâu hơn thì rất khó."* Vũ sửa approach: tập user truyền qua [[ltv-cpi-formula|CPI]] chứ không qua demographics sâu.

### Test Không Quảng Cáo

Phần Hiệp đẩy lên — quan điểm gây tranh luận. Cách các studio quốc tế (Voodoo, Lion, Cowally) test:

> *"Phố nó test là nó lạc đầu, thì thường không có quảng cáo luôn. Tại vì sao?"*

Logic: nếu test có quảng cáo từ đầu, không phân biệt được user bỏ vì game không hay (idea kém) hay vì quảng cáo phiền (UX kém). Bản không quảng cáo cho phép đo: user có thực sự **hứng thú** với game không (15-20 phút engagement thuần).

Sau 3-5 ngày test bản không quảng cáo, đẩy bản có quảng cáo → so sánh 2 con để tách 2 biến.

## Kết Luận

Prototype và MVP **không phải 2 phase của cùng 1 sản phẩm** — chúng có mục tiêu khác, biến số khác, audience khác. Designer pha trộn 2 phase sẽ:

- Tốn thời gian prototype quá sâu (vẽ thêm vẽ thêm) khi mục tiêu chỉ là test 1 idea.
- Đẩy MVP quá rộng (nhiều feature) khi mục tiêu chỉ là validate market fit.

Quy tắc Vũ: **prototype = ít biến nhất; MVP = ít feature nhất nhưng đủ loop**.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Prototype vs MVP", "Feelings Trong Prototype", "MVP — Test Gì?", "Mục Tiêu Prototype — Ít Biến Số Nhất"
