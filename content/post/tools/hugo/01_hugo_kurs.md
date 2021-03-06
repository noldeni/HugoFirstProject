---
title: "Udemy Hugo Kurs"
date: 2018-07-16T16:20:08+02:00
draft: true
description: "Zusammenfassung des Udemy Kurses -Deine kostenlose Webseite mit Hugo und GitHub Pages-"
tags: ["Udemy","Hugo"]
---

## Tips

* `ctrl-u` öffnet Quelltext im Browser
* [Wordpress hacken](https://wpscan.org/)
* [Offene Sicherheitslücken](http://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=wordpress)
* VSCode: `strg-ö` Terminalfenster ein/ausschalten
* [Kostenlose Bilder](https://unsplash.com)

## Projekt starten

* `hugo new site HugoFirstProject --force` (force bei existierendem Projekt)

## Themes

* `cd themes && git submodule add https://github.com/halogenica/beautifulhugo.git`
* _config.toml_ ergänzen: `theme = "beautifulhugo"`

## Inhalt

* `hugo new post/2018/07/01_erster_post.md` (Verzeichnisse werden angelegt)
* `hugo` -> generiert alle Seiten im _public_ Ordner

## Konfiguration

* Globale Konfiguration in `config.toml`

