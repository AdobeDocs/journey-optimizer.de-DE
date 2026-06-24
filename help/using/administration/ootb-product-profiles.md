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
TQID: https://experienceleague.adobe.com/LkOCFOSH-AzwWMoteNN-XI3R2yYkO5iBrVwMtobd4iI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 2684
ht-degree: 76%

---

# Integrierte Rollen {#ootb-product-profiles}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Informieren Sie sich über die integrierten Rollen und Berechtigungen, die jede Rolle enthält, damit Sie Benutzern schnell eine vorgefertigte Zugriffsebene gewähren können, die ihren Verantwortlichkeiten entspricht.

>[!ENDSHADEBOX]

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

Die Rolle **[!DNL Journey Approver]** ermöglicht es Benutzenden, Sendungen zu genehmigen und zu veröffentlichen. Später können sie den Erfolg ihrer Sendungen anhand der Berichte **[!DNL Journey]** überprüfen.

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
| Daten-Management | <ul> <li>**[!DNL Manage datasets]**: Lesen, Erstellen, Bearbeiten und Löschen von Datensätzen.</li> </ul> |
| Datenmodellierung | <ul> <li>**[!DNL Manage schemas]**: Lesen, Erstellen, Bearbeiten und Löschen von Schemata und zugehörigen Ressourcen.</li> </ul> |
| Entscheidungs-Management | <ul><li>**[!DNL Manage decisions]**: Lesen, Erstellen, Bearbeiten und Löschen von Entscheidungen.</li><li>**[!DNL Manage ranking strategies]**: Lesen, Erstellen, Bearbeiten und Löschen von Rangfolgestrategien.</li></ul> |
| Journey Optimizer-Regeln | <ul> <li>**[!DNL View frequency rules]**: Schreibgeschützter Zugriff auf Häufigkeitsregeln.</li><li>**[!DNL Manage frequency rules]**: Lesen, Erstellen, Bearbeiten oder Löschen von Häufigkeitsregeln.</li> </ul> |
| Nachrichten | <ul><li> **[!DNL Manage Messages]**: Lesen, Erstellen, Bearbeiten und Löschen von Nachrichten. </li> **[!DNL Manage Messages Preview and Test]**: Genehmigen und Veröffentlichen von Nachrichten, wenn eine Richtlinie angewendet wird.</li><li>**[!DNL Publish Messages]**: Veröffentlichen von Nachrichten. </li><li>**[!DNL View Messages Report]**: Lesen und Bearbeiten von Nachrichtenberichten. <li></ul> |
| Orchestrierte Kampagnen | <ul><li> **[!DNL Manage orchestrated campaigns]**: Lesen, Erstellen, Bearbeiten und Löschen von orchestrierten Kampagnen.</li> <li>**[!DNL Manage orchestrated campaigns admin]**: Lesen, Erstellen, Bearbeiten und Löschen von Links und Abstimmungen zwischen Adobe Experience Platform-Profilen und Entitäten des relationalen Speichers.</li><li>**[!DNL Publish orchestrated campaigns]**: Veröffentlichen von orchestrierten Kampagnen</li><li>**[!DNL View orchestrated campaigns report]**: Lesen und Bearbeiten von Berichten zu orchestrierten Kampagnen.</li></ul> |

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

Mit der Rolle **[!DNL Orchestrated Campaign Approver]** können Benutzende orchestrierte Kampagnen veröffentlichen.

| Ressourcen | Berechtigungen |
|-|-|
| Adobe Experience Platform | <ul> <li>**[!DNL Manage segments]**: Lesen, Erstellen, Bearbeiten und Löschen von Segmentdefinitionen.</li> <li>**[!DNL Manage profiles]**: Lesen, Erstellen, Bearbeiten und Löschen von Profilen.</li> <li>**[!DNL View datasets]**: Nur-Lese-Zugriff auf Datensätze.</li> <li>**[!DNL View schemas]**: schreibgeschützter Zugriff auf Schemata.</li> <li>**[!DNL Manage merge policies]**: Lesen, Erstellen, Bearbeiten und Löschen von Zusammenführungsrichtlinien.</li> <li>**[!DNL Enable AI Assistant]**: Aktivieren von KI-gestützten Kampagnen- und Zielgruppenfunktionen oder Zugreifen auf diese.</li>  <li>**[!DNL View operational insights]**: Schreibgeschützter Zugriff auf Erkenntnis- und Überwachungs-Dashboards auf Systemebene.</li></ul> |
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

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Journey Optimizer wird mit integrierten Rollen ausgeliefert - vom Kampagnenadministrator bis zum orchestrierten Kampagnen-Viewer - die jeweils einen vorgefertigten Berechtigungssatz enthalten, sodass Admins Benutzenden schnell Zugriff gewähren können, der ihren Verantwortlichkeiten entspricht, ohne eine Rolle von Grund auf neu zu erstellen.

**intents:**

