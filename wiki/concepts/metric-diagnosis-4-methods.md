---
title: "Bốn Phương Pháp Chẩn Đoán Biến Động Chỉ Số"
source: "compiled"
date_added: 2026-05-06
tags: [concept, analytics, kpi, diagnosis, methodology]
aliases: [4 method analysis, chẩn đoán KPI, metric diagnosis, root cause analysis game]
status: draft
related:
  - "[[game-analytics-mindset]]"
  - "[[funnel-analysis]]"
  - "[[databuckets]]"
summary: "Bốn phương pháp khoanh vùng nguyên nhân khi KPI biến động bất thường — timing, dimension breakdown, related metrics, reference comparison."
---

## Định Nghĩa

Khi một KPI quan trọng (eCPM, retention, RV impressions, IAP conversion) biến động bất thường, tài liệu Databuckets đề xuất bốn phương pháp bổ trợ áp dụng tuần tự để khoanh vùng nguyên nhân. Mục đích: đi từ "con số" đến "insight cốt lõi" rồi đến "giải pháp tối ưu". Bốn phương pháp này là chương dày nhất của tài liệu và là công cụ cốt lõi cho bước 5 trong [[game-analytics-mindset|quy trình 6 bước]].

Triết lý: "Một con số không phải insight. Insight phải trả lời vì sao và gợi ý làm gì."

## Method 1 — Xác Định Thời Điểm Phát Sinh Vấn Đề

Khi KPI rớt hoặc tăng mạnh, câu hỏi đầu tiên là "từ ngày nào?". Sau đó kiểm tra changelog để biết game/UA/Monet thay đổi gì lúc đó. Cách này khoanh vùng nguyên nhân vào product code, UA traffic, hoặc ad network — ba nguồn biến động phổ biến nhất.

Ví dụ tài liệu: eCPM tụt từ 15/10 → xem changelog ngày 14/10 phát hiện "cập nhật code ads". Retention giảm từ 1/10 → game update hôm đó "thêm ads early".

## Method 2 — Bóc Tách Chỉ Số Theo Dimension

Một chỉ số tổng là trung bình hoặc tổng của nhiều dimension. Phân rã theo country, ad format, level bracket, app version để tìm dimension nào đang gây biến động. Phương pháp này hữu ích khi Method 1 không có changelog rõ ràng hoặc thay đổi không giải thích đủ.

Ví dụ: eCPM chung giảm — tách theo country và ad format thấy eCPM India giảm mạnh trong khi traffic India lại tăng. Hoặc retention chung giảm — tách theo version 1.0 và 2.0, phát hiện chỉ 2.0 bị ảnh hưởng.

## Method 3 — Liên Kết Chỉ Số

Nhiều KPI trong game có quan hệ toán học hoặc nhân quả với nhau. Khi một chỉ số biến động, kiểm tra các chỉ số liên quan để xác định nguyên nhân gốc.

Tài liệu liệt kê các quan hệ phổ biến: `Ad Earnings = eCPM × impressions`, `eCPM ∝ CTR`, retention thường tỷ lệ với session time. Ứng dụng: estimated earnings giảm — câu hỏi tiếp là do eCPM giảm hay impressions giảm. Nếu eCPM giảm thì check CTR; nếu impressions giảm thì check requests và match rate.

## Method 4 — So Sánh Với Tham Chiếu Khác

Để đánh giá một chỉ số là cao hay thấp, cần baseline so sánh. Ba loại baseline thường dùng: thời gian cũ (tháng trước, tuần trước), dimension khác (region, ad source, level bracket), và sản phẩm khác cùng nhóm.

Ví dụ: show rate của vị trí A là 70% và của vị trí B là 78% — vị trí A thấp hơn 8%, gợi ý logic load ads ở A chưa tối ưu. Không có tham chiếu B thì 70% có thể được hiểu nhầm là "ổn".

## Áp Dụng Tuần Tự — Case eCPM Rewarded Video Giảm 15%

Tài liệu minh hoạ phối hợp bốn method qua một case cụ thể.

Method 1 phát hiện eCPM giảm từ ngày 20, đối chiếu changelog ngày 19 thấy "update ad network X". Method 2 bóc tách eCPM theo country, kết quả India giảm mạnh nhưng traffic India tăng. Method 3 dùng quan hệ `eCPM ∝ CTR`, kiểm tra CTR thấy giảm 30%. Method 4 so sánh với eCPM Banner thấy Banner vẫn ổn — vấn đề chỉ ở RV.

Insight tổng hợp: user spam request ads, network trả ads chất lượng kém nên CTR giảm. Action: giới hạn tần suất request, test reward coin, thay placement.

## Case Retention D1 Sụt 3%

Method 1: giảm từ ngày 15, changelog cùng ngày có "level 2 difficulty + ads frequency". Method 2: tách theo country và app version, thấy chỉ version 2.0 và region US bị ảnh hưởng (-4%). Method 3: kiểm tra session time cũng giảm, củng cố giả thuyết user nản. Method 4: so retention JP với US — JP vẫn ổn, US tụt.

Insight: user US cài version 2.0 thấy level 2 quá khó và ads early gây nản. Action: hạ độ khó, giảm ads spam, A/B test version 2.1. Liên hệ trực tiếp với [[hard-level-design]] — level early không nên là hard level.

## Liên Hệ / Ứng Dụng

Bốn phương pháp này là khung cốt lõi cho mọi bài toán root cause analysis trong game. Kết hợp với [[funnel-analysis|funnel]] (Method 2 thường tách funnel theo dimension), [[game-analytics-mindset|quy trình 6 bước]] (4 method là phần triển khai bước 5), và [[databuckets|Databuckets Query Builder]] (công cụ thực thi).

Quy trình tổng hợp tài liệu đề xuất: nhìn số → Method 1 (thời điểm) → Method 2 (dimension) → Method 3 (chỉ số liên quan) → Method 4 (tham chiếu) → segment & 5 Whys → chốt insight kèm action ưu tiên.

## Nguồn Tham Khảo

- `raw/papers/User Guideline _ Phương pháp phân tích & tối ưu Game.html` — Databuckets training guide, Phần "Phương Pháp Phân Tích Chỉ Số → Insight → Action", mục 5–7
