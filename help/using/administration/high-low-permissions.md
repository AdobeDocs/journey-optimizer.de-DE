---
solution: Journey Optimizer
product: journey optimizer
title: Berechtigungsebenen
description: Erfahren Sie mehr zu Berechtigungen auf hoher und niedriger Ebene, mit denen Benutzende auf die verschiedenen Funktionen zugreifen können.
topic: Administration
feature: Access Management
role: Admin, Developer
level: Experienced
keywords: Berechtigung, hohe Ebene, niedrige Ebene, Profil, Admin Console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 100%

---

# Berechtigungsebenen {#high-low-permissions}


Jede Rolle besteht aus Berechtigungen, die Benutzenden den Zugriff auf die verschiedenen Funktionen ermöglichen.

Sie können in zwei Typen unterteilt werden:

* **Berechtigung auf hoher Ebene**: stellt die verschiedenen Berechtigungen dar, die **[!UICONTROL Rolle]** zugewiesen werden können, wie **[!DNL Publish journeys]** und **[!DNL Manage subdomains delegation]**. Berechtigungen auf hoher Ebene beinhalten Berechtigungen auf niedriger Ebene. Berechtigungen auf hoher Ebene werden auf [dieser Seite](ootb-permissions.md) genauer beschrieben.

* **Berechtigungen auf niedriger Ebene**: beinhalten die verschiedenen Berechtigungen, die von der Berechtigung auf hoher Ebene stammen.

Der Rolle **[!DNL Journey administrator]** ist zum Beispiel die Berechtigung **[!DNL Manage journeys]** zugewiesen. Aus dieser Berechtigung stammen die Berechtigungen auf niedriger Ebene, die es Journey-Admins ermöglichen, Journeys zu schreiben, zu lesen und zu löschen.

![](assets/do-not-localize/permissions.png){width="70%"}


## Journey-Ressource {#journey-capability}

* Die Berechtigung **[!DNL Manage journeys]** auf hoher Ebene ermöglicht es Benutzenden, neue Journeys zu erstellen und bestehende Journeys zu bearbeiten/löschen/stoppen bzw. anzuhalten sowie auf die Objekte zuzugreifen, die zur Erstellung des Journey-Flusses in der Journey-Arbeitsfläche verwendet werden.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

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

  +++

* Mit der Berechtigung **[!DNL Publish journeys]** auf hoher Ebene können Benutzende Journeys veröffentlichen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  
   * Spezifisch für Journey Optimizer:
      * journeys.publish
      * journeys.read

  +++

* Mit der Berechtigung **[!DNL View journeys]** auf hoher Ebene können Benutzende Journeys durchsuchen und anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * journeys.read

   * Spezifisch für Adobe Experience Platform:
      * segments.read
      * profiles.read

  +++

* Mit der Berechtigung **[!DNL Manage journeys events, data sources and actions]** auf hoher Ebene können Benutzende Ereignis- und Datenkonfigurationen durchführen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

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

  +++

* Die Berechtigung **[!DNL View journeys events, data sources and actions]** auf hoher Ebene erlaubt es Benutzenden, Ereignisse und Daten im Journey-Fluss zu verwenden.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * journeys_events.read
      * journeys_data_sources.read
      * journeys_actions.read

   * Spezifisch für Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

  +++

* Mit der Berechtigung **[!DNL View journeys report]** auf hoher Ebene können Benutzende auf schreibgeschützte Journey-Berichte zugreifen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * journeys_report.read
      * messages_report.read

   * Spezifisch für Adobe Experience Platform:
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++

## Journey Optimizer-Regelressource {#journey-rules-capability}

* Mit der Berechtigung **[!DNL Manage frequency rules]** auf hoher Ebene können Benutzende Häufigkeitsregeln lesen, erstellen, bearbeiten, löschen und aktivieren/deaktivieren.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

  +++

* Mit der Berechtigung **[!DNL View frequency rules]** auf hoher Ebene können Benutzende Häufigkeitsregeln anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * frequency_rules.read

  +++

## Kampagnenressource {#campaign-capability}

* Mit der Berechtigung **[!DNL Export suppression list]** auf hoher Ebene können Benutzende die Unterdrückungsliste als CSV-Datei herunterladen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:
      * suppression_list.export

   * Spezifisch für Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

* Mit der Berechtigung **[!DNL Manage campaigns]** auf hoher Ebene können Benutzende Kampagnen erstellen und bearbeiten/löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

  +++

* Mit der Berechtigung **[!DNL Publish campaigns]** auf hoher Ebene können Benutzende Kampagnen veröffentlichen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

  +++

* Mit der Berechtigung **[!DNL View campaigns report]** auf hoher Ebene können Benutzende Kampagnenberichte lesen und bearbeiten.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

  +++

## Entscheidungs-Management-Ressource {#decisions-permissions}

* Mit der Berechtigung **[!DNL Manage decisions]** auf hoher Ebene können Benutzende neue **[!DNL Activity entities]** erstellen und solche vorhandenen Aktivitäten bearbeiten/löschen sowie Objekte verwalten, die in diesen Aktivitäten zur Entscheidungsfindung verwendet werden.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

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

  +++

* Mit der Berechtigung **[!DNL View decisions]** auf hoher Ebene können Benutzende eine vorhandene Aktivität und zugehörige Geschäftsobjekte verwenden, um Entscheidungen zu treffen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für das Entscheidungs-Management:
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Spezifisch für Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read

  +++

* Mit der Berechtigung **[!DNL Manage offers]** auf hoher Ebene können Benutzende alle Angebote, Komponenten, Leseentscheidungen und Sammlungen erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

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

  +++

* Mit der Berechtigung **[!DNL Manage ranking strategies]** auf hoher Ebene können Benutzende Rangfolgestrategien lesen, erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für das Entscheidungs-Management:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

  +++

## Kanalkonfigurationsressource {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ This permission includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* Mit der Berechtigung **[!DNL Manage file routing]** auf hoher Ebene können Benutzende Datei-Routing-Konfigurationen erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  
   * Spezifisch für Journey Optimizer:

      * file_routing.read
      * file_routing.write
      * file_routing.delete

  +++

* Mit der Berechtigung **[!DNL Manage IP pools]** auf hoher Ebene können Benutzende eine Affinitätsdefinition erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  
   * Spezifisch für Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

  +++

* Mit der Berechtigung **[!DNL Manage landing page settings]** auf hoher Ebene können Benutzende Landingpage-Subdomains und Voreinstellungen lesen, erstellen und bearbeiten.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

  +++

* Mit der Berechtigung **[!DNL Manage messages general settings]** auf hoher Ebene können Benutzende globale Einstellungen auf Sandbox-Ebene erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Spezifisch für Adobe Experience Platform:
      * schemas.read

  +++

* Mit der Berechtigung **[!DNL Manage messages presets]** auf hoher Ebene können Benutzende Kanalkonfigurationen kanalübergreifend auf Sandbox-Ebene erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * Spezifisch für die Datenerfassung:
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

  +++

* Mit der Berechtigung **[!DNL Manage PTR records]** auf hoher Ebene können Benutzende basierend auf der Subdomain konfigurierte PTR-Einträge lesen und bearbeiten.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

  +++

* Die Berechtigung **[!DNL Manage Seedlist]** auf hoher Ebene erlaubt Benutzenden das Lesen, Erstellen, Bearbeiten und Löschen von Testadressenlisten.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:
      * seedlist.read
      * seedlist.write
      * seedlist.delete

  +++

* Mit der Berechtigung **[!DNL Manage SMS subdomains]** auf hoher Ebene können Benutzende SMS-Subdomains lesen, erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

  +++

* Mit der Berechtigung **[!DNL Manage subdomains delegations]** auf hoher Ebene können Benutzende Delegierungen von Subdomains (einschließlich IP-Pool) erstellen, bearbeiten und löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  
   * Spezifisch für Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

  +++

* Mit der Berechtigung **[!DNL Manage suppression]** auf hoher Ebene können Benutzende definieren, wie viele Bounces auftreten können, bevor eine E-Mail-Adresse zur Unterdrückungsliste hinzugefügt wird, sowie Einträge zur Unterdrückungsliste hinzufügen und aus ihr löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  
   * Spezifisch für Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

  +++

* Mit der Berechtigung **[!DNL View file routing]** auf hoher Ebene können Benutzende Datei-Routing-Konfigurationen anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  
   * Spezifisch für Journey Optimizer:

      * file_routing.read

  +++

