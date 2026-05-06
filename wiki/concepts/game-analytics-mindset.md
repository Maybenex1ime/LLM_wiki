---
title: "Game Analytics Mindset & Quy Trình 6 Bước"
source: "compiled"
date_added: 2026-05-06
tags: [concept, analytics, game-analytics, methodology, kpi]
aliases: [tư duy phân tích game, game analysis mindset, quy trình 6 bước]
status: draft
related:
  - "[[funnel-analysis]]"
  - "[[metric-diagnosis-4-methods]]"
  - "[[databuckets]]"
  - "[[rv-placement-strategy]]"
  - "[[hard-level-design]]"
summary: "Khung tư duy phân tích game — 5 nguyên tắc cốt lõi và quy trình 6 bước biến mục tiêu kinh doanh thành event tracking và action."
---

## Định Nghĩa

Game Analytics Mindset là khung tư duy chuẩn cho Product Owner, Game Designer và Data Analyst khi phân tích dữ liệu game. Khung này được trình bày trong tài liệu training của [[databuckets|Databuckets]] dưới dạng 5 nguyên tắc nền và một quy trình 6 bước. Triết lý cốt lõi: phân tích game là **mô phỏng lại hành vi người chơi**, biến mỗi bước hành vi thành chỉ số đo được, rồi truy ngược về hành động tối ưu.

Tài liệu nhấn mạnh: "Con số không phải insight. Insight phải trả lời **vì sao** và gợi ý **làm gì**." Chỉ số churn 60% chưa phải insight — "user out vì fail level 2 do tutorial booster thiếu" mới là insight.

## Năm Nguyên Tắc Cốt Lõi

**1. Bắt đầu từ mục tiêu sản phẩm.** Mọi phân tích phải xuất phát từ KPI cụ thể như D1/D7 retention, RV impressions, IAP conversion. Không có mục tiêu thì phân tích lan man và thiếu actionable. Tài liệu đối chiếu hai cách hỏi: "Mình muốn biết người chơi xem quảng cáo bao nhiêu lần" (mơ hồ) so với "Mình muốn tăng doanh thu ads, nên cần biết người chơi xem ads ở đâu, khi nào và vì sao họ không xem được" (gắn mục tiêu).

**2. Phân rã hành vi thành funnel.** Mọi mục tiêu lớn đều là kết quả của một chuỗi hành động nhỏ. Funnel mua IAP gồm `open_shop → view_item → click_item → purchase_success`. Funnel rewarded video gồm `rv_offer_shown → rv_click → rv_complete`. Từ funnel xác định bottleneck — nghẽn ở bước nào và vì sao. Xem chi tiết tại [[funnel-analysis]].

**3. Mô phỏng hành vi người chơi.** Đặt mình vào vai user để diễn lại hành trình. "Để user xem một video, họ thấy offer chưa? Offer có hấp dẫn? Có bị interstitial dày đặc khiến họ khó chịu?" Mỗi bước trong chuỗi mô phỏng tương đương với một thông tin cần đo lường, và mỗi thông tin tương đương với một event cần track.

**4. So sánh nhóm "có" vs "không".** Muốn biết yếu tố nào ảnh hưởng đến hành vi, đối chiếu nhóm có hành vi (mua IAP, dùng booster, xem ads) với nhóm không có. Khác biệt ở level reached, booster usage, ad engagement giúp khoanh vùng nguyên nhân.

**5. Câu hỏi phải đo được và actionable.** Mỗi câu hỏi cần kiểm tra hai điều: cần chỉ số nào để trả lời, và nếu biết kết quả thì team sẽ làm gì. Không dẫn đến action thì câu hỏi chưa quan trọng.

## Quy Trình 6 Bước

Quy trình biến mục tiêu kinh doanh thành chu trình phân tích khép kín.

**Bước 1 — Xác định mục tiêu.** Chốt KPI và cột mốc cụ thể. Ví dụ: D1 retention từ 40% lên 50%, D7 từ 15% lên 20%, RV từ 3 lên 6 impressions/user/ngày.

**Bước 2 — Đặt câu hỏi theo funnel và mô phỏng.** Mỗi mục tiêu lớn rẽ thành các câu hỏi nhỏ gắn với funnel. Ví dụ với retention: "Tại sao user out sau Day 1, 2? Họ nản ở level 5–6? Không có daily quest ngày 3? Session day 2 quá ngắn?"

**Bước 3 — Xác định thông tin cần biết.** Từ mỗi câu hỏi liệt kê thông tin cần để trả lời. Với "Vì sao D7 thấp?": user chơi đến level nào trong Day 3–5, fail rate và retry count ở level 5–15, thời gian login Day 2 và Day 4, có claim daily bonus không.

**Bước 4 — Quy định chỉ số và event tracking.** Biến thông tin thành event có param. Tên event phải cụ thể (`start_level`, `fail_level`) kèm param như `level_id`, `day_since_install`, `coin_balance`. Chỉ số thường gặp gồm tỷ lệ phần trăm (retention, CTR), số lần (impression, shop view), thời lượng (session time), distribution (level funnel).

**Bước 5 — Phân tích, ra insight, đưa action.** Xây dashboard, tìm bottleneck, đặt giả thuyết, ra hành động cụ thể. Ví dụ: insight "user fail level 2 vì booster tutorial thiếu" dẫn đến action "giảm chướng ngại level 2, thêm gợi ý booster, A/B test". Xem [[metric-diagnosis-4-methods]] cho phương pháp chẩn đoán chi tiết.

**Bước 6 — Theo dõi cohort và lặp lại.** Sau khi triển khai action, so sánh KPI cohort cũ và mới. KPI cải thiện thì duy trì hoặc scale up; không cải thiện thì A/B test tiếp. Tài liệu nhấn mạnh chu trình liên tục: phân tích → điều chỉnh → đo lường → phân tích tiếp.

## Liên Hệ / Ứng Dụng

Khung này áp dụng trực tiếp cho các bài design trong wiki. Quyết định về [[hard-level-design|hard level]] và [[easy-level-design|easy level]] đều cần kiểm chứng qua funnel completion và win rate. Vị trí [[rv-placement-strategy|RV placement]] cần đo qua funnel `rv_offer_shown → rv_click → rv_complete`. [[level-iteration-testing|S1–S4 testing]] là dạng cohort comparison ở quy mô nhỏ trước khi scale.

Triết lý đóng từ tài liệu: "Phân tích mà không ra action = mổ xẻ xong để đó. Action mà không gắn KPI = thay đổi mù quáng. Phải có vòng lặp khép kín: chỉ số → insight → action → đo lường."

## Nguồn Tham Khảo

- `raw/papers/User Guideline _ Phương pháp phân tích & tối ưu Game.html` — Databuckets training guide, case study "Brain Blocks"
