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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 32%

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

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden die beiden mathematischen Funktionen dokumentiert, die in AJO-Journey-Ausdrücken verfügbar sind: `random` zum Generieren einer zufälligen Dezimalzahl zwischen 0 und 1 und `round` zum Runden einer Dezimalzahl oder Ganzzahl auf die nächste Ganzzahl.

**intents:**
* Generieren eines zufälligen Dezimalwerts zwischen 0 und 1 für die Sampling- oder Randomisierungslogik mithilfe von `random`
* Eine Dezimalzahl mithilfe von `round` auf die nächste Ganzzahl runden
* Rundung in der Geschäftslogik anwenden, wenn ganze Zahlen aus Dezimalberechnungen erforderlich sind

**Glossar:**
* **random**: Eine Funktion, die einen pseudo-zufälligen Dezimalwert von 0 (einschließlich) bis 1 (ausschließlich) *(produktspezifisch) zurückgibt*
* **round**: Eine Funktion, die die nächste Ganzzahl zur Eingabe zurückgibt, wobei die Halbwerte auf eine positive Unendlichkeit gerundet werden

**Leitplanken:**
* `random()` akzeptiert keine Parameter
* `round` akzeptiert eine Dezimal- oder Ganzzahleingabe und gibt immer eine Ganzzahl zurück.
* Bindungen in `round` werden durch Rundungen in Richtung positiver Unendlichkeit aufgelöst (z. B. 3,5 auf 4, -3,5 auf -3)

**Terminologie:**
* Kanonische Bezeichnung: Mathematische Funktionen — Akronym: none — Varianten: Mathematische Funktionen, numerische Funktionen
* Synonyme: „round“ = „auf nächste ganze Zahl runden“
* Verwechseln Sie dies nicht: „round“ (rundet auf die nächste ganze Zahl) ≠ Konversionsfunktionen wie `toInteger` (kürzt den Dezimalteil ohne Rundung)

**FAQ:**
* **F: Was gibt `random()` zurück?** — Gibt eine zufällige Dezimalzahl zwischen 0 und 1 zurück.
* **F: Wie behandelt `round` negative Zahlen?** — Er rundet auf positive Unendlichkeit, sodass `round(-3.14)` -3 zurückgibt und `round(-3.54)` ebenfalls -3 zurückgibt (engste Ganzzahl auf positive Unendlichkeit).
* **F: Was ist der Unterschied zwischen `round` und `toInteger`?** — `round` rundet auf die nächste Ganzzahl (3,7 wird zu 4), während `toInteger` den Dezimalteil ohne Rundung abschneidet (3,7 wird zu 3).
* **F: Nimmt `random` Parameter?** — Nein, `random()` erfordert keine Parameter und gibt immer eine Dezimalzahl zwischen 0 und 1 zurück.

+++
