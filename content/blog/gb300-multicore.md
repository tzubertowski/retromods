---
title: "GB300 - Port Multicore, przyśpieszenie/polepszenie jakości emulacji"
description: "Kompilacja nowych wersji emulatorów, znaczące przyśpieszenie emulacji SNES/GBA"
image: "images/post/gb300-multicore/multicore_gb300.jpg"
date: 2024-04-28T11:56:47+06:00
draft: false
author: "Prosty"
tags: ["gb300", "sf2000", "multicore", "gpsp", "dynarec", "cfw"]
categories: ["Retro Handhelds"]
---
## Wstep
Pragnę przyśpieszyć tego posta dla osób zainteresowanych. Wraz z użytkownikami discorda [Retro Handhelds](https://discord.com/invite/retrohandhelds) przeportowaliśmy modyfikację oprogramowania Mutlicore z SF2000 na GB300.
Jeżeli wiesz co i jak, zostawiam linki. Jeżeli nie wiesz - czytaj dalej

Multicore dla GB300:
- [Na moim repozytorium github](https://github.com/tzubertowski/gb300_multicore/releases)

## Instalacja Multicore na GB300
### Co to multicore?
Multicore to modyfikacja orginalnego oprogramowania GB300 (oraz SF2000) która umożliwia nam włączanie własnych emulatorów. W moim buildzie multicore dla GB300 dołączonych jest wiele zaktualizowanych emulatorów, znaczna część z nich przekompikowana do najnowszych (często szybszych) wersji wraz z ulepszeniami prędkości emulacji. Eg. emulator GBA teraz wspiera dynamiczną rekompilację, przez to **znaczna** część gier na GBA jest grywalna w pełnej prędkości.

### Jak zainstalować Multicore na GB300
#### Kroki
Proces ten jest stosunkowo prosty, będzie składał się on z kilku kroków
- naprawa błędu bootloadera (opcjonalne, ale mocno rekomendowane)
- backup orginalnej karty pamięci (opcjonalne, ale mocno rekomendowane)
- instalacja multicore
- instrukcja obsługi (opcjonalne, ale mocno rekomendowane)

#### 1. Naprawa błędu bootloadera
GB300, tak jak jego starszy brat SF2000, cierpią na błąd w bootloaderze który sprawia że często po zmianie plików systemu na karcie pamięci nie możemy ponownie włączyć konsoli. Aby go naprawic:

- ściągamy [tadpole](https://github.com/EricGoldsteinNz/tadpole/releases)
- podłączamy kartę pamieci z GB3000 do PC
- włączamy tadpole
- z menu kontekstowego wybieramy bootloader fix

![Bootloader fix](/blog/images/gb300-multicore/install-step1.jpg)

- dalej kieruj się sugestiami tadpole aż do samego końca

#### 2. Backup orginalnej karty pamięci
Tu nie ma kombinowania, wystarczy zgrać całą zawartość karty pamięci GB300 na dysk. 

**UWAGA** jeżeli tego nie zrobicie i będziecie musieli formatować kartę SD stracicie wszystkie romy, które dostaliście razem z GB300.

#### 3. Instalacja multicore
- ściągamy [gb300 multicre](https://github.com/tzubertowski/gb300_multicore/releases)
- rozpakowujemy zawartość archiwum bezpośrednio do głownego folderu karty pamięci GB300
![Multicore GB300 7z](/blog/images/gb300-multicore/install-step3.jpg)


I to by było na tyle w kontekście samej instalacji Multicore. Włóż kartę pamięci do GB300, włącz ją i upewnij się, że wszystko działa.

### Szybka instrukcja ubsługi Multicore
#### 1. Struktura folderów
Multicore ładuje emulator na podstawie folderu, do którego wrzucisz roma na karcie pamięci. Wrzucamy roma z danej konsoli do folderu 

> GB3000/roms/NAZWA_EMULATORA

Eg. romy wrzucone do folderu:
```
GB300/roms/gba
```
Odpalą nam się przez emulator GBA (GPSP) z listy poniżej.


Romy wrzucone do folderu:
```
GB300/roms/wswan
```
Odpalą nam się przez emulator Wonderswan.

Na dole artykułu zamieszczam pełną listę nazw folderów, wraz z emulatorem który jest za nie odpowiedzialny. 


#### 2. Inicjalizacja romów
Po wrzuceniu swoich romów do odpowiedniego folderu musimy jeszcze odpalić mały skrypt (każdorazowo wrzucając nowego roma), na karcie pamięci znajduje się

```
make-romlist.bat //dla windowsa
make-romlist.sh //dla linuxa/windowsa11
```

Po prostu odpalamy odpowiedni dla nas plik. Po tym jesteśmy już gotowi na odpalenie swoich romów przy użyciu zaktualizowanych corów przez multicore : )


#### 3. Na przykładzie gry - Pokemon FireRed
Na przykładzie gry którą posiadam - Pokemonów FireRed
![Pokemon FireRed](/blog/images/gb300-multicore/pokemonred.jpg)
- roma wrzucam na kartę pamięci do folderu roms/GBA
![Lokacja na karcie](/blog/images/gb300-multicore/pokemonred-step1.jpg)
- z głównego folderu karty pamięci GB300 odpalam skrypt
![Skrypt](/blog/images/gb300-multicore/pokemonred-step2.jpg)
- po jego zakonczeniu zamykam okno/naciskam jakikolwiek przycisk
![Skrypt](/blog/images/gb300-multicore/pokemonred-step3.jpg)
- wyjmuję kartę pamięci, wkładam do GB300 i włączam konsolę
- nawiguję do menu "ROMS", lokalizuję swojego roma (teraz nazwany gba;Nazwagry.gba)
![Skrypt](/blog/images/gb300-multicore/pokemonred-step3.5.jpg)

- włączam grę przyciskiem A

Naszym oczom początkowo ukaże się menu ładowania emulatora i roma
![Skrypt](/blog/images/gb300-multicore/pokemonred-step4.jpg)
po czym gra wystartuje - tym razem w pełni prędkości dzięki multicore :)
![Skrypt](/blog/images/gb300-multicore/pokemonred-step5.jpg)

## Pełna lista emulatorów w Multicore wraz z nazwami folderów
Emulatory konsol które dołączonej są w tej paczce:
- amstradb (cap32)
- m2k (mame2000)
- a26 (stella2014)
- a5200 (a5200)
- a78 (prosystem)
- a800 (atari800lib)
- lnx (handy)
- wswan (beetle-swan)
- chip8
- col (gearcol)
- fcf (FreeChaF)
- retro8
- vapor (vaporspec)
- gong
- outrun
- wolf3d
- prboom
- flashback (REminiscence)
- xrick
- gw
- cdg (pocketcdg)
- int (FreeIntv)
- msx (blueMSX)
- gme
- pce (beetle-pce)
- ngpc (RACE)
- gba (gpsp z modyfikacją dynarec)
- gbb (gambatte)
- gbgb (gearboy)
- gb (tgbdual)
- nes (fceumm)
- nesq (QuickNES)
- pokem (PokeMini)
- snes02 (snes9x2002)
- snes (snes9x2005)
- sega (picodrive; megadrive)
- gg (Gearsystem)
- zx81 (81)
- spec (fuse)
- thom (theodore)
- vec (vecx)
- wsv (potator)
- amstrad (crocods)
- arduboy (arduous)
- lnxb (beetle-lynx)
- c64sc (vice)
- c64 (vice)
- vic20 (xvic)
- fake08
- lowres-nx
- jnb
- cavestory (port)
- o2em
- pcesgx (beetle-supergrafx)
- pc8800 (quasi88)
- pcfx (beetle-pcfx)
- gbav (vba-next)
- mgba
- nest (nestopia)
- vb (beetle-vb)
- gpgx (Genesis-Plus-GX)
- xmil
- quake (port)