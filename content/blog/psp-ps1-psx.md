---
title: "Gry z PS1 na PSP"
description: "PS1 na PSP poradnik"
image: "images/post/psp-psx/bg-top.jpg"
date: 2022-05-23T16:56:47+06:00
draft: false
author: "Prosty"
tags: ["PSP", "PSX2PSP", "PSP PS1", "PSP CFW", "PSP PSX"]
categories: ["PSP"]
---

### 1. PS1 na PSP, jak to możliwe?
Większość z nas, fanów retro, zdaje sobie sprawę z możliwości gry w tytuły z Playstation 1 na Playstation Portable. Niewielu natomiast zastanawia się - jak to możliwe.

PSP w początkowych wersjach softu nie umożliwiało gry w tytuły z Playstation 1. Możliwość ta została dodana po wielu miesiącach w momencie, gdy Sony zaczęło wydawać elektroniczne wersje klasyków na Playstation Store. Łatwo więc można stwierdzić, że to emulacja softowa i koniec tematu. Ale to tylko półprawda.

Wiele z urządzeń dedykowanych retro, jak BittBoy, Powkiddy v90 etc., pomimo o niebo lepszej specyfikacji technicznej (PSP 333 MHz vs BittBoy 1.5 Ghz) nie radzi sobie z emulacją Playstation 1. Tymczasem emulacja na PSP jest praktycznie idealna (do wydania Duckstation emulator PS1 na PSP był jednym z najbardziej kompatybilnych emulatorów na rynku). Jak dokonało tego Sony kilkanaście lat temu, na o niebo gorszym sprzęcie?

Ano, PSP nie emuluje w pełni Playstation 1. Część architektury procesora PSP pokrywa się z architekturą procesora Playustation 1. Dzięki temu tłumaczenie instrukcji (emulacja) nie musi przebiegać w pełni. Znaczna część instrukcji CPU/GPU działa jak na Playstation 1.
Ponadto Sony, jako jedyne, posiada specyfikację techniczną zarówno Playstation 1 jak i PSP. Dzięki temu programiści pracujący nad tym projektem nie musieli domyślać się działania PS1, spędzać dni na poprawce i implementacji niedziałających aspektów emulacji. Zamiast tego, mogli skupić się na optymalizacji.

### 2. Skąd kupić gry PS1 na PSP? (Bez potrzeby CFW)
Dalej mamy możliwość kupna gier PS1 poprzez Playstation Store. Niestety, nie mamy możliwościa ściągnięcia takich poprzez Playstation Store na PSP. Store od wielu już lat nie działa na PSP z racji kosztów utrzymania i bezpieczeństwa.

Jedynym oficjalnym sposobem wrzucenia gier kupionych z Playstation Store na PSP jest:
- ściągnięcie ich na PS3 przez Playstation Store
- przesłanie ich z PS3 na PSP kablem USB

Niestety, wymaga to posiadania PS3. Ponadto znaczna część tytułów z PS1 nie jest dostępna na Playstation Store.


