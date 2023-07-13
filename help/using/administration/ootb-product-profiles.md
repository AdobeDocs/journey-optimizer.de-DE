---
solution: Journey Optimizer
product: journey optimizer
title: In Journey Optimizer integrierte Rollen
description: Erfahren Sie mehr über die integrierten Rollen.
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: Berechtigungen, Authoring, Nachrichten
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 95%

---

# Integrierte Rollen {#ootb-product-profiles}

## [!DNL Campaign Administrator] {#campaign-administrator}

Die Rolle **[!DNL Campaign Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Kampagnen zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li> **[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Kampagnen-Berichten.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Zuweisungen.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li><li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li><li> **[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li><li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li><li>**[!DNL Export suppression list]**: Zugriff, um die Unterdrückungsliste als CSV-Datei zu exportieren.</li><li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li><li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Kampagnen, Nachrichten und Berechtigungen.</li><li>**[!DNL Manage landing page settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für Landingpages.</li><li>**[!DNL Manage SMS settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für SMS-Nachrichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li><li>**[!DNL Manage segments]**: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen. <li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Die Rolle **[!DNL Campaign Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der Berichte **[!DNL Campaigns]** überprüfen.

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li>**[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichen von Kampagnen.</li><li>**[!DNL View Campaigns report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul> |
| Administration | <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Die Rolle **[!DNL Campaign Manager]** ermöglicht Benutzenden das Erstellen und Bearbeiten von **[!UICONTROL Kampagnen]** und gibt ihnen Zugriff auf alle Funktionen, die mit **[!UICONTROL Kampagnen]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li>**[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul> |
| Administration | <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Die Rolle **[!DNL Campaign Viewer]** ermöglicht schreibgeschützten Zugriff auf die Funktionen **[!UICONTROL Kampagnen]** und **[!UICONTROL Entscheidungs-Management]**.

Benutzende, denen diese Rolle zugewiesen wurde, können weder bearbeiten noch veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li>**[!DNL View campaigns]**: Nur-Lese-Zugriff auf Kampagnen.</li><li>**[!DNL View campaigns report]**: Nur-Lese-Zugriff auf Kampagnen-Berichte.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Die Rolle **[!DNL Journey Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Journeys zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Journeys | <ul><li> **[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journeys]**: Veröffentlichen von Journeys.</li><li>**[!DNL Manage journeys events, data sources and actions]**: Lesen, Erstellen, Bearbeiten und Löschen von Ereignissen, Quellen oder Aktionen.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Berichten zu Journeys.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Zuweisungen.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li><li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li><li>**[!DNL Manage channel surfaces]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage Landing page settings]**: Erstellen, Bearbeiten und Löschen von Landingpage-Subdomains und Landingpage-Voreinstellungen.</li><li> **[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li><li>**[!DNL Manage SMS settings]**: Erstellen, Bearbeiten und Löschen von API-Anmeldeinformationen und SMS-Kanaloberflächen, die für die Aktivierung des SMS-Kanals erforderlich sind.</li><li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li><li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li><li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Journeys und Berechtigungen.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li><li>**[!DNL Manage segments]**: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul> |
| Journey Optimizer-Bibliothek | <ul><li>**[!DNL Manage Library Items]**: Hinzufügen und Löschen gespeicherter Ausdrücke in der [!DNL Journey Optimizer] Bibliothek.</li></ul> |
| Data Governance | <ul><li>**[!DNL Manage usage label]**: Nutzungsbezeichnungen lesen, erstellen und löschen.</li><li>**[!DNL Manage data usage policies]**: Datennutzungsrichtlinien lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL View data usage policies]**: schreibgeschützter Zugriff auf Datennutzungsrichtlinien.</li><li>**[!DNL View user activity log]**: Auditprotokolle lesen und exportieren.</li></ul> |

## [!DNL Journey Approver] {#journey-approver}

Die Rolle **[!DNL Journey Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der **[!DNL Journey]**-Berichte überprüfen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journey]**: Veröffentlichen von Journeys.</li><li>**[!DNL View journeys events, data sources and actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage segments]**: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul> |
| Administration | <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Die Rolle **[!DNL Journey Manager]** ermöglicht Benutzenden das Erstellen und Bearbeiten von **[!UICONTROL Journeys]** und Zugriff auf alle Funktionen, die mit **[!UICONTROL Journeys]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL View journeys events]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul> |
| Administration | <ul><li>**[!DNL View channel surfaces]**: schreibgeschützter Zugriff auf Kanaloberflächen.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Die Rolle **[!DNL Journey viewer]** ermöglicht schreibgeschützten Zugriff auf die Funktionen **[!UICONTROL Journeys]** und **[!UICONTROL Entscheidungs-Management]**.

Benutzende, denen diese Rolle zugewiesen wurde, können weder bearbeiten noch veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Journeys | <ul><li>**[!DNL View journeys]**: Nur-Lese-Zugriff auf Journeys.</li><li>**[!DNL View journeys event, data sources, actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse und Datenquellen.</li><li>**[!DNL View journeys report]**: Nur-Lese-Zugriff auf Berichte von Journeys.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Die Rolle **[!DNL Decisioning manager]** ermöglicht nur den Zugriff auf das Menü **[!UICONTROL Entscheidungs-Management]**. Benutzende, denen diese Rolle zugewiesen wurde, können nur Entscheidungen verwalten, anzeigen und veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen |
|-|-|
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li><li>**[!DNL Publish decisions]**: Aktivieren oder Deaktivieren von Entscheidungsaktivitäten.</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

Die Rolle **[!DNL Content Library Manager]** ermöglicht nur den Zugriff auf das Menü **[!UICONTROL Inhaltsvorlagen]**. Benutzende, denen diese Rolle zugewiesen wurde, können nur auf die Vorlagenbibliothek zugreifen, um Inhalte zu erstellen, aber nicht auf die Journeys oder Kampagnen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen |
|-|-|
| Journey Optimizer-Bibliothek | <ul><li>**[!DNL Manage library items]**: Journey Optimizer-Bibliothekselemente lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage simulate content]**: Zugriff auf die Option **[!UICONTROL Inhalt simulieren]** für Vorschau und Testversand.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li> **[!DNL Manage segments]**: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Read datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL Read schemas]**: Nur-Lese-Zugriff auf Schemas.</li><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li></ul> |
