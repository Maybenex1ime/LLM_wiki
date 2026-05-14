---
title: "GD Doc 7 — UI/UX & Monetize Design (Khóa Game Design Negaxy + IEC)"
source: "raw/videos/Game Design Course by Negaxy + IEC/GD Doc 7.m4a"
date_added: 2026-05-14
tags: [video, course-transcript, game-design, ui, ux, monetization, iap, ads, dark-ux, mobile-games, vietnamese]
aliases: ["GD Doc 7", "Buổi 7 UI UX Monetize", "UI UX Monetize Design Vũ"]
status: draft
related:
  - "[[negaxy-iec-gd-doc-02-level-design]]"
  - "[[negaxy-iec-gd-doc-04-level-data-and-iap]]"
summary: "Buổi 7 (Vũ + học viên): 3 tiêu chí UX (số bước thao tác, thông tin, quản trị sự chú ý) qua case study equipment system của Hiệp và hero info của Đồng; 2 trường phái IAP (First-IAP vs giữ giá trị); subscription pack cho game nhạc; Piggy Bank và 5 dạng Dark UX để boost conversion."
---

# GD Doc 7 — UI/UX & Monetize Design

**Speakers:**
- **Vũ** — Lecturer chính (xưng "anh"/"mình", người dẫn buổi).
- **Hiệp** — Học viên/co-lecturer có dự án game tower-base với hero + equipment, được mời lên bóc case option 1.
- **Tài** — Học viên đề xuất phương án auto-equip làm option 3.
- **Đức** — Học viên phản biện về auto-equip và chia sẻ case Dark UX "Arm Break" của Voodoo. Từng làm publisher VNG (One Punch Man The Strongest).
- **Đồng** — Học viên với game RPG turn-based ("Darwin"), case study chính cho tiêu chí thông tin và quản trị noti.
- **Giang** — Học viên có dự án thực tế, đặt câu hỏi về subscription pack (Amanote) và core game evolution.
- Một số học viên khác (Tùng, người dự thính).

**Format:** ~150 phút, tiếng Việt. Tiếp nối Doc 6 (UI). Doc 6 ghi âm thành 2 file video (`GD Doc 6 Part 1 - UI.mp4` + `GD Doc 6 Part 2 - UX.mp4`) — Doc 7 này là audio session liền sau, deep-dive 3 tiêu chí UX + monetize design.

**Source file:** `raw/videos/Game Design Course by Negaxy + IEC/GD Doc 7.m4a` (audio gốc) → `GD Doc 7.m4a.txt` (transcript thô) → `GD Doc 7.m4a.cleaned.txt` (1032 dòng cleaned, đã sửa ASR errors "Y/Y wick" → "UI/UX").

---

## Tiếp Nối Doc 6 — Phân Biệt UI vs UX

Vũ tóm tắt: bữa trước đã nói về UI và UX theo định nghĩa riêng.

- **UI** không nói về cảm xúc. UI chỉ nói "làm được hay không làm được". Khi làm UI thì làm flow, pace, và các thứ khác. Sau khi làm nhiều vòng, mới đưa ra UI — các phần bên trong, các trạng thái, các trường hợp có thể xảy ra. UI này code và deck đều dùng.
- **UX** là cái trải nghiệm để tối giảm hóa công sức bỏ ra, tối giảm hóa phần nhận về, tối giảm hóa phần xuất. Hành trình trải nghiệm có rất nhiều yếu tố — bữa trước mới chỉ nói yếu tố core của sản phẩm, làm cho user cảm giác sướng.

Vũ note: bữa trước Hiệp đưa ra ví dụ về UX game của bạn ấy, Vũ không trả lời option nào tốt hơn. *"Bây giờ tới lúc mình sẽ tìm ra các tiêu chí để đánh giá xem option nào sẽ là option tốt hơn, dựa trên cái phương làm UX."*

3 tiêu chí UX đã chốt ở Doc 6 (hôm nay deep-dive từng tiêu chí):
1. **Số bước thao tác** (số lần user phải bấm/tương tác).
2. **Thông tin** (số lượng + cách hiển thị + dung dạng).
3. **Quản trị sự chú ý / Giảm thiểu quyết định** (notification, attention management).

---

## Tiêu Chí UX 1 — Số Bước Thao Tác (Case Study Equipment Hiệp)

### Option 1 — Đi Từ Hero, Đếm 6 Bước

Vũ hỏi Hiệp: để user thay được 1 vũ khí (lấy từ hero khác lắp vào con của mình) thì mất bao nhiêu bước thao tác? Mặc định đếm từ màn hero info, bỏ bước bấm vào nút mở màn.

Hiệp ban đầu trả lời "3 bước" (chọn hero → chọn weapon → confirm). Vũ bóc tách kỹ hơn — phát hiện Hiệp **quên 1 nút Swap** quan trọng:

> *"Em quên cái nút này, nhưng nó là nút thay đổi, đổi vũ khí khác. Không được quên nha — sản phẩm của mình làm không được quên. Bây giờ hỏi giám đốc 'anh ơi tháng này doanh thu bao nhiêu' mà bảo 'ơ quên rồi' thì hơi khoai đấy."*

Sau khi liệt kê đầy đủ, tổng số bước user mất:

| Bước | Action | Note |
|------|--------|------|
| 1 | Chọn hero | 1.1 nếu hero đích ở vị trí đại diện → bỏ qua; 1.2 nếu hero ở danh sách dưới → swipe up |
| 2 | Click vào slot weapon | — |
| (cond) | Slot có weapon hay không | Có 2 nhánh, không tính là bước |
| 3 | Pop info — show weapon đang đeo | — |
| 4 | Nút Swap | Bước Vũ phải nhắc Hiệp thêm vào |
| 5 | Storage hiện ra — user đọc, chọn | Có "thinking time" giữa các bước |
| 6 | Equip + Confirm | — |

Vũ loại bỏ những bước không chắc chắn (như Swap, các trường hợp đã có sẵn) khỏi total để dễ so sánh.

### Option 2 — Đi Từ Weapon (3 Bước)

