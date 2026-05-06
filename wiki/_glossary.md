---
title: "Glossary"
date_added: 2025-01-01
status: canonical
summary: "Key terms and definitions used across the wiki"
---

# 📖 Glossary

> Definitions of key terms used across the wiki. The AI adds terms here during `/compile` when it encounters important terminology.

---

## ARPU
**Translation:** Average Revenue Per User
**Definition:** Doanh thu trung bình trên mỗi người chơi. Track riêng theo level (Level ARPU) và cumulative (Cum ARPU).
**See also:** [[level-iteration-testing]]

## ARPDAU
**Translation:** Average Revenue Per Daily Active User
**Definition:** Doanh thu trung bình mỗi user active/ngày. `Total_ARPDAU = Total_rev / DAU`. Tách thành `IAP_ARPDAU` và `Ad_ARPDAU` để biết cấu trúc revenue.
**See also:** [[monetization-dashboard]]

## Bottleneck
**Translation:** Điểm nghẽn
**Definition:** Bước trong funnel có drop-off lớn nhất, là nơi cần tập trung tối ưu để cải thiện chỉ số tổng.
**See also:** [[funnel-analysis]]

## Booster Combo
**Translation:** Tổ hợp booster
**Definition:** Tập hợp các loại booster mà game có. Lion Studios khuyến nghị `1PA+1SE`, `1PA+1SE+1RD`, hoặc `2PA+1SE+1RD`.
**See also:** [[booster-design-puzzle]]

## Cohort
**Translation:** Nhóm cùng kỳ
**Definition:** Nhóm người chơi có cùng đặc điểm về thời điểm cài đặt (ví dụ: cài tuần 1/10–7/10). Dùng để so sánh KPI trước-sau khi triển khai action.
**See also:** [[metric-diagnosis-4-methods]], [[level-iteration-testing]]

## Cooldown Level
**Translation:** Level xả áp lực
**Definition:** Easy level đặt ngay sau hard level để giảm tension trước khi tăng difficulty trở lại.
**See also:** [[level-funnel-heartbeat]]

## DAU / PAU
**Translation:** Daily Active Users / Paying Active Users
**Definition:** DAU = số user unique active trong ngày. PAU = số user phát sinh revenue trong ngày. PAU/DAU = IAP conversion rate. Theo XGAME: "PAU luôn phải phân tích cùng DAU."
**See also:** [[retention-dashboard]], [[monetization-dashboard]]

## Drop Rate (Sub-Types)
**Translation:** Tỷ lệ rời bỏ (3 sub-type)
**Definition:** `drop_af_lose` (drop sau thua), `drop_af_win` (drop sau thắng), `drop_bf_complete` (drop trước hoàn tất). Tổng 3 sub-type = 100% total drop. Mỗi sub-type chỉ ra nguyên nhân khác nhau.
**See also:** [[level-analytics-dashboard]]

## eCPM
**Translation:** Effective Cost Per Mille (1000 impressions)
**Definition:** Doanh thu trung bình quảng cáo trên mỗi 1000 lượt hiển thị. eCPM tỷ lệ với CTR; Earnings = eCPM × impressions.
**See also:** [[metric-diagnosis-4-methods]], [[rv-placement-strategy]]

## Earn / Sink
**Translation:** Nguồn kiếm / Nguồn tiêu (soft currency)
**Definition:** Earn = nguồn người chơi nhận soft currency (complete level, ads, event). Sink = nguồn tiêu thụ (booster, revive, lives). Cân bằng Earn vs Sink quyết định economy có inflation hay choke.
**See also:** [[economy-balance-dashboard]]

## Choke Point
**Translation:** Điểm tắc tiền
**Definition:** Level hoặc giai đoạn mà người chơi cạn soft currency và không thể tiến tiếp. Trái ngược với inflation.
**See also:** [[economy-balance-dashboard]], [[hard-level-design]]

## Inflation (Economy)
**Translation:** Lạm phát kinh tế game
**Definition:** Trạng thái Earn > Sink kéo dài, người chơi tích trữ soft currency mà không cần mua thêm — làm giảm IAP conversion.
**See also:** [[economy-balance-dashboard]]

## Soft Currency
**Translation:** Tiền mềm
**Definition:** Tiền tệ trong game kiếm được qua gameplay (không phải IAP). Phổ biến gọi là Gold, Coin. Đối lập với hard currency (gem, diamond — chỉ mua bằng tiền thật).
**See also:** [[economy-balance-dashboard]]

