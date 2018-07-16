---
title: "Office 365"
date: 2018-07-16T16:29:20+02:00
draft: true
description: "Umstellung auf Office 365"
tags: ["IT40","Office","Cloud"]
menu:
  main:
    parent: 'it40'
    weight: 1
---

## Aktuelle konfiguration

### Office

Aktuell ist auf jedem Clientrechner eine Office Lizenz installiert. Die Lizenzen kommnen aus dem Microsoft Partner Programm. 

> Problem 1: Sollte das Programm nicht mehr verlängert werden können, muss für jeden Rechner eine Lizenz erworben werden.

> Problem 2: Eine Zusammenarbeit ist aussschliesslich über Netzlaufwerke möglich und erfordert bei externem Zugriff eine VPN Verbindung.

### E-Mail

Bei der E-Mail Kommunikation sind folgende Komponenten beteiligt:

1. Der **AlfaHosting Server** nimmt eingehende Mails entgegen und speichert sie in einem **POP3 Postfach**
1. Auf dem **Exchange Server** läuft die Software **POPCon**, welche die E-Mails alle 5 Min. abholt und in **Exchange Postfächer** einsortiert
1. Der **Exchange Server** übernimmt die interne bearbeitung der Mails und dient als Speicher für **Kontakte**
1. Die Software **CodeTwo Exchange Rules** läuft auch auf dem **Exchange Server** und hängt die zentrale Signatur an alle ausgehenden E-Mails an
1. Der **Exchange Server** übermittelt ausgehende E-Mails an den **AlfaHosting Server**

> Problem 1: Latenzzeit von 5 Min.

> Problem 2: Exchange 2010 muss upgedated werden.

> Problem 3: CodeTwo Exchange Rules ist nicht mit aktuellen Office Versionen kompatibel.

## Lösung mit Office 365

Eine Umstellung auf Office würde folgende Vorteile mit sich bringen:

1. Wegfall des **Exchange Servers**
1. Wegfall der **POPCon** Software
1. Wegfall der **CodeTwo Exchange Rules** Software
1. Reduzierung der Last auf dem Virtualisierungsserver
1. Evtl. wegfall der Notwendigkeit der Redundanz
1. Office Online und Lokal in aktuellster Version nutzbar
1. Lizenzierung flexibel anpassbar

Es gibt aber auch ein paar Nachteile zu beachten:

1. Eine Umstellung kann nicht successive erfolgen, sondern muss in einem Rutsch gemacht werden.
1. Das Office 365 aus dem Microsoft Partnerprogramm liegt nicht auf deutschen Servern. 
1. Was passiert bei einem Wegfall der Partnerschaft?
1. Backup noch ungeklärt.
1. Zentrale Signatur ist möglich, aber nur umständlich über PowerShell Kommandos zu realisieren.

### Kosten

Ausgehend von der aktuell verfügbaren Microsoft Partner Lizenzierung, die 25 User beinhaltet, ergeben sich die folgenden Kosten:

|Produkt                            |Land|Benutzer/Monat|Benutzer|Monat   |1 Jahr    |3 Jahre     |
|-----------------------------------|----|-------------:|-------:|-------:|---------:|-----------:|
|Office 365 Enterprise E3           |USA |0,00€         |25	     |0,00€   |0,00€     |0,00€       |
|Office 365 Enterprise E3           |USA |19,70€        |25	     |492,50€ |5.910,00€ |17.730,00€  |
|Office 365 Business Premium        |USA |10,50€        |25	     |262,50€ |3.150,00€ |9.450,00€   |
|Office 365 Business Premium        |DE  |13,20€        |25	     |330,00€ |3.960,00€ |11.880,00€  |
|Office 365 Business Premium Telekom|DE  |11,95€        |25      |298,75€ |3.585,00€ |10.755,00€  | 

Bei einer neu Lizenzierung mit 15 Usern entstehen folgende Kosten:

|Produkt                            |Land|Benutzer/Monat|Benutzer|Monat   |1 Jahr    |3 Jahre     |
|-----------------------------------|----|-------------:|-------:|-------:|---------:|-----------:|
|Office 365 Business Premium        |USA |10,50€        |15	     |157,50€ |1.890,00€ |5.670,00€   |
|Office 365 Business Premium        |DE  |13,20€        |15	     |198,00€ |2.376,00€ |7.128,00€   |
|Office 365 Business Premium Telekom|DE  |11,95€        |15	     |179,25€ |2.151,00€ |6.453,00€   |
