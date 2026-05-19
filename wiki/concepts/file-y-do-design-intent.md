---
title: "File Ý Đồ — Design Intent Document"
source: "[[raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap]]"
date_added: 2026-05-15
tags: [concept, level-design, design-intent, documentation]
aliases: [file ý đồ, file tiêu chí, design intent doc, lộ trình content]
status: draft
related:
  - "[[level-content-vs-level-data]]"
  - "[[level-data-vs-handcrafted]]"
  - "[[match3-difficulty-levers]]"
  - "[[pattern-habit-break]]"
summary: "2 file đầu vào (file tiêu chí + file ý đồ) + 1 file output (level design). Vũ chỉ ra anti-pattern phổ biến: designer skip 2 file đầu, làm thẳng output, đến level 3-4 quên ý định ban đầu"
---

## Định Nghĩa

Vũ chỉ ra anti-pattern phổ biến: *"Các bạn sẽ làm một file output luôn — level design xuất đầu ra luôn."* Designer bỏ qua 2 file đầu vào quan trọng — và đến level thứ 3-4 thì *"bắt đầu quên — và bạn trình bày khác đi so với những gì bạn ấy đang thực làm."*

3 file của 1 level design flow:

```
File 1: File Tiêu Chí (validation criteria)
   ↓
File 2: File Ý Đồ (design intent + roadmap)
   ↓
File Output: Level Design (số mu, vị trí object, config thật)
```

## File 1 — File Tiêu Chí

Định nghĩa level cần đạt được cái gì TRƯỚC KHI thiết kế:

- **Content**: có bẫy số 1, bẫy số 2, đến cái thứ mấy.
- **Mức độ**: easy / hard / tutorial / nightmare.
- **Chỉ tiêu validation**: same-art, tỷ lệ replay target, các metric mong muốn.

Ví dụ tiêu chí cho 6 level đầu:

```
Lvl 1: Tutorial → 100% win
Lvl 2-3: Easy → 0% thua (build trust)
Lvl 4: Medium → 5% replay
Lvl 5: Hard → 8% replay
Lvl 6: Nightmare → 15% replay
```

## File 2 — File Ý Đồ

Bao gồm cách triển khai từ tiêu chí → level cụ thể. Cấu trúc 1 ý đồ chuẩn:

```
Tutorial → Easy → Easy → Medium → Hard → Nightmare
100%      0%      0%      5%       8%      15%
win       thua    thua    replay   replay  replay
```

Sau khi pick ý đồ, dự án soát chéo: *"Eo, sao mày ác kê, mới vừa 16 mà mày cho người ta 15% chơi lại rồi — anh nghĩ là ít thôi, khoảng tầm 10% là vừa."* Có cuộc trao đổi cụ thể giữa người trong dự án để chốt con số.

File ý đồ tồn tại để designer **không quên** ý định của chính mình giữa chừng. Đây là điểm khác biệt cốt lõi giữa designer chuyên nghiệp và amateur.

## File Output — Level Design

Đến đoạn convert tiêu chí thành số mu (moves) cụ thể:
- Tutorial: 1-2 mu.
- Easy: tăng dần theo dòng game.
- Hard: hardcore = 20 mu thì thực để 23-25 mu cho user → ép tỷ lệ replay vào ~15%.
- Lý do gap (hardcore vs hiển thị): *"Kỹ năng của mình sẽ tốt hơn của user — tính cho user thoải mái hơn tí."*

## Quote Chốt — Designer Hay Quên

> *"Anh gặp rất nhiều các bạn — khi mình chơi thử level design của bạn ấy và khi bạn ấy trình bày thì lúc đầu mình hiểu hiểu một tí, nhưng sau mình mới đổ không hiểu. Bởi vì là qua một level, hai level thì bạn ấy còn nhớ, đến level thứ ba bắt đầu quên — và bạn trình bày khác đi so với những gì bạn ấy đang thực làm."*

File ý đồ giải quyết bằng cách viết ra. Designer không phải nhớ — đọc lại file là đủ.

## Lý Do Pick Level Cho Event

Khi học viên Quân nói *"đặt yes ở level 8, 18, 28..."*, Vũ hỏi *"vì sao"* — đáp án phải đến từ phân bổ ad density / engagement time, không phải đoán:

```
Ad target = 10 ads/day
Time engagement = 20 phút
Level time = 1 phút → ~20 trận/session
Density inter:reward = X:Y
→ Suy ra placement của từng "yes" trên trục level.
```

File ý đồ chính là nơi note ra cái calculation này — không để miệng kể lại lúc review.

## Liên Hệ Wiki

[[level-content-vs-level-data]] cho 2 trục thiết kế — file ý đồ phải tách rõ trục nào đang lock và trục nào đang scale. [[level-data-vs-handcrafted]] cho 2 dạng level design — file ý đồ áp dụng cho cả 2 nhưng output khác (Excel với Level Data; Unity scene với handcrafted). [[match3-difficulty-levers]] cho 5 lever cụ thể để quy ra số. [[pattern-habit-break]] là pattern thiết kế ý đồ — 3 level tạo thói quen + 1 level phá.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` § "Trình Tự Xây Dựng Level Design — 2 File Indo + 1 File Output"
- `raw/videos/negaxy-iec-gd-doc-02-level-design.md` § "File Ý Đồ — Thiếu Sót Phổ Biến Của Designer"
