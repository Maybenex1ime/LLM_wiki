---
title: "Level Analytics Dashboard — Phân Tích Chỉ Số Theo Level"
source: "compiled"
date_added: 2026-05-06
tags: [concept, analytics, level-analytics, dashboard, puzzle]
aliases: [level analytics, dashboard level analytics, level performance dashboard]
status: draft
related:
  - "[[game-analytics-mindset]]"
  - "[[funnel-analysis]]"
  - "[[metric-diagnosis-4-methods]]"
  - "[[economy-balance-dashboard]]"
  - "[[hard-level-design]]"
  - "[[easy-level-design]]"
  - "[[booster-design-puzzle]]"
summary: "22 chỉ số phân tích level và 17 case pattern action — engagement, drop, booster, pacing, monetization theo từng level."
---

## Định Nghĩa

Level Analytics Dashboard là bộ chỉ số chi tiết cho từng level trong puzzle game, được mô tả trong tài liệu hướng dẫn của XGAME. Dashboard chia thành ba lớp phân tích: **engagement** (start, win/lose, retry), **drop analysis** (3 sub-types), và **monetization** (revenue breakdown theo source). Tài liệu liệt kê 22 chỉ số gốc và 17 case pattern có sẵn action tương ứng.

Tài liệu nhấn mạnh nguyên tắc đọc: "Trước khi đọc, cần xác định rõ bạn đang muốn trả lời câu hỏi gì. Nếu không xác định trước mục tiêu, rất dễ bị đọc trong quá nhiều chỉ số." Sáu câu hỏi mặc định: level nào gây drop, level nào quá khó/dễ, level nào gây uninstall, level nào monet tốt nhưng đánh đổi retention, có vấn đề booster/timer/pacing không, version mới có thay đổi hành vi level không.

## Engagement Metrics

`reach_rate` đo tỷ lệ user tới được level (số user start level / tổng input user). `start_users` là số user đã bắt đầu level ít nhất một lần. `start_times_per_users` là trung bình số lần start level/user — chỉ số cao gợi ý level khó hoặc hấp dẫn.

`win_rate` = tổng win / tổng lượt chơi level (mức độ khó kỹ thuật). `win_user_rate` = số user thắng / số user start level (mức độ khó từ góc nhìn user). Kết hợp hai chỉ số: `win_rate` thấp + `win_user_rate` cao → level khó nhưng hấp dẫn (user retry nhiều lần). `win_rate` thấp + `win_user_rate` thấp → level khó và không đủ hấp dẫn.

`lose_rate`, `lose_user_rate` tương tự cho thua. `lose_times_per_users` = trung bình số lần thua/user — cao có nghĩa user kiên nhẫn retry. `retry_af_lose_rate` = số user chơi lại sau thua / số user thua, đo độ hấp dẫn của level.

## Drop Analysis (3 Sub-Metrics)

`drop_rate.total_drop` đo tỷ lệ user chỉ chơi đến level đó rồi không quay lại trong khoảng Drop Time. Tài liệu chia drop thành ba sub-type, tổng luôn bằng 100%.

`drop_rate.drop_af_lose` — drop sau thua. Cao thì level quá khó hoặc trải nghiệm thất bại tệ. `drop_rate.drop_af_win` — drop sau thắng. Cao thì UX sau win có vấn đề (popup quảng cáo phá flow, reward không hấp dẫn, không có hook cho level kế). `drop_rate.drop_bf_complete` — drop trước khi hoàn tất. Cao ở early game là tự nhiên (user lọc), cao ở mid/late thì level dài hoặc khó hiểu.

## Booster Behavior

`use_booster_rate` đo tỷ lệ user dùng booster tại level. `use_booster_times_per_user` = số lần booster trung bình/user. `lose_af_use_booster_rate` = user dùng booster mà vẫn thua / tổng user dùng booster — chỉ số phán xét trực tiếp hiệu quả booster.

Tài liệu đề xuất threshold của Lion Studios style: nếu `use_booster_rate` thấp + `lose_af_use_booster_rate` cao → booster yếu hoặc user không tin booster, cần buff hoặc thiết kế lại. Liên hệ trực tiếp với [[booster-design-puzzle|booster design framework]].

