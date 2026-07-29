# Implementation checklist for Grok Build

## 1. Extract
Unzip `SoV_MapPack_PHASE1_COMPLETE_CLEAN.zip` into:
```
public/assets/pixel2d/maps/
```

## 2. Per-zone loader
```js
loadZone('scorched_highlands') // meta.json + atlases + layers
```

## 3. Atlas processing
- Key color: #FF00FF
- Slice cells; scale to 64×32 (tiles) / 64×64 (props)

## 4. Layers
- ground.json → tilemap walkable + edges + hazards
- collision.json → 0 walk / 1 block / 2 hazard (/ 3 portal city)
- props.json → place props by id+x+y
- spawns.json → enemies, chests, nodes, waypoints, portals, player_spawn

## 5. Hub rules (city_venekia)
- No combat enemies
- NPCs: quest_giver, blacksmith, merchant
- 4 portal pads to all Phase1 zones

## 6. Camera
bounds from maps/*/meta.json

## 7. Do not regenerate
Characters, HUD, skills, VFX from F1.1 stay as-is.
