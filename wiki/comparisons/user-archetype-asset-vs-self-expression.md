---
title: "Nhóm Tài Sản vs Nhóm Thể Hiện Bản Thân"
source: "[[raw/videos/negaxy-iec-gd-doc-08-phan-tap-user]]"
date_added: 2026-05-15
tags: [comparison, user-segmentation, archetype, player-type]
aliases: [tài sản vs thể hiện bản thân, archetype user 2 nhóm sở thích]
status: draft
related:
  - "[[user-segmentation-3-axes]]"
  - "[[s-t-genre-grid]]"
  - "[[feeling-of-assets]]"
summary: "2 nhóm sở thích chính trên trục S: Nhóm Tài Sản (RoK, Lost Mobile — build lòng vòng, đợi đủ lớn rồi đánh) vs Nhóm Thể Hiện Bản Thân (Chess, Tower Defense — build thẳng, PvP sớm)"
---

## Bối Cảnh

Vũ phân trục S (sở thích) trong khung [[user-segmentation-3-axes]] thành 2 nhóm chính. Hai nhóm có thể overlap nhưng hành vi user khác hẳn nhau — phân biệt rõ là điều kiện tiên quyết cho IAP strategy và content design.

## Bảng So Sánh

| Tiêu Chí | Nhóm Tài Sản | Nhóm Thể Hiện Bản Thân |
|----------|--------------|--------------------------|
| Game tham chiếu | Rise of Kingdoms, Lost Mobile | Chess, Cờ Tướng, Tower Defense |
| Kỹ năng tay | Không yêu cầu | Vừa phải, không cần nhanh |
| Tính toán | Cực kỳ khủng khiếp, lòng vòng | Cao nhưng đơn giản hơn |
| Build hero/tướng | Đa chiều, lòng vòng, đợi đủ lớn rồi đánh | Build đường thẳng, focus 1 nhánh |
| Thời điểm tham chiến | Im hơi lặng tiếng, đợi đủ lớn | PvP sớm, vào trận ngay |
| Yếu tố PvP | Có nhưng đợi power max | Cộng lớn, vào sớm |
| Khả năng bỏ game | Thấp (gắn với tài sản tích lũy) | Cao hơn (chơi vì challenge) |
| Source IAP | Pack tài sản, profit, gói tích lũy | Power-up, skin, challenge mode |

## Phân Tích

### Nhóm Tài Sản

Đặc trưng:
- Không yêu cầu kỹ năng tay. *"Hoàn toàn không yêu cầu kỹ năng tay một chút nào, nhưng mà khả năng tính toán lại cực kỳ khủng khiếp."*
- Quyết định nâng cấp đắt — sai 1 nhánh phải trả giá vài ngày, có khi phải nạp tiền để fix.
- User không dám tự build → phải dựa vào clan, kênh YouTube guide. *"Thậm chí có những người chơi mà không dám tự build. Buộc phải chơi chung với người khác mà chỉ hướng dẫn."*
- Trận chiến không cần thao tác: *"Bấm chỉ đánh vào nhà xong rồi 15 phút sau mới đánh, cuối cùng vào cũng chỉ xem thôi."*

Bài học thiết kế: cần độ "lòng vòng" của hệ thống chỉ số. *"Một con tướng nhóm LOK nó có rất nhiều dòng. Đầu tiên là vào chọn trục tập thì sẽ có lợi thế gì — 5% tốc độ khai thác hoặc 5% tốc độ hành quân. Xong rồi mỗi một con tướng tăng 30% chỉ số này chỉ số kia. Tức là nó rất là lòng vòng."*

Cái lòng vòng = yếu tố quyết định user mua hay không. Designer chiều dài stat tree để user cảm thấy *"tôi đang tối ưu"* — chính là driver chi tiêu.

### Nhóm Thể Hiện Bản Thân

Đặc trưng:
- *"Cái đội mà thích thể hiện bản thân lên chiến đấu nó thích giải những cái bài toán khó. Những cái bộ môn mà nó có cái tính challenge cao."*
- Kỹ năng tay vừa phải, không cần nhanh — *"Tất cả các dòng game mà chơi chậm chậm chậm là đội này chơi được hết."*
- Khả năng tính toán cân dòng tiền + cảm nhận quân.
- Có yếu tố PvP là cộng lớn — *"Nó có yếu tố PvP sẽ là cái yếu tố mà nó rất thích."*

Build pattern:
> *"Bọn nào đã build một con tướng nào đấy theo đường quân này thì thậm chí là nó chỉ tập trung focus vào mỗi một cái đường ấy thôi. Kể cả từ tech này cho tới tướng này, bọn nó sẽ build thẳng."*

Build thẳng = chọn 1 strategy và follow đến cùng. Game không cần lòng vòng — user muốn thấy progress rõ ràng.

## Sự Khác Biệt Trong Thiết Kế Game

| Element | Nhóm Tài Sản | Nhóm Thể Hiện Bản Thân |
|---------|--------------|--------------------------|
| Hero/Unit stat tree | Đa chiều, nhiều layer (5% A, 30% B, level upgrade tăng C) | Đơn giản, clear: skill 1/2/3, level cap |
| PvP | Có nhưng chỉ ở endgame (đợi max power) | Có ngay từ early game |
| Clan / Guild | Quan trọng — bang chủ T3 là target tier | Optional — user vẫn play solo |
| Content gating | Time-based (đợi 15 phút build) | Skill-based (qua được màn này thì mở) |
| IAP | Pack đa dạng theo tier (T2/T3/T4) | Power-up, skin, challenge mode unlock |
| Time investment | High commitment, daily ritual | Episodic, dài-ngắn không cố định |

## Overlap

Hai nhóm overlap khi game có cả 2 element. Ví dụ: Clash of Clans có element tài sản (xây base, đợi build) + element thể hiện (PvP attack). Designer phải prioritize main archetype — Clash of Clans primarily là "tài sản với PvP element" chứ không phải "thể hiện với base element".

Designer pha trộn không có chủ ý → game không serve được nhóm nào tốt. Xem [[replay-rate-distribution]] — nếu metric phân cực, có thể game đang cố serve 2 nhóm trong 1 sản phẩm → tách thành 2.

## Kết Luận

Trước khi build, designer phải pick **một archetype primary**:
- Nhóm Tài Sản → build hệ thống stat tree lòng vòng + clan + time-gated content.
- Nhóm Thể Hiện → build skill-based progression + PvP sớm + challenge curve clear.

Pick sai = wasted development. Nhóm Tài Sản không quan tâm skill challenge; Nhóm Thể Hiện không quan tâm "lòng vòng" stat.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-08-phan-tap-user.md` § "Trục Sở Thích — Đánh Vào Tài Sản", "Trục Sở Thích — Thể Hiện Bản Thân", "Khác Biệt Với Nhóm Tài Sản"
