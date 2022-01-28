---
title: Berechtigungsebenen
description: Erfahren Sie mehr über Berechtigungen auf hoher und niedriger Ebene.
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: bbeecbacb4838dfb0794d5625eb2774cf4b983ef
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 55%

---

# Berechtigungsebenen {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Jedes Produktprofil besteht aus Berechtigungen, die Benutzern den Zugriff auf die verschiedenen Funktionen ermöglichen.
Sie können in zwei Typen unterteilt werden:

* **Berechtigung auf hoher Ebene**: stellt die verschiedenen Berechtigungen dar, die zugewiesen werden können **[!UICONTROL Produktprofil]** im [!DNL Admin console], z. B. **[!DNL Publish journeys]** und **[!DNL Manage subdomains delegation]**. Berechtigungen auf hoher Ebene beinhalten Berechtigungen auf niedriger Ebene.

* **Berechtigung auf niedriger Ebene**: beinhalten die verschiedenen Berechtigungen, die von der Berechtigung auf hoher Ebene stammen.

Beispiel: die **[!DNL Journey administrator]** dem Produktprofil wird die **[!DNL Manage journeys]** Berechtigung. Aus dieser Berechtigung stammen die Berechtigungen auf niedriger Ebene, die es dem Journey-Administrator ermöglichen, Journeys zu schreiben, zu lesen und zu löschen.

## Journey-Funktion {#journey-capability}

### [!DNL Manage journeys] Berechtigung {#manage-journeys}

Die **[!DNL Manage journeys]** Die Berechtigung auf hoher Ebene ermöglicht es Benutzern, neue Journey zu erstellen und bestehende zu bearbeiten/zu löschen sowie auf die Objekte zuzugreifen, die in der Journey-Arbeitsfläche zum Erstellen des Journey-Flusses verwendet werden.

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

### [!DNL Publish journeys] Berechtigung {#publish-journeys}

Die **[!DNL Publish journeys]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, Journey zu veröffentlichen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys.publish
   * journeys.read

### [!DNL View journeys] Berechtigung {#view-journeys}

Die **[!DNL View journeys]** -Berechtigung auf hoher Ebene ermöglicht Benutzern das Durchsuchen und Anzeigen von Journey.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys.read

