# Upland Trove Data

Community data for the **Smart Address Clipboard (for Upland)** Chrome extension: which troves each
service structure gives, which recipes exist, and which plants give troves.

This project is independent and not affiliated with Uplandme, Inc. Use at your own risk.

## Files

| File | Content |
|---|---|
| `manifest.json` | Data version, date, counts and a SHA-256 for each file. The extension reads this small file first and downloads the others only when the version changed. |
| `troves.json` | All troves with their category, the structures and plants where they can be found, and the recipes that make them. |
| `buildings.json` | Buildings as named in the game: group, game type number (`modelId`) when known, troves, recipes crafted there. |
| `recipes.json` | Recipes with ingredients and quantities, and where they are crafted. A product can have two variants (`product-1`, `product-2`). |
| `plants.json` | Plant species that give troves. Species not listed give none yet. |

## Notes on the data
- `group`: buildings that give exactly the same troves and recipes share a group id (G001...).
- `verified: true`: the in-game page of this building was read and matches the listed troves.
- `status: pending`: building not read yet (for example still under construction). `no-troves`: housing and Metaventures.
- No personal data: no owner names, no addresses, no inventories.
- Drop probabilities are not included.

## Updates
The data is refreshed by its maintainer whenever new buildings or troves are released. See `dataVersion` and `generatedAt` in `manifest.json`.
