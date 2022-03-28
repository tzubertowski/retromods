---
title: "Jak podłączyć dysk do ps2"
description: "meta description"
image: "images/post/ps2-hdd/ps2hdd.jpg"
date: 2022-03-27T16:56:47+06:00
draft: false
author: "Prosty"
tags: ["Diy", "PS2", "OPL", "HDD", "network adapter"]
categories: ["PS2"]
---

### 1. Expansion bay. Dla kogo to? Czemu to służy?
Pierwsze modele PS2 w regonie PAL i NTSC (różnie to bywało z NTSC-J), powszechnie znane jako "PS2 FAT" (SCPH-10000 - SCPH-500xx), od premiery wspierały dodatkowe akcesoria przez tzw. "expansion bay". Według planu Sony expansion bay miał być wykorzystywany jako modularny sposób na powiększenie możliwości PS2.

<p align="center">
  <img alt="Expansion bay dla PS2 fat" width="500" src="/post/ps2-hdd/expansion-bay.jpg#center" />
</p>

Realnie expansion bay wykorzystywany był najczęściej do dodania możliwości siecowych (karta sieciowa z ethernet) oraz do podłączenia dysku twardego do konsoli. Możliwość taką oferował tzw. network adapter.

<p align="center">
  <img alt="Network adapter" width="350" src="/post/ps2-hdd/network1.jpg" />
  <img alt="Network adapter" width="350" src="/post/ps2-hdd/network2.jpg" />
</p>

Wszystkie modele PS2 slim wyposażone są w kartę sieciową, a w ich konstrukcji kompletnie usunięto port Expansion Bay. Tym samym **nie podłączymy takiego network adaptera do PS2 slim**. To nie oznacza, że nie podłączymy dysku do PS2 slim, na końcu zostawię o tym kilka informacji.

Dysk HDD w konsoli PS2 wykorzystywany był w niewielu tytułach, takich jak Final Fantasy XI oraz kilku innych grach sieciowych. PS2, w przeciwieństwie do PS3/PS4/PS5 nie umożliwiało w standardzie instalacji posiadanych gier na dysk HDD.
A przynajmniej było tak przed powstaniem modyfikacji oprogramowania. Aktualnie na dysk PS2 jesteśmy w stanie wrzucać komfortowo nasze kopie gier, emulatory, romy oraz inne.

### 2. Network adapter a dysk IDE/SATA
Ci z was którzy mieli komputer PC w latach 90, zauważyli na pewno, że network adapter od Sony posiada złącze typu IDE. Tym samym sam network adapter umożliwia podpięcie tylko i wyłącznie dysków IDE.

Niestety, dyski z tym złączem są już stare. Dyski są drogie, rzadkie i małych rozmiarów. Ich mechaniczna konstrukcja oznacza, że wraz z wiekiem narażone są one na uszkodzenia fizyczne, bad sektory oraz utratę danych. Zdecydowanie odradzam zakup takiego dysku, nawet na potrzeby 20 letniego już PS2.

<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/ps2-hdd/sata-ide.jpg" />
</p>

Głowa do góry. Jest kilka opcji jak podłaćzyć tańszy, większy i szybszy dysk do PS2. Z pomocą przychodzi SATA.
Większość komputerów stacjonarnych i laptopów od wielu latu żywa standardu podłączenia dysków SATA. SATA jest bezpośrednim następcą portu IDE, o którym pisałem powyżej.

IDE jest złe, SATA jest ok. Jak sprawić, żeby PS2 zaakceptowało dyski SATA?

#### 2.1 Chińskie network adaptery
<p align="center">
  <img alt="Expansion bay dla PS2 fat" width="500" src="/post/ps2-hdd/chnkada.jpg" />
</p>
Chinczycy oferują nam Network Adaptery które zamiast portów IDE, jak to ma przypadek w orginalnych adapterach Sony, posiadają port SATA. Wystarczy kupić taki adapter, kupić dysk SATA i wszystko śmiga.

**Minusy**

W czym problem? 
- Chińskie Network Adaptery **nie wspierają połączenia sieciowego**

Na dzisiejszy dzień użyteczność połączenia sieciowego w przypadku PS2 jest znikoma. Oficjalne serwery gier PS2 są od dawna wyłączone. Do kilku gier istnieją jednak serwery prywatne, eg. do SOCOMa.
To, co boli bardziej to to, że połączenie sieciowe może zostać wykorzystane do podłączenia PS2 do sieci lokalnej i zgrywania kopii gier bezpośrednio na dysk przez sieć. Tym samym nie musimy rozkręcać konsoli za kazdym razem, gdy chcemy wgrać nową grę. Zgrywanie te jednak jest dość powolne i mija się z celem w przypadku wgrywania dużej kolekcji gier.

**Plusy**

Jeżeli nie zależy wam na zrzucaniu gier przez sieć lokalną oraz na graniu w tę garstkę gier z prywatnymi serwerami - bierzcie tani (koszt ok. 50 zł), chiński adapter z portem SATA.

Dołączam link do adaptera, który sam posiadam oraz polecam każdemu zainteresowanemu tematyką HDD na PS2:
- https://bit.ly/3IFFr5b


#### 2.2 Modyfikacja orginalnego network adaptera
<p align="center">
  <img alt="Expansion bay dla PS2 fat" width="500" src="/post/ps2-hdd/idesata.jpg" />
</p>

Jeżeli masz troszkę umiejętności manualnych i nie boisz się śrubowkręta to:
- kup oryginalny Network Adapter Sony
- kup adapter IDE -> SATA i zainstaluj go w konsoli

**Minusy**

