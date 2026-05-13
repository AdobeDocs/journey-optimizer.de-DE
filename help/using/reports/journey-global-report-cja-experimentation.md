---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Bericht zu Experimenten
description: Informationen zum Verwenden von Experimentdaten aus dem Journey-Bericht
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a2b4ef74-96a9-4907-ba70-7aee69e45f20
TQID: https://experienceleague.adobe.com/oN7VFQvhQlwNa2U5CmcAYkGbKb0Vnxc7yA5rCLDjQw4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 100%

---

# Experimente-Journey-Bericht {#campaign-global-report-cja-experimentation}

Ihr Journey-Bericht bietet Ihnen einen vollständigen Überblick über das Abschneiden Ihres Experiments sowie die wichtigsten Metriken, die Sie benötigen, um die Auswirkungen zu verstehen.

In Journey Optimizer ist das Experimentieren mit Journeys in zwei Typen unterteilt:

* [Experimente mit Inhalten](../content-management/content-experiment.md)

  Beachten Sie, dass die für Ihr Inhaltsexperiment angegebenen Tabellen und KPIs mit denen für ein Pfadexperiment übereinstimmen. Wenn Sie ein Inhaltsexperiment eingerichtet haben, lesen Sie die [folgende Dokumentation](#experimentation).

* [Pfadexperimente](../building-journeys/optimize.md)

## Pfadexperiment {#experimentation}

### Experiment-KPIs {#experimentation-kpis}

![](assets/journey-report-experiment-1.png)

Die **Zusammenfassung der Experimente** bietet wichtige Erkenntnisse zur Performance der einzelnen Varianten und ermittelt die erfolgreichste Variante. Beachten Sie, dass es ein wenig dauern kann, um die beste Leistung zu ermitteln. Wenn Ihr Experiment nicht erfolgreich ist, wird es auf **Nicht stichhaltig** gesetzt.

Die **KPIs zum Experimentieren** dienen als allumfassendes Dashboard und liefern eine Analyse der wesentlichen Metriken, die mit Ihren Experimenten verknüpft sind.

+++ Weitere Informationen zu den Metriken für Experiment-KPIs

* **[!UICONTROL Steigerung]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Abwandlung im Vergleich zur Baseline.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Abwandlung mit der Baseline-Abwandlung identisch ist. [Weitere Informationen](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++



### Variante nach Erfolgsmetriken {#variant-inbound}

![](assets/cja-experimentation-variants.png)

Die Tabelle **Variante nach Erfolgsmetriken** zeigt, wie die einzelnen Varianten bezüglich der Erfolgsmetrik abschneiden, die beim Einrichten des Experiments ausgewählt wurde.
Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie auf [dieser Seite](../content-management/get-started-experiment.md#interpret-results).

+++ Weitere Informationen zu Varianten nach Erfolgsmetrik

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Nachrichten eignen.

* **[!UICONTROL Eingehende Klicks]**: Gesamtwert der Erfolgsmetrik, die zuvor beim Erstellen der Experimente ausgewählt wurde.

* **[!UICONTROL Konversionsrate]**: Der Gesamtwert der Erfolgsmetrik, die zuvor beim Erstellen der Experimente ausgewählt wurde, dividiert durch die Anzahl der Profile.

* **[!UICONTROL Steigerung]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Abwandlung im Vergleich zur Baseline.

* **[!UICONTROL Konfidenzuntergrenze]**: Niedrigster geschätzter Wert der Konversionsratendifferenz zwischen der Abwandlung und der Baseline innerhalb des gewählten Konfidenzintervalls.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Abwandlung mit der Baseline-Abwandlung identisch ist. [Weitere Informationen](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL Konfidenzobergrenze]**: Höchster geschätzter Wert der Konversionsratendifferenz zwischen der Abwandlung und der Baseline innerhalb des gewählten Konfidenzintervalls.

+++

### Konversionsrate für Erfolgsmetrik {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

Das Diagramm **[!UICONTROL Konfidenzintervall]** zeigt den Bereich der möglichen Verbesserung an, indem die Baseline mit der Abwandlung mit der besten Performance bezüglich der ausgewählten Erfolgsmetrik verglichen wird. [Weitere Informationen](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences).
