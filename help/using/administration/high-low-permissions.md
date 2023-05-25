---
solution: Journey Optimizer
product: journey optimizer
title: Berechtigungsebenen
description: Erfahren Sie mehr über Berechtigungen auf hoher und niedriger Ebene. Dadurch wird Benutzenden der Zugriff auf die verschiedenen Funktionen ermöglicht.
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: Berechtigung, hohe Ebene, niedrige Ebene, Profil, Admin Console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 7ac2ae714f2d11d2559b6195af37e2dece35b17c
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 54%

---

# Berechtigungsebenen {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

Jede Rolle besteht aus Berechtigungen, die Benutzern den Zugriff auf die verschiedenen Funktionen ermöglichen.
Sie können in zwei Typen unterteilt werden:

* **Berechtigung auf hoher Ebene**: stellt die verschiedenen Berechtigungen dar, die zugewiesen werden können **[!UICONTROL Rolle]** im [!DNL Admin console], z. B. **[!DNL Publish journeys]** und **[!DNL Manage subdomains delegation]**. Berechtigungen auf hoher Ebene beinhalten Berechtigungen auf niedriger Ebene.

* **Berechtigung auf niedriger Ebene**: beinhalten die verschiedenen Berechtigungen, die von der Berechtigung auf hoher Ebene stammen.

Beispiel: die **[!DNL Journey administrator]** Rolle zugewiesen wird, wird die **[!DNL Manage journeys]** Berechtigung. Aus dieser Berechtigung stammen die Berechtigungen auf niedriger Ebene, die es dem Journey-Administrator ermöglichen, Journeys zu schreiben, zu lesen und zu löschen.

## Journey-Ressource {#journey-capability}

* **[!DNL Manage journeys]** Die Berechtigung auf hoher Ebene ermöglicht es Benutzern, neue Journey zu erstellen und bestehende zu bearbeiten/zu löschen sowie auf die Objekte zuzugreifen, die in der Journey-Arbeitsfläche zum Erstellen des Journey-Flusses verwendet werden.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

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

* **[!DNL Publish journeys]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, Journey zu veröffentlichen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:
   * Spezifisch für Journey Optimizer:
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** -Berechtigung auf hoher Ebene ermöglicht Benutzern das Durchsuchen und Anzeigen von Journey.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * journeys.read
   * Spezifisch für Adobe Experience Platform:
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** Mit Berechtigungen auf hoher Ebene können Benutzer Ereignis- und Datenkonfigurationen konfigurieren.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

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

* **[!DNL View journeys events, data sources and actions]** -Berechtigung auf hoher Ebene ermöglicht Benutzern die Verwendung von Ereignissen und Daten im Journey-Fluss.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * journeys_events.read
      * journeys_data_sources.read
      * journeys_actions.read
   * Spezifisch für Adobe Experience Platform:
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, schreibgeschützten Journey-Bericht zu erstellen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

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

* **[!DNL Manage frequency rules]** Mit Berechtigungen auf hoher Ebene können Benutzer Frequenzregeln lesen, erstellen, bearbeiten, löschen und aktivieren/deaktivieren.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** Mit Berechtigungen auf hoher Ebene können Benutzer Frequenzregeln anzeigen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * frequency_rules.read

+++

## Kampagnenressource {#campaign-capability}

* **[!DNL Manage campaigns]** Berechtigung auf hoher Ebene ermöglicht Benutzern das Erstellen neuer und Bearbeiten/Löschen von Kampagnen

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:

      * campaign.read
      * campaign.write
      * campaign.delete

      <!--* experiments.read
      * experiments.write
      * experiments.delete-->
+++

* **[!DNL Publish campaigns]** Mit allgemeinen Berechtigungen können Benutzer Kampagnen veröffentlichen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:

      * campaign-read
      * campaign-publish
         <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** Mit allgemeinen Berechtigungen können Benutzer Kampagnenberichte lesen und bearbeiten.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * campaign.read
      * campaign-report.read

      <!--* experiments.read
      * experiments_report.read-->
+++

## Entscheidungsmanagement-Ressource {#decisions-permissions}

* **[!DNL Manage decisions]** Berechtigung auf hoher Ebene ermöglicht Benutzern das Erstellen neuer und Bearbeiten/Löschen vorhandener **[!DNL Activity entities]** und verwalten die Objekte, die in diesen Aktivitäten für die Entscheidungsfindung verwendet werden.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

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

* **[!DNL View decisions]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, eine vorhandene Aktivität und verwandte Geschäftsobjekte zu verwenden, um Entscheidungen zu treffen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

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

+++

* **[!DNL Manage offers]** Mit der Berechtigung auf hoher Ebene können Benutzer alle Angebote, Komponenten, Leseentscheidungen und Sammlungen erstellen, bearbeiten und löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für das Entscheidungs-Management:
      * offers_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read
   * Spezifisch für Adobe Experience Platform:
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]** Mit allgemeinen Berechtigungen können Benutzer Rangstrategien lesen, erstellen, bearbeiten und löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für das Entscheidungs-Management:
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## Kanalkonfigurationsressource {#administration-permissions}

* **[!DNL Manage subdomains delegation]** Mit einer allgemeinen Berechtigung können Benutzer Subdomain-Delegationen erstellen, bearbeiten und löschen (einschließlich IP-Pool).

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:
   * Spezifisch für Journey Optimizer:

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage PTR records]** Mit allgemeinen Berechtigungen können Benutzer PTR-Einträge lesen und bearbeiten, die basierend auf der Subdomain konfiguriert wurden.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL View PTR records]** Mit einer allgemeinen Berechtigung können Benutzer PTR-Datensätze anzeigen, die basierend auf der Subdomain konfiguriert wurden.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:
   * Spezifisch für Journey Optimizer:

      * PTR_records.read
      * subdomains_delegation.read

+++

* **[!DNL Manage IP pools]** Mit Berechtigung auf hoher Ebene können Benutzer die Affinitätsdefinition erstellen, bearbeiten und löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:
   * Spezifisch für Journey Optimizer:
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage messages general settings]** Mit Berechtigungen auf hoher Ebene können Benutzer globale Einstellungen auf Sandbox-Ebene erstellen, bearbeiten und löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete
   * Spezifisch für Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL View messages general settings]** -Berechtigung auf hoher Ebene ermöglicht Benutzern, allgemeine Einstellungen für Nachrichten wie die Ausführungsadresse anzuzeigen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * messages_general_settings.read
   * Spezifisch für Adobe Experience Platform:
      * schemas.read

+++

* **[!DNL Manage channel surface]** Mit Berechtigung auf hoher Ebene können Benutzer Kanaloberflächen auf Kanalebene auf Sandbox-Ebene erstellen, bearbeiten und löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
      * mobile_setting.read (aus Adobe Experience Platform Launch)

+++

<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->

* **[!DNL Manage suppression]** Mit einer allgemeinen Berechtigung können Benutzer die Anzahl der Bounces definieren, bevor eine E-Mail-Adresse zur Unterdrückungsliste hinzugefügt wird, sowie Einträge zur Unterdrückungsliste hinzufügen und daraus löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:
   * Spezifisch für Journey Optimizer:
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View suppression list]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, den Inhalt und die Einstellungen der Unterdrückungsliste anzuzeigen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * suppression_list.view
   * Spezifisch für Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Export suppression list]** -Berechtigung auf hoher Ebene ermöglicht es Benutzern, die Unterdrückungsliste als CSV-Datei herunterzuladen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * suppression_list.export
   * Spezifisch für Adobe Experience Platform:
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage landing page settings]** Mit allgemeinen Berechtigungen können Benutzer Landingpage-Subdomains und Vorgabeneinstellungen lesen, erstellen und bearbeiten.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

* **[!DNL Manage messages presets]** Mit allgemeinen Berechtigungen können Benutzer Inhalte-Branding lesen, erstellen, bearbeiten und löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
   * Datenerfassungsspezifisch:
      * Mobile_setting.read

+++

* **[!DNL View messages presets]** Berechtigung auf hoher Ebene ermöglicht Benutzern das Anzeigen von Nachrichtenvorgaben.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read
   * Datenerfassungsspezifisch:
      * Mobile_setting.read

+++

* **[!DNL Manage SMS subdomains]** Mit einer allgemeinen Berechtigung können Benutzer SMS-Subdomains lesen, erstellen, bearbeiten und löschen.

+++ Sie umfasst die folgenden Berechtigungen auf niedriger Ebene:

   * Spezifisch für Journey Optimizer:
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete
+++
