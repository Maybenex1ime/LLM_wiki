---
title: "ARPU vs ARPPU — Trade-off Cho ERP"
source: "[[raw/videos/negaxy-iec-gd-doc-03-phase-du-an]]"
date_added: 2026-05-15
tags: [comparison, monetization, arpu, arppu, pay-rate]
aliases: [ARPU vs ARPPU, whale heavy vs pay rate cao, trade-off ERP]
status: draft
related:
  - "[[iap-pricing-user-value]]"
  - "[[fueling-pacing]]"
  - "[[user-segmentation-3-axes]]"
summary: "ARPU = doanh thu / tổng user (kể cả free); ARPPU = doanh thu / chỉ user trả tiền. ARPPU cao + pay rate thấp = whale heavy. ARPU cao đến qua tăng pay rate. Vũ khuyên ERP đẩy ARPU thay vì chỉ ARPPU"
---

## Bối Cảnh

Doc 3 Part 2, Vũ giải thích 2 metric doanh thu user và trade-off khi tối ưu chúng. Học viên có game ERP thường confuse 2 chỉ số này — đẩy ARPPU cao tưởng là tốt nhưng pay rate quá thấp thì ARPU vẫn đi ngang.

## Định Nghĩa

- **ARPU** (Average Revenue Per User) — tổng doanh thu / tổng số user (kể cả không trả tiền).
- **ARPPU** (Average Revenue Per Paying User) — doanh thu / chỉ số user đã trả tiền.

Quote Vũ:

> *"Em thấy ARPPU làm gì khi mà tỷ lệ nó lại thấp? Đúng rồi — ARPU cao."*

## Bảng So Sánh

| Tiêu Chí | ARPU | ARPPU |
|----------|------|-------|
| Mẫu số | Tổng user (paying + free) | Chỉ paying user |
| Phụ thuộc pay rate | Có — pay rate càng cao thì ARPU càng tăng | Không — pay rate không ảnh hưởng |
| Whale risk | Spread risk khi pay rate cao | High khi pay rate thấp |
| Đặc trưng | Tăng được qua converting free → paying | Tăng được qua bán pack đắt hơn |
| Insight | Sức khỏe tổng thể monetization | Tâm lý mua của user đã pay |

## Trade-off Pattern

Hai pattern thường gặp khi tối ưu:

### Pattern 1 — ARPPU Cao + Pay Rate Thấp

- Số ít whale (vd 0.5%) đóng góp đại đa số doanh thu.
- ARPPU rất cao (vd $200) nhưng ARPU thấp (vd $1).
- Game phụ thuộc whale → 1 whale bỏ = tụt doanh thu mạnh.

Đặc trưng: gói IAP đắt, pack lớn, designed for whale. Phù hợp game RPG cao tầng nhưng risk concentration.

### Pattern 2 — ARPPU Cân Bằng + Pay Rate Cao

- Nhiều user (vd 5%) cùng trả ít (vd $20 trung bình).
- ARPPU thấp ($20) nhưng ARPU cao ($1 vẫn) — ổn định hơn.
- Game không phụ thuộc whale → 1 user bỏ không ảnh hưởng lớn.

Đặc trưng: gói IAP nhỏ (micro-pack $0.99-$4.99), pricing dễ tiếp cận. Phù hợp game casual / hybrid.

## Khuyến Cáo Cho ERP

Vũ khuyên ưu tiên đẩy ARPU lên qua pay rate, không chỉ đẩy ARPPU:

> *"Đối với ERP nhé — hãy cố gắng biến user free thành user trả tiền. Khi user đã trả tiền rồi hãy cứ dừng với họ. Cứ dừng càng kéo thì em sẽ kéo cái credit này càng cao."*

"Cứ dừng càng kéo" = **giữ user trả tiền lâu dài thay vì ép họ trả thật nhiều ngay lần đầu**. Pattern này liên quan đến [[fueling-pacing]] (kéo break-even từ D3 sang D7+) và [[iap-pricing-user-value]] (định giá pack theo journey value).

## Khi Nào Tối Ưu ARPPU

ARPPU vẫn là metric quan trọng cho:

- **Game whale-heavy đặt design** (vd. high-end MOBA, premium card battler) — chấp nhận pay rate thấp.
- **Đánh giá impact của 1 promotion** lên user đã trả tiền — không bị nhiễu bởi free user.
- **Theo dõi tier upgrade** — user T0 → T2 → T5 progression.

Whale heavy không phải sai — chỉ là risk concentration cao. Đối với [[user-segmentation-3-axes]] tier T2 (nhanh tay, top spending), pattern whale-heavy là hợp lý.

## Liên Hệ Với Phân Tập User

ARPU/ARPPU ratio gợi ý tập user:
- ARPPU/ARPU > 100 → whale-heavy → tập T2 (top spender) dominate.
- ARPPU/ARPU < 20 → distributed → tập T3-T4 spread đều.

Phân tích này áp dụng [[metric-diagnosis-4-methods]] method "dimension" — tách ARPU theo segment user.

## Kết Luận

ARPU và ARPPU không phải 2 metric đối lập — chúng đo 2 khía cạnh khác. ARPU đo **sức khỏe tổng** monetization; ARPPU đo **chất lượng** từng paying user. Game tối ưu 1 cái mà bỏ cái còn lại đều risky:

- Bỏ ARPU → game phụ thuộc whale.
- Bỏ ARPPU → game không có gói cao tier để user power-up.

Vũ khuyên ERP: ưu tiên ARPU qua convert nhiều user → trả tiền nhỏ thường xuyên (sustainable), thay vì ép ARPPU lên (fragile).

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-03-phase-du-an.md` § "ARPU vs ARPPU — Trade-off Cho ERP"
