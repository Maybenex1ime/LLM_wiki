---
title: "Asset Hardware Tradeoff — Giới Hạn Phần Cứng Cho Asset"
source: "[[raw/videos/negaxy-iec-gd-doc-02-level-design]]"
date_added: 2026-05-15
tags: [concept, art, performance, asset, mobile-games]
aliases: [giới hạn phần cứng asset, chiều sâu vs chiều rộng, cắt khớp asset]
status: draft
related:
  - "[[gd-role-as-machine-link]]"
  - "[[feeling-of-assets]]"
summary: "Game designer phải set giới hạn phần cứng cho art ngay từ đầu — 10 vs 10 quân thì design chiều sâu, 30 vs 30 thì chiều rộng. Bài học game chiến thuật 3D ngày xưa: 100 con × 15k tris = vỡ trận"
---

## Định Nghĩa

Vũ kể bài học từ game chiến thuật 3D ngày xưa làm ví dụ điển hình cho việc GD phải set giới hạn phần cứng trước khi art thiết kế chi tiết.

Setup vấn đề:
- Thiết bị tham chiếu: ~200k triangles giới hạn (iPhone đời cũ).
- Yêu cầu level design: 100 vs 100 quân.
- Art làm chi tiết: mỗi con ~15k triangles.
- Math: 200 con × 15k = 3M triangles → vượt giới hạn 15 lần → game crash.

Bài học giảng viên rút ra:

> *"Các bạn đã đè một cái nhà 10 tầng lên trên một cái móng chỉ có 3 tầng thôi. Bây giờ ông code làm thế nào?"*

Đây là instance cụ thể của [[gd-role-as-machine-link]] — GD phải define giới hạn trước khi art vẽ, không phải để art tự định.

## Pattern Fix

Vũ liệt kê các cách giảm chip:

1. **Cắt khớp ít hơn** — zombie 20 đốt giảm xuống 6 đốt. Animation rig đơn giản hơn, ít triangle hơn.
2. **Thay đổi logic ăn point** — trước 5 điểm = 1 đốt mới. Sau: 5 điểm → 10 → 50 (ăn theo lộ trình tăng dần) → tổng số đốt giảm theo thời gian.
3. **Giữ first impression** — lúc onboard hiển thị "fill 20 con" nhưng late-game cắt khớp dần để giữ performance.

Quote về bộ giáp Wukong:

> *"Ảnh tản nó cũng sướng, mẩn cho đôi tuần một cái. Xong lên nó mặc, mặc được cái áo để game còn chạy được. Mặc thêm cái quần là game đứt — crack luôn."*

Art muốn cho hero mặc full bộ giáp (áo + quần + giày + mũ). Nhưng mặc 1 món thì performance OK, mặc 2 món thì crash. GD phải quyết định show món nào, không thể chiều art mọi mặt.

## 2D Cũng Dính

Vũ note 2D cũng không thoát: quá nhiều khớp trong một màn hình → lag không optimize được. Phụ thuộc engine (Unity vs Cocos vs custom), nhưng nguyên tắc *"có ngân sách chip thì design trong ngân sách"* vẫn áp.

## Chiều Sâu vs Chiều Rộng

Khi quy đổi giới hạn phần cứng sang lựa chọn thiết kế:

- **10 vs 10 quân** (ít số lượng) → level design theo **chiều sâu** (depth). Mỗi quân chỉ số phức tạp, skill set rộng, animation chi tiết. Giống RPG.
- **30 vs 30 quân** (nhiều số lượng) → level design theo **chiều rộng** (breadth). Mỗi quân đơn giản nhưng đa dạng loại. Giống RTS / TD.

Quy tắc Vũ chốt từ Doc 2: *"Định nghĩa MTV thì chỉ thiết kế đến đó thôi. Không thêm gì cả, không nghĩ đến tính năng gì cả. Hãy làm tốt nhất để nó ra cái này."*

Cùng concept này áp dụng cho game dài hạn vs ngắn hạn:
- **Ngắn hạn / hyper**: chiều sâu (Match-3 1000 level cùng mechanic).
- **Dài hạn / hybrid**: chiều rộng (RPG nhiều mode — PvP, Arena, bang hội, boss).

## Liên Hệ Wiki

[[gd-role-as-machine-link]] là tiền đề — GD phải define giới hạn cho art. [[feeling-of-assets]] là góc nhìn khác về asset (đánh vào tâm lý user qua khan hiếm, achievement, khoe tài sản). Phần cứng giới hạn số tài sản tối đa có thể có trên màn hình, do đó cũng giới hạn cách show off tài sản.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "Giới Hạn Phần Cứng — Trade-off Cho Asset", "Chiều Sâu vs Chiều Rộng"
