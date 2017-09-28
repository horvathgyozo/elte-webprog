---
title: Webes szoftvertechnológia labor
layout: subject
permalink: /webtech.html
---

# Leírás

A webes szoftvertechnológia labor keretében lehetőség van különböző webes projektekben részt venni. A projektek elsősorban a frontendre fókuszálnak, szerveroldalon az üzleti rétegig terjednek. A labor tématerületei:

* webes frontendek fejlesztése
* webes adatok vizualizációja
* banki informatika
* webes startupok világa

# Projektek

<div class="list-group">
  {% for project in site.projects %}
      <a href="{{ project.permalink }}" class="list-group-item">
        <span class="pull-right">
          {% for tag in project.tags %}
            <span class="label label-{{ tag.context }}">{{ tag.label }}</span>
          {% endfor %}
          <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
        </span>
        <strong class="list-group-item-heading">{{ project.title }}</strong>
        <br>
        <br>
        <p class="list-group-item-text"><small>{{ project.shortdesc }}</small></p>
      </a>
  {% endfor %}
</div>