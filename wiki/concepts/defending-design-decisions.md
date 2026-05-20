---
title: "Defending Design Decisions — Document Reasoning Trước Khi Pitch"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-2-ux]]"
date_added: 2026-05-20
tags: [concept, gd-craft, process, mindset]
aliases: [defending decisions, document reasoning, bull start dự án, bảo vệ đồng chí, reasoning framework]
status: draft
related:
  - "[[file-y-do-design-intent]]"
  - "[[5-levels-of-idea]]"
  - "[[multi-start-design]]"
  - "[[level-iteration-testing]]"
summary: "GD phải document **lý do** của feature decisions trước khi pitch. Vũ chốt: 'Bull start dự án phải bảo vệ đồng chí em.' Khi UA/sếp hỏi 'tại sao,' nếu không trả lời được = fail communication. Test fail mà không có reasoning = không iterate được."
---

## Định Nghĩa

Defending Design Decisions = practice document **lý do** cho mọi feature decision trước khi pitch. Bao gồm:

- **Mục đích** của feature (vấn đề nó giải quyết).
- **Alternatives đã consider** (vì sao không chọn).
- **Expected outcome** (KPI dự kiến).
- **Test plan** (cách đo success/failure).
- **Failure mode** (kế hoạch khi fail).

Mục tiêu: GD có thể **trả lời câu hỏi** từ stakeholders mà không cần ad-hoc explain.

## Vũ's Quote — "Bull Start Dự Án Phải Bảo Vệ Đồng Chí Em"

Context: Đồng (học viên) muốn pivot game kingdom từ 1-hero sang 3-hero multi-start. Vũ cảnh báo:

> *"Bull start dự án là phải bảo vệ đồng chí em."*

Tức là: ngay từ giai đoạn start dự án, mọi feature decision phải **defensible**. Khi đứng trước sếp/team/UA, designer phải articulate lý do.

> *"Đấy là cái rất khó về tầm mình đấy. Một con game hoặc là một con app của mình nó được cấu tạo từ rất rất rất nhiều thứ. Nên đôi lúc mình cũng chả biết là nó đúng ở cái gì là cái nào. Nhưng mà chúng ta làm một cách là không có hệ thống dễ dễ bị thuyết phục."*

## Common Failure Mode — Khi GD Không Document

Vũ describes typical conflict:

> *"Hay bị trường hợp conflict đó là các ông available là các ông thuần tách. Thì người đó sẽ hỏi tại sao lại dùng vùng ảnh này, tại sao lại diễn cái action này trong khoảng thời gian này. Các bố chẳng trả lời được."*

Scenario:
1. UA team làm video creative dựa trên gameplay.
2. UA hỏi GD: "Vì sao vùng ảnh này / action này tại timing này?"
3. GD không có document → không trả lời được.
4. UA implement creative không match design intent → ad rate kém.
5. Designer phải post-hoc fix → tốn time + lose ad spend.

Same scenario với code team, art team, QA: mỗi đối tác hỏi "vì sao?" — GD không có answer = fail.

## Framework Defending

### Question Frame

> *"Tất cả các câu hỏi của mọi người nằm trong tất cả cái khuôn của mình. Và nếu mọi người hỏi những câu hỏi ngoài khuôn, hoàn toàn có thể đi bên lại."*

GD chia câu hỏi thành 2 zones:

| Zone | GD's Response |
|------|---------------|
| **Trong khuôn** (in scope) | Trả lời được, có reasoning |
| **Ngoài khuôn** (out of scope) | "Tôi không cover phần này — đi đến anh A" |

Cả 2 OK. Fail = "trong khuôn" mà không trả lời được.

### Test Cheap vs Test Expensive

> *"Theo anh là như thế này anh tư vấn anh không không nếu như trường hợp đấy các bạn ấy làm nhanh không. Nếu bạn bạn nếu bạn chứng minh được làm nhanh thì có thể thử còn nếu mà bạn ấy thấy ra là phải áp dụng cái đấy nó nó rất là lâu thì cũng phải để mình các bạn ấy làm nhanh anh sẽ thật."*

Decision gate:
- **Test rẻ** (1-2 ngày code) → cứ thử. Document reasoning post-hoc.
- **Test đắt** (1+ tháng code) → defend logic chặt trước. Đảm bảo nếu fail vẫn iterate được.

Đồng's case (pivot 1-hero → 3-hero kingdom): high cost, no precedent, hero stat chưa ngon. *"Rất khó quay đầu."* → defend logic chặt trước khi commit.

## Khi Test Fail Mà Không Có Reasoning

Worst-case scenario:

> *"Kể cả là thuyết phục được rồi sau lúc sau test chả biết nó đúng hay sai ở đâu. Khó nhất là cái việc đấy luôn. Các sếp đã dễ tính cho test rồi thì về sau nó đúng thì không sao đâu — nó đúng có nghĩa là anh ạ chả biết đúng ở đâu. Nó đúng có sai ở đâu. Cười với nhau hết một lần."*

Test pass mà không biết tại sao → không iterate được:
- Không biết extend feature theo hướng nào.
- Không biết feature gãy ở point nào nếu condition thay đổi.
- Designer phụ thuộc luck.

Test fail mà không biết tại sao → không learn được:
- Không biết feature fail vì design hay vì execution.
- Không biết feature fail vì cohort hay vì timing.
- Designer rebuild blindly.

## Practical Checklist

Trước khi pitch / commit feature:

| Item | Format | Example |
|------|--------|---------|
| **Goal** | 1-line | "Increase D7 retention từ 15% → 20%" |
| **Hypothesis** | 1-line | "Daily challenge tăng touchpoint" |
| **Alternative considered** | List | "Considered: ad-for-life, gem reward, mission swap. Chose challenge vì lý do X" |
| **KPI to measure** | 2-3 metrics | "D7 retention, daily session count, IAP conversion" |
| **Test duration** | Specific | "2 weeks A/B test, 50/50 split" |
| **Success criteria** | Threshold | "D7 retention +3 percentage points = win" |
| **Failure plan** | Decision | "Nếu D7 < +1pp → revert + post-mortem" |

Format này = "khuôn" cho stakeholder hỏi. Mọi câu hỏi map vào 1 row.

## Anti-Pattern: Chiều Học Viên / Team Member Quá

> *"Em cứ chia sẻ là em nghĩ là em nhiều lúc em cũng chiều các bạn cực kì luôn. Các bạn muốn làm gì thì họ cũng đã cho các bạn thoải mái ấy. Nhưng ở góc độ về đầu tư là mình lo thật."*

Đồng admit: chiều team member dù không tin tưởng tech. Vũ frame: chiều quá → mất control sản phẩm.

Trade-off:
- **Chiều quá** → team morale OK ngắn hạn, sản phẩm trượt hướng dài hạn.
- **Strict quá** → team demoralized, project delays.
- **Balance**: cho team test ý tưởng RẺ, defend logic cho ý tưởng ĐẮT.

## Liên Hệ Wiki

[[file-y-do-design-intent]] cho file design intent — output của process này. [[5-levels-of-idea]] cho thang chín 5 mức — cấp 4-5 yêu cầu defending logic chặt. [[multi-start-design]] cho case study Đồng pitch multi-start, defending vs Hiệp (defensible vs not). [[level-iteration-testing]] cho framework test 4 phase (S1-S4) — defending logic là pre-step.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-2-ux.md` § "Defending Decisions — Bull Start Dự Án Phải Bảo Vệ Đồng Chí Em"
