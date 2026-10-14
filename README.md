# MuMain Upscaled Textures

*[Wersja polska](Readme.pl.md)*

Upscaled textures for the [MuMain](https://github.com/sven-n/MuMain) game client:
7388 OZJ/OZT files from the client's `Data/` folder, 7271 of them at ×4 and 117 at ×2.
They cover the world, monsters, players, items, effects and the UI. The repository is
an overlay: it holds only the upscaled files, and the client keeps using its own
copies of everything else.

![Original (left) and upscaled (right), same area of each texture](docs/assets/comparison.jpg)

*Left: the original texture, enlarged with no smoothing. Right: the upscaled file.*

## Requirements

The client has to recognise the scale marker in these files. Support for it was
proposed to MuMain in PR 718. A client without it draws every texture several
times too large.

The textures are made from the original game files in MuMain's `Data/` folder.
World, model and effect textures do not depend on the UI. The `Interface/`
textures are drawn by both RmlUi themes (`legacy` uses most of them, `modern` fewer)
and by the parts of the UI not yet moved to RmlUi.

## Installing

1. Download the archive from [Releases](../../releases), or clone the repository.
2. Copy its `Data/` folder into the client folder, next to `Main` / `Main.exe`, and
   let it overwrite the existing files.

To go back, restore the original files from your client package or from
`src/bin/Data` in the MuMain repository.

The upscaled files take about 2.8 GB on disk and need correspondingly more video
memory than the originals.

## How it works

The first four bytes of an OZJ or OZT header are unused by the client. Here they
hold the marker `M` `U` `X` followed by the scale (2 or 4). A client that knows the
marker uploads the full image but keeps the original size as the texture size, so
terrain, models and UI layouts stay as they were. The upscaled textures also get
mipmaps and trilinear filtering, so their detail does not shimmer at a distance.

Files without the marker load as before, so original and upscaled files can be
mixed freely, for example to upscale only the world and keep the original UI.

## What is not upscaled

93 files stay original: canvases the client draws into, terrain lighting, files
too large for the client's 1024 px limit and files the upscaler cannot read.
The full list with reasons is in [docs/not-upscaled.md](docs/not-upscaled.md).

## How the textures were made

Each file was decoded, upscaled with an ESRGAN model and written back in its
original format, with the marker added:

- **World, models, effects, items** (6406 files): `4x-UltraSharp` by Kim2091.
- **UI** (`Interface`, `Logo`, `Local`, `InGameShopBanner`, 982 files):
  `4x_foolhardy_Remacri` by FoolhardyVEVO.

Files that would exceed 1024 px at ×4 were upscaled ×2 instead.

## License

The original textures are part of the MU Online client by Webzen. These files are
derived from them and are not open source. Both upscaling models are licensed
under CC BY-NC-SA 4.0, so no commercial use. Details in [NOTICE](NOTICE).

Original author: [Nolt](https://github.com/nolt).
