# SoV Map Packs

## M0 – Scorched Highlands ✅

**Zip Drive:** https://drive.google.com/file/d/ (see folder) `SoV_MapPack_M0_Highlands.zip`

### Atlases
- `atlas_highlands_floors.png` — 12 floors 64×32 iso
- `atlas_highlands_edges.png` — 8 cliffs
- `atlas_highlands_transitions_hazards.png` — 4 trans + 3 hazards
- `atlas_highlands_props.png` — 12 props 64×64
- `atlas_highlands_master.png`
- `atlas_highlands_collision_ref.png` — green=walk red=block orange=hazard

### Demo map 40×30
`maps/scorched_highlands_demo/`
- meta.json (spawn, portals, bounds)
- layers/ground.json
- layers/collision.json (0 walk / 1 block / 2 hazard)
- layers/props.json
- layers/spawns.json (5 enemies, chest, mining, waypoint)

### Hand-off Build
```
public/assets/pixel2d/maps/scorched_highlands/
  atlas_*.png
  meta.json
  maps/scorched_highlands_demo/
```
Loader → tilemap layers → collision → spawns → camera clamp

### Next
- M1 Whispering Jungle
- M2 City of Venekia