## Pacing & Time Metrics

`avg_play_time`, `avg_win_time`, `avg_lose_time` đo thời lượng trung bình. `avg_progress` = trung bình % tác vụ hoàn thành trước khi thua (đo "user đã đi được bao xa"). Phát hiện: `avg_lose_time < avg_win_time` cho thấy user thua sớm — pacing đầu level có vấn đề. `avg_progress < 30%` ở mid-game gợi ý hướng dẫn không rõ.

## Monetization Per Level

`rev` = tổng doanh thu level (Ad + IAP). `ad_rev` / `IAP_rev` chia theo nguồn. `ad_LTV` / `IAP_LTV` = giá trị tích lũy từ level 1 đến level N / tổng user mở game — đo LTV theo progression. `ad_user_percent` / `IAP_user_percent` = tỷ lệ user xem ads / mua IAP tại level. `ad_imp_per_user` = số impression ads/user — tài liệu cảnh báo phải đối chiếu với drop_rate để tránh "ép quảng cáo" gây churn.

`IAP_rev` cao nhưng `IAP_user_percent` thấp → hành vi whale (số ít user chi nhiều). Nguyên tắc đối ứng từ [[easy-level-design|easy level design]]: easy level là nơi nhồi reward không phù hợp — chart breakdown này verify trực tiếp.

## Case Patterns Có Sẵn Action

Tài liệu mô tả 17 case pattern; sáu pattern phổ biến nhất.

**Case 1 — `win_rate` thấp + `lose_times_per_user` thấp.** User thua một lần rồi bỏ. Action: kiểm tra độ hấp dẫn gameplay, cải thiện trải nghiệm sau thua (reward, gợi ý), giảm pacing.

**Case 2 — `drop_rate.drop_af_lose` cao.** Level quá khó hoặc trải nghiệm thua tệ. Action: rà số bước, độ random, may rủi; thêm reward động viên sau thua; check pacing.

**Case 3 — `drop_rate.drop_af_win` cao.** UX sau win có vấn đề. Action: kiểm tra reward win, popup/quảng cáo cắt mạch, tạo hook cho level kế (teaser, mini-story).

**Case 4 — `use_booster_rate` thấp + `lose_af_use_booster_rate` cao.** Booster yếu, user mất niềm tin. Action: tăng sức mạnh, làm rõ hiệu ứng, mở booster cấp cao premium.

**Case 5 — `rev` cao + `drop_rate` cao.** Monet tốt nhưng đánh đổi retention. Action: A/B test giảm ad density, kiểm tra `ad_imp_per_user` quá tải, đánh đổi 7–8% revenue có đáng mất 20–30% user không.

**Case 6 — `ad_rev_per_user` tăng tại level `win_rate` thấp.** User kẹt → chơi lại → xem nhiều ads. Tài liệu khuyên: nếu `drop_rate` chấp nhận được, giữ và tận dụng; nếu drop cao, cân lại độ khó.

## Liên Hệ / Ứng Dụng

Dashboard này là phân tích chi tiết nhất ở cấp level — bổ sung cho [[economy-balance-dashboard|economy dashboard]] (vĩ mô) và [[player-journey-dashboard|player journey dashboard]] (funnel level). Khi áp dụng [[metric-diagnosis-4-methods|4 phương pháp chẩn đoán]], dashboard này thường là nơi triển khai Method 2 (bóc tách dimension theo level) cho các KPI vĩ mô. 17 case pattern là implementation cụ thể của bước 5 ("phân tích → insight → action") trong [[game-analytics-mindset|quy trình 6 bước]].

Verify quan trọng: nếu áp dụng [[hard-level-design|hard level design framework]], các hard level dự kiến phải có `win_rate` thấp + `win_user_rate` cao (user retry) + `use_booster_rate` cao + `ad_rev_per_user` cao. Nếu thực tế chỉ có `win_rate` thấp đơn lẻ → hard level đang trở thành choke point thay vì monetization trigger.

## Nguồn Tham Khảo

- `raw/papers/XGAME_DA_ Hướng dẫn đọc phân tích các chart trong dashboard_Level Analytics.md` — XGAME DA Level Analytics guide, 386 dòng
