---
title: "Icon vs Text Framework — Khi Nào Icon Đủ, Khi Nào Cần Text"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ui, icon-design, button-design, tutorial, mobile-ui]
aliases: [icon vs text, button text length, +1 slot Tiny Battle, remove ad text]
status: draft
related:
  - "[[inherited-habit-conventions]]"
  - "[[user-test-no-explanation]]"
  - "[[ux-3-criteria]]"
summary: "Test bằng user: hiểu icon → không cần text. Không hiểu → cần text. D0-D7 hay cần text + icon; D7+ chuyển sang icon-only. Case Tiny Battle '+1 slot' không text → click rate thấp. Remove Ad bắt buộc text. Cap 5-7 ký tự cho text trong button."
---

## Định Nghĩa

Icon vs Text = decision framework cho mỗi button: dùng icon only, text only, hay icon + text.

Quyết định dựa trên:
- User test result.
- Game phase (D0-D7 vs D7+).
- Convention familiarity ([[inherited-habit-conventions]]).
- Space constraint.

## Pattern Test — User Hiểu Không?

Process:

1. Cho user mới scan UI 3-5 giây.
2. Hỏi *"đây là nút làm gì?"*.
3. Đo accuracy:
   - **≥ 80% hiểu** → icon đủ.
   - **< 80% hiểu** → cần text bổ sung.

⚠️ Constraint: GD KHÔNG được explain. *"Các bạn đi giải thích thì người ta hiểu mất rồi còn đâu — lần sau người ta hỏi làm sao được nữa."* Xem [[user-test-no-explanation]] cho rule này.

## Phase-Based Strategy

| Phase | Icon vs Text |
|-------|--------------|
| **D0-D7** (tutorial era) | Icon + Text — user chưa biết game |
| **D7-D30** (learning) | Icon + Text fade-out gradually |
| **D30+** (committed) | Icon-only — user đã quen |

Designer thiết kế **2 versions UI**:
- Version A: full text + icon, cho user mới.
- Version B: icon-only, cho user đã quen.

Switch trigger: user reach session count threshold, hoặc dismiss tutorial.

Lợi:
- D0-D7 không bị lost (text guide).
- D7+ get clean UI (icon-only).
- IAP slot có thêm space khi text bị bỏ.

## Case Study Tiny Battle "+1 Slot"

Vũ kể anti-pattern:

> *"Anti-pattern: icon 'dấu cộng + cờ' không có text → user không hiểu là gì → click rate thấp."*

Original:
- Icon: dấu cộng + cờ ⊕🏳.
- No text.
- Position: side panel.

User behavior: scan icon → không hiểu → skip.

Fix:
- Icon + text "+1 slot".
- Click rate **tăng nhiều**.

> *"Đối với những cái nào mà nó khó hiểu thì gọi nên sự tài thiện. Còn các game khác — tính năng phổ thông của nhiều con game rồi — thì không cần đặc biệt."*

Bài học: feature **mới / unique cho game này** → cần text. Feature **phổ thông** (home, play, settings) → icon đủ.

## Case Study Remove Ad

Vũ chốt: "Remove Ad" 2 chữ → ngắn nhất, **bắt buộc text**.

Lý do:
- "Remove Ad" không có icon universal (chữ X, no-ad symbol — chưa thành standard).
- User cần explicit hiểu "đây là remove ad," không nhầm với close/cancel.
- Trigger: sau inter-ad → offer remove ad popup → user emotional moment → text rõ ràng = high convert.

Plus: vị trí icon-only nếu space tight, thêm text khi có space.

## Text Length Cap

Vũ chốt cap 5-7 ký tự max cho text trong button.

| Text | OK? |
|------|-----|
| "Home" | ✅ 4 ký tự |
| "Battle" | ✅ 6 ký tự |
| "Weapon" | ✅ 6 ký tự |
| "Item" | ✅ 4 ký tự |
| "Shop" | ✅ 4 ký tự |
| "Settings" | ⚠️ 8 ký tự (border) |
| "Inventory" | ❌ 9 ký tự (use icon) |
| "Achievement" | ❌ 11 ký tự (use icon) |

Tips:
- Bỏ số "1" → "Slot" thay vì "1 Slot."
- Bỏ chữ "Esc" → text ngắn nhất.
- Title-case tốt hơn UPPERCASE (đọc nhanh hơn).

> *"Để text to nhất có thể trong diện tích nút."*

Lợi text to:
- D7+ user scan nhanh.
- Old users (>40 tuổi) đọc dễ.
- Avoid translation overflow (Vietnamese → English có thể giảm/tăng độ dài).

## Icon Convention vs Custom Icon

| Convention | Recommend Icon Only? |
|------------|----------------------|
| Home (nhà 🏠) | ✅ Universal |
| Settings (gear ⚙) | ✅ Universal |
| Play (▶) | ✅ Universal |
| Back (←) | ✅ Universal |
| Inventory (bag 🎒) | ✅ Common in RPG |
| Custom feature (như +1 slot) | ❌ Need text |
| Custom mechanic (game-specific) | ❌ Need text |

Universal icon = inherited habit (xem [[inherited-habit-conventions]]). User đã memorize.

Custom icon = need teach. Text bổ sung hoặc tutorial repetition.

## Anti-Pattern

- **Custom icon thay convention** — phá inherited habit.
- **Text > 7 ký tự trong button** — không đọc kịp / font phải nhỏ.
- **Text + icon mà text redundant với icon** — waste space.
- **Icon-only cho feature custom** — click rate thấp (Tiny Battle case).
- **GD giải thích icon trong test** — invalidate user signal.

## Liên Hệ Wiki

[[inherited-habit-conventions]] cho universal icons không cần text. [[user-test-no-explanation]] cho rule khi test. [[ux-3-criteria]] tiêu chí 2 (giảm thông tin) — icon-only là form ngắn nhất nếu user hiểu.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "Icon vs Text — Decision Framework"
