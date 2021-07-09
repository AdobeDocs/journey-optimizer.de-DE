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
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Kontrollgruppen
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: ht
source-wordcount: '1171'
ht-degree: 100%

---

# Berechtigungsebenen {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

Jedes Produktprofil besteht aus Berechtigungen, die Benutzern den Zugriff auf die verschiedenen Funktionen ermöglichen.
Sie können in zwei Typen unterteilt werden:

* **Berechtigung auf hoher Ebene**: beinhalten die verschiedenen Berechtigungen, die **[!UICONTROL Produktprofilen]** in [!DNL Admin console] zugewiesen werden können, z. B. **[!UICONTROL Veröffentlichen von Journeys]** und **[!UICONTROL Verwalten der Subdomain-Zuweisung]**. Berechtigungen auf hoher Ebene beinhalten Berechtigungen auf niedriger Ebene.

* **Berechtigung auf niedriger Ebene**: beinhalten die verschiedenen Berechtigungen, die von der Berechtigung auf hoher Ebene stammen.

Beispielsweise wird dem Produktprofil **[!UICONTROL Journey-Administrator]** die Berechtigung **[!UICONTROL Journey verwalten]** zugewiesen. Aus dieser Berechtigung stammen die Berechtigungen auf niedriger Ebene, die es dem Journey-Administrator ermöglichen, Journeys zu schreiben, zu lesen und zu löschen.

## Journey-Funktion {#journey-capability}

### Berechtigung zum Verwalten von Journeys {#manage-journeys}

Die Berechtigung **[!UICONTROL Journeys verwalten]** auf hoher Ebene ermöglicht Benutzern das Erstellen neuer und das Bearbeiten/Löschen vorhandener Journeys sowie den Zugriff auf die Objekte, die in der Journey-Arbeitsfläche zum Erstellen des Journey Flow verwendet werden.

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

### Berechtigung zum Veröffentlichen von Journeys {#publish-journeys}

Mit der Berechtigung **[!UICONTROL Journeys veröffentlichen]** auf hoher Ebene können Benutzer Journeys veröffentlichen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys.publish
   * journeys.read

### Berechtigung zum Anzeigen von Journeys {#view-journeys}

Die Berechtigung **[!UICONTROL Journeys anzeigen]** auf hoher Ebene ermöglicht Benutzern das Durchsuchen und Anzeigen von Journeys.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys.read

* Spezifisch für Adobe Experience Platform:
   * segments.read
   * profiles.read

### Berechtigung zur Verwaltung von Journey-Ereignissen, Datenquellen und Aktionen {#manage-journeys-events}

Mit der Berechtigung **[!UICONTROL Journey-Ereignisse, Datenquellen und Aktionen verwalten]** auf hoher Ebene können Benutzer Ereignis- und Datenkonfigurationen vornehmen.

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

### Berechtigung zum Anzeigen von Journey-Ereignissen, Datenquellen und Aktionen {#view-journeys-event}

Die Berechtigung **[!UICONTROL Journey-Ereignisse, Datenquellen und Aktionen anzeigen]** auf hoher Ebene ermöglicht Benutzern die Verwendung von Ereignissen und Daten im Journey Flow.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * datasets.read
   * identity_namespace.read

### Berechtigung zur Ansicht von Journey-Berichten {#view-journeys-report}

Mit der Berechtigung **[!UICONTROL Journey-Bericht anzeigen]** auf hoher Ebene können sich Benutzer einen schreibgeschützten Journey-Bericht ansehen.

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

### Berechtigung zur Verwaltung von Nachrichten {#manage-messages}

Mit der Berechtigung **[!UICONTROL Nachrichten verwalten]** auf hoher Ebene können Benutzer Nachrichten erstellen und bearbeiten/löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Spezifisch für Adobe Experience Platform:
   * segments.read
   * schemas.read

### Berechtigung zum Verwalten der Nachrichtenvorschau und von Tests {#mange-messages-preview}

Die Berechtigung **[!UICONTROL Vorschau und Tests von Nachrichten verwalten]** auf hoher Ebene ermöglicht Benutzern die Vorschau von personalisierten Nachrichten.

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

### Berechtigung zum Veröffentlichen von Nachrichten {#publish-messages}

Mit der Berechtigung **[!UICONTROL Nachrichten veröffentlichen]** auf hoher Ebene können Benutzer Nachrichten veröffentlichen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages.publish

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * schemas.read
   * datasets.read

### Berechtigung zum Anzeigen von Nachrichten {#view-messages}

Mit der Berechtigung **[!UICONTROL Nachrichten anzeigen]** auf hoher Ebene können Benutzer nur Nachrichten lesen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages.read
   * messages_presets.read

* Spezifisch für Adobe Experience Platform:
   * schemas.read
   * segments.read

### Berechtigung zum Anzeigen von Nachrichtenberichten {#view-message-reports}

Mit der Berechtigung **[!UICONTROL Nachrichtenbericht anzeigen]** auf hoher Ebene können Benutzer schreibgeschützte E-Mail- und Push-Berichte lesen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## Entscheidungsverwaltungsfunktion {#decisions-permissions}

### Berechtigung zum Verwalten von Entscheidungen {#manage-decisioning}

Die Berechtigung **[!UICONTROL Entscheidungen verwalten]** auf hoher Ebene ermöglicht Benutzern das Erstellen neuer und das Bearbeiten/Löschen vorhandener **[!UICONTROL Aktivitätsentitäten]** sowie das Verwalten der Objekte, die in diesen Aktivitäten zur Entscheidungsfindung verwendet werden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für die Entscheidungsverwaltung:
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

