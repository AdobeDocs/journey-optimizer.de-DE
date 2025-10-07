---
solution: Journey Optimizer
product: journey optimizer
title: Metriken zu Journey Optimizer Experimentation Accelerator
description: Verbessern Ihrer Fähigkeit, Experimente effektiv durchzuführen und Erkenntnisse zu gewinnen
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: Inhalt, Experiment, mehrere, Zielgruppe, Abwandlung
exl-id: 74868625-f4ea-44f9-ae2a-8e5fdd22a081
source-git-commit: fc741db8db2ca9c05dbb87a41712e90a62a18c13
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 100%

---

# Metriken {#experiment-accelerator-metrics}

Auf der Seite **[!UICONTROL Metriken]** werden Erfolgsmetriken aus Journey Optimizer- und Target-Experimenten an einer Stelle angezeigt, was eine Leistungsüberwachung, Vergleiche und gründlichere Erkenntnisse ermöglicht.

## Dashboard {#dashboard}

Beim Zugriff auf die Registerkarte **[!UICONTROL Metriken]** werden alle verfügbaren Erfolgsmetriken aus Journey Optimizer und Adobe Target in einer konsolidierten Ansicht aufgelistet. So können die Leistung über verschiedene Initiativen hinweg verfolgen, Ergebnisse vergleichen und schnell Bereiche identifizieren, die Aufmerksamkeit erfordern.

Greifen Sie auf Filter zu, indem Sie auf ![](assets/do-not-localize/Smock_Filter_18_N.svg) klicken. Dadurch stehen kontextspezifische Optionen zur Verfügung, z. B. Filterung nach **[!UICONTROL Quelle]** oder **[!UICONTROL In aktiven Experimenten verwendet]**.

Alternativ können Sie schnell nach einer Metrik suchen, indem Sie ihren Namen in die Suchleiste eingeben.

![](assets/experiment-monitor-metrics.png)

## Metrikdetails {#metric-details}

### Inkrementell im Zeitverlauf

![](assets/experiment-monitor-metrics-2.png)

Das Diagramm **[!UICONTROL Inkrementell im Zeitverlauf]** bietet eine visuelle Aufschlüsselung der Entwicklung der ausgewählten Metrik über einen ausgewählten Zeitraum hinweg. Verwenden Sie das Dropdown-Menü, um zwischen der täglichen oder wöchentlichen Ansicht zu wechseln und die Granularität anzupassen.

Folgende Zusammenfassungswerte stehen als Kurzreferenz zur Verfügung:

* **[!UICONTROL Gesamt]**: Der kumulative Wert der ausgewählten Metrik über den Berichtszeitraum hinweg.

* **[!UICONTROL Durchschnitt]**: Der typische Wert der Metrik, berechnet für den ausgewählten Zeitraum. Durch den Ausgleich von täglichen oder wöchentlichen Schwankungen liefert er ein klareres Bild der normalen Leistung und kann als Ausgangsbasis für Vergleiche verwendet werden.

* **[!UICONTROL Konversionsrate]**: Prozentsatz der Profile, die die gewünschte Aktion (z. B. Kauf, Anmeldung) abgeschlossen haben, nachdem sie die Abwandlung gesehen haben.

Jeder Wert enthält eine prozentuale Änderung gegenüber dem vorherigen Zeitraum, sodass leicht erkennbar ist, ob die Leistung zunimmt, abnimmt oder stabil bleibt.

### Experimenteffekt

In diesem Abschnitt werden alle aktiven Experimente innerhalb des ausgewählten Zeitraums (letzte 90 Tage, letzte 30 Tage oder letzte 7 Tage) angezeigt und ihr Beitrag zur Metrik hervorgehoben.

Folgende Metriken sind verfügbar:

* **[!UICONTROL Steigerung]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Abwandlung im Vergleich zur Baseline.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Abwandlung mit der Baseline-Abwandlung identisch ist. [Weitere Informationen](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Beitrag]**: Der Anteil der Gesamtänderung der Metrik, der einem bestimmten Experiment oder einer bestimmten Abwandlung zugeschrieben werden kann, sodass sich die Initiativen mit der größten relativen Wirkung identifizieren lassen.
