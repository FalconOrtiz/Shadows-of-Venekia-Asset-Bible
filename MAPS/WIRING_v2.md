# Map WIRING v2 — Why maps looked terrible & how Build must load them

## Root cause
Previous `ground.json` demos filled every cell with **random floor variants** and sprinkled hazards with `(x+y) % N`. Build rendered noise. Atlases also lacked a hard slice contract.

## Download (USE THIS)
**SoV_MapPack_PHASE1_WIRED_v2.zip**  
https://drive.google.com/file/d/1DPAxwp8tNYYQ-d2Wu7cuKiG4bocMg6Xt/view?usp=drivesdk  

Alt: SoV_MapPack_WIRED_v2.zip → https://drive.google.com/file/d/1wnGTcLJxanidhNzUkdjynyOs86z1gWol/view  
PHASE2 redesigned plains/peaks: https://drive.google.com/file/d/1_DG-yAH-ClWGSCJNEZKeVYbp2W-To1dF/view  

Folder: https://drive.google.com/drive/folders/1JiKCX5zEypRHgscJ7roMqJhkNYJcH1G8

## Designed layout rules (now in ground.json)
1. **Regions** — large rectangles of ONE floor id (not checker noise)
2. **Paths** — continuous road from player_spawn → waypoint → portals
3. **Hazard pools** — blobs only (lava/toxic), not every 17th tile
4. **Transitions** — only near portal approaches
5. **Edges/cliffs** — border only

## Build pipeline (mandatory)
```
1. Load zone/meta.json
2. Slice each atlas_*.png with chroma #FF00FF
   - index 0 = top-left, row-major
   - use atlas_layouts {cols,rows,cell_w,cell_h,padding}
3. Map tiles[].id → {atlas, index, walk}
4. ground.tiles[y][x] = id → draw THAT frame only
5. collision: 0 walk / 1 block / 2 hazard / 3 portal
6. props.json + spawns.json same grid
7. Iso: screenX=(x-y)*32, screenY=(x+y)*16  (64x32 tiles)
```

## DO NOT
- Random floor frames
- Treat whole atlas as one sprite
- Ignore meta.tiles index
- Use old M0/M1 random ground.json

## Per-zone files
```
{zone}/meta.json
{zone}/atlas_*.png
{zone}/maps/{zone}_demo/layers/ground.json
{zone}/maps/{zone}_demo/layers/collision.json
{zone}/maps/{zone}_demo/layers/props.json
{zone}/maps/{zone}_demo/layers/spawns.json
WIRING.json
```
