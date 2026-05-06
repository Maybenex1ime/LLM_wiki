---
title: "Funnel Analysis Trong Phân Tích Game"
source: "compiled"
date_added: 2026-05-06
tags: [concept, analytics, funnel, conversion, kpi]
aliases: [funnel analysis, phân tích funnel, conversion funnel]
status: draft
related:
  - "[[game-analytics-mindset]]"
  - "[[metric-diagnosis-4-methods]]"
  - "[[rv-placement-strategy]]"
  - "[[ftue-curve]]"
summary: "Funnel — chuỗi tuần tự các bước hành vi người chơi để xác định bottleneck và điểm rơi cần tối ưu."
---

## Định Nghĩa

Funnel là kỹ thuật bóc tách một mục tiêu hành vi (mua IAP, xem rewarded video, retention ngày 2) thành chuỗi tuần tự các bước nhỏ. Mỗi bước trở thành một event đo lường. Tỷ lệ chuyển đổi giữa các bước cho biết **bottleneck** — điểm người chơi rơi rớt nhiều nhất, từ đó khoanh vùng nguyên nhân và đưa action.

Tài liệu Databuckets mô tả funnel là một trong năm nguyên tắc cốt lõi của [[game-analytics-mindset|tư duy phân tích game]]: "Khi muốn user xem RV hoặc mua IAP, họ phải đi qua chuỗi bước. Funnel = liệt kê tuần tự hành động."

## Cấu Trúc Một Funnel

Mỗi funnel có ba thành phần. Một là chuỗi event tuần tự, đặt tên cụ thể với param đi kèm. Hai là chỉ số chuyển đổi giữa từng cặp bước liền kề (ví dụ `click_rate = rv_click / rv_offer_shown`). Ba là baseline tham chiếu để biết tỷ lệ thấp/cao — có thể là cohort cũ, region khác, hoặc benchmark sản phẩm tương tự.

Quy tắc đặt tên event: cụ thể (`start_level`, `fail_level` thay vì `level_action`), kèm param đủ phân tích (`level_id`, `day_since_install`, `coin_balance`).

## Ba Funnel Chuẩn Cho Puzzle Game

**Funnel rewarded video.** Chuỗi `rv_offer_shown → rv_click → rv_complete`. Param quan trọng: `placement` (end-level, lose-level, daily-bonus x2), `reward_type` (coin/booster). Câu hỏi tài liệu đề xuất: "Bao nhiêu user thấy offer? Bao nhiêu click? Reward có đủ hấp dẫn? Interstitial có quá nhiều?" Liên hệ trực tiếp với [[rv-placement-strategy]].

**Funnel IAP.** Chuỗi `open_shop → view_item → click_item → purchase_success`. Param: `item_id`, `item_type`, `price`, `shop_source`. Mục đích: phát hiện khoảng cách giữa user mở shop và user thực mua. Tài liệu nêu giả thuyết phổ biến: "Shop quá khuất, freebies nhiều nên user không cần, starter pack chưa hiển thị."

**Funnel retention.** Chuỗi `daily_login → start_level → end_level → win/fail → time_spent_level`, soi qua nhiều ngày. Phân tích thường tách theo `day_since_install` để tìm ngày nào drop-off bất thường. Liên hệ với [[ftue-curve]] — fail rate ở 20–25 level đầu là một trong những drop-off điểm chính.

## Phân Tích Bottleneck

Sau khi dựng funnel, đọc tỷ lệ chuyển đổi giữa các cặp bước liền kề. Tài liệu hướng dẫn quy trình tư duy: tách cohort theo dimension (country, version, level bracket), so sánh nhóm có hành vi với nhóm không có, đặt giả thuyết theo 5 Whys, kiểm tra logic với các chỉ số liên quan.

Ví dụ ứng dụng từ tài liệu: "Phân tích shop open rate cao nhưng purchase thấp" — bottleneck nằm giữa `view_item` và `purchase_success`. Giả thuyết có thể là giá quá cao, freebies dư thừa, hoặc UI gói không rõ. Mỗi giả thuyết dẫn đến action khác nhau.

## Liên Hệ / Ứng Dụng

Funnel là công cụ trung tâm của [[game-analytics-mindset|quy trình 6 bước]] tại bước 2 (đặt câu hỏi theo funnel) và bước 5 (phân tích bottleneck). Khi kết hợp với [[metric-diagnosis-4-methods|4 phương pháp chẩn đoán chỉ số]], funnel cung cấp granularity cần thiết để truy nguyên nhân biến động KPI tổng.

Trong puzzle game, funnel ứng dụng cho mọi hệ thống monetization: [[booster-design-puzzle|booster usage]], [[rv-placement-strategy|RV slots]], starter pack/flash sale conversion. Từng hệ thống có funnel riêng nhưng cùng nguyên tắc đo lường.

## Nguồn Tham Khảo

- `raw/papers/User Guideline _ Phương pháp phân tích & tối ưu Game.html` — Databuckets training guide, Phần II–III & V
