---
title: Berichten über Entscheidungsfindung
description: Erfahren Sie, wie Sie über Entscheidungsfindung berichten.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jbakmb7S9cFitmpa7ypVe8YrYvbZh0E0VogYi3KpNbo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 83%

---

# Berichten über Entscheidungsfindung {#decisioning-report}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Greifen Sie auf dedizierte Entscheidungsberichte zu und erstellen Sie Customer Journey Analytics-Dashboards, damit Sie wichtige Leistungsindikatoren überwachen und analysieren können, wie Kunden mit Ihren Entscheidungselementen interagieren.

>[!ENDSHADEBOX]

## Reporting zur Entscheidungsfindung {#campaigns}

Sobald Journey oder Kampagnen mit Auswahlstrategien verfügbar sind, können Sie auf dedizierte Berichte zugreifen, um KPIs (Decision Key Performance Indicators) zu überwachen.

<!--
Once code-based experiences are live, you can access dedicated reports to monitor Key Performance Indicators (KPIs) as an all-encompassing dashboard, delivering an analysis of essential metrics associated with your campaign.

This encompasses details related to the decision items performances and how users interacted with them. [Learn how to work with Code-based experience reports](../reports/campaign-global-report-cja-code.md)
-->

![](../reports/assets/cja-decisioning-kpis.png)

Sie können auch auf Details zur Leistung von Entscheidungselementen und zur Art und Weise zugreifen, wie Benutzende mit ihnen interagiert haben, um eine Analyse der wesentlichen Metriken zu erhalten, die mit Ihrer Kampagne verknüpft sind.

![](../reports/assets/cja-decisioning-item-performance.png)

In [diesem Abschnitt](../reports/campaign-global-report-cja-code.md#decisioning-reporting) erfahren Sie, wie Sie mit Code-basierten Erlebnisberichten zur Entscheidungsfindung arbeiten.

## Reporting in Customer Journey Analytics {#cja}

Wenn Sie mit Customer Journey Analytics arbeiten, können Sie benutzerdefinierte Reporting-Dashboards für Ihre Code-basierten Kampagnen erstellen, die die Entscheidungsfindung nutzen.

Die wichtigsten Schritte sind unten aufgeführt. Detaillierte Informationen zum Arbeiten mit Customer Journey Analytics finden Sie in der [Dokumentation zu Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Erstellen und konfigurieren Sie eine **Verbindung** in Customer Journey Analytics. So können Sie eine Verbindung zu dem Datensatz herstellen, für den Sie Berichte erstellen möchten. [Informationen zum Erstellen einer Verbindung](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Erstellen Sie eine **Datenansicht** und verknüpfen Sie sie mit der zuvor erstellten Verbindung. Wählen Sie auf der Registerkarte **[!UICONTROL Komponenten]** die entsprechenden Schemafelder aus, die im Reporting angezeigt werden sollen. Stellen Sie sicher, dass Sie für die Entscheidungsfindung die Felder **propositioninteract** und **propositiondisplay** einschließen. [Informationen zum Erstellen und Konfigurieren von Datenansichten](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Kombinieren Sie Datenkomponenten, Tabellen und Visualisierungen in **Workspace-Projekten**, um Berichte für Ihre Code-basierte Kampagne zu erstellen und freizugeben. [Informationen zum Erstellen von Workspace-Projekten](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
