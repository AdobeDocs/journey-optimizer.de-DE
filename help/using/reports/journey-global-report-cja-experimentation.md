---
solution: Journey Optimizer
product: journey optimizer
title: Journey Experimentbericht
description: Erfahren Sie, wie Sie Experimentierdaten aus dem Journey-Bericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: b63dea783a2f85d17aacc12c23a9f63d880aeeee
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 36%

---

# Experimentier-Journey-Bericht {#campaign-global-report-cja-experimentation}

Ihr Journey-Bericht bietet Ihnen einen vollständigen Überblick über die Leistung Ihres Experiments sowie die wichtigsten Metriken, die Sie benötigen, um die Auswirkungen zu verstehen.

In Journey Optimizer ist das Journey-Experimentieren in zwei Typen unterteilt:

* [Inhaltsexperimente](../content-management/content-experiment.md)
* [Pfadexperimente](../building-journeys/optimize.md)

## Pfadexperiment {#experimentation}

>[!NOTE]
>
> Die für Ihr Inhaltsexperiment detaillierten Tabellen und KPIs sind mit denen für ein Pfadexperiment identisch. Wenn Sie ein Inhaltsexperiment eingerichtet haben, lesen Sie die folgende Dokumentation.

### Experiment-KPIs {#experimentation-kpis}

![](assets/journey-report-experiment-1.png)

Die **Experimentzusammenfassung** bietet wichtige Einblicke in die Leistung Ihres Experiments und ermittelt die erfolgreichste Variante. Beachten Sie, dass es ein wenig dauern kann, um die beste Leistung zu ermitteln.  Wenn Ihr Experiment nicht erfolgreich ist, wird es auf **Nicht stichhaltig** gesetzt.

Die **Experiment-KPIs** dienen als umfassendes Dashboard und liefern eine Analyse der wichtigsten Metriken, die mit Ihrem Experiment verbunden sind.

+++ Weitere Informationen zu den Metriken für Experiment-KPIs

* **[!UICONTROL Steigerung]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Abwandlung im Vergleich zur Baseline.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Abwandlung mit der Baseline-Abwandlung identisch ist. [Weitere Informationen](../content-management/experiment-calculations.md#understand-confidence)

+++



### Varianten nach Erfolgsmetriken {#variant-inbound}

![](assets/cja-experimentation-variants.png)

Die Tabelle **Variante nach Erfolgsmetriken** zeigt, wie jede Variante basierend auf der Erfolgsmetrik funktioniert, die beim Einrichten des Experiments ausgewählt wurde.
Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie auf [dieser Seite](../content-management/get-started-experiment.md#interpret-results).

+++ Weitere Informationen über Varianten nach Erfolgsmetrik

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Nachrichten eignen.

* **[!UICONTROL Eingehende Klicks]**: Gesamtwert der Erfolgsmetrik, die zuvor beim Erstellen der Experimente ausgewählt wurde.

* **[!UICONTROL Konversionsrate]**: Der Gesamtwert der Erfolgsmetrik, die zuvor beim Erstellen der Experimente ausgewählt wurde, dividiert durch die Anzahl der Profile.

* **[!UICONTROL Steigerung]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Abwandlung im Vergleich zur Baseline.

* **[!UICONTROL Konfidenzuntergrenze]**: Niedrigster geschätzter Wert der Konversionsratendifferenz zwischen der Behandlung und der Grundlinie innerhalb des gewählten Konfidenzintervalls.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Abwandlung mit der Baseline-Abwandlung identisch ist. [Weitere Informationen](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Konfidenzobergrenze]**: Höchster geschätzter Wert der Konversionsratendifferenz zwischen der Behandlung und der Grundlinie innerhalb des gewählten Konfidenzintervalls.

+++

### Konversionsrate für Erfolgsmetriken {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

Das Diagramm **[!UICONTROL Konfidenzintervall]** zeigt den Bereich der möglichen Verbesserung an, indem die Grundlinie mit der Behandlung mit der besten Leistung für die ausgewählte Erfolgsmetrik verglichen wird. [Weitere Informationen](../content-management/experiment-calculations.md#confidence-intervals).
