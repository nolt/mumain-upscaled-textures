# MuMain Upscaled Textures

*[English version](README.md)*

Powiększone tekstury dla klienta gry [MuMain](https://github.com/sven-n/MuMain):
7388 plików OZJ/OZT z katalogu `Data/` klienta, z tego 7271 w skali ×4 i 117 w skali ×2.
Obejmują świat, potwory, postacie, przedmioty, efekty i interfejs. Repozytorium jest
nakładką: zawiera tylko powiększone pliki, a całą resztę klient bierze z własnych kopii.

![Oryginał (z lewej) i wersja powiększona (z prawej), ten sam fragment tekstury](docs/assets/comparison.jpg)

*Z lewej oryginalna tekstura, powiększona bez wygładzania. Z prawej plik powiększony.*

## Wymagania

Klient musi rozpoznawać znacznik skali w tych plikach (MuMain PR 718) i obsługiwać
paczki tekstur w `Data/TexturePacks/` (MuMain PR 763). Klient bez znacznika rysuje
każdą teksturę kilka razy za dużą. Klient ze znacznikiem, ale bez paczek tekstur
pomija tę paczkę; do niego służy wydanie v1.0, którego pliki nadpisują te w `Data/`.

Tekstury powstały z oryginalnych plików gry z katalogu `Data/` w MuMain. Tekstury
świata, modeli i efektów nie zależą od interfejsu. Tekstury z `Interface/` rysują
oba motywy RmlUi (`legacy` korzysta z większości, `modern` z mniejszej części)
oraz te części interfejsu, których jeszcze nie przeniesiono do RmlUi.

## Instalacja

1. Pobierz archiwum z [Releases](../../releases) albo sklonuj repozytorium.
2. Skopiuj jego katalog `Data/` do katalogu klienta, obok `Main` / `Main.exe`.
   Tekstury trafiają do `Data/TexturePacks/Upscaled/` i żaden oryginalny plik nie
   jest nadpisywany.
3. W opcjach gry, w zakładce **Interface**, wybierz `Upscaled` w polu
   **Texture Pack** (w polskim interfejsie **Paczka tekstur**) i uruchom grę ponownie.

Żeby wrócić do oryginalnych tekstur, wybierz tam **Original** (po polsku **Oryginalne**)
i uruchom grę ponownie.
Potem folder można usunąć.

Powiększone pliki zajmują około 2,8 GB na dysku i potrzebują odpowiednio więcej
pamięci karty graficznej niż oryginały.

## Jak to działa

Pierwsze cztery bajty nagłówka OZJ i OZT nie są używane przez klienta. Tutaj
zapisany jest w nich znacznik `M` `U` `X` i skala (2 albo 4). Klient, który zna
znacznik, wgrywa cały obraz, ale jako rozmiar tekstury przyjmuje rozmiar oryginału,
więc teren, modele i układ interfejsu zostają bez zmian. Powiększone tekstury
dostają też mipmapy i filtrowanie trójliniowe, dzięki czemu szczegóły nie migoczą
z daleka.

Dla każdej tekstury klient czyta kopię z aktywnej paczki, jeśli istnieje, a w przeciwnym
razie oryginał z `Data/`. Pliki bez znacznika ładują się jak dotąd, więc oryginały
i pliki powiększone można dowolnie mieszać, na przykład zostawić oryginalny interfejs,
usuwając `Data/TexturePacks/Upscaled/Interface/`.

## Czego nie powiększono

93 pliki zostały w oryginale: płótna, po których klient rysuje, oświetlenie terenu,
pliki za duże na limit klienta 1024 px oraz pliki, których program do powiększania
nie potrafi odczytać. Pełna lista z powodami jest w
[docs/not-upscaled.pl.md](docs/not-upscaled.pl.md).

## Jak powstały tekstury

Każdy plik został zdekodowany, powiększony modelem ESRGAN i zapisany z powrotem
w oryginalnym formacie, z dodanym znacznikiem:

- **Świat, modele, efekty, przedmioty** (6406 plików): `4x-UltraSharp`, autor Kim2091.
- **Interfejs** (`Interface`, `Logo`, `Local`, `InGameShopBanner`, 982 pliki):
  `4x_foolhardy_Remacri`, autor FoolhardyVEVO.

Pliki, które w skali ×4 przekroczyłyby 1024 px, powiększono ×2.

## Licencja

Oryginalne tekstury są częścią klienta MU Online firmy Webzen. Te pliki są z nich
wywiedzione i nie są open source. Oba modele są na licencji CC BY-NC-SA 4.0, więc
bez użytku komercyjnego. Szczegóły w pliku [NOTICE](NOTICE).

Autor oryginalny: [Nolt](https://github.com/nolt).
