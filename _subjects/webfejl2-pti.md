---
title: Webfejlesztés 2. (PTI)
toc: true
shortdesc: >
    Bevezetés a dinamikus kliens- és szerveroldali programozás világába. Alapvető JavaScript és PHP ismeretek.
lectures:
  - title: 1. Bevezetés, követelmények, JavaScript nyelvi alapok
    permalink: webfejl2/ea/01/
    date: 2018.02.14.
  - title: 2. A HTML programozás alapjai
    permalink: webfejl2/ea/02/
    date: 2018.02.21.
  - title: 3. Események, nyelvi elemek, beépített objektumok
    permalink: webfejl2/ea/03/
    date: 2018.02.28.
  - title: 4. Űrlapok, képek, táblázatok, böngésző
    permalink: webfejl2/ea/04/
    date: 2018.03.07.
  - title: 5. Stílusok, animáció
    permalink: webfejl2/ea/05/
    date: 2018.03.14.
---

# Általános információk

Óraszám
: 1 előadás + 2 gyakorlat + 1 konzultáció

Előfeltétel
: Webfejlesztés 1.

Célkitűzés
: A dinamikus kliens- és szerveroldali webprogramozás alapjainak a megismertetése. A félév első felében a JavaScript nyelvvel és a hozzá kapcsolódó alapfokú webes technológiákkal ismerkednek meg a hallgatók, a félév második felében a PHP nyelven keresztül ismerkednek meg a szerveroldali webprogramozás alapjaival.

Környezet
: A szerveroldali dinamikus weblapok készítését a webprogramozas.inf.elte.hu szerver segítségével végezzük el. A szerveren Nginx webszerver, 7-es verziójú PHP fut. A szerverre a félév elején, a gyakorlati jelentkezések lejártakor minden hallgató kap hozzáférést. A webprogramozás szerverre kell a beadandó feladatokat feltölteni, ezen folyik a félév második felében a gyakorlati munka, illetve ezen írjuk a félév végi évfolyam ZH-t is.

# Beadandók

**A következő információk folyamatosan frissülnek!!!**

Ebben a félévben az Etológia Tanszék kérésére kisgyerekeknek szóló webes (telefonon futó) játékokat készítünk el. Több játék közül lehet választani, mindegyikre kb. 20 hallgató jut. A megfelelő táblázatban jelentkezni kell majd, hogy ki melyik játék implementálását végzi el. Mindegyik játék esetén a megoldások közül kiválasztjuk a legjobbat. A legjobb megoldások készítői nyereményben részesülnek, bemutatjuk alkalmazásaikat az előadáson és a webprogramozas oldalon is.

A játékok leírásai alább találhatók. Ezek egyelőre még nem véglegesek. Az implementálás olyan részleteihez, mint érintésvezérlés, vagy mobilra optimalizálás, adunk segítséget leírás formájában. 

