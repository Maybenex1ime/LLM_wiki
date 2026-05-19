---
title: "Organic Rate — Diễn Giải Đúng"
source: "[[raw/videos/negaxy-iec-gd-doc-08-phan-tap-user]]"
date_added: 2026-05-15
tags: [concept, ua, organic, analytics]
aliases: [organic rate, tỷ lệ organic, organic không phải designer chủ động]
status: draft
related:
  - "[[ltv-cpi-formula]]"
  - "[[user-segmentation-3-axes]]"
  - "[[metric-diagnosis-4-methods]]"
summary: "Organic rate cao không suy ra tập user thuần và trẻ hoá thị trường. Phải tách: tỷ lệ vs số tuyệt đối, trend tạm thời vs ổn định. Vũ note organic là thuật toán Google, không phải designer chủ động được"
---

## Định Nghĩa

Organic rate = % user tải về tự nhiên (không qua marketing campaign). Học viên Doc 8 hỏi: *"Một con game mà có tỉ lệ organic cao ấy thì có phải là tập user đấy là tập user mà chơi các cái game cùng thể loại đấy nhiều không?"*

Vũ phản biện: **không hoàn toàn đúng**. Phải tách 3 yếu tố trước khi kết luận.

## 1. Tỷ Lệ vs Số Tuyệt Đối

Organic rate cao không nói lên gì nếu **số tuyệt đối nhỏ**:

> *"Cái tỷ lệ organic của em nó còn do liên quan đến cả số nữa. Nhưng mà cái đấy nó khó giá lắm. Em chạy có nhiều đâu... Tỷ lệ nó cao nhưng mà cái số lại nhỏ thì nó cũng không chuẩn lắm. Nên là nó cũng khó đánh giá."*

Ví dụ: 80% organic trong 100 install = 80 user. 30% organic trong 10.000 install = 3.000 user. Số tuyệt đối quan trọng hơn tỷ lệ. Đây là application của [[metric-diagnosis-4-methods]] method 1 (timing/volume) — không tin metric đơn lẻ.

## 2. User Vô Chi Dropoff Sớm — Case Survival IO

Survival IO map vào T2S1 — user vô chi + thích tài sản. Trải nghiệm Vũ:
- Chơi Archero (gốc) → tắc map 2, không nạp được, drop.
- Chuyển sang Survivor IO (kiểu Slime) → chơi vì giống tên Tổ, drop sau vì *"không có thêm những cái thứ mà anh cần."*
- Archero của Api làm tốt hơn về phần tài sản (skin, quần áo).

Vũ kết luận: dropoff giữa các con cùng dòng → tỷ lệ organic cao có thể chỉ là user **nhảy cóc giữa các game cùng dòng**, không phải dòng game đang trẻ hoá thị trường.

User pattern này nguy hiểm cho designer mới — dễ tưởng organic cao = thị trường rộng, nhưng thực ra là user lifetime ngắn trong từng game.

## 3. Trend Tạm Thời — Hyper Sụp → Puzzle Nổi

Trải nghiệm năm trước:

- Hyper casual sụp đổ → để khoảng trống thị trường.
- Puzzle có *"mức độ phù hợp với đông người"* + tốc độ sản xuất chậm → tỷ lệ tìm kiếm tăng → organic puzzle tăng.
- Bây giờ tất cả studio nhảy vào → bão hòa → organic trở lại mặt bằng.

Quote:

> *"Sau khi mà... biết... có con đường đẹp rộng thênh thang... thì tất cả các xe cứ lại đâm vào đấy, lại húp vào đấy... thì bây giờ ở đây nó lại thất. Nó lại trở về mặt bằng thị trường."*

Hệ quả: tăng organic ngắn hạn (1-3 tháng) thường do trend, không phải do game thiết kế tốt. Kết luận quá sớm dẫn đến chiến lược sai.

## 4. Organic Là Thuật Toán Google

Vũ note rõ:

> *"Cái đội đấy đâu phải là nắm đội thuật toán. Chứ còn mình chỉ là người đi follow theo nó thôi."*

Organic phụ thuộc Google Play / App Store algorithm (search rank, category ranking, feature). Designer không trực tiếp control. Đây là tương tự với [[ecpm-blackbox]] — biến hộp đen.

## Case Boost Organic Sai

Trải nghiệm cũ Vũ kể:

- 1 con game có organic cao chỉ ở **1 thị trường**, các thị trường khác không có.
- Team đoán *"phù hợp văn hóa"*.
- Khi tăng marketing budget → organic theo lên → tưởng đã hiểu.
- Tuần sau lại sụp → boost tiếp → vẫn sụp.

Kết luận: organic không phải là cái team có thể chủ động. *"Nếu mà các sếp mà biết làm organic như thế nào tốt ấy thì làm hết organic của chạy cam, thì nó khổ thường đấy."*

Pattern này tương tự với [[ecpm-blackbox]] — designer không kiểm soát biến cuối cùng, chỉ kiểm soát các đầu vào (game quality, retention, store optimization).

## Bài Học Cho Designer

1. **Không infer tập user từ organic rate.** Phải có data trực tiếp (demographics, behavior).
2. **Trend organic ngắn hạn không = product fit.** Kiểm tra organic stable qua 3-6 tháng.
3. **Không phụ thuộc organic** để scale. UA paid mới là biến control được.

## Liên Hệ Wiki

[[ltv-cpi-formula]] không tính organic trong CPI — organic là "bonus" không reliable. [[user-segmentation-3-axes]] cho khung tách tập user — phải xác định tập user qua engagement metric chứ không qua organic rate. [[metric-diagnosis-4-methods]] method "dimension" và "reference" áp dụng để diagnose organic spike.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-08-phan-tap-user.md` § "Organic Rate — Không Phải Cứ Cao Là Tập Trùng"
