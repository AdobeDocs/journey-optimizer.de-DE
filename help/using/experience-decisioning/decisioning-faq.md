---
title: Häufig gestellte Fragen zur Entscheidungsfindung
description: Erhalten Sie Antworten auf häufig gestellte Fragen zu Entscheidungsfunktionen
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: 7bb72527-d4e1-49f8-b2c3-c943d65903f2
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 100%

---

# Häufig gestellte Fragen zur Entscheidungsfindung {#decisioning-faq}

Auf dieser Seite finden Sie Antworten auf häufig gestellte Fragen zu den Entscheidungsfunktionen in Adobe Journey Optimizer.

## Begrenzungsregeln {#capping-rules}

+++**Was passiert, wenn mehrere Begrenzungsregeln auf ein einzelnes Angebot angewendet werden?**

Ein Angebot wird begrenzt, sobald **eine einzelne Bedingung erfüllt ist**. Wenn mehrere Begrenzungsregeln vorhanden sind, wird das Angebot nicht mehr angezeigt, sobald eine Regel ihren Schwellenwert erreicht.

**Beispiel:**
Wenn Sie zwei Begrenzungsregeln für ein Angebot definieren:
* 5-mal pro Profil pro Woche
* 100-mal über alle Benutzenden hinweg

Das Angebot wird einer Person nicht mehr angezeigt, sobald sie es fünfmal in einer Woche gesehen hat, selbst wenn die Gesamtobergrenze von 100 noch nicht erreicht wurde. Sobald 100 Impressions insgesamt erreicht sind, wird das Angebot für alle Benutzenden nicht mehr angezeigt.

Weitere Informationen zu [Begrenzungsregeln](items.md#capping).

+++

## Rangfolgenformeln {#ranking-formulas}

+++**Welche Rolle spielen Zielgruppen im Vergleich zu einem vollständigen Datensatz in KI-Modellen?**

Beim Konfigurieren von [KI-Modellen](ranking/ai-models.md) dienen Datensätze und Zielgruppen unterschiedlichen Zwecken.

* **Datensätze:** Erfassen Konversionsereignisse (Klicks, Bestellungen, Umsatz), die als Optimierungsziele für das Modell dienen.
* **Zielgruppen:** Dienen als Prädiktorvariablen, mit denen das Modell Empfehlungen basierend auf der Zugehörigkeit zu einem Kundensegment personalisieren kann.

Zielgruppen schränken den Umfang des Modells nicht ein und erweitern ihn nicht. Stattdessen bieten sie kontextuelle Attribute, die die Fähigkeit des Modells verbessern, personalisierte Prognosen über verschiedene Kundensegmente hinweg zu erstellen.

Beide Komponenten sind für eine effektive Modellleistung bei [personalisierten Optimierungsmodellen](ranking/personalized-optimization-model.md) erforderlich.

+++

+++**Wie wirken sich Änderungen an Angebotssammlungen auf die automatische Optimierung oder personalisierte Optimierungsmodelle aus?**

Das Modell mit automatischer Optimierung stellt Traffic zum nächstbesten verfügbaren Angebot bereit, basierend auf Traffic-Daten der letzten 14 Tage, unabhängig davon, ob das personalisierte Optimierungsmodell Traffic-Daten der letzten 30 Tage verwendet.

Wenn mehrere Angebote gleichzeitig entfernt werden und die verbleibenden Angebote innerhalb des 14- oder 30-tägigen Fensters minimale Traffic-Daten haben, kann das Modell ein suboptimales Verhalten aufweisen, einschließlich zufälliger Verteilungsmuster oder Tendenzen zu Angeboten mit höheren Konversionsraten auf der Grundlage begrenzter Impression-Daten.

**Best Practice:** Wenn Sie Angebotssammlungen erheblich ändern, überprüfen Sie, ob die verbleibenden Angebote über ausreichende historische Leistungsdaten verfügen, um die Modelleffektivität aufrechtzuerhalten.

+++

+++**Wie schnell binden KI-Modelle neue Angebote ein?**

KI-Modelle identifizieren und testen neu verfügbarer Angebote im nächsten Trainings-Zyklus:

* **Automatische Optimierung** identifiziert und testet neue Angebote im nächsten Trainings-Zyklus. Das Training zur automatischen Optimierung findet 3- bis 4-mal täglich etwa alle 6 Stunden statt.
* **Personalisierte Optimierung** identifiziert und testet neue Angebote, sobald sie zur Angebotsstrategie hinzugefügt werden. Sie werden in den zufälligen Explorations-Traffic einbezogen. Anschließend werden diese Angebote im nächsten Trainings-Zyklus des Modells personalisiert, der wöchentlich stattfindet.

Nach der Identifizierung beginnen beide Modelle sofort damit, einigen Besuchenden die neuen Angebote zu unterbreiten, um ihre Leistung zu testen und Daten über ihre Effektivität zu sammeln.

Erfahren Sie mehr zu Modellen für die [automatische Optimierung](ranking/auto-optimization-model.md) und [personalisierte Optimierung](ranking/personalized-optimization-model.md).

+++

+++**Wie optimieren KI-Modelle ohne Kontrollgruppen?**

Sowohl Modelle für die automatische Optimierung als auch für die personalisierte Optimierung verwenden eine „Explore-Exploit“-Strategie, bei der keine dedizierten Kontrollgruppen mehr erforderlich sind.

* **Erste Phase:** Die Modelle beginnen mit einer 100%igen Exploration und testen verschiedene Angebote, um grundlegende Leistungsdaten zu ermitteln.
* **Adaptive Optimierung:** Wenn sich Verhaltensereignisse akkumulieren und die Prognosegenauigkeit steigt, gleichen Modelle automatisch Exploration und Exploitation aus.
* **Kontinuierliches Lernen:** Das System ordnet nach und nach leistungsstarken Angeboten mehr Traffic zu und testet gleichzeitig weiterhin Alternativen.

Dadurch wird kontinuierliches Lernen und eine Optimierung über den gesamten Traffic hinweg sichergestellt, ohne dass separate Kontrollgruppen erforderlich sind.

+++

+++**Was sind die minimalen Traffic-Anforderungen für eine optimale KI-Modellleistung?**

Adobe empfiehlt die folgenden Mindestschwellenwerte, um eine effektive Modellleistung sicherzustellen:
* 1.000 Impressions pro Angebot/Element pro Woche
* 100 Konversionsereignisse pro Angebot/Element pro Woche

<!--
**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item
-->

Standardmäßig versucht das System nicht, personalisierte Modelle für Angebote/Elemente mit weniger als 1.000 Impressions oder 50 Konversionsereignissen zu erstellen.

>[!NOTE]
>
>In Produktionsumgebungen mit großen Angebotskatalogen (~300 Angebote) und restriktiven Geschäftsregeln können einige Angebote niedrigere absolute Schwellenwerte erreichen (250 Impressions und 25 Konversionen pro 30 Tage). Diese stellen die Mindestanforderungen an die Daten für das Modell-Training dar, garantieren jedoch möglicherweise keine optimale Leistung.

Erfahren Sie mehr über [Anforderungen bei der Datenerfassung](data-collection/data-collection.md).

+++

+++**Wie wirken sich ähnliche Angebote auf die KI-Modellleistung aus?**

KI-Modelle bieten größere Personalisierungsvorteile, wenn sie für bestimmte Kundensegmente interessant sind. Wenn Angebote sich stark ähneln, sind zwei Ergebnisse typisch:

* **Vergleichbare Leistung:** Angebote funktionieren gleich und erhalten annähernd die gleiche Traffic-Verteilung.
* **Dominantes Angebot**: Geringfügige Unterschiede führen dazu, dass ein Angebot in allen Segmenten die anderen übertrifft und den Großteil des Traffics erfasst.

>[!NOTE]
>
>Eine ausgewogene Traffic-Verteilung ist durch die Differenzierung des Angebots nicht gewährleistet. Angebote mit objektiv höherwertigen Wertversprechen (z. B. 100 € Rabatt gegenüber 50 € Rabatt) dominieren in der Regel über alle Kundensegmente hinweg, unabhängig vom Personalisierungsaufwand.

**Best Practice:** Entwerfen Sie Angebote mit aussagekräftiger Differenzierung, die auf die Präferenzen bestimmter Kundensegmente abgestimmt sind, um die Effektivität des KI-Modells zu maximieren.

+++

+++**Wie wirken sich Traffic-Anomalien auf die KI-Modellleistung aus?**

Traffic-Anomalien werden proportional innerhalb des 30-tägigen rollierenden Fensters in das Modell integriert, was für Modellstabilität bei temporären Traffic-Schwankungen sorgt. Kurzfristige Spitzen oder Rückgänge stören die Modellvorhersagen oder die Leistung nicht wesentlich.

Eine temporäre Traffic-Spitze (z. B. doppelter täglicher Traffic) hat minimale Auswirkungen auf die Gesamtmodellleistung, da der anomale Traffic einen kleinen Bruchteil des 30-Tage-Datensatzes ausmacht.

+++
