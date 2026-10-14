# Tekstury pozostawione w oryginale

*[English version](not-upscaled.md)*

93 z 7481 plików OZJ/OZT klienta nie ma w tym repozytorium. Klient dalej używa
własnych kopii, więc niczego nie brakuje.

## Nigdy nie powiększać (55)

Klient rysuje po tych teksturach albo wczytuje je do buforów o stałym rozmiarze.
Powiększona kopia psuje tekst albo wywraca klienta.

- Płótna rysowane co klatkę (tekst starego UI, herb gildii):
  - `Data/Interface/FontInput.OZT`
  - `Data/Interface/guild.OZT`
- Oświetlenie terenu (53 plików), dekodowane do bufora 256×256 przez osobny
  loader, który nie czyta znacznika skali:
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

## Za duże (29)

Klient wczytuje tekstury do 1024 px na bok. Te mają już co najmniej połowę tego,
więc nie zmieści się nawet ×2.

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

## Dane TGA w pliku OZJ (8)

Te pliki mają rozszerzenie OZJ, ale zawierają dane TGA. W oryginalnym kliencie
też są uszkodzone.

- `Data/Object34/ma_001.OZJ`
- `Data/Object34/Pool001.OZJ`
- `Data/Object35/cr1_shadow.OZJ`
- `Data/Object35/ma_001.OZJ`
- `Data/Object35/Pool001.OZJ`
- `Data/Object47/cage2.OZJ`
- `Data/object55/ma_001.ozj`
- `Data/object55/pool001.ozj`

## TGA 24-bitowe (1)

Program do powiększania obsługuje tylko 32-bitowe pliki OZT.

- `Data/Monster/wolfa02.OZT`
