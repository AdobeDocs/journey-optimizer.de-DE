---
product: journey optimizer
title: Mathematische Funktionen
description: Erfahren Sie mehr über mathematische Funktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Mathematik, Funktionen, Ausdruck, Journey, Berechnung, Zahl
version: Journey Orchestration
exl-id: da710b22-3112-41fe-8b91-2b6563b79f27
TQID: https://experienceleague.adobe.com/POIbPCZrqtqGjHqn3ehGonxwv9KhKWlgg2igdN8Y4yw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 100%

---

# Mathematische Funktionen {#math-functions}

Mathematische Funktionen bieten wichtige mathematische Operationen für numerische Berechnungen in Ihren Journey-Ausdrücken. Mit diesen Funktionen können Sie präzise numerische Berechnungen und Umwandlungen an Ihren Daten durchführen.

Verwenden Sie mathematische Funktionen, wenn Sie Folgendes tun müssen:

* Generieren von Zufallswerten für Tests, Stichproben oder Randomisierung ([random](#random))
* Runden von Dezimalzahlen auf die nächste Ganzzahl, um die Datendarstellung zu vereinfachen ([round](#round))
* Durchführen von mathematischen Berechnungen für numerische Felder
* Umwandeln von numerischen Werten für Geschäftslogik und Entscheidungsfindung

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

Gibt den nächsten ganzzahligen Wert für das Argument zurück, wobei gleiche Werte auf positive Unendlichkeit gerundet werden.

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
