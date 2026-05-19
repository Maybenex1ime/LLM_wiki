---
title: "D7 Hoà vs D3 Hoà — Quyết Định Scale"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [comparison, monetization, breakeven, ua, scale]
aliases: [D7 vs D3 hoà, lãi ở đây vs lãi ở đây mũ, điểm hoà]
status: draft
related:
  - "[[fueling-pacing]]"
  - "[[ltv-cpi-formula]]"
  - "[[iaa-iap-migration]]"
summary: "Game lãi ở D3 dễ ra quyết định, scale hạn chế. Game lãi ở D7+ khó làm hơn nhưng dễ scale qua UA. Quyết định phụ thuộc dòng game: hyper cho phép D0/D1, hybrid/ERP nên D3-D7+"
---

## Bối Cảnh

Vũ đặt câu hỏi trong Doc 3: tại sao test lãi ở D7 thì dễ scale hơn lãi ở D3? Giang phản biện đầu tiên rằng D3 dễ ra quyết định hơn. Vũ xác nhận quan điểm Giang đúng — *với điều kiện coi đây là một cách chơi game (kinh doanh game phải ra lợi nhuận)*. Nhưng để **scale**, D7 win.

> *"Anh làm cho người ta đây một cách chơi game. Lãi ở D7 sẽ đúng khi mà chúng ta coi đây là một cách chơi game. Chơi game thì phải ra lợi nhuận mà. Nhưng nó không phải là chơi game."*

## Bảng So Sánh

| Tiêu Chí | D3 Hoà | D7 Hoà (hoặc xa hơn) |
|----------|--------|----------------------|
| Quyết định scale | Dễ — chốt số nhanh | Khó — phải đợi 7 ngày dữ liệu |
| Bền vững | Thấp — pool user nhỏ, lifecycle ngắn | Cao — pool lớn, user retain dài |
| UA ROAS/GPA | D0/D0-1 cao → UA *"không chạy được dụng chạy luôn"* | UA scale được, GPA target xa cho phép pool lớn |
| Mặt feeling user | Bị ép sớm → mệt → bỏ nhanh | Cảm thấy "đáng chơi" → quay lại |
| Phù hợp dòng | Hyper (lifecycle 3-6 tháng, CPI rẻ) | Hybrid / ERP / partial puzzle |
| Content tiền đề | Vài ngày là đủ | Phải kéo dài tới ít nhất D7 |
| Pool sản phẩm | Có thể "hơi tệ" vẫn ra tiền sớm | Phải "chất lượng" — không bán "quả dưa bị thối" |
| Vùng khai thác | Hẹp — D2-D5 | Rộng — D7-D30+ |
| Case study | Múc Càn Trô cũ: ~30 triệu downloads | Múc Càn Trô mới: ~200 triệu downloads |

## Phân Tích

### Lý Do Kỹ Thuật — UA Không Scale Cho D0/D1

Vũ giải thích góc UA:

> *"Chạy tất cả con game các bạn đến thời điểm hiện tại. Với mặt UA các bạn có thể chạy ROAS, chạy GPA, các bạn nào target D0, D0-1 càng cao gần như cao của bạn không chạy được dụng chạy luôn. Cái này là thực tế nhất."*

UA platform (Facebook, Google, AppLovin) optimize theo target metric. Target D0/D1 ROAS cao → platform có ít user pool phù hợp (vì rare user nạp ngay ngày 1). Target D7 ROAS → pool user phù hợp lớn hơn nhiều → CPI hiệu quả thấp hơn → scale dễ hơn.

### Mặt Feeling User

Vũ phân tích góc trải nghiệm:

> *"Khi mà các bạn dồn dộng quá nhiều các thứ thì chúng ta kiếm tiền thôi user, cho người ta ra đầu — có nghĩa là người ta sẽ bỏ rất nhanh."*

Analogy mua nhà: *"người ta phải dàn trả ra trả nợ — nó không bắt bạn trả nợ ngay được. Chúng ta phải bỏ mặt tràn trải ra, sau đó người ta thanh toán."*

User ép D1 = ép trả tiền ngay khi vừa biết game. Pattern này có thể work cho hyper (lifecycle ngắn, không cần loyalty) nhưng fail cho hybrid (cần user gắn bó).

### Vùng Khai Thác

Vũ vẽ sơ đồ trên 2 con sản phẩm chất lượng tương đương:

- **Sản phẩm A**: Điểm hoà = D2. CPI tăng thì D2 sẽ tụt → phần dư khai thác hẹp.
- **Sản phẩm B**: Điểm hoà = D7 (hoặc D6/D8). Phần dư khai thác kéo dài → giá trị về tiền keo ~15.

> *"Thay vào việc điểm hoà đây chúng ta cộng cái số nhỏ, và điểm hoà đây chúng ta cộng cái số lớn — thì cái nào sẽ mang lại giá trị? Cái này nó sẽ chỉ mang là chúng ta sẽ khó quất tích trong giai đoạn nặng."*

Sản phẩm A có thể lãi sớm nhưng tổng lifetime revenue giới hạn. Sản phẩm B mất công đợi nhưng tổng lifetime revenue cao hơn nhiều.

### Quyết Định Theo Dòng Game

- **Hyper** → tỷ lệ ép sớm OK (anh em đã chạy quen, lifecycle ngắn).
- **Hybrid / partial / ERP** → nên target D3 hoà hoặc D7 hoà — dòng game cho phép pacing dài hơn.

Vũ note: D3 hoà cho hybrid là **trung gian an toàn**, D7+ là **scale ceiling cao** nhưng cần content đủ dài. Đây là quyết định liên quan đến [[fueling-pacing]] và [[iaa-iap-migration]].

## Kết Luận

D3 vs D7 không phải đúng/sai — phụ thuộc:
1. **Dòng game**: hyper buộc D0/D1, hybrid cho phép D3-D7+.
2. **Content có đủ kéo dài không**: nếu D5 đã hết content thì D7 hoà vô nghĩa.
3. **Quality sản phẩm**: chỉ D7 work nếu game đủ tốt để user retain.

Vũ chốt nguyên tắc: chuyển điểm hoà từ D2 sang D7 là **một bước scale lớn trong cùng cấu trúc game** — nhưng phải đầu tư đủ content và monetization spread.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "Day 7 Hoà Dễ Scale Hơn Day 3 Hoà", "Điểm Hoà — Càng Muộn Thì Vùng Khai Thác Càng Dài"