Vũ chốt một nguyên lý lớn trước khi đi tiếp:

> *"Khi mà các bạn đã tìm được 1 phương án, các bạn sẽ phích luôn lên phương án tốt nhất và không bao giờ nghĩ khác được phương án thứ 2. Thậm chí khi những người khác nói phương án thứ 2 các bạn sẽ vết ngay lại với người ta, bảo 'như thế này không đúng', nhưng vấn đề là các bạn chưa từng phân tích nó để xem nó có vấn đề gì hay không."*

Option 2: bắt đầu từ weapon thay vì hero. Pop-up list hero nằm phía trên weapon info, chọn hero và confirm.

```
Chọn weapon → 1
(weapon info hiện trên cùng) → 1.5
Chọn hero từ list → 2
Confirm (chỉ khi hero đang cầm vũ khí cũ — trường hợp thay) → 3
```

Kết quả: **3 bước** thay vì 6. Quy tắc Vũ chốt:

> *"Anh muốn từ nay không phải chỉ vụ này, mà tất cả những kinh doanh khác, em sẽ làm cái việc là em tách mình ra 2-3 option, sau đó các option đi bắt lẫn nhau và chọn ra một cái tốt nhất. Em không có vấn đề đúng hay sai."*

### Option 3 — Auto-Equip (Tài Đề Xuất)

Tài đề xuất: tự động equip dựa trên combat power. Click 1 con là auto-lắp toàn bộ trang bị tốt nhất. 2 bước — chọn con + đeo.

Vũ "bẻ" để cả lớp thấy điểm yếu:

- Nếu auto-equip lấy đồ tốt nhất ráp vào con đang bấm → mỗi lần bấm con khác, bộ đồ "xịn số 1" lại bay sang con đó. Cuối cùng chỉ có 1 con luôn được bộ xịn nhất.
- Nếu auto-equip *"lấy đồ tốt nhất đang chưa mặc cho ai cả"* → con thứ nhất bộ xịn 1, con thứ 2 bộ xịn 2 — vẫn được, nhưng khi user muốn *"chia niệm sức mạnh"* (con này áo xịn, con này kiếm xịn) thì thay rất khó.

### 3 Loại Game Phân Theo Số Hero — Auto-Equip Phù Hợp Khi Nào

Đức phản biện: *"Em chẳng thấy thốn, em thấy rất tiện. Khi em có một cái bun đến mười mấy con tướng, em không thể nào ngồi mặc từng quát một."* Đức cho ví dụ **One Punch Man The Strongest của VNG** — game thẻ bài, mỗi con 6 trang bị, auto-equip cứ lấy từ trang bị mạnh nhất ra mặc vào.

Vũ chốt 3 loại game theo số hero:

| Loại | Số hero | Auto-equip phù hợp? |
|------|---------|---------------------|
| **Loại 1** | 1 con (Nyachero, Survival) | Rất tốt. *"Nhà có 1 đứa con, tất cả tinh túy nhất là dành cho nó."* |
| **Loại 2a** | 1-5 con + có fun role (kiếm/cung/giáo cố định) | OK. Mỗi con dùng class riêng, không tranh nhau. |
| **Loại 2b** | 1-5 con + KHÔNG fun role (mặc lẫn — game của Hiệp) | Không OK. Bắt đầu tranh. Phải phân bổ tay. |
| **Loại 3** | Mười mấy con (Lít-tờ-bíc GD) | Bắt buộc auto. *"Thời gian chơi gameplay không còn — chỉ mặc quần áo, nhặt đồ thì hết ngày."* |

Quy tắc Vũ chốt:

> *"Cái gì ít thì bao giờ cũng chất, cái gì nhiều thì sẽ bị giảm đi. Nhà bố mẹ thu nhập 1 tháng 50 triệu mà có 1 thằng con thì may ra được mặc giày Adidas, mặc quần Gucci. Chứ mà để 10 đứa thì mặc kiểu gì luôn."*

Pattern hỗn hợp: nhiều game cho cả 2 — menu thay từng slot + auto. *"Bởi vì không biết người ta thích cái gì."*

### Tối Ưu Option 1 — Sáng Tạo Là Việc Nhỏ

Bài tập: Hiệp tối ưu 6 bước xuống. Cả lớp đưa ra 3 đề xuất:

1. **Bỏ nút Swap** — hiện luôn weapon hiện tại nửa trên, các weapon khác nửa dưới. Tap đổi chỗ. Còn 5 bước.
2. **Drag-and-drop** — kéo weapon từ list lên slot. Tooltip cho weapon info nếu text ngắn; panel riêng nếu nhiều thông tin (skin, upgrade).
3. **Chia 2 filter** (tab weapon + tab hero) — bấm vào kiếm là kiếm, bấm vào khiên là khiên, không phải chọn từng slot. **Còn 3 bước.**

Vũ chốt nguyên lý sáng tạo trong UI:

> *"Mọi người hãy hỏi tôi sáng tạo đâu — sáng tạo nằm đây này. Nó là những việc nhỏ, để cho user cảm thấy tiện hơn. Trước kia người ta thay 1 vũ khí rất cực, bây giờ người ta thay ít cực hơn. Trong 1 session chơi 20 phút, các bạn sẽ chơi được nhiều trận hơn, thử được nhiều loại chiến thuật hơn — tất nhiên họ sẽ chịu hơn."*

Lưu ý: đây mới là **luồng** (flow). Chưa nói gì về màu sắc, đồ họa.

### Vai Trò Của UI Flow Trong Estimate Dự Án

Khi không có UI flow rõ → estimate sai. Một là quá lâu vì không biết cần làm gì. Hai là estimate nhanh nhưng giữa kỳ phình ra.

Trong estimate, GD phải tự cho mình thời gian phân tích UI, thời gian chơi game tham chiếu. *"Một game mới chưa chơi bao giờ thì phải có thời gian chơi loại game đấy. Phích cứng luôn — mỗi lần chơi game chỉ được 30-45 phút. Chúng ta chơi game không phải là chơi, chúng ta chơi game là để nghiên cứu."* Monetize phải tính riêng — không thể chơi 30-45 phút mà ra được monetize.

---

## Tiêu Chí UX 2 — Thông Tin (Case Study Hero Info Của Đồng)

### 2 Câu Hỏi Mở Đầu

Vũ hỏi Đồng:
1. Tổng số trường dữ liệu (data field) cho 1 con hero là bao nhiêu?
2. Số trường show ra cho user là bao nhiêu?

Đồng đáp: **20 field total, show 10-12**. 8-10 còn lại bị ẩn vì *"hơi khó hình dung, hơi phức tạp, không khác biệt tương tự với nhau"*.

### Liệt Kê Các Trường Hiển Thị

| Trường | Hiển thị | Format |
|--------|----------|--------|
| Công, Thủ, Máu (ATK, DEF, HP) | Show — không bỏ được | Text |
| Crit rate | Show | Text (Vũ gợi ý dùng icon) |
| U-skin / U-skill (Unique) | Show | Hình ảnh |
| Số lượng U-skin (U0, U1) | Show | — |
| Rarity | Show | Hình ảnh |
| Mảnh tướng | Show có điều kiện | Hình ảnh khi chưa unlock |
| Daily book | Show có/không | Boolean |
| Cấp tiến hóa (Evo) | Có nút Elixir | Nút |
| Team skill | Show | — |
| Cấp độ hero | Show | Text (LVL) |
| Trang bị (6 slot) | Show | Slot icon |
| Passive skill | Show | Hình ảnh, không số |
| Ultimate | Show | Hình ảnh |

### 3 Loại Tối Ưu Thông Tin

Vũ chốt framework:

1. **Số lượng đầu thông tin** — có cắt bớt được trường nào không?
2. **Cách thức hiển thị** — icon vs text vs số. Trường nào dùng icon thay text được?
3. **Dung dạng thông tin** — cùng 1 trường, hiển thị bao nhiêu chữ?

#### Tối Ưu Số Lượng — HP và DEF Có Cần Tách Đôi?

Đồng giải thích công thức: `damage_taken = damage * DEF / (DEF + 2000)`. Vũ thử thách:

> *"Có thể quy cái đống DEF kia thành 1 HP khác không? Ví dụ với chỉ số hiện tại, tương đương HP bằng khoảng 10k không? Có nhất thiết phải sinh ra 2 chỉ số hay không?"*

Đồng giữ DEF vì *"đồ lắp vào tăng DEF"* — tăng DEF có hiển thị hệ số giảm sát thương, vẫn cần làm signal cho user thấy giá trị tài sản. Vũ accept: *"Anh chỉ đang hỏi thôi. Đấy là quá trình tối ưu."*

#### Tối Ưu Hiển Thị — Icon vs Text

Trên Hero info card, các trường nên chia thành:
- **Hiện text** (số): công/thủ/máu, crit rate, level.
- **Hiện icon**: passive (1 hình ảnh), ultimate (hình ảnh).
- **Hiện 1/2 (icon + số)**: nâng cấp với cộng chỉ số.

Quote về quy tắc đặt số bên ngoài button:

> *"Cái Ultimate kia của em có thể biến thành 1 dòng tech ở phía dưới nút upgrade kia không? Ví dụ như lên level 20 cộng crit 30%. Em đưa thông tin đấy ra ngoài, ngay dưới nút upgrade. Thứ nhất là nhanh hơn. Thứ 2 nữa là em nhồi hết tất cả cái đống ATK, HP, Defty của em trở thành icon gái thì nó ra gọn được rất nhiều."*

Quote chốt khái niệm icon vs text:

> *"Đây chính là cách mà tại sao nó lại phải dùng chữ — có dùng icon được hay không, và lý do vì sao."*

#### Tối Ưu Dung Dạng — Skill Description ≤ 8-10 Chữ

Khi bấm vào 1 skill, dòng mô tả nên ngắn:

> *"Em cố gắng tối đa từ 8 đến 10 chữ một lúc. Cái gì đấy em cố gắng tránh tình trạng là nó nhiều thứ quá khiến user bớt đảo, không muốn đảo."*

3 giá trị của việc bớt chữ:
1. User nhìn lướt → đọc → hiểu → so sánh được giữa các skill/skin.
2. Giải quyết lỗi ngắt câu/ngắt chữ khi xuống dòng nhiều.
3. User nước ngoài đọc cũng hiểu — không bị tràn câu, không biết câu nào chấm hết.

**Tip thêm**: số phải dùng màu khác (xanh hoặc nổi bật) để hút mắt user vào số trước, không phải đọc từ trên xuống dưới đều đều.

### Show Có Điều Kiện (Conditional Display)

Vũ hỏi: trường nào có lúc cần hiện, có lúc không?
- **Nút Evo (Evolve)** — chưa đủ mảnh tướng thì vẫn hiện nút (để user biết cách tiến tới).
- **Nút Upgrade** — nếu đủ tài nguyên thì sáng (xanh), thiếu thì xám.

Vũ note lỗi pattern: Đồng dùng nút màu đỏ thay vì xanh khi đủ tài nguyên. *"Em đang đi hơi khác logic thông thường. Thường để 1 xám thì nghĩa là không bấm được."*

### Hiển Thị Yêu Cầu Nâng Cấp Bên Ngoài

Khi popup mở, requirement (gold cần để nâng cấp) nên show ngoài hay trong popup? Vũ đề xuất:
- **Bên ngoài** — user nhìn thấy gold hiện tại (2.2m gold) và requirement luôn → quyết định nhanh.
- Hoặc giấu cộng-icon bên cạnh chỉ số → bấm là nâng cấp, không cần popup.

### Quy Tắc Đặt Tên Và Vị Trí

- **Thống nhất trái-phải/trên-dưới** cho cùng 1 loại thông tin. Nếu icon đứng trước số trong row 1, thì row 2 cũng phải icon trước số. *"Thống nhất một cái thôi."*
- **Vị trí nút theo logic thông thường** — tên hero trên, level dưới. *"Info bao giờ người ta cũng để trên góc trái."*
- **Hiển thị khác biệt cho hero chưa unlock** — locked hero phải khác visual so với unlocked hero (2 dòng đen, khung tạo tổ).

### Phá Vỡ Sự Đồng Bộ Khi Cần Hướng Sự Chú Ý

Đồng dùng chữ "Passive" và "Start" cho 2 phần trên Hero info. Vũ chỉ ra: nếu 2 phần khác nhau thì nên phá đồng bộ chứ không cố làm giống nhau. *"Ở khung dưới em cứ nguyên bỏ chữ Start, cái chữ Passive trên em hẳn 1 khung màu hẳn luôn, 1 khung khác hẳn luôn."*

### Hiển Thị Phần Trăm Cho Stat Ẩn (Dodge)

Đồng có stat **Dodge** (né đòn) nhưng không hiển thị số. Vũ chỉ ra: *"Vấn đề là người ta sẽ họng. Anh là user, anh cũng hiểu. Thế làm thế nào để biết là 20%?"* — phải show phần trăm khi có 2+ chỉ số ẩn cộng dồn.

---

## Tiêu Chí UX 3 — Quản Trị Sự Chú Ý (Notification Spam)

### Nguyên Lý: Giảm Quyết Định

> *"Vì sao phải giảm thiểu đưa quyết định? Đưa cho nó ít quyết định thôi, đừng có đưa ra nhiều quá. Hỏi hôm nay ăn gì — nó kể cho bức tranh, đưa 2 ốc sần. Hỏi 1 câu chuyện nhất thôi: 'đố em hôm nay ăn gì', nói trả lời đưa 1 món, đi ăn món đấy."*

### Đếm Noti Trên Màn Hình Đồng

Trên home screen của game Darwin (Đồng): **18 noti** trong đó có 3 cái dạng dương (animation). Vũ liệt kê: VIP, daily reward, season/battle pass, tournament, gói nạp, mission, mail, hero info, chapter rewards…

### 5 Loại Noti

1. **Loại 1: Nhận thưởng** (reward, gift)
2. **Loại 2: Playable** (có thể chơi — mode, tournament)
3. **Loại 3: Mission** (nhắc việc phải làm)
4. **Loại 4: IAP** (gói nạp)
5. **Loại 5: Ads** (xem 1 quảng cáo)

### Thứ Tự User Muốn vs Thứ Tự Mình Muốn (Designer)

| Thứ tự | User muốn (priority cao = đọc trước) | Designer muốn (priority cao = push trước) |
|--------|----------------------------------------|---------------------------------------------|
| 1 | Nhận thưởng | IAP |
| 2 | Playable | Ads |
| 3 | Mission | Mission |
| 4 | Ads | Playable |
| 5 | IAP | Nhận thưởng |

Hai bên ngược nhau hoàn toàn. *"Mình không có cách nào để chiều lòng cả đôi, cho nên mình chỉ có cách làm dung hòa thôi."*

### Chiến Lược Thực Tế — Theo Ý User Trước

> *"Việc đầu tiên, theo ý biết: mày chưa sướng thì không có chi tiêu gì hết. Cứ cho nhận thưởng đây đã, không chết ai cả... Nhận thưởng xong rồi tự dưng nó thấy có nhiều tiền, nó sướng — tâm trạng cảm xúc đang lên. Giống như mấy bà bán hàng áo cấp — vào chưa thấy mua bán gì, cứ cháu tặng các bác này tới mười hoa."*

Quy tắc cho 2 nhóm còn lại (Playable vs Mission):
- Mission **dễ có quà hơn** → user thích hơn → push Mission trước Playable.
- **Nguyên tắc**: bao giờ user cũng thích nhận quà trước, làm việc sau. *"Chả ai lại khổ sở đến mức quà có thể có 1 cái kiếm nhưng vẫn ra trận bằng tay chần, xong một tí về lấy kiếm sau."*

### Khi Nào Show Playable Noti

Không cần noti playable mặc định. *"Chỉ nên noti playable khi user nó quên mất chức năng này thôi."*

Pattern: vào đầu game, có tournament/dungeon → không noti. Sau 3-5 phút user không chơi → noti. Lý do: lúc đầu có quá nhiều việc (campaign, mission, lucky screen, ID reward...). Tránh user học pattern *"bấm nút T lần 1 có thưởng, lần 2 có thưởng, lần 3 có thưởng, nút 4 chắc có thưởng"*.

Tournament đặc biệt quan trọng với user dài ngày → hiển thị **số lượt còn lại (2/2, 1/2)** hoặc **level tournament** bên ngoài button → user biết có gì mới mà không cần bấm vào.

### Xử Lý Spam Noti

1. **3 cái dạng dương → chọn phát sáng** thay vì dung (chuyển động). User vào game không hiểu phải làm gì khi *"tất cả mọi thứ đều chuyển động"*.
2. **Daily reward**: phọc user xem luôn — *"vào liền phát phọc nó bắt nó nhận luôn"*, không để noti lừng lững.
3. **Battle pass/Season**: chuyển noti thành "hơi sáng lên một tí", không dạng chấm đỏ.
4. **Gói nạp đã hiện**: không cần noti — *"nạp xong là mất gói nạp rồi thì mình không tin"*.
5. **Tournament**: hiển thị `3/3` lượt chơi trực tiếp, không dùng noti chung chung.

### Cặp Màu Không Nên Dùng — Mũi Tên Đỏ + Mũi Tên Xanh

Đồng có vũ khí màu đỏ với mũi tên xanh đi kèm. Đức phản ánh: *"Cái mũi tên ở dưới nó lại màu xanh á. Nhìn trông nó kiểu cái gai mắt."*

Vũ note: hệ rarity chuẩn thường là **vàng > tím > xanh lá > xanh lam**. Đỏ ít dùng trừ khi là *"ý thích"* (rarity cao nhất tự chế).

---

## Phá UI — Đập Vỡ Grid Để Hút Mắt

Bình thường thiết kế UI theo grid để cân đều. **Phá UI** là cố tình làm lệch.

2 trường hợp thường phá UI:
1. **IAP** — nút to hơn bình thường, đẹp hơn, có effect.
2. **Giới thiệu content mới** — nút lệch hẳn khỏi grid.

