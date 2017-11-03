---
layout: subject
title: Alkalmazások fejlesztése
permalink: alkfejl.html
toc: true
shortdesc: >
    Modern kliens-szerver alkalmazások írása webtechnológiák segítségével. A technológiai ismereteken túl az alkalmazásfejlesztés életciklusával is megismerkednek a hallgatók a tervezéstől a tesztelésen át a dokumentálásig.
---

# Általános információk

Óraszám
: 2 gyakorlat

Előfeltétel
: Programozási technológiák 2.

Célkitűzés
: A hagyományos asztali egyfelhasználós alkalmazásoktól továbblépve ebben a tárgyban a hallgatók megismerkedhetnek a kliens-szerver architektúrákkal, annak is egy igen népszerű ágával, a webes protokollokat és technológiákat használó alkalmazások fejlesztésével. A webes alkalmazások készítéséhez felhasználjuk a programozási technológiákon megismert modellezési eszközöket, és azokat webes környezetre ültetjük át. A tantárgy célja, hogy kiindulási ponttul szolgálhasson azok számára, akik modern webes alkalmazásokat szeretnének fejleszteni.

Környezet
: Az órai munkákat a lokális gépeken telepített futtató- és fejlesztőkörnyezetek segítségével igyekszünk megoldani. A használt környezetek és szerkesztőprogramok a választott technológiáktól is függenek. Bizonyos esetekben felhőalkalmazások segítségét is igénybe vehetjük.

# Számonkérés

## Az értékelés összetevői

