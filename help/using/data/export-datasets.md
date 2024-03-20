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
source-git-commit: 83751eae9f703a89a57cb337492377ff2478d4a0
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 48%

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

Machen Sie sich mit der Tabelle vertraut, unter welchen Journey Optimizer-Datensätzen Sie exportieren können.

| Datensatz | Beschreibung |
| ------- | ------- | 
| AJO BCC Feedback-Ereignis-Datensatz | AJO BCC Feedback-Ereignis-Datensatz |
| AJO-Klassifizierungsdatensatz | Datensatz zur Aufnahme von E-Mail- und Push-App-Feedback-Ereignissen aus Journey Optimizer. Erstellt über SDK. |
| Datensatz des AJO Consent Service | Speichert Zustimmungsinformationen eines Profils. |
| Ereignisdatensatz zu Erfahrungen beim AJO-E-Mail-Tracking | Interaktionsprotokolle für den E-Mail-Kanal, der für Berichte und die Erstellung von Zielgruppen verwendet wird.  |
| AJO-Entitäts-Datensatz | Datensatz zum Speichern von Entitätsmetadaten für Nachrichten, die an den Endbenutzer gesendet werden.  |
| Ereignisdatensatz für eingehende AJO-Aktivitäten | Datensatz für Journey Optimizer-Web- und In-App-Kanäle für Bereitstellungs- und Interaktionsereignisse. |
| AJO-Profildatensatz für interaktive Nachrichten | Speichert Profile, die erstellt wurden, um API-gesteuerte Kampagnen zu unterstützen |
| Ereignisdatensatz mit Feedback zu AJO-Nachrichten | Versandlogs der Nachrichten. Informationen über den gesamten Nachrichtenversand von Journey Optimizer zu Zwecken des Reportings und der Zielgruppenerstellung. In diesem Datensatz wird auch das Feedback von E-Mail-ISPs zu Bounces aufgezeichnet. |
| AJO Profile Counters-Erweiterung | Enthält eine Zuordnung von Objekten, die &quot;counter_value&quot;und &quot;iryDate&quot;enthalten, die von &quot;counter_id&quot;eingegeben wurden |
| AJO Push Profile DataSet | Speichert Push-Token eines Profils. |
| Ereignisdatensatz zu Erfahrungen beim AJO-Push-Tracking | Interaktionsprotokolle für den Push-Kanal, die für Berichte und die Erstellung von Zielgruppen verwendet werden.  |
| AJO-Oberflächen-Datensatz | Leerer Datensatz im Zusammenhang mit dem Schema &quot;Eingehende Journey Optimizer-Oberflächen&quot; |
| AOOutputForUPSDataset | Enthält alle AO-Zielgruppenmitgliedschaften, die in UPS zurückgeschrieben werden sollen |
| Zielgruppen-Orchestrierung Profil-Datensatz | Wird durch die Zielgruppenkomposition für Zielgruppen der Zielgruppenkomposition generiert. Enthält alle Zielgruppen &quot;Zielgruppenkomposition&quot;, deren Attribute und Anreicherungsdaten |
| Decision Object Repository - Aktivitäten | auch als Entscheidungen in der Benutzeroberfläche bezeichnet. Dies sind jedoch die Objekte, die eine Benutzerin bzw. ein Benutzer erstellt, mit denen alle Bausteine zusammengeführt werden, einschließlich der Entscheidungslogik. Beispielsweise für eine bestimmte Platzierung (Position), welche Angebote (Angebotskollektion) berücksichtigt werden sollen und welche Rangmethode für diese Angebote verwendet werden soll. |
| Decision Object Repository - Fallback-Angebote | Dies ist das Repository für den anderen Angebotstyp, den ein Benutzer erstellt. Insbesondere wenn sie nicht geeignet sind, ein personalisiertes Angebot zu sehen, und sie etwas sehen müssen, dann sehen sie zumindest das Fallback-Angebot. Dieser Datensatz enthält die Attribute für diesen Angebotstyp |
| Decision Object Repository - Personalisierte Angebote | Dies ist das Repository für einen Angebotstyp, den ein Benutzer erstellt. Dieser Datensatz enthält also die Attribute zu diesem Angebotstyp | Ultimate |
| Entscheidungsobjekt-Repository - Platzierungen | Dies ist das Repository von Objekten, die den Speicherort definieren, an dem ein Angebot angezeigt werden soll. |
| Journey-Schritt-Ereignisse | Erfasst alle von Journey Optimizer generierten Journey-Schritt-Erlebnisereignisse, die von Diensten wie Reporting genutzt werden können. |
| Journeys | Informationen zur Speicherung von Metadaten-Datensätzen für jeden Schritt in einer Journey |
| ODE DecisionEvents - prod decisioning | Jedes Mal, wenn wir eine auf einer Anfrage basierende Entscheidung treffen, zählen wir dies als Entscheidungsereignis |

