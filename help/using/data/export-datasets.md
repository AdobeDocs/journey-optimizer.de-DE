---
solution: Journey Optimizer
product: journey optimizer
title: Exportieren von Datensätzen zu Orten im Cloud-Speicher
description: Erfahren Sie, wie Sie Ihre Datensätze mit Adobe Experience Platform-Cloud-Speicherzielen exportieren können.
feature: Datasets
role: User
level: Beginner
keywords: Plattform, Data Lake, Erstellen, Lake, Datensätze, Profil
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 100%

---

# Exportieren von Datensätzen zu Orten im Cloud-Speicher {#export-datasets}

Journey Optimizer ermöglicht es Ihnen, eine Live-Verbindung mit Zielen im Cloud-Speicher herzustellen, um den Inhalt Ihrer Datensätze zu exportieren.

Durch den periodischen Export Ihrer Daten können Sie sicherstellen, dass Sie über einen vollständigen und aktuellen Eintrag Ihrer Kundeninteraktionen verfügen, sodass diese jederzeit für Berichte, Archivierungen oder Datenanalysen verfügbar sind.

## Unterstützte Cloud-Speicher-Ziele {#destinations}

Sie können Datensätze in 6 Cloud-Speicher-Ziele exportieren, auf die Sie über das Menü **[!UICONTROL Ziele]** auf der Registerkarte **[!UICONTROL Katalog]** zugreifen können.

![](assets/dataset-export-setup.png)


Detaillierte Informationen zu den einzelnen Zielen finden Sie in der Adobe Experience Platform-Dokumentation:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html?lang=de)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html?lang=de)
* [Azure Data Lake Gen2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html?lang=de)
* [Data Landing Zone](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html?lang=de)
* [Google Cloud Storage](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html?lang=de)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html?lang=de)

## Verfügbare Datensätze für den Export {#datasets}

Machen Sie sich durch die Tabelle unten damit vertraut, welche Journey Optimizer-Datensätze Sie exportieren können.

| Datensatz | Beschreibung |
| ------- | ------- | 
| Ereignisdatensatz mit Feedback zu AJO-BCC | Ereignisdatensatz mit Feedback zu AJO-BCC |
| AJO-Klassifizierungs-Datensatz | Datensatz zur Aufnahme von Feedback-Ereignissen zu E-Mail- und Push-Anwendungen aus Journey Optimizer.  Erstellt über SDK. |
| AJO-Einverständnisdienst-Datensatz | Speichert Einverständnisinformationen eines Profils. |
| Ereignisdatensatz zu Erfahrungen beim AJO-E-Mail-Tracking | Interaktionsprotokolle für den E-Mail-Kanal, der zu Zwecken des Reportings und der Zielgruppenerstellung genutzt wird.  |
| AJO-Entitäts-Datensatz | Datensatz zum Speichern von Entitätsmetadaten für Nachrichten, die an die Endbenutzenden gesendet werden.  |
| Ereignisdatensatz für eingehende AJO-Aktivitäten | Datensatz für Web- und In-App-Kanäle von Journey Optimizer für Versand- und Interaktionsereignisse. |
| Profildatensatz für interaktive AJO-Nachrichten | Speichert Profile, die erstellt wurden, um API-gesteuerte Kampagnen zu unterstützen |
| Ereignisdatensatz mit Feedback zu AJO-Nachrichten | Nachrichten-Versandlogs.  Informationen über den gesamten Nachrichtenversand von Journey Optimizer zu Zwecken des Reportings und der Zielgruppenerstellung. In diesem Datensatz wird auch das Feedback von E-Mail-ISPs zu Bounces aufgezeichnet. |
| AJO Profile Counters-Erweiterung | Enthält eine Zuordnung von Objekten, die „counter_value“ und „expiryDate“ enthalten, die von „counter_id“ eingegeben wurden. |
| AJO-Push-Profil-Datensatz | Speichert Push-Token eines Profils. |
| Erlebnisereignisdatensatz beim AJO-Push-Tracking | Interaktionsprotokolle für den Push-Kanal, der zu Zwecken des Reportings und der Zielgruppenerstellung genutzt wird.  |
| AJO-Oberflächen-Datensatz | Leerer Datensatz im Zusammenhang mit dem Schema „Eingehende Journey Optimizer-Oberflächen“ |
| AOOutputForUPSDataset | Enthält alle AO-Zielgruppenzugehörigkeiten, die in UPS zurückgeschrieben werden sollen |
| Profil-Datensatz der Zielgruppen-Orchestrierung | Wird durch die Zielgruppenkomposition für Zielgruppenkompositions-Zielgruppen generiert. Enthält alle Zielgruppenkompositions-Zielgruppen, ihre Attribute und Anreicherungsdaten |
| Entscheidungsobjekt-Repository – Aktivitäten | in der Benutzeroberfläche auch als „Entscheidungen“ bezeichnet. Dies sind jedoch die Objekte, die eine Benutzerin bzw. ein Benutzer erstellt, mit denen alle Bausteine zusammengeführt werden, einschließlich der Entscheidungslogik. Beispielsweise wird für eine bestimmte Platzierung (Position) entschieden, welche Angebote (Angebotssammlung) berücksichtigt werden sollen und welche Rangfolgenmethode für diese Angebote verwendet werden soll.  |
| Entscheidungsobjekt-Repository – Fallback-Angebote | Dies ist das Repository für den anderen Angebotstyp, den eine Benutzerin oder ein Benutzer erstellt. Insbesondere wenn sie nicht geeignet sind, ein personalisiertes Angebot zu sehen, und sie etwas sehen müssen, dann sehen sie zumindest das Fallback-Angebot. Dieser Datensatz enthält die Attribute für diesen Angebotstyp |
| Entscheidungsobjekt-Repository – Personalisierte Angebote | Dies ist das Repository für einen Angebotstyp, den eine Benutzerin oder ein Benutzer erstellt. Dieser Datensatz enthält also die Attribute zu diesem Angebotstyp | Ultimate |
| Entscheidungsobjekt-Repository – Platzierungen | Dies ist das Repository von Objekten, die die Stelle definieren, an der ein Angebot angezeigt werden soll. |
| Journey-Schrittereignisse | Erfasst alle von Journey Optimizer generierten Journey-Schritt-Erlebnisereignisse, die von Services wie Reporting genutzt werden können.  |
| Journeys | Metadaten-Datensatz, der Informationen zu jedem Schritt in einer Journey enthält. |
| ODE DecisionEvents – Produktions-Entscheidungsfindung | Jedes Mal, wenn wir eine auf einer Anfrage basierende Entscheidung treffen, zählen wir dies als Entscheidungsereignis |

