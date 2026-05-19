---
title: "Leaderboard Vĩnh Viễn vs Theo Mùa"
source: "[[raw/videos/negaxy-iec-gd-doc-08-phan-tap-user]]"
date_added: 2026-05-15
tags: [comparison, leaderboard, retention, whale, ua]
aliases: [leaderboard permanent vs seasonal, top vĩnh viễn, season reset]
status: draft
related:
  - "[[user-segmentation-3-axes]]"
  - "[[user-archetype-asset-vs-self-expression]]"
summary: "Leaderboard vĩnh viễn (whale giữ ghế) vs theo mùa (user mới có cơ hội). Trade-off: whale-retention vs user-acquisition. Quyết định phụ thuộc tập user mục tiêu"
---

## Bối Cảnh

Vũ phân tích trade-off thiết kế leaderboard trong Doc 8, dựa trên trục **thời gian**: leaderboard reset hay không. 2 mô hình có hệ quả khác hẳn về retention strategy.

## Bảng So Sánh

| Tiêu Chí | Vĩnh Viễn (Permanent) | Theo Mùa (Seasonal) |
|----------|------------------------|----------------------|
| Reset | Không bao giờ | 1 tuần / 1 tháng / 1 quý |
| Top giữ ghế | Whale giữ vĩnh viễn (chỉ tụt 1 hạng nếu thằng khác làm tốt hơn) | Reset đầu mùa, ai cũng có cơ hội |
| Lợi cho whale | Cao — đầu tư lâu dài có giá trị | Thấp — phải tái đầu tư mỗi mùa |
| Cơ hội user mới | Thấp — phải đổ rất nhiều tiền + thời gian | Cao — chọn mùa nào tham gia |
| Chiến lược user | Đua tới chết để giữ vị trí | Chọn mùa, nghỉ-đua tùy ý |
| Phù hợp tập user | Whale-heavy (T2 trong [[user-segmentation-3-axes]]) | Mass user, casual / seasonal players |
| Retention model | Whale-retention | User-acquisition + flexible engagement |

## Phân Tích

### Loại 1 — Vĩnh Viễn

- Thằng top không bao giờ mất ghế. Chỉ tụt 1 hạng nếu có thằng khác làm tốt hơn.
- **Lợi**: whale nạp tiền nhiều giữ được vị trí → tạo cảm giác đầu tư có giá trị lâu dài. Whale không bỏ vì bỏ = mất tất cả công sức.
- **Hại**: user mới không có đường lên top hoặc phải đổ rất nhiều tiền + thời gian. Là **chướng ngại vật** cho thằng mới.

Hệ quả: game có top board "đông cứng" theo thời gian. Sau 1-2 năm, top 100 toàn whale veteran. User mới scroll xuống thấy không có ai từ install gần đây → cảm giác "không bao giờ với tới" → bỏ.

Phù hợp khi game đã có whale loyal community + không cần aggressive UA.

### Loại 2 — Theo Mùa

- Mỗi season 1 tuần / 1 tháng. Thành tích reset.
- **Lợi**: user mới có cơ hội — *"Mùa này tôi không đua cũng được, không sao. Mùa 2 tập trung đua thì đó nó sẽ cày tiền từ thời điểm này đi lên để gần danh những cái tốt. Mùa 2 nó có thể đua, mùa 3 nó có thể bỏ, mùa 4 nó có thể đua tùy cách nó chọn."*
- User có quyền **chọn mùa nào để đầu tư**.

Hệ quả: top board fresh mỗi season → user mới có hope. Bù lại, whale phải tái đầu tư mỗi mùa → có thể frustration. Một số whale bỏ vì *"tao đã top mùa 1 rồi, mùa 2 phải đua lại à?"*.

Phù hợp khi game muốn UA aggressive + cho phép user *"in/out"* tùy hứng.

## Quyết Định Theo Mục Tiêu

| Mục Tiêu | Chọn |
|----------|------|
| Retain whale lâu dài | Permanent |
| Maximize convert free → paying ở user mới | Seasonal |
| Cộng đồng nhỏ, loyal | Permanent |
| Mass market, casual touch | Seasonal |
| Esports game | Seasonal (with permanent stats / lifetime achievements) |

Một số game mix: leaderboard mùa cho competition + bảng "Hall of Fame" vĩnh viễn cho lịch sử. Pattern này serve cả 2 — whale có vĩnh viễn record để khoe, user mới có seasonal để đua.

## Phân Tích Game Phải Phân Loại Theo Tập Trả Phí vs Free

Mini-insight Vũ chốt cuối phần leaderboard. Hai góc nhìn user khác hẳn nhau khi phân tích game:

- **User nạp tiền**: *"Cái đội nạp tiền nó sẽ có cái kiểu tư duy là nó thích cái gì là nó sẽ đưa vào trong game về đấy."*
- **User không nạp tiền**: *"Tới lúc mà bắt đi thanh minh, bắt đi giải trình là vì sao làm gói nạp cái này hơi khoai. Bị khó."*

Quote: *"Đây là kỹ năng phân tích game. Và khi các bạn phân tích mà theo kiểu nào các bạn sẽ thấy khác."*

Hệ quả thiết kế leaderboard: nếu designer toàn nạp tiền, có xu hướng nghĩ leaderboard vĩnh viễn ổn vì *"ai chẳng giống mình"*. Phải tự kiểm tra qua góc nhìn user free để cân bằng.

## Kết Luận

Quyết định leaderboard không phải vĩnh viễn vs seasonal đúng/sai — phụ thuộc:

1. **Tập user mục tiêu** (xem [[user-archetype-asset-vs-self-expression]]): Nhóm Tài Sản phù hợp vĩnh viễn (đầu tư dài); Nhóm Thể Hiện Bản Thân thường thích seasonal (challenge mới).
2. **Stage game**: launch mới → seasonal; mature có whale loyal → permanent có thể OK.
3. **UA strategy**: aggressive UA cần seasonal để give hope; organic-only có thể dùng permanent.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-08-phan-tap-user.md` § "Leaderboard — Vĩnh Viễn vs Theo Mùa", "Phân Tích Game Phải Phân Loại Theo Tập Trả Phí vs Free"
