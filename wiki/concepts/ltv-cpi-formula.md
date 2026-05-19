---
title: "Công Thức LTV > CPI"
source: "[[raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset]]"
date_added: 2026-05-15
tags: [concept, monetization, ltv, cpi, ua, mobile-games]
aliases: [LTV vs CPI, công thức bán dự án, ngoại suy D7 D60]
status: draft
related:
  - "[[5-levels-of-idea]]"
  - "[[ecpm-blackbox]]"
  - "[[iaa-iap-migration]]"
  - "[[d7-vs-d3-breakeven]]"
  - "[[fueling-pacing]]"
summary: "Khung số liệu Hiệp dùng để bảo vệ dự án — phân tách inputs (CPI) và outputs (LTV) thành các biến đo lường được, điều kiện duyệt: LTV > CPI"
---

## Định Nghĩa

LTV > CPI là **điều kiện business cốt lõi** Hiệp dùng để bảo vệ dự án với sếp. Mỗi vế là một composite metric:

```
Input vào con game ─→ CPI (Cost Per Install)
                  ├─ pool thị trường (lớn → CPI thấp)
                  ├─ trend / hot keyword
                  ├─ LTV reference của dòng
                  └─ creative đang viral

Output từ con game ─→ LTV (Lifetime Value)
                   ├─ time chơi / session
                   ├─ retention chuỗi (D1, D3, D7, D30)
                   ├─ impressions tổng cộng
                   └─ A-B-B metric

Điều kiện duyệt dự án: LTV > CPI
```

Khung này biến quyết định *"có làm dự án này không"* từ chuyện cảm tính ("idea hay quá!") thành chuyện số học. Hiệp nhấn: *"Đây là cái mà các bạn cần để bảo vệ với sếp, không phải mồm."*

## Tính Impression Từ Session

Hiệp đưa ví dụ tính cụ thể impression để ước lượng LTV qua ad revenue:

```
Time chơi target:    30 phút / session
Break down (Doc 2):  10 inter ads / session
Retention chuỗi:     D1=40%, D2=30%, D3=20%, D4=10%

Tổng impression đến D4 = 10 + 4 + 3 + 2 + 1 = 20 ads/user
LTV ad ≈ 20 × eCPM tham chiếu / 1000
```

Phép tính tương tự áp dụng cho IAP nếu game có pay rate ước lượng được. Khi LTV ad + LTV iap > CPI ước lượng → dự án có cơ sở duyệt.

## Ngoại Suy Cho Game Dài Hạn

Đảng phản biện: với game dài hạn, đến D60 mới hòa được CPI, mà test chỉ chốt số ở D3-D7. Hiệp trả lời:

- Phải có **kinh nghiệm ngoại suy** từ D7 → D30 → D60.
- Bên ngoài (Trung Quốc) hay dùng công thức ngoại suy nhiều hơn.
- Áp dụng đúng công thức chỉ ~1% chốt quyết định — *"nó sẽ không 100% được, và về sau có rất nhiều biến số khác."*
- Phụ thuộc **năng lực team**: nếu GD biết tối ưu D7 đến ngưỡng X thì ngoại suy D60 đúng. Nếu chỉ làm D3 đẹp mà D7 đã tụt thì công thức sai.

Vũ thêm bối cảnh: ngày xưa mua game Trung Quốc về VDC, chỉ số nước ngoài và Việt Nam không khớp nhau. Trust số thị trường khó.

## Limit Của Công Thức — eCPM Là Hộp Đen

Vũ chia sẻ case cay đắng: **2 con game giống hệt nhau** mọi mặt (cơ chế, art, balance, retention) nhưng eCPM một con gấp 3 lần con kia. *"Bí ẩn thật. Đúng không? Đó là giải thích được không? Đó không có câu trả lời."*

Có sản phẩm chỉ số "rất tuyệt vời nhưng eCPM không gì cả — chịu". Có sản phẩm chỉ số bình thường, CPI cũng đấy nhưng eCPM trên rời, vẫn win. eCPM phụ thuộc CTR, tệp khách hàng UA, mức độ đồ họa, style game, performance trên Play Store — nhiều biến ngoài tầm kiểm soát của designer. Xem [[ecpm-blackbox]] cho deep-dive.

Hệ quả: LTV ước lượng có thể đúng về retention/impression nhưng sai về tổng revenue do eCPM lệch. Bên Hiệp gửi gắm: dùng công thức để **decide go/no-go** chứ không phải để forecast doanh thu chính xác.

## Anti-Pattern — "Nói Mồm"

Quote Hiệp: *"Sếp dám bỏ 2 tuần — nếu LTV ước lượng > CPI nhưng không làm được — đây là dự án mới của lá."* Khi designer pitch mà không có 2 vế (CPI input + LTV output) số liệu cụ thể, sếp sẽ default từ chối hoặc giao mơ hồ. Cách Hiệp dùng để vận hành: từng dự án mới, designer phải tự nộp LTV-CPI estimate.

Sensor Tower / mock số thị trường: Hiệp không tin. *"Anh em hỏi thật, anh em nhìn vào chỉ số sensor tower anh em có tin không? Mình nhìn vào hồi xưa, có vẻ — chắc là hơi khói free thì không đúng."* Trust chỉ đến từ chính con game của mình.

## Liên Hệ Wiki

LTV > CPI là điểm chốt của [[5-levels-of-idea]] level 5 (idea phải có CPI/LTV plan). [[fueling-pacing]] giải thích cách kéo dài LTV bằng giãn break-even từ D3 sang D7 — cùng cấu trúc game nhưng vùng khai thác mở rộng. [[iaa-iap-migration]] giải thích tại sao IAA dependent quá nhiều vào eCPM thị trường, push studios migrate sang IAP để tách biệt.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-01-gd-role-mindset.md` § "Công Thức LTV > CPI", "Ngoại Suy Cho Game Dài Hạn", "Sensor Tower? Không Trust"
