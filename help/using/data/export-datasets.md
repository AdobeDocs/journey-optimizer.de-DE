---
solution: Journey Optimizer
product: journey optimizer
title: Exportieren von Datensätzen in Cloud-Speicherorte
description: Erfahren Sie, wie Sie Ihre Datensätze mit Adobe Experience Platform Cloud-Speicher-Zielen exportieren.
role: User
level: Beginner
badge: label="Beta" type="Informative"
keywords: Plattform, Data Lake, Erstellen, Lake, Datensätze, Profil
source-git-commit: c3ad875b50999da833d75e97a787cab9e24e38d4
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 10%

---


# Exportieren von Datensätzen in Cloud-Speicherorte {#export-datasets}

>[!AVAILABILITY]
>
>Die Funktion zum Exportieren von Datensätzen befindet sich derzeit in der Beta-Phase und steht allen Adobe Journey Optimizer-Benutzern zur Verfügung. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie noch keinen Zugriff auf Ziele haben.

Mit Journey Optimizer können Sie eine Live-Verbindung mit Cloud-Speicherorten herstellen, um den Inhalt Ihrer Datensätze zu exportieren.

Durch den regelmäßigen Export Ihrer Daten können Sie sicherstellen, dass Sie über einen vollständigen und aktuellen Datensatz Ihrer Kundeninteraktionen verfügen, diese Informationen zu Berichts- oder Analysezwecken verwenden und die gesetzlichen Anforderungen erfüllen.

## Verfügbare Cloud-Speicher-Ziele {#destinations}

Sie können Datensätze in 6 Cloud-Speicher-Ziele exportieren, auf die über die **[!UICONTROL Ziele]** im Menü **[!UICONTROL Katalog]** Registerkarte.

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>Diese Ziele sind alle in der Beta-Version verfügbar und können geändert werden.

Detaillierte Informationen zu den einzelnen Zielen finden Sie in der Adobe Experience Platform-Dokumentation:

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure Data Lake Gen 2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [Data Landing Zone](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google Cloud Storage](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## Voraussetzungen {#prerequisites}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie mit dem Export Ihrer Datensätze beginnen:

* Zum Exportieren von Datensätzen benötigen Sie die [Zugriffssteuerungsberechtigungen](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions) **Ziele verwalten**, **Ziele anzeigen**, **Ziele aktivieren** und **Datensatzziele verwalten und aktivieren** Lesen Sie die [Übersicht über die Zugriffskontrolle](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) oder wenden Sie sich an Ihren Produktadministrator, um die erforderlichen Berechtigungen zu erhalten.

* Diese Funktion unterstützt nur den Export von Daten der ersten Generation, d. h. von Rohdaten, wie in der Variablen [Real-time Customer Data Platform-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). Stellen Sie sicher, dass der zu exportierende Datensatz keine Daten der zweiten Generation enthält.

## Die wichtigsten Schritte zum Exportieren von Datensätzen {#main-steps}

Die wichtigsten Schritte zum Exportieren eines Datensatzes in einen Cloud-Speicher sind:

![](assets/dataset-export-process.png)

Detaillierte Informationen zu den einzelnen Schritten finden Sie in der Adobe Experience Platform-Dokumentation: [Exportieren von Datensätzen in Cloud-Speicher-Ziele](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en).

1. **Einrichten des Cloud-Speicher-Ziels**. Wenn Sie dies noch nicht getan haben, stellen Sie im Zielkatalog eine Verbindung zu einem Cloud-Speicher-Ziel her. [Erfahren Sie, wie Sie eine neue Zielverbindung erstellen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **Wählen Sie das Cloud-Speicher-Ziel aus** wo Sie Ihre Datensätze exportieren möchten. Klicken Sie im Zielkatalog auf die **[!UICONTROL Exportieren von Datensätzen]** auf der gewünschten Karte klicken und die zu verwendende Verbindung auswählen.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Wenn Sie Adobe Journey Optimizer zusammen mit Echtzeit-Kundenprofilen verwenden, wird auf den Zielkarten die Schaltfläche &quot;Aktivieren&quot;angezeigt, über die Sie je nach den Berechtigungen, die Sie aktiviert haben, Datensätze exportieren und Segmente für dieses Ziel aktivieren können.

1. **Datensatz(e) auswählen** , das Sie an das ausgewählte Ziel exportieren möchten.

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Export planen** Ihres Datensatzes. Geben Sie an, wann der Export beginnen soll und mit welcher Häufigkeit er erfolgen soll.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Export überprüfen und bestätigen** durch Überprüfung der Zusammenfassung, die am Ende der Konfiguration angezeigt wird.

   <!--![](assets/dataset-export-review.png)-->

Sobald der Export abgeschlossen ist, wird der Inhalt Ihres Datensatzes gemäß dem von Ihnen konfigurierten Zeitplan auf Ihrem Cloud-Speicher abgelegt. [Erfahren Sie, wie Sie einen erfolgreichen Datensatzexport überprüfen.](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
