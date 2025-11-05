---
product: journey optimizer
title: Mathematische Funktionen
description: Erfahren Sie mehr über mathematische Funktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Mathematisch, Funktionen, Ausdruck, Journey, Berechnung, Zahl
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 35%

---

# Mathematische Funktionen {#math-functions}

Mathematische Funktionen bieten wichtige mathematische Operationen für numerische Berechnungen in Ihren Journey-Ausdrücken. Mit diesen Funktionen können Sie präzise numerische Berechnungen und Umwandlungen an Ihren Daten durchführen.

Verwenden Sie mathematische Funktionen, wenn Sie Folgendes tun müssen:

* Generieren von Zufallswerten für Tests, Stichproben oder Randomisierung ([random](#random))
* Dezimalzahlen werden auf die nächste Ganzzahl gerundet, um die Datendarstellung zu vereinfachen ([round](#round))
* Durchführen mathematischer Berechnungen für numerische Felder
* Transformieren numerischer Werte für Geschäftslogik und Entscheidungsfindung

Mathematische Funktionen verarbeiten sowohl Dezimal- als auch Ganzzahltypen und verwalten automatisch Typkonvertierungen, um präzise Ergebnisse in Ihren Journey-Ausdrücken sicherzustellen.

## random {#random}

Generiert eine zufällige Zahl zwischen 0 und 1.

+++Syntax

`random()`

+++

+++Signatur und zurückgegebener Typ

`random()`

Gibt eine Dezimalzahl zurück.

+++

## round {#round}

Gibt den nächstgelegenen ganzzahligen Wert für das Argument zurück, wobei gleiche Werte auf positive Unendlichkeit gerundet werden.

+++Syntax

`round(<parameters>)`

+++

+++Parameter

* decimal
* integer

+++

+++Signaturen und zurückgegebener Typ

`round(<decimal>)`

`round(<integer>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`round(3.14)`

Gibt 3 zurück.

`round(3.54)`

Gibt 4 zurück.

`round(-3.14)`

Gibt -3 zurück.

`round(3)`

Gibt 3 zurück.

+++

