# Character Animation F2 — Warrior / Hunter / Mage

**Zip:** SoV_Anim_F2_WarriorHunterMage.zip  
**Drive:** https://drive.google.com/drive/folders/1JiKCX5zEypRHgscJ7roMqJhkNYJcH1G8

## Per class
```
warrior_base/atlas_warrior_base_anim.png + anim.json
hunter_base/atlas_hunter_base_anim.png + anim.json
mage_base/atlas_mage_base_anim.png + anim.json
atlas_skills_vfx_bases.png
```

## anim.json contract
- pivot feet (0.5, 1.0)
- idle 4f, walk 6f x 4 dirs, attack 4f, cast 5f
- hit_frame / vfx_frame for combat sync

## Build
```
public/assets/pixel2d/characters/{class}/
```
Slice sheet rows → play via AnimationController.
Production tip: re-grid in Aseprite for perfect frame sizes.