### Berechtigung zum Anzeigen von Entscheidungen {#view-decisions}

Mit der Berechtigung **[!UICONTROL Entscheidungen anzeigen]** auf hoher Ebene können Benutzer eine vorhandene Aktivität und zugehörige Geschäftsobjekte verwenden, um Entscheidungen zu treffen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für die Entscheidungsverwaltung:
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

### Berechtigung zur Veröffentlichung von Angebotsentscheidungen {#publish-decisions}

Die Berechtigung **[!UICONTROL Angebotsentscheidung veröffentlichen]** auf hoher Ebene ermöglicht es Benutzern, Angebotsaktivitäten zu genehmigen bzw. deren Genehmigung zurückzunehmen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für die Entscheidungsverwaltung:
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

### Berechtigung zur Verwaltung von Rangfolgestrategien {#manage-decisions}

Mit der Berechtigung **[!UICONTROL Ranking-Strategien verwalten]** auf hoher Ebene können Benutzer benutzerdefinierte Nachrichtenberichte lesen, erstellen, bearbeiten und löschen sowie Aktionsfunktionen verwenden.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für die Entscheidungsverwaltung:
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## Verwaltungsfunktionen {#administration-permissions}

### Berechtigung zur Verwaltung von Subdomain-Zuweisungen {#manage-subdomain}

Mit der Berechtigung **[!UICONTROL Zuweisung von Subdomains verwalten]** auf hoher Ebene können Benutzer die Zuweisung von Subdomains erstellen, bearbeiten und löschen (einschließlich IP-Pool).

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* subdomains_delegation.read
* subdomains_delegation.write
* subdomains_delegation.delete

### Berechtigung zum Anzeigen von PTR-Datensätzen {#view-ptr}

Die Berechtigung **[!UICONTROL PTR-Datensätze anzeigen]** auf hoher Ebene ermöglicht Benutzern das Anzeigen von PTR-Datensätzen, die basierend auf der Subdomain konfiguriert wurden, und umfasst die folgenden Berechtigungen auf niedriger Ebene:

* PTR_records.read
* subdomains_delegation.read

### Berechtigung zur Verwaltung von IP-Pools {#manage-ip-pools}

Mit der Berechtigung **[!UICONTROL IP-Pools verwalten]** auf hoher Ebene können Benutzer eine Affinitätsdefinition erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### Berechtigung zur Verwaltung der allgemeinen Einstellungen von Nachrichten {#manage-message-settings}

Mit der Berechtigung **[!UICONTROL Allgemeine Einstellungen von Nachrichten verwalten]** auf hoher Ebene können Benutzer globale Einstellungen auf Sandbox-Ebene erstellen, bearbeiten und löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete

* Spezifisch für Adobe Experience Platform:
   * schemas.read

### Berechtigung zum Anzeigen der allgemeinen Einstellungen von Nachrichten {#view-message-settings}

Die Berechtigung **[!UICONTROL Allgemeine Einstellungen von Nachrichten anzeigen]** auf hoher Ebene ermöglicht Benutzern das Anzeigen von allgemeinen Nachrichteneinstellungen wie Unterdrückungsregeln oder Ausführungsadressen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_general_settings.read
* Spezifisch für Adobe Experience Platform:
   * schemas.read

### Berechtigung zur Verwaltung von Nachrichtenvoreinstellungen {#manage-message-presets}

Die Berechtigung **[!UICONTROL Nachrichtenvorgaben verwalten]** auf hoher Ebene ermöglicht es Benutzern, Nachrichtenvorgaben über Kanäle hinweg auf Sandbox-Ebene zu erstellen, zu bearbeiten und zu löschen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation.read
   * IP_pools.read
   * mobile_setting.read (aus Adobe Experience Platform Launch)

### Berechtigung zur Anzeige von Nachrichtenvoreinstellungen {#view-message-presets}

Mit der Berechtigung **[!UICONTROL Nachrichtenvorgaben anzeigen]** auf hoher Ebene können Benutzer Nachrichtenvorgaben anzeigen, um zu erfahren, welche Nachrichtenvorgaben beim Erstellen einer Nachricht verwendet werden sollen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (aus Adobe Experience Platform Launch)

### Berechtigung zum Verwalten von Unterdrückungsregeln {#manage-suppression-rules}

Mit der Berechtigung **[!UICONTROL Unterdrückungsregeln verwalten]** auf hoher Ebene können Benutzer die Anzahl der Bounces definieren, die auftreten dürfen, bevor die E-Mail-Adresse eines Benutzers zur Unterdrückungsliste hinzugefügt wird.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* suppression_rules.read
* suppression_rules.write
* suppression_rules.delete

### Berechtigung zum Anzeigen der Unterdrückungsliste {#view-suppresion-list}

Die Berechtigung **[!UICONTROL Unterdrückungsliste anzeigen]** auf hoher Ebene ermöglicht Benutzern das Anzeigen von Nachrichtenkonfigurationen, einschließlich Nachrichtenvorgaben und allgemeiner Nachrichteneinstellungen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Journey Optimizer:
   * suppression_list.view
* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * datasets.read

### Berechtigung zum Exportieren der Unterdrückungsliste {#export-suppression-list}

Die Berechtigung **[!UICONTROL Unterdrückungsliste exportieren]** auf hoher Ebene ermöglicht Benutzern das Festlegen von Nachrichtenkonfigurationen, einschließlich Nachrichtenvorgaben und allgemeiner Nachrichteneinstellungen.

Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

* Spezifisch für Adobe Experience Platform:
   * profiles.read
   * datasets.read
