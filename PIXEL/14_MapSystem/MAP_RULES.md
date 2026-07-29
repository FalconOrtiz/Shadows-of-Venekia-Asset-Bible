# MAP SYSTEM – Non-Repeating Traversal Rules
Shadows of Venekia Pixel · Task Bar Hero Style

## Goal
Player can walk the entire world + dungeons for minutes without seeing the same 3–4 tiles looped.

## Implementation (recommended for Grok Build / Canvas 2D)

### 1. Tileset Design (already generated)
- **Phase 1** (`Pixel_Tileset_Phase1_Modular.jpg`):  
  Scorched Highlands (12 variants), Whispering Jungle (12), Cursed Coast (10), Mines of Robir (10) + transitions
- **Phase 2 + City** (`Pixel_Tileset_Phase2_City.jpg`):  
  Eternal Plains (8), Crystal Peaks (8), City streets (12), House of Orders plaza
- **Dungeons** (`Pixel_Dungeon_Tilesets.jpg`):  
  4 full dungeon sets with floor / wall / corner / door / trap / hazard pieces

### 2. Runtime Rules (code-side)

```js
// Pseudo
const RECENT = new Set() // last 6 placed tile IDs
const BIOME_WEIGHTS = { highland: 1.0, jungle: 1.0, ... }

function pickTile(biome, x, y, neighbors) {
  let candidates = tileset[biome].filter(t => !RECENT.has(t.id))
  // prefer autotile match with neighbors
  candidates = candidates.filter(t => matchesWang(t, neighbors))
  if (candidates.length === 0) candidates = tileset[biome] // fallback
  const chosen = weightedRandom(candidates)
  RECENT.add(chosen.id)
  if (RECENT.size > 6) RECENT.delete(RECENT.values().next().value)
  return chosen
}
```

### 3. Biome Transition
- Use dedicated transition tiles (already in Phase1 pack)
- 8–16 tile wide corridors between zones
- Never hard-cut biomes

### 4. Dungeon Room Generation
- Modular pieces: floor_A-H, wall_N/E/S/W, corner, door, trap, hazard
- Room templates (3–5 layouts) + random fill from piece pool
- Guaranteed unique combination of last 4 rooms

### 5. Seed
- World seed = player account + act
- Same seed = same map for multiplayer sync
- Different seed = completely different feel

### 6. LOD / Performance
- 32×32 or 48×48 base
- Atlas all tiles into one or two spritesheets
- Canvas 2D drawImage with batching

## Files
- `05_Zones_Tilesets/Phase1/Pixel_Tileset_Phase1_Modular.jpg`
- `05_Zones_Tilesets/Phase2/Pixel_Tileset_Phase2_City.jpg`
- `06_Dungeons/Pixel_Dungeon_Tilesets.jpg`

Slice these into individual tiles (or use as reference sheets for more variants).