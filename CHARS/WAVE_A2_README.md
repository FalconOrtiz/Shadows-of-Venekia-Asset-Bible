# Wave A.2 — Individual PNG Frames

**Zip:** [SoV_WaveA2_IndividualFrames.zip](https://drive.google.com/file/d/REPLACE/view)  
**Folder:** https://drive.google.com/drive/folders/1JiKCX5zEypRHgscJ7roMqJhkNYJcH1G8

## Goal
Eliminate manual atlas slicing. One file per frame.

## Naming
`Class_State_Dir_Frame##.png`  
Example: `Warrior_Walk_S_01.png`

## Ready now
| Set | Frames |
|-----|--------|
| warrior_base | idle S/E, walk S×3 + E, attack S, cast S |
| hunter_base | idle S, walk S×2, attack S, cast S |
| mage_base | idle S, walk S×2, attack S, cast S |
| Celestial Vanguard | idle, walk, cast S |
| Eagle Eye Legend | idle, walk S |
| Primordial Mage | idle, cast S |
| Highlands tiles | base×4, path×2, cliff N, lava |

## Build path
```
public/assets/pixel2d/characters/{class}/frames + anim.json
public/assets/pixel2d/maps/scorched_highlands/tiles/
```

## Missing (next)
- Full 6-frame walk × 4 dirs all bases
- W/N dirs
- hit/death
- individual tiles other biomes
