---
title: "Level Data vs Level Xếp Tay (Handcrafted)"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [comparison, level-design, match-3, puzzle, rpg]
aliases: [level data vs handcrafted, xếp tay vs Excel, 2 dạng level design]
status: draft
related:
  - "[[level-content-vs-level-data]]"
  - "[[file-y-do-design-intent]]"
  - "[[match3-difficulty-levers]]"
summary: "2 dạng level design cơ bản: Level Data (Excel/Grid, scale theo số) cho Match-3/Sort; Level Xếp Tay (Unity, handcrafted) cho Pull-the-Pin/Puzzle vật lý/RPG. Một số game lai cả 2"
---

## Bối Cảnh

Vũ mở đầu Doc 4 bằng việc nhóm tất cả các kiểu level design thành 2 trục, để học viên biết game của mình thuộc nhóm nào trước khi áp công cụ.

Quy tắc cốt lõi: *"Nó thuộc nhóm nào thì mình bổ vào — nó mới dễ."* Trước khi học cách làm, phải biết game thuộc nhóm nào.

## Bảng So Sánh

| Tiêu Chí | Level Data | Level Xếp Tay (Handcrafted) |
|----------|-----------|------------------------------|
| Công cụ | Excel hoặc Grid (ô vuông, lục giác) | Unity editor (kéo thả) |
| Output | Số liệu: number of moves, drop rate, spawn rate | Vị trí object cụ thể trên scene |
| Game phù hợp | Match-3, Sort, các game có ô lưới | Puzzle Pin (pull-the-pin), puzzle vật lý, Action Puzzle, RPG, environment shooter, game chiến thuật |
| Scale level | Tăng số → tăng khó | Sửa từng level riêng biệt |
| Multivariable | Quy về 1 biến cuối (số mu) để control | Khó tính công thức — phải test |
| File output | CSV / JSON config | Unity scene / prefab |
| Difficulty curve | Vẽ được bằng formula | Phải test thực tế từng level |
| Speed | Nhanh — copy paste row Excel | Chậm — mỗi level kéo tay |

## Phân Tích

### Level Data — Excel/Grid

Đặc trưng: game có lưới rõ ràng, level scale qua thay đổi số.

Ví dụ: *"level 1 có con này bao nhiêu, level mấy số bao nhiêu"*. Match-3 standard:
- Số mu (moves).
- Số object goal cần thu.
- Tỷ lệ drop từng màu (xem [[match3-difficulty-levers]]).
- Vị trí blocker trên grid.

Designer có thể có 1000 level chỉ qua thay đổi 1-2 số trong file CSV. Đây là lý do Match-3 commercial scale dễ hơn puzzle vật lý.

### Level Xếp Tay — Unity Editor

Designer kéo thả vị trí object trong Unity. Áp dụng cho:
- **Puzzle Pin** (pull-the-pin) — vị trí pin trên màn quyết định độ khó.
- **Puzzle vật lý** — vị trí block, lực đẩy ban đầu.
- **Action Puzzle** — vị trí trap, kẻ thù.
- **RPG** — map layout, vị trí spawn enemy.
- **Environment shooter** — cover placement, sight lines.
- **Game chiến thuật cần xếp map** — terrain features.

Mỗi level là 1 Unity scene riêng → khó scale. Bù lại, designer kiểm soát chi tiết hơn cho mỗi moment chơi.

## Game Lai — Hybrid

Một số game lai cả 2 dạng:

- **1 map dùng chung cho level 2 và level 7** (map không đổi). Map xếp tay trong Unity → handcrafted layer.
- **Đội quân spawn ở vị trí khác, số lượng khác, timing thả khác nhau** → Data layer.
- *"Bọn này đi thả theo thời gian, cách nhau là không phải — cách nhau 2 giây, con bạn này cách nhau 3 giây."*

Map có boss → file config boss riêng (HP/damage/tốc độ chạy/vị trí spawn trong map). Đây là dạng "data trên map handcrafted" — designer thay đổi data quân mà không phải redesign map.

## Bài Toán Multivariable Của Giang

Giang phản biện: con Pull-the-Pin không tính được difficulty bằng công thức — *"Cứ làm nó ướm ướm thôi. Chạy xong có user thì nhìn cái kết quả rồi mình chỉnh lại."*

Multivariable cụ thể (Pull-the-Pin level 15 vs 16):
- Số lượng pin: bằng nhau.
- Khác biệt: **mật độ đan xen** giữa các pin trong layout — pin block lẫn nhau hay không.

Vũ và Hiệp thừa nhận:
- Một số game (Pull-the-Pin, MoSort/IQ optimization) **biến trong biến**, hàm chồng hàm → công thức không tính ra được.
- Vẫn cần [[file-y-do-design-intent|file tiêu chí]]: target = 85% win-rate cho level 15 → chỉnh số pin / đan xen cho đến khi đạt target qua test.
- *"Đến cuối cùng vẫn là cái pin — cái pin sẽ là cái biến cuối. Các biến số bên trong (đan xen, vị trí) sẽ nằm vào trong đấy."*

Tức là ngay cả Level Xếp Tay vẫn cần đầu ra số (vd. số pin = biến cuối) — chỉ khác là designer không tính trước được, phải test rồi adjust.

## Phối Hợp Với Trục "Content vs Data"

[[level-content-vs-level-data]] là trục độc lập với 2 dạng trên. Cả Level Data lẫn Level Xếp Tay đều có thể mix Content + Data:

- Match-3 (Level Data) thêm blocker mới = Content thay đổi; giảm số mu = Data thay đổi.
- Pull-the-Pin (Xếp Tay) thêm yếu tố mới (mở khóa, đá trở vật) = Content; sắp pin sát nhau hơn = Data.

## Kết Luận

Phân biệt 2 dạng level design là bước đầu tiên. Sau đó designer phải biết:
- Nếu Level Data → setup file ý đồ với formula clear, scale qua số.
- Nếu Level Xếp Tay → setup file tiêu chí với target metric (win-rate), test từng level.
- Nếu hybrid → tách rõ data layer (config files) và handcrafted layer (scene), không trộn.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "2 Dạng Level Design Cơ Bản", "Bài Toán Của Giang — Multivariable Không Tính Được"
