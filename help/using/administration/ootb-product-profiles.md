---
solution: Journey Optimizer
product: journey optimizer
title: Integrierte Produktprofile
description: Erfahren Sie mehr über die integrierten Produktprofile
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# Integrierte Produktprofile {#ootb-product-profiles}


## Über Berechtigungen für Nachrichten{#message-permissions}

Adobe Journey Optimizer hat neue Inline-Authoring-Funktionen veröffentlicht, mit denen Sie Ihre Nachrichten direkt aus einer Journey oder einer Kampagne erstellen und erstellen können.

Diese Funktion wirkt sich wie folgt auf die Berechtigungen aus:

| Name der Berechtigung | Wird in |
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

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li> **[!DNL Manage campaigns]**: Kampagnen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichungskampagnen.</li><li>**[!DNL View campaigns report]**: Kampagnenbericht lesen und bearbeiten.</li></ul>| |Administration|<ul><li>**[!DNL Manage subdomains delegation]**: Subdomain-Zuweisung lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage IP pools]**: IP-Pool lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage PTR records]**: PTR-Datensätze lesen und bearbeiten.</li><li>**[!DNL View PTR records]**: schreibgeschützter Zugriff auf PTR-Datensätze.</li><li> **[!DNL Manage messages general settings]**: Allgemeine Einstellungen für Nachrichten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage messages presets]**: Inhaltsbranding lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf Lese-, Erstellungs-, Bearbeitungs- und Löschunterdrückungsregeln.</li><li>**[!DNL Export suppression list]**: Zugriff auf die Exportunterdrückungsliste als CSV-Datei.</li><li>**[!DNL View suppression list]**: lokale Unterdrückungsliste lesen und exportieren.</li><li>**[!DNL Manage alerts]**: Warnhinweise für Kampagnen, Nachrichten und Berechtigungen aktivieren/deaktivieren.</li><li>**[!DNL Manage landing page settings]**: Landingpage-Einstellungen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage SMS settings]**: SMS-Einstellungen lesen, erstellen, bearbeiten und löschen.</li></ul>| |Entscheidungsverwaltung |<ul><li>**[!DNL Manage decisions]**: Entscheidungen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage ranking strategies]**: Rangstrategien lesen, erstellen, bearbeiten und löschen.</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Zugriff auf Sandboxes gewähren.</li><li>**[!DNL Manage segments]**: Segmente lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Profile lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Read datasets]**: schreibgeschützter Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: schreibgeschützter Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: schreibgeschützter Zugriff auf Identitäts-Namespace.</li><li>**[!DNL Manage merge policies]**: Zusammenführungsrichtlinien lesen, erstellen, bearbeiten und löschen.</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

Die **[!DNL Campaign Approver]** Produktprofil ermöglicht Benutzern, Sendungen zu validieren und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen mit der **[!DNL Campaigns]** Berichte.

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li>**[!DNL Manage campaigns]**: Kampagnen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichungskampagnen.</li><li>**[!DNL View Campaigns report]**: Journey-Berichte lesen und bearbeiten.</li></ul>| |Entscheidungsverwaltung | <ul><li>**[!DNL Manage decisions]**: Entscheidungsentitäten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Nachrichtenberichte und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: Segmente lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Profile lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Read datasets]**: schreibgeschützter Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: schreibgeschützter Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Zusammenführungsrichtlinien lesen, erstellen, bearbeiten und löschen.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: Schreibgeschützter Zugriff auf Nachrichtenvorgaben.</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

Die **[!DNL Campaign Manager]** Produktprofil ermöglicht Benutzern das Erstellen und Bearbeiten von **[!UICONTROL Campaigns]** und alle damit verbundenen Funktionen **[!UICONTROL Campaigns]** aber nicht in der Lage sein, sie zu veröffentlichen.

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li>**[!DNL Manage campaigns]**: Kampagnen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL View campaigns report]**: den Journey-Bericht lesen und bearbeiten.</li></ul>| |Entscheidungsverwaltung | <ul><li>**[!DNL Manage decisions]**: Entscheidungsentitäten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Nachrichtenberichte und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: Segmente lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Profile lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Read datasets]**: schreibgeschützter Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: schreibgeschützter Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Zusammenführungsrichtlinien lesen, erstellen, bearbeiten und löschen.</li></ul>| |Administration| <ul><li>**[!DNL View messages presets]**: Schreibgeschützter Zugriff auf Nachrichtenvorgaben.</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

Die **[!DNL Campaign Viewer]** Produktprofil ermöglicht schreibgeschützten Zugriff auf die **[!UICONTROL Campaigns]** und **[!UICONTROL Decision management]** Funktionen.

Benutzer, die diesem Produktprofil zugewiesen sind, können weder bearbeiten noch veröffentlichen.

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Kampagnen| <ul><li>**[!DNL View campaigns]**: schreibgeschützter Zugriff auf Kampagnen.</li><li>**[!DNL View campaigns report]**: schreibgeschützter Zugriff auf Kampagnenberichte.</li></ul>| |Entscheidungsverwaltung | <ul><li>**[!DNL View decisions]**: schreibgeschützter Zugriff auf Entscheidungsentitäten.</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

Die **[!DNL Journey Administrator]** Produktprofil ermöglicht die Verwaltung von Menüs mit der Möglichkeit, Journeys und Entscheidungsmanagement zu verwalten und zu veröffentlichen.

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Journeys| <ul><li> **[!DNL Manage journeys]**: Journeys lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Publish journeys]**: Journeys veröffentlichen.</li><li>**[!DNL Manage journeys events, data sources and actions]**: Ereignisse, Quellen oder Aktionen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL View journeys report]**: den Bericht Journeys lesen und bearbeiten.</li></ul>| |Administration|<ul><li>**[!DNL Manage subdomains delegation]**: Subdomain-Zuweisung lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage IP pools]**: IP-Pool lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage PTR records]**: PTR-Datensätze lesen und bearbeiten.</li><li>**[!DNL View PTR records]**: schreibgeschützter Zugriff auf PTR-Datensätze.</li><li>**[!DNL Manage channel surfaces]**: Inhaltsbranding lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage Landing page settings]**: Erstellen, bearbeiten und löschen Sie Landingpage-Subdomains und Landingpage-Vorgaben.</li><li> **[!DNL Manage messages general settings]**: Allgemeine Einstellungen für Nachrichten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage SMS settings]**: Erstellen, bearbeiten und löschen Sie API-Anmeldeinformationen und SMS-Kanal-Oberflächen, die für die Aktivierung des SMS-Kanals erforderlich sind.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf Lese-, Erstellungs-, Bearbeitungs- und Löschunterdrückungsregeln.</li><li>**[!DNL View suppression list]**: lokale Unterdrückungsliste lesen und exportieren.</li><li>**[!DNL Manage alerts]**: Warnhinweise für Journeys und Berechtigungen aktivieren/deaktivieren.</li></ul>| |Entscheidungsverwaltung |<ul><li>**[!DNL Manage decisions]**: Entscheidungen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage ranking strategies]**: Rangstrategien lesen, erstellen, bearbeiten und löschen.</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**: Zugriff auf Sandboxes gewähren.</li><li>**[!DNL Manage segments]**: Segmente lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Profile lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Read datasets]**: schreibgeschützter Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: schreibgeschützter Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: schreibgeschützter Zugriff auf Identitäts-Namespace.</li><li>**[!DNL Manage merge policies]**: Zusammenführungsrichtlinien lesen, erstellen, bearbeiten und löschen.</li></ul>| |Journey Optimizer-Bibliothek|<ul><li>**[!DNL Manage Library Items]**: Hinzufügen und Löschen gespeicherter Ausdrücke im [!DNL Journey Optimizer] Bibliothek.</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

Die **[!DNL Journey Approver]** Produktprofil ermöglicht Benutzern, Sendungen zu validieren und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen mit der **[!DNL Journey]** Berichte.

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Journeys| <ul><li>**[!DNL Manage journeys]**: Journeys lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Publish journey]**: Journeys veröffentlichen.</li><li>**[!DNL View journeys events, data sources and actions]**: schreibgeschützter Zugriff auf Journey-Ereignisse, benutzerdefinierte Aktionen für Journeys und Datenquellen für Journeys.</li><li>**[!DNL View journeys report]**: Journey-Berichte lesen und bearbeiten.</li></ul>| |Entscheidungsverwaltung | <ul><li>**[!DNL Manage decisions]**: Entscheidungsentitäten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Berichte und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**: Segmente lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Profile lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Read datasets]**: schreibgeschützter Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: schreibgeschützter Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Zusammenführungsrichtlinien lesen, erstellen, bearbeiten und löschen.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

Die **[!DNL Journey Manager]** Produktprofil ermöglicht Benutzern das Erstellen und Bearbeiten von **[!UICONTROL Journeys]** und alle damit verbundenen Funktionen **[!UICONTROL Journeys]** aber nicht in der Lage sein, sie zu veröffentlichen.

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Journeys| <ul><li>**[!DNL Manage journeys]**: Journeys lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL View journeys events]**: schreibgeschützter Zugriff auf Journey-Ereignisse, benutzerdefinierte Aktionen für Journeys und Datenquellen für Journeys.</li><li>**[!DNL View journeys report]**: den Journey-Bericht lesen und bearbeiten.</li></ul>| |Entscheidungsverwaltung | <ul><li>**[!DNL Manage decisions]**: Entscheidungsentitäten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Berichte und Verwenden von Aktionsfunktionen.</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**: Segmente lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Profile lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Read datasets]**: schreibgeschützter Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: schreibgeschützter Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Zusammenführungsrichtlinien lesen, erstellen, bearbeiten und löschen.</li></ul>| |Administration| <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

Die **[!DNL Journey viewer]** Produktprofil ermöglicht schreibgeschützten Zugriff auf die **[!UICONTROL Journeys]** und **[!UICONTROL Decision management]** Funktionen.

Benutzer, die diesem Produktprofil zugewiesen sind, können weder bearbeiten noch veröffentlichen.

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Journeys| <ul><li>**[!DNL View journeys]**: schreibgeschützter Zugriff auf Journeys.</li><li>**[!DNL View journeys event, data sources, actions]**: schreibgeschützter Zugriff auf Journey-Ereignisse und Datenquellen.</li><li>**[!DNL View journeys report]**: schreibgeschützter Zugriff auf Berichte zu Journeys.</li></ul>| |Entscheidungsverwaltung | <ul><li>**[!DNL View decisions]**: schreibgeschützter Zugriff auf Entscheidungsentitäten.</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

Die **[!DNL Decisioning manager]** Das Produktprofil ermöglicht nur die **[!UICONTROL Decision management]** Menü. Benutzer, die diesem Produktprofil zugewiesen sind, können nur Entscheidungen verwalten, anzeigen und veröffentlichen.

Dieses Produktprofil umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen| |-|-| |Entscheidungsverwaltung | <ul><li>**[!DNL Manage decisions]**: Entscheidungsentitäten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL View decisions]**: schreibgeschützter Zugriff auf Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Berichte und Verwenden von Aktionsfunktionen.</li><li>**[!DNL Publish decisions]**: Aktivierung oder Deaktivierung von Entscheidungsaktivitäten.</li></ul>|