## Voraussetzungen {#prerequisites}

Zum Exportieren von Datensätzen benötigen Sie die [Zugriffssteuerungsberechtigungen](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=de#permissions){target="_blank"} listed below. Read the [access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html?lang=de){target="_blank"} oder wenden Sie sich an Ihre Produktadmins, um die erforderlichen Berechtigungen zu erhalten.

| Kategorie | Berechtigung |
|--|--|
| Ziele | Verwalten und Aktivieren von Datensatzzielen |
| Daten-Management | Anzeigen von Datensätzen |
| Ziele | Anzeigen von Zielen |

## Die wichtigsten Schritte zum Exportieren von Datensätzen {#main-steps}

Die wichtigsten Schritte zum Exportieren eines Datensatzes in einen Cloud-Speicherort sind:

![](assets/dataset-export-process.png)

Detaillierte Informationen zu jedem Schritt finden Sie in der [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=de){target="_blank"}.

1. **Einrichten des Cloud-Speicher-Ziels**. Falls Sie dies noch nicht getan haben, stellen Sie eine Verbindung zu einem Cloud-Speicher-Ziel aus dem Zielkatalog her. In der [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=de#setup){target="_blank"} erfahren Sie, wie Sie eine neue Zielverbindung erstellen.

   <!--![](assets/dataset-export-setup.png)-->

1. **Wählen Sie das Cloud-Speicher-Ziel aus**, wohin Sie Ihre Datensätze exportieren möchten. Klicken Sie im Zielkatalog auf die Schaltfläche **[!UICONTROL Datensätze exportieren]** auf der gewünschten Karte und wählen Sie die zu verwendende Verbindung.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Wenn Sie Adobe Journey Optimizer zusammen mit Echtzeit-Kundenprofilen verwenden, wird auf den Zielkarten die Schaltfläche **Aktivieren** angezeigt, mit der Sie abhängig von den aktivierten Berechtigungen sowohl Datensätze exportieren als auch Zielgruppen für dieses Ziel aktivieren können.

1. **Wählen Sie die Datensätze aus**, die Sie an das ausgewählte Ziel exportieren möchten. [Weitere Informationen zu für den Export verfügbare Journey Optimizer-Datensätze](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Planen Sie den Export** Ihres Datensatzes. Geben Sie an, wann der Export beginnen soll und mit welcher Häufigkeit er erfolgen soll.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Überprüfen und bestätigen Sie den Export**, indem Sie die Zusammenfassung durchgehen, die am Ende der Konfiguration angezeigt wird.

   <!--![](assets/dataset-export-review.png)-->

Sobald der Export abgeschlossen ist, wird der Inhalt des Datensatzes gemäß dem konfigurierten Zeitplan am Cloud-Speicherort abgelegt. [Informationen zum erfolgreichen Überprüfen eines Datensatzexports](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=de#verify){target="_blank"}.
