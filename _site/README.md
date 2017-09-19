# Webprogramozás weboldal - Jekyll guide

## Buildelés

```
bundle exec jekyll build
```

## Buildelés és kiszolgálás

```
bundle exec jekyll serve
```

## Tantárgyak

Minden egyes tantárgynak egy saját `.md` file-ja van az `_subjects` mappában.
Minden fájlból saját link generálódik a főoldalon, illetve azon tárgyak, melyek rendelkeznek rövid leírással, azok kártyaként is megjelennek a "Tárgyak" részben.

Minden egyes `.md` fájlnak kell legyen egy "Front matter" része, ami az alábbi információkat kell tartalmazza:

```xml
---
layout: subject
title: <az adott tárgy neve>
permalink: <az adott tárgy linkje>
toc: <true|false - legyen-e automatikus tartalomjegyzék>
shortdesc: >
  <rövid leírás - opcionális>
---
```

## Tananyagok

Minden egyes tananyagnak egy saját `.md` file-ja van az `_materials` mappában. Ezek a fájlok nem kerülnek renderelésre, csak metaadatokat tartalmaznak és "külső" oldalakra linkelnek. Ezeket a külső oldalakat el lehet helyezni a Jekyll projekt root mappájába, ha nem `_`-ral kezdődik a mappa neve, akkor automatikusan renderelésre kerül.

Minden egyes `.md` fájlnak az alábbi "Front matter" információkat kell tartalmaznia:

```xml
title: <az adott tananyag neve>
permalink: <az adott tananyag elérési útja>
shortdesc: >
  <az adott tananyag rövid leírása>
```

## Projektek

Minden egyes projektnek egy saját `.md` file-ja van az `_projects` mappában.