### 3. Co należy mieć aby pograć w dowolną grę z PS1 na PSP? (bez potrzeby posiadania PS3 ;) )
#### 3.1. Przerobione PSP / CFW
Aby tego dokonać musimy wpierw posiadać PSP z CFW (custom firmware). Jak przerobić dowolne PSP i zainstalowac najnowsze/najstabilniejsze? Wysyłam do polecanego przeze mnie [poradnika na Youtube](https://youtu.be/h-pZeWV5Q8E).

#### 3.2. PSX2PSP
PSX2PSP to aplikacja pozwalająca nam przerobić każdą grę z PS1 na EBOOT - plik akceptowany przez PSP. Proces ten wykorzystuje wspomniany poprzednio emulator PS1 który stworzyło Sony.

Aplikację tą [pobieramy ze strony oficjalnej](https://psp.brewology.com/downloads/get.php?id=9697). Na [tej stronie](https://www.cfwaifu.com/psx2psp/) opisany jest też sposób użycia tej aplikacji. Ale poniżej także go zamieszczę.

#### 3.3. Obraz gry z Playstation 1
W moim przypadku przerabiać będę jedną z moich ukochanych gier na PS1 - Digimon World. Musimy zdobyć obaz w formacie ISO, PBP lub BIN/CUE naszej płytki. 

Mamy na to kilka opcji:
- Zrzucenie posiadanej przez nas płytki gry. Jak tego dokonać? Polecam [poradnik z wiki gametech](https://emulation.gametechwiki.com/index.php/Ripping_games#Sony_PlayStation_1.2F2).
- Zdobycie ISO w inny sposób, eg. poprzez ściągniecie ISO/PBP ze sklepu Sony lub innego źródła 🏴‍☠️

### 4. Przerabianie gry PS1 na PSP.
#### 4.1. Podstawowa przeróbka obrazu gry PS1
<p align="center">
  <img alt="PSX2PSP struktura folderów" width="1000" src="/post/psx-psp/foldery-2.jpg" />
</p>

- Rozpakowujemy poprzednio sćiągnięte PSX2PSP, zapamiętujemy gdzie umieściliśmy obraz naszej gry PS1.
- Nawigujemy do rozpakowanego folderu.
- Odpalamy PSX2PSP.exe


<p align="center">
  <img alt="PSX2PSP struktura folderów" width="500" src="/post/psx-psp/psxpsp-1.jpg" />
</p>

- Klikamy w "Convert menu" aby wyświetlić opcje przeróbki

<p align="center">
  <img alt="PSX2PSP struktura folderów" width="500" src="/post/psx-psp/psxpsp-2.jpg" />
</p>

- W polu nr. 1 wybieramy nasze ISO/PBP lub plik bin
- Program automatycznie powinien zgadnąć nazwę gry, jeżeli nie to wypełniamy pozostałe okienka. Poniżej przykład mojej gry.

<p align="center">
  <img alt="PSX2PSP struktura folderów" width="500" src="/post/psx-psp/psxpsp-3.jpg" />
</p>

#### 4.2. Opcjonalne: ikona, tło w menu, etc.
Opcjonalnie możemy dodać obrazek/ikonę gry, tło, muzykę etc.

<p align="center">
  <img alt="PSX2PSP struktura folderów" width="500" src="/post/psx-psp/psxpsp-4.jpg" />
</p>
- W tym celu klikamy w Customize PBP

<p align="center">
  <img alt="PSX2PSP struktura folderów" width="500" src="/post/psx-psp/psxpsp-5.jpg" />
</p>
- W moim przypadku dodawać będę tylko ikonę gry, ale zachęcam do zabawy pozostałymi opcjami

#### 4.3. Przerobienie obrazu do EBOOT
Pozostało nam już tylko stworzyć plik EBOOT.

<p align="center">
  <img alt="PSX2PSP struktura folderów" width="500" src="/post/psx-psp/psxpsp-6.jpg" />
</p>

- Klikamy na "convert"
- Gotowy folder z grą znajdziemy w folderze zaznaczonym na screenie pod nr. 2. 

<p align="center">
  <img alt="PSX2PSP struktura folderów" width="1000" src="/post/psx-psp/foldery-3.jpg" />
</p>

Folder będzie posiadał nazwę z nr. gry. W przypadku Digimon World - SLUS01032. Możemy zmienić nazwę folderu, to nie ma znaczenia. Ja nazwę swój - "DIGIMON-WORLD-PSX" w celu łatwiejszego odnalezienia w przyszłości.

#### 4.4. Wrzucenie przerobionej gry na PSP
<p align="center">
  <img alt="PSX2PSP struktura folderów" width="1000" src="/post/psx-psp/foldery-4.jpg" />
</p>
Aby zainstalować przerobioną grę po prostu umieszczamy ją na karcie pamięci PSP w folderze PSP/GAME.

- Wkładamy kartę do PSP
- Odpalamy konsolę i szukamy nowej pozycji w menu
- Gramy w Digimon World przez kolejne 13 godzin bez jedzenia, picia i rozmowy