# Seamless Tiles v1 (Master Prompt)

**Zip:** SoV_Tiles_Seamless_v1.zip  

## Rules baked in
- Single iso diamond per cell (2:1)
- Pure #FF00FF outside diamonds
- Floors 4×3, path indices **5–6**
- No text, no characters, no full scenes in a cell

## Biomes
scorched_highlands · whispering_jungle · city_venekia · cursed_coast · mines_of_robir · eternal_plains · crystal_peaks

## Build
```
public/assets/pixel2d/maps/{zone}/atlas_* + meta.json
```
Chroma key → slice by meta.atlas_layouts → id→index.
Pair with WIRED ground.json (path roles).
