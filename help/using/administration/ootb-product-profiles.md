---
title: Integrierte Produktprofile
description: Informationen zu integrierten Produktprofilen
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 5087c5a13eda0b9b5894197b393788f82413690b
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 96%

---

# Integrierte Produktprofile {#ootb-product-profiles}

Adobe Journey Optimizer bietet die neue Funktion „Inline-Authoring“, mit der Sie Ihre Nachrichten direkt in einer Journey erstellen und verfassen können. Weiterführende Informationen zu dieser neuen Funktion finden Sie auf dieser Seite.

>[!WARNING]
>
>Wenn Sie Benutzende haben, die nur dem Produktprofil **[!DNL Message Manager]**, nicht aber dem Produktprofil **[!DNL Journey manager]** zugeordnet sind, müssen Sie ihnen ein neues Produktprofil zuweisen, damit sie weiterhin Inhalte bearbeiten können.

Diese Funktion wirkt sich wie folgt auf die Berechtigungen aus:

| Name der Berechtigung | Wird enthalten sein in |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Nach dem 25. Juli** werden Berechtigungen in Bezug auf Nachrichten weiterhin verfügbar sein, da auf Nachrichten weiterhin zugegriffen werden kann, um den Übergang zu ermöglichen, und Sie können sie weiterhin als Vorlage speichern.

**Ab dem 6. September** werden die Berechtigungen im Zusammenhang mit Nachrichten entfernt und die Nachrichten werden nicht mehr zugänglich sein.

## [!DNL Journey Administrator] {#journey-administrator}

Das Produktprofil **[!DNL Journey Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Journeys zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li> **[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journeys]**: Veröffentlichen von Journeys.</li><li>**[!DNL Manage journeys events, data sources and actions]**: Lesen, Erstellen, Bearbeiten und Löschen von Ereignissen, Quellen oder Aktionen.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Berichten zu Journeys.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Zuweisungen.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li><li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li><li>**[!DNL Manage channel surfaces]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage Landing page settings]**: Erstellen, bearbeiten und löschen Sie Landingpage-Subdomains und Landingpage-Vorgaben.</li><li> **[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li><li>**[!DNL Manage SMS settings]**: Erstellen, bearbeiten und löschen Sie API-Anmeldeinformationen und SMS-Kanal-Oberflächen, die für die Aktivierung des SMS-Kanals erforderlich sind.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li><li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li><li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Journeys und Berechtigungen.</li></ul>|
|Entscheidungs-Management|<ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>|
|Journey Optimizer-Bibliothek|<ul><li>**[!DNL Manage Library Items]**: Hinzufügen und Löschen gespeicherter Ausdrücke in der [!DNL Journey Optimizer] Bibliothek.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Das Produktprofil **[!DNL Journey Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der Berichte **[!DNL Journey]** überprüfen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journey]**: Veröffentlichen von Journeys.</li><li>**[!DNL View journeys events, data sources and actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Das Produktprofil **[!DNL Journey Manager]** ermöglicht Benutzern das Erstellen und Bearbeiten von **[!UICONTROL Journeys]** und Zugriff auf alle Funktionen, die mit **[!UICONTROL Journeys]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL View journeys events]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

Das Produktprofil **[!DNL Journey viewer]** ermöglicht schreibgeschützten Zugriff auf die Funktionen **[!UICONTROL Journeys]** und **[!UICONTROL Entscheidungs-Management]**.

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
|Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li><li>**[!DNL Publish decisions]**: Aktivieren oder Deaktivieren von Entscheidungsaktivitäten.</li></ul>|