### Bố Cục Tầm Tay (Thumb Zone) — Case Darwin

Vũ phản hồi layout home của Darwin (Đồng):
- 2 hàng button ở **trên cao** → người dùng phải vươn ngón tay lên.
- Phần dưới màn hình **rất trống**.
- *"Sao trả tiền quá khổ thế. Rơi điện thoại là nó bỏ game luôn đấy."*

Quy tắc: **kéo các nút quan trọng (đặc biệt là IAP) vào vị trí ngón tay người ta dễ bấm**. So với game gốc:
- Game gốc: nút setting/noti (ít quan trọng) ở góc xa.
- Game gốc: nút trả tiền + nút play ở vùng thumb-friendly (1/2 dưới màn hình).
- Darwin: tất cả nút compress vào 1/3 trên → không giống game gốc dù tham chiếu nó.

Pattern phân tay:
- **Tay phải**: đa số user (số liệu Đức: tay trái rất hiếm) → bố cục lệch phải.
- **Tay trái + Tay phải đều**: Đồng (tay trái) — số lượng "vương" rất ít.

---

## Monetize Design — Phân Loại Hành Vi IAP vs Ads

### 12 Driver Quyết Định Xem Ad / IAP

Cả lớp liệt kê (Vũ bổ sung):

1. Thua + cần thắng (giải quyết tình huống).
2. Tiêu / thêm tài nguyên.
3. Rút ngắn thời gian chơi.
4. Gacha (sở hữu tài sản).
5. Buster (thua).
6. Content.
7. Sở hữu tài sản.
8. Đi tìm bóng (random reward).
9. Cạnh tranh.
10. Sợ lỡ cơ hội (FOMO).
11. Ganh đua → tăng sức mạnh.
12. Lợi ích / profit so sánh.

### Quy Tắc IAP vs Ads Theo Trường Hợp

| Trường hợp | Khuyến cáo | Lý do |
|------------|------------|-------|
| **Thua + giải quyết tình huống tức thời** | Ads > IAP | IAP "không có giá trị giải quyết tức thời". Nếu thua vì thiếu sức mạnh → IAP nhưng chỉ bước nhỏ. |
| **Thiếu tài nguyên ít** | Ads | — |
| **Thiếu tài nguyên nhiều** | IAP | — |
| **So sánh profit (gói tổ hợp)** | IAP thuần | Tâm lý: hiệu ứng chim mồi (rẻ-vừa-đắt), bán theo thời gian, bán theo progress. |
| **Sở hữu tài sản (sinh giá trị)** | IAP | Ads stack được — không phải xem trực tiếp 1 quảng cáo, mà stack N quảng cáo trong 1 ngày để unlock. |
| **Rút ngắn thời gian chơi** | Ads | IAP "cảm thấy lãng phí" — không có tài sản rõ ràng để cầm tay. *"Sau 3 ngày không xem ad, nó vẫn tới mốc đó"*. |
| **No Ad** | IAP only | — |
| **Thêm content** | IAP (có thể mix Ads để test demand) | Content giá thấp qua Ad → user không quý content. *"1 con hero bằng 1-2 quảng cáo, mọi người sẽ phải sản xuất đến hàng chục con hero để nhận được khoảng 2-3 chục quảng cáo thì nó mới đủ chị hồi vốn."* |
| **Tăng sức mạnh bước nhỏ** | IAP | — |
| **Tăng sức mạnh bước lớn** (item, đồ làm khoẻ hẳn) | Ads | — |

Định nghĩa monetize Vũ nhấn:

> *"Monetize ở đây không phải là sao quảng cáo gì, mà là phải sao quảng cáo gì để tối ưu hóa được lực lượng sử dụng với nó."*

### Buster Khi Thua — Combo Quà Lớn Hơn

Pattern: khi user thua, đưa combo lớn (revive + buster + thậm chí không mất team) thay vì 1 buster đơn lẻ.

> *"1 của bom thì nó không xem. Nhưng 3 của bom cậu với việc không mất team — chỉ quyết định cái nào tốt hơn. Một số game đặc biệt là kể cả game chỉ đấu, cả battle, còn có tính năng: hồi sinh + cộng 20% attack speed để cho chận sau chơi vẻ thoải mái hơn."*

Lý do: phần này chỉ giải quyết tình huống, không tích lũy → cho thoải mái, không gãy balance. User không thích replay 2-3 lần 1 màn — *"mẫu lớn là luôn luôn muốn có cái mới vì sự thăng tiến của mình"*.

### Thiếu Tài Nguyên — Giá Tiệm Cận Progress

Quy tắc: giá Ads + giá IAP phải **tiệm cận với progress** (giá tài nguyên tăng theo level user).

Ví dụ:
- Level 1: nâng cấp hết 100 gold. Ads cho 100 gold. IAP $0.99 cho ~10 lần nâng cấp.
- Level 2-10: nâng cấp hết 200-1000 gold. Ads phải **giật tăng** theo (Ads = 200, 300, 1000 gold). IAP vẫn $0.99 nhưng chỉ còn ~6-7 lần nâng cấp.

*"Liệu rằng nó có ngồi chờ bạn — nó chờ đến tận 999 đếm cho nó mới được xem 1 ad? Vậy thì bạn hãy để cho phần này luôn luôn tiệm cận với cái thằng này."*

---

## Monetize — 2 Tư Duy First-Time Purchase

> *"Câu hỏi ở đây khác nhau. Mọi người sẽ phải đưa ra 1 quyết định ngay từ ban đầu trong lúc mùa chích kế: mọi người muốn có số ít user nạp tiền nhiều, hay muốn có số nhiều user nạp?"*

### Cách 1 — Giữ Nguyên Giá Trị (x2)

- First-time purchase chỉ x2.
- Lý do: nếu first-time x8 → user so sánh gói $1 với gói $10 sau đó → thấy đắt → không nạp tiếp.
- Phù hợp với game muốn giữ tỷ lệ giá trị giữa các tier IAP cân bằng.

### Cách 2 — First-IAP (x8, x cao 85%)

