---
title: "Operations Log"
date_added: 2025-01-01
status: canonical
summary: "Chronological log of all wiki operations"
---

# 📝 Operations Log

> Append-only chronological record of all operations performed on this vault.
> Each workflow (`/ingest`, `/compile`, `/ask`, `/cleanup`) appends one line here.
> Format: `## [YYYY-MM-DD] action | description`

---

<!-- Operations will be appended below this line -->

## [2026-04-23] ingest | gamerefinery-match-3-code-part-2 (How to Crack the Match 3 Code? - Part 2)
## [2026-04-23] ingest | linkedin-tandon-match-3-code-part-1 (How to Crack the Match 3 Code? - Part 1)
## [2026-05-05] compile | 10 bài mới (1 publisher + 9 concepts) từ Lion Studios MVP Guide + Level Design Playbook
## [2026-05-06] compile | 4 bài mới (3 concepts + 1 tool) từ User Guideline Databuckets
## [2026-05-06] compile | 1 bài mới (economy-balance-dashboard, 11 ảnh chart) từ XGAME Economy dashboard guide
## [2026-05-06] compile | 5 bài mới (level-analytics, monetization, offer-system, player-journey, retention dashboards) từ 5 file XGAME còn lại + 26 ảnh chart
## [2026-05-15] transcribe | GD Doc 3 - Phase du an.MOV (10 chunks → 1500 dòng) + cleanup doc2/doc3/doc8 chunks (~460MB)
## [2026-05-15] update | negaxy-iec-gd-doc-03-phase-du-an (471→690 dòng): fix Feelings/Fueling label theo audio gốc, thêm Part 2 (UX, retention, ARPU/ARPPU, imba balance, hierarchy reward quảng cáo)
## [2026-05-15] compile | 48 bài mới (35 concepts + 9 comparisons + 3 people + 1 tool) + 3 cập nhật từ 6 GD Docs notes (Khóa Game Design Negaxy + IEC)
## [2026-05-18] transcribe | GD Doc 3 - Phase du an.MOV (re-run, 20×10-min chunks, beam=1 fallback): 192KB / 4318 dòng — ~3× content vs run 2026-05-15. Backup cũ giữ `.bak.20260518-090832`. Compile lại raw note còn pending.
## [2026-05-19] update | negaxy-iec-gd-doc-03-phase-du-an (690→1313 dòng): re-compile từ transcription 4318 dòng. Thêm Part 3 — Improve Chỉ Số framework với 17 sections mới (chỉ số nào GD can thiệp, critique độ tuổi/văn hoá, content vs theme, UX deep dive iPhone/Úc/Nhật, 3 loại stack, 4 mức học-rèn-thử-master, sướng vs khổ, ngắt mềm vs cứng, Daily Challenge 28-day, notification expectations, ad timing vs skill unlock, hierarchy reward theo dòng game, Imposter Solo Queue case, hyper vs hybrid lifetime curves, win-screen ad tricks 18 versions, bán song song vs gated, IAP package structure 5-tier, revenue chart shape ERP). Mở rộng terminology section với 5 nhóm thuật ngữ mới.
## [2026-05-20] transcribe | GD Doc 6 Part 2 - UX.mp4 (86.8 phút, faster-whisper large-v3 int8): 9×10-min chunks; chunks 001/003/008 re-split thành 5-min sub-parts (sub5/) do hallucination loop. Hôm nay transcribe nốt `sub5/chunk_008_part_1.wav` (1.78 phút) — chunk cuối còn dở từ 2026-05-19. Concat → `GD Doc 6 Part 2 - UX.mp4.txt` 2075 dòng / 95KB. Compile raw note còn pending.
## [2026-05-20] compile-raw | negaxy-iec-gd-doc-06-part-2-ux.md (470 dòng) — biên dịch transcript 2075 dòng thành raw note structured. Bao phủ: UX yêu ích definition, hành vi vs lời nói, value perception 4 kỹ thuật, gameplay UX (Negabon/CoC/Farm/Royale-vs-Rumble), heart system, 3 giảm thiểu UI, multi-start, defending decisions. Buổi dừng sớm 10:20pm, Dark UX/Upstreet dời sang buổi sau.
## [2026-05-20] compile | 30 bài mới (24 concepts + 6 comparisons) + 3 cập nhật từ 4 raw notes Doc 5/6 (Part 1/Part 2 mỗi doc). Concepts: ux-yeu-ich-definition, behavior-vs-stated-preference, value-perception-techniques, inherited-habit-conventions, heart-system-design, multi-start-design, material-count-decision-paralysis, skin-bridging-comparison, slot-locked-upgrade, single-button-skill-collapse, clash-of-clans-punishment-evolution, defending-design-decisions, ui-wireframe-workflow, ui-button-3-levels, ui-button-3-spawn-types, ui-rule-max-2-levels, ui-5-color-brief, clash-royale-percent-stat-display, icon-vs-text-framework, user-test-no-explanation, art-brief-3-parts, form-base-art-template, mep-mep-affordance, animation-brief-essentials, hit-reaction-3-approaches, projectile-design-types, blend-animation-pattern, gd-reverse-skin-time. Comparisons: equip-flow-hero-vs-weapon, vector-vs-bitmap-game-art, cast-time-cao-bang-vs-per-con, farm-game-resource-gates, clash-royale-vs-warcraft-rumble, hearthstone-vs-uvo-card-text. Cập nhật: ux-3-criteria (note Doc 6 P2 origin), hiep-iec (add Negabon + Pokemon multi-start contributions), negaxy-iec-gd-course (Doc 5/6 entries). Wiki: 68 → 102 articles.
