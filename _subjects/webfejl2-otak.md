---
title: Webfejlesztés 2. (OTAK)
toc: true
lectures:
  - title: 1. A HTML programozás alapjai
    permalink: webfejl2t/ea/01/
  - title: 2. A HTML programozás alapjai, események, nyelvi elemek, beépített objektumok
    permalink: webfejl2t/ea/02_03/
  - title: 3. Stílusok kezelése, rasztergrafika, nyelvi elemek
    permalink: webfejl2t/ea/04_05/
  - title: 4. Kódszervezés, TypeScript, külső függvénykönyvtárak
    permalink: webfejl2t/ea/06_07/
---

# Általános információk

Óraszám
: 1 előadás + 2 gyakorlat + 1 konzultáció

Előfeltétel
: Webfejlesztés 1.

Célkitűzés
: A dinamikus kliens- és szerveroldali webprogramozás alapjainak a megismertetése. A félév első felében a JavaScript nyelvvel és a hozzá kapcsolódó alapfokú webes technológiákkal ismerkednek meg a hallgatók, a félév második felében a PHP nyelven keresztül ismerkednek meg a szerveroldali webprogramozás alapjaival.

Környezet
: A szerveroldali dinamikus weblapok készítését a webprogramozas.inf.elte.hu szerver segítségével végezzük el. A szerveren Apache webszerver, 7.0.9-es verziójú PHP fut. A szerverre a félév elején, a gyakorlati jelentkezések lejártakor minden hallgató kap hozzáférést. A webprogramozás szerverre kell a beadandó feladatokat feltölteni, ezen folyik a félév második felében a gyakorlati munka.

# Számonkérés

Összevont (folyamatos) értékelésű tárgy.

## Az értékelés összetevői

* Beadandó feladat: JavaScript (DOM)
    Határidő: 2017. november 19. éjfél
* Beadandó feladat: JavaScript (canvas)
    Határidő: 2017. december 31. éjfél  
* Beadandó feladat: PHP
    Határidő: 2018. január 21. éjfél

## Beadandó feladat: JavaScript (DOM)

### Feladat

A feladatod, hogy készíts egy olyan minialkalmazást, ami bemutatja valamelyik gyűjtemény típusú adatszerkezet (**_sor, verem, prioritási sor, kupac, halmaz, hatványhalmaz, láncolt lista_**) működését és műveleteit. Válassz ki egyet a felsorolt adatszerkezetekből, és készíts megfelelő űrlapot, ami segítségével az egyes típusműveletek elvégezhetőek (pl. verem esetében `üres`, `tető`, `verembe`, `veremből`). Látszódjon az alkalmazásban az adott adatszerkezet valamilyen grafikus módon ábrázolva, és az adott műveletek bemenete és kimenete legyen egy HTML űrlapon látható. Minden egyes művelet után jelenjen meg újra, a módosított adatszerkezet, vagy ha csak adatkiolvasás történt, akkor valahogy jelezd, hogy melyik elemen történt az olvasás.

### Értékelési szempontok

* Az adott adatszerekezet neve látszik
* Az adatszerkezet műveleteinek megfelelő vezérlőgombok és ki- és bemeneti mezők látaszanak
* Az adatszerkezet valamilyen formában ábrázolásra kerül
* Az adatszerkezeten annak műveletei elvégezhetőek
* A grafikus ábrázolásban látszik, ha módosult valami az adatszerkezeten
* A grafikus ábrázolásban látszik, hogy ha olvasás volt, akkor melyik elemet olvastuk ki
* Az űrlapon minden művelet után helyesen jelenik meg a művelet kimenete (pl. a kiolvasott adat)
* Nincsenek fura jelenségek, bugok

## Beadandó feladat: Javascript (canvas)

### Feladat

