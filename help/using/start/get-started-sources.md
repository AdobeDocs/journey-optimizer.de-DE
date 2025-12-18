---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Quellen-Connectoren in Journey Optimizer
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Daten aus externen Quellen aufnehmen.
feature: Integrations, Data Ingestion
role: User
level: Beginner
exl-id: 359ea3c6-7746-469e-8a24-624f9726f2d8
source-git-commit: 7864012ad148c2e52bc38598016e7bd7fac9644e
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 11%

---

# Erste Schritte mit Quell-Connectoren {#sources-gs}

## Was ist eine -Quelle? {#what-is-source}

Eine **Quelle** ist ein Connector, der externe Daten in Adobe Journey Optimizer einbringt. Mit -Quellen können Sie Kundeninformationen aus Systemen importieren, die Sie bereits verwenden, z. B. CRM-Plattformen, Cloud-Speicher oder Datenbanken, und diese Daten für die Erstellung personalisierter Kunden-Journey zur Verfügung stellen.

Stellen Sie sich Quellen als Brücken zwischen Journey Optimizer und Ihren externen Datensystemen vor. Sie synchronisieren automatisch Daten, damit Sie immer über aktuelle Kundeninformationen verfügen, um Ihre Marketing-Kampagnen zu unterstützen.

## Warum Quellen wichtig sind {#why-sources-matter}

-Quellen sind für die Erstellung personalisierter, datengesteuerter Kundenerlebnisse in Journey Optimizer unerlässlich. Und zwar aus folgenden Gründen:

* **Einheitliche Kundenansicht** - Kombinieren Sie Daten aus mehreren Systemen, um das vollständige Bild jedes Kunden zu sehen
* **Echtzeit-Personalisierung** - Verwenden Sie neue Daten, um zeitnahe, relevante Nachrichten in Ihren Journey zu senden.
* **Automatisierte Datensynchronisation** - Halten Sie Kundeninformationen ohne manuelle Datenimporte auf dem neuesten Stand.
* **Effiziente Workflows** - Einmal verbinden und dann automatisch Daten in Ihre Journey fließen lassen

Beispielsweise können Sie mithilfe von Quellen den Kaufverlauf aus Ihrer E-Commerce-Plattform importieren und dann Journey erstellen, die basierend auf den Käufen personalisierte Produktempfehlungen senden.

## Was Sie mit Quellen tun können {#sources-use-cases}

Häufige Anwendungsfälle für Quellen in Journey Optimizer sind:

* **Kundendaten aus CRM-Systemen importieren** - Synchronisieren von Kontaktinformationen, Voreinstellungen und Interaktionsverlauf von Plattformen wie Salesforce oder Microsoft Dynamics
* **Kaufdaten verbinden** - Binden Sie den Auftragsverlauf und die Produktvoreinstellungen von E-Commerce-Plattformen ein, um Angebote zu personalisieren
* **Treueprogramm-Daten integrieren** - Zugreifen auf Punktestände und Stufeninformationen, um Ihre aktivsten Kunden zu belohnen
* **Verhaltensdaten synchronisieren** - Importieren von Website-Interaktionen und App-Nutzungsmustern in Trigger-relevante Journey
* **Aktualisieren von Profilattributen** - Halten Sie Kundenprofile mit Daten aus dem Cloud-Speicher oder Datenbanken auf dem neuesten Stand.

## Allgemeine Quelltypen {#source-types}

Journey Optimizer unterstützt verschiedene Quelltypen für die Verbindung mit Ihren bestehenden Systemen:

**Adobe-Programme:**
* Adobe Analytics
* Adobe Audience Manager
* Adobe Campaign
* Adobe Commerce

**Cloud-Speicher:**
* Amazon S3
* Azur Blob Storage
* Google Cloud Storage
* SFTP

**Datenbanken:**
* Amazon Redshift
* Google BigQuery
* Microsoft SQL Server
* MySQL
* PostgreSQL

**CRM und Marketing-Automatisierung:**
* Microsoft Dynamics
* Salesforce
* Salesforce Marketing Cloud

➡️ Die vollständige Liste finden Sie im [Experience Platform-Quellkatalog](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"}

## Voraussetzungen {#prerequisites}

Stellen Sie vor dem Konfigurieren von Quellen Folgendes sicher:

* **Entsprechende Berechtigungen** - Zugriff auf die Verwaltung von Quellen in Adobe Experience Platform
* **Source-Systemanmeldeinformationen** - Authentifizierungsdetails für das externe System, das Sie verbinden möchten
* **Verständnis Ihrer Daten** - Erfahren Sie, welche Datenfelder Sie benötigen und wie sie Journey Optimizer-Profilen zugeordnet sind

➡️ Informationen zu [Zugriffssteuerung und Berechtigungen](../administration/permissions.md)

## Funktionsweise von Quellen {#how-sources-work}

Adobe Journey Optimizer verwendet das Quellen-Framework von Adobe Experience Platform. Im Folgenden finden Sie den grundlegenden Workflow:

1. **Connect** - Einrichten der Authentifizierung für Ihr externes Datensystem
2. **Daten auswählen** - Wählen Sie aus, welche Daten importiert werden sollen und wie oft die Synchronisierung erfolgen soll.
3. **Felder zuordnen** - Definieren, wie externe Datenfelder den Journey Optimizer-Profilattributen entsprechen
4. **Zeitplan** - Einrichten automatischer Datenaktualisierungsintervalle
5. **Überwachen** - Verfolgen des Datenflusses und Beheben von Synchronisierungsproblemen

Nach der Konfiguration werden Quellen automatisch im Hintergrund ausgeführt, sodass Ihre Kundendaten aktuell und für die Verwendung in Journey bereit sind.

## Weitere Informationen {#learn-more}

![](assets/sources-home.png)

In diesem Video erfahren Sie mehr über Quell-Connectoren und deren Konfiguration in Journey Optimizer:

>[!VIDEO](https://video.tv.adobe.com/v/335919?quality=12)

Detaillierte Informationen zum Konfigurieren und Verwalten von Quellen finden Sie in der [Dokumentation zu Adobe Experience Platform-Quellen](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=de){target="_blank"}.

## Nächste Schritte {#next-steps}

Jetzt, da Sie verstehen, was Quellen sind und warum sie wichtig sind:

* Suchen Sie im [Quellkatalog](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html#sources-catalog){target="_blank"} nach Connectoren für Ihre Systeme
* Erfahren Sie, wie [ eine Quellverbindung erstellen](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/overview.html){target="_blank"}
* Verstehen von [Datenzuordnung und -umwandlung](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/overview.html){target="_blank"}
* Siehe „Verwenden [ importierten Daten in Journey&quot;](../building-journeys/journey-gs.md)
