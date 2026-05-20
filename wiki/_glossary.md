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
**Definition:** Doanh thu trung bình trên mỗi người chơi (kể cả free user). Track riêng theo level (Level ARPU) và cumulative (Cum ARPU). Vũ khuyến cáo game ERP đẩy ARPU qua tăng pay rate, không chỉ ARPPU.
**See also:** [[level-iteration-testing]], [[arpu-vs-arppu]]

## ARPPU
**Translation:** Average Revenue Per Paying User
**Definition:** Doanh thu / chỉ số user đã trả tiền. ARPPU cao + pay rate thấp = whale-heavy; ARPPU cân bằng + pay rate cao = distributed.
**See also:** [[arpu-vs-arppu]]

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

## 5 Levels Of Idea
**Translation:** Thang 5 mức độ chín idea
**Definition:** Khung Vũ phân tầng idea khi pitch sếp: L1 (mô tả như user), L2 (bóc tách element), L3 (cách triển khai), L4 (logic monetization), L5 (original có giải pháp CPI).
**See also:** [[5-levels-of-idea]]

## Mũ Nét (Money Knot)
**Translation:** Điểm tiêu tiền của user trong game
**Definition:** Vị trí thiết kế monetization point. Game "lãi ở đây" = mũ nét ngay D0/D1 (hyper); game "lãi ở đây mũ" = mũ nét sâu trong game (hybrid, dễ scale).
**See also:** [[fueling-pacing]], [[d7-vs-d3-breakeven]]

## Fueling
**Translation:** Pacing khai thác value
**Definition:** Tốc độ / phân bổ khai thác value từ user qua thời gian. Hyper ép D0/D1; Hybrid/ERP dàn trải D3-D7+. Khác với "fueling = battle simulation" mà một số bản phiên âm sai.
**See also:** [[fueling-pacing]]

## Imba (Balance)
**Translation:** Imbalance — mất cân bằng
**Definition:** Khi MTV (Material Target Value) user mua không khớp với Power yêu cầu tại checkpoint. Imba cao quá sớm = user vượt content; imba thấp = user trả tiền xong vẫn không qua được.
**See also:** [[imba-balance-meta]]

## Dark UX (Đắc UX)
**Translation:** Kỹ thuật UX có chủ đích lừa user
**Definition:** Trade-off tăng conversion với rủi ro retention. Bao gồm Click vs Hold, đảo X3, Arm Break, bán content khoá level. *"Chỉ dùng khi monetize lành mạnh đã tối ưu nhưng conversion vẫn thấp."*
**See also:** [[dark-ux-techniques]]

## Piggy Bank
**Translation:** Lợn tích tiền
**Definition:** Cơ chế hút máu — tiền user kiếm tự động vào "lợn", phải xem ad hoặc trả tiền để rút. Chu kỳ 9-15 phút khớp session 40-50 phút.
**See also:** [[piggy-bank-monetization]]

## Arm Break
**Translation:** Animation giải lao trước inter
**Definition:** Pattern Voodoo: animation 2 giây với icon cốc cà phê dạy user "= giải lao bình thường". Sau khi train, spam Inter với cùng icon → user tưởng arm break, không skip.
**See also:** [[dark-ux-techniques]]

## File Ý Đồ
**Translation:** Design intent document
**Definition:** 1 trong 2 file đầu vào của level design (file tiêu chí + file ý đồ → file output). Bao gồm lộ trình + cách triển khai. Tồn tại để designer không quên ý định giữa chừng.
**See also:** [[file-y-do-design-intent]]

## Pattern Habit Break
**Translation:** Phá thói quen người chơi
**Definition:** Kỹ thuật tạo độ khó: 3 level đầu tạo thói quen (pattern lặp lại) → 1 level phá (thay đổi 1 element nhỏ) → user chết 1 lần → đạt tỷ lệ replay đã set.
**See also:** [[pattern-habit-break]]

## Hidden Variable
**Translation:** Biến ẩn điều chỉnh khó
**Definition:** Các biến không hiển thị (freestyle ratio, drop rate, mix density) để tune khó sau IAP mà user không nhận ra.
**See also:** [[hidden-variable-difficulty]]

## Tắc Ẩn
**Translation:** RNG có chủ đích chặn level
**Definition:** Pattern Match-3: chặn level qua tỷ lệ chip drop + bố cục sinh chip, không qua moves/time/obstacle hiển nhiên. Là lever 5 trong 5 yếu tố tạo độ khó.
**See also:** [[match3-difficulty-levers]], [[chip-spawn-algorithm]]

## MVP (Minimum Value Product)
**Translation:** Bản nhỏ nhất có thể test thị trường
**Definition:** Bản đẩy ra thị trường thu data thật (đủ gameplay loop, vẫn là minimum, không full feature). Khác với Prototype (bản thử nghiệm nội bộ).
**See also:** [[prototype-vs-mvp]]

