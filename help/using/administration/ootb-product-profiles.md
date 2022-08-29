---
title: Integrierte Produktprofile
description: Informationen zu integrierten Produktprofilen
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 3afef10461ce29b811cb20a2c8c4e94f452daf1f
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 75%

---

# Integrierte Produktprofile {#ootb-product-profiles}


## Über Berechtigungen für Nachrichten{#message-permissions}

Adobe Journey Optimizer hat neue Inline-Authoring-Funktionen eingeführt, mit denen Sie Ihre Nachrichten direkt über eine Journey oder eine Kampagne erstellen und erstellen können. Weitere Informationen zu dieser neuen Funktion finden Sie unter [auf diese Seite verweisen](../rn/inline-messages.md).

Diese Funktion wirkt sich wie folgt auf die Berechtigungen aus:

| Name der Berechtigung | Wird enthalten sein in |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**Nach dem 25. Juli**, Berechtigungen im Zusammenhang mit **Nachrichten** weiterhin verfügbar sind, da der Zugriff auf Nachrichten nach wie vor erfolgt, um die Transition zu aktivieren, und Sie sie dennoch als Vorlage speichern können.

**Seit dem 6. September**, Berechtigungen im Zusammenhang mit **Nachrichten** entfernt und Nachrichten sind nicht mehr verfügbar.

>[!WARNING]
>
>Wenn Sie Benutzer zugewiesen haben, die der **[!DNL Message Manager]** nur Produktprofil ohne **[!DNL Journey manager]** Produktprofil erstellen, müssen Sie ein neues Produktprofil zuweisen, damit sie mit der Bearbeitung von Inhalten fortfahren können.


## [!DNL Campaign Administrator] {#campaign-administrator}

Die **[!DNL Campaign Administrator]** Produktprofil ermöglicht die Verwaltung von Menüs mit der Möglichkeit, Kampagnen und Entscheidungsverwaltung zu verwalten und zu veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li> **[!DNL Manage campaigns]**: Kampagnen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichungskampagnen.</li><li>**[!DNL View campaigns report]**: Kampagnenbericht lesen und bearbeiten.</li></ul>|
|Administration|<ul><li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Zuweisungen.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li><li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li><li> **[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li><li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li><li>**[!DNL Export suppression list]**: Zugriff auf die Exportunterdrückungsliste als CSV-Datei.</li><li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li><li>**[!DNL Manage alerts]**: Warnhinweise für Kampagnen, Nachrichten und Berechtigungen aktivieren/deaktivieren.</li><li>**[!DNL Manage landing page settings]**: Landingpage-Einstellungen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage SMS settings]**: SMS-Einstellungen lesen, erstellen, bearbeiten und löschen.</li></ul>|
|Entscheidungs-Management|<ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

Das Produktprofil **[!DNL Campaign Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der Berichte **[!DNL Campaigns]** überprüfen.

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li>**[!DNL Manage campaigns]**: Kampagnen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichungskampagnen.</li><li>**[!DNL View Campaigns report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

Die **[!DNL Campaign Manager]** Produktprofil ermöglicht Benutzern das Erstellen und Bearbeiten von **[!UICONTROL Kampagnen]** und alle damit verbundenen Funktionen **[!UICONTROL Kampagnen]** aber nicht in der Lage sein, sie zu veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li>**[!DNL Manage campaigns]**: Kampagnen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

Die **[!DNL Campaign Viewer]** Produktprofil ermöglicht schreibgeschützten Zugriff auf die **[!UICONTROL Kampagnen]** und **[!UICONTROL Entscheidungsmanagement]** Funktionen.

Benutzer, die diesem Produktprofil zugewiesen sind, können weder bearbeiten noch veröffentlichen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li>**[!DNL View campaigns]**: schreibgeschützter Zugriff auf Kampagnen.</li><li>**[!DNL View campaigns report]**: schreibgeschützter Zugriff auf Kampagnenberichte.</li></ul>|
|Entscheidungs-Management| <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

Das Produktprofil **[!DNL Journey Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Journeys zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Dieses Produktprofil umfasst folgende Berechtigungen:

| Funktion | Berechtigungen|
|-|-|
|Journeys | <ul><li> **[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journeys]**: Veröffentlichen von Journeys.</li><li>**[!DNL Manage journeys events, data sources and actions]**: Lesen, Erstellen, Bearbeiten und Löschen von Ereignissen, Quellen oder Aktionen.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Berichten zu Journeys.</li></ul>| |Administration|<ul><li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Zuweisungen.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li><li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li><li>**[!DNL Manage channel surfaces]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage Landing page settings]**: Erstellen, bearbeiten und löschen Sie Landingpage-Subdomains und Landingpage-Vorgaben.</li><li> **[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li><li>**[!DNL Manage SMS settings]**: Erstellen, bearbeiten und löschen Sie API-Anmeldeinformationen und SMS-Kanal-Oberflächen, die für die Aktivierung des SMS-Kanals erforderlich sind.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li><li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li><li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Journeys und Berechtigungen.</li></ul>|
|Entscheidungs-Management|<ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul>|
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