- Gói đầu rất rẻ, giá trị rất cao.
- *"Chỉ cần user bỏ gói đầu rồi là đã làm game thành công rồi."*
- Trade-off: gói thứ 2 rất khó convert vì gói đầu đã giá trị quá cao.
- Phù hợp với game muốn tối đa convert rate, mỗi user "đẹp nhất phá hết".

### Tránh Cỡ Giữa

> *"Mọi người hay bị cái lỡ cỡ ở giữa — đưa ra gói first time ban đầu cũng không hấp dẫn lắm nhưng giá trị lại cao. Dẫn tới cái tập khách hàng về sau: số lượng người trả gói đầu không được cao, mà những người đi sau cảm thấy gói đầu vẫn bị đắt, các gói sau vẫn bị đắt."*

### Bí Quyết: Bán Cái Không So Sánh Được

Học viên (game Battle Royale style của Hiệp/Tài) chia sẻ pattern bán **upgrade choice**: thay vì 3 skill khi lên level → 4 skill. Gói này không thể so sánh được với gói tài nguyên thông thường.

Pay rate: **gần 1%**. Trong số người mua, gói đó chiếm **80-90%** (cao bất thường so với gói khác chỉ 10-20%).

Vũ accept: *"Anh sẽ dừng câu hỏi ở đây bởi vì anh chưa có trải nghiệm làm cái kiểu như thế. Anh chỉ biết về mặt chín giá thôi."*

### Vị Trí Gói First-Time — Không Để Trong Shop

Pattern: gói first-time để **trên màn hình home**, không trong shop.

> *"Tâm lý user vào shop nó không cao — vào đấy là chỉ mất tiền chứ không được mẹ gì. Khi user nó vào, mình nói là ít 8, nó có tâm lý nó muốn mua. Còn không có ai tự dưng đi vào shop để làm cái gì cả."*

Phải có gói tham chiếu chứ — mới biết user hiểu "x2" là gì.

### Server-Side Detect — Biến First-Time Thành "Độ Hiếm"

Pattern Vũ đang dùng: server detect user nào sắp đến điểm phù hợp → push gói đầu trong 1-2 ngày → user thấy gói có "thời gian giới hạn" thay vì gói default. Hậu quả: user không so sánh gói này với gói shop sau đó, mà coi như gói event riêng.

---

## Subscription Pack — Case Study Game Nhạc (Amanote)

Giang hỏi: game nhạc tập trung subscription pack, không IAP. Khi nào nên dùng subscription?

### Số Liệu Amanote

| Metric | Số liệu Giang biết | Số liệu Vũ biết (2019) |
|--------|---------------------|--------------------------|
| Doanh thu từ subscription | 80% | ~100% |
| Pay rate (sub) | ~3% | 1.3-1.5% |
| Gói tuần | $5 | — |
| Gói tháng | $20 | $5 |

### Tâm Lý Mua Subscription

> *"Bản thân những trò chơi kiểu âm nhạc — anh có hỏi bên Amanote lúc trước, họ nói rằng game âm nhạc thì có cái đặc thù là chu kỳ tâm lý của họ khá dài. Yêu giữa có thể chơi 2-3 ngày, sau đó lại nghỉ. Lúc nào cũng quay lại chơi, rồi lại nghỉ. Họ không bỏ."*

Game nhạc:
- UX rất tả mát, content không lập lại được (không thể chơi 3 level cùng 1 bài nhạc).
- Số lượng content yêu cầu cao → bán gói $10-$20 cho 100 bài rất khó.
- Cơ chế sub: 80%+ user không tắt sub *"cho tới khi —"*. Yêu dơ không biết cách tắt. Khi nhận ra bị mất tiền vài lần thì mới tắt.
- *"Lượng tiền họ kiếm được trong cái quá trình kéo dài đấy nói nhiều hơn là việc giá trị họ có thể mua được 1 gói."*

### Khi Nào Nên Dùng Subscription

Sub OK khi:
- Game content / view (game nhạc, đọc truyện, xem phim, Netflix).
- *"Em đừng tự tưởng — chỉ cần 1 bài hát mới mà mình được chơi là họ đã đủ sướng rồi."*
- Giá trị mỗi ngày tương đương nhau, người ta thấy "ngày nào cũng nhận được gì đó".

Sub KHÔNG OK khi:
- Game RPG/Battle/AI Giang/Negamon — *"Người ta không biết là $100 sẽ giải quyết được cái gì cho 1 tháng. Làm sao người ta dám xuống tiền?"*
- Vũ ví dụ: Negamon bán con thú, nhưng không ép subscribe. *"Bọn anh chưa đến mức phải ép người dùng. Mình sẽ chỉ kiểm tra khi con game thật sự tốt."*
- Battle Pass / gói 30 ngày của RPG **không phải sub** — chỉ là chưa setup theo kiểu sub. Setup sub là khi hết 30 ngày tự trừ tiền, tự tặng lại quà.

### Sub Cho Cơ Hội Mua (Wukong)

Vũ kể case **Wukong**: mua skin được khoảng 100 gòn. Sau đó bán cái sub 100 gòn — user mua sub chỉ để được mua skin. *"Sub để mua skin đã là quá đáng, đây là sắp để mua cơ hội."*

### Bài Học Cho Game Mix IAP + Sub

Giang chia sẻ: game nhạc Giang đang làm vẫn để IAP ngay từ đầu + sub. User chưa kịp trải nghiệm content thì bị show IAP/sub → drop nhiều.

Vũ note bài học 2019: bên Amanote yêu cầu *"game chỉ có sub thôi, cũng quảng cáo hẳn kiếp"*. Game nhạc có bộ phận user *"chỉ là cấm cái tay nghe nhạc"* — quảng cáo lên là khó chịu, rú hầm. Vũ không update sau 2019 nên không chắc 2026 còn đúng không.

---

## UX Của Core Game — Tiêu Chí Thứ 3 Khi Click Pop-up Reward

Giang đặt câu hỏi của Doc 6 lại — về việc evolve core game qua các thế hệ. Vũ trả lời trực tiếp qua case study **Fast IAP popup** của Đồng (phần afk reward).

