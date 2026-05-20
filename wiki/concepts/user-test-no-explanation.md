---
title: "User Test Rule — Đừng Giải Thích Khi User Hỏi"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ux, user-research, testing, mindset]
aliases: [dont explain during test, user test rule, no help during test, GD invalidate test]
status: draft
related:
  - "[[behavior-vs-stated-preference]]"
  - "[[icon-vs-text-framework]]"
  - "[[playtest-protocol-designer]]"
summary: "Khi user test, GD KHÔNG được giải thích. User hỏi 'đây là gì?' = signal GD đã fail communication qua icon/text. Giải thích = invalidate data (user hiểu mất, lần sau không hỏi). Test fail = redesign, không phải hint."
---

## Định Nghĩa

User Test Rule = nguyên tắc bắt buộc khi observe user mới chơi game / sử dụng UI mới. GD KHÔNG được explain ANY UI element while user testing.

> *"Tất cả câu hỏi mà các bạn nhận được — game này là gì, nút này là gì — chỉ quy lại một vấn đề thôi: user nó không hiểu. Các bạn đi giải thích thì người ta hiểu mất rồi còn đâu — lần sau người ta hỏi làm sao được nữa."*

## Lý Do

### 1. Question = Signal Of Failure

User hỏi *"đây là gì?"* = GD đã **fail communication** qua:
- Icon không rõ.
- Text không informative.
- Position không follow convention.
- Color không cue priority.

Signal này là **data point** đáng giá. Bỏ qua = miss insight.

### 2. Explanation Invalidates Data

Khi GD giải thích:
- User hiểu icon/feature.
- Lần test tiếp theo (cùng cohort) → user không hỏi nữa.
- → False positive: "user hiểu" (actually because of explanation, not because UI clear).
- → Final UI ship với fail communication, user mass bị lost.

Test data phải reflect **organic behavior**, không reflect post-explanation behavior.

### 3. Repeat Test = Bias

Cùng group user test multiple iterations → memorize UI từ session trước. Designer phải:
- Recruit user mới mỗi iteration, hoặc
- Reset test với gap > 2 weeks, hoặc
- Use A/B test online (no facilitator).

## Process Đúng

Khi user hỏi:

1. **Acknowledge** — "I hear you."
2. **Redirect** — "Bạn thử tap thử xem nó làm gì?" (encourage exploration).
3. **Observe** — note user reaction khi tap (positive/confused/abandon).
4. **Document** — log question + outcome.

Sau session:

1. Review questions across users → identify common confusion points.
2. Redesign UI elements that triggered questions.
3. Re-test với cohort khác.

## Process Sai (Anti-Pattern)

GD's natural urge to help → typical responses:

| User Question | Wrong Response | Why Wrong |
|---------------|----------------|-----------|
| "Đây là gì?" | "Đây là nút Battle." | Invalidates icon design |
| "Làm sao chơi?" | "Bạn vuốt sang phải để start." | Invalidates onboarding |
| "Tap vào đâu?" | "Nút màu vàng ở dưới." | Invalidates visual hierarchy |
| "Tôi không hiểu" | "Để tôi giải thích..." | Loses entire signal |

Mỗi response chính là **redesign opportunity bị lost**.

## Connection To Communication-First Design

> *"User hỏi tức là **GD đã fail communication** qua icon/text/visual."*

Game design philosophy: UI là **silent communication**. Tutorial là crutch. Designer should aim for UI that needs no tutorial.

Test mục tiêu:
- < 5% user hỏi questions = UI clear.
- 10-20% user hỏi = needs refinement.
- > 20% user hỏi = redesign required.

## Connection To Inherited Habit

[[inherited-habit-conventions]] giảm câu hỏi:
- Home icon 🏠 → user không hỏi.
- Settings ⚙ → user không hỏi.
- Custom icon ⊕🏳 (+1 slot) → user hỏi → redesign with text.

Inherited habit = lower friction, lower question rate, higher test validity.

## Process Sai Khác

### "Tutorial Cover Up"

Designer detect UI confusion → add tutorial layer thay vì fix UI.

Hệ quả:
- Tutorial overhead D0 → fatigue → drop rate tăng.
- D7+ user không có tutorial → vẫn confused.
- Tăng technical debt (tutorial system maintenance).

Fix proper: redesign UI, eliminate tutorial requirement.

### Survey After Test

Designer hỏi *"Bạn có hiểu nút X không?"* → user trả lời "có" (politeness bias) → designer ship UI bị fail.

Fix proper: observe actions, not ask opinions. User stated preference ≠ behavior (xem [[behavior-vs-stated-preference]]).

## Edge Case — Tutorial Đã Plan

Tutorial mode (D0-D3) trong game có explicit teaching. User test trong này:
- OK to test "tutorial works?"
- Question rate trong tutorial OK (đó là điểm — guide user).
- Sau tutorial complete → re-test với fresh UI (post-tutorial state) → apply no-explanation rule.

## Liên Hệ Wiki

[[behavior-vs-stated-preference]] cho rationale rộng hơn (design cho hành vi, không cho lời nói). [[icon-vs-text-framework]] cho fix khi user hỏi icon. [[playtest-protocol-designer]] (skill) cho framework playtest đầy đủ.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "Đừng Giải Thích Khi User Test"
