---
title: "Vector vs Bitmap — Game Art Format Trade-Off"
source: "[[raw/videos/negaxy-iec-gd-doc-05-part-1-art]]"
date_added: 2026-05-20
tags: [comparison, art, asset-pipeline, vector, bitmap, raster]
aliases: [vector vs bitmap, vector graphics, bitmap raster, art format choice]
status: draft
related:
  - "[[art-brief-3-parts]]"
  - "[[form-base-art-template]]"
summary: "Vector giữ chất lượng ở mọi zoom level, lý tưởng cho card-based games (Tam Quốc, Kiếm Hiệp). Bitmap đẹp khi zoom in nhưng vỡ khi zoom out. Outline 2-3 pixel cho vector giúp tách hình khi zoom nhỏ. Art behavior: zoom in để vẽ chi tiết → zoom out để check → bitmap fail step 2."
---

## Bối Cảnh

Đức (game thẻ bài) đề cập "hạn chế dùng Guardian (Bitmap)." Vũ đào sâu lý do trong Doc 5 Part 1, dẫn case 2Cơ Game / IEC luôn dùng vector cho card-based games.

> *"Em nên sử dụng vector và đẩy outline vào. Thì khi zoom nhỏ ảnh của em sẽ không bị vỡ."*

## Bảng So Sánh

| Aspect | Vector | Bitmap (Raster) |
|--------|--------|------------------|
| **Đặc trưng** | Mathematical paths | Pixel grid |
| **Zoom in** | Sharp ở mọi level | Sharp đến 100%, sau đó pixelated |
| **Zoom out** | Sharp, scaled down clean | Bị vỡ ("muddied") khi quá nhỏ |
| **File size** | Smaller (formula data) | Larger (per-pixel data) |
| **Software** | Illustrator, Affinity Designer, Inkscape | Photoshop, Procreate, Krita |
| **Animation** | Skeletal rig efficient | Per-frame redraw |
| **Memory in-game** | Texture memory low | Texture memory higher |
| **Art workflow** | Zoom in to vẽ chi tiết, scale clean | Zoom in vẽ, scale fail |
| **Detail ceiling** | Limited bởi shape complexity | High (per-pixel control) |

## Phân Tích

### Art Behavior Khi Vẽ

> *"Em có biết là art của họ có behavior phóng to lên để họ vẽ, sau đó họ sẽ zoom nhỏ lại không? Đấy chính là lý do mà vì sao cái level design này thường sẽ bị sai. Có cái ảnh sẽ rất nhìn to rất đẹp — nhưng khi zoom nhỏ lại rất khó."*

Workflow chuẩn của art:
1. Zoom in 200-500% → vẽ chi tiết.
2. Zoom out 100% → check overall.
3. Repeat.

Bitmap fail step 2: chi tiết vẽ ở 500% bị **lost** khi scale về 100%. Vector preserve detail.

### Card Size Card-Based Games

Card games hay có 30-50 thẻ trên màn cùng lúc:
- Phone resolution: 1080 × 1920.
- 30 cards → mỗi card khoảng 150-200 pixel.
- Card size nhỏ này = vector zone.

Bitmap card 200 pixel:
- Original art có thể là 800 × 1200.
- Scale xuống 200 pixel → 25% size → details lost.
- → "ảnh muddied," không rõ.

Vector card 200 pixel:
- Original path render at 200 pixel → sharp.
- Outline 2-3 pixel emphasizes edge.
- → user thấy rõ subject vs background.

### Outline Pattern

> *"Outline em chỉ cần chỉnh lại theo đường bo của con đấy — ví dụ outline 3 pixel hay 2 pixel."*

Outline cho vector:
- Width: 2-3 pixel ở 100% zoom.
- Color: contrast với fill (black outline trên light fill, white outline trên dark fill).
- Effect: tách subject khỏi background ngay cả khi card 100 pixel.

Bitmap không có "outline" concept inherent — phải vẽ manual stroke per pixel.

## Khi Nào Dùng Vector

- **Card-based games** (Hearthstone, Tam Quốc, Kiếm Hiệp).
- **Mobile UI** (icon, button — must be sharp at any DPI).
- **2D characters** với animation rig (joints + skeletal).
- **Logo / Branding** (web + game).
- **Map / Tile-based games** (consistent tile rendering).

## Khi Nào Dùng Bitmap

- **High-fidelity 2D illustration** (game adventure, visual novel).
- **3D rendered textures** (game 3D — texture maps).
- **Photo-realistic art** (concept art, splash screen).
- **Sprite animation** với per-frame variation (pixel art).
- **Background art** lớn không scale.

## Hybrid Pattern

Phổ biến: combine cả 2.
- **Card layout** = vector (sharp at any scale).
- **Card art** = bitmap (detail).
- **UI overlay** = vector (HUD, buttons).
- **3D model textures** = bitmap.

Vũ confirm: 2Cơ Game và IEC dùng vector cho **collection panel 2D** (card library) + 3D model trong battle.

## Anti-Pattern: Bitmap Cho Mọi Asset

Studio không think về scale:
- Designer paste reference Photoshop → art workflow.
- Output: bitmap PNG cho mọi asset.
- Performance: lag khi nhiều card render cùng lúc.
- Visual: card nhỏ bị vỡ.

Fix: convert workflow sang vector cho UI / card / icon. Keep bitmap cho gameplay 3D textures.

## Performance Implication

| Resource | Vector | Bitmap |
|----------|--------|--------|
| Storage | Smaller (path data) | Larger (pixel grid) |
| Memory load | Faster | Slower |
| Render time | More compute per frame | Less compute (just blit) |
| Scaling | Smooth | Mip-mapping required |

Mobile target rộng (low-end Android included): vector tốt hơn cho UI / card. Bitmap OK cho mainline gameplay textures.

## Liên Hệ Wiki

[[art-brief-3-parts]] — Part 1 (Art Style) include vector vs bitmap choice. [[form-base-art-template]] — vector form base scale tốt hơn bitmap, lợi cho production line.

## Nguồn Tham Khảo

- `raw/videos/negaxy-iec-gd-doc-05-part-1-art.md` § "Vector vs Bitmap — Phải Outline"