A feladatod, hogy készíts egy olyan minialkalmazást, ami HTML űrlap beviteli mezők segítségével megkapja egy tetszőleges, legfejlebb harmadfokú polinom (**_y = ax<sup>3</sup> + bx<sup>2</sup> + cx + d_**) együtthatóit (**_a, b, c, d_**), és ezek alapján egy gombra kattintva ábrázolja egy megadott (**_x<sub></sub>, x<sub>2</sub>_**) tartományban az adott polinom grafikonját.

A grafikon megrajzolását `canvas` techonológiával kell megoldani.

### Értékelési szempontok

* A szükséges paramétereket meg lehet adni az űrlapmezőkön keresztül
* A gomb megnyomására valamilyen grafikon megjelenik
* A grafikonon tengelyek látszanak
* A tengelyeknek valamilyen osztásköze látszik
* A tengelyeken látszik, hogy mettől meddig (**_x<sub>1</sub>, x<sub>2</sub>_**) van ábrázolva a polinom
* A polinom bizonyos pontjai helyesen megjelennek
* A polinom helyesen, összefüggően kirajzolódik
* A grafikon **_x_** irányban automatikusan méreteződik, hogy a polinom beleférjen
* A grafikon **_y_** irányban automatikusan méreteződik, hogy a polinom beleférjen
* Nincsenek fura jelenségek, bugok

## Beadandó feladat: PHP

### Feladat

A feladatod, hogy készíts egy egyszerű időpont-foglaló rendszert. Az alkalmazásban egy táblázatban jelennek meg a foglalható időpontok a hét minden napjára 8-20 óra között egy órás bontásban. A táblázat mellett egy űrlap látható, melyen a név, az adott nap és azon belül az adott időpont (óra) kiválasztásával lehet foglalni időpontot. Az "elküldés" gombra kattintva tároljuk el, hogy ki és melyik időpontra jelentkezett. Ha hiba történt (nem megfelelően kitöltött adatok, nem szabad az időpont) azt megfelelő hibaüzenettel jelezzük. A rögzített foglalások a táblázatban színes háttérrel jelenjenek meg és tartalmazzák a foglaló nevét. A foglalásra kattintva azt lehessen törölni, illetve legyen lehetőség az összes foglalás egyidejű törlésére is.

Az adatokat **adatbázisban** kell tárolni.

### Értékelési szempontok

* Az űrlapon megadhatóak a foglaláshoz szükséges adatok
* Létezik az adatbázis és alkalmas a szükséges adatok tárolására
* A gomb megnyomására az adatok eltárolódnak az adatbázisban
* Hibás bemenet esetén azt megfelelő hibaüzenet jelzi
* Hibaüzenet jelzi, ha a foglalni kívánt időpont már nem üres
* A foglalások megjelennek a táblázatban, látszik a foglaló neve
* Egy foglalás törölhető ha rákattintunk
* Van lehetőség az összes foglalás törlésére
* Nincsenek fura jelenségek, bugok

## A beadandók értékelése

* A beadandók értékelése jeggyel történik: 1-5 jegy kapható rá.
* Az értékelés egy mindenki számára elérhető szempontok alapján történik.
* A beadandókat határidőre kell elkészíteni.
* A beadandókat a webprogramozás szerverre kell feltölteni a [feltöltő felületen](http://webprogramozas.inf.elte.hu/ebr) keresztül.
* A beadandók plágiumellenőrzésen mennek keresztül az esetleges másolásokat kiszűrendő.
* A beadandók készítőit szükség esetén megkérhetjük megoldásaik megvédésére.

## Jegyszerzés feltételei

* Részvétel a gyakorlatok legalább 75%-án (maximum 3 hiányzás)
* Három elfogadott beadandó

## Értékelés

* A három beadandó feladat jegyének átlaga

# Előadások

{% include lectures-external.html %}

# Segédanyagok

## Elektronikus tananyag

* [Bevezetés a kliens- és szerveroldali webalkalmazások készítésébe (elektronikus tananyag)](http://webprogramozas.inf.elte.hu/tananyag/wf2/index.html)

# Oktatók

## Előadó

Horváth Győző

## Gyakorlatvezető

Visnovitz Márton