* Identifizieren Sie, welche integrierte Rolle am besten zu den Aufgabenbereichen eines Benutzers passt.
* Verstehen, was jede integrierte Rolle tun kann und was nicht (einschließlich Veröffentlichungsberechtigungen)
* Rollen in Journey-, Kampagnen- und orchestrierten Kampagnendomänen vergleichen
* Zuweisen einer vorgefertigten Rolle anstelle der Erstellung einer benutzerdefinierten Rolle
* verstehen, welche Rollen den Zugriff auf KI-Assistenten umfassen

**Glossar:**

* **Integrierte Rolle**: Ein vordefinierter Satz von Berechtigungen und Ressourcenrechten, die Benutzern ohne benutzerdefinierte Konfiguration zugewiesen werden können *(produktspezifisch)*
* **Journey-Administrator**: Integrierte Rolle, die die Verwaltung und Veröffentlichung von Journey und Entscheidungs-Management ermöglicht, einschließlich Kanalkonfiguration und Data-Governance-Berechtigungen *(produktspezifisch)*
* **Campaign-Administrator**: Integrierte Rolle, die die Verwaltung und Veröffentlichung von Kampagnen und das Entscheidungs-Management ermöglicht, einschließlich Kanalkonfigurationen *(produktspezifisch)*
* **Entscheidungs-Manager**: Integrierte Rolle, die ausschließlich Zugriff auf das Menü Entscheidungs-Management bietet; kann Entscheidungen verwalten, anzeigen und veröffentlichen *(produktspezifisch)*
* **Inhaltsbibliotheks-Manager**: Integrierte Rolle, die nur Zugriff auf das Menü Inhaltsvorlagen bietet; kein Zugriff auf Journey oder Kampagnen *(produktspezifisch)*
* **Testmodus**: Ein Journey-Ausführungsmodus, auf den in den Berechtigungen Journey verwalten und Journey veröffentlichen verwiesen wird (Journey-Administrator kann Journey im Testmodus stoppen; Berechtigung zum Veröffentlichen von Journey umfasst das Starten des Testmodus) *(produktspezifisch)*
* **Probelauf** Ein Journey-Ausführungsmodus, auf den in den Berechtigungen Journey verwalten und Journey veröffentlichen neben dem Testmodus verwiesen wird *(produktspezifisch)*

**Terminologie:**

* Kanonischer Name: Integrierte Rollen - Varianten: vordefinierte Rollen, vordefinierte Rollen, Produktprofile
* Verwechseln Sie nicht: „Kampagnen-Genehmiger“ (kann Kampagnen genehmigen und veröffentlichen) ≠ „Kampagnen-Manager“ (kann Kampagnen erstellen und bearbeiten, aber nicht veröffentlichen)
* Verwechseln Sie nicht: &quot;Journey-Genehmiger“ (kann Journey genehmigen und veröffentlichen) ≠ &quot;Journey-Manager“ (kann Journey erstellen und bearbeiten, aber nicht veröffentlichen)
* Verwechseln Sie nicht: &quot;Journey-Viewer“ (Nur-Lese-Zugriff auf Journey und Entscheidungs-Management) ≠ „Kampagnen-Viewer“ (Nur-Lese-Zugriff auf Kampagnen und Entscheidungs-Management)
* Verwechseln Sie nicht: „Administrator für orchestrierte Kampagnen“ (verwaltet orchestrierte Kampagnen, umfasst KI-Assistenten und Datenaufnahme/-verwaltung) ≠ „Kampagnenadministrator“ (verwaltet Standardkampagnen; umfasst keine Berechtigungen für orchestrierte Kampagnen)
* Verwechseln Sie nicht: „Testmodus“ (referenziert als Journey-Ausführungsstatus, der über Journey verwalten / Publish-Journey angehalten oder gestartet werden kann) ≠ „Probelauf“ (ein separater Journey-Ausführungsmodus, der auch in diesen Berechtigungen referenziert wird)

**FAQ:**

* **F: Welche integrierten Rollen können Journey veröffentlichen?** — Journey-Administrator und Journey-Genehmiger können Journey veröffentlichen.
* **F: Kann ein Journey-Manager Journey veröffentlichen?** — Nein; Journey-Manager kann Journey erstellen und bearbeiten, aber die Berechtigung Journey veröffentlichen ist in dieser Rolle nicht enthalten.
* **F: Welche Rolle gewährt nur Zugriff auf das Menü des Entscheidungs-Managements?** — Entscheidungs-Manager.
* **F: Welche Rolle bietet nur Zugriff auf Inhaltsvorlagen?** — Content Library Manager.
* **F: Welche integrierten Rollen enthalten die Berechtigung KI-Assistenten aktivieren?** — Administrator der orchestrierten Kampagne, Genehmigende Person der orchestrierten Kampagne, Manager der orchestrierten Kampagne und Betrachtende der orchestrierten Kampagne.

+++
<!-- ai-accordion-version: 1 | source-hash: b9740765 -->




