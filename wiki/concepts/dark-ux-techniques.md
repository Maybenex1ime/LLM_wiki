---
title: "Dark UX Techniques"
source: "[[raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize]]"
date_added: 2026-05-15
tags: [concept, ux, monetization, dark-pattern, ads, iap]
aliases: [dark UX, đắc UX, lừa user UX, arm break]
status: draft
related:
  - "[[ux-3-criteria]]"
  - "[[piggy-bank-monetization]]"
  - "[[notification-management]]"
  - "[[first-iap-strategy]]"
summary: "6 kỹ thuật Dark UX: Click vs Hold, đảo pop-up nâng cấp khi thua, bán content khoá level, No Ad mix với buster, Arm Break (Voodoo), đảo nút X3. Trade-off: tăng conversion nhưng có thể ảnh hưởng retention"
---

## Định Nghĩa

Dark UX = kỹ thuật UI/UX có chủ đích **lừa user** để tăng conversion (ad click, IAP). Vũ định nghĩa:

> *"Đắc UX thường chỉ chỉ sử dụng khi mà những cái thứ về monetize mình làm mình nghĩ là tốt lắm rồi mà nó vẫn có chuyển đổi thấp — thì mình mới nên sử dụng đắc UX."*

Trade-off: tỷ lệ click tăng nhưng user **nhiều cho cái chức năng đấy**, có thể ảnh hưởng retention.

## 6 Kỹ Thuật Chính

### 1. Click vs Hold Trong Tăng Sức Mạnh

Gameplay nâng cấp: nên hold (giữ chấm) hay click (bấm)?

- **Gameplay**: hold OK — user dí 1 phát lên level cao luôn.
- **Monetize**: phải là **click** — mỗi lần bấm là 1 cơ hội show quảng cáo. Nếu hold thì không có event để bấm vào, popup IAP không bao giờ trigger được.

Designer chọn click dù gameplay-wise có thể tệ hơn, vì mỗi click là điểm intercept.

### 2. Đảo Vị Trí Pop-up Nâng Cấp Khi Thua

Khi user thua màn → thay vì show pop-up win-lose, show pop-up **nâng cấp con nhân vật** ở đúng vị trí pop-up win-lose. User theo thói quen bấm vào → vô tình bấm Upgrade.

Đề xuất: 1 quảng cáo → cộng 10-12 level **mà không mất tài nguyên** (bình thường nâng level mất gold). Tỷ lệ user xem ad tăng thêm 1-2 ad/user.

> *"Vấn đề ở chỗ: bọn user nó đang hiểu — màn chơi đấy nó bấm vào nút đấy để bách ra ngoài. Nhưng anh đặt cái nút nâng cấp vào đấy."*

### 3. Bán Content Khoá Theo Level

Pattern Vũ đã từng dính: game bán hero **chưa unlock**.
- Hero level 20 mới sử dụng được.
- Game bán hero ở level 6 user với giá rẻ (10k gold = $1-2).
- User mua xong vẫn chưa dùng được — phải cày tiếp đến level 20.
- *"Mình bắt đầu tưởng tự trong đầu: 'mày hỏi tao mua ở đây tao càn quét hết, mày mua pvp 1 litre bot này kia'. Mua xong rồi mới phát hiện ra đến tận level 20 nó mới ăn lấp. Khác gì lừa."*
- Refund chỉ vài tiếng → user không kịp refund.

Vũ nhấn pattern này là dark thật sự, không phải "đẩy biên" — hậu quả lớn cho lòng tin user dài hạn.

### 4. No Ad Mix Với Buster / Tiền

Bán No Ad đơn thuần ít người mua. **Mix No Ad với gói có thêm buster hoặc tiền** → tăng giá trị gói, user dễ mua. Hoặc giới hạn No Ad chỉ trong vài ngày (Kenny Krut, Damon vẫn làm) — không thông báo rõ.

Trade-off: user tưởng mua No Ad vĩnh viễn nhưng thực ra chỉ 30 ngày. Khi hết → quảng cáo lại → user phản ứng tiêu cực.

### 5. Arm Break / Inter Disguise (Voodoo)

Đức chia sẻ pattern Voodoo dạy user: trước mỗi inter ad, chạy animation 2 giây có icon **cốc cà phê** — *"Arm Break"*. User học cách hiểu *"icon cốc cà phê = giải lao bình thường"*.

Sau khi train xong, game spam Inter ad với cùng icon → user tưởng là Arm Break, không skip.

Đức (publisher VNG trước đây): *"Em vứt bố cái gói nó hoẹp đi luôn"* (quá ức chế). Vũ ngày trước cũng dùng (animation 2 giây Inter trong popup level up). Cảnh báo: hậu quả lớn, anh không update nữa.

Pattern này có tỷ lệ tiền lưu fan No Ad cao — *"100 ông thì không có lòng lấy fan"*.

### 6. Đảo Nút X3

User vẫn nhầm giữa Inter (click nhầm) và Reward (chủ động). Pattern:
- Nút Reward thường X3 (xem 3 quảng cáo nhận 3x).
- Cố tình **đảo vị trí 2 nút (Net + X3)**, dù kết quả như nhau (vẫn xem 1 quảng cáo) → tỷ lệ Reward tăng.

Hai nút có cùng kết quả monetize (1 ad show), chỉ khác cảm xúc user. Đảo vị trí khiến user thói quen bấm vào nút Reward thay vì Net → conversion ad tăng.

## Quy 1 Bước Ngoài — Tận Dụng Pop-up Nhỏ

Pattern bonus: pop-up 2 tab (Reward + IAP) khi thua/cạn energy bắt user *"đọc thông tin cũ + so sánh"* — 90% skip cả 2.

Sửa: quy ra 1 con số tương đương bên ngoài pop-up. User chỉ có 1 bước.

Số liệu Vũ test: tỷ lệ tích cho khoảng **8%** với pattern ít bước nhất.

> *"Càng nhiều bước thì tỉ lệ càng cố thực hiện theo ý của mình càng cao... Người ta càng ít suy nghĩ, khả năng xin theo quýt luôn. Người ta suy nghĩ càng nhiều thì người ta bỏ qua, cái ký càng càng lớn."*

## Tổng Hợp Dark UX Per Loại Trường Hợp

| Loại Vấn Đề | Dark UX Áp Dụng |
|-------------|------------------|
| Thua giải quyết tình huống | Đảo vị trí pop-up nâng cấp khi thua |
| Tài nguyên tự nhiên / không đủ | [[piggy-bank-monetization]] |
| So sánh profit | First-time gói server-side detect (biến gói thành "độ hiếm") |
| Rút ngắn thời gian | Inter sau khi finish — disguise Arm Break |
| Thêm content | Bán content khoá level (rẻ nhưng cần level cao mới dùng) |
| Tăng sức mạnh | Click thay vì Hold; đảo nút X3 |
| No Ad | Mix với buster/tiền; giới hạn thời gian |

## Liên Hệ Wiki

[[ux-3-criteria]] là khung "good UX" — dark UX là deliberate violation. [[piggy-bank-monetization]] là một dark UX cụ thể có nguyên tắc thời gian riêng. [[notification-management]] cho noti management — đảo X3 và Arm Break đều là noti manipulation. [[first-iap-strategy]] cho server-side detect first-time pack pattern.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-07-ui-ux-monetize.md` § "Dark UX — 5 Kỹ Thuật Cụ Thể", "Tổng Hợp Dark UX Per Loại Trường Hợp", "UX Của Core Game"
