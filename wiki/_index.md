---
title: "Wiki Index — Master Catalog"
date_added: 2025-01-01
status: canonical
summary: "Master index listing all wiki articles with summaries and aliases"
---

# 📚 Wiki Index

> Master catalog of the entire wiki. This file is automatically updated by the AI every time an article is added or removed.

**Total articles:** 20
**Last updated:** 2026-05-06

---

## Concepts (18 articles)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[hard-level-design]] | thiết kế level khó, hard level | Hard level là currency sink để trigger booster/revive — không phải để chặn người chơi |
| [[easy-level-design]] | thiết kế level dễ, easy level | Easy level <1.3 attempts — chứa monetization potential lớn nếu làm khó hơn 1 chút và ngắn hơn 20% |
| [[ftue-curve]] | first time user experience, onboarding curve | Curve fail rate cho 20-25 levels đầu của puzzle game — 0-5% → 8-10% → 15% → 20% |
| [[level-funnel-heartbeat]] | heartbeat pattern, difficulty pattern | Pattern bố trí hard/mid/easy levels trong daily loop — 20-25% hard levels, gap 4-6 giữa 2 hard |
| [[booster-design-puzzle]] | thiết kế booster, booster combo | 3 function types (PA/SE/RD), combo composition, rollout schedule |
| [[new-mechanic-introduction]] | introduce mechanic mới, mechanic rollout | Khi nào và cách introduce mechanic mới — D0/D1 explore (2-3), D2-D4 (1/day), D5+ every other day |
| [[timer-design]] | thiết kế timer, time-based puzzle | Quy trình set timer cho puzzle level — before/after first test methodology |
| [[level-iteration-testing]] | iteration testing, S1-S4 testing | 4 phases test (S1-S4) và quick funnel/level fix techniques |
| [[rv-placement-strategy]] | rewarded video placement, RV slot | Cách đặt RV slot trong level để monetize mà không cannibalize booster/IAP revenue |
| [[game-analytics-mindset]] | tư duy phân tích game, quy trình 6 bước | Khung tư duy phân tích game — 5 nguyên tắc + quy trình 6 bước biến mục tiêu thành event tracking |
| [[funnel-analysis]] | phân tích funnel, conversion funnel | Funnel — chuỗi tuần tự các bước hành vi để xác định bottleneck (RV, IAP, retention funnel) |
| [[metric-diagnosis-4-methods]] | 4 method analysis, chẩn đoán KPI | 4 phương pháp khoanh vùng nguyên nhân biến động chỉ số — timing, dimension, related, reference |
| [[economy-balance-dashboard]] | economy dashboard, soft currency dashboard | 11 chart phân tích cân bằng kinh tế (Earn vs Sink) puzzle game — từ tổng thể đến level và segment |
| [[level-analytics-dashboard]] | level analytics, level performance dashboard | 22 chỉ số + 17 case pattern action cho từng level — engagement, drop, booster, pacing, monetization |
| [[monetization-dashboard]] | monetization dashboard, iap ads dashboard | 9 chart doanh thu IAP + Ads, ARPDAU, RPI, conversion, ad load, cohort revenue, purchase depth |
| [[offer-system-dashboard]] | offer dashboard, offer analytics | 5 chart hiệu quả Offer/Pack — revenue, volume, conversion từ shown, first purchase timing |
| [[player-journey-dashboard]] | player journey, level funnel dashboard | 6 chart hành trình người chơi — reach rate, churn level, win/lose có-không booster, playerbase |
| [[retention-dashboard]] | retention dashboard, dau pau dashboard | 6 chart retention theo cohort, DAU/PAU, install Paid vs Organic, session count & length |

## Tools (2 articles)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[lion-studios]] | Lion Studios by AppLovin | Publisher mobile casual games — nguồn của Level Design Playbook và MVP Guidelines |
| [[databuckets]] | Databuckets, query builder | Nền tảng analytics cho game với Query Builder dạng step-by-step |

## People (0 articles)

| Article | Aliases | Summary |
|---------|---------|---------|
| _Empty_ | | |

## Comparisons (0 articles)

| Article | Aliases | Summary |
|---------|---------|---------|
| _Empty_ | | |

---

## Raw Sources (9 documents)

| Source | Type | Date Ingested |
|--------|------|---------------|
| `raw/papers/Lion Studios MVP Guide.pptx.pdf` | Paper (PPTX→PDF, 17 pages) | 2026-05-05 |
| `raw/papers/Lion.pdf` | Paper (Level Design Playbook, 32 pages, image-based) | 2026-05-05 |
| `raw/papers/User Guideline _ Phương pháp phân tích & tối ưu Game.html` | Paper (Databuckets training guide, ~1150 lines extracted) | 2026-05-06 |
| `raw/papers/XGAME_DA_ ..._Economy.pdf` | Paper (XGAME Economy dashboard, 10 pages, 11 charts) | 2026-05-06 |
| `raw/papers/XGAME_DA_ ..._Level Analytics.md` | Markdown (XGAME Level Analytics guide, 386 lines) | 2026-05-06 |
| `raw/papers/XGAME_DA_ ..._Monetization.pdf` | Paper (XGAME Monetization dashboard, 7 pages, 9 charts) | 2026-05-06 |
| `raw/papers/XGAME_DA_ ..._Offer System.pdf` | Paper (XGAME Offer System dashboard, 5 pages, 5 charts) | 2026-05-06 |
| `raw/papers/XGAME_DA_ ..._Player Journey.pdf` | Paper (XGAME Player Journey dashboard, 6 pages, 6 charts) | 2026-05-06 |
| `raw/papers/XGAME_DA_ ..._Retention.pdf` | Paper (XGAME Retention dashboard, 5 pages, 6 charts) | 2026-05-06 |

---

## Meta Files

| File | Purpose |
|------|---------|
| `overview.md` | Executive summary for cross-project access |
| `_index.md` | Master index (this file) |
| `_glossary.md` | Term glossary |
| `_absorb_log.json` | Tracks which raw sources have been compiled |
| `_ops_log.md` | Operations log (chronological) |
| `_backlinks.json` | Reverse link index |
| `_build_backlinks.py` | Script to auto-build backlinks |
