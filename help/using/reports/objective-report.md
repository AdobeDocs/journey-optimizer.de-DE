---
solution: Journey Optimizer
product: journey optimizer
title: Globaler Bericht zu Kampagnen
description: Erfahren Sie, wie Sie Daten im globalen Bericht in Campaign verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6b8983d3f3fa989bd7190fc6a8b51fa8989b2293
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 71%

---

# Globaler Bericht zu Kampagnen {#objective-report}

Globaler Bericht zu Kampagnen können direkt über Ihre Kampagne mit der **[!UICONTROL Bericht anzeigen]** Schaltfläche.

Der **[!UICONTROL Globale Bericht]** in Campaign ist in verschiedene Widgets unterteilt, die Erfolge und Fehler bei Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/global-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](global-report.md#list-of-components-global.md)

## Registerkarte „Kampagne“ {#campaign-global-objectives}

### Versand {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

Das Widget **[!UICONTROL Kampagnenstatistiken]** enthält die wichtigsten Informationen zu Ihrer Kampagne:

* **[!UICONTROL Eingetretene Profile]**: Anzahl der Profile, die mit der Journey begonnen haben.

* **[!UICONTROL Bereitgestellte Aktionen]**: Gesamtzahl der eindeutigen Fälle, in denen eine Aktion in der Journey ausgeführt wurde.

* **[!UICONTROL Fehlgeschlagene Aktionen in %]**: Gesamtzahl der eindeutigen Fälle, in denen eine Aktion in der Journey fehlgeschlagen ist, verglichen mit der Gesamtzahl der eindeutigen Fälle, in denen eine Aktion erfolgreich ausgeführt wurde.

### Zielsetzungsbericht {#objective-global}

>[!AVAILABILITY]
>
>Die **Zielgruppenbericht** ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie beim Adobe-Support.

![](assets/performance_report.gif)

Die **[!UICONTROL Ziele]** können Sie die Berichte Ihrer Sendungen durch Targeting einer bestimmten Metrik besser anpassen.

Die aufgeführten **[!UICONTROL Ziele]** sind mit **[!UICONTROL Datensätzen]** verbunden, die eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen. Eine Liste mit integrierten **[!UICONTROL Zielen]** ist verfügbar, Sie können jedoch Ihre eigenen hinzufügen, indem Sie einen neuen **[!UICONTROL Datensatz]** hinzufügen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../campaigns/reporting-configuration.md).

Nach Auswahl der Ziele, die Sie in Angriff nehmen möchten, bieten die beiden Widgets für **[!UICONTROL Leistungsübersicht]** und **[!UICONTROL Kampagnenziel]** eine detaillierte Zusammenfassung Ihrer Versandleistung.

Mit dem Widget **[!UICONTROL Kampagnenziel]** können Sie auch Ihr Hauptziel mit einer anderen Metrik vergleichen.

### Experimentationsbericht {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

Die **[!UICONTROL Experimentieren]** -Tab bietet wichtige Einblicke in die Leistung der einzelnen Varianten und ermittelt die erfolgreichste Variante.

Beachten Sie, dass es ein wenig dauern kann, um die beste Leistung zu ermitteln. Sie wird durch das Symbol ![](assets/experimentation_report_1.png) gekennzeichnet.

+++ Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den Experimentationsbericht verfügbar sind.

Die Widget **[!UICONTROL Experimentergebnis]** liefert Details zur Leistung der einzelnen Varianten. Sie können Ihre Grundlinie ändern, indem Sie eine der Behandlungen aus der Dropdown-Liste **[!UICONTROL Grundlinie]** auswählen. Die beste Behandlung wird mit einem Sternsymbol gekennzeichnet.

Die Tabelle enthält die folgenden Metriken:

* **[!UICONTROL Steigerung gegenüber dem Ausgangswert]**: Messung der prozentualen Verbesserung der Konversionsrate einer bestimmten Behandlung im Vergleich zum Ausgangswert.

* **[!UICONTROL Konfidenz]**: Belege dafür, dass eine bestimmte Behandlung mit der Grundlinienbehandlung identisch ist. [Weitere Informationen](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Ausgehende Einzelklicks]**: Gesamtanzahl der Klicks in allen ausgehenden Kanälen.

* **[!UICONTROL Profile]**: Anzahl der für diese Behandlung ausgewählten Profile.

* **[!UICONTROL Eindeutige ausgehende Klicks/Profile]**: Gesamtwert der Erfolgsmetrik, die zuvor beim Erstellen Ihrer Experimente ausgewählt wurde, dividiert durch die Anzahl der Profile.

Die **[!UICONTROL Konfidenzintervall]** -Diagramm misst Unsicherheit um Verbesserung. Sie zeigt den prozentualen Leistungsunterschied zwischen der Basislinie und der Behandlung mit der besten Performance. [Weitere Informationen](../campaigns/experiment-calculations.md#confidence-intervals).
+++

Einen tiefen Einblick in diese Ergebnisse und ihre Interpretation finden Sie auf [dieser Seite](../campaigns/get-started-experiment.md#interpret-results).

