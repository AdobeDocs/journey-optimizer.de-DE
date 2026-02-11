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
source-git-commit: a91d5c6a22f81411d7a9acbe2bbc8e86c1a4da13
workflow-type: tm+mt
source-wordcount: '2031'
ht-degree: 96%

---

# Integrierte Rollen {#ootb-product-profiles}

Integrierte Rollen sind eine Reihe von vereinheitlichten Rechten, die Benutzenden den Zugriff auf bestimmte Funktionen oder Objekte in der Schnittstelle ermöglichen. Auf [dieser Seite](ootb-permissions.md) finden Sie eine Liste der verfügbaren Berechtigungen zur Erstellung Ihrer Rolle.


## [!DNL Campaign Administrator] {#campaign-administrator}

Die Rolle **[!DNL Campaign Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Kampagnen zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li> <li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li> <li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li> <li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li> <li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li> <li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li> <li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li> </ul> |
| Kampagnen | <ul><li> **[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Kampagnen-Berichten.</li></ul> |
| Kanalkonfigurationen | <ul> <li>**[!DNL Export suppression list]**: Zugriff auf das Exportieren der Unterdrückungsliste als CSV-Datei.</li> <li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Kampagnen, Nachrichten und Berechtigungen.</li> <li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li> <li>**[!DNL Manage landing page settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für Landingpages.</li> <li>**[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li> <li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li> <li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li> <li>**[!DNL Manage SMS settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für SMS-Nachrichten.</li> <li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Delegierung.</li> <li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li> <li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li> <li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li> </ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul> |

## [!DNL Campaign Approver] {#campaign-approver}

Die Rolle **[!DNL Campaign Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der Berichte **[!DNL Campaigns]** überprüfen.

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li></ul> |
| Kampagnen | <ul><li>**[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL Publish campaigns]**: Veröffentlichen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Kampagnenberichten.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |


## [!DNL Campaign Manager] {#campaign-manager}

Die Rolle **[!DNL Campaign Manager]** ermöglicht Benutzenden das Erstellen und Bearbeiten von **[!UICONTROL Kampagnen]** und gibt ihnen Zugriff auf alle Funktionen, die mit **[!UICONTROL Kampagnen]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li></ul> |
| Kampagnen | <ul><li>**[!DNL Manage campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von Kampagnen.</li><li>**[!DNL View campaigns report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

Die Rolle **[!DNL Campaign Viewer]** ermöglicht schreibgeschützten Zugriff auf die Funktionen **[!UICONTROL Kampagnen]** und **[!UICONTROL Entscheidungs-Management]**.

Benutzende, denen diese Rolle zugewiesen wurde, können weder bearbeiten noch veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Kampagnen | <ul><li>**[!DNL View campaigns]**: Nur-Lese-Zugriff auf Kampagnen.</li><li>**[!DNL View campaigns report]**: Nur-Lese-Zugriff auf Kampagnen-Berichte.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul> |

## [!DNL Content Library Manager] {#content-library-manager}

Die Rolle **[!DNL Content Library Manager]** ermöglicht nur den Zugriff auf das Menü **[!UICONTROL Inhaltsvorlagen]**. Benutzende, denen diese Rolle zugewiesen wurde, können nur auf die Vorlagenbibliothek zugreifen, um Inhalte zu erstellen, aber nicht auf die Journeys oder Kampagnen.

Diese Berechtigung umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Journey Optimizer-Bibliothek | <ul><li>**[!DNL Manage library items]**: Journey Optimizer-Bibliothekselemente, einschließlich Inhaltsvorlagen und Fragmenten lesen, erstellen, bearbeiten und löschen.</li><li>**[!DNL Manage simulate content]**: Zugriff auf die Option **[!UICONTROL Inhalt simulieren]** für Vorschau und Testversand.</li><li>**[!DNL Publish Fragment]**: Veröffentlichen von Inhaltsfragmenten.</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

Die Rolle **[!DNL Decisioning manager]** ermöglicht nur den Zugriff auf das Menü **[!UICONTROL Entscheidungs-Management]**. Benutzende, denen diese Rolle zugewiesen wurde, können nur Entscheidungen verwalten, anzeigen und veröffentlichen.

Diese Berechtigung umfasst die folgenden Berechtigungen:

| Funktion | Berechtigungen |
|-|-|
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li><li>**[!DNL Publish decisions]**: Aktivieren oder Deaktivieren von Entscheidungsaktivitäten.</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

Die Rolle **[!DNL Journey Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, Journeys zu verwalten und zu veröffentlichen sowie das Entscheidungs-Management zu nutzen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li> <li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li> <li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li> <li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li> <li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li> <li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li> <li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li> </ul> |
| Kanalkonfigurationen | <ul> <li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Journeys und Berechtigungen.</li> <li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li> <li>**[!DNL Manage Landing page settings]**: Erstellen, Bearbeiten und Löschen von Landingpage-Subdomains und Landingpage-Voreinstellungen.</li> <li>**[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li> <li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li> <li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li> <li>**[!DNL Manage SMS settings]**: Erstellen, Bearbeiten und Löschen von API-Anmeldedaten und SMS-Kanalkonfigurationen, die für die Aktivierung des SMS-Kanals erforderlich sind.</li> <li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Delegierung.</li> <li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li> <li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li> <li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li> </ul> |
| Data Governance | <ul> <li>**[!DNL Manage data usage policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Datennutzungsrichtlinien.</li> <li>**[!DNL Manage usage label]**: Lesen, Erstellen und Löschen von Nutzungs-Labels.</li> <li>**[!DNL View data usage policies]**: Schreibgeschützter Zugriff auf Datennutzungsrichtlinien.</li> <li>**[!DNL View user activity log]**: Schreibgeschützter Zugriff zur Anzeige aufgezeichneter Auditprotokolle zu Experience Platform-Aktivitäten.</li> </ul> |
| Entscheidungs-Management | <ul> <li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li> <li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li> </ul> |
| Journeys | <ul> <li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten, Stoppen (Live, Testmodus und Probelauf) und Löschen von Journey. </li> <li>**[!DNL Manage journeys events, data sources and actions]**: Lesen, Erstellen, Bearbeiten und Löschen von Ereignissen, Quellen oder Aktionen.</li> <li>**[!DNL Publish journeys]**: Veröffentlichen, Testmodus starten, Probelauf starten, Journey pausieren und fortsetzen. </li> <li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Berichten zu Journeys.</li> </ul> |
| Journey Optimizer-Bibliothek | <ul> <li>**[!DNL Manage Library Items]**: Hinzufügen und Löschen gespeicherter Ausdrücke in der [!DNL Journey Optimizer] Bibliothek.</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

Die Rolle **[!DNL Journey Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der **[!DNL Journey]**-Berichte überprüfen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View channel configurations]**: Nur-Lese-Zugriff auf Kanalkonfigurationen.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten, Stoppen (Live, Testmodus und Probelauf) und Löschen von Journey. </li><li>**[!DNL Publish journey]**: Veröffentlichen, Testmodus starten, Probelauf starten, Journey pausieren und fortsetzen. </li><li>**[!DNL View journeys events, data sources and actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

Die Rolle **[!DNL Journey Manager]** ermöglicht Benutzenden das Erstellen und Bearbeiten von **[!UICONTROL Journeys]** und Zugriff auf alle Funktionen, die mit **[!UICONTROL Journeys]** verknüpft sind. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li><li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View channel configurations]**: Nur-Lese-Zugriff auf Kanalkonfigurationen.</li></ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Berichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Journeys | <ul><li>**[!DNL Manage journeys]**: Lesen, Erstellen, Bearbeiten, Stoppen (Live, Testmodus und Probelauf) und Löschen von Journey.</li><li>**[!DNL View journeys events]**: Nur-Lese-Zugriff auf Journey-Ereignisse, benutzerdefinierte Journey-Aktionen und Datenquellen von Journeys.</li><li>**[!DNL View journeys report]**: Lesen und Bearbeiten von Journey-Berichten.</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

Die Rolle **[!DNL Journey viewer]** ermöglicht schreibgeschützten Zugriff auf die Funktionen **[!UICONTROL Journeys]** und **[!UICONTROL Entscheidungs-Management]**.

Benutzende, denen diese Rolle zugewiesen wurde, können weder bearbeiten noch veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Entscheidungs-Management | <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul> |
| Journeys | <ul><li>**[!DNL View journeys]**: Nur-Lese-Zugriff auf Journeys.</li><li>**[!DNL View journeys event, data sources, actions]**: Nur-Lese-Zugriff auf Journey-Ereignisse und Datenquellen.</li><li>**[!DNL View journeys report]**: Nur-Lese-Zugriff auf Berichte von Journeys.</li></ul> |

## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

Die Rolle **[!DNL Orchestrated Campaign Administrator]** ermöglicht den Zugriff auf die Administrationsmenüs mit der Möglichkeit, orchestrierte Kampagnen zu verwalten und zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Enable AI Assistant]**: Aktivieren von KI-gestützten Kampagnen- und Zielgruppenfunktionen oder Zugreifen auf diese.</li> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li> <li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li> <li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li> <li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li> <li>**[!DNL Read Identity namespace]**: Nur-Lese-Zugriff auf Identity-Namespace.</li> <li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li> <li>**[!DNL Sandbox]**: Gewähren des Zugriffs auf Sandboxes.</li> <li>**[!DNL View operational insights]**: Schreibgeschützter Zugriff auf Erkenntnis- und Überwachungs-Dashboards auf Systemebene.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL Export suppression list]**: Zugriff auf das Exportieren der Unterdrückungsliste als CSV-Datei.</li> <li>**[!DNL Manage alerts]**: Aktivieren/Deaktivieren von Warnhinweisen für Kampagnen, Nachrichten und Berechtigungen.</li> <li>**[!DNL Manage custom dashboards]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Dashboards.</li><li>**[!DNL Manage IP pools]**: Lesen, Erstellen, Bearbeiten und Löschen von IP-Pools.</li> <li>**[!DNL Manage landing page settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für Landingpages.</li> <li>**[!DNL Manage messages general settings]**: Lesen, Erstellen, Bearbeiten und Löschen der allgemeinen Einstellungen für Nachrichten.</li> <li>**[!DNL Manage messages presets]**: Lesen, Erstellen, Bearbeiten und Löschen von Inhalts-Branding.</li><li>**[!DNL Manage PTR records]**: Lesen und Bearbeiten von PTR-Einträgen.</li> <li>**[!DNL Manage SMS settings]**: Lesen, Erstellen, Bearbeiten und Löschen der Einstellungen für SMS-Nachrichten.</li> <li>**[!DNL Manage subdomains delegation]**: Lesen, Erstellen, Bearbeiten und Löschen von Subdomain-Delegierung.</li> <li>**[!DNL Manage suppression rules]**: Zugriff auf das Lesen, Erstellen, Bearbeiten und Löschen von Unterdrückungsregeln.</li> <li>**[!DNL View PTR records]**: Nur-Lese-Zugriff auf PTR-Einträge.</li> <li>**[!DNL View suppression list]**: Lesen und Exportieren der lokalen Unterdrückungsliste.</li> </ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Widgets und Widget-Schemata über die Widget-Bibliothek.</li> </ul> |
| Data Governance | <ul> <li>**[!DNL View user activity log]**: Schreibgeschützter Zugriff zur Anzeige aufgezeichneter Auditprotokolle zu Experience Platform-Aktivitäten. </li> </ul> |
| Datenaufnahme | <ul> <li>**[!DNL Manage sources]**: Lesen, Erstellen, Bearbeiten und Deaktivieren von Quellen.</li> </ul> |
| Daten-Management | <ul> <li>**[!DNL Manage datasets]**: Lesen, Erstellen, Bearbeiten und Löschen von Datensätzen. </li> </ul> |
| Datenmodellierung | <ul> <li>**[!DNL Manage schemas]**: Lesen, Erstellen, Bearbeiten und Löschen von Schemata und zugehörigen Ressourcen.</li> </ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul> |
| Journey Optimizer-Regeln | <ul> <li>**[!DNL View frequency rules]**: Schreibgeschützter Zugriff auf Häufigkeitsregeln.</li><li>**[!DNL Manage frequency rules]**: Lesen, Erstellen, Bearbeiten oder Löschen von Häufigkeitsregeln.</li> </ul> |
| Nachrichten | <ul><li> **[!DNL Manage Messages]**: Lesen, Erstellen, Bearbeiten und Löschen von Nachrichten. </li> **[!DNL Manage Messages Preview and Test]**: Genehmigen und Veröffentlichen von Nachrichten, wenn eine Richtlinie angewendet wird.</li><li>**[!DNL Publish Messages]**: Veröffentlichen von Nachrichten. </li><li>**[!DNL View Messages Report]**: Lesen und Bearbeiten von Nachrichtenberichten. <li></ul> |
| Orchestrierte Kampagnen | <ul><li> **[!DNL Manage orchestrated campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von orchestrierten Kampagnen.</li> <li>**[!DNL Manage orchestrated campaigns admin]**: Lesen, Erstellen, Bearbeiten und Löschen von Links und Abstimmungen zwischen Adobe Experience Platform-Profilen und Entitäten des relationalen Speichers.</li><li>**[!DNL Publish orchestrated campaigns]**: Veröffentlichen von orchestrierten Kampagnen</li><li>**[!DNL View orchestrated campaigns report]**: Lesen und Bearbeiten von Berichten zu orchestrierten Kampagnen.</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

Mit der Rolle **[!DNL Orchestrated Campaign Approver]** können Benutzende orchestrierte Kampagnen veröffentlichen.

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen. </li> <li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li> <li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li> <li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li> <li>**[!DNL Enable AI Assistant]**: Aktivieren von KI-gestützten Kampagnen- und Zielgruppenfunktionen oder Zugreifen auf diese.</li>  <li>**[!DNL View operational insights]**: Schreibgeschützter Zugriff auf Erkenntnis- und Überwachungs-Dashboards auf Systemebene.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL View messages presets]**: Nur-Lese-Zugriff auf Nachrichtenvoreinstellungen.</li> <li>**[!DNL Manage custom dashboards]**: Erstellen, Bearbeiten und Löschen benutzerdefinierter Dashboards.</li></ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Widgets und Widget-Schemata über die Widget-Bibliothek.</li> </ul> |
| Data Governance | <ul> <li>**[!DNL View user activity log]**: Schreibgeschützter Zugriff zur Anzeige aufgezeichneter Auditprotokolle zu Experience Platform-Aktivitäten.</li> </ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Journey Optimizer-Regeln | <ul> <li>**[!DNL View frequency rules]**: Schreibgeschützter Zugriff auf Häufigkeitsregeln.</li></ul> |
| Nachrichten | <ul><li> **[!DNL Manage Messages]**: Lesen, Erstellen, Bearbeiten und Löschen von Nachrichten. </li> **[!DNL Manage Messages Preview and Test]**: Genehmigen und Veröffentlichen von Nachrichten, wenn eine Richtlinie angewendet wird.</li><li>**[!DNL Publish Messages]**: Veröffentlichen von Nachrichten. </li><li>**[!DNL View Messages Report]**: Lesen und Bearbeiten von Nachrichtenberichten. <li></ul> |
| Orchestrierte Kampagnen | <ul><li>**[!DNL Manage orchestrated campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von orchestrierten Kampagnen.</li><li>**[!DNL Publish orchestrated campaigns]**: Veröffentlichen von orchestrierten Kampagnen</li><li>**[!DNL View orchestrated campaigns admin]**: Schreibgeschützter Zugriff auf Links und Abstimmungen zwischen Adobe Experience Platform-Profilen und Entitäten des relationalen Speichers.</li><li>**[!DNL View orchestrated campaigns report]**: Lesen und Bearbeiten von Berichten zu orchestrierten Kampagnen.</li></ul> |

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

Die Rolle **[!DNL Orchestrated Campaign Manager]** ermöglicht es Benutzenden, **[!UICONTROL orchestrierte Kampagnen]** und alle mit **[!UICONTROL orchestrierten Kampagnen]** verbundenen Funktionen zu erstellen und zu bearbeiten. Sie sind jedoch nicht in der Lage, diese zu veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: Aktivieren von KI-gestützten Kampagnen- und Zielgruppenfunktionen oder Zugreifen auf diese.</li> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li><li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li><li> **[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li><li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li>  <li>**[!DNL View operational insights]**: Schreibgeschützter Zugriff auf Erkenntnis- und Überwachungs-Dashboards auf Systemebene.</li><li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL Manage custom dashboards]**: Erstellen, Bearbeiten und Löschen benutzerdefinierter Dashboards.</li><li>**[!DNL View messages presets]**: Schreibgeschützter Zugriff auf Nachrichtenvoreinstellungen.</li></ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Widgets und Widget-Schemata über die Widget-Bibliothek.</li> </ul> |
| Data Governance | <ul> <li>**[!DNL View user activity log]**: Schreibgeschützter Zugriff zur Anzeige aufgezeichneter Auditprotokolle zu Experience Platform-Aktivitäten.</li> </ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungsfindungsentitäten.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von benutzerdefinierten Nachrichtenberichten und Verwenden von Aktionsfunktionen.</li></ul> |
| Journey Optimizer-Regeln | <ul> <li>**[!DNL View frequency rules]**: Schreibgeschützter Zugriff auf Häufigkeitsregeln. </li></ul> |
| Nachrichten | <ul><li> **[!DNL Manage Messages]**: Lesen, Erstellen, Bearbeiten und Löschen von Nachrichten. </li> **[!DNL Manage Messages Preview and Test]**: Genehmigen und Veröffentlichen von Nachrichten, wenn eine Richtlinie angewendet wird.</li><li>**[!DNL View Messages Report]**: Lesen und Bearbeiten von Nachrichtenberichten. </li></ul> |
| Orchestrierte Kampagnen | <ul><li>**[!DNL Manage orchestrated campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von orchestrierten Kampagnen.</li><li>**[!DNL View orchestrated campaigns report]**: Lesen und Bearbeiten von orchestrierten Kampagnen.</li><li>**[!DNL View orchestrated campaigns admin]**: Schreibgeschützter Zugriff auf Links und Abstimmungen zwischen Adobe Experience Platform-Profilen und Entitäten des relationalen Speichers.</li></ul> |

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

Die Rolle **[!DNL Campaign Viewer]** ermöglicht schreibgeschützten Zugriff auf die Funktionen für **[!UICONTROL orchestrierte Kampagnen]**.

Benutzende, denen diese Rolle zugewiesen wurde, können weder bearbeiten noch veröffentlichen.

Diese Rolle umfasst die folgenden Berechtigungen:

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul><li>**[!DNL Enable AI Assistant]**: Aktivieren von KI-gestützten Kampagnen- und Zielgruppenfunktionen oder Zugreifen auf diese.</li> <li>**[!DNL View operational insights]**: Schreibgeschützter Zugriff auf Erkenntnis- und Überwachungs-Dashboards auf Systemebene.</li></ul> |
| Kanalkonfigurationen | <ul><li>**[!DNL Manage custom dashboards]**: Erstellen, Bearbeiten und Löschen benutzerdefinierter Dashboards.</li></ul> |
| Dashboard | <ul> <li>**[!DNL Manage standard dashboard]**: Lesen, Erstellen, Bearbeiten und Löschen benutzerdefinierter Widgets und Widget-Schemata über die Widget-Bibliothek.</li> </ul> |
| Data Governance | <ul> <li>**[!DNL View user activity log]**: Schreibgeschützter Zugriff zur Anzeige aufgezeichneter Auditprotokolle zu Experience Platform-Aktivitäten.</li> </ul> |
| Entscheidungs-Management | <ul><li>**[!DNL View decisions]**: Nur-Lese-Zugriff auf Entscheidungsentitäten.</li></ul> |
| Journey Optimizer-Regeln | <ul> <li>**[!DNL View frequency rules]**: Schreibgeschützter Zugriff auf Häufigkeitsregeln.</li></ul> |
| Orchestrierte Kampagnen | <ul><li>**[!DNL View orchestrated campaigns]**: Schreibgeschützter Zugriff auf orchestrierte Kampagnen.</li><li>**[!DNL View orchestrated campaigns report]**: Schreibgeschützter Zugriff auf Berichte zu orchestrierten Kampagnen.</li></ul> |