* Mit der Berechtigung **[!DNL View messages general settings]** auf hoher Ebene können Benutzende allgemeine Nachrichteneinstellungen wie Ausführungsadressen anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:
      * messages_general_settings.read

   * Spezifisch für Adobe Experience Platform:
      * schemas.read

  +++

* Mit der Berechtigung **[!DNL View messages presets]** auf hoher Ebene können Benutzende Nachrichtenvoreinstellungen anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 

   * Spezifisch für Journey Optimizer:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * Spezifisch für die Datenerfassung:
      * Mobile_setting.read

  +++

* Mit der Berechtigung **[!DNL View PTR records]** auf hoher Ebene können Benutzende basierend auf der Subdomain konfigurierte PTR-Einträge anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene: 
   * Spezifisch für Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

  +++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ This permission includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* Mit der Berechtigung **[!DNL View suppression list]** auf hoher Ebene können Benutzende den Inhalt und die Einstellungen der Unterdrückungsliste anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * suppression_list.view

   * Spezifisch für Adobe Experience Platform:
      * profiles.read
      * datasets.read

  +++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ This permission includes the following low-level permissions: 
-->

## KI-Assistent-Ressource {#ai-permissions}

* Die Berechtigung auf hoher Ebene **[!DNL Generate content]** ermöglicht Benutzenden den Zugriff auf den KI-Assistenten in Journey Optimizer.

  +++ Er umfasst die folgende Berechtigung auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:
      * ai-assistant-generated-content.generate

  +++

## Ressource für orchestrierte Kampagnen {#ai-orchestrated-campaign}

* Mit der Berechtigung **[!DNL Manage orchestrated campaigns]** auf hoher Ebene können Benutzende Kampagnen erstellen und orchestrierte Kampagnen bearbeiten/löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:

      * orchestrated_campaigns.read
      * orchestrated_campaigns.write
      * orchestrated_campaigns.delete
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.write
      * cjm-message.delete
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * cjm-message-preview-test.write
      * experiment.read
      * experiment.write
      * experiment.delete

   * Spezifisch für Adobe Experience Platform:

      * identity-graph.read
      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read
      * sandboxes.view

  +++

* Mit der Berechtigung **[!DNL Manage orchestrated campaigns admin]** auf hoher Ebene können Benutzende neue Links und Abstimmungen zwischen Adobe Experience Platform-Profilen und Entitäten des relationalen Speichers erstellen und bearbeiten/löschen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read
      * cjm-orchestrated-campaign-admin.write
      * cjm-orchestrated-campaign-admin.delete

  +++

* Mit der Berechtigung **[!DNL Publish orchestrated campaigns]** auf hoher Ebene können Benutzende orchestrierte Kampagnen veröffentlichen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-orchestrated-campaign.publish
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.publish
      * cjm-library-item.read

   * Spezifisch für Adobe Experience Platform:

      * sandboxes.view

  +++

* Mit der Berechtigung **[!DNL View orchestrated campaigns]** auf hoher Ebene können Benutzende orchestrierte Kampagnen und deren Inhalte anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:

      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * experiment.read

   * Spezifisch für Adobe Experience Platform:

      * sandboxes.view
      * segments.read
      * profiles.read

  +++

* Mit der Berechtigung **[!DNL View orchestrated campaigns admin]** auf hoher Ebene können Benutzende die Admin-Einstellungen anzeigen, aber keine Einstellungen bearbeiten.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:

      * cjm-orchestrated-campaign-admin.read

  +++

* Mit der Berechtigung **[!DNL View orchestrated campaigns report]** auf hoher Ebene können Benutzende die Leistung der orchestrierten Kampagnen sowohl im Live- als auch im Geschäftsbericht anzeigen.

  +++ Diese Berechtigung beinhaltet die folgenden Berechtigungen auf niedriger Ebene:  

   * Spezifisch für Journey Optimizer:

      * cjm-orchestrated-campaign-reports.read
      * cjm-message-report.read
      * cjm-channel-report.read
      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * experiment.read
      * experiment-report.read

   * Spezifisch für Adobe Experience Platform:

      * sandboxes.view
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

  +++
