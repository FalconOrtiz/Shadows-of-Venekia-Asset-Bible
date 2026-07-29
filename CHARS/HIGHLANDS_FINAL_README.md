# Highlands Characters FINAL — Step 1

**Status:** HIGHLANDS_CHARS_READY (review)  
**Zip:** SoV_Highlands_Characters_FINAL.zip  
**Drive folder:** https://drive.google.com/drive/folders/1JiKCX5zEypRHgscJ7roMqJhkNYJcH1G8

## Classes
- warrior — iron plate, crimson, sword+shield
- hunter — leather hood longbow
- mage — violet robes crystal staff

## Runtime
```
public/assets/graphics/characters/{class}/atlas.webp
public/assets/graphics/characters/{class}/anim.json
public/assets/graphics/ui/portraits/bases/char_{class}_base.webp
```

## anim.json
frame_w 128 · frame_h 160 · pivot 0.5/1.0 · dir_order S,E,W,N  
rows: idle6 · walk S/E/W/N ×8 · attack6 hit_frame=3 · cast6 vfx_frame=2 · hit3 · death6

## §B0
1 Opaque body · 2 Four-dir walk · 3 Weapon motion — see pack 00_docs/ACCEPTANCE_B0.md

Tiles/mobs NOT started (await character accept).
