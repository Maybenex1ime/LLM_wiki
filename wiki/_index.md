---
title: "Wiki Index — Master Catalog"
date_added: 2025-01-01
status: canonical
summary: "Master index listing all wiki articles with summaries and aliases"
---

# 📚 Wiki Index

> Master catalog of the entire wiki. This file is automatically updated by the AI every time an article is added or removed.

**Total articles:** 102
**Last updated:** 2026-05-20

---

## Concepts (81 articles)

### Game Design Mindset & Business

| Article | Aliases | Summary |
|---------|---------|---------|
| [[gd-role-as-machine-link]] | vai trò game designer, define cho code và art | GD không phải vị trí ra lệnh — là mắt xích trong cỗ máy, có trách nhiệm define đủ thông tin cho code/art |
| [[5-levels-of-idea]] | 5 cấp độ idea, thang thuyết phục sếp | Thang 5 mức độ chín của game idea khi pitch sếp/CEO — từ mô tả như user đến idea original có CPI plan |
| [[ltv-cpi-formula]] | LTV vs CPI, ngoại suy D7 D60 | Khung số Hiệp dùng để bảo vệ dự án — phân tách inputs (CPI) và outputs (LTV), điều kiện duyệt: LTV > CPI |
| [[ecpm-blackbox]] | eCPM phụ thuộc cái gì, app quality | eCPM là biến doanh thu quảng cáo mà designer không kiểm soát — 2 game giống hệt có thể eCPM gấp 3 lần nhau |
| [[iaa-iap-migration]] | IAA sang IAP, hybrid monetization | Xu hướng studio mobile chuyển từ IAA sang IAP/hybrid — eCPM hyper sụp, puzzle dominate, IAP độc lập ad-network |
| [[daily-login-design]] | 3 mô hình daily login | 3 mô hình (7-day loop, 28-day no-loop bỏ qua, 28-day no-loop tiếp tục) và anti-pattern không define mục đích từ đầu |

### Level Design

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
| [[match3-difficulty-levers]] | 5 yếu tố tạo khó Match-3, tắc ẩn | 5 levers cốt lõi tạo độ khó Match-3: giới hạn tài nguyên, obstacle, bài trí, mục tiêu, tắc ẩn (RNG có chủ đích) |
| [[chip-spawn-algorithm]] | thuật toán sinh chip, adaptive key object | Logic spawn chip Match-3: limit màu, bias ô liền kề, tỷ lệ drop, adaptive key object theo số fail |
| [[match3-player-archetypes]] | 3 nhóm user Match-3 | First-Look (chọn combo to nhất), Logic (tính cascade), Scattered (đi không theo logic) |
| [[level-content-vs-level-data]] | 2 trục thiết kế level | Level Content (thêm element mới) vs Level Data (tăng/giảm số mu) — mix → khó control khi fix |
| [[asset-hardware-tradeoff]] | giới hạn phần cứng asset, chiều sâu vs chiều rộng | 10 vs 10 quân = chiều sâu, 30 vs 30 = chiều rộng. 100 con × 15k tris = vỡ trận |
| [[pattern-habit-break]] | phá thói quen người chơi | 3 level tạo thói quen → 1 level phá → user chết 1 lần → đạt tỷ lệ replay đã set |
| [[hidden-variable-difficulty]] | biến ẩn điều chỉnh khó, distract variable | 3 loại biến: trên mặt (rủi ro), biến ẩn (khuyến cáo), distract (đổi tông màu) |
| [[file-y-do-design-intent]] | file ý đồ, file tiêu chí | 2 file đầu vào (tiêu chí + ý đồ) + 1 file output (level design). Designer skip 2 file đầu → quên ý định giữa chừng |
| [[replay-rate-distribution]] | phân cực replay rate | Average 1.3 không đủ — phân cực 1.1 vs 1.5 = phục vụ 2 tập user, nên tách thành 2 sản phẩm |

### Phase Dự Án & Pacing

| Article | Aliases | Summary |
|---------|---------|---------|
| [[fueling-pacing]] | fueling, mũ nét, money knot | Tốc độ khai thác value qua thời gian. Game lãi D7+ khó hơn nhưng dễ scale hơn game lãi D0/D1 |
| [[balance-scale]] | balance scale, phân tỷ trọng module | Sơ đồ phân tỷ trọng tài nguyên giữa các module game (tổng 100%) — thêm module mới phải lấy bớt từ module khác |
| [[imba-balance-meta]] | imba balance, tường mới | Bán gói meta phải balance MTV vs Power tại checkpoint. Imba có chủ ý ngắn hạn ok, mất cân bằng dài hạn → game mất giá trị |
| [[retention-curve-design]] | R1 R3 R7 retention | Mỗi mốc retention (R1 trong session, D1 ngày sau, D3, D7) cần thiết kế khác — in-session vs cross-day |