### Vấn Đề: Pop-up 2 Tab (Reward + IAP)

Khi user thua/cạn energy, pop-up hiện 2 option:
- Reward (xem quảng cáo)
- Mua 15 thể lực bằng ngọc (IAP)

Vũ phân tích:
- User mất 2 bước: bấm pop-up + đọc thông tin cũ + so sánh.
- Bắt user nhớ thông tin trước (giá energy normally) → 90% user sẽ skip cả Reward lẫn 15-thể-lực-mua.
- Con số IAP "200 mấy" rất khó nhận diện (vs "2.6").

### Sửa: Quy 1 Bước Ngoài

> *"Tại sao em không thể làm ở bên ngoài luôn — em quy ra 1 con số để xem tương đương bên ngoài, tương đương khoảng 30%. Em vừa không phải xấu bảng này, không phải nghĩ mà user chỉ có 1 bước thôi."*

Số liệu bên Vũ test: nắn ít bước nhất → **tỷ lệ tích cho nó khoảng 8%**.

> *"Càng nhiều bước thì tỉ lệ càng cố thực hiện theo ý của mình càng cao... Người ta càng ít suy nghĩ, khả năng xin theo quýt luôn. Người ta suy nghĩ càng nhiều thì người ta bỏ qua, cái ký càng càng lớn."*

---

## Dark UX — 5 Kỹ Thuật Cụ Thể

### Định Nghĩa và Nguyên Lý

> *"Đắc UX thường chỉ chỉ sử dụng khi mà những cái thứ về monetize mình làm mình nghĩ là tốt lắm rồi mà nó vẫn có chuyển đổi thấp — thì mình mới nên sử dụng đắc UX."*

Dark UX = lừa user. Trade-off: tỷ lệ click tăng nhưng user **nhiều cho cái chức năng đấy**, có thể ảnh hưởng retention.

### Dark UX 1 — Click vs Hold Trong Tăng Sức Mạnh

Trong gameplay nâng cấp: nên **hold** (giữ chấm) hay **click** (bấm)?

- **Gameplay**: hold OK — user dí 1 phát lên level cao luôn.
- **Monetize**: phải là **click** — mỗi lần bấm là 1 cơ hội show quảng cáo. Nếu hold thì không có event để bấm vào, popup IAP không bao giờ trigger được.

### Dark UX 2 — Đảo Vị Trí Pop-up Nâng Cấp Khi Thua

Khi user thua màn → thay vì show pop-up win-lose, show pop-up **nâng cấp con nhân vật** ở đúng vị trí pop-up win-lose. User theo thói quen bấm vào → vô tình bấm Upgrade.

Đề xuất: 1 quảng cáo → cộng 10-12 level **mà không mất tài nguyên** (bình thường nâng level mất gold). Tỷ lệ user xem ad tăng thêm 1-2 ad/user.

> *"Vấn đề ở chỗ: bọn user nó đang hiểu — màn chơi đấy nó bấm vào nút đấy để bách ra ngoài. Nhưng anh đặt cái nút nâng cấp vào đấy."*

### Dark UX 3 — Bán Content Khoá Theo Level

Pattern Vũ đã từng dính: game bán hero **chưa unlock**.
- Hero level 20 mới sử dụng được.
- Game bán hero ở level 6 user với giá rẻ (10k gold = $1-2).
- User mua xong vẫn chưa dùng được — phải cày tiếp đến level 20.
- *"Mình bắt đầu tưởng tự trong đầu: 'mày hỏi tao mua ở đây tao càn quét hết, mày mua pvp 1 litre bot này kia'. Mua xong rồi mới phát hiện ra đến tận level 20 nó mới ăn lấp. Khác gì lừa."*
- Refund chỉ vài tiếng → user không kịp refund.

### Dark UX 4 — No Ad Mua Kèm Buster / Tiền

Bán No Ad đơn thuần ít người mua. **Mix No Ad với gói có thêm buster hoặc tiền** → tăng giá trị gói, user dễ mua. Hoặc giới hạn No Ad chỉ trong vài ngày (Kenny Krut, Damon vẫn làm) — không thông báo rõ.

### Dark UX 5 — Arm Break / Inter Disguise

Đức chia sẻ pattern Voodoo dạy user: trước mỗi inter ad, chạy animation 2 giây có icon cốc cà phê — *"Arm Break"*. User học cách hiểu *"icon cốc cà phê = giải lao bình thường"*.

Sau khi train xong, game spam Inter ad với cùng icon → user tưởng là Arm Break, không skip.

Đức: *"Em vứt bố cái gói nó hoẹp đi luôn"* (quá ức chế). Vũ:

> *"Em tỉnh lệ mà lấy fan No Ad chắc chắn là chỉ 1%. 100 ông thì không có lòng lấy fan. Nhưng không phải chiều — bọn anh thì gói No Ad thì hầu như không bị lấy fan, tỷ lệ thấp lắm. Bởi vì đấy thì bọn anh vẫn để nó là bỏ cả Inter, cả Reward."*

Vũ ngày trước cũng dùng (animation 2 giây Inter trong popup level up). Cảnh báo: cái này nay hậu quả lớn, anh không update nữa.

### Dark UX 6 — Đảo Nút X3

User vẫn nhầm giữa Inter (click nhầm) và Reward (chủ động). Pattern:
- Nút Reward thường X3 (xem 3 quảng cáo nhận 3x). Khi cố tình **đảo vị trí 2 nút (Net + X3)**, dù kết quả như nhau (vẫn xem 1 quảng cáo) → tỷ lệ Reward tăng.

---

## Piggy Bank — Cơ Chế Hút Máu Cho Thiếu Tài Nguyên

Pattern Vũ làm trên game **Tidy Battle**:
- Bình thường xem ad được 1.000 tiền.
- Cho Piggy Bank tích thêm 500 nữa.
- Vào Piggy Bank xem 1 ad → được tầm 1.500.

Cơ chế thuần (game khác làm): tiền user kiếm được tự động vào Piggy Bank → user phải dùng tiền thật mua lại chính tiền mình kiếm. Vũ nhận: *"Của con anh áp dụng thử — anh thường nhận là nó cũng hút máu thật."*

