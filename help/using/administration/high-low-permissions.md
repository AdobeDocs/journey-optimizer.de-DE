---
solution: Journey Optimizer
product: journey optimizer
title: Berechtigungsebenen
description: Erfahren Sie mehr über Berechtigungen auf hoher und niedriger Ebene.
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 100%

---

# Berechtigungsebenen {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Jedes Produktprofil besteht aus Berechtigungen, die Benutzenden den Zugriff auf die verschiedenen Funktionen ermöglichen.
Sie können in zwei Typen unterteilt werden:

* **Berechtigung auf hoher Ebene**: beinhaltet die verschiedenen Berechtigungen, die **[!UICONTROL Produktprofilen]** in [!DNL Admin console] zugewiesen werden können, z. B. **[!DNL Publish journeys]** und **[!DNL Manage subdomains delegation]**. Berechtigungen auf hoher Ebene beinhalten Berechtigungen auf niedriger Ebene.

* **Berechtigung auf niedriger Ebene**: beinhalten die verschiedenen Berechtigungen, die von der Berechtigung auf hoher Ebene stammen.

Dem Produktprofil **[!DNL Journey administrator]** wird zum Beispiel die Berechtigung **[!DNL Manage journeys]** zugewiesen. Aus dieser Berechtigung stammen die Berechtigungen auf niedriger Ebene, die es dem Journey-Administrator ermöglichen, Journeys zu schreiben, zu lesen und zu löschen.

## Journey-Funktion {#journey-capability}

### Berechtigung [!DNL Manage journeys] {#manage-journeys}

Die Berechtigung **[!DNL Manage journeys]** auf hoher Ebene ermöglicht Benutzenden das Erstellen neuer und das Bearbeiten/Löschen vorhandener Journeys sowie den Zugriff auf die Objekte, die in der Journey-Arbeitsfläche zum Erstellen des Journey Flow verwendet werden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Spezifisch für Adobe Experience Platform:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### Berechtigung [!DNL Publish journeys] {#publish-journeys}

Mit der Berechtigung **[!DNL Publish journeys]** auf hoher Ebene können Benutzende Journeys veröffentlichen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys.publish
   * journeys.read

### Berechtigung [!DNL View journeys] {#view-journeys}

Die Berechtigung **[!DNL View journeys]** auf hoher Ebene ermöglicht Benutzenden das Durchsuchen und Anzeigen von Journeys.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys.read

* Spezifisch für Adobe Experience Platform:
   * segments.read
   * profiles.read

### Berechtigung [!DNL Manage journeys events, data sources and actions] {#manage-journeys-events}