### Monetization & IAP

| Article | Aliases | Summary |
|---------|---------|---------|
| [[inter-reward-ratio]] | Y:R ratio, tỷ lệ inter reward | Fix tổng ad/day, A/B tỷ lệ inter vs reward. 8:2 vs 7:3 không có đúng/sai |
| [[inter-ad-redefinition]] | inter là phích thời gian, không spam | Inter là phích thời gian giữa 2 session căng thẳng, không phải bộ đếm level để spam |
| [[feeling-of-assets]] | 6 đặc tính tài sản | Số lượng, chất lượng, khan hiếm, achievement, khoe tài sản, giá trị tăng theo thời gian |
| [[iap-pricing-user-value]] | định giá IAP, cất bằng sai đồng tiền | User value = thời gian chơi × giá phút theo quốc gia. Anti-pattern: bán $10 cho hero pack mở ra $300 worth journey |
| [[iap-purchase-drivers]] | 12 driver IAP, why people pay | Drivers IAP: giải quyết vấn đề liên tục, time-starve, aesthetic, social, phá giới hạn bản thân, rich-user impulse |
| [[rpg-unit-weakness-principle]] | unit weakness, tuning RPG | Mỗi unit S-tier ở 1 hệ phải C/B ở các hệ khác. Unit không weakness → game mỏng |
| [[piggy-bank-monetization]] | Piggy Bank, hút máu user | Tiền user kiếm tự động vào lợn, xem ad/IAP để rút. Chu kỳ 9-15 phút khớp session 40-50 phút |
| [[subscription-pack-design]] | subscription pack, Amanote case | Sub phù hợp game content/view (nhạc, đọc) — không phù hợp RPG/Battle |
| [[dark-ux-techniques]] | dark UX, arm break, đảo X3 | 6 kỹ thuật Dark UX: Click vs Hold, đảo pop-up nâng cấp, bán content khoá level, No Ad mix, Arm Break, đảo X3 |

### UI/UX

| Article | Aliases | Summary |
|---------|---------|---------|
| [[ux-3-criteria]] | 3 tiêu chí UX, 3 Giảm Thiểu | (1) số bước thao tác, (2) thông tin, (3) quản trị sự chú ý / giảm thiểu quyết định. Doc 6 P2 + Doc 7 |
| [[ux-yeu-ich-definition]] | yêu ích, dual-goal UX | UX = tối ưu trải nghiệm × tối đa lợi ích nhà sản xuất (từ sách Pháp inspire Apple) |
| [[behavior-vs-stated-preference]] | hành vi vs lời nói | User nói A làm B → design cho B. Case 3 quán ăn quen |
| [[inherited-habit-conventions]] | inherited habit, icon convention | Icon home/hotel/settings đã universal. Reinvent = phá habit, force re-learn |
| [[value-perception-techniques]] | big numbers, anchor, Highland upsell | 4 kỹ thuật: 100 gold > 1 gold, 33% > 7%, gift-on-package, +2k-3k size L |
| [[thumb-zone-design]] | thumb zone, phá UI | Nút quan trọng (IAP) phải nằm trong vùng ngón cái. Phá UI = cố tình lệch grid để hút mắt |
| [[notification-management]] | 5 loại noti, user vs designer priority | 5 loại noti (Reward/Playable/Mission/IAP/Ads). User và designer priority ngược nhau — chiến lược theo user trước |
| [[auto-equip-design]] | auto-equip 3 loại game | Auto-equip phù hợp game 1 hero (Loại 1) hoặc 10+ hero (Loại 3), không phù hợp 1-5 hero không có fun role (Loại 2b) |
| [[mep-mep-affordance]] | mép mép, edge affordance | Grid 5×6 + mép phía dưới = user reflex vuốt, không cần text/arrow guide |
| [[user-test-no-explanation]] | dont explain test | User hỏi = signal fail communication. Explain = invalidate data |
| [[icon-vs-text-framework]] | icon vs text, +1 slot text | D0-D7 icon+text; D7+ icon-only. Text cap 5-7 ký tự. Custom feature cần text |

### UI Wireframe & Hierarchy (Doc 6 Part 1)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[ui-wireframe-workflow]] | 3 bước UI, Core vs Flow | Vũ workflow VN: (1) chọn approach Core vs Flow, (2) draft vuông tròn tam giác + đắp case, (3) làm UI thật với levels |
| [[ui-button-3-levels]] | 3 level nút, Key Blue Hidden | Key (thumb zone gameplay), Blue (optional event/achievement), Hidden (settings/tab) |
| [[ui-button-3-spawn-types]] | popup state luồng lên đới | Mỗi nút trigger: (1) Popup báo cứng, (2) State của button, (3) Luồng phụ. List trước khi vẽ |
| [[ui-rule-max-2-levels]] | rule 2 tầng, max depth UI | UI tối đa 2 tầng menu. Setting → option (đúng); Setting → Music → Stereo/BGM/SFX (sai) |
| [[ui-5-color-brief]] | 5 màu UI brief | Đỏ (chú ý cao IAP), Cam (monetize ad), Vàng (core gameplay), Xanh lá (deemphasize), Xanh dương (rare confusion) |
| [[clash-royale-percent-stat-display]] | base × % per level | HP = Base × (1 + 10% × level). Đơn giản hơn table absolute. User nhớ base + level |

### Art & Animation (Doc 5)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[art-brief-3-parts]] | art brief 3 thành phần | Art Style (form, joints, ratios) + Level Detail (mật độ chi tiết) + Color (palette per đối tượng + contrast) |
| [[form-base-art-template]] | form base, con đầu tiên 10 điểm | Vẽ 1 con kỹ → fix tỷ lệ → các con sau đổi outfit/đầu, giữ chân tay. Production line-able |
| [[animation-brief-essentials]] | anim brief, frame chuẩn | Detail per action + transition + frame count + FPS + tương tác môi trường + biên độ theo form |
| [[hit-reaction-3-approaches]] | hit reaction 3 cách, dồn | Kệ mẹ (brawler), Block Time (song đấu), Anim Kêu Lại (chiến thuật cào bằng) |
| [[projectile-design-types]] | projectile 3 type | Cắt ra là chúng (default mass), Platformer (chạm thật), 3D real-position (homing/predict) |
| [[blend-animation-pattern]] | blend anim, combo chain | Fade-out + fade-in 0.1-0.2s. Tránh vẽ N² transition files. Combo + wall collision |
| [[gd-reverse-skin-time]] | GD reverse, fix skin time | Fix time trước (1s cast) → tính action nhồi → cân bằng số học. Result thực tế = lý thuyết |

### UX Foundation (Doc 6 Part 2)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[heart-system-design]] | tim, lives system | Có tim: tăng session/day + monetize gate. Không tim: gameplay gây nghiện. Ad-for-heart > paywall |
| [[multi-start-design]] | đa khởi đầu, class selection | 3 use cases (mạnh đầu/yếu đầu/phụ trợ), 3 risks (non-linear, balance mess, no restart). Encounter friendly fix regret |
| [[material-count-decision-paralysis]] | số loại material, 2 vs 4 | 2 loại = habit-driven. 4 loại = paralysis. Mix-match worse. Default 2 cho casual/mid-core |
| [[skin-bridging-comparison]] | ABC BCD ACD, skin overlap | Disjoint (ABC vs DEF) không so sánh được. Bridging (ABC/BCD/ACD) cho phép loại dần. A+ (same skill, stat khác) tối ưu |
| [[slot-locked-upgrade]] | level gắn slot không gắn con | Upgrade gắn slot (helmet, armor) → swap áo giữ level. Phá cơ chế trừng phạt, user experiment thoải mái |
| [[single-button-skill-collapse]] | Negabon 1-tap skill | Negabon (Hiệp) collapse Pokemon 4-tap skill flow → 1 tap. Tap thanh giữa = skill, thanh bên = attack |
| [[clash-of-clans-punishment-evolution]] | quân chết hồi, phá trừng phạt | 3 versions: V1 quân chết hẳn → V2 hồi 1 phút → V3 không chết. Mass studios phase out punishment |
| [[defending-design-decisions]] | bull start dự án bảo vệ | Document reasoning trước khi pitch. Test rẻ = thử. Test đắt = defend logic. Fail không reasoning = không iterate |

### User Segmentation