Quy tắc thời gian Piggy Bank:
- 9-15 phút cho 1 lần xem.
- Không đặt dài hơn vì user tầm chơi 40-50 phút/ngày, dài quá user không quay lại được.

Lý do hiệu quả:

> *"Rõ ràng giá trị của 1 quảng cáo nếu xem thông thường là 1 con số x, nhưng xem ở 1 chỗ khác lại là giá trị x của y. Về lý người chơi gì tính toán thích cái x của y này hơn. Việc có x của y này nó đẩy nhanh quá trình giá của y — xo ra này nhiều hơn. Vì sao? Vì họ thấy ra có 1 cái lỡ."*

---

## Tổng Hợp Dark UX Per Loại Trường Hợp

| Loại | Dark UX áp dụng |
|------|------------------|
| Thua giải quyết tình huống | Đảo vị trí pop-up nâng cấp khi thua |
| Tài nguyên tự nhiên / không đủ | Piggy Bank |
| So sánh profit | First-time gói server-side detect (biến gói thành "độ hiếm") |
| Rút ngắn thời gian | Inter sau khi finish — disguise Arm Break |
| Thêm content | Bán content khoá level (rẻ nhưng cần level cao mới dùng) |
| Tăng sức mạnh | Click thay vì Hold (mỗi click 1 cơ hội ad/IAP); đảo nút X3 |
| No Ad | Mix với buster/tiền; giới hạn thời gian |

---

## Câu Hỏi / Chủ Đề Còn Nợ

- **Reach-out monetize riêng theo loại game** (câu hỏi Đức cuối buổi) — Vũ chưa trả lời sâu, hẹn buổi sau.
- **Live-Off model** — Đức gợi ý, Vũ chưa thử.
- **Update game nhạc 2026** — Vũ số liệu chỉ từ 2019, không chắc Amanote còn cùng pattern.

---

## Thuật Ngữ Buổi Này

- **UI Flow** — luồng (sequence) các màn hình và states user đi qua khi thực hiện 1 task. Không phải đồ họa, không phải màu sắc.
- **Số Bước Thao Tác** — tiêu chí UX 1, đếm số bấm/swipe user phải làm để hoàn thành 1 task. Càng ít càng tốt.
- **Auto-Equip** — tự động lắp toàn bộ trang bị tốt nhất cho hero hiện tại. Phù hợp game loại 1 (1 hero) và loại 3 (10+ hero), không phù hợp loại 2b (1-5 hero không có fun role).
- **Fun Role** — vai trò class cố định cho mỗi hero (kiếm/cung/giáo) khiến hero không tranh đồ lẫn nhau.
- **Thumb Zone** — vùng ngón tay user (đặc biệt ngón cái) dễ với tới trên màn hình điện thoại. Nút quan trọng phải nằm trong vùng này.
- **Phá UI** — cố tình thiết kế lệch grid để hút mắt vào element quan trọng (thường là IAP).
- **3 Loại Tối Ưu Thông Tin** — (1) Số lượng đầu thông tin, (2) Cách thức hiển thị (icon/text/số), (3) Dung dạng thông tin (số chữ).
- **5 Loại Noti** — Nhận thưởng / Playable / Mission / IAP / Ads.
- **Hiệu Ứng Chim Mồi** — 3 gói (rẻ-nhỏ / vừa-vừa / đắt-best-value) để đẩy user vào gói giữa hoặc đắt.
- **First-IAP** — tư duy gói đầu giá trị rất cao (x8, x cao 85%) để tối đa convert user free → user nạp.
- **Tư Duy Giữ Giá Trị** — gói đầu chỉ x2 để giữ tỷ lệ giá trị cân bằng với các gói sau.
- **Subscription Pack (Sub)** — gói tự trừ tiền định kỳ. Phù hợp game content/view (nhạc, đọc, xem phim), không phù hợp game RPG/Battle.
- **Dark UX (Đắc UX)** — kỹ thuật UI/UX có chủ đích lừa user để tăng conversion. Trade-off với churn rate / retention.
- **Piggy Bank** — pattern Ads/IAP: tiền user kiếm được tự tích vào "lợn", user phải xem ad hoặc trả tiền để rút.
- **Arm Break** — pattern Voodoo dạy user qua animation "cốc cà phê" trước mỗi quảng cáo để user nhầm Inter Ads là giải lao.
- **Đảo Nút X3** — đảo vị trí 2 nút Inter (Net) và Reward (X3) trong popup để user nhầm sang Reward, dù kết quả cùng là 1 quảng cáo.
- **Stack Ads** — yêu cầu user xem N quảng cáo trong khoảng thời gian (1 ngày, từ đầu game) để unlock tài sản — thay vì xem 1 quảng cáo trực tiếp.
- **Pay Rate** — % user trong tổng population có IAP. Sub Amanote: 1.3-3%. Game của học viên (gói không-so-sánh-được): 1%.
- **Buy7** — % user mua IAP trong 7 ngày đầu (mention chéo Doc 4).

---

## Nguồn

- Folder: `raw/videos/Game Design Course by Negaxy + IEC/`
- Audio gốc: `GD Doc 7.m4a`
- Transcript thô: `GD Doc 7.m4a.txt`
- Transcript cleaned: `GD Doc 7.m4a.cleaned.txt` (1032 dòng, đã polish, sửa ASR errors "Y/Y wick" → "UI/UX", thêm heading)
- Vị trí trong khóa: theo curriculum là **Buổi 7 (UI/UX/Monetize)**. Tiếp nối buổi 6 — buổi 6 đã ghi âm thành 2 video riêng (`GD Doc 6 Part 1 - UI.mp4` và `GD Doc 6 Part 2 - UX.mp4`) do được tách thành 2 phần khi quay.
- Reference từ Doc 2: "Style / Art direction sâu → Doc 7" — phần này buổi 7 không đi sâu, có thể được deal trong session khác.
- Khóa học: Game Design Course by Negaxy + IEC (8 buổi).
