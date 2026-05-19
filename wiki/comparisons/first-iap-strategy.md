---
title: "First-IAP vs Giữ Giá Trị — 2 Trường Phái Pricing"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [comparison, monetization, iap, pricing, first-time-purchase]
aliases: [first-IAP, giữ giá trị, x2 vs x8, first-time purchase strategy]
status: draft
related:
  - "[[iap-pricing-user-value]]"
  - "[[iap-purchase-drivers]]"
  - "[[dark-ux-techniques]]"
summary: "First-time IAP: x2 (giữ giá trị cân bằng với gói sau) vs x8 (tối đa convert, ép user vào trạng thái paying). Anti-pattern: lỡ cỡ giữa — gói đầu vừa không hấp dẫn vừa làm gói sau khó bán"
---

## Bối Cảnh

Vũ đặt câu hỏi cốt lõi cho monetize trong Doc 7:

> *"Câu hỏi ở đây khác nhau. Mọi người sẽ phải đưa ra 1 quyết định ngay từ ban đầu trong lúc mùa chích kế: mọi người muốn có số ít user nạp tiền nhiều, hay muốn có số nhiều user nạp?"*

Có 2 trường phái chính khi định giá gói IAP đầu tiên (first-time purchase) — chọn 1 trường phái phải lock từ đầu, không trộn lẫn.

## Bảng So Sánh

| Tiêu Chí | Cách 1 — Giữ Giá Trị (x2) | Cách 2 — First-IAP (x8, +85%) |
|----------|----------------------------|--------------------------------|
| Giá trị gói đầu | x2 normal value | x8 normal value (hoặc cao hơn) |
| Mục tiêu | Cân bằng tỷ lệ với gói sau | Tối đa convert free → paying |
| Convert rate | Vừa phải | Cao |
| Gói thứ 2 trở đi | Dễ bán (giá trị tương đối hợp lý) | Khó bán (gói đầu đã quá rẻ) |
| ARPPU | Tăng dần qua tier | Spike ở gói đầu rồi flat |
| Whale potential | Cao — whale leo dần tier | Thấp — không có lý do leo tier |
| Phù hợp | Game lifetime dài, RPG/strategy | Game lifetime ngắn, casual |
| Rủi ro | Convert rate thấp ban đầu | Mất giá trị tier sau |

## Phân Tích

### Cách 1 — Giữ Giá Trị (x2)

Lý do chọn:
- Nếu first-time x8 → user so sánh gói $1 với gói $10 sau đó → thấy đắt → không nạp tiếp.
- Giữ tỷ lệ giá trị giữa các tier IAP cân bằng (gói 1 / gói 2 / gói 3 đều thấy "đáng giá").

Phù hợp với game muốn xây dựng paying ladder dài hạn — user leo từ T0 → T2 → T5. Mỗi tier có lý do tồn tại riêng.

### Cách 2 — First-IAP (x8, +85%)

> *"Chỉ cần user bỏ gói đầu rồi là đã làm game thành công rồi."*

Lý do:
- Gói đầu rất rẻ với giá trị cao → tỷ lệ convert lớn.
- User chuyển từ "free user" sang "paying user" → tâm lý thay đổi → dễ mua tiếp.

Trade-off: gói thứ 2 rất khó convert vì gói đầu đã giá trị quá cao. ARPPU dồn vào gói đầu, các gói sau flat.

Phù hợp game muốn tối đa convert rate, mỗi user "đẹp nhất phá hết" — quality over lifetime.

## Anti-Pattern — Lỡ Cỡ Giữa

Vũ cảnh báo:

> *"Mọi người hay bị cái lỡ cỡ ở giữa — đưa ra gói first time ban đầu cũng không hấp dẫn lắm nhưng giá trị lại cao. Dẫn tới cái tập khách hàng về sau: số lượng người trả gói đầu không được cao, mà những người đi sau cảm thấy gói đầu vẫn bị đắt, các gói sau vẫn bị đắt."*

Vấn đề lỡ cỡ giữa:
- Gói đầu **x4** (giữa x2 và x8): không đủ rẻ để spike convert, không đủ cân bằng để giữ tier về sau.
- User free thấy không đủ hấp dẫn → không mua.
- User đã pay thấy gói đầu *"đã rẻ"* nên gói sau tưởng đắt → không nạp tiếp.

Quy tắc: pick 1 trong 2 trường phái rõ ràng, không pha trộn.

## Bí Quyết — Bán Cái Không So Sánh Được

Học viên (game Battle Royale style của Hiệp/Tài) chia sẻ pattern bán **upgrade choice**: thay vì 3 skill khi lên level → 4 skill. Gói này không thể so sánh được với gói tài nguyên thông thường.

Pay rate: **gần 1%**. Trong số người mua, gói đó chiếm **80-90%** (cao bất thường so với gói khác chỉ 10-20%).

Pattern này phá ra khỏi 2 trường phái: không thuộc x2 hay x8 mà thuộc "không có baseline để so". Tâm lý user không so sánh được → không complain về giá. Vũ accept: *"Anh sẽ dừng câu hỏi ở đây bởi vì anh chưa có trải nghiệm làm cái kiểu như thế."*

## Vị Trí Gói First-Time

Pattern Vũ recommend: gói first-time để **trên màn hình home**, không trong shop.

> *"Tâm lý user vào shop nó không cao — vào đấy là chỉ mất tiền chứ không được mẹ gì. Khi user nó vào, mình nói là ít 8, nó có tâm lý nó muốn mua. Còn không có ai tự dưng đi vào shop để làm cái gì cả."*

Phải có gói tham chiếu chứ — mới biết user hiểu "x2" là gì.

## Server-Side Detect — Biến First-Time Thành "Độ Hiếm"

Pattern Vũ đang dùng: server detect user nào sắp đến điểm phù hợp → push gói đầu trong 1-2 ngày → user thấy gói có "thời gian giới hạn" thay vì gói default.

Hậu quả: user không so sánh gói này với gói shop sau đó, mà coi như gói event riêng. Đây là instance của [[dark-ux-techniques]] — biến gói default thành "rare opportunity".

## Kết Luận

First-IAP strategy quyết định toàn bộ pricing ladder. Chọn x2 = giữ tier balance, ARPU thấp ban đầu; chọn x8 = spike convert, ARPU concentrate ở gói đầu. Pha trộn = mất ưu thế cả 2 trường phái.

Designer phải lock chọn lựa ngay khi design pricing — không sửa được dễ vì user đã mua sẽ phản ứng nếu giá tier thay đổi sau khi họ đã pay.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Monetize — 2 Tư Duy First-Time Purchase", "Bí Quyết: Bán Cái Không So Sánh Được"
