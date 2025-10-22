# Artefakt:
- **Talizman Talii (chuj wie co)** – _Speed II_ dla gracza noszącego
- **Kompas Rogiera (polaczone 4 kompasy w 1)** – _Step Height_ dla gracza noszącego
Po jednym dla każdej osoby w wygrywającej parze.
# Lore:
**Talia** była alchemiczką, eksperymentowała z magia i sie zamienila w rybe. Rogier był nawigatorem/korsarzem/marynarzem, który za wszelką cenę próbował ją odnaleźć.
## Talia
- Zamieniona w rybe Smarkula
- asdasd
- sdads
## Nawigator 
- Bezimienny do samego konca.
- Na finalnym artefakcie smaczek ze to tak naprawde byl rogier
- fasifhaosi
- faoshfoas????????
# Lokacje:
- **Okręt Rogiera** 
	`/execute in minecraft:overworld run tp @s 4741.06 69.68 2450.92 -172.16 57.26`
	![Okręt Rogiera](2025-10-23_00.06.58.png)
- **Domek Talii**
	`/execute in minecraft:overworld run tp @s 5401.77 70.06 3351.76 -1882.49 9.36`
	![Domek Talii](2025-10-23_00.03.54.png)![Domek Talii 2](2025-10-23_00.04.39.png)
- **Morski labirynt**
	`/execute in minecraft:overworld run tp @s 7430.89 -20.00 1915.67`
	![Morski labirynt](2025-10-23_00.07.40.png)
	![Morski labirynt 2](2025-10-23_00.08.23.png)
- **Strażnica morska**
	`/execute in minecraft:overworld run tp @s 4168.08 72.60 2775.46 -302.39 -13.66`
	![Strażnica morska](2025-10-23_00.05.30.png)
	![Strażnica morska 2](2025-10-23_00.06.12.png)
# Etapy:
## Początek:
Przygoda zaczyna sie od znalezienia w jednej z osad notatki o ptzycumowanym ogrecie gdzies tam. Na okrecie da sie znalezc pierwszy kompas prowadzacy do smarkuli, oraz w skrzyni 2 notatki (1 szyfrem, druga czesciowo przetlumaczona). Zrobie to tak zeby dalo sie przy odrobinie pracy poskladac solucje do szyfru.
## Main Hub:
Domek Talii, przy łóżku ukryte zejscie do piwnicy gdzie znajduje sie smarkula i lista wyzwań, po ukonczeniu wszytstkich bedzie tam tez teleport/jakis pokoj finalowy gdzie dostaje sie artefakt od talii i zaklina kompas tez w artefakt idk.

## Wyzwania:
==TODO: napisaćplugin do obsługi kompasów, dodać interakcje co finalizuje dane wyzwanie==
Aktualnie zdecydowałem się pójść w 4 typy wyzwać tak jak jest 4 żywiołów. Do każdego wyzwania da się podchodzić w dowolnej kolejności. Tylko 1 para może robić dane wyzwanie na raz. Mechanizm failsafe, jak ktos blokuje wyzwanie na za długo to automatycznie otwiera następnej parze a tamtych kickuje. Zrobienie wszystkich 4 wyzwań jest wymagane do odblokowania finału.

1. [x] **Latarnia morska** (wyzwanie powietrza) - Wymagana jest 2 graczy, 1 oosoba musi aktywowac beacon zeby nawigator mogl wejsc na szczyt
2. [ ] **Morski labirynt** (wyzwanie wody)- teoretycznie da sie zrobic solo na razie, trzeba sie przekrasc przez ocean monument na niewidoku, pod nim jest labirytnt, jedna osoba idzie przez labirynt, druga prowadzi, w rogu jest ukryta mapa z solucja, ==TODO: Dodać pistony i ukryte przescia ktore sie otwieraja po wcisniecciu guziku, dodatkowo lepiej udekorowac bo szpetne so far==
3. [ ] **Układ słoneczny** (wyzwanie ziemi) - wielkie czarne pomieszczenie, w środku symulacja układu slonecznego (moze tylko slonce, ksiezyc, ziemia), jakiś redstone albo interakcje do kontrolowania uplywu czasu w symulacji, planuje zrobic tak zeby normalnie byla animacja jak planety plywaja wogol slonca, jakies notatki napisane szyfrem, które zawierają instrukcje jak operować symulacją układu, jak sie ustawi wszystkie w obiekty w jednej linii otwiera sie przejscie do pokoju z interakcją kończącą wyzwanie, ==TODO: W zasadzie wszystko do zrobienia, trzeba zbudować i napsiac commandblocki bo tak chyba najłatwiej i najczyściej bedzie sie robić symulację, command blocki obią obliczenia na podstawie scoreboard czas i tempo uplywu czasu==
4. [ ] coś w netherze idk co jeszcze, ale moze coś chillowego. Myślałem nad jakimś takim nieskończonym tunelem w stylu ze spadasz tubą i jak docierasz do konca to cie teleportuje znowu na góre tak zeby dawac iluzje ze spada sie w nieskonczonosc. moze jakies laminal spaces w stylu ze obchodzisz jakis filar i po zrobieniu kółka lokacja wygląda nieco inaczej. idk jeszcze
# Komendy:
*Efekty obsługiwane są przez plugin*
## Artefakty
- Artefakt 1:
```java
give WujekRadek rabbit_foot[custom_name=[{"text":"Talisman Talii","italic":false}],lore=[[{"text":"linijka 1","color":"aqua"}],[{"text":"linijka 2","color":"aqua"}],[{"text":"linijka 3","color":"aqua"}],[{"text":"linijka 4","color":"aqua"}],[{"text":"linijka 5","color":"aqua"}]]]
```
## Notatki dodatkowe
 - Notatka szyft - Wyzwanie Powietrza
```java
give WujekRadek paper[custom_name=[{"text":"Wyzwanie Powietrza","italic":false,"color":"gray","font":"minecraft:alt"}],rarity=rare]
```
- Notatka szyft - Wyzwanie Ognia
```java
give WujekRadek paper[custom_name=[{"text":"Wyzwanie Ognia","italic":false,"color":"red","font":"minecraft:alt"}],rarity=rare]
```
- Notatka szyft - Wyzwanie Ziemi
```java
give WujekRadek paper[custom_name=[{"text":"Wyzwanie Ziemi","italic":false,"color":"#92450c","font":"minecraft:alt"}],rarity=rare]
```
- Notatka szyft - Wyzwanie Wody
```java
give WujekRadek paper[custom_name=[{"text":"Wyzwanie Wody","italic":false,"color":"dark_aqua","font":"minecraft:alt"}],rarity=rare]
```
## Dodatkowe komendy
- dodawanie zone zeby po przybyciu na lokacje wyswietlila sie jej nazwa
```java
/zone add <nazwa> <lokacji> <itp> <ostatni argument - promień strefy>
/zone add Morski Labirynt 60
```
