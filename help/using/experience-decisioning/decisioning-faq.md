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
source-git-commit: 59e85eb7a14f88d95b2ef97e3ace11a65f115b75
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 1%

---

# Häufig gestellte Fragen zu Entscheidungen {#decisioning-faq}

Auf dieser Seite finden Sie Antworten auf häufig gestellte Fragen zu den Entscheidungsfunktionen in Adobe Journey Optimizer.

## Begrenzungsregeln {#capping-rules}

+++**Was passiert, wenn Sie mehr als eine Begrenzungsregel für ein Angebot erstellen? Wird das Angebot nicht mehr angezeigt, wenn eine oder alle Begrenzungsregeln erfüllt sind?**

Das Angebot wird begrenzt, sobald **eine Bedingung erfüllt ist**. Dies bedeutet, dass eine der Begrenzungsregeln die Anzeige des Angebots verhindert, sobald sein Schwellenwert erreicht ist.

Wenn Sie beispielsweise zwei Begrenzungsregeln haben:
* 5-mal pro Profil pro Woche
* 100-mal über alle Benutzer hinweg

Das Angebot wird einem Benutzer nicht mehr angezeigt, sobald er es fünf Mal in einer Woche gesehen hat, selbst wenn die Gesamtobergrenze von 100 noch nicht erreicht wurde. Wenn erst einmal 100 Impressions insgesamt erreicht sind, wird das Angebot nicht mehr für alle Benutzer angezeigt.

