---
title: "Inherited Habit Conventions — Đừng Reinvent Icon Phổ Thông"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, ux, ui, habit, convention]
aliases: [inherited habit, kế thừa thói quen, icon convention, đừng reinvent, home icon hotel icon]
status: draft
related:
  - "[[ux-yeu-ich-definition]]"
  - "[[ui-button-3-levels]]"
  - "[[ux-3-criteria]]"
summary: "User đã có habit từ game khác. Icon home/hotel/settings/play đã universal — designer reinvent = phá habit, force user re-learn = friction. Habit có 2 nguồn: tạo mới (đắt) và kế thừa (free). Default: dùng convention sẵn."
---

## Định Nghĩa

Habit (thói quen) là pattern user lặp lại không suy nghĩ. Habit cần repetition để hình thành — đắt với designer (mỗi habit tốn weeks of exposure).

Designer có 2 nguồn habit:

| Nguồn | Cost | Khi Dùng |
|-------|------|----------|
| **Tạo mới** | Cao — cần tutorial + repetition | Mechanic unique của game |
| **Kế thừa** | Free — user đã có | Mọi pattern phổ thông |

> *"Vậy thì làm ơn đừng làm cái gì khác cả. Nó cứ vậy đi."*

## Universal Icons (Đã Kế Thừa)

| Icon | Ý Nghĩa | Reference |
|------|---------|-----------|
| **Nhà 🏠** | Home / Main menu | Mọi mobile game + mobile OS |
| **Nhà nghỉ (hotel)** | Inn / Rest spot | Game RPG/strategy (Clash of Clans cũng để pattern này) |
| **Bánh răng ⚙** | Settings | Mọi app |
| **Tam giác ▶** | Play / Start | Media player, mọi game |
| **X ❌** | Close / Cancel | Mọi UI |
| **Mũi tên ←** | Back | Android/iOS standard |
| **Túi 🎒** | Inventory | RPG genre |
| **Thanh kiếm ⚔** | Attack / Battle | RPG/Strategy |

Vũ test lớp về icon hotel:

> *"Bố nào nhìn cái này thì các bố nghĩ ra là cái gì? Là cái hotel. Là cái nhà nghỉ. Đúng không ạ? Vậy thì cái này chúng ta đã được kế thừa rồi — làm ơn đừng thay đổi nó."*

## Anti-Pattern: Reinvent Để "Style"

Designer hay reinvent vì:
- Muốn "khác biệt visual."
- Muốn match aesthetic của game (sci-fi → icon home thiết kế lại theo phong cách sci-fi).
- Không trust convention.

Hậu quả:
- User scan UI không tìm thấy nút quen → ngừng tap → drop session.
- Force tutorial để explain → tăng cost onboarding.
- Re-learn time → friction trước value moment.

> *"Bây giờ không phải vẽ cái nút home là cái nút này tổ chức với bố thật."*

Ngay cả game thờ chung cổ (Clash of Clans) vẫn để nút Home theo convention bình thường — không thử "đổi mới" icon. Lý do: convention rẻ hơn creativity.

## Khi Nào Tạo Habit Mới (Đáng Cost)

Habit mới đáng làm khi:
- Mechanic là **core differentiation** của game (Match-3 swap, Pull-the-Pin pull).
- Không có pattern phổ thông tương đương.
- Game có budget tutorial + repetition để teach.

Designer phải explicit chấp nhận cost: tutorial level, hint arrows, animated demo. Xem [[pattern-habit-break]] cho cách quản lý habit-formation-then-break trong level design.

## Inherited vs Customize

Nhầm lẫn phổ biến: customize (cá nhân hoá) ≠ reinvent.

- ✅ **Customize**: thay icon home thành emoji theo theme (mặt cười cho casual, kiếm cho RPG) — visual khác nhưng vẫn rõ ý nghĩa.
- ❌ **Reinvent**: thay icon home bằng hình kim tự tháp Maya vì game có theme Aztec — user không hiểu là Home.

Test fast: cho 3 user mới scan UI 3 giây, hỏi "đâu là nút Home?" — nếu < 2/3 trả lời đúng → đã reinvent quá mức.

## Inheritable Per Genre

Một số habit chỉ universal trong genre:

| Genre | Habit Riêng |
|-------|-------------|
| **Match-3** | Swipe để swap, tap để select combo |
| **Idle/Tycoon** | Tap-and-hold để accelerate, swipe down để collect |
| **RPG turn-based** | Tap skill → tap target |
| **Strategy** | Long-press để info, drag to deploy |
| **Endless runner** | Swipe up/down/left/right (vuốt 4 hướng) |

Designer trong genre đã có 90% pattern set. Chỉ design new khi genre cần innovation thật sự.

## Liên Hệ Wiki

[[ux-yeu-ich-definition]] cho khung UX. [[ux-3-criteria]] tiêu chí 3 (giảm lượng quyết định) chính là tận dụng inherited habit. [[pattern-habit-break]] cho cách phá habit chủ ý để monetize. [[user-test-no-explanation]] để test convention work — nếu user hỏi "đây là gì," tức là đã reinvent quá mức.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Building Block của UX" — Inherited Habit
