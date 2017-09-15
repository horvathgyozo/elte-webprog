---
layout: default
title: Webprogramozás az ELTE IK-n
---

<section id="nav">
    <ul class="nav nav-justified">
        {% for page in site.subjects %}
            <li role="presentation">
                <a href="{{ page.permalink }}" class="nav-item nav-link text-white">{{ page.title }}</a>
            </li>
        {% endfor %}
    </ul>
</section>

<section class="text-center feher">
    <h2>Tárgyak</h2>
    <div class="container">
        <div class="row text-center equal">
            {% for page in site.subjects %}
                {% if page.shortdesc %}
                    <div class="col-sm-6 col-md-4">
                        <div class="thumbnail">
                            <div class="caption">
                                <h3>{{ page.title }}</h3>
                                <p>{{ page.shortdesc }}</p>
                                <a href="{{ page.permalink }}" class="btn btn-primary" role="button">
                                    Továbblépés az oldalra
                                </a>
                            </div>
                        </div>
                    </div>
                {% endif %}
            {% endfor %}
        </div>
    </div>
</section>

<section class="text-center kek">
    <div class="container">
        <h2>Tananyagok</h2>
    </div>
</section>

<section class="text-center sarga">
    <div class="container">
        <div class="col-md-6 col-md-offset-3">
            <h2>Projektek</h2>
            <p>A webes szoftvertechnológia labor keretében lehetőség van különböző webes projektekben részt venni. A projektek elsősorban a frontendre fókuszálnak, szerveroldalon az üzleti rétegig terjednek.</p>
            <a href="" class="btn btn-primary">Projektleírások</a>
        </div>
    </div>
</section>

