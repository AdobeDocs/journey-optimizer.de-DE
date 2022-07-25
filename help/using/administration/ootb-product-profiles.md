---
title: Integrierte Produktprofile
description: Informationen zu integrierten Produktprofilen
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 67%

---

# Integrierte Produktprofile {#ootb-product-profiles}

Adobe Journey Optimizer bietet eine neue Funktion, das Inline-Authoring, mit der Sie Ihre Nachrichten direkt über eine Journey erstellen und erstellen können. Weiterführende Informationen zu dieser neuen Funktion finden Sie auf dieser Seite.

>[!WARNING]
>
>Wenn Sie Benutzer zugewiesen haben, die der **[!DNL Message Manager]** nur Produktprofil ohne **[!DNL Journey manager]** Produktprofil erstellen, müssen Sie ein neues Produktprofil zuweisen, damit sie mit der Bearbeitung von Inhalten fortfahren können.

Diese Funktion wirkt sich wie folgt auf die Berechtigungen aus:

| Name der Berechtigung | Wird in |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Nach dem 25. Juli**, sind weiterhin Berechtigungen für Nachrichten verfügbar, da der Zugriff auf Nachrichten nach wie vor möglich ist, um die Transition zu aktivieren, und Sie sie dennoch als Vorlage speichern können.

**Seit dem 6. September**, werden die Berechtigungen für Nachrichten entfernt und Nachrichten können nicht mehr aufgerufen werden.

## [!DNL Journey Administrator] {#journey-administrator}

Die **[!DNL Journey Administrator]** Produktprofil ermöglicht die Verwaltung von Menüs mit der Möglichkeit, Journey und Entscheidungsmanagement zu verwalten und zu veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li> **[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journeys]**: Veröffentlichen von Journeys.</li><li>**[!DNL Manage journeys events, data sources and actions]**: Lesen, Erstellen, Bearbeiten und Löschen von Ereignissen, Quellen oder Aktionen.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Berichten zu Journeys.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Zuweisungen.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li><li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li><li> **[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li><li>**[!DNL Manage channel surfaces]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li><li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li><li>**[!DNL Manage alerts]**: Warnhinweise für Journey und Berechtigungen aktivieren/deaktivieren.</li></ul>|
|Entscheidungs-Management|<ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>|
|Journey Optimizer-Bibliothek|<ul><li>**[!DNL Manage Library Items]**: Hinzufügen und Löschen gespeicherter Ausdrücke in der [!DNL Journey Optimizer] Bibliothek.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Das Produktprofil **[!DNL Journey Approver]** ermöglicht es Benutzern, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen mit der **[!DNL Journey]** Berichte.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journey]**: Veröffentlichen von Journeys.</li><li>**[!DNL View journeys events, data sources and actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Berichte und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Das Produktprofil **[!DNL Journey Manager]** ermöglicht Benutzern das Erstellen und Bearbeiten von **[!UICONTROL Journeys]** und Zugriff auf alle Funktionen, die mit **[!UICONTROL Journeys]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL View journeys events]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Berichte und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

Die **[!DNL Journey viewer]** Produktprofil ermöglicht schreibgeschützten Zugriff auf die **[!UICONTROL Journey]** und **[!UICONTROL Entscheidungsmanagement]** Funktionen.

Benutzer, die diesem Produktprofil zugewiesen sind, können weder bearbeiten noch veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL View journeys]**: Nur-Lese-Zugriff auf Journeys.</li><li>**[!DNL View journeys event, data sources, actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse und Datenquellen.</li><li>**[!DNL View journeys report]**: Nur-Lese-Zugriff auf Berichte von Journeys.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Das Produktprofil **[!DNL Decisioning manager]** erlaubt nur das Menü **[!UICONTROL Entscheidungs-Management]**. Benutzer, die diesem Produktprofil zugewiesen sind, können nur Entscheidungen verwalten, anzeigen und veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Berichte und Verwenden von Aktionsfunktionen.</li><li>**[!DNL Publish decisions]**: Aktivieren oder Deaktivieren von Entscheidungsaktivitäten.</li></ul>|
