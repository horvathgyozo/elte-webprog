---
title: Webes alkalmazásfejlesztés 1.
toc: true
shortdesc: >
    Kliens- és szerveroldali programozás magasabb szinten. Modern programozási minták a JavaScript és PHP programozásának világában.
lectures:
  - title: 1. Bevezetés, követelmények, JavaScript nyelvi alapok
    permalink: webfejl2/ea/01/
  - title: Követelmények ismertetése. JavaScript nyelvi alapok
    permalink: weaf1/ea/weaf1_01.pdf
  - title: JavaScript: függvények
    permalink: weaf1/ea/weaf1_02.pdf
  - title: JavaScript: objektumok
    permalink: weaf1/ea/weaf1_03.pdf
  - title: JavaScript: BOM és DOM (jQuery)
    permalink: weaf1/ea/weaf1_04.pdf
  - title: JavaScript: objektumok létrehozása klasszikus OOP stílusban. Kódszervezés. Modularizált JavaScript.
    permalink: weaf1/ea/weaf1_05.pdf
  - title: JavaScript: Programozási és tervezési minták. jQuery plugin készítés
    permalink: weaf1/ea/weaf1_06.pdf
  - title: Nagy méretű kliensoldali webes alkalmazások
    permalink: weaf1/ea/weaf1_07.pdf
  - title: PHP nyelvi elemei (ismétlés). PHP a webszerveren. Webes alkalmazások és adatbázis. PHP és adatbázis (MySQL).
    permalink: weaf1/ea/weaf1_09.pdf
  - title: Model-View-Controller minta. MVC keretrendszerek. CodeIgniter keretrendszer bemutatása.
    permalink: weaf1/ea/weaf1_10.pdf
  - title: Saját MVC-s keretrendszer (miniMVC), MVC minta finomítása, egyéb funkciók beillesztése az MVC mintába. További funkciók helye az MVC mintában. CodeIgniter plusz tulajdonságok.
    permalink: weaf1/ea/weaf1_11.pdf
  - title: AJAX: elvek, megvalósítások, keretrendszerek. Aszinkronitás kezelése.
    permalink: weaf1/ea/weaf1_12.pdf
  - title: Weboldalak progresszív fejlesztése.
    permalink: weaf1/ea/weaf1_13.pdf
practices:
  - title: Nyelvi alapok
    permalink: weaf1/gyak/weaf1_02_feladatsor.html
  - title: A HTML dokumentum módosítása JavaScripttel jQuery keretrendszer segítségével. DOM és BOM.
    permalink: weaf1/gyak/weaf1_04_feladatsor.html
  - title: JavaScript programozási minták és alkalmazásai.
    permalink: weaf1/gyak/weaf1_06_feladatsor.html
  - title: MVC gyakorlása
    permalink: weaf1/gyak/weaf1_07_feladatsor.html
  - title: Adatbázis elérés PHP-ból. MVC alapok. PDO. CodeIgniter bevezető
    permalink: weaf1/gyak/weaf1_09_feladatsor.html
  - title: CodeIgniter és adatbázis
    permalink: weaf1/gyak/weaf1_11_feladatsor.html
  - title: Sablonkezelés. Hitelesítés, jogosultságkezelés. AJAX.
    permalink: weaf1/gyak/weaf1_13_feladatsor.html
---

# Általános információk

Óraszám
: 1 előadás + 1 gyakorlat

Feltételezett ismeretek
: HTML, CSS, alapszintű JavaScript és PHP

Célkitűzés
: Korszerű programozási minták a kliens- és szerveroldali dinamikus webprogramozásban. A félév első felében a modern JavaScript programozással és a hozzá kapcsolódó korszerű webes technológiákkal és programozási mintákkal ismerkednek meg a hallgatók, a félév második felében a PHP nyelven keresztül vesszük végig a szerveroldali webprogramozás során alkalmazott korszerű tervezési mintákat.

Környezet
: A szerveroldali dinamikus weblapok készítését a webprogramozas.inf.elte.hu szerver segítségével végezzük el. A szerveren Nginx webszerver, 7-es verziójú PHP fut. A szerverre a félév elején, a gyakorlati jelentkezések lejártakor minden hallgató kap hozzáférést.

# Számonkérés

Összevont (folyamatos) értékelésű tárgy.

## Az értékelés összetevői

* Beadandó feladat: JavaScript
    Határidő: TBA
* Beadandó feladat: PHP
    Határidő: TBA

<!-- 
## Az értékelés összetevői

- Évfolyam zh: JavaScript 
- 2017. május 16. kedd, 14-16, PC5
- Évfolyam zh: PHP 
- 2017. április 4. kedd, 14-16, PC5
- Összetett beadandó feladat 
- Időpont: egyeztetés alatt...
- JavaScript pót zh 
- Időpont: egyeztetés alatt...
- PHP pót zh 
- Időpont: egyeztetés alatt...

## Az évfolyam zh-k és beadandók értékelése

- 1-től 5-ig
- A beadandókat a webprogramozas szerverre kell feltölteni. Elkészültéről értesíteni kell a gyakorlatvezetőt.

## Jegyszerzés feltételei

- Részvétel a gyakorlatok legalább 75%-án (maximum 3 hiányzás)
- Két megírt évfolyam zh
- Elfogadott beadandó

## Értékelés

- A 2-es érdemjegyhez legalább 2-esre megírt évfolyamzh-k és beadandó szükségesek.
- Az érdemjegy a háromféle számonkérés átlagából adódik.
-->
# Előadások

{% include lectures-external.html %}

# Gyakorlatok

<div class="list-group">
  {% for practice in page.practices %}
      <a href="{{ practice.permalink }}" class="list-group-item">
          <strong>{{ practice.title }}</strong>
          <span class="glyphicon glyphicon-menu-right pull-right" aria-hidden="true"></span>
      </a>
  {% endfor %}
</div>

# Segédanyagok

## Elektronikus tananyag

* [Modern programozási minták a kliens és szerveroldali webprogramozásban (elektronikus tananyag)](http://webprogramozas.inf.elte.hu/user/gyozke/honlap_backup/tananyag/weaf1/index.html)

# Oktatók

## Előadó

Horváth Győző

## Gyakorlatvezetők

* Horváth Győző