* Összetett feladat megadása funkcionális és nem funkcionális követelmények specifikálásával. 
* Határidők:
    * [Projektötlet](#projektötlet)  
      4\. tanulmányi hét (2017.10.08.)
    * [Backend megvalósítása](#backend-megvalósítása)  
      7\. tanulmányi hét (2017.10.29)
    * [Működő prototípus megvalósítása](#működő-prototípus)  
      10\. tanulmányi hét (2017.11.22)
    * [Kész alkalmazás, dokumentáció, bemutatás](#kész-alkalmazás)  
      Határidő: Utolsó gyakorlat

## A beadandó feladat

A félév során egyetlen feladat lépésenkénti elkészítése lesz a cél. A feladatot **kétfős csoportok** végzik el. A fejlesztéshez **git** verziókövető rendszert kell használni, az egyes fázisokat megfelelően rögzítve a rendszerben (azaz nem a teljes fejlesztést követően kell a kódtárat feltölteni). Az alkalmazást **publikus Github kódtár**ként kell közzétenni a csoporttagok egyikének azonosítója alatt. A csoport másik tagja közreműködőként van a kódtárhoz rendelve. A feladathoz **dokumentáció** írása is szükséges. Végül az elkészült alkalmazást a dokumentációval együtt **be kell mutatni**. A fejlesztés egyes fázisait a megfelelő határidőre el kell készíteni, és erről a gyakorlatvezetőt értesíteni kell.

A fejlesztendő alkalmazásnak hasonló komplexitásúnak kell lennie, mint ami a [webes alkalmazások fejlesztése](http://people.inf.elte.hu/groberto/elte_waf/feladatok/elte_waf_feladatok.pdf) tárgynál elvárnak. A feladatnak tartalmaznia kell:

- Adatbázis
    + legalább 4 táblát
    + legyen benne 1-sok kapcsolat
    + legyen benne sok-sok kapcsolat
    + az adatbázis-kezelő az órán megismert `h2` rendszer lehet
- Szerveroldal
    + Java Spring Boot technológia használata
    + MVC modell
    + REST API
    + authorizált végpontokkal
- Kliensoldal
    + technológiát illetően az órán megismert Angular keretrendszert kell használni (2+ verzió).
    + legalább három tábla adatait szerkeszteni kell tudni a felületen: lista, új, módosít, töröl (vagy inaktívvá tesz)
    + legyenek benne csak hitelesítés után elérhető funkciók (autentikáció)
    + ügyelni kell, hogy csak a megfelelő adatokhoz férjen hozzá a megfelelő felhasználó (autorizáció)
    + a szerverrel AJAX kérésekkel történjen a kommunikáció

További feladatötletek:

- Receptek és hozzávalók
- Tantárgyak felvétele (mini Neptun)
- Raktár bevételezés
- Családi todo
- Családi büdzsé
- Névjegyek kezelése
- Munkaidő nyilvántartás

## Projektötlet

Első lépésként egy rövid feladatleírást kell megadni a projekt Github főoldalán a `README.md` állományban. A feladatleírásnak a következő elemeket kell tartalmaznia rövid leírás vagy felsorolás formájában:

- feladat funkcionális követelményeit 
- feladat nem funkcionális követelményei
- szakterületi fogalomjegyzék (azon fogalmak definiálása, ami köré az alkalmazás épül)
- szerepkörök

## Backend megvalósítása

Első fejlesztési fázisként a Java backend és az adatbázis elkészítése szükséges az órán tanult módszerekkel, illetve -- ha szükséges -- további megoldásokkal. Az elkészült munkának meg kell felelnie a feladatleírásnál fentebb leírt követelményeknek. Az elkészült kód mellé szükséges elkészíteni az adott réteg aktuális dokumentációját, ami a következőket tartalmazza:

- fejlesztői környezet bemutatása, beállítása, használt technológiák
- adatbázis-terv: táblák kapcsolati UML diagramja
- alkalmazott könyvtárstruktúra bemutatása
- Végpont-tervek és leírások
- 1 db végpont működésének leírása, mi történik, milyen lépések követik egymást (szekvenciadiagram)
- fontosabb specifikumok bemutatása (ha van ilyen)

## Működő prototípus

A következő lépésben a felhasználói felület kialakítása a cél backend szolgáltatások nélkül. Egy olyan, komponensekből, oldalakból és végpontokból álló alkalmazást kell készíteni, amely működik, de egyelőre statikus, beégetett adatokkal dolgozik. A dokumentációt a következő elemekkel szükséges bővíteni:

- használati eset diagram: melyik szerepkör mely felületekhez fér hozzá
- fejlesztői környezet bemutatása, beállítása, használt technológiák
- az alkalmazott könyvtárstruktúra bemutatása
- (felületi tervek, oldalvázlatok)

## Kész alkalmazás

Utolsó fázisban összekötjük a backendet a frontenddel, a felületek működését a szerveren tárolt adatokkal biztosítjuk, az alkalmazást végső állapotra csiszoljuk. A dokumentáció a következőket tartalmazza:

- kliensoldali szolgáltatások listája, rövid leírással
- kapcsolat a szerverrel
- állapotdiagram (ha szükséges)
- egy funkció folyamatának leírása, azaz mi történik kattintástól a visszajelzésig
- tesztelés
- felhasználói dokumentáció

## Bemutatás

A bemutatás az utolsó gyakorlaton történik. Minden csapatra kb. 9 perc jut, de számítsunk arra, hogy ekkor túlléphetjük a gyakorlat időkeretét. A bemutatónak tartalmaznia kell:

- a feladat ismertetését (fél perc)
- az alkalmazás bemutatását (2 perc)
- az alkalmazás működésének részleteit (1 perc)
- a dokumentáció gyors bemutatását (1 perc)
- fejlesztési tapasztalatokat (fél perc)
- a csapatmunka részleteit (fél perc)

A bemutatás után a gyakorlatvezető és a csoporttagok is kérdéseket tehetnek fel, megjegyzéseket fűzhetnek a munkához. Az értékelés helyben történik.

## Jegyszerzés feltételei

* Részvétel a gyakorlatok legalább 75%-án (maximum 3 hiányzás)
* Minden "milestone" beadása időben
* Elkészített és bemutatott alkalmazás
* Kérdőív kitöltése

## Értékelés

* A beadandó feladatokra 0-10 pont kapható, ezt a csoport két tagja saját belátása szerint osztja el egymás között.

# Segédanyagok

* [A tárgy e félévi Github oldala](https://github.com/horvathgyozo/alkfejl-2017)
* [Segítség a dokumentációhoz](https://github.com/horvathgyozo/alkfejl_minta)
* Mintadokumentációk
    - [Képgalériás alkalmazás (Bartalos Gábor)](https://github.com/KisGabo/gallery-elteik/wiki)
    - [Szerepjáték (Teleki Miklós)](https://github.com/Telmike91/alkfejlszerver)
* [HTML tananyag (Abonyi-Tóth Andor): A weblapkészítés technikája (HTML5, CSS3) és ergonómiája](http://tamop412.elte.hu/tananyagok/weblapkeszites)
* [Bevezetés a kliens- és szerveroldali webalkalmazások készítésébe (elektronikus tananyag)](http://webprogramozas.inf.elte.hu/tananyag/wf2/)
* [Webadatbázis-programozás (elektronikus tananyag, PHP alapokon, de a tervezés, az MNV-minta bemutatása és a kliensoldali fejlesztés része itt is aktuális)](http://ade.web.elte.hu/wabp)

# Oktatók

## Tárgyfelelős

Horváth Győző

## Gyakorlatvezetők

* Godzsák Dávid
* Horváth Győző
* Kereszti Krisztián
* Rakonczai Sándor
* Visnovitz Márton