---
title: "GD Doc 6 Part 1 — UI: Wireframe, Button States, Flow Rules & 5-Color UI Brief (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 6 Part 1 - UI.mp4"
date_added: 2026-05-19
date_updated: 2026-05-19
tags: [video, course-transcript, game-design, ui, wireframe, button-states, equip-flow, color-coding, vietnamese]
aliases: ["GD Doc 6 Part 1", "Buổi 6 Phần 1 UI", "UI Wireframe Vũ"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-05-part-1-art]]"
  - "[[negaxy-iec-gd-doc-06-part-2-ux]]"
  - "[[negaxy-iec-gd-doc-07-ui-ux-monetize]]"
summary: "Buổi 6 Part 1 (Vũ + Cường + Minh + Đức + Hiệp + học viên): cách GD làm UI brief — 3 bước (xác định cách làm Core vs Flow, vẽ draft, đắp case), 3 level nút (Key/Blue/Hidden), 3 nảy sinh khi bấm (Popup/State/Luồng lên đới), Lucky Spin 4 trạng thái case, rule UI tối đa 2 tầng, equip vũ khí workflow chi tiết, 5 màu code (đỏ/cam/vàng/xanh-lá/xanh-dương), phá UI tactic, icon vs text decision (Tiny Battle +1 slot case). Insight: vẽ 2-3 draft mới so sánh được."
---

# GD Doc 6 Part 1 — UI: Wireframe, Button States & Brief

**Speakers:**
- **Vũ** — Lecturer chính. Reference IEC, 2Cơ Game, Tiny Battle/Tiny Kingdom.
- **Cường** — Học viên có background thiết kế web UI/UX, làm theo con game gốc.
- **Minh** — Học viên từng làm dự án freelance/hybrid VN-quốc tế, share workflow Manny Noel / Soft Cache.
- **Đức** — Học viên có game thẻ bài, cùng demo từ Doc 5.
- **Hiệp** — Reference con NegaMod làm material UI tốt.
- **Giang** — Lurker session này.

**Format:** Buổi học trao đổi, ~110 phút, tiếng Việt. Phần 1 của Doc 6 — chỉ về **UI**, KHÔNG đụng UX (sẽ ở Part 2). Vũ chủ động tách hai để không trộn.

