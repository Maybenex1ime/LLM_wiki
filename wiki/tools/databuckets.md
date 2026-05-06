---
title: "Databuckets"
source: "compiled"
date_added: 2026-05-06
tags: [tool, analytics, data-platform, game-analytics]
aliases: [Databuckets, query builder]
status: draft
related:
  - "[[game-analytics-mindset]]"
  - "[[funnel-analysis]]"
  - "[[metric-diagnosis-4-methods]]"
summary: "Nền tảng analytics cho game với Query Builder dạng step-by-step, hướng đến Product Owner và Data Analyst."
---

## Tổng Quan

Databuckets là nền tảng phân tích dữ liệu game dành cho Product Owner, Game Designer và Data Analyst. Tài liệu training "User Guideline | Phương pháp phân tích & tối ưu Game" do đội ngũ Databuckets phát hành, dùng case study giả định "Brain Blocks" (puzzle level-based) để hướng dẫn người dùng cách biến câu hỏi kinh doanh thành chỉ số đo được.

Đặc trưng tiếp cận của Databuckets: hướng dẫn người dùng tự xác định thông tin cần biết, xây chỉ số và thiết kế event tracking thay vì chỉ cung cấp dashboard có sẵn. Triết lý tài liệu: "Bản chất dữ liệu là Event-based, nhưng góc phân tích thường là theo User, Session… Xác định sai góc, kết quả sẽ khó diễn giải."

## Vai Trò Trong Phân Tích Game

Databuckets phục vụ vòng lặp dữ liệu khép kín mà tài liệu mô tả: chỉ số → insight → action → đo lường. Cụ thể, công cụ hỗ trợ ba khâu quan trọng. Một là dựng [[funnel-analysis|funnel]] hành vi (RV, IAP, retention) qua Funnel Chart. Hai là so sánh cohort cài đặt khác nhau qua Cohort Chart. Ba là segment người chơi (có/không hành vi) qua Segmentation Tool.

Công cụ cung cấp tính năng Share cho phép gắn Variables (time range, country) để người nhận tự tuỳ chỉnh báo cáo, hỗ trợ luân chuyển insight giữa các vai trò trong team.

## Query Builder — Quy Trình Step-By-Step

Query Builder của Databuckets dùng cách tiếp cận chia nhỏ phép tính phức tạp thành nhiều step. Tài liệu mô tả pattern chuẩn cho bài toán tỷ lệ phần trăm (retention rate, conversion rate, IAP rate).

**Step 0** tính mẫu số bằng aggregation phù hợp (`count_distinct`, `sum`, `count`). Ví dụ tính `iap_rate per country`: Step 0 group theo country, count distinct user_pseudo_id thành alias `active_user`.

**Step 1** tính tử số tương tự nhưng có filter điều kiện. Ví dụ: count distinct user_pseudo_id với filter `event_name = iap` thành alias `iap_user`.

**Step 2** dùng "Add previous column" để kéo cả hai số liệu vào cùng một bảng, rồi viết formula `iap_user / active_user * 100` thành alias `iap_rate`.

Tài liệu khuyến nghị: alias đặt tên rõ nghĩa (`conversion_rate`, `active_user_count`), set Invisible cho các cột trung gian kỹ thuật, dùng Pivot và Time Bucket để xoay theo dimension thời gian hoặc quốc gia, sort/limit để lấy top X giá trị quan trọng.

## Tám Bước Tư Duy Từ Câu Hỏi Đến Insight

Tài liệu trình bày quy trình tám bước cho một phân tích hoàn chỉnh trong Databuckets. Bước 1 xác định vấn đề và mục tiêu sử dụng insight. Bước 2 chọn chủ thể (User, Session, Event, Content) và đơn vị phân tích. Bước 3 thu hẹp scope qua time range, filter, dataset. Bước 4 viết công thức tự nhiên cho chỉ số bằng tiếng Việt hoặc pseudo-code. Bước 5 dịch công thức sang Query Builder theo pattern Step 0/1/2 ở trên. Bước 6 tối ưu hiển thị (alias, invisible, pivot, sort). Bước 7 kiểm nghiệm logic (tỷ lệ có vượt 100% không, kết quả có quá lớn hay quá nhỏ). Bước 8 chia sẻ qua Share hoặc đào sâu bằng Multi Steps, Sequence, Transform.

## Lợi Thế / Hạn Chế

Lợi thế từ tài liệu: cách tiếp cận step-by-step buộc analyst tách rõ tử/mẫu số và group by, giảm sai sót logic. Variables trong Share giúp người nhận tự khám phá thay vì chờ analyst chạy lại query. Tích hợp sẵn Funnel Chart, Cohort Chart, Segmentation Tool đáp ứng các use case phổ biến nhất của game analytics.

Tài liệu không trình bày hạn chế của công cụ. Đánh giá khách quan cần thông tin từ nguồn khác.

## Nguồn Tham Khảo

- `raw/papers/User Guideline _ Phương pháp phân tích & tối ưu Game.html` — Databuckets training guide chính thức