| Article | Aliases | Summary |
|---------|---------|---------|
| [[user-segmentation-3-axes]] | phân tập user, 3 yếu tố, T2 T3 T4 | 3 trục: sở thích (tài sản / thể hiện), tư chất (T2/T3/T4), tài chính (khả năng chi) |
| [[s-t-genre-grid]] | lưới ST, S×T grid, S1T2 | Lưới 2 chiều map genre vào archetype. S1T2 = casual repeat. S2T2-T4 = challenge cao tay |
| [[organic-rate-interpretation]] | organic rate, organic không phải designer chủ động | Organic rate cao không suy ra tập user trẻ. Là thuật toán Google, designer không kiểm soát |

### Analytics & Dashboards

| Article | Aliases | Summary |
|---------|---------|---------|
| [[game-analytics-mindset]] | tư duy phân tích game, quy trình 6 bước | Khung tư duy phân tích game — 5 nguyên tắc + quy trình 6 bước biến mục tiêu thành event tracking |
| [[funnel-analysis]] | phân tích funnel, conversion funnel | Funnel — chuỗi tuần tự các bước hành vi để xác định bottleneck (RV, IAP, retention funnel) |
| [[metric-diagnosis-4-methods]] | 4 method analysis, chẩn đoán KPI | 4 phương pháp khoanh vùng nguyên nhân biến động chỉ số — timing, dimension, related, reference |
| [[economy-balance-dashboard]] | economy dashboard, soft currency dashboard | 11 chart phân tích cân bằng kinh tế (Earn vs Sink) puzzle game — từ tổng thể đến level và segment |
| [[level-analytics-dashboard]] | level analytics, level performance dashboard | 22 chỉ số + 17 case pattern action cho từng level — engagement, drop, booster, pacing, monetization |
| [[monetization-dashboard]] | monetization dashboard, iap ads dashboard | 9 chart doanh thu IAP + Ads, ARPDAU, RPI, conversion, ad load, cohort revenue, purchase depth |
| [[offer-system-dashboard]] | offer dashboard, offer analytics | 5 chart hiệu quả Offer/Pack — revenue, volume, conversion từ shown, first purchase timing |
| [[player-journey-dashboard]] | player journey, level funnel dashboard | 6 chart hành trình người chơi — reach rate, churn level, win/lose có-không booster, playerbase |
| [[retention-dashboard]] | retention dashboard, dau pau dashboard | 6 chart retention theo cohort, DAU/PAU, install Paid vs Organic, session count & length |
| [[rv-placement-strategy]] | rewarded video placement, RV slot | Cách đặt RV slot trong level để monetize mà không cannibalize booster/IAP revenue |

## Tools (3 articles)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[lion-studios]] | Lion Studios by AppLovin | Publisher mobile casual games — nguồn của Level Design Playbook và MVP Guidelines |
| [[databuckets]] | Databuckets, query builder | Nền tảng analytics cho game với Query Builder dạng step-by-step |
| [[negaxy-iec-gd-course]] | khóa GD Negaxy IEC, GD Course 2026 | Khóa Game Design 8 buổi 2026 do Vũ + Hiệp đồng giảng — mindset, level design, phase dự án, UI/UX/monetize, phân tập user |

## People (3 articles)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[vu-negaxy]] | Vũ Negaxy, lecturer GD Course | Lecturer chính khóa GD Negaxy + IEC. Đặc trưng phân loại theo trục (S×T, 5 levels of idea), giảng qua case study |
| [[hiep-iec]] | Hiệp IEC, co-lecturer | Co-lecturer khóa GD Negaxy + IEC. Đóng góp LTV>CPI, test prototype không quảng cáo, giãn inter LTV 60-70% |
| [[giang-student]] | Giang IAA IAP, Giang Pull-the-Pin | Học viên case study lặp lại (Whale Content Burn, IAA→IAP migration, Pull-the-Pin multivariable, gói tướng meta) |

## Comparisons (15 articles)

