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

## Booster Combo
**Translation:** Tổ hợp booster
**Definition:** Tập hợp các loại booster mà game có. Lion Studios khuyến nghị `1PA+1SE`, `1PA+1SE+1RD`, hoặc `2PA+1SE+1RD`.
**See also:** [[booster-design-puzzle]]

## Cooldown Level
**Translation:** Level xả áp lực
**Definition:** Easy level đặt ngay sau hard level để giảm tension trước khi tăng difficulty trở lại.
**See also:** [[level-funnel-heartbeat]]

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
