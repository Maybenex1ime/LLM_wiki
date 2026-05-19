---
title: "UI vs UX"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [comparison, ui, ux, design]
aliases: [UI vs UX, phân biệt UI và UX]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[thumb-zone-design]]"
  - "[[notification-management]]"
summary: "UI = cấu trúc nút/màn hình (làm được/không làm được). UX = trải nghiệm tiện hay không tiện, quen hay không quen. UI cho code/deck dùng, UX cho user feel"
---

## Bối Cảnh

Doc 3 và Doc 7 đều mở đầu bằng việc Vũ chỉnh lại định nghĩa UI/UX của học viên. Học viên định nghĩa UX là *"một người chơi với các cái button — như mình hiện cái nút đấy lên thôi."* Vũ chỉnh:

> *"Vấn đề là kiểu cái nút đấy người dùng có cảm thấy tiện không? Người ta thấy kiểu quen thuộc không? Thì cái đấy gọi là user experience."*

UI và UX trùng nhau ở một số khía cạnh (đều liên quan đến màn hình + tương tác) nhưng có target và output khác hẳn.

## Bảng So Sánh

| Tiêu Chí | UI | UX |
|----------|-----|----|
| Định nghĩa | Cấu trúc nút/màn hình | Trải nghiệm khi user tương tác |
| Câu hỏi cốt lõi | "Làm được hay không làm được?" | "Có tiện không? Có quen không?" |
| Output | Flow, pace, các state, button locations | Cảm xúc user, số bước, friction |
| Liên quan đến cảm xúc | Không | Có — sướng / khó chịu / paralysis |
| Ai dùng | Code (build) + Deck (presentation) | User |
| Khi nào hoàn thiện | Sau nhiều vòng iteration: layout, state | Sau khi UI ổn → tối ưu trải nghiệm |
| Đo lường | Có thể test functionality | Test với 10 người ra 10 reaction khác nhau |

## Phân Tích

### UI — Layout và Function

UI là layer thiết kế **trước**:
- Sau khi làm nhiều vòng, mới đưa ra UI — các phần bên trong, các trạng thái, các trường hợp có thể xảy ra.
- UI này code và deck đều dùng.
- UI không có cảm xúc — chỉ có "làm được" hay "không làm được".

Ví dụ UI cho màn chọn nhân vật: 3 nhân vật trên, 3 nút hệ dưới, switch character theo hệ. UI define rõ vị trí, kích thước, state (selected/unselected).

### UX — Trải Nghiệm

UX là layer thiết kế **sau** UI:
- UX là cái trải nghiệm để tối giảm hóa công sức bỏ ra, tối giảm hóa phần nhận về, tối giảm hóa phần xuất.
- Hành trình trải nghiệm có rất nhiều yếu tố.

Ví dụ UX cho màn chọn nhân vật (cùng UI):
- **Bạn 1**: bấm vào hệ ở thanh dưới → nhân vật switch theo.
- **Bạn 2**: bấm trực tiếp vào nhân vật trên màn hình.

Cả hai đều "đúng" về function nhưng phản ánh UX khác nhau. Vũ nhấn:

> *"Không phải user nào họ cũng tag vào đây, không phải user nào họ cũng thích tag vào đây. UX là làm sao để 10 thằng user nó đều trải nghiệm tốt nhất — mà 10 thằng user 10 tính cách hoàn toàn khác nhau."*

UI handle 1 cách interact; UX cần handle nhiều cách interact đồng thời.

### Edge Case Vật Lý

Vũ kể case con survival có nút multimedia thiết kế ban đầu cho user tay phải. Feedback từ user tay trái: *"tao phải đánh nhầm."*

Bài học: UX phải tính cả thằng tay trái, thằng tay phải, thằng ngón dài, thằng ngón ngắn — không thể design 1 layout phục vụ mọi cách cầm. UI có thể chỉ define 1 layout, UX phải nghĩ qua nhiều scenario.

## Kết Luận

UI và UX không thay thế nhau — chúng là 2 layer của cùng 1 thiết kế:

1. **UI trước** — define functional structure: nút ở đâu, state thế nào, flow ra sao.
2. **UX sau** — đánh giá: với UI đã có, user thấy thế nào? Có tiện không? Có nhiều cách dùng không?

Designer thường skip UX vì *"UI đã chạy được rồi"*. Vũ chốt: UI đúng nhưng UX tệ vẫn fail. Phải tách 2 phase rõ ràng — và dùng [[ux-3-criteria]] để evaluate UX option có hơn nhau không.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Tiếp Nối Doc 6 — Phân Biệt UI vs UX"
- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Phân Biệt UI vs UX"