Tiếp nối Doc 5 Part 2 (Animation) và đặt nền cho Doc 6 Part 2 (UX), Doc 7 (UI/UX & Monetize).

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 6 Part 1 - UI.mp4` (1.4 GB, ~110 phút) + `GD Doc 6 Part 1 - UI.mp4.txt` (2,425 dòng, faster-whisper large-v3 chunked qua `doc6_ui_chunks/` — 11 chunks 10-phút + 2 chunks tách 5-phút cho phần OOM).

---

## Wireframe Workflow — Từ Cường

Cường (background web UI/UX) chia sẻ flow của bạn ấy:

1. Chọn **tỷ lệ màn hình** (18:9, dùng preset iPhone 14 Pro Max trong XD/Figma).
2. Bật **lưới căn** (Photoshop-like grid) — cân lưới 2 phía.
3. Vẽ **bố cục chính** dọc:
   - HUD top: setting, currency (góc trái-phải).
   - Nút tương tác chính ở **1/3 dưới** — thumb zone.
4. **Data setup**: file Excel song song cho từng tính năng, không thay đổi quá 7-30 ngày.

Vũ note: cách này phù hợp khi làm theo con game gốc (đã có template). Khi làm game mới, flow phải khác.

---

## Workflow Pro Của Minh — Manny Noel / Hybrid

Minh share workflow khi làm với team quốc tế:

1. **Flowchart toàn bộ trường hợp** — màn inventory: có item / full / thiếu tiền / no internet → all branches.
2. **Sketch màn gameplay + home trước** — 2 màn quan trọng nhất → ấn tượng đầu + xuyên suốt.
3. **Mood board + color palette** — đồng bộ UI / VFX / gameplay.
4. **Wireframe vuông tròn tam giác** — yes/no decision tree before pixel polish.
5. **Detail từng màn** — break down từng feature (popup offer, home, gameplay, gameboard).
6. **Estimate theo breakdown** — 2D, 3D, VFX, environment estimate riêng.

Vũ comment: bộ tài liệu Minh nói là chuẩn freelance / agency quốc tế. Việt Nam thường không cần phức tạp đến mức đó — Vũ sẽ adapt sao cho phù hợp VN volume.

---

## 3 Bước Làm UI Cho VN Studio

Vũ chốt simplified flow:

### Bước 1 — Xác Định Cách Làm

2 approach:

- **Đi Từ Core Đi Ra** — tính năng (weapon, inventory) → từng nút → từng case. Cho phép flow **nhiều tầng**, mở rộng được.
- **Đi Từ Flow Đi Vào** — flow user → màn hình → button. Giới hạn ở flow user, không xử lý được case lồng nhau sâu.

### Bước 2 — Triển Khai

- Vẽ **draft đầu tiên** (vuông tròn tam giác).
- Đắp **case** vào draft.
- **Vòng lại** để hoàn thiện draft + bổ sung case mới phát hiện.
- Lặp đến khi draft cho ra cái UI hợp lý.

### Bước 3 — Làm UI Thật

- Sau khi draft hoàn thiện → mới dàn vị trí nút.
- Phân **levels of priority**:
  - Nút key (must) → vị trí thumb zone.
  - Nút blue (optional) → vị trí ít quan trọng.
  - Nút not-decisive → giấu trong tab.

---

## 3 Level Nút Trong UI

Vũ phân loại để bố trí UI:

| Level | Tên | Đặc điểm | Vị trí gợi ý |
|-------|-----|----------|--------------|
| 1 | **Key (Gameplay)** | Không có thì không chơi được | Thanh dưới, 2 lề trái-phải, thumb zone |
| 2 | **Blue (Optional)** | Có thì chơi tốt hơn, không có vẫn được. VD: achievement, event, lucky spin | Vị trí ít quan trọng, side panel |
| 3 | **Hidden (Không Quyết Định)** | Không cần thiết. Có thể giấu / cất vào tab khác | Trong setting menu / collapsed tab |

> *"Cái nào quan trọng thì mình để ra ngoài. Cái nào không quan trọng mình có thể 2 bớt nó đi."*

Tùy game: có game event là **Key** (event-driven monetization), có game event chỉ là **Blue** (event optional).

---

## 3 Nảy Sinh Khi Bấm Nút

Mỗi nút có thể trigger:

### 1. Pop Up

Báo cứng (cannot dismiss to other flow):
- Thông báo kết quả level 20.
- Bấm Close / Tham gia sau → tắt thôi.
- Đây là **luồng cứng** — không phát sinh flow khác.

### 2. State Của Button

State của chính nút đó:
- Active / Inactive (xám).
- Locked (level chưa đủ).
- Loading (đang fetch art).
- Loading fail (text báo).
- Watch ad (icon video).
- Count-down (sau khi xem ad, đợi 30s mới xem tiếp).

### 3. Luồng Lên Đới (Flow-Up)

Nút sinh flow phụ:
- Bấm mua → thiếu tiền → popup mua vàng → store → flow IAP.
- Bấm equip → flow chọn vũ khí → flow chọn nhân vật.

> *"Tại sao mình tách popup này và popup này nó ra khác nhau? Cái luồng này là luồng cứng — mình không thể làm gì khác được. Còn thế này là nó có một luồng lên đới phụ xảy ra theo trường hợp đấy."*

---

## Case Study: Lucky Spin — 4 Trạng Thái

Vũ test bằng Lucky Spin (logic: 1 lần free / 1 tiếng + 1 lần watch ad cộng dụng):

| State # | Icon | Màu | Trigger |
|---------|------|-----|---------|
| 1 | "Lucky Spin" text + icon | Vàng | Sẵn sàng quay free |
| 2 | "Turn back after X min" count-down | Xám | Đang cooldown |
| 3 | "Spin" + icon video | Xanh | Sau khi dùng free, xem ad để quay tiếp |
| 4 | "Level 20" + khóa | Xám-locked | Chưa đủ level |

> *"Đề nghị các bạn vẽ như sau: nút này ở đây trạng thái 1, 2, 3, 4. Làm 1 thích nút ở bên cạnh: 1 là gì, 2 là gì, 3 là gì. Trường hợp nào từ 1 sang 2 hay 2 sang 3. File này thì sẽ là art và code dùng chung."*

State table = **single source of truth** cho cả art + code. Liệt kê transition rules ngay trong file UI.

---

## Rule UI Cốt Lõi: Tối Đa 2 Tầng

> *"Tuyệt đối không đưa cái này sang cái 1.1.1 cái gì nữa. Tức là nút nó chỉ có đến 2 tầng thôi."*

### Ví Dụ Setting

- ✅ **Đúng**: Setting → Music slider, Language flag, Connect Facebook button (cùng 1 màn).
- ❌ **Sai**: Setting → Music → Stereo / Background music / SFX (3 tầng).

### Ví Dụ Language

- ✅ **Đúng**: Language → list cờ Anh / Pháp / Mỹ — chọn vuốt.
- ❌ **Sai**: Language → dropdown chỏ xuống → list (web pattern, không phù hợp mobile game).

### Lý Do

Mỗi tầng thêm → flow UX rắc rối. Mọi cờ phải nằm 1 màn, không drill down 3 lần.

> *"Nếu không game của các bạn các luồng flow mà lúc sau phần UX sẽ cực kỳ rắc rối."*

---

## Case Equip Vũ Khí — Bài Toán Khó Nhất

Vũ dạy qua case study chi tiết: equip vũ khí cho nhân vật.

### Approach A: Từ Nhân Vật

- User bấm con nhân vật → inventory vũ khí available hiện ra (popup 2/3 màn hình).
- Bấm vũ khí → equip ngay (1 action).
- Lợi: user "chọn con nào dùng vũ khí gì hợp" — quyết định driven by hero.

### Approach B: Từ Vũ Khí

- User bấm vũ khí → popup info → equip → chọn nhân vật từ list hero.
- Lợi: user nhìn tổng quan **tất cả vũ khí** trước → biết rare hierarchy, biết owner.

### So Sánh Bước

| Tình huống | Approach A | Approach B |
|------------|-----------|------------|
| Equip lần đầu | 3 bước | 3 bước |
| Switch giữa nhiều con nhanh | Nhiều bước (mỗi con select riêng) | Ít hơn (chỉ bấm hero icon) |
| Upgrade vũ khí | Vào info ngược | Trực tiếp từ inventory |
| Biết owner hiện tại của vũ khí | Phải dò | Hiện icon owner ngay |

Vũ key insight:

> *"Phải có 2 phương án mới so sánh được. Yêu thì yêu 2-3 cô — yêu mỗi 1 đứa rồi bảo là tốt nhất trần đời xem chừng nó bốc phép."*

GD phải vẽ **multiple drafts** rồi compare bằng số bước / dễ hiểu, không thể từ 1 phương án đã đưa "best."

### Improvement: Icon Owner

Hiển thị icon owner trên vũ khí trong inventory:
- Icon màu vàng = đang cầm bởi tướng legendary.
- Icon màu xanh = đang cầm bởi tướng rare.
- Vũ khí không có icon = available.

User nhìn ngay biết phải tháo của ai để equip cho người mới.

---

## Material & Stat UI — NegaMod Reference

Vũ chỉ ra anti-pattern của Đức và pattern tốt của NegaMod (Hiệp):

### Anti-Pattern

- Để material to bằng HP/Attack/Defense → nhìn tổng quan rối.
- Material để dưới attack → user không biết "level-up cần bao nhiêu material."

### Pattern Tốt (NegaMod)

- Material list ở **góc top-right**, nhỏ gọn.
- Trên nút "Level Up" ghi rõ **cost** (X gà + Y thịt) ngay trong button label.
- HP/Attack/Defense - kích thước vừa phải.

### Slot Locked UI

Nếu slot bị khóa (chưa đủ level / chưa epic) → phải có text giải thích:
- "Epic trở lên mới được cầm."
- "Level 50 mới được mở slot này."

❌ Anti-pattern: chỉ 1 cục tối thui không text → user không biết tại sao locked.

---

## Hiển Thị Inventory — 3 Strategies

Khi mở inventory vũ khí, hiển thị thế nào?

1. **Hiện tất cả** (kể cả đang được cầm bởi con khác) — user nhìn tổng quan rare hierarchy, biết owner.
2. **Chỉ phù hợp slot** — kiếm thì không hiện cung. User không cần lọc.
3. **Chỉ available (exclude cầm)** — user thấy luôn vũ khí free, không cần móc của con khác.

Vũ recommend #1 cho game tướng meta:

> *"Hiện tất cả những con đang còn, đang có, kể cả con khác. Thằng này có thể nhìn tổng quan tất cả vũ khí — bạn có thể thấy biết được cái nào đa hơn cái nào luôn mà không cần phải so sánh."*

#1 + icon owner = user có **toàn bộ thông tin** trong 1 cái nhìn → quyết định nhanh.

---

## Clash Royale Innovation — Tăng % Per Level

Vũ giải thích vì sao Clash Royale thay đổi pattern stat:

### Trước Clash Royale

- HP per level: con A level 7 có HP 1450, con A level 8 có HP 1620.
- Designer phải define từng level → table phức tạp.
- User phải **nhớ stat absolute** để so sánh giữa các level.

### Sau Clash Royale

- Base stat × (1 + 10% × level).
- Con nào tốt từ đầu = tốt mãi mãi.
- User chỉ cần **nhớ base stat** + level.

Bài học UI: simplification logic → simplification stat display → UI gọn hơn (chỉ cần show base stat + level multiplier).

---

## File UI Brief — 5 Màu Code

Vũ chốt convention 5 màu cho file UI brief (art + code đều đọc):

| Màu | Ý nghĩa | Ví dụ |
|-----|---------|-------|
| 🔴 **Đỏ** | Phải chú ý cao, làm đẹp nhất | Pop-up starter pack, event banner, IAP shop |
| 🟠 **Cam** | Liên quan monetize | Nút xem reward ad |
| 🟡 **Vàng** | Tính năng core, user phải đọc/hiểu | Battle button, gameplay HUD |
| 🟢 **Xanh Lá** | User bớt focus | Setting, refund button (cần có nhưng mờ đi) |
| 🔵 **Xanh Dương** | Gây nhuận lận (rare) | Icon video màu đỏ giả YouTube, asymmetric button size |

### Document Color Convention

Tương tự cho document text:
- **Đen** = sẽ làm bản này, hoặc đã làm bản cũ.
- **Đỏ** = update làm bản tới.
- **Xanh lá** = ghi chú lung tung, đừng đọc vào (ghi cho bản sau).

GD viết note tương lai ngay trong doc chung → màu xanh lá → người khác auto skip.

---

## Phá UI Tactic — Đặt Sự Bất Đồng Có Chủ Ý

Pattern thông thường: các nút trong dãy bằng nhau. **Phá** pattern bằng cách:

- 1 nút event nhảy lên to hơn 30% → có effect glow.
- Trong dãy text-only → 1 nút có icon → nổi bật.
- Free button + Ad button cùng size = bằng nhau → ad to hơn = nguy hiểm. Yêu cầu:
  - Icon ad **nhỏ** + để **góc** + màu **mờ** đi.
  - Tăng size text "Free" và cân giữa.

### Anti-Pattern: Icon Ad Màu Đỏ Giả YouTube

> *"Các bạn art rất thích vẽ icon video màu đỏ giống YouTube. Tóm lại là cái icon màu đỏ nó sẽ rất là sợ — nguy hiểm."*

User reflex: thấy đỏ giống YouTube → tab ra → drop ad rate. GD phải explicitly require small + side + mờ.

---

## Typography — GD Chỉ Mô Tả Style

Vũ admit typography không phải thế mạnh của GD:

- GD chỉ mô tả: "game sci-fi → typo có nét nhọn sắc."
- Designer art chọn font cụ thể.
- Diện tích text trong nút thường nhỏ (vì icon chiếm chính) → không cần fancy font.

---

## Icon vs Text — Decision Framework

Có nên thêm text dưới icon?

### Pattern Test: User Hiểu Không?

- User test nhìn icon → hiểu → **không cần text**.
- User test "không hiểu" → **cần text**.

GD không được tự giải thích cho user test → user sẽ "hiểu mất" → lần sau không hỏi → kết quả bias.

### Case Tutorial vs Long-Term

Workflow đa cấp:
- **D0-D7** (tutorial era): text + icon.
- **D7+** (đã quen): chuyển sang icon-only → giảm clutter, tăng diện tích cho stat.

Yêu cầu thiết kế 2 versions UI.

### Case Tiny Battle "+1 Slot"

Anti-pattern: icon "dấu cộng + cờ" không có text → user không hiểu là gì → click rate thấp.

Fix: thêm text "+1 slot" → click rate **tăng nhiều**.

> *"Đối với những cái nào mà nó khó hiểu thì gọi nên sự tài thiện. Còn các game khác — tính năng phổ thông của nhiều con game rồi — thì không cần đặc biệt."*

### Remove Ad — Bắt Buộc Text

- "Remove Ad" 2 chữ → ngắn nhất rồi, không thu được nữa.
- Đặt nguyên text ở nút (không chỉ icon).
- Trigger: sau inter-ad → offer remove ad popup.

### Text Length Limit Cho Nút

- 5-7 ký tự max: Home, Battle, Weapon, Item, Shop.
- Bỏ số "1", bỏ chữ "Esc" → "Slot" thay vì "1 Slot."
- Để text to nhất có thể trong diện tích nút.

---

## Đừng Giải Thích Khi User Test

Vũ chốt nguyên tắc test user:

> *"Tất cả câu hỏi mà các bạn nhận được — game này là gì, nút này là gì — chỉ quy lại một vấn đề thôi: user nó không hiểu. Các bạn đi giải thích thì người ta hiểu mất rồi còn đâu — lần sau người ta hỏi làm sao được nữa."*

- Test user feedback "không hiểu" = signal phải redesign.
- GD giải thích = invalidate test data.
- User hỏi tức là **GD đã fail communication** qua icon/text/visual.

---

## Recommended Reference Games

Để học UI patterns nhiều phong cách:

- **Supercell** (Clash Royale, Clash of Clans, Brawl Stars) — icon trained over many games.
- **Blizzard** (Warcraft Rumble, Hearthstone) — mỗi game đặc thù khác nhau.

Tránh chỉ chơi **các game của Kinh** — UI giống nhau, ít variation → không học được gì mới.

---

## Anti-Pattern Tổng Hợp

- **Chỉ 1 phương án** rồi bảo "tốt nhất" — phải có 2-3 drafts để compare.
- **3+ tầng menu** (setting → music → background music) — vi phạm rule 2 tầng.
- **Icon ad màu đỏ giống YouTube** — user reflex tab ra.
- **Material to bằng HP/Attack** — nhìn rối, không biết level-up cost.
- **Locked slot không text** — user không biết tại sao locked.
- **Vũ khí "đang được cầm" không icon owner** — user phải dò.
- **Equipment text vô hồn** — không biết ai đang cầm.
- **Giải thích cho user khi test** — invalidate feedback.
- **Stat tăng absolute per level** (HP per level) — user khó nhớ.
- **Nút text-only quá dài** (>7 ký tự) — không đọc kịp / nhỏ quá.
- **Dropdown language** trên mobile game — pattern web, không phù hợp.

---

## Thuật Ngữ Buổi Này

### UI Workflow
- **Draft** — wireframe vuông tròn tam giác, chưa có art polish.
- **Core Approach** — đi từ tính năng → button → case. Cho phép flow nhiều tầng.
- **Flow Approach** — đi từ user flow → màn → button. Đơn giản hơn nhưng giới hạn.
- **Case Đắp Vào Draft** — pop-up, state, luồng lên đới — phải list trước khi vẽ pixel.

### Button States
- **Active** — sẵn sàng tương tác.
- **Cooldown** — count-down state, kèm timer.
- **Locked** — chưa đủ điều kiện, kèm text giải thích.
- **Loading** — đang fetch, icon spin.
- **Watch Ad** — sau khi hết free, icon video.

### Flow Types
- **Luồng Cứng** — popup không sinh flow phụ.
- **Luồng Lên Đới** — popup sinh flow phụ (thiếu tiền → store).

### UI Hierarchy
- **Key Button** — không có thì không chơi được. Đặt thumb zone.
- **Blue Button** — optional, achievements, event.
- **Hidden Button** — cất trong tab/menu, không quyết định gameplay.

### Equip Workflow
- **Equip Từ Hero** — bấm hero → chọn vũ khí.
- **Equip Từ Weapon** — bấm vũ khí → chọn hero.
- **Icon Owner** — visual indicator vũ khí đang được ai cầm.

### File UI Brief
- **5-Color Convention** — đỏ/cam/vàng/xanh-lá/xanh-dương cho priority level.
- **Phá UI** — chủ ý làm 1 element khác pattern để nổi bật.

### Text vs Icon
- **Icon-Only** — sau khi user quen, D7+.
- **Icon + Text** — D0-D7 tutorial era.
- **Text Cap** — 5-7 ký tự max trong nút.
- **Locked Text** — "Level 50 mới mở," không chỉ icon khóa.

### Stat Display
- **% Per Level** (Clash Royale style) — tăng theo phần trăm, user dễ nhớ.
- **Absolute Per Level** (legacy) — stat fix per level, user khó nhớ.

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Video gốc: `GD Doc 6 Part 1 - UI.mp4` (1.4 GB, ~110 phút).
- Transcript đầy đủ: `GD Doc 6 Part 1 - UI.mp4.txt` (2,425 dòng, faster-whisper large-v3 chunked 11×10-phút qua `doc6_ui_chunks/`, 2 chunks 5,6 tách lại thành 5-phút sub-chunks sau OOM).
- Khoá học: Game Design Course by Negaxy + IEC (8 buổi, đang ingest dần).
- Vị trí trong khoá: **Buổi 6 Phần 1 — UI** (nằm sau Doc 5 Part 2 Animation; đặt nền cho Doc 6 Part 2 UX, Doc 7 UI/UX & Monetize).
- Date updated 2026-05-19: compile lần đầu sau khi chunked transcription hoàn thành (gồm sub-chunk retry).
