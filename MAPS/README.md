# Shadows of Venekia — Map Packs PHASE1 COMPLETE

**Status:** ✅ All 5 zones ready · CLEAN text-free atlases · Build drop-in

## Primary download (use this)
**SoV_MapPack_PHASE1_COMPLETE_CLEAN.zip** (9.8 MB)  
→ https://drive.google.com/file/d/1afrk6SWo_gZiBO03-5CAKOtKqQ77HEpq/view?usp=drivesdk  

Folder: https://drive.google.com/drive/folders/1JiKCX5zEypRHgscJ7roMqJhkNYJcH1G8

## Zones
| Zone | Demo | Atlases | Hub |
|------|------|---------|-----|
| scorched_highlands | 40×30 | floors, edges, hazards, props | no |
| whispering_jungle | 40×30 | floors, edges, hazards, props | no |
| city_venekia | 32×32 | floors, edges, portals, props | **yes** |
| cursed_coast | 40×30 | floors, edges+hazards, props | no |
| mines_of_robir | 40×30 | floors, edges+hazards, props | no |

## Build path
```
public/assets/pixel2d/maps/
  scorched_highlands/
  whispering_jungle/
  city_venekia/
  cursed_coast/
  mines_of_robir/
```
Each contains: atlas_*.png + meta.json + maps/*_demo/layers/{ground,collision,props,spawns}.json

## Pipeline
1. Chroma `#FF00FF` → transparent
2. Slice grid (measure first cell)
3. Scale tiles → 64×32, props → 64×64
4. Load meta + layers
5. Portals ↔ enterZone / goCity

## Individual zips (also CLEAN)
- M0 Highlands
- M1 Jungle
- M2 City
- M2b Coast+Mines
- CLEAN TextFree (atlases only)

## Commits history
- M0: 8d9af85
- M1: 774eeb8
- M2 City: 755f0b0
- CLEAN regen: 91f903f
- This PHASE1 complete: see latest