## Prototype
**Translation:** Bản thử nghiệm sơ khai
**Definition:** Bản test idea + truyền đạt ý đồ nội bộ. Sơ khai, biến số ít nhất. Không phải bản đẩy ra thị trường.
**See also:** [[prototype-vs-mvp]]

## CTR (Click-Through Rate)
**Translation:** Tỷ lệ click vào ad
**Definition:** Tỷ lệ user click vào ad / tổng impression. Cũng dùng làm metric đầu tiên đánh giá prototype có được chấp nhận không (chạy 10 user → CTR ~80% → idea OK).
**See also:** [[prototype-vs-mvp]], [[ecpm-blackbox]]

## Subscription Pack
**Translation:** Gói tự trừ tiền định kỳ
**Definition:** Phù hợp game content/view (nhạc, đọc, xem phim). Pay rate Amanote 1.3-3%. Khác với Battle Pass (mua 1 lần / 30 ngày, không auto-renew).
**See also:** [[subscription-pack-design]]

## Thumb Zone
**Translation:** Vùng ngón cái tầm tay
**Definition:** Vùng ngón cái user dễ với tới trên màn hình điện thoại. Nút quan trọng (đặc biệt IAP) phải nằm trong vùng này.
**See also:** [[thumb-zone-design]]

## Phá UI
**Translation:** Đập vỡ grid hút mắt
**Definition:** Cố tình thiết kế lệch grid để hút mắt vào element quan trọng (thường là IAP). Designer chấp nhận UI không cân đối nếu tăng click rate.
**See also:** [[thumb-zone-design]]

## S × T Grid
**Translation:** Lưới phân loại genre user
**Definition:** Lưới 2 chiều: S (sở thích — trục dọc) × T (tư chất — trục ngang). Ví dụ: S1T2 = casual repeat (Sudoku); S2T2-T4 = challenge cao tay (MOBA).
**See also:** [[s-t-genre-grid]], [[user-segmentation-3-axes]]

## T2 / T3 / T4
**Translation:** Tier tư chất user
**Definition:** T4 = siêu nhân (tìm counter optimal); T3 = support, profit, bang chủ; T2 = nhanh tay nhanh mắt, top spender. IAP strategy khác cho mỗi tier.
**See also:** [[user-segmentation-3-axes]]

## Cất Bằng Sai Đồng Tiền
**Translation:** Định giá IAP sai
**Definition:** Anti-pattern: bán gói $10 mở ra $300 worth journey → user đi dài quá, designer chưa kịp set next paywall.
**See also:** [[iap-pricing-user-value]]

## Buy7
**Translation:** % user mua IAP trong 7 ngày đầu
**Definition:** Metric IAP. Buy7 1.8% là cao bất thường (con bắn máy bay cao nhất 0.07%) nhưng có thể signal progress mất cân bằng — user mua nhiều tier thấp, không leo tier cao.
**See also:** [[iap-pricing-user-value]]

## D7 Hoà / D3 Hoà
**Translation:** Break-even ở ngày 7 / ngày 3
**Definition:** Tổng doanh thu = chi phí UA ở D7 hoặc D3. D7 dễ scale qua UA hơn (ROAS/GPA target xa cho phép pool user lớn).
**See also:** [[d7-vs-d3-breakeven]]

## Balance Scale
**Translation:** Sơ đồ phân tỷ trọng module
**Definition:** Bảng phân % giữa các module (core, phụ bản, PvP, sự kiện). Tổng phải 100%. Thêm module mới phải bớt từ module khác.
**See also:** [[balance-scale]]

## Organic Rate
**Translation:** Tỷ lệ user tải về tự nhiên
**Definition:** % user install không qua marketing. Vũ note là thuật toán Google, designer không kiểm soát. Organic cao không suy ra tập user trẻ — phải tách tỷ lệ vs số tuyệt đối, trend tạm thời vs ổn định.
**See also:** [[organic-rate-interpretation]]

## Auto-Equip
**Translation:** Tự động lắp trang bị
**Definition:** Pattern UX phù hợp game 1 hero (Loại 1) hoặc 10+ hero (Loại 3), không phù hợp 1-5 hero không có fun role (Loại 2b) vì hero tranh đồ lẫn nhau.
**See also:** [[auto-equip-design]]

## Fun Role
**Translation:** Class cố định cho hero
**Definition:** Khi mỗi hero có class riêng (kiếm/cung/giáo), pool đồ phân tách → không tranh đồ. Quyết định auto-equip có phù hợp hay không.
**See also:** [[auto-equip-design]]

## Yêu Ích
**Translation:** UX (User Experience) theo cách dịch của Vũ
**Definition:** Tối ưu hoá trải nghiệm người dùng × tối đa hoá lợi ích nhà sản xuất. Định nghĩa từ sách của nhà thiết kế đồ gia dụng Pháp, được nhận là nguồn inspire cho thiết kế chính Apple. Khác UX academic — game studio version có dual-goal đi cặp monetization.
**See also:** [[ux-yeu-ich-definition]]

