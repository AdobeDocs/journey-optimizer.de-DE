---
title: Häufig gestellte Fragen zu Entscheidungen
description: Erhalten Sie Antworten auf häufig gestellte Fragen zu Entscheidungsfunktionen
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 7205017785283e3db4d64ed595ac8f187f43307b
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Häufig gestellte Fragen zu Entscheidungen {#decisioning-faq}

Auf dieser Seite finden Sie Antworten auf häufig gestellte Fragen zu den Entscheidungsfunktionen in Adobe Journey Optimizer.

## Begrenzungsregeln {#capping-rules}

+++**Was passiert, wenn mehrere Begrenzungsregeln auf ein einzelnes Angebot angewendet werden?**

Ein Angebot wird begrenzt, sobald **eine einzelne Bedingung erfüllt ist**. Wenn mehrere Begrenzungsregeln vorhanden sind, wird das Angebot nicht mehr angezeigt, sobald eine Regel ihren Schwellenwert erreicht.

**Beispiel:**
Wenn Sie zwei Begrenzungsregeln für ein Angebot definieren:
* 5-mal pro Profil pro Woche
* 100-mal über alle Benutzer hinweg

Das Angebot wird einem Benutzer nicht mehr angezeigt, sobald er es fünf Mal in einer Woche gesehen hat, selbst wenn die Gesamtobergrenze von 100 noch nicht erreicht wurde. Wenn erst einmal 100 Impressions insgesamt erreicht sind, wird das Angebot nicht mehr für alle Benutzer angezeigt.

Weitere Informationen zu [Begrenzungsregeln](items.md#capping).

+++

## Rangfolgenformeln {#ranking-formulas}

+++**Welche Rolle spielen Zielgruppen in KI-Modellen?**

Beim Konfigurieren [personalisierter Optimierungsmodelle](ranking/personalized-optimization-model.md) dienen sowohl Datensätze als auch Zielgruppen unterschiedlichen Zwecken:

* **Datensätze**: Erfasst Konversionsereignisse (Klicks, Bestellungen, Umsatz), die als Optimierungsziele für das Modell dienen.
* **Zielgruppen**: Sie dienen als Prädiktorvariablen, mit denen das Modell Empfehlungen basierend auf der Zugehörigkeit zu einem Kundensegment personalisieren kann.

Zielgruppen schränken den Umfang des Modells nicht ein und erweitern ihn nicht. Stattdessen bieten sie kontextuelle Attribute, die die Fähigkeit des Modells verbessern, personalisierte Prognosen über verschiedene Kundensegmente hinweg zu erstellen.

Beide Komponenten sind für eine effektive Leistung des personalisierten Optimierungsmodells erforderlich. Weitere Informationen zu [KI-Modellen](ranking/ai-models.md).

+++

+++**Wie wirken sich Änderungen an Angebotssammlungen auf KI-Modelle aus, wenn Modelle für die automatische Optimierung oder die personalisierte Optimierung verwendet werden?**

Beide Modelle liefern Traffic zum nächstbesten verfügbaren Angebot, das auf Traffic-Daten der letzten 30 Tage basiert.

Wenn mehrere Angebote gleichzeitig entfernt werden und die verbleibenden Angebote innerhalb des 30-tägigen Fensters minimale Traffic-Daten haben, kann das Modell ein suboptimales Verhalten aufweisen, darunter:
* Zufällige Verteilungsmuster
* Tendenz zu Angeboten mit höheren Konversionsraten auf der Basis begrenzter Impression-Daten

**Best Practice**: Wenn Sie Angebotssammlungen erheblich ändern, überprüfen Sie, ob die verbleibenden Angebote über ausreichende historische Leistungsdaten verfügen, um die Modelleffektivität aufrechtzuerhalten.

+++

+++**Wie schnell binden KI-Modelle neue Angebote ein?**

KI-Modelle identifizieren und beginnen mit dem Testen neu verfügbarer Angebote im nächsten Trainings-Zyklus:

* **Automatische Optimierung**: Tägliche Trainings-Läufe
* **Personalisierte Optimierung**: Wöchentliche Trainings-Läufe

Sobald sie identifiziert sind, beginnen beide Modelle sofort damit, einigen Besuchern die neuen Angebote zu unterbreiten, um ihre Leistung zu testen und Daten über ihre Effektivität zu sammeln.

Erfahren Sie mehr über [automatische Optimierung](ranking/auto-optimization-model.md) und [personalisierte &#x200B;](ranking/personalized-optimization-model.md)).

+++

+++**Wie optimieren KI-Modelle ohne Kontrollgruppen?**

Sowohl Modelle für die automatische Optimierung als auch für die personalisierte Optimierung verwenden eine Explore-Exploit-Strategie, die keine dedizierten Kontrollgruppen mehr erfordert:

* **Anfangsphase**: Die Modelle beginnen mit einer 100%igen Untersuchung und testen verschiedene Angebote, um grundlegende Leistungsdaten zu ermitteln.
* **Adaptive Optimierung**: Wenn sich Verhaltensereignisse akkumulieren und die Prognosegenauigkeit steigt, gleichen Modelle automatisch Exploration und Exploitation aus.
* **Fortlaufendes Lernen**: Das System ordnet nach und nach leistungsstarken Angeboten mehr Traffic zu und testet gleichzeitig weiterhin Alternativen.

Dadurch wird ein kontinuierliches Lernen und eine Optimierung über den gesamten Traffic hinweg sichergestellt, ohne dass separate Kontrollgruppen erforderlich sind.

+++

+++**Was sind die minimalen Traffic-Anforderungen für eine optimale KI-Modellleistung?**

Adobe empfiehlt die folgenden Mindestschwellenwerte, um eine effektive Modellleistung sicherzustellen:

**Empfohlene Mindestwerte (pro Woche):**
* 1.000 Impressionen pro Angebot/Element
* 100 Konversionsereignisse pro Angebot/Element

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Standardmäßig versucht das System nicht, personalisierte Modelle für Angebote/Elemente mit weniger als 1.000 Impressionen oder 50 Konversionsereignissen zu erstellen.

>[!NOTE]
>
>In Produktionsumgebungen mit großen Angebotskatalogen (~300 Angebote) und restriktiven Geschäftsregeln können einige Angebote niedrigere absolute Schwellenwerte erreichen (250 Impressions und 25 Konversions pro 30 Tage). Diese stellen die Mindestanforderungen an die Daten für das Modell-Training dar, garantieren jedoch möglicherweise keine optimale Leistung.

Weitere Informationen zu [Datenerfassungsanforderungen](data-collection/data-collection.md).

+++

+++**Wie wirkt sich die Ähnlichkeit der Angebote auf die Leistung des KI-Modells aus?**

KI-Modelle bieten größere Personalisierungsvorteile, wenn sie für unterschiedliche Kundensegmente interessant sind. Wenn Angebote sich stark ähneln, sind zwei Ergebnisse typisch:

* **Gleichwertige Leistung**: Angebote funktionieren genauso und erhalten annähernd die gleiche Traffic-Verteilung.
* **Dominantes Angebot**: Geringfügige Unterschiede führen dazu, dass ein Angebot andere in allen Segmenten übertrifft und den Großteil des Traffics erfasst.

>[!NOTE]
>
>Eine ausgewogene Traffic-Verteilung ist durch die Differenzierung des Angebots nicht gewährleistet. Angebote mit objektiv höherwertigen Angeboten (z. B. 100 € Rabatt gegenüber 50 € Rabatt) dominieren in der Regel über alle Kundensegmente hinweg, unabhängig vom Personalisierungsaufwand.

**Best Practice**: Entwerfen Sie Angebote mit aussagekräftiger Differenzierung, die mit unterschiedlichen Kundensegmentpräferenzen übereinstimmen, um die Effektivität des KI-Modells zu maximieren.

+++

+++**Wie wirken sich Traffic-Anomalien auf die KI-Modellleistung aus?**

Traffic-Anomalien werden proportional innerhalb des 30-tägigen rollierenden Fensters in das Modell integriert.

**Folgenabschätzung:**
Eine temporäre Traffic-Spitze (z. B. 2x täglicher Traffic) hat minimale Auswirkungen auf die Gesamtmodellleistung, da der anomale Traffic einen kleinen Bruchteil des 30-Tage-Datensatzes ausmacht.

**Wichtige insight**: Das rollierende 30-Tage-Datenfenster bietet Modellstabilität bei temporären Traffic-Schwankungen. Kurzfristige Spitzen oder Rückgänge stören die Modellvorhersagen oder die Leistung nicht wesentlich.

+++
