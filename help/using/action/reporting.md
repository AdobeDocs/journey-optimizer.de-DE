---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Bericht
description: Informationen zum Verwenden von Daten aus dem Journey-Bericht
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 3%

---

# Überwachen von benutzerdefinierten Aktionen {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="Überwachen von benutzerdefinierten Aktionen"
>abstract="Auf **[!UICONTROL Berichtseite für benutzerdefinierte]** können Sie die Leistung und Zuverlässigkeit von API-Aufrufen verfolgen, die Ihre Journey an Drittanbietersysteme durchführen."

>[!AVAILABILITY]
>
>Berichte zu benutzerdefinierten Aktionen sind derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit).

Auf **[!UICONTROL Berichtseite]** Benutzerdefinierte Aktion“ können Sie die Zuverlässigkeit und Leistung von API-Aufrufen von Ihren Journey an Drittanbietersysteme überwachen. Diese Berichte helfen Ihnen dabei, Integrationsprobleme, Latenzengpässe oder Einschränkungs-/Begrenzungsbeschränkungen, die sich auf die Bereitstellung auswirken können, schnell zu identifizieren.

Die Berichtseite für benutzerdefinierte Aktionen funktioniert wie andere Echtzeitberichte in Journey Optimizer. Weitere Informationen zu Dashboard-Funktionen finden Sie in [dieser Dokumentation](../reports/report-cja-manage.md).

Um auf die Berichtseite **[!UICONTROL Benutzerdefinierte Aktion]** zuzugreifen, klicken Sie auf der ![](assets/do-not-localize/Smock_Monitoring_18_N.svg)-**[!UICONTROL auf]** .

![](assets/monitor-1.png)

➡️ [Erfahren Sie mehr über die Konfiguration Ihrer benutzerdefinierten Aktionen](../action/about-custom-action-configuration.md)

## KPIs {#kpis}

![](assets/monitor-2.png)

Die **[!UICONTROL Benutzerdefinierte Aktion]** Key Performance Indicators (KPIs) dienen als zentralisiertes Dashboard, das einen konsolidierten Überblick über den Betriebszustand und die Zuverlässigkeit Ihrer benutzerdefinierten Aktionsaufrufe bietet. Mit diesen Metriken können Sie die Leistung bewerten, Engpässe identifizieren und stabile Integrationen mit externen Systemen sicherstellen.

+++ Weitere Informationen zu KPIs für benutzerdefinierte Aktionen

* **[!UICONTROL Erfolgreiche Aufrufe]**: Gesamtzahl der HTTP-Aufrufe, die eine gültige Antwort ohne Fehler zurückgegeben haben.

* **[!UICONTROL 4xx/5xx-Fehler]**: Anzahl fehlgeschlagener Aufrufe aufgrund von Client-seitigen (4xx) oder Server-seitigen (5xx) Fehlern, wobei Konfigurationsprobleme oder Endpunktfehler hervorgehoben werden.

* **[!UICONTROL Zeitüberschreitungen]**: Anzahl der Aufrufe, die fehlgeschlagen sind, weil sie die maximale Antwortzeit überschritten haben. Dies hilft bei der Oberfläche von Latenzzeiten oder Leistungsproblemen mit externen Endpunkten.

* **[!UICONTROL Begrenzte Aufrufe]**: Anzahl der Aufrufe, die aufgrund von Begrenzungen blockiert wurden, um sicherzustellen, dass nachgelagerte Systeme nicht überlastet werden.

* **[!UICONTROL Durchschnittlicher RPS]**: Anzahl der Anfragen pro Sekunde, die von der benutzerdefinierten Aktion über den ausgewählten Zeitraum verarbeitet wurden.

+++

## Anrufe im Zeitverlauf {#calls}

![](assets/monitor-3.png)

Das **[!UICONTROL Aufrufe im Zeitverlauf]** zeigt den KPI-Trend der HTTP-Aufrufe über den für den Bericht ausgewählten Zeitraum an. Die Granularität der Zeitreihe hängt vom ausgewählten Zeitbereich ab. Beispiel:

* Bei einem siebentägigen Bericht zeigt jeder Datenpunkt die KPIs für einen Tag an.
* Wenn Sie einen Zeitraum von 1 Tag auswählen, zeigt das Diagramm die KPIs pro Stunde an.
* Wenn Sie einen Zeitbereich von 1 Stunde auswählen, zeigt das Diagramm die KPIs pro Minute an.

➡️[Im Abschnitt KPIs finden Sie eine Beschreibung der Metriken für HTTP-Aufrufe](#kpis)

## Aufschlüsselung der Anrufe {#breakdown}

![](assets/monitor-4.png)

Die Tabelle **[!UICONTROL Aufschlüsselung]** bietet eine hierarchische Aufschlüsselung der HTTP-Aufrufmetriken, von den Gesamtmetriken pro Endpunkt auf der obersten Ebene über die Metriken pro benutzerdefinierter Aktion bei Verwendung jedes Endpunkts bis hin zu den Journeys, die auf ihnen auf der untersten Ebene basieren.

➡️[Im Abschnitt KPIs finden Sie eine Beschreibung der Metriken für HTTP-Aufrufe](#kpis)


