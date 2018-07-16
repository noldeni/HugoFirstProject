---
title: "Cloudstorage"
date: 2018-07-16T16:30:06+02:00
draft: true
description: "Auslagerung von Storage in die Cloud"
tags: ["IT40","Cloud","Storage"]
menu:
  main:
    parent: 'it40'
    weight: 2
---

## Rackstation1

Auf der Rackstation1 sind momentan folgende Volumes eingerichtet:

|Device             |Size  |Used  |Free  |%Free|Volume  |
|-------------------|-----:|-----:|-----:|----:|--------|
|/dev/vg1/volume_1  | 2.0T | 776G | 1.3T | 39% |/volume1|
|/dev/vg1/volume_2  |  99G |  33G |  67G | 33% |/volume2|
|/dev/vg1/volume_3  |  99G |  74G |  25G | 76% |/volume3|
|/dev/vg1/volume_5  |  50G |  27G |  23G | 54% |/volume5|
|/dev/vg1/volume_4  |1008G | 875G | 134G | 87% |/volume4|
|/dev/vg1/volume_6  | 689G | 477G | 213G | 70% |/volume6|
|/dev/vg1/volume_7  | 493G | 7.2G | 485G |  2% |/volume7|
|/dev/vg1/volume_10 | 296G |  77G | 219G | 27% |/volume10|
|/dev/vg1/volume_8  | 2.0T | 805G | 1.2T | 41% |/volume8|
|/dev/vg1/volume_9  | 493G | 269G | 223G | 55% |/volume9|

## Cloud

Davon können folgende Verzeichnisse in die Cloud ausgelagert werden:

|Size|Directory|
|------:|---------------------|
|74.0G  |/volume3/Deltacontrol|
|26.0G  |/volume5/Temp|
|269.0G |/volume9/Projekte|
|77.0G  |/volume10/homes|
|446.0G |Gesamt|

## Lokal

Die folgenden Verzeichnisse sollten lokal bleiben:

|Size|Directory|
|------:|---------------------|
|  2.3G| /volume1/AbteilungGF|
| 29.0G| /volume1/AbteilungKA|
|738.0G| /volume1/Projektarchiv|
|  2.1G| /volume1/surveillance|
|  4.4G| /volume1/SFirmV3|
| 32.0G| /volume2/Adminshare|
|874.0G| /volume4/Software|
|480.0K| /volume5/Scannerfiles|
|476.0G| /volume6/ISO-Store1|
|  6.7G| /volume7/ondesostore1|
|805.0G| /volume8/vBackup|
|G|Gesamt|

## Kostenschätzung

TODO