---
title: Berechtigungsebenen
description: Erfahren Sie mehr über Berechtigungen auf hoher und niedriger Ebene
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
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Kontrollgruppen
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Berechtigungsstufen {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Jedes Produktprofil besteht aus Berechtigungen, die Benutzern den Zugriff auf die verschiedenen Funktionen ermöglichen.
Sie können in zwei Typen unterteilt werden:

* **Allgemeine Berechtigung**: stellt die verschiedenen Berechtigungen dar, die  **[!UICONTROL Produkt-]** Profilen in zugewiesen werden können,  [!DNL Admin console]z. B.  **[!UICONTROL Veröffentlichen von]** Journeys und  **[!UICONTROL Verwalten der Subdomain-Zuweisung]**. Berechtigungen auf hoher Ebene umfassen Berechtigungen auf niedriger Ebene.

* **Berechtigung** auf niedriger Ebene: stellt die verschiedenen Berechtigungen dar, die von der Berechtigung auf hoher Ebene stammen.

Beispielsweise wird dem Produktprofil **[!UICONTROL Journey administrator]** die Berechtigung **[!UICONTROL Journey verwalten]** zugewiesen. Aus dieser Berechtigung resultieren die Berechtigungen auf niedriger Ebene, die es dem Journey-Administrator ermöglichen, Journey zu schreiben, zu lesen und zu löschen.

## Journey-Funktion {#journey-capability}

### Berechtigung für Journey verwalten {#manage-journeys}

Die Berechtigung **[!UICONTROL Journey verwalten]** auf hoher Ebene ermöglicht Benutzern das Erstellen neuer und Bearbeiten/Löschen vorhandener Journey sowie den Zugriff auf die Objekte, die in der Arbeitsfläche des Journey zum Erstellen des Journey-Flusses verwendet werden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Adobe Experience Platform-spezifisch:

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### Berechtigung für Journey veröffentlichen {#publish-journeys}

Mit der Berechtigung **[!UICONTROL Journey veröffentlichen]** auf hoher Ebene können Benutzer Journey veröffentlichen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * journeys.publish
   * journeys.read

### Berechtigung für Journey anzeigen {#view-journeys}

Die Berechtigung **[!UICONTROL Journey anzeigen]** auf hoher Ebene ermöglicht Benutzern das Durchsuchen und Anzeigen von Journey.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * journeys.read

* Adobe Experience Platform-spezifisch:
   * segments.read
   * profiles.read

### Berechtigung für Journey-Ereignisse, Datenquellen und Aktionen verwalten {#manage-journeys-events}

Mit der Berechtigung **[!UICONTROL Journey-Ereignisse, Datenquellen und Aktionen verwalten]** auf hoher Ebene können Benutzer Ereignis- und Datenkonfigurationen konfigurieren.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * Journey_events.read
   * Journey_events.write
   * Journey_events.delete
   * Journey_data_sources.read
   * Journey_data_sources.write
   * Journey_data_sources.delete
   * Journey_actions.read
   * Journey_actions.write
   * Journey_actions.delete
* Adobe Experience Platform-spezifisch:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Berechtigung zum Anzeigen von Journey-Ereignissen, Datenquellen und Aktionen {#view-journeys-event}

Die Berechtigung **[!UICONTROL Journey-Ereignisse, Datenquellen und Aktionen anzeigen]** auf hoher Ebene ermöglicht Benutzern die Verwendung von Ereignissen und Daten im Journey-Flow.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * Journey_events.read
   * Journey_data_sources.read
   * Journey_actions.read

* Adobe Experience Platform-spezifisch:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Berechtigung für Journey-Bericht anzeigen {#view-journeys-report}

Mit der Berechtigung **[!UICONTROL Journey anzeigen]** auf hoher Ebene können Benutzer einen schreibgeschützten Journey-Bericht erstellen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * Journey_report.read
   * messages_report.read

* Adobe Experience Platform-spezifisch:
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## Nachrichtenfunktion {#message-capability}

### Berechtigung für Nachrichten verwalten {#manage-messages}

Mit der Berechtigung **[!UICONTROL Nachrichten verwalten]** auf hoher Ebene können Benutzer Nachrichten erstellen und bearbeiten/löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform-spezifisch:
   * segments.read
   * schemas.read

### Berechtigung für Vorschau und Testen von Nachrichten verwalten {#mange-messages-preview}

Die Berechtigung **[!UICONTROL Vorschau und Test von Nachrichten verwalten]** auf hoher Ebene ermöglicht Benutzern die Vorschau von personalisierten Nachrichten.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Adobe Experience Platform-spezifisch:
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### Berechtigung zum Veröffentlichen von Nachrichten {#publish-messages}

Mit der Berechtigung **[!UICONTROL Nachrichten veröffentlichen]** auf hoher Ebene können Benutzer Nachrichten veröffentlichen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages.publish

* Adobe Experience Platform-spezifisch:
   * profiles.read
   * schemas.read
   * datasets.read

### Berechtigung für Nachrichten anzeigen {#view-messages}

Mit der Berechtigung **[!UICONTROL Nachrichten anzeigen]** auf hoher Ebene können Benutzer nur Nachrichten lesen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages.read
   * messages_presets.read

* Adobe Experience Platform-spezifisch:
   * schemas.read
   * segments.read

### Berechtigung für Nachrichtenbericht anzeigen {#view-message-reports}

Mit der allgemeinen Berechtigung **[!UICONTROL Bericht &quot;Nachrichten anzeigen]**&quot;können Benutzer schreibgeschützte E-Mail- und Push-Berichte erstellen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Entscheidungsverwaltungsfunktion {#decisions-permissions}

### Entscheidungsberechtigungen verwalten {#manage-decisioning}

Die Berechtigung **[!UICONTROL Entscheidungen verwalten]** auf hoher Ebene ermöglicht Benutzern das Erstellen neuer und Bearbeiten/Löschen vorhandener **[!UICONTROL Aktivitätsentitäten]** sowie das Verwalten der Objekte, die in diesen Aktivitäten verwendet werden, um die Entscheidungen zu treffen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisches Entscheidungsmanagement:
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

* Adobe Experience Platform-spezifisch:
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### Entscheidungsberechtigungen anzeigen {#view-decisions}

Mit der Berechtigung **[!UICONTROL Entscheidungen anzeigen]** auf hoher Ebene können Benutzer eine vorhandene Aktivität und zugehörige Geschäftsobjekte verwenden, um Entscheidungen zu treffen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisches Entscheidungsmanagement:
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Adobe Experience Platform-spezifisch:
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### Entscheidungsberechtigung für Veröffentlichungen von Angeboten {#publish-decisions}

Die Berechtigung **[!UICONTROL Angebote veröffentlichen]** auf hoher Ebene ermöglicht Benutzern den Zugriff auf die Aktivitäten, die Angebote genehmigen/nicht genehmigen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisches Entscheidungsmanagement:
   * offer_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform-spezifisch:
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### Berechtigung für Rangstrategien verwalten {#manage-decisions}

Mit der Berechtigung **[!UICONTROL Ranking-Strategien verwalten]** auf hoher Ebene können Benutzer benutzerdefinierte Nachrichtenberichte lesen, erstellen, bearbeiten und löschen sowie Aktionsfunktionen verwenden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisches Entscheidungsmanagement:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Verwaltungsfunktionen {#administration-permissions}

### Berechtigung für die Zuweisung von Subdomains verwalten {#manage-subdomain}

Mit der Berechtigung **[!UICONTROL Zuweisung von Subdomains verwalten]** auf hoher Ebene können Benutzer die Zuweisung von Subdomains erstellen, bearbeiten und löschen (einschließlich IP-Pool).

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### Berechtigung für PTR-Datensätze anzeigen {#view-ptr}

Die Berechtigung **[!UICONTROL PTR-Datensätze anzeigen]** auf hoher Ebene ermöglicht Benutzern das Anzeigen von PTR-Datensätzen, die basierend auf der Subdomain konfiguriert wurden, und umfasst die folgenden Berechtigungen auf niedriger Ebene:

* PTR_records.read
* subdomains_delegation.read

### Berechtigung für IP-Pools verwalten {#manage-ip-pools}

Mit der Berechtigung **[!UICONTROL IP-Pools verwalten]** auf hoher Ebene können Benutzer eine Affinitätsdefinition erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Berechtigung für allgemeine Einstellungen für Nachrichten verwalten {#manage-message-settings}

Mit der Berechtigung **[!UICONTROL Allgemeine Einstellungen für Nachrichten verwalten]** auf hoher Ebene können Benutzer globale Einstellungen auf Sandbox-Ebene erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete

* Adobe Experience Platform-spezifisch:
   * schemas.read

### Berechtigung für allgemeine Einstellungen für Nachrichten anzeigen {#view-message-settings}

Die allgemeine Berechtigung **[!UICONTROL Anzeigen von Nachrichten]** auf hoher Ebene ermöglicht Benutzern das Anzeigen von allgemeinen Nachrichteneinstellungen wie Unterdrückungsregeln oder Ausführungsadressen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages_general_settings.read
* Adobe Experience Platform-spezifisch:
   * schemas.read

### Berechtigung für Nachrichtenvorgaben verwalten {#manage-message-presets}

Die Berechtigung **[!UICONTROL Nachrichten verwalten]** auf hoher Ebene ermöglicht Benutzern das Erstellen, Bearbeiten und Löschen von Nachrichtenvorgaben über Kanäle hinweg auf Sandbox-Ebene.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (aus Adobe Experience Platform Launch)

### Berechtigung für Nachrichtenvorgaben anzeigen {#view-message-presets}

Mit der Berechtigung **[!UICONTROL Nachrichtenvorgaben anzeigen]** auf hoher Ebene können Benutzer Nachrichtenvorgaben anzeigen, um zu erfahren, welche Nachrichtenvorgaben beim Erstellen einer Nachricht verwendet werden sollen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (aus Adobe Experience Platform Launch)

### Berechtigung für Unterdrückungsregeln verwalten {#manage-suppression-rules}

Mit der Berechtigung **[!UICONTROL Unterdrückungsregeln verwalten]** auf hoher Ebene können Benutzer die Anzahl der Bounces definieren, bevor die E-Mail-Adresse des Benutzers zur Unterdrückungsliste hinzugefügt wird.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete

### Berechtigung für Unterdrückungsliste anzeigen {#view-suppresion-list}

Die Berechtigung **[!UICONTROL Unterdrückungsliste anzeigen]** auf hoher Ebene ermöglicht Benutzern das Anzeigen von Nachrichtenkonfigurationen, einschließlich Nachrichtenvorgaben und allgemeinen Nachrichteneinstellungen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Journey Optimizer-spezifisch:
   * suppression_list.view
* Adobe Experience Platform-spezifisch:
   * profiles.read
   * datasets.read

### Berechtigung zur Export-Unterdrückungsliste {#export-suppression-list}

Die Berechtigung **[!UICONTROL Export-Unterdrückungsliste]** auf hoher Ebene ermöglicht Benutzern die Konfiguration von Nachrichtenkonfigurationen, einschließlich Nachrichtenvorgaben und allgemeinen Nachrichteneinstellungen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Adobe Experience Platform-spezifisch:
   * profiles.read
   * datasets.read
