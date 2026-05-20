---
title: "3 Tiêu Chí UX — Bước, Thông Tin, Sự Chú Ý"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]], [[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
date_updated: 2026-05-20
tags: [concept, ux, ui, mobile-games]
aliases: [3 tiêu chí UX, 3 giảm thiểu, số bước thao tác, quản trị sự chú ý, dung dạng thông tin]
status: draft
related:
  - "[[ui-vs-ux]]"
  - "[[notification-management]]"
  - "[[thumb-zone-design]]"
  - "[[auto-equip-design]]"
  - "[[hearthstone-vs-uvo-card-text]]"
  - "[[material-count-decision-paralysis]]"
  - "[[ui-rule-max-2-levels]]"
summary: "3 tiêu chí đánh giá UX của Vũ (3 Giảm Thiểu): (1) số bước thao tác (càng ít càng tốt), (2) thông tin (số lượng + cách hiển thị + dung dạng), (3) quản trị sự chú ý / giảm thiểu quyết định. Doc 6 P2 introduce, Doc 7 expand với case study."
---

## Định Nghĩa

Vũ chốt 3 tiêu chí khung để evaluate UX option, sau khi đã tách [[ui-vs-ux]]. Còn gọi là **3 Giảm Thiểu**:

1. **Số bước thao tác** — đếm số lần user phải bấm/swipe để hoàn thành 1 task.
2. **Thông tin** — số lượng đầu thông tin + cách hiển thị + dung dạng.
3. **Quản trị sự chú ý / Giảm thiểu quyết định** — quản trị notification, đưa ra ít quyết định.

3 tiêu chí này không thay thế cho [[lion-studios]] design patterns mà là khung **so sánh option** — khi designer có nhiều cách thiết kế cùng 1 flow, dùng 3 tiêu chí để chọn ra cái tốt nhất.

> *"3 cái này nó hiển thị theo 3 bước, theo 3 cái tư duy này. Làm theo số bước là gì? Nhanh hơn. Theo số lượng thông tin gọn hơn. Và số lượng thứ 3 là biến user trở thành những người hành động theo thói quen, không cần phải suy nghĩ quá nhiều."*

Doc 6 Part 2 introduce framework. Doc 7 expand với case study chi tiết (skill description ≤ 8-10 chữ, dung dạng thông tin, equipment flow).

## Tiêu Chí 1 — Số Bước Thao Tác

Case study Equipment Hiệp (đếm bước thay 1 vũ khí):

| Option | Bước | Note |
|--------|------|------|
| Option 1 — Đi từ Hero | 6 | Mặc định, Hiệp đã quên nút Swap |
| Option 2 — Đi từ Weapon | 3 | Tối ưu hơn |
| Option 3 — Auto-Equip | 2 | Tùy loại game (xem [[auto-equip-design]]) |

Quy tắc Vũ chốt:

> *"Anh muốn từ nay không phải chỉ vụ này, mà tất cả những kinh doanh khác, em sẽ làm cái việc là em tách mình ra 2-3 option, sau đó các option đi bắt lẫn nhau và chọn ra một cái tốt nhất. Em không có vấn đề đúng hay sai."*

Số bước ít hơn ≠ luôn tốt hơn (auto-equip 2 bước có thể fail ở game 1-5 hero không có fun role). Phải đối chiếu với 2 tiêu chí còn lại.

### Tối Ưu Bước

3 đề xuất tối ưu Option 1 trong Doc 7:
1. **Bỏ nút Swap** — hiện luôn weapon hiện tại, tap đổi chỗ. Còn 5 bước.
2. **Drag-and-drop** — kéo weapon từ list lên slot.
3. **Chia 2 filter** (tab weapon + tab hero) — bấm vào kiếm là kiếm, bấm vào khiên là khiên. Còn 3 bước.

Vũ chốt nguyên lý sáng tạo trong UI:

> *"Mọi người hãy hỏi tôi sáng tạo đâu — sáng tạo nằm đây này. Nó là những việc nhỏ, để cho user cảm thấy tiện hơn."*

Sáng tạo UI = giảm bước, không phải vẽ animation đẹp.

## Tiêu Chí 2 — Thông Tin

Case study Hero Info Đồng (game Darwin): 20 field total, show 10-12. Vũ chốt 3 loại tối ưu thông tin:

1. **Số lượng đầu thông tin** — có cắt bớt được trường nào không? (vd. có nhất thiết phải tách HP và DEF không, hay merge thành "effective HP"?)
2. **Cách thức hiển thị** — icon vs text vs số. Trường nào dùng icon thay text được?
3. **Dung dạng thông tin** — cùng 1 trường, hiển thị bao nhiêu chữ?

### Skill Description ≤ 8-10 Chữ

Quote Vũ về tối ưu dung dạng:

> *"Em cố gắng tối đa từ 8 đến 10 chữ một lúc. Cái gì đấy em cố gắng tránh tình trạng là nó nhiều thứ quá khiến user bớt đảo, không muốn đảo."*

3 giá trị của việc bớt chữ:
1. User nhìn lướt → đọc → hiểu → so sánh được giữa các skill/skin.
2. Giải quyết lỗi ngắt câu/ngắt chữ khi xuống dòng nhiều.
3. User nước ngoài đọc cũng hiểu — không bị tràn câu.

**Tip phụ**: số phải dùng màu khác (xanh hoặc nổi bật) để hút mắt user vào số trước.

### Thống Nhất Vị Trí

Quy tắc đặt tên và vị trí:
- Thống nhất trái-phải/trên-dưới cho cùng 1 loại thông tin.
- Vị trí nút theo logic thông thường — tên hero trên, level dưới.
- Info để góc trái trên (convention chung).
- Phá đồng bộ khi cần hướng sự chú ý — nếu 2 phần khác nhau thì nên có khung màu khác nhau.

## Tiêu Chí 3 — Quản Trị Sự Chú Ý

Nguyên lý:

> *"Vì sao phải giảm thiểu đưa quyết định? Đưa cho nó ít quyết định thôi, đừng có đưa ra nhiều quá. Hỏi hôm nay ăn gì — nó kể cho bức tranh, đưa 2 ốc sần. Hỏi 1 câu chuyện nhất thôi: 'đố em hôm nay ăn gì', nói trả lời đưa 1 món, đi ăn món đấy."*

Case study home screen Darwin: **18 noti** trong đó có 3 dạng dương (animation). VIP, daily reward, season/battle pass, tournament, gói nạp, mission, mail, hero info, chapter rewards… tất cả cùng lúc → user paralysis.

Designer phải prioritize. Xem [[notification-management]] cho 5 loại noti và thứ tự user vs designer mong muốn.

## Liên Hệ Wiki

[[ui-vs-ux]] (comparison) là tiền đề phân biệt UI và UX. [[notification-management]] cho deep-dive tiêu chí 3. [[thumb-zone-design]] cho phần liên quan đến tiêu chí 1 (bố cục nút trong vùng ngón cái). [[auto-equip-design]] là case study cụ thể của tiêu chí 1 — option 3 (auto-equip) giảm bước nhưng fail ở loại game không hợp. [[hearthstone-vs-uvo-card-text]] cho deep-dive tiêu chí 2 (keyword compression vs dense description). [[material-count-decision-paralysis]] cho tiêu chí 3 ở mảng economy. [[ui-rule-max-2-levels]] cho tiêu chí 1 ở mảng navigation.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "UI Triết Lý — 3 Giảm Thiểu" (introduce framework)
- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Tiêu Chí UX 1 — Số Bước Thao Tác", "Tiêu Chí UX 2 — Thông Tin", "Tiêu Chí UX 3 — Quản Trị Sự Chú Ý" (expand)
