---
title: Berichten über Entscheidungsfindung
description: Erfahren Sie, wie Sie über Entscheidungsfindung berichten.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 4c0605d6ccff5cd62ef7aeb04e0610342d7cc3d5
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 68%

---


# Berichten über Entscheidungsfindung {#decisioning-report}

## Reporting über codebasierte Kampagnen {#campaigns}

Sobald Code-basierte Erlebnisse verfügbar sind, können Sie auf dedizierte Berichte zugreifen, um Key Performance Indicators (KPIs) als umfassendes Dashboard zu überwachen und eine Analyse der mit Ihrer Kampagne verbundenen wesentlichen Metriken bereitzustellen.

Diese umfasst Details zu den Leistungen der Entscheidungselemente und zur Interaktion der Benutzenden mit diesen. [Erfahren Sie, wie Sie mit Code-basierten Erlebnisberichten arbeiten](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Reporting in Customer Journey Analytics {#cja}

Wenn Sie mit Customer Journey Analytics arbeiten, können Sie benutzerdefinierte Reporting-Dashboards für Ihre Code-basierten Kampagnen erstellen, die die Entscheidungsfindung nutzen.

Die wichtigsten Schritte sind unten aufgeführt. Detaillierte Informationen zur Verwendung von Customer Journey Analytics finden Sie in der Dokumentation zu [Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Erstellen und konfigurieren Sie eine **Verbindung** in Customer Journey Analytics. So können Sie eine Verbindung zu dem Datensatz herstellen, für den Sie Berichte erstellen möchten. [Erfahren Sie, wie Sie eine Verbindung erstellen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Erstellen Sie eine **Datenansicht** und verknüpfen Sie sie mit der zuvor erstellten Verbindung. Wählen Sie auf der Registerkarte **[!UICONTROL Komponenten]** die entsprechenden Schemafelder aus, die im Reporting angezeigt werden sollen. Stellen Sie sicher, dass Sie für die Entscheidungsfindung die Felder **propositioninteract** und **propositiondisplay** einschließen. [Erfahren Sie, wie Sie Datenansichten erstellen und konfigurieren](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Kombinieren Sie Datenkomponenten, Tabellen und Visualisierungen in **Workspace-Projekten**, um Berichte für Ihre Code-basierte Kampagne zu erstellen und freizugeben. [Erfahren Sie, wie Sie Workspace-Projekte erstellen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
