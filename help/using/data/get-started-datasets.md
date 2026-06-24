---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Datensätzen
description: Erfahren Sie, wie Sie Adobe Experience Platform-Datensätze in Adobe Journey Optimizer verwenden
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: Plattform, Data Lake, Erstellen, Lake, Datensätze, Profil
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
TQID: https://experienceleague.adobe.com/VYD0k1jjQB-7iEShgFWKDfaVl5BFvtnxxjSrqBiYThw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 79b0c44fffb4297a9a5675200f086c5de544ec88
workflow-type: tm+mt
source-wordcount: 1326
ht-degree: 78%

---

# Erste Schritte mit Datensätzen {#datasets-gs}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie auf Adobe Experience Platform-Datensätze zugreifen, sie erstellen und steuern können, damit Sie die Daten für Journey, Kampagnen und Berichte in Adobe Journey Optimizer speichern und untersuchen können.

>[!ENDSHADEBOX]

Alle Daten, die in Adobe Experience Platform aufgenommen werden, bleiben als Datensätze im Data Lake erhalten. Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet.

## Leitlinien und Einschränkungen

* Seit dem 1. November 2024 werden Senden- und Öffnen-Ereignisse aus Tracking- und Feedback-[!DNL Journey Optimizer]Datensätzen nicht mehr durch die Streaming-Segmentierung unterstützt. Verwenden Sie stattdessen Geschäftsregeln, um die Frequenzbegrenzung oder die Ermüdungsverwaltung zu implementieren. Weitere Informationen finden Sie in [diesem Abschnitt](../conflict-prioritization/rule-sets.md), eine Erklärung zu Anwendungsfällen für die tägliche Begrenzung finden Sie [hier](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510?profile.language=de){target="_blank"}.

* Ab Februar 2025 wird für systemgenerierte Journey Optimizer-Datensätze ein Time-to-Live-Schutzmechanismus (TTL) eingeführt. [Weitere Informationen](datasets-ttl.md)

* Die Aktivierung eines Datensatzes für Profil hat dauerhafte Auswirkungen auf der Schemaebene. Planen Sie Ihren Schema- und Identitätsentwurf sorgfältig, bevor Sie ihn aktivieren. [Weitere Informationen](#profile-datasets)

## Zugriff auf Datensätze {#access}

Der Arbeitsbereich **Datensätze** in der [!DNL Adobe Journey Optimizer]-Benutzeroberfläche ermöglicht es Ihnen, Daten zu erkunden und Datensätze zu erstellen. Um das Dashboard „Datensätze“ zu öffnen, wählen Sie im linken Navigationsbereich die Option **Datensätze** aus.

![](assets/datasets-home.png)

Wählen Sie die Registerkarte **Durchsuchen**, um die Liste aller für Ihr Unternehmen verfügbaren Datensätze anzuzeigen. Für jeden aufgeführten Datensatz werden Details angezeigt, einschließlich seines Namens, des Schemas, dem der Datensatz entspricht, und des Status der letzten Aufnahmeausführung. Standardmäßig werden nur die Datensätze angezeigt, die Sie aufgenommen haben. Wenn Sie die systemgenerierten Datensätze anzeigen möchten, aktivieren Sie im Filter den Umschalter **Systemdatensätze zeigen**.

![](assets/ajo-system-datasets.png)


Wählen Sie den Namen eines Datensatzes aus, um auf seinen Datensatzaktivitäts-Bildschirm zuzugreifen und Details zum ausgewählten Datensatz anzuzeigen. Die Registerkarte „Aktivität“ enthält ein Diagramm, das die Rate der konsumierten Nachrichten sowie eine Liste erfolgreicher und fehlgeschlagener Batches visuell darstellt.

Um eine Vorschau eines Datensatzes anzuzeigen, wählen Sie die Option **Datensatz in der Vorschau ansehen** in der rechten oberen Ecke Ihres Bildschirms aus, um die Vorschau des letzten erfolgreichen Batches in diesem Datensatz anzuzeigen. Wenn ein Datensatz leer ist, ist der Vorschau-Link nicht aktiv.

![](assets/dataset-preview.png)

## Systemdatensätze in [!DNL Journey Optimizer] {#system-datasets}

In diesem Abschnitt werden die von [!DNL Journey Optimizer] verwendeten Systemdatensätze aufgelistet. Die vollständige Liste der Felder und Attribute für jedes Schema finden Sie im [Journey Optimizer-Schemawörterbuch](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de){target="_blank"}.

>[!CAUTION]
>
> Systemdatensätze **dürfen nicht geändert werden**. Jede Änderung wird bei jeder Produktaktualisierung automatisch rückgängig gemacht.

* Berichterstellung

   * _Reporting – Datensatz mit Nachrichten-Feedback-Ereignissen_: Versand-Logs der Nachrichten. Informationen über den gesamten Nachrichtenversand von Journey Optimizer zu Zwecken des Reportings und der Zielgruppenerstellung. In diesem Datensatz wird auch das Feedback von E-Mail-ISPs zu Bounces aufgezeichnet. **Dieser Datensatz verwendet die Batch-Aufnahme - rechnen Sie mit einer Datenlatenz von bis zu 2 Stunden.**
   * _Reporting – Ereignisdatensatz des E-Mail-Tracking-Erlebnisses:_ Interaktionsprotokolle für den E-Mail-Kanal und WhatsApp-Kanal-Kontextdaten unter der Feldergruppe „`whatsAppChannelContext`“. Wird für das Reporting und die Erstellung von Zielgruppen verwendet. Die gespeicherten Informationen enthalten die von Endbenutzenden durchgeführten Aktionen in Bezug auf E-Mails (Öffnungen, Klicks usw.) sowie WhatsApp-Interaktionen.
   * _Reporting – Push-Tracking-Erlebnisereignis-Datensatz_: Interaktionsprotokolle für den Push-Kanal, der zu Zwecken des Reportings und der Zielgruppenerstellung genutzt wird. Die gespeicherten Informationen geben Aufschluss über die von Endbenutzenden durchgeführten Aktionen bei Push-Benachrichtigungen.
   * _Reporting – Journey-Schrittereignis_: Erfasst alle von Journey Optimizer generierten Journey-Schritt-Erlebnisereignisse, die von Services wie Reporting genutzt werden können. Auch wichtig für die Erstellung von Berichten in Customer Journey Analytics für die Jahresanalyse. An Journey-Metadaten gebunden.
   * _Reporting – Journeys_: Metadaten-Datensatz, der Informationen zu jedem Schritt in einer Journey enthält.
   * _Reporting – BCC_: Feedback-Ereignis-Datensatz, in dem die Versand-Logs für BCC-E-Mails gespeichert werden. Wird zu Reporting-Zwecken verwendet.

* Einverständnis

  _Einverständnis-Service-Datensatz_: speichert die Einverständnisinformationen eines Profils.

* Nachrichtenexport

  _Exportdatensatz für AJO-Nachrichten_: speichert den Inhalt gesendeter E-Mails und SMS-Nachrichten zu Exportzwecken. Einträge werden nach der Aufnahme 7 Kalendertage lang aufbewahrt. Nur für Organisationen verfügbar, die das Add-on für den Nachrichtenexport erworben haben. [Weitere Informationen](../configuration/message-export.md)

* Intelligent Services

  _Sendezeit-Optimierungsbewertungen/Interaktionswerte_: Ausgabebewertungen der Journey-KI.

* Eingehend

  _Ereignisdatensatz für eingehende AJO-Aktivitäten_: Speichert eingehende Aktivitätsereignisse für eingehende Nachrichten, die in [!DNL Journey Optimizer] empfangen werden.

>[!NOTE]
>
>Ein Profil muss über mindestens eine von [!DNL Journey Optimizer] gesendete Nachricht verfügen, bevor eingehende Nachrichten in diesem Datensatz erfasst werden.

## Erstellen von Datensätzen{#create-datasets}

Das Hinzufügen von Daten zu [!DNL Adobe Experience Platform] bildet die Grundlage für die Erstellung eines Profils. Anschließend können Sie Profile in [!DNL Adobe Journey Optimizer] nutzen. Definieren Sie zunächst Schemata, verwenden Sie ETL-Tools, um Ihre Daten vorzubereiten und zu standardisieren, und erstellen Sie dann Datensätze basierend auf Ihren Schemata.

Sie können einen Datensatz aus einem Schema oder einer CSV-Datei erstellen. Ausführliche Informationen zum Erstellen von Datensätzen finden Sie in der Dokumentation zu [!DNL Adobe Experience Platform]:

* [Datensatz mit vorhandenem Schema erstellen](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/user-guide#schema){target="_blank"}
* [Zuordnen einer CSV-Datei zu einem vorhandenen XDM-Schema](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/tutorials/map-csv/existing-schema){target="_blank"}

In diesem Video erfahren Sie, wie Sie einen Datensatz erstellen, ihn einem Schema zuordnen, ihm Daten hinzufügen und bestätigen, dass die Daten aufgenommen wurden.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## Aktivieren von Datensätzen für Profile {#profile-datasets}

Wenn Sie einen Datensatz erstellen, können Sie ihn aktivieren, um einen Beitrag zum [Echtzeit-Kundenprofil“ &#x200B;](../audience/get-started-profiles.md). Dadurch können die darin enthaltenen Daten für die Segmentierung, Personalisierung und das Journey in [!DNL Journey Optimizer] verwendet werden.

Beachten Sie vor dem Aktivieren Folgendes:

* **Die Aktivierung des Schemas ist dauerhaft.** Sobald das einem Datensatz zugrunde liegende Schema für das Profil aktiviert wurde, kann dies nicht mehr rückgängig gemacht werden. Das Schema kann nicht mehr deaktiviert oder gelöscht werden. Nur der Datensatz selbst kann separat deaktiviert oder gelöscht werden.
* **Die Deaktivierung eines Datensatzes hat Folgen.** Sie können einen Datensatz für das Profil unabhängig vom Schema deaktivieren oder löschen, dadurch werden jedoch die zugehörigen Profildatensätze entfernt und die Segmentierungs- und Aktivierungs-Workflows können unterbrochen werden.
* **Planung der Konfiguration vor der Aktivierung.** Das Ändern von Identitätsfeldern und Feldergruppenauswahlen wird nach der Aktivierung des Profils schwieriger. Schließen Sie zuerst den Schemaentwurf ab.

Ausführliche Anleitungen finden Sie in der Dokumentation zu Adobe Experience Platform:

* [Planung der Profilaktivierung](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"} - Checkliste vor der Aktivierung, die die Identitätskonfiguration, die Feldergruppenauswahl und die Validierung des Datensatzzwecks umfasst.
* [Verwalten von profilaktivierten Schemata](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"} - Anleitung zur Einstellung von profilaktivierten Schemata, einschließlich Umbenennungsstrategien.

## Data Governance

Sie können in einem Datensatz die Registerkarte **Data Governance** durchsuchen, um Kennzeichnungen auf Datensatz- und Feldebene zu überprüfen. Mit Data Governance werden Daten entsprechend dem anzuwendenden Richtlinientyp kategorisiert.

Eine der Kernfunktionen von [!DNL Adobe Experience Platform] ist es, Daten aus verschiedenen Unternehmenssystemen zusammenzuführen, damit Marketing-Experten Kunden besser identifizieren, verstehen und ansprechen können. Diese Daten können Nutzungsbeschränkungen unterliegen, die von Ihrem Unternehmen oder durch gesetzliche Bestimmungen festgelegt werden. Daher müssen Sie dafür sorgen, dass Ihre Datenoperationen die entsprechenden Datennutzungsrichtlinien einhalten.

Mit [!DNL Adobe Experience Platform Data Governance] können Sie Kundendaten verwalten und bei der Verwendung von Daten die Einhaltung von relevanten Vorschriften, Einschränkungen und Richtlinien sicherstellen. Die Funktion spielt in Experience Platform auf verschiedenen Ebenen eine wichtige Rolle, wie z. B. bei Katalogisierung, Ermittlung der Datenherkunft, Datennutzungsbezeichnung, Datennutzungsrichtlinien und Steuerung der Nutzung von Daten für Marketing-Aktionen.

Weitere Informationen zu Data Governance und Datennutzungskennzeichnungen finden Sie in der [Dokumentation zur Data Governance](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html?lang=de){target="_blank"}.

## Beispiele und Anwendungsfälle {#samples}

* [Tutorial – Aufnehmen von Daten in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=de){target="_blank"}
* [End-to-End-Anwendungsfall](../audience/creating-test-profiles.md) – Erstellen eines Schemas oder eines Datensatzes und Aufnehmen von Daten zum Hinzufügen von Testprofilen in [!DNL Adobe Journey Optimizer]
* [Abfragebeispiele](../data/datasets-query-examples.md) – [!DNL Adobe Journey Optimizer]-Datensätze und zugehörige Anwendungsfälle.

>[!MORELIKETHIS]
>
>* [Erste Schritte mit Daten-Management in Journey Optimizer](gs-data.md)
>* [Dokumentation zu Datensätzen](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de){target="_blank"}
>* [Dokumentation zur Datenaufnahme](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target="_blank"}.
>* [Best Practices für die Verwaltung von Daten im Rahmen von Lizenzberechtigungen](https://experienceleague.adobe.com/de/docs/experience-platform/landing/license/data-management-best-practices#data-management-best-practices){target="_blank"}
>* [Verwalten von profilaktivierten Schemata](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}
