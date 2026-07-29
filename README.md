# Shadows of Venekia – Asset Bible

## ⚠️ MAPS — use WIRED v2 (not old random demos)

| Pack | Link | Notes |
|------|------|-------|
| **PHASE1 WIRED v2** | [download](https://drive.google.com/file/d/1DPAxwp8tNYYQ-d2Wu7cuKiG4bocMg6Xt/view) | **Use in Build** — designed layouts + wiring |
| PHASE2 layouts | [download](https://drive.google.com/file/d/1_DG-yAH-ClWGSCJNEZKeVYbp2W-To1dF/view) | Plains/Peaks redesigned |
| F1.1 chars/UI | [download](https://drive.google.com/file/d/1NKI7fwlIQcjxMU8Z6WRw_dkwMbxNIL5u/view) | 35 assets |

**Docs:** [MAPS/WIRING_v2.md](MAPS/WIRING_v2.md)

### Why old maps looked broken
`ground.json` was random tile noise. WIRED v2 uses regions + paths + hazard pools + `meta.tiles[].index` contract.

### Build drop
```
public/assets/pixel2d/maps/{zone}/
```
Chroma `#FF00FF` · resolve tile id → atlas index · never random frames.

Drive folder: https://drive.google.com/drive/folders/1JiKCX5zEypRHgscJ7roMqJhkNYJcH1G8
