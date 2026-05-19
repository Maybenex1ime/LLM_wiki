---
title: "Notification Management — User vs Designer Priority"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [concept, ux, notification, attention, mobile-games]
aliases: [5 loại noti, quản trị noti, user vs designer priority, noti spam]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[thumb-zone-design]]"
  - "[[dark-ux-techniques]]"
summary: "5 loại noti (Reward/Playable/Mission/IAP/Ads). User và designer priority ngược nhau hoàn toàn. Chiến lược: theo user trước (cho thưởng dụ tâm trạng), sau đó push Mission/Playable/IAP"
---

## Định Nghĩa

Notification (noti) là các signal trên home screen game (chấm đỏ, animation, badge) báo có gì đó user nên click. Khi quá nhiều noti cùng lúc, user bị paralysis — Darwin (case Đồng) có **18 noti**, 3 trong đó là dạng animation.

Vũ phân thành 5 loại để designer prioritize:

## 5 Loại Noti

1. **Loại 1: Nhận thưởng** (reward, gift)
2. **Loại 2: Playable** (có thể chơi — mode, tournament)
3. **Loại 3: Mission** (nhắc việc phải làm)
4. **Loại 4: IAP** (gói nạp)
5. **Loại 5: Ads** (xem 1 quảng cáo)

## Thứ Tự Ưu Tiên — User vs Designer

Hai bên ngược nhau hoàn toàn:

| Thứ tự | User muốn (đọc trước) | Designer muốn (push trước) |
|--------|------------------------|-----------------------------|
| 1 | Nhận thưởng | IAP |
| 2 | Playable | Ads |
| 3 | Mission | Mission |
| 4 | Ads | Playable |
| 5 | IAP | Nhận thưởng |

User muốn nhận trước, làm việc sau. Designer muốn user trả tiền/xem ad trước, nhận thưởng sau cùng. *"Mình không có cách nào để chiều lòng cả đôi, cho nên mình chỉ có cách làm dung hòa thôi."*

## Chiến Lược Thực Tế — Theo Ý User Trước

Vũ chốt: theo ý user trước, sau đó dụ.

> *"Việc đầu tiên, theo ý biết: mày chưa sướng thì không có chi tiêu gì hết. Cứ cho nhận thưởng đây đã, không chết ai cả... Nhận thưởng xong rồi tự dưng nó thấy có nhiều tiền, nó sướng — tâm trạng cảm xúc đang lên. Giống như mấy bà bán hàng áo cấp — vào chưa thấy mua bán gì, cứ cháu tặng các bác này tới mười hoa."*

Pattern:
1. Cho user click Reward trước → tâm trạng lên.
2. Tâm trạng tốt → user sẵn sàng click Mission, sau đó Playable.
3. Khi user có nhiều tiền (từ reward) → push IAP để upgrade nhanh hơn.

Quy tắc cho 2 nhóm còn lại (Playable vs Mission):
- Mission **dễ có quà hơn** → user thích hơn → push Mission trước Playable.
- **Nguyên tắc**: bao giờ user cũng thích nhận quà trước, làm việc sau. *"Chả ai lại khổ sở đến mức quà có thể có 1 cái kiếm nhưng vẫn ra trận bằng tay chần, xong một tí về lấy kiếm sau."*

## Khi Nào Show Playable Noti

Không cần noti playable mặc định. *"Chỉ nên noti playable khi user nó quên mất chức năng này thôi."*

Pattern: vào đầu game, có tournament/dungeon → không noti. Sau 3-5 phút user không chơi → noti. Lý do: lúc đầu có quá nhiều việc (campaign, mission, lucky screen, ID reward...). Tránh user học pattern *"bấm nút T lần 1 có thưởng, lần 2 có thưởng, lần 3 có thưởng, nút 4 chắc có thưởng"*.

Tournament đặc biệt quan trọng với user dài ngày → hiển thị **số lượt còn lại (2/2, 1/2)** hoặc **level tournament** bên ngoài button → user biết có gì mới mà không cần bấm vào.

## Xử Lý Spam Noti

5 quy tắc Vũ đưa ra cho case Darwin:

1. **3 cái dạng dương → chọn phát sáng** thay vì dung (chuyển động). User vào game không hiểu phải làm gì khi *"tất cả mọi thứ đều chuyển động"*.
2. **Daily reward**: phọc user xem luôn — *"vào liền phát phọc nó bắt nó nhận luôn"*, không để noti lừng lững.
3. **Battle pass/Season**: chuyển noti thành "hơi sáng lên một tí", không dạng chấm đỏ.
4. **Gói nạp đã hiện**: không cần noti — *"nạp xong là mất gói nạp rồi thì mình không tin"*.
5. **Tournament**: hiển thị `3/3` lượt chơi trực tiếp, không dùng noti chung chung.

## Liên Hệ Wiki

[[ux-3-criteria]] là khung 3 tiêu chí UX, notification management là deep-dive tiêu chí 3. [[thumb-zone-design]] cho bố cục — noti quan trọng phải nằm trong vùng ngón cái. [[dark-ux-techniques]] dùng noti theo cách "lừa" user — đảo nút X3, animation cốc cà phê (arm break).

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Tiêu Chí UX 3 — Quản Trị Sự Chú Ý"