Niestety adapter IDE -> SATA to dość spory koszt, bo ok 60-70 zł. Jest stosunkowo ciężko dostępny, wymaga instalacji ręcznej. Ponadto trzeba doliczyć koszta oryginalnego Network Adaptera od Sony (grubo ponad 100 zł)

**Plusy**

Jedynym plusem w porównaniu do chinskiego klona jest fakt, że możemy podłączyć PS2 do sieci.


Adapter IDE na SATA znajdziemy np. tu:
- https://www.amazon.com/Adapter-Upgrade-Original-Network-Large%E2%80%91Capacity/dp/B08PP5RSDV


### 3. Ok, mam adapter z SATA. Jaki kupić dysk?
Do wyboru mamy dwa typy dysków. Dysk HDD i SSD. 

#### 3.1 SSD do PS2?
Mimo iż network adapter wspiera dyski SATA, to prędkość odczytu dalej zostaje taka sama jak w przypadku dysków IDE. PS2 maksymalnie odczytuje dane z dysku z prędkością **max 66MB/s**. Standardowe, nie-serwerowe dyski SSD SATA mają prędkość odczytu do 700-750 MB/s. 

Tym samym SSD jak i HDD w PS2 będą limitowane do 66MB/s. SSD nie ma przewagi prędkościowej. Jedynym atutem dysku SSD, który może przełożyć się na mikrosekundy przy ładaniu gier, jest caching plików. Ale ta różnica jest tak znikoma, że nie warta rozpatrzenia.

**Plusy**

Dyski SSD wobec dysków HDD w przypadku PS2 mają jeden atut: dysk SSD nie posiada cześci mechanicznych, przez co ma o niebo większą żywotność. Mniej się psują oraz mniej hałasują.

#### 3.2 HDD do PS2?
Tak, jak najbardziej.

**Plusy**

Dyski HDD są tanie, mają dużą pojemność i są łatwo dostępne oraz ciche (jeżeli wiecie na co patrzeć).

Na co patrzymy - wybierając dysk HDD?
- polecam dyski 2.5", gdyż takie montuje się w laptopach. Duża dostępność w niskich cenach
- dysk HDD powinien mieć optymalnie 7200 RPM. Takie dyski są o niebo lepszej jakości niż dyski 5200 RPM, gdyż 7200 RPM zazwyczaj mają zastosowania biznesowe bądź serwerowe gdzie każda awaria to ogromny problem. Ponadto dyski 7200 posiadają cache podobny od tego z dysków SSD, przez co odczytują dane szybciej
- to tylko preferencja co do marki, ale serdecznie polecam dyski WD. Mniej polecam dyski Seagate

Ile zapłacić za taki dysk? Ja za używany dysk 1TB, 7200 RPM, 2.5" WD zapłaciłem 39 zł ;) Nie przepłacajcie.

### Dodatkowe notki
#### 1. PS2 Slim i podłączenie dysku
<p align="center">
  <img alt="Expansion bay dla PS2 fat" width="500" src="/post/ps2-hdd/slimhdd.jpg" />
</p>
Żadne PS2 slim nie wspiera network adaptera z portem SATA/IDE. Jednak część modeli PS2 slim (700XX do V13 włącznie) na swojej płycie wsparcie dla expansion bay, które nie jest wyprowadzone jako port. 

Tym samym istnieją modyfikacje, którze umożliwiają wlutowanie taśmy IDE na gorąco pod samą płytę główną ;)
- https://www.elektroda.pl/rtvforum/topic944160.html

Nie polecam jednak tego sposobu. Na PS2 slim, za dosłownie mniej niż 60 zł, możemy złożyć sobie serwer SMB który będzie wygodniejszym sposobem na zrzucanie sobie gier z bardzo podobną prędkościa co w przypadku dysku HDD 2x wolniejszy maksymalny transfer, ale różnica jest niedostrzegalna gdyż samo PS2 nie jest w stanie użyć maksymalnego transferu HDD IDE.

#### 2. PS2 Fat + Network Adapter i karty SD
<p align="center">
  <img alt="Expansion bay dla PS2 fat" width="500" src="/post/ps2-hdd/sdreader.jpg" />
</p>
Nie chcecie się bawić wcale w dyski? Jeżeli macie PS2 fat to macie opcję podłączenia sobie czytnika kart SD zamiast fizycznego dysku. Po prostu wpinacie adapter pod port IDE/SATA waszego Network Adaptera a kartę SD przygotowujecie tak, jakby była zwykłym dyskiem od PS2.

- https://bit.ly/3qDtO8M
- https://bit.ly/3qIFmYi

#### 3. Czy potrzebuję dysku żeby mieć swoją kolekcję gier w jednym miejscu?
<p align="center">
  <img alt="Expansion bay dla PS2 fat" width="500" src="/post/ps2-hdd/smb.jpg" />
</p>
W mojej opinii najlepszą formą przechowywania kopii waszych gier (wygodniejsza niż HDD) oraz odpalania ich na PS2 jest tzw. serwer SMB.

Rozwiązanie te polega na tym, że do PS2 podłączamy router/raspberry pi/inny mały komputer, który dzieli pliki naszych gier bezpośrednio przez sieć do PS2.

**Plusy**
- realna prędkość ładowania gier porównywalna jest do PS2 Fat z HDD
- rozwiązanie to działa zarówno z PS2 Fat jak i Slim
- zrzucamy kopie naszych gier przez sieć domową z pełną prędkością przesyłu
- koszt całkowity to ok. 60 zł

**Minusy**
- na biurku/szafce mamy malutkie pudełko z routerem/komputerem działającym jako serwer SMB
- minimalnie gorsza kompatybliność gier (niezauważalna róznica)