Mit der Berechtigung **[!DNL Manage journeys events, data sources and actions]** auf hoher Ebene können Benutzende Ereignis- und Datenkonfigurationen durchführen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys_events.read
   * journeys_events.write
   * journeys_events.delete
   * journeys_data_sources.read
   * journeys_data_sources.write
   * journeys_data_sources.delete
   * journeys_actions.read
   * journeys_actions.write
   * journeys_actions.delete

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Berechtigung [!DNL View journeys events, data sources and actions] {#view-journeys-event}

Die Berechtigung **[!DNL View journeys events, data sources and actions]** auf hoher Ebene ermöglicht Benutzenden die Verwendung von Ereignissen und Daten im Journey Flow.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Berechtigung [!DNL View journeys report] {#view-journeys-report}

Die Berechtigung **[!DNL View journeys report]** auf hoher Ebene ermöglicht es Benutzenden, auf schreibgeschützte Journey-Berichte zuzugreifen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys_report.read
   * messages_report.read

* Spezifisch für Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Entscheidungs-Management-Funktion {#decisions-permissions}

### Berechtigung [!DNL Manage decisions] {#manage-decisioning}

Die Berechtigung **[!DNL Manage decisions]** auf hoher Ebene ermöglicht Benutzenden das Erstellen neuer und das Bearbeiten/Löschen vorhandener **[!DNL Activity entities]** sowie das Verwalten der Objekte, die in diesen Aktivitäten zur Entscheidungsfindung verwendet werden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für das Entscheidungs-Management:
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Spezifisch für Adobe Experience Platform:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### Berechtigung [!DNL View decisions] {#view-decisions}

Mit der Berechtigung **[!DNL View decisions]** auf hoher Ebene können Benutzende eine vorhandene Aktivität und zugehörige Geschäftsobjekte verwenden, um Entscheidungen zu treffen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für das Entscheidungs-Management:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### Berechtigung [!DNL Publish offers decisioning] {#publish-decisions}

Die Berechtigung **[!DNL Publish offers decisioning]** auf hoher Ebene ermöglicht es Benutzenden, Angebotsaktivitäten zu genehmigen bzw. deren Genehmigung zurückzunehmen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für das Entscheidungs-Management:
   * offers_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### Berechtigung [!DNL Manage ranking strategies] {#manage-ranking-strategies}

Die Berechtigung auf hoher Ebene **[!DNL Manage ranking strategies]** ermöglicht es Benutzenden, Rangfolgestrategien zu lesen, zu erstellen, zu bearbeiten und zu löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für das Entscheidungs-Management:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Verwaltungsfunktionen {#administration-permissions}

### Berechtigung [!DNL Manage subdomains delegation] {#manage-subdomain}

Mit der Berechtigung **[!DNL Manage subdomains delegation]** auf hoher Ebene können Benutzende die Zuweisung von Subdomains (einschließlich IP-Pool) erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### Berechtigung [!DNL Manage PTR records] {#manage-ptr}

Die **[!DNL Manage PTR records]** High-Level-Berechtigung ermöglicht es Benutzern, PTR-Einträge, die basierend auf der Subdomain konfiguriert wurden, zu lesen und zu bearbeiten.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### Berechtigung [!DNL View PTR records] {#view-ptr}

Die Berechtigung **[!DNL View PTR records]** auf hoher Ebene ermöglicht Benutzenden das Anzeigen von PTR-Einträgen, die basierend auf der Subdomain konfiguriert wurden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* PTR_records.read
* subdomains_delegation.read

### Berechtigung [!DNL Manage IP pools] {#manage-ip-pools}

Mit der Berechtigung **[!DNL Manage IP pools]** auf hoher Ebene können Benutzende eine Affinitätsdefinition erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->

### Berechtigung [!DNL Manage channel surface] {#manage-channel-surface}

Die Berechtigung **[!DNL Manage channel surface]** auf hoher Ebene ermöglicht es Benutzenden, Kanaloberflächen kanalübergreifend auf Sandbox-Ebene zu erstellen, zu bearbeiten und zu löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (aus Adobe Experience Platform Launch)

### Berechtigung [!DNL View channel surface] {#view-channel-surface}

Die Berechtigung **[!DNL View channel surface]** auf hoher Ebene ermöglicht es Benutzenden, Kanaloberflächen zu anzusehen, um festzustellen, welche Kanaloberflächen zu verwenden sind.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (aus Adobe Experience Platform-Datensammlung)

### Berechtigung [!DNL Manage suppression] {#manage-suppression}

Mit der Berechtigung auf hoher Ebene **[!DNL Manage suppression]** können Benutzende definieren, wie viele Bounces auftreten können, bevor eine E-Mail-Adresse zur Unterdrückungsliste hinzugefügt wird, sowie Einträge zur Unterdrückungsliste hinzufügen und daraus löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### Berechtigung [!DNL View suppression list] {#view-suppression-list}

Mit der Berechtigung **[!DNL View suppression list]** auf hoher Ebene können Benutzende den Inhalt und die Einstellungen der Unterdrückungsliste anzeigen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * suppression_list.view

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Berechtigung [!DNL Export suppression list] {#export-suppression-list}

Mit der Berechtigung auf hoher Ebene **[!DNL Export suppression list]** können Benutzende die Unterdrückungsliste als CSV-Datei herunterladen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * suppression_list.export

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Berechtigung [!DNL Manage landing page settings] {#manage-landing-page-settings}

Die Berechtigung auf höchster Ebene in **[!DNL Manage landing page settings]** erlaubt es Benutzenden, Landingpage-Subdomains und Voreinstellungen zu lesen, zu erstellen und zu bearbeiten.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### Berechtigung [!DNL Manage frequency rules] {#manage-frequency-rules}

Die Berechtigung auf hoher Ebene **[!DNL Manage frequency rules]** ermöglicht es Benutzenden, Häufigkeitsregeln zu lesen, zu erstellen, zu bearbeiten, zu löschen und zu aktivieren/deaktivieren.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### Berechtigung [!DNL View frequency rules] {#view-frequency-rules}

Mit der Berechtigung **[!DNL View frequency rules]** auf hoher Ebene können Benutzende Häufigkeitsregeln lesen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * frequency_rules.read
