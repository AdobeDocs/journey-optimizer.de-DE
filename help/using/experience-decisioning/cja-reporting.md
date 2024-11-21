---
title: Bericht zu Entscheidungen
description: Erfahren Sie, wie Sie Berichte zu Decisioning erstellen.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 616e1dd9fbfd029f7209356d5c19cfff9d4b4f06
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 55%

---


# Bericht zu Entscheidungen {#decisioning-report}

## Codebasierte Kampagnenberichte {#campaigns}

Sobald das code-basierte Erlebnis live ist, können Sie auf dedizierte Berichte zugreifen, um Key Performance Indicators (KPIs) als allumfassendes Dashboard zu überwachen und so eine Analyse der wesentlichen Metriken zu Ihrer Kampagne bereitzustellen.

Dies umfasst Details zu den Leistungselementen und zur Interaktion der Benutzer mit ihnen. [Erfahren Sie, wie Sie mit Code-basierten Erlebnisberichten arbeiten](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Reporting in Customer Journey Analytics {#cja}

Wenn Sie mit Customer Journey Analytics arbeiten, können Sie benutzerdefinierte Berichterstellungs-Dashboards für Ihre code-basierten Kampagnen erstellen, indem Sie Decisioning nutzen.

Die wichtigsten Schritte sind unten aufgeführt. Ausführliche Informationen über die Arbeit mit Customer Journey Analytics finden Sie in der [Customer Journey Analytics-Dokumentation](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Erstellen und konfigurieren Sie eine **Verbindung** in Customer Journey Analytics. So können Sie eine Verbindung zu dem Datensatz herstellen, für den Sie Berichte erstellen möchten. [Erfahren Sie, wie Sie eine Verbindung herstellen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Erstellen Sie eine **Datenansicht** und verknüpfen Sie sie mit der zuvor erstellten Verbindung. Wählen Sie auf der Registerkarte **[!UICONTROL Komponenten]** die entsprechenden Schemafelder aus, die im Reporting angezeigt werden sollen. Stellen Sie bei der Entscheidungsfindung sicher, dass Sie die Felder **propositioninteract** und **propositiondisplay** einschließen. [Erfahren Sie, wie Sie Datenansichten erstellen und konfigurieren können](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Kombinieren Sie Datenkomponenten, Tabellen und Visualisierungen in **Workspace-Projekten**, um Berichte für Ihre Code-basierte Kampagne zu erstellen und gemeinsam zu nutzen.[Erfahren Sie, wie Sie Workspace-Projekte erstellen können](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
