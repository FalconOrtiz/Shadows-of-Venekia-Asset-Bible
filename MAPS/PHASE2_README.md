# PHASE 2 Map Pack — COMPLETE

**Version:** PHASE2.0 CLEAN text-free  
**Commit:** `8aab896`  

## Download
**SoV_MapPack_PHASE2_COMPLETE_CLEAN.zip** (6.7 MB)  
→ https://drive.google.com/file/d/1P8v1FNXu14lLl0uUzIRs57ydVBcpw67Z/view?usp=drivesdk  

Folder: https://drive.google.com/drive/folders/1JiKCX5zEypRHgscJ7roMqJhkNYJcH1G8

## Contents
| Zone | Demos | Atlases |
|------|-------|---------|
| eternal_plains | 40×30 | floors, edges, props, hazards |
| crystal_peaks | 40×30 | floors, edges, props |
| eternal_spire | f1–f4 (24×24), **boss on f4** | floors, props |
| dungeons | f1–f4 (30×30) | floors, walls/props |
| boss_arenas | 20×20 generic | arena hazards |
| transitions | — | Phase1↔2 corridor tiles |
| minimap | — | micro-tiles all biomes |

## Build drop
```
public/assets/pixel2d/maps/
  eternal_plains/
  crystal_peaks/
  eternal_spire/
  dungeons/
  boss_arenas/
  transitions/
  minimap/
```

Chroma `#FF00FF` · tiles **64×32** · props **64×64** · **no text on tiles**.

## Portal graph (Phase2)
- Plains ↔ City / Peaks / Spire
- Peaks ↔ Plains / City / Spire  
- Spire F1↔F2↔F3↔F4 (boss) · exit City
- Dungeons deeper · exit City
- Boss arena exit City
