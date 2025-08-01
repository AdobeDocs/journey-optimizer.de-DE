---
solution: Journey Optimizer
product: journey optimizer
title: 'In Journey Optimizer integrierte Rollen '
description: Erfahren Sie mehr über die integrierten Rollen.
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: Berechtigungen, Authoring, Nachrichten
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: ee2e07353762a81aadd3d63580c528f617599623
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 100%

---

# Integrierte Rollen {#ootb-product-profiles}

Integrierte Rollen sind eine Reihe von vereinheitlichten Rechten, die Benutzenden den Zugriff auf bestimmte Funktionen oder Objekte in der Schnittstelle ermöglichen. Auf [dieser Seite](ootb-permissions.md) finden Sie eine Liste der verfügbaren Berechtigungen zur Erstellung Ihrer Rolle.

## [!DNL Content Library Manager] {#content-library-manager}

Die Rolle **[!DNL Content Library Manager]** ermöglicht nur den Zugriff auf das Menü **[!UICONTROL Inhaltsvorlagen]**. Benutzende, denen diese Rolle zugewiesen wurde, können nur auf die Vorlagenbibliothek zugreifen, um Inhalte zu erstellen, aber nicht auf die Journeys oder Kampagnen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen |
|-|-|
| Journey Optimizer-Bibliothek | <ul><li>**[!DNL Manage library items]**: Journey Optimizer-Bibliothekselemente, einschließlich Inhaltsvorlagen und Fragmenten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage simulate content]**: Zugriff auf die Option **[!UICONTROL Inhalt simulieren]** für Vorschau und Testversand.</li><li>**[!DNL Publish Fragment]**: Veröffentlichen von Inhaltsfragmenten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: Nur-Lese-Zugriff auf Schemata.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Die Rolle **[!DNL Decisioning manager]** ermöglicht nur den Zugriff auf das Menü **[!UICONTROL Entscheidungs-Management]**. Benutzende, denen diese Rolle zugewiesen wurde, können nur Entscheidungen verwalten, anzeigen und veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen |
|-|-|
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li><li>**[!DNL Publish decisions]**: Aktivieren oder Deaktivieren von Entscheidungsaktivitäten.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

Die Rolle **[!DNL Campaign Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Kampagnen zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li> **[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Kampagnen-Berichten.</li></ul> |
| Kanalkonfigurationen | <ul> <li>**[!DNL Export suppression list]**: Zugriff auf das Exportieren der Unterdrückungsliste als CSV-Datei.</li> <li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Kampagnen, Nachrichten und Berechtigungen.</li> <li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li> <li>**[!DNL Manage landing page settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für Landingpages.</li> <li>**[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li> <li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li> <li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li> <li>**[!DNL Manage SMS settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für SMS-Nachrichten.</li> <li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Delegierung.</li> <li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li> <li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li> <li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li> </ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li> <li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li> <li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li> <li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li> <li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li> <li>**[!DNL View schemas]**: Nur-Lese-Zugriff auf Schemata.</li> <li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Die Rolle **[!DNL Campaign Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der Berichte **[!DNL Campaigns]** überprüfen.

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li>**[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Kampagnenberichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: Nur-Lese-Zugriff auf Schemata.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

Die Rolle **[!DNL Campaign Manager]** ermöglicht Benutzenden das Erstellen und Bearbeiten von **[!UICONTROL Kampagnen]** und gibt ihnen Zugriff auf alle Funktionen, die mit **[!UICONTROL Kampagnen]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li>**[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: Nur-Lese-Zugriff auf Schemata.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul> |

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
| Journeys | <ul> <li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li> <li>**[!DNL Manage journeys events, data sources and actions]**: Lesen, Erstellen, Bearbeiten und Löschen von Ereignissen, Quellen oder Aktionen.</li> <li>**[!DNL Publish journeys]**: Veröffentlichen von Journeys.</li> <li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Berichten zu Journeys.</li> </ul> |
| Kanalkonfigurationen | <ul> <li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Journeys und Berechtigungen.</li> <li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li> <li>**[!DNL Manage Landing page settings]**: Erstellen, Bearbeiten und Löschen von Landingpage-Subdomains und Landingpage-Voreinstellungen.</li> <li>**[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li> <li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li> <li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li> <li>**[!DNL Manage SMS settings]**: Erstellen, Bearbeiten und Löschen von API-Anmeldedaten und SMS-Kanalkonfigurationen, die für die Aktivierung des SMS-Kanals erforderlich sind.</li> <li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Delegierung.</li> <li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li> <li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li> <li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li> </ul> |
| Entscheidungs-Management | <ul> <li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li> <li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li> <li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li> <li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li> <li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li> <li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li> <li>**[!DNL View schemas]**: Nur-Lese-Zugriff auf Schemata.</li> <li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li> </ul> |
| Journey Optimizer-Bibliothek | <ul> <li>**[!DNL Manage Library Items]**: Hinzufügen und Löschen gespeicherter Ausdrücke in der [!DNL Journey Optimizer] Bibliothek.</li> </ul> |
| Data Governance | <ul> <li>**[!DNL Manage data usage policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Datennutzungsrichtlinien.</li> <li>**[!DNL Manage usage label]**: Lesen, Erstellen und Löschen von Nutzungs-Labels.</li> <li>**[!DNL View data usage policies]**: schreibgeschützter Zugriff auf Datennutzungsrichtlinien.</li> <li>**[!DNL View user activity log]**: Auditprotokolle lesen und exportieren.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

Die Rolle **[!DNL Journey Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der **[!DNL Journey]**-Berichte überprüfen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL Publish journey]**: Veröffentlichen von Journeys.</li><li>**[!DNL View journeys events, data sources and actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: Nur-Lese-Zugriff auf Schemata.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View channel configurations]**: Nur-Lese-Zugriff auf Kanalkonfigurationen.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Die Rolle **[!DNL Journey Manager]** ermöglicht Benutzenden das Erstellen und Bearbeiten von **[!UICONTROL Journeys]** und Zugriff auf alle Funktionen, die mit **[!UICONTROL Journeys]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten und Löschen von Journeys.</li><li>**[!DNL View journeys events]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: Nur-Lese-Zugriff auf Schemata.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View channel configurations]**: Nur-Lese-Zugriff auf Kanalkonfigurationen.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Die Rolle **[!DNL Journey viewer]** ermöglicht schreibgeschützten Zugriff auf die Funktionen **[!UICONTROL Journeys]** und **[!UICONTROL Entscheidungs-Management]**.

Benutzende, denen diese Rolle zugewiesen wurde, können weder bearbeiten noch veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Journeys | <ul><li>**[!DNL View journeys]**: Nur-Lese-Zugriff auf Journeys.</li><li>**[!DNL View journeys event, data sources, actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse und Datenquellen.</li><li>**[!DNL View journeys report]**: Nur-Lese-Zugriff auf Berichte von Journeys.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Orchestrated Campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: read, create, edit, and delete custom dashboards.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: Read, create, edit and delete links and reconciliations between Adobe Experience Platform Profiles and Relational store entities.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL View sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to publish Orchestrated campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaign reports.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li> </ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Orchestrated campaigns]** and every capability linked to **[!UICONTROL Orchestrated campaigns]** but will not be able to publish them.

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Orchestrated campaigns]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Messages|<ul><li>**[!DNL View messages]**: view messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

-->