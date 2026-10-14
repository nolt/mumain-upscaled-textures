# Textures kept original

*[Wersja polska](not-upscaled.pl.md)*

93 of the 7481 OZJ/OZT files of the client are not in this repository. The
client keeps using its own copies, so nothing is missing.

## Never upscale (55)

The client draws into these textures or reads them into buffers of a fixed size.
An upscaled copy garbles text or crashes the client.

- Canvases redrawn every frame (old UI text, guild mark):
  - `Data/Interface/FontInput.OZT`
  - `Data/Interface/guild.OZT`
- Terrain lighting (53 files), decoded into a fixed 256×256 buffer by a
  separate loader that does not read the scale marker:
  - `Data/World1/TerrainLight.OZJ`
  - `Data/World10/TerrainLight.OZJ`
  - `Data/World11/TerrainLight.OZJ`
  - `Data/World12/TerrainLight.OZJ`
  - `Data/World19/TerrainLight.OZJ`
  - `Data/World2/TerrainLight.OZJ`
  - `Data/World25/TerrainLight.OZJ`
  - `Data/World3/TerrainLight.OZJ`
  - `Data/World31/TerrainLight.OZJ`
  - `Data/World31/TerrainLight2.OZJ`
  - `Data/World31/terrainlighttest.ozj`
  - `Data/World31/terrainlighttest2.ozj`
  - `Data/World32/TerrainLight.OZJ`
  - `Data/World34/TerrainLight.OZJ`
  - `Data/World35/TerrainLight.OZJ`
  - `Data/World35/TerrainLight1.OZJ`
  - `Data/World35/TerrainLight2.OZJ`
  - `Data/World38/TerrainLight.OZJ`
  - `Data/World39/TerrainLight.OZJ`
  - `Data/World4/TerrainLight.OZJ`
  - `Data/World40/TerrainLight.OZJ`
  - `Data/World41/TerrainLight.OZJ`
  - `Data/World42/TerrainLight.OZJ`
  - `Data/World43/TerrainLight.OZJ`
  - `Data/World47/TerrainLight.OZJ`
  - `Data/World5/TerrainLight.OZJ`
  - `Data/World52/TerrainLight.OZJ`
  - `Data/world55/terrainlight.ozj`
  - `Data/world56/terrainlight.ozj`
  - `Data/World57/TerrainLight.OZJ`
  - `Data/World58/TerrainLight.OZJ`
  - `Data/World59/TerrainLight.OZJ`
  - `Data/World63/TerrainLight.OZJ`
  - `Data/World64/TerrainLight.OZJ`
  - `Data/World65/TerrainLight.OZJ`
  - `Data/World66/TerrainLight.OZJ`
  - `Data/World67/TerrainLight.OZJ`
  - `Data/World68/TerrainLight.OZJ`
  - `Data/World69/TerrainLight.OZJ`
  - `Data/World7/TerrainLight.OZJ`
  - `Data/World70/TerrainLight.OZJ`
  - `Data/World71/TerrainLight.OZJ`
  - `Data/World72/TerrainLight.OZJ`
  - `Data/World73/TerrainLight.OZJ`
  - `Data/World74/TerrainLight.OZJ`
  - `Data/World75/TerrainLight.OZJ`
  - `Data/World78/TerrainLight.OZJ`
  - `Data/World79/TerrainLight.OZJ`
  - `Data/World8/TerrainLight.OZJ`
  - `Data/World80/TerrainLight.OZJ`
  - `Data/World81/TerrainLight.OZJ`
  - `Data/World82/TerrainLight.OZJ`
  - `Data/World9/TerrainLight.OZJ`

## Too large (29)

The client loads textures up to 1024 px per side. These are already at or above
half of that, so not even ×2 fits.

- `Data/Effect/lavagiantBa_e.OZJ`
- `Data/Interface/InGameShop/Ingame_Shopback.OZJ`
- `Data/Monster/giantmemud_sc.OZJ`
- `Data/Monster/icewalker_sc.OZJ`
- `Data/Monster/serufan_sc.OZJ`
- `Data/Monster/strangerabbit_sc.OZJ`
- `Data/NPC/magicstore_sc.OZJ`
- `Data/Skill/null.OZJ`
- `Data/World1/mini_map.OZT`
- `Data/World11/mini_map.OZT`
- `Data/World2/mini_map.OZT`
- `Data/World3/mini_map.OZT`
- `Data/World32/mini_map.OZT`
- `Data/World34/mini_map.OZT`
- `Data/World35/mini_map.OZT`
- `Data/World38/mini_map.OZT`
- `Data/World39/mini_map.OZT`
- `Data/World4/mini_map.OZT`
- `Data/World42/mini_map.OZT`
- `Data/World5/mini_map.OZT`
- `Data/World52/mini_map.OZT`
- `Data/World57/mini_map.OZT`
- `Data/World58/mini_map.OZT`
- `Data/World64/mini_map.OZT`
- `Data/World78/bg_b_05.OZJ`
- `Data/World8/mini_map.OZT`
- `Data/World81/mini_map.OZT`
- `Data/World82/mini_map.OZT`
- `Data/World9/mini_map.OZT`

## TGA data in an OZJ file (8)

These files have the OZJ extension but hold TGA data. They are broken in the
original client too.

- `Data/Object34/ma_001.OZJ`
- `Data/Object34/Pool001.OZJ`
- `Data/Object35/cr1_shadow.OZJ`
- `Data/Object35/ma_001.OZJ`
- `Data/Object35/Pool001.OZJ`
- `Data/Object47/cage2.OZJ`
- `Data/object55/ma_001.ozj`
- `Data/object55/pool001.ozj`

## 24-bit TGA (1)

The upscaler handles only 32-bit OZT files.

- `Data/Monster/wolfa02.OZT`