## Funnel
**Translation:** Phễu hành vi
**Definition:** Chuỗi tuần tự các bước hành vi người chơi (ví dụ: `rv_offer_shown → rv_click → rv_complete`). Mỗi bước là một event đo lường, tỷ lệ chuyển đổi giữa các bước cho biết bottleneck.
**See also:** [[funnel-analysis]], [[game-analytics-mindset]]

## Foreseeable Failure
**Translation:** Fail nhìn thấy trước
**Definition:** Cơ chế cho phép người chơi nhận thức được fail đang đến trước khi nó xảy ra, tạo window để bán booster.
**See also:** [[hard-level-design]]

## FTUE
**Translation:** First Time User Experience
**Definition:** Trải nghiệm 20-25 levels đầu của người chơi mới. Bao gồm 3 lớp: difficulty curve, mechanic introduction, booster rollout.
**See also:** [[ftue-curve]]

## Heartbeat Pattern
**Translation:** Mẫu nhịp tim
**Definition:** Pattern phân bố hard/mid/easy levels trong daily loop để tạo tension/relief flow. Khác với heartbeat within a level.
**See also:** [[level-funnel-heartbeat]], [[hard-level-design]]

## Reach Rate
**Translation:** Tỷ lệ user đạt level
**Definition:** `Reach Rate = Số user đạt level X / Tổng user FO (First Open)`. Curve reach rate theo level chính là [[funnel-analysis|funnel]] retention theo progression.
**See also:** [[player-journey-dashboard]], [[level-analytics-dashboard]]

## RPI
**Translation:** Revenue per Install
**Definition:** `RPI = Tổng revenue từ cohort / số install cohort`, đo theo retention day. Cho biết monetize tập trung early hay long tail, có phụ thuộc whale không.
**See also:** [[monetization-dashboard]]

## Whale
**Translation:** Người chơi chi tiêu lớn
**Definition:** Số ít user chi nhiều USD (vd: `IAP_user_percent` thấp + `IAP_rev` cao = whale-driven). Tài liệu XGAME cảnh báo "whale risk cao" khi 1 pack chiếm >30% revenue.
**See also:** [[monetization-dashboard]], [[offer-system-dashboard]]

## Insight (vs. Metric)
**Translation:** Hiểu biết cốt lõi
**Definition:** Insight là lời giải thích "vì sao" và gợi ý "làm gì" — không phải con số. "Churn 60%" là metric; "user out vì fail level 2 do tutorial booster thiếu" là insight.
**See also:** [[game-analytics-mindset]], [[metric-diagnosis-4-methods]]

## Near-Miss
**Translation:** Suýt thắng
**Definition:** Cơ chế để fail xảy ra sau khi người chơi đã hoàn thành 60-80% level, kích hoạt cảm xúc "suýt nữa thì xong" → trigger revive.
**See also:** [[hard-level-design]]

## PA / SE / RD
**Translation:** Progression Accelerator / Strategic Enhancer / Revenue Driver
**Definition:** 3 function types của booster theo phân loại Lion Studios. PA giúp clear blocker; SE thêm tactical depth; RD là premium tool.
**See also:** [[booster-design-puzzle]]

## Perceived Difficulty
**Translation:** Độ khó cảm nhận
**Definition:** Mức độ khó mà người chơi cảm thấy, khác với actual fail rate. Cùng fail rate, perceived high → 2.5x RV watch.
**See also:** [[hard-level-design]]

## RV (Rewarded Video)
**Translation:** Quảng cáo có thưởng
**Definition:** Ad format cho phép người chơi xem video để nhận reward trong game. Power = amount × placement reach.
**See also:** [[rv-placement-strategy]]

## S1-S4 (Testing Phases)
**Translation:** 4 giai đoạn iteration testing
**Definition:** S1 basic mechanics; S2 initial data check; S3 heartbeat optimize + 4-5 mechanics; S4 ARPU + coin sinks optimization.
**See also:** [[level-iteration-testing]]

## Warm-up Level
**Translation:** Level làm nóng
**Definition:** Level đặt sau cooldown, re-increase difficulty từ từ. Không gây fails nhiều nhưng player phải cẩn thận.
**See also:** [[level-funnel-heartbeat]]
