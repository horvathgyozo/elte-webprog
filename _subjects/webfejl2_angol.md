---
layout: subject
title: Web Development 2.
permalink: webdev.html
toc: true
lectures:
---

# General information

Classes
: 1 lecture + 2 practice + 1 consultation

Prerequisite
: Web Development 1

Goals
: Learning the basics of dynamic client and server side web-programming. The first part of the semester introduces the JavaScript programming language and related web technologies, the second part is about server side web programming through the PHP programming language.

Environment
: Server side dynamic websites are hosted on the webprogramozas.inf.elte.hu server. The server runs Nginx and PHP version 7. Every student is provided with credentials to access the server. The credentials expire at the end of the semester.

# Requirements

<!--Összevont (folyamatos) értékelésű tárgy.

## Az értékelés összetevői

* Beadandó feladat: JavaScript (DOM)
    Határidő: 2017. november 19. éjfél
* Beadandó feladat: JavaScript (canvas)
    Határidő: 2017. december 31. éjfél  
* Beadandó feladat: PHP
    Határidő: 2018. január 21. éjfél


## A beadandók értékelése

* A beadandók értékelése jeggyel történik: 1-5 jegy kapható rá.
* Az értékelés egy mindenki számára elérhető szempontok alapján történik.
* A beadandókat határidőre kell elkészíteni.
* A beadandókat a webprogramozas szerverre kell feltölteni a [feltöltő felületen](http://webprogramozas.inf.elte.hu/ebr) keresztül.
* A beadandók plágiumellenőrzésen mennek keresztül az esetleges másolásokat kiszűrendő.
* A beadandók készítőit szükség esetén megkérhetjük megoldásaik megvédésére.

## Jegyszerzés feltételei

* Részvétel a gyakorlatok legalább 75%-án (maximum 3 hiányzás)
* Három elfogadott beadandó

## Értékelés

* A három beadandó feladat jegyének átlaga

-->

# Lectures

<div class="list-group">
    {% for lecture in page.lectures %}
        <a href="{{ lecture.permalink }}" class="list-group-item">
            {{ lecture.title }}
            <span class="glyphicon glyphicon-menu-right pull-right" aria-hidden="true"></span>
        </a>
    {% endfor %}
</div>

<!--
# Segédanyagok

## Elektronikus tananyag

* [Bevezetés a kliens- és szerveroldali webalkalmazások készítésébe (elektronikus tananyag)](http://webprogramozas.inf.elte.hu/tananyag/wf2/index.html)

# Oktatók

## Előadó

Horváth Győző

## Gyakorlatvezető

Horváth Győző

-->