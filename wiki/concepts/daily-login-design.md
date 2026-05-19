---
title: "Daily Login Design"
source: "[[raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset]]"
date_added: 2026-05-15
tags: [concept, retention, daily-login, mobile-games]
aliases: [daily login 3 mô hình, 7-day loop, 28-day no-loop]
status: draft
related:
  - "[[gd-role-as-machine-link]]"
  - "[[retention-curve-design]]"
  - "[[notification-management]]"
summary: "3 mô hình daily login (7-day loop, 28-day no-loop bỏ qua, 28-day no-loop tiếp tục) và anti-pattern phổ biến — không define mục đích từ đầu rồi đến cuối thấy không còn quà để cho"
---

## Định Nghĩa

Daily Login là cơ chế nhỏ nhưng được Vũ dùng làm **case study về define trước**. Lý do: nhiều designer mặc định "đặt một bảng daily login là xong" mà không define rõ mục đích của bảng và cấu trúc reward → đến cuối bị bí, dồn legendary item vào ngày 28 → user cảm thấy *"từng ngày bình thường không có sức nặng, không thấy quý giá"*.

Vũ liệt kê 3 mô hình mà GD phải chọn TRƯỚC KHI thiết kế reward:

## Mô Hình 1 — 7-Day Loop, Lặp Lại

Reward 7 ngày, sau đó loop lại từ đầu. Đặc trưng:
- Reward ô to dễ vẽ art (1 ngày 2-3 quà cũng ok).
- Phù hợp game ít content, không cần "drama" trong daily login.
- Mỗi tuần reset → user không sợ miss một ngày sẽ mất nhiều.

## Mô Hình 2 — 28-30 Day No-Loop, Miss Thì Bỏ Qua

Reward 28-30 ngày, không loop. Nếu user miss ngày 5 thì ngày 5 không còn được. Đặc trưng:
- Phải design state "disabled icon" cho ô đã miss.
- Tạo pressure phải login đều — user lỡ một ngày thì biết là mất reward.
- Risk: user lỡ 1 ngày có thể cảm thấy "lỗi rồi" rồi bỏ luôn.

## Mô Hình 3 — 28-30 Day No-Loop, Miss Thì Tiếp Tục Hôm Sau

Reward 28-30 ngày, không loop, miss ngày 5 thì ngày 5 hôm sau lấy được. Đặc trưng:
- Không ép user vào nhịp khắt khe.
- Nhịp login chậm hơn — user chơi 28 ngày thực tế có thể trải qua 35-40 ngày calendar.
- Phù hợp khi muốn tăng retention rộng (không cần daily hard).

## Anti-Pattern Phổ Biến

Vũ chỉ ra cách làm sai phổ biến: designer thiết kế reward theo cảm tính, đến cuối thấy *"không còn quà gì để cho → ngày 28 phải bỏ legendary item vào → user thấy từng ngày bình thường không có sức nặng"*. Sau đó cãi nhau giữa GD/art/operations để dồn quà ra đầu (tăng giá trị ngày 1-3) hoặc ra cuối (tạo apex ngày 28) → mất nhất quán.

Bài học không phải "loại nào đúng" mà là **GD phải define ngay từ đầu mục đích Daily Login để làm gì**. Sau đó cân bằng reward sao cho UI/UX truyền tải đủ tầm quan trọng → user dù bận thế nào cũng vào 1 phút lấy reward. Đây là instance cụ thể của triết lý [[gd-role-as-machine-link]] — define đủ trước khi build.

## Quote Hiệp Về Tâm Lý User

> *"Em mất đậm trong cái Daily Login — nó không hề quan trọng như việc đấy, thì người ta mới không còn muốn ngày hôm sau. Nhưng nếu ngày D3 đã làm cho người ta hiểu rằng tôi sẽ phải đăng nhập liên tục D4, D5, D6, D7 để nhận cái này, thì hôm sau bỏ ra 1 phút thôi log in, xong rồi đi chơi với bạn gái — chuyện rất bình thường."*

Quy luật: UX phải build expectation từ D1-D3 rằng *"đăng nhập tiếp ngày sau sẽ có giá trị cao hơn"*. Nếu D1-D3 cho reward đều đều, không escalate → user không thấy lý do quay lại D4+.

## Liên Hệ Wiki

Daily login là một thành phần của [[retention-curve-design]] (cross-day retention). Cách hiển thị reward ngày tiếp theo gắn với [[notification-management]] — daily login noti phải để user thấy không bấm cũng biết có quà. Daily login định nghĩa thành công sớm thuộc về tinh thần [[gd-role-as-machine-link]]: GD phải define đủ trước khi push xuống art/UI.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset.md` § "Daily Login — Case Study Define Trước"