[Játékok](https://drive.google.com/open?id=1Bxc7mUzePM-J7eFUhylTenT4gYXaWDeS):

- Irányok mátrix
- 2D mátrix
- Irányok
- Tangram
- Szín sudoku
- Memória
- TicTacToe
- Mastermind

## Technikai segítség

A játékokat szeretnénk mobiltelefonok böngészőjében futtatni. Ehhez összeraktunk egy olyan kis oldalt, amely példát mutathat számos apektusban. A legtöbb játékban ugyanis van drag and drop, az oldal felosztása, stb. Hangsúlyozzuk, ez nem egy sablon, nem egy az egyben kell átvenni, de vannak benne olyan megoldások, amelyeket alkotó módon fel lehet használni a megoldásban:

- [Forráskód](https://repl.it/@horvathgyozo/touch2)
- [Kipróbálás, pl. mobiltelefonon](https://touch2--horvathgyozo.repl.co)

### Tesztelés

Az alkalmazás teszteléséhez nem kell állandóan mobiltelefonon kipróbálni a változtatásokat. A Chrome böngészőben pl. a fejlesztői eszköztár bal felső sarkában a 2. ikon épp arra szolgál, hogy az oldalt mobiltelefonos környezetben szimulálja. Ez nemcsak az oldal átméretezését jelenti, hanem az események szinjén is az egéreseményeket érintéseseménnyé alakítja. Ebben ajánlott tesztelni az alkalmazást.

### Eseménykezelés

Ha azt szeretnénk, hogy az alkalmazásunkat egérrel, érintéssel vagy érintős tollal is lehessen használni, akkor nehéz helyzetbe kerülhetünk, mert külön események vannak az egérhez (`mouse`), az érintéshez (`touch`) és a tollhoz (`pen`). Szerencsére az utóbbi években megjelent egy olyan eseménymodell, amely ezeket egységes interfészen keresztül kezeli: [Pointer Events](https://developer.mozilla.org/en-US/docs/Web/API/Pointer_events). Gyakorlatilag az egéreseményekben lévő `mouse` kulcsszót kell `pointer`-re cserélni, így lesznek a következő események:

- `pointerdown`
- `pointermove`
- `pointerup`
- stb.

Az eseményeket a következő kiegészítik a következő CSS tulajdonságok:

- `touch-action`: a mobilböngészőnek számos alapértelmezett művelete van érintés esetén, pl. az oldal görgetése. Bármelyik elemhez hozzáérünk, akkor ez az alapértelmezett művelet hajtódik végre, és ez megállítja a `pointer` eseményeket. Hogy a böngésző ne reagáljon az alapértelmezett műveletekre, ezt CSS-ben a `touch-action: none;`-nal lehet beállítani. A fenti példában az egész játékfelületet adó `#container` elemre van ez beállítva.

- `pointer-events`: nem összekeverendő a fentebb említett esemény API-val. A `pointer-events` CSS tulajdonsággal azt lehet beállítani, hogy egy adott elem érzékelje-e egyáltalán a kattintást, érintést. A `pointer-events: none;` beállítással például az pointer eseményekre átlátszó elemeket lehet megadni. A példában ott használjuk ezt ki, hogy amikor draggeljük a négyzetet, akkor a négyzet alatti elemre vagyunk kíváncsiak, hogy az droppable zóna-e. Így az elemen kikapcsoljuk az események érzékelését draggelés közben.

### Drag and drop érintéssel

A HTML5 drag and drop API kiválóan alkalmas asztali böngészőkben egéreseményekkel. Sajnos azonban egyelőre egyáltalán nem optimalizálták érintésvezérlésre ezt az API-t. Így a drag and drop-ot nekünk kell megvalósítani. Ehhez kétféle segédosztályt vezettem be: `.draggable` jelzi a vonszolható objektumokat, `.dropzone` az ejtési zónákat. Emellett van egy `activeDropZone` nevű globális változó, ami nyomon követi, hogy aktuálisan melyik zóna fölött vagyunk.

1. **onPointerDown**: a container kap egy `.dragging` stílusosztályt, hogy pár elem viselkedését megváltoztathassuk. A vonszolt objektum `.active` lesz. A `setPointerCapture`-rel pedig azt állítjuk be, hogy a vonszolás során az *összes* eseményt a vonszolt objektum kapja meg.

2. **onPointerMove**: először kiszűrjük azokat az elemeket, akikhez valóban tartozik az esemény (`hasPointerCapture`), majd lekérjük az egér x, y koordinátáit. Az `elementFromPoint` metódussal lekérdezzük az egérmutató alatti elemet (átlát a `pointer-events: none` elemeken). A következő if-ekben az ejtési zóna kezelése van: nem-aktív --> aktív, aktív --> aktív, aktív --> nem-aktív. Végül a vonszolt elemet (`e.target`) az egérmutató alá helyezzük.

3. **onPointerUp**: a stílusosztályok eltávolítása mellett a legfontosabb, hogy ha ejtési zóna fölött vagyunk, akkor mi történjen: a mi esetünkben az adott elem gyerekeként adjuk hozzá a vonszolt elemet (`appendChild`).


### Mobil layout

A legtöbb alkalmazásban szükség lesz egy fejlécre, és egy -- akár több részre osztott -- játéktérre. Mivel különböző oldalarányú eszközökön is futhat a játék, ezt valahogy kezelni kell. A méreteket akár a játék elején JavaScripttel is beállíthatjuk, erre mutat példát az `index.js` elején található pár kikommentelt kódsor. Ugyanakkor a layout nagy része CSS-sel is megoldható. Az `index.css` első része tartalmazza az ehhez kapcsolódó kódot.

- elemek elhelyezése: mind a `body`, mind a `#container` flexboxot használ arra, hogy az elemeket egymás alá, megfelelő módon helyezze el.

- elemek szélessége és magassága: a `width`, `height`, `max-width`, `max-height` tulajdonságokkal, és `vw`, `vh` mértékegységekkel és a `calc` metódussal lehet megoldani pár trükköt. A szélességet például a magasságban lehet limitálni, a magasságot pedig a szélességben, így alakulhat ki a példában egy mindig négyzet alakú játéktér (erre nem biztos, hogy minden játék esetén szükség van!).


# Számonkérés

Összevont (folyamatos) értékelésű tárgy.

## Az értékelés összetevői

* Beadandó feladat: JavaScript
    Határidő: TBA
* Beadandó feladat: PHP
    Határidő: TBA
* Évfolyam ZH
    2018\. május 28. 9:00-12:00 és 2018. május 29. 9:00-12:00, Lovarda, Nyelvi- és Adatbázis labor
* PótZH
    2018\. június 5. 9:00-12:00, Lovarda

## A beadandók értékelése

* A beadandók értékelése háromértékű skálán történik: -0,5; 0; 0,5 jegy kapható rá.
* Az értékelés egy mindenki számára elérhető szempontok alapján történik.
* A beadandókat határidőre kell elkészíteni.
* A határidő leteltével a beadandó jegyéből a késés mértékének megfelelően vonunk le pontokat
* A beadandókat a webprogramozás szerverre kell feltölteni a [feltöltő felületen](http://webprogramozas.inf.elte.hu/ebr) keresztül. Más módon küldött beadandókat nem fogadunk el.
* A beadandók plágiumellenőrzésen mennek keresztül az esetleges másolásokat kiszűrendő.
* A beadandók készítőit szükség esetén megkérhetjük megoldásaik megvédésére.

## Az évfolyam ZH értékelése

* Az évfolyam ZH értékelése jeggyel történik 1-5 skálán.
* A megoldások plágiumellenőrzésen esnek át a ZH után. A gyanúsan hasonló megoldást adó hallgatókat megkérhetjük a ZH-ik megvédésére. A másolt ZH-k automatikusan 1-es osztályzatot kapnak.

## Jegyszerzés feltételei

* Részvétel a gyakorlatok legalább 75%-án (maximum 3 hiányzás)
* Két elfogadott beadandó
* Megírt évfolyam ZH

## Értékelés

* Évfolyam ZH jegye + a két beadandó értékelése
* A kettes érdemjegyhez legalább kettesre megírt évfolyam ZH szükséges

# Előadások

{% include lectures-external.html %}

# Gyakorlatok

{% include practices.html %}

# Segédanyagok

## Elektronikus tananyag

* [Bevezetés a kliens- és szerveroldali webalkalmazások készítésébe (elektronikus tananyag)](http://webprogramozas.inf.elte.hu/tananyag/wf2/index.html)

## Példa beadandók és ZH-k

* [Példa JavaScript beadandó feladat](webfejl2/gyak/js_grafilogika.html)
* [Példa PHP beadandó feladat](webfejl2/gyak/php_grafilogika.html)
* [Példa évfolyam ZH (névjegy)](webfejl2/gyak/pelda_zh.html)
* [Példa évfolyam ZH (csillag)](webfejl2/gyak/pelda_zh2.html)

# Oktatók

## Előadó

Horváth Győző

## Gyakorlatvezetők

* Bende Imre
* Demsa Miklós
* Kereszti Krisztián
* Kereszti Zalán
* Horváth Győző
* Rakonczai Sándor
* [Visnovitz Márton](https://github.com/vimtaai/elte/tree/master/2017-18-2)
