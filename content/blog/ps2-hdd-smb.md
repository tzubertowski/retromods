---
title: "PS2 - granie bez użycia DVD"
description: "meta description"
image: "images/post/ps2-opl/bg.jpg"
date: 2022-03-29T12:56:47+06:00
draft: false
author: "Prosty"
tags: ["Diy", "PS2", "OPL", "HDD", "SMB", "USB", "network adapter"]
categories: ["PS2"]
---
Jeżeli jesteście posiadaczami PS2 to zapewne spotkaliście się z problemem, gdy konsola nie czyta niektórych (lub wszystkich) płyt. Zazwyczaj zaczyna się to od zaprzestania czytania płyt CD, szczególnie gier z PS1.
Niestety, ale projekt lasera który został użyty w PS2 nie wytrzymał próby czasu. Lasery PS2 prędzej czy później przestają działać, a wymiana ich na nieoficjalne kopie to walka z wiatrakami. Prędzej czy później twoje PS2 przestanie czytać płyty.

### 1. Czy na każdym PS2 da się grać bez płyt?
Aby grac w nasze kopie gier, musimy posiadać przerobione PS2. 

Od kilku lat każde jedno PS2 jest modyfikowalne softowo - bez użycia chipa. Najczęściej spotykaną metodą takiej przeróbki jest FreeMcBoot (FreeHddBoot dla PS2 fat z HDD). Mitem jest, jakoby modele PS2 Slim 9000 nie wspierały takowej przeróbki, od wielu lat bowiem FunTuna pozwala nam na odpalenie FreeMcBoot.

Co daje nam taka przeróbka softowa? Pozwala nam na odpalanie programów homebrew - tworzonych przez społeczność fanów PS2. Najbardziej znanym programem tego typu jest **OPL - Open PS2 Loader**.

### 2. W jaki sposób odpalimy gry bez DVD na OPL?
OPL umożliwia nam włączanie kopii swoich gier, min z:
- nośników USB (pendrivy, czytniki kart SD)
- HDD (w przypadku PS2, lub niektórych modyfikowanych PS2 slim)
- serwerów sieciowych SMB
- MC2SIO/MX4SIO; adapterów na karty SD w slocie na karty pamięci na PS2

Problemem jest to, że niektóre z tych możliwości są wolniejsze, mniej kompatybilne od innych.

##### 2.1 OPL + USB
Wiele osób czytając USB pomyśli sobie - o, hej, PS2 wspiera ładowanie przez USB? Problem z głowy! Niestety nie ma tak słodko. Interfejs USB na PS2 to zaledwie USB 1.1. Transfer danych przez USB 1.1 jest o wiele wolniejszy niż gdyby PS2 czytało dane z płyty DVD/CD.

Tym samym ładując gry przez USB możemy oczekiwac baaaardzo wolnego ładowania gier. To nie było by takie złe, ale znaczna większość filmów z gier (FMV) przy użyciu USB będzie zacinała. Ponadto wiele z najlepszych gier na PS2 wcale się nie włączy przy użyciu ładowania z USB.

To najgorsza opcja z wyżej przedstawionych, nie wchodźcie w to.

##### 2.2 OPL + HDD
To najlepsza, najtańsza, najszybsza opcja.. jeżeli mamy PS2 fat. Teoretycznie kilka modeli PS2 Slim także można zmusić do ładowania gier z HDD, ale traktowałbym to jako ciekawostkę a nie jako opcję.

Używanie dysku HDD oznacza ładowanie dużo szybsze niz z DVD, kompatybilność minimalnie mniejszą jak przy użyciu nośników optycznych.
Jesteś zainteresowany? Przeczytaj [artykuł który napisałem o HDD w PS2](https://www.retromods.pl/blog/ps2-hdd/). Niedługo pojawi się także artykuł/film jak na taki HDD wgrywać kopie gier.

##### 2.3 OPL + serwer SMB
To druga najlepsza opcja po dysku HDD! Minusem jest to, że ładowanie gier jest niezauważalnie wolniejsze niż w przypadku HDD. Plusem natomiast to, że każde jedno PS2 wspiera ładowanie gier przez serwer SMB.

A co to ten cały serwer SMB? Mały komputerek (ja polecam router TPlink nano TL-WR802N, niektórzy używają RaspberryPi) który podłączamy za pomocą kabla ethernet do konsoli. Komputerek ten dzieni naszemu PS2 gry, po sprawie : ).
Na stronie pojawi się dedykowany artykuł jak złożyć takie cudo.

##### 2.4 OPL + MC2SIO/MX4SIO
To opcja wolniejsza niż HDD i SMB, wolniejsza też niż ładowanie gier z DVD. Plusem jest to, że jest nieco szybsza niż ładowanie z USB więc większość filmów FMV ładuje się nam poprawnie! Jest to też wygodna opcja, gdzie po prostu operujemy na karcie MicroSD zamiast odłączać dysk, czy bawić się w serwery SMB.

Największy minus? Kompatybilność gier jest najniższa ze wszystkich opisywanych tu metod. Nie możemy też zapisywać (aktualnie) stanu swojej rozgrywki. 
To raczej ciekawostka, aniżeli coś co mogę polecić.

### 3. Jakie są problemy OPL?
- Nie wszystkie gry działają z OPL, chociaż zdecydowana większośc jak najbardziej działa. 
- Kopie naszych gier musimy przygotować specjalnym programem (OPL manager).
- Brak natywnego, wbudowanego wsparcia dla gier z PS1. Część gier możemy odpalić za pomocą POPS loadera - emulatora PS1 dla PS2. Niestety gry często tną, lub się nie włączają. Jeżeli chcemy grać w gry z PS1 - pozostaje nam sprawny laser i/lub przeróbka chipem.


Społeczność PS2 powoli rozwija opcję odpalania gier z PS1 bez użycia modchipa, przeczytaj o MechaPWN jezeli cię to zainteresowało.

### 4. Jakie rozwiązanie dla mojego PS2?
Wiecie już jakie są możliwości. Którą wybrać dla siebie? Prosta sprawa.

- **PS2 Fat**: HDD i Network Adapter
- **PS2 Slim**: Serwer SMB

Reszta rozwiązań jest w powijakach, jest ciekawostką (jak PS2 Slim i HDD) albo sprawia za dużo problemów w użytkowaniu.
