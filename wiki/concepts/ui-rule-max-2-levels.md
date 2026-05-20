---
title: "UI Rule — Max 2 Tầng Menu"
source: "[[raw/videos/negaxy-iec-gd-doc-06-part-1-ui]]"
date_added: 2026-05-20
tags: [concept, ui, navigation, depth-limit, mobile-design]
aliases: [rule 2 tầng, max 2 menu levels, depth limit UI, không drill 3 lần]
status: draft
related:
  - "[[ui-button-3-spawn-types]]"
  - "[[ui-wireframe-workflow]]"
  - "[[ux-3-criteria]]"
summary: "Vũ chốt rule: UI tối đa 2 tầng menu. Nút → popup. Không nút → popup → sub-popup. Vi phạm = UX rắc rối ở layer UX sau. Example: Setting → Music slider (đúng) vs Setting → Music → Stereo/BGM/SFX (sai 3 tầng)."
---

## Định Nghĩa

UI Rule = navigation depth tối đa 2 tầng kể từ root màn:
- Tầng 1: button click → popup / sub-screen.
- Tầng 2: option trong popup.
- Tầng 3+: ❌ KHÔNG cho phép.

> *"Tuyệt đối không đưa cái này sang cái 1.1.1 cái gì nữa. Tức là nút nó chỉ có đến 2 tầng thôi."*

## Lý Do

> *"Nếu không game của các bạn các luồng flow mà lúc sau phần UX sẽ cực kỳ rắc rối."*

3+ tầng = vi phạm các nguyên tắc UX:
- **Quy luật "khoảng cách"** — user phải tap nhiều lần → friction.
- **Cognitive load** — user phải nhớ context của các tầng cha.
- **Back navigation** — user mất tracking, sai exit point.
- **Test coverage** — exponential combination → khó QA.

## Examples Đúng vs Sai

### Setting Menu

| Pattern | Tầng | Đánh Giá |
|---------|------|----------|
| Setting → Music slider, Language flag, Connect Facebook | 2 | ✅ Đúng |
| Setting → Music → Stereo / Background / SFX | 3 | ❌ Sai |

Mọi setting option phải fit trong 1 màn. Nếu có nhiều option, dùng:
- **Tabs** trong 1 màn (Music tab, Display tab, Account tab) — vẫn 2 tầng.
- **Scrollable list** — vẫn 1 màn.
- **Collapsable section** — visual, không phải tầng riêng.

### Language Selection

| Pattern | Tầng | Đánh Giá |
|---------|------|----------|
| Language → list cờ Anh / Pháp / Mỹ (chọn vuốt) | 2 | ✅ Đúng |
| Language → dropdown chỏ xuống → list | 3 | ❌ Sai (web pattern không phù hợp mobile) |

Mobile game không dùng dropdown. List cờ trực tiếp visible.

### Equipment Flow

Approach A từ [[equip-flow-hero-vs-weapon]]:
- Tap hero → popup vũ khí available → tap equip. **2 tầng** ✅

Approach sai:
- Tap hero → popup info → tap equip → popup list weapon → popup weapon detail → confirm. **5 tầng** ❌

## Workaround Khi Cần Depth

Khi feature thực sự cần > 2 tầng, dùng các tactics:

### 1. Tab Trong 1 Màn

Thay vì:
- Setting → Music → Stereo / BGM / SFX (3 tầng)

Dùng:
- Setting với 3 tab: General, Audio, Account.
- Tab Audio có 3 slider (Music, BGM, SFX) cùng màn.
- Vẫn 2 tầng.

### 2. Scroll Vertical

Setting list dài 20 option → scroll trong 1 màn. Vẫn 1 màn.

### 3. Collapse Group

```
Audio Settings
├── Music: ──●──
├── BGM: ──●──
└── SFX: ──●──
```

Collapse/expand không tăng tầng (visual change only).

### 4. Mega Modal

Modal popup chiếm full màn với tabs + sections. Tốt cho complex feature (deck building, character upgrade).

## Khi Web Pattern Nhầm Vào Mobile

Designer có background web hay nhầm:
- **Dropdown chỏ xuống** — web pattern, mobile không touch-friendly.
- **Tooltip hover** — mobile không có hover.
- **Multi-level breadcrumb** — web pattern, mobile không có space.

> *"Như kiểu mình chơi cái Pokemon Hay Diablo lúc đầu lúc nào. Mình chả phải chọn nhân vật đầu tiên."*

Adapt sang mobile:
- Dropdown → flat list / scroll.
- Tooltip → tap-to-show inline.
- Breadcrumb → back button.

## Mobile vs PC

PC/Console game có thể có 3-4 tầng menu (cursor + keyboard chấp nhận navigation cost).

Mobile = touch + thumb = max 2 tầng. Tăng thêm tầng = drop rate tăng exponential.

## Liên Hệ Wiki

[[ui-button-3-spawn-types]] cho 3 loại trigger (popup là tầng 1, flow lên đới là tầng 2). [[ui-wireframe-workflow]] cho workflow apply rule này. [[ux-3-criteria]] tiêu chí 1 (giảm số bước) — rule 2 tầng là instance của tiêu chí 1.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-06-part-1-ui.md` § "Rule UI Cốt Lõi: Tối Đa 2 Tầng"