## Hành Vi vs Lời Nói
**Translation:** Behavior vs Stated Preference
**Definition:** User nói A, làm B → designer phải design cho B. Lời nói rẻ và không tin cậy; hành vi đắt nhưng đáng tin (analytics, playtest, A/B test). Cảm xúc ≠ sự thật.
**See also:** [[behavior-vs-stated-preference]]

## Big Numbers
**Translation:** Cảm xúc số to
**Definition:** Cùng tỷ lệ purchasing power, số to (100 gold) cảm xúc hơn số nhỏ (1 gold). Currency scale chọn từ đầu — không downscale được sau.
**See also:** [[value-perception-techniques]]

## Anchor Effect (Gift-on-Package)
**Translation:** Hiệu ứng neo, tặng trên total package
**Definition:** "Tặng X trên tổng gói Y" (Y > X) khiến user cảm thấy deal — phát sinh nhu cầu mua. "Tặng X" thuần không có anchor → user không thấy giá trị. Anti-pattern: starter pack không hiển thị giá gốc gạch ngang.
**See also:** [[value-perception-techniques]], [[first-iap-strategy]]

## Inherited Habit
**Translation:** Thói quen kế thừa
**Definition:** Icon/pattern user đã quen từ game khác (home, hotel, settings, play). Reinvent = friction. Default: dùng convention sẵn có.
**See also:** [[inherited-habit-conventions]]

## 3 Giảm Thiểu (3 Reductions)
**Translation:** 3 nguyên tắc minimization UI/UX
**Definition:** (1) Giảm số bước, (2) Giảm lượng thông tin, (3) Giảm lượng quyết định. Doc 6 P2 introduce, Doc 7 expand với case study cụ thể.
**See also:** [[ux-3-criteria]]

## Multi-Start
**Translation:** Đa khởi đầu
**Definition:** Pattern onboarding cho user chọn role/class đầu game ảnh hưởng gameplay. 3 use cases (mạnh đầu/yếu đầu/phụ trợ), 3 risks (non-linear, balance mess, no restart path). Khác Customize Start (cosmetic only).
**See also:** [[multi-start-design]]

## Material Count
**Translation:** Số loại tài nguyên upgrade
**Definition:** 2 loại = habit-driven, 4+ loại = decision paralysis. Game design hay sai phía "phong phú" → kill habit. Default 2 cho casual/mid-core.
**See also:** [[material-count-decision-paralysis]]

## Skin Bridging
**Translation:** Skill set overlap để bắc cầu so sánh
**Definition:** Pattern ABC/BCD/ACD cho phép user so sánh card qua skill chung. Disjoint (ABC vs DEF) không có cơ sở compare. A+ (same skill, stat khác) tối ưu nhất.
**See also:** [[skin-bridging-comparison]]

## Slot-Locked Upgrade
**Translation:** Level gắn slot không gắn con
**Definition:** Equipment upgrade gắn slot (helmet, armor) thay vì cái áo cụ thể. User swap áo giữ level → no penalty, habit-friendly.
**See also:** [[slot-locked-upgrade]]

## Heart System
**Translation:** Hệ thống tim / mạng / lives
**Definition:** Bottleneck cho số phiên chơi. Có tim → tăng session/day + monetize gate. Không tim → gameplay phải gây nghiện. Ad-for-heart > paywall money cho ad-funded game.
**See also:** [[heart-system-design]]

## Cào Bằng (Cast Time)
**Translation:** Equal cast time across units
**Definition:** Approach: tất cả unit dùng C1 cast time. Code đơn giản, balance accurate (DPS = damage/time pure). Đối lập Per Con (riêng từng unit, balance theory ≠ thực tế).
**See also:** [[cast-time-cao-bang-vs-per-con]]

## Hit Reaction
**Translation:** Anim phản ứng khi bị tấn công
**Definition:** Ngửa người ~0.4s. Bài toán dồn: attacker hit liên tiếp khi defender chưa recover. 3 cách xử lý: Kệ Mẹ (brawler), Block Time (song đấu), Anim Kêu Lại (chiến thuật).
**See also:** [[hit-reaction-3-approaches]]

## Form Base
**Translation:** Tỷ lệ thân thể chuẩn cho production line
**Definition:** Vẽ 1 con kỹ (10 điểm) → fix tỷ lệ chân tay → các con sau đổi outfit/đầu giữ form. 3 form recommended: trung bình / béo / gầy.
**See also:** [[form-base-art-template]]

## Mép Mép Affordance
**Translation:** Visual cue cho vuốt qua layout
**Definition:** Grid 5×6 + row mép phía dưới (30-40% chiều cao) → user reflex vuốt. Hide affordance trong layout, không qua text/arrow.
**See also:** [[mep-mep-affordance]]

## Bull Start Dự Án Phải Bảo Vệ
**Translation:** Document reasoning trước khi pitch
**Definition:** GD phải có khuôn lý do cho mọi feature decision. UA/sếp/code hỏi "tại sao?" → GD trả lời được = pass; không trả lời = fail communication. Fail test mà không có reasoning = không iterate.
**See also:** [[defending-design-decisions]]
