---
layout: subject
title: Webfejlesztés 2. (PTI)
permalink: webfejl2_pti.html
toc: true
shortdesc: >
    Bevezetés a dinamikus kliens- és szerveroldali programozás világába. Alapvető JavaScript és PHP ismeretek.
lectures:
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

<div class="list-group">
    {% for lecture in page.lectures %}
        <a href="{{ lecture.permalink }}" class="list-group-item">
            {{ lecture.title }}
            <span class="glyphicon glyphicon-menu-right pull-right" aria-hidden="true"></span>
        </a>
    {% endfor %}
</div>

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

Bende Imre
Demsa Miklós
Kereszti Krisztián
Kereszti Zalán
Horváth Győző
Rakonczai Sándor
[Visnovitz Márton](https://github.com/vimtaai/elte/tree/master/2017-18-2)