Weitere Informationen zu [Begrenzungsregeln](items.md#capping).

+++

## Rangfolgenformeln {#ranking-formulas}

+++**Warum sollte ich eine Zielgruppe zu einem KI-Modell hinzufügen? Was ist der Vorteil des Hinzufügens von Zielgruppen gegenüber einem vollständigen Datensatz? Wird das Modell eingeschränkt oder erweitert?**

Beim Arbeiten mit KI-Modellen (insbesondere [personalisierte Optimierungsmodelle](ranking/personalized-optimization-model.md)):

* **Datensätze** werden hinzugefügt, um Ihre Konversionsereignisse (Klicks, Bestellungen, Umsatz) zu erfassen. Dies sind die Ergebnisse, für die das Modell zu optimieren versucht.
* **Zielgruppen** werden hinzugefügt, um sie als Prädiktorvariablen im Modell zu verwenden. Sie helfen bei der Personalisierung von Prognosen, um Klicks, Bestellungen oder Umsätze für verschiedene Kundensegmente vorherzusagen.

Datensätze und Audiences sind erforderlich, damit das Modell der personalisierten Optimierung effektiv funktioniert. Zielgruppen **das Modell weder** noch erweitern, sondern bieten stattdessen zusätzlichen Kontext, der dem Modell hilft, bessere personalisierte Entscheidungen zu treffen.

Weitere Informationen zu [KI-Modellen](ranking/ai-models.md).

+++

+++**Hat das Hinzufügen oder Entfernen von Angeboten zu einer Sammlung Auswirkungen auf das Modell, wenn ich Modelle mit automatischer Optimierung oder personalisierter Optimierung verwende?**

Beide Modelle liefern Traffic zum nächstbesten verfügbaren Angebot, das auf Traffic-Daten der letzten 30 Tage basiert.

Wenn mehrere Angebote gleichzeitig entfernt werden und die verbleibenden Angebote in den letzten 30 Tagen nur sehr wenig Traffic erhalten haben, kann sich die Angebotsverteilung unerwartet verhalten. Dies könnte zu einer zufälligen Verteilung oder zu Verzerrungen bei bestimmten Angeboten führen, die eine höhere Konversionsrate basierend auf nur wenigen Impressions aufweisen.

**Best Practice**: Wenn Sie wesentliche Änderungen an Angebotssammlungen vornehmen, stellen Sie sicher, dass die verbleibenden Angebote über ausreichende historische Leistungsdaten verfügen, um eine optimale Modellleistung aufrechtzuerhalten.

+++

+++**Wie lange dauert es, bis die KI-Modelle verstehen, dass neue Inhalte hinzugefügt wurden, und beginnen, sie zum Mix hinzuzufügen?**

Beide KI-Modelle identifizieren beim nächsten Trainings-Lauf neu verfügbare Angebote:

* **Automatische Optimierung**: Tägliche Trainings-Läufe
* **Personalisierte Optimierung**: Wöchentliche Trainings-Läufe

Sobald sie identifiziert sind, beginnen beide Modelle sofort damit, einigen Besuchern die neuen Angebote zu unterbreiten, um ihre Leistung zu testen und Daten über ihre Effektivität zu sammeln.

Erfahren Sie mehr über [automatische Optimierung](ranking/auto-optimization-model.md) und [personalisierte &#x200B;](ranking/personalized-optimization-model.md)).

+++

+++**Wenn wir in den KI-Modellen keine Kontrollgruppen haben, lernen wir dann den gesamten Traffic und optimieren ihn, alles zur gleichen Zeit?**

Ja. Beide KI-Modelle (automatische Optimierung und personalisierte Optimierung) verwenden einen „Explore and Exploit“-Ansatz:

* Zunächst lauten beide Modelle **100 % Exploration**, d. h. sie testen verschiedene Angebote, um Leistungsdaten zu erfassen.
* Im Laufe der Zeit **die Modelle automatisch den Zielkonflikt zwischen Explore/Exploit**, da Verhaltensereignisse erfasst und Prognosen verbessert werden.
* Die Modelle verlagern allmählich mehr Traffic auf leistungsfähigere Angebote und untersuchen und testen gleichzeitig andere Optionen.

Dadurch wird ein kontinuierliches Lernen und eine Optimierung über den gesamten Traffic hinweg sichergestellt, ohne dass separate Kontrollgruppen erforderlich sind.

+++

+++**Wie viele Optimierungsereignisse müssen wir statistisch signifikant sein? Gibt es einen minimalen Traffic-Grenzwert für eine Oberfläche?**

Um eine optimale Modellleistung zu gewährleisten, empfiehlt Adobe die folgenden Mindestwerte:

**Empfohlene Mindestwerte (pro Woche):**
* Mindestens **1.000 Impressionen** pro Angebot/Element
* Mindestens **100 Konversionsereignisse** pro Angebot/Element

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Standardmäßig versucht das System nicht, personalisierte Modelle für Angebote/Elemente mit weniger als 1.000 Impressionen oder 50 Konversionsereignissen zu erstellen.

**Wichtig**: In der Praxis haben einige Kunden viele Angebote (~300) in einem einzigen Modell, und einige Angebote können sehr restriktive Geschäftsregeln haben. Die absoluten Mindestwerte (250 Impressionen / 25 Konversionen pro 30 Tage) stellen den niedrigsten Schwellenwert dar, den das System für die Erstellung von Modellen unterstützen kann.

Weitere Informationen zu [Datenerfassungsanforderungen](data-collection/data-collection.md).

+++

+++**Muss der Inhalt der Angebote klar differenziert werden, damit die KI-Modelle gut funktionieren? Was passiert, wenn ich mehrere Angebote habe, die einander zu ähnlich sind?**

Im Allgemeinen wird das KI-Modell eher Vorteile aus der Personalisierung ziehen, wenn **Angebote für verschiedene Kundentypen geeignet sind**.

Wenn Angebote sehr ähnlich sind, ist eines von zwei Ergebnissen wahrscheinlich:

* **Ähnliche Leistung**: Die Angebote werden identisch abschneiden und einen relativ gleichmäßigen Traffic erhalten.
* **Dominanz**: Kleine Unterschiede können dazu führen, dass ein Angebot über alle Kundentypen hinweg die anderen dominiert und den Großteil des Traffics erhält.

>[!NOTE]
>
>Unterschiede in den Angeboten sind keine Garantie dafür, dass ein Angebot das andere nicht dominiert. Ein Angebot mit einem Rabatt von 100 € übertrifft fast immer ein Angebot mit einem Rabatt von 50 € für alle Kundentypen, unabhängig von der Personalisierung.

**Best Practice**: Stellen Sie sicher, dass Ihre Angebote eine aussagekräftige Differenzierung bieten, die für eine optimale KI-Modellleistung an verschiedene Kundensegmente appellieren kann.

+++

+++**Was passiert mit dem Modell, wenn es eine Traffic-Anomalie gibt, z. B. eine riesige Traffic-Spitze? Wird es Probleme verursachen oder die Eigenartigkeit steigern?**

Eine Traffic-Spitze würde bei der Modellierung proportional zum anderen Traffic in den letzten 30 Tagen einbezogen.

Beispielsweise hat eine 2x tägliche Traffic-Spitze eine relativ geringe Auswirkung auf das Gesamtmodell, da es 29 Tage normalen Traffics gibt, die deutlich mehr Verhaltensdaten repräsentieren.

**Wichtiger Punkt**: Das rollierende 30-Tage-Fenster hilft dem Modell, die Stabilität bei temporären Traffic-Anomalien aufrechtzuerhalten. Kurzfristige Spitzen oder Tiefpunkte beeinträchtigen die Modellleistung nicht wesentlich.

+++

## Verwandte Themen {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Erstellen von Entscheidungselementen](items.md)
* [KI-Modelle - Übersicht](ranking/ai-models.md)
* [Leitlinien und Einschränkungen für die Entscheidungsfindung](decisioning-guardrails.md)

