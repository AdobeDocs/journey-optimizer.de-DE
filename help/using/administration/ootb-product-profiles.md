---
title: Integrierte Produktprofile
description: Informationen zu integrierten Produktprofilen
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: f5627a23ceb0d00dd01db8766e72fed1b5d652a3
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 99%

---

# Integrierte Produktprofile {#ootb-product-profiles}

## [!DNL Journey Administrator] {#journey-administrator}

Das Produktprofil **[!DNL Journey Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Journeys und Nachrichten zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li> **[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journeys]**: Veröffentlichen von Journeys.</li><li>**[!DNL Manage journeys events, data sources and actions]**: Lesen, Erstellen, Bearbeiten und Löschen von Ereignissen, Quellen oder Aktionen.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Berichten zu Journeys.</li></ul>|
|Nachrichten|<ul><li> **[!DNL Manage messages]**: Lesen, Erstellen und Bearbeiten der Nachrichtenvorschau und Durchführen von Testsendungen.</li><li>**[!DNL Manage messages preview and test]**: Veröffentlichen von Nachrichten.</li><li>**[!DNL Publish messages]**: Lesen, Erstellen und Bearbeiten der Nachrichtenvorschau und Durchführen von Testsendungen.</li><li>**[!DNL View messages report]**: Lesen und Bearbeiten von Nachrichtenberichten.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Zuweisungen.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li><li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li><li> **[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li><li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li><li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li><li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Journeys, Nachrichten und Berechtigungen.</li></ul>|
|Entscheidungs-Management|<ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Rangstrategien lesen, erstellen, bearbeiten und löschen.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>|
|Journey Optimizer-Bibliothek|<ul><li>**[!DNL Manage Library Items]**: Hinzufügen und Löschen gespeicherter Ausdrücke in der [!DNL Journey Optimizer] Bibliothek.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Das Produktprofil **[!DNL Journey Approver]** ermöglicht es Benutzern, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der Berichte **[!DNL Message]** und **[!DNL Journey]** überprüfen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journey]**: Veröffentlichen von Journeys.</li><li>**[!DNL View journeys events, data sources and actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Nachrichten| <ul><li>**[!DNL Manage messages]**: Lesen, Erstellen, Bearbeiten und Löschen von Nachrichten.</li><li>**[!DNL Publish messages]**: Veröffentlichen von Nachrichten.</li><li>**[!DNL Manage messages preview and test]**: Lesen, Erstellen und Bearbeiten der Nachrichtenvorschau und Durchführen von Testsendungen.</li><li>**[!DNL View messages report]**: Lesen, Erstellen und Bearbeiten und Löschen von Nachrichtenberichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Das Produktprofil **[!DNL Journey Manager]** ermöglicht Benutzern das Erstellen und Bearbeiten von **[!UICONTROL Journeys]** und Zugriff auf alle Funktionen, die mit **[!UICONTROL Journeys]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL View journeys events]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Nachrichten| <ul><li>**[!DNL Manage messages]**: Lesen, Erstellen, Bearbeiten und Löschen von Nachrichten.</li><li> **[!DNL Manage messages preview and test]**: Lesen, Erstellen und Bearbeiten der Nachrichtenvorschau und Durchführen von Testsendungen.</li><li>**[!DNL View messages report]**: Lesen, Erstellen und Bearbeiten und Löschen von Nachrichtenberichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul>|

## [!DNL Journey viewer] {#journey-viewer}

Das Produktprofil **[!DNL Journey viewer]** ermöglicht Nur-Lese-Zugriff auf die Funktionen **[!UICONTROL Journeys]**, **[!UICONTROL Ziele]**, **[!UICONTROL Nachrichten]** und **[!UICONTROL Entscheidungs-Management]**.

Benutzer, die diesem Produktprofil zugewiesen sind, können weder bearbeiten noch veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL View journeys]**: Nur-Lese-Zugriff auf Journeys.</li><li>**[!DNL View journeys event, data sources, actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse und Datenquellen.</li><li>**[!DNL View journeys report]**: Nur-Lese-Zugriff auf Berichte von Journeys.</li></ul>|
|Nachrichten| <ul><li>**[!DNL View messages]**: Nur-Lese-Zugriff auf Nachrichten.</li><li>**[!DNL View messages report]**: Nur-Lese-Zugriff auf Nachrichtenberichte.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul>|

## [!DNL Message Manager] {#message-manager}

Das Produktprofil **[!DNL Message Manager]** ermöglicht Benutzern das Erstellen und Bearbeiten von **[!UICONTROL Nachrichten]** und bietet Zugriff auf das **[!UICONTROL Entscheidungs-Management]**. Sie können Nachrichten aber nicht veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL View journeys]**: Nur-Lese-Zugriff auf Journeys.</li><li>**[!DNL View Journeys events, data sources and actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li></ul>|
|Nachrichten| <ul><li>**[!DNL Manage messages]**: Lesen, Erstellen, Bearbeiten und Löschen von Nachrichten.</li><li>**[!DNL Manage messages preview and test]**: Lesen, Erstellen und Bearbeiten der Nachrichtenvorschau und Durchführen von Testsendungen.</li><li> **[!DNL View messages report]**: Lesen, Erstellen und Bearbeiten und Löschen von Nachrichtenberichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Read profiles]**: Nur-Lese-Zugriff auf Profile für Vorschau und Test.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Das Produktprofil **[!DNL Decisioning manager]** erlaubt nur das Menü **[!UICONTROL Entscheidungs-Management]**. Benutzer, die diesem Produktprofil zugewiesen sind, können nur Entscheidungen verwalten, anzeigen und veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li><li>**[!DNL Publish decisions]**: Aktivieren oder Deaktivieren von Entscheidungsaktivitäten.</li></ul>|