## Voraussetzungen {#prerequisites}

Zum Exportieren von Datensätzen benötigen Sie die [Zugriffssteuerungsberechtigungen](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=de#permissions){target="_blank"} listed below. Read the [access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html?lang=de){target="_blank"} oder wenden Sie sich an Ihren Produktadministrator, um die erforderlichen Berechtigungen zu erhalten.

| Kategorie | Berechtigung |
|--|--|
| Ziele | Verwalten und Aktivieren von Datensatzzielen |
| Daten-Management | Anzeigen von Datensätzen |
| Ziele | Anzeigen von Zielen |

## Wichtige Schritte zum Exportieren von Datensätzen {#main-steps}

Die wichtigsten Schritte zum Exportieren eines Datensatzes in einen Cloud-Speicherort sind:

![](assets/dataset-export-process.png)

Detaillierte Informationen zu den einzelnen Schritten finden Sie unter [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=de){target="_blank"}.

1. **Einrichten des Cloud-Speicher-Ziels**. Falls Sie dies noch nicht getan haben, stellen Sie eine Verbindung zu einem Cloud-Speicher-Ziel aus dem Zielkatalog her. Erfahren Sie, wie Sie eine neue Zielverbindung erstellen in [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=de#setup){target="_blank"}.

   <!--![](assets/dataset-export-setup.png)-->

1. **Wählen Sie das Cloud-Speicher-Ziel aus**, wohin Sie Ihre Datensätze exportieren möchten. Klicken Sie im Zielkatalog auf die Schaltfläche **[!UICONTROL Datensätze exportieren]** auf der gewünschten Karte und wählen Sie die zu verwendende Verbindung.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Wenn Sie Adobe Journey Optimizer zusammen mit Echtzeit-Kundenprofilen verwenden, zeigen die Zielkarten eine **Aktivieren** -Schaltfläche, über die Sie Datensätze exportieren und Zielgruppen für dieses Ziel aktivieren können, hängt von den Berechtigungen ab, die Sie aktiviert haben.

1. **Wählen Sie die Datensätze aus**, die Sie an das ausgewählte Ziel exportieren möchten. [Weitere Informationen zu für den Export verfügbare Journey Optimizer-Datensätze](#datasets)

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Planen Sie den Export** Ihres Datensatzes. Geben Sie an, wann der Export beginnen soll und mit welcher Häufigkeit er erfolgen soll.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Überprüfen und bestätigen Sie den Export**, indem Sie die Zusammenfassung durchgehen, die am Ende der Konfiguration angezeigt wird.

   <!--![](assets/dataset-export-review.png)-->

Sobald der Export abgeschlossen ist, wird der Inhalt des Datensatzes gemäß dem konfigurierten Zeitplan am Cloud-Speicherort abgelegt. [Erfahren Sie, wie Sie einen erfolgreichen Datensatzexport überprüfen.](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=de#verify){target="_blank"}.