| Article | Aliases | Summary |
|---------|---------|---------|
| [[prototype-vs-mvp]] | prototype vs MVP, phase dự án | Prototype = test idea nội bộ (sơ khai, ít biến); MVP = đẩy ra thị trường (đủ loop, ít feature) |
| [[d7-vs-d3-breakeven]] | D7 vs D3 hoà, lãi ở đây vs lãi ở đây mũ | Game lãi D3 dễ quyết định, hyper. Game lãi D7+ khó làm nhưng dễ scale qua UA |
| [[arpu-vs-arppu]] | ARPU vs ARPPU, whale heavy | ARPU = doanh thu / tổng user; ARPPU = / paying user. ERP nên đẩy ARPU qua pay rate |
| [[ui-vs-ux]] | UI vs UX, phân biệt | UI = cấu trúc nút/màn hình (làm được/không); UX = trải nghiệm tiện/quen |
| [[first-iap-strategy]] | first-IAP vs giữ giá trị, x2 vs x8 | First-time IAP: x2 (giữ tier balance) vs x8 (tối đa convert). Anti-pattern: lỡ cỡ giữa |
| [[level-data-vs-handcrafted]] | level data vs xếp tay, Excel vs Unity | Level Data (Excel/Grid) cho Match-3/Sort; Level Xếp Tay (Unity) cho Pull-the-Pin/Puzzle vật lý/RPG |
| [[mobile-vs-pc-console-skill]] | mobile vs PC, dung sai input | Mobile phải tối đa dung sai (user làm chưa đúng cũng cho làm đủ); PC/Console combo phức tạp OK |
| [[leaderboard-permanent-vs-seasonal]] | leaderboard vĩnh viễn vs theo mùa | Vĩnh viễn giữ whale; theo mùa cho user mới cơ hội. Trade-off: whale-retention vs user-acquisition |
| [[user-archetype-asset-vs-self-expression]] | tài sản vs thể hiện bản thân | Nhóm Tài Sản (RoK — build lòng vòng, đợi đủ lớn rồi đánh) vs Nhóm Thể Hiện (Chess, TD — build thẳng, PvP sớm) |
| [[equip-flow-hero-vs-weapon]] | equip từ hero vs từ weapon | Từ hero (3 bước, tutorial-friendly) vs từ weapon (3 bước, tổng quan rare hierarchy + icon owner). Vẽ 2 drafts để compare |
| [[vector-vs-bitmap-game-art]] | vector vs bitmap, format art game | Vector sharp at any zoom + outline 2-3 pixel (card games). Bitmap đẹp 100% nhưng vỡ zoom out |
| [[cast-time-cao-bang-vs-per-con]] | cast time approach | Cào bằng: code đơn giản, balance accurate. Per con: feel rich, balance lý thuyết ≠ thực tế |
| [[farm-game-resource-gates]] | Farm vs Hay Day vs Township | Cùng "trồng cây" nhưng resource gate khác → UX khác. Theft + seed → seed only → tiền + batch unlimited |
| [[clash-royale-vs-warcraft-rumble]] | skill-gated vs asset-friendly | Clash Royale = PvP skill gate (skill player). Warcraft Rumble = PvE asset-friendly (asset player). Forced choice archetype |
| [[hearthstone-vs-uvo-card-text]] | keyword compression vs dense | uvo dense text = niche. Hearthstone keyword (taunt, charge) = mass audience parse trong 2 giây |

---

## Raw Sources (19 documents)

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
| `raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset.md` | Video transcript (Buổi 1 — mindset, 485 dòng) | 2026-05-15 |
| `raw/videos/negaxy-iec-gd-doc-02-level-design.md` | Video transcript (Buổi 2 — level design, 364 dòng) | 2026-05-15 |
| `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` | Video transcript (Buổi 3 — phase dự án, 1313 dòng) | 2026-05-15 |
| `raw/videos/negaxy-iec-gd-doc-04-level-data-and-iap.md` | Video transcript (Buổi 4 — level data + IAP, 411 dòng) | 2026-05-15 |
| `raw/videos/negaxy-iec-gd-doc-05-part-1-art.md` | Video transcript (Buổi 5 P1 — Art, 327 dòng) | 2026-05-20 |
| `raw/videos/negaxy-iec-gd-doc-05-part-2-animation.md` | Video transcript (Buổi 5 P2 — Animation, 385 dòng) | 2026-05-20 |
| `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` | Video transcript (Buổi 6 P1 — UI, 463 dòng) | 2026-05-20 |
| `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` | Video transcript (Buổi 6 P2 — UX, ~470 dòng) | 2026-05-20 |
| `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` | Video transcript (Buổi 7 — UI/UX/Monetize, 631 dòng) | 2026-05-15 |
| `raw/videos/negaxy-iec-gd-doc-08-phan-tap-user.md` | Video transcript (Buổi 8 — phân tập user, 350 dòng) | 2026-05-15 |

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