* Spezifisch für Adobe Experience Platform:
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] Berechtigung {#manage-journeys-events}

Die **[!DNL Manage journeys events, data sources and actions]** Mit Berechtigungen auf hoher Ebene können Benutzer Ereignis- und Datenkonfigurationen konfigurieren.

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

### [!DNL View journeys events, data sources and actions] Berechtigung {#view-journeys-event}

Die **[!DNL View journeys events, data sources and actions]** -Berechtigung auf hoher Ebene ermöglicht Benutzern die Verwendung von Ereignissen und Daten im Journey-Fluss.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * Journey_events.read
   * Journey_data_sources.read
   * Journey_actions.read

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] Berechtigung {#view-journeys-report}

Die **[!DNL View journeys report]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, schreibgeschützten Journey-Bericht zu erstellen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys_report.read
   * messages_report.read

* Spezifisch für Adobe Experience Platform:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Nachrichtenfunktionen {#message-capability}

### [!DNL Manage messages] Berechtigung {#manage-messages}

Die **[!DNL Manage messages]** -Berechtigung auf hoher Ebene ermöglicht Benutzern das Erstellen und Bearbeiten und Löschen von Nachrichten.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Spezifisch für Adobe Experience Platform:
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] Berechtigung {#mange-messages-preview}

Die **[!DNL Manage messages preview and test]** -Berechtigung auf hoher Ebene ermöglicht Benutzern die Vorschau einer personalisierten Nachricht.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### [!DNL Publish messages] Berechtigung {#publish-messages}

Die **[!DNL Publish messages]** -Berechtigung auf hoher Ebene ermöglicht Benutzern das Veröffentlichen von Nachrichten.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages.publish

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] Berechtigung {#view-messages}

Die **[!DNL View messages]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, nur Nachrichten zu lesen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages.read
   * messages_presets.read

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * segments.read

### [!DNL View messages report] Berechtigung {#view-message-reports}

Die **[!DNL View messages report]** Mit allgemeinen Berechtigungen können Benutzer schreibgeschützte E-Mail- und Push-Berichte erstellen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Entscheidungs-management-funktion {#decisions-permissions}

### [!DNL Manage decisions] Berechtigung {#manage-decisioning}

Die **[!DNL Manage decisions]** Berechtigung auf hoher Ebene ermöglicht Benutzern das Erstellen neuer und Bearbeiten/Löschen vorhandener **[!DNL Activity entities]** und verwalten die Objekte, die in diesen Aktivitäten für die Entscheidungsfindung verwendet werden.

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

### [!DNL View decisions] Berechtigung {#view-decisions}

Die **[!DNL View decisions]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, eine vorhandene Aktivität und verwandte Geschäftsobjekte zu verwenden, um Entscheidungen zu treffen.

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

### [!DNL Publish offers decisioning] Berechtigung {#publish-decisions}

Die **[!DNL Publish offers decisioning]** -Berechtigung auf hoher Ebene ermöglicht Benutzern den Zugriff auf die Genehmigung/Aufhebung der Genehmigung von Angebotsaktivitäten.

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

### [!DNL Manage ranking strategies] Berechtigung {#manage-decisions}

Die **[!DNL Manage ranking strategies]** Mit allgemeinen Berechtigungen können Benutzer benutzerdefinierte Nachrichtenberichte lesen, erstellen, bearbeiten und löschen sowie Aktionsfunktionen verwenden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für das Entscheidungs-Management:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Verwaltungsfunktionen {#administration-permissions}

### [!DNL Manage subdomains delegation] Berechtigung {#manage-subdomain}

Die **[!DNL Manage subdomains delegation]** Mit einer allgemeinen Berechtigung können Benutzer Subdomain-Delegationen erstellen, bearbeiten und löschen (einschließlich IP-Pool).

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] Berechtigung {#manage-ptr}

Die **[!DNL Manage PTR records]** Mit allgemeinen Berechtigungen können Benutzer PTR-Einträge, die basierend auf der Subdomain konfiguriert wurden, lesen, erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* PTR_records.read
* PTR_records.write
* subdomains_delegation.read

### [!DNL View PTR records] Berechtigung {#view-ptr}

Die **[!DNL View PTR records]** Mit einer allgemeinen Berechtigung können Benutzer PTR-Datensätze anzeigen, die basierend auf der Subdomain konfiguriert wurden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* PTR_records.read
* subdomains_delegation.read

### [!DNL Manage IP pools] Berechtigung {#manage-ip-pools}

Die **[!DNL Manage IP pools]** Mit Berechtigung auf hoher Ebene können Benutzer die Affinitätsdefinition erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### [!DNL Manage messages general settings] Berechtigung {#manage-message-settings}

Die **[!DNL Manage messages general settings]** Mit Berechtigungen auf hoher Ebene können Benutzer globale Einstellungen auf Sandbox-Ebene erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Spezifisch für Adobe Experience Platform:
   * schemas.read

### [!DNL View messages general settings] Berechtigung {#view-message-settings}

Die **[!DNL View messages general settings]** -Berechtigung auf hoher Ebene ermöglicht Benutzern, allgemeine Einstellungen für Nachrichten wie die Ausführungsadresse anzuzeigen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_general_settings.read
* Spezifisch für Adobe Experience Platform:
   * schemas.read

### [!DNL Manage messages presets] Berechtigung {#manage-message-presets}

Die **[!DNL Manage messages presets]** Mit Berechtigung auf hoher Ebene können Benutzer Nachrichtenvorgaben kanalübergreifend auf Sandbox-Ebene erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (aus Adobe Experience Platform Launch)

### [!DNL View messages presets] Berechtigung {#view-message-presets}

Die **[!DNL View messages presets]** Mit Berechtigung auf hoher Ebene können Benutzer Nachrichtenvorgaben anzeigen, um zu erfahren, welche Nachrichtenvorgaben beim Erstellen einer Nachricht verwendet werden sollen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (aus der Adobe Experience Platform-Datenerfassung)

### [!DNL Manage suppression] Berechtigung {#manage-suppression}

Die **[!DNL Manage suppression]** Mit einer allgemeinen Berechtigung können Benutzer die Anzahl der Bounces definieren, bevor eine E-Mail-Adresse zur Unterdrückungsliste hinzugefügt wird, sowie Einträge zur Unterdrückungsliste hinzufügen und daraus löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] Berechtigung {#view-suppression-list}

Die **[!DNL View suppression list]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, den Inhalt und die Einstellungen der Unterdrückungsliste anzuzeigen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * suppression_list.view

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] Berechtigung {#export-suppression-list}

Die **[!DNL Export suppression list]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, die Unterdrückungsliste als CSV-Datei herunterzuladen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * suppression_list.export

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * datasets.read
