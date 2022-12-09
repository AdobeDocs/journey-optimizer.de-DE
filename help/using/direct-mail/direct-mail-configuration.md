---
title: Briefpost-Konfiguration
description: Erfahren Sie, wie Sie den Briefpost-Kanal in Journey Optimizer konfigurieren.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: a7c9cbcc23e4a2ef8a3acd887c0f51e51c5befc0
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 0%

---

# Briefpost-Konfiguration {#direct-mail-configuration}

[!DNL Journey Optimizer] ermöglicht Ihnen, die von Briefpost-Dienstleistern benötigten Dateien zu personalisieren und zu generieren, um E-Mails an Ihre Kunden zu senden.

Wann [Briefpost-Nachricht erstellen](../direct-mail/create-direct-mail.md), definieren Sie die Zielgruppendaten, einschließlich der ausgewählten Kontaktinformationen (z. B. Postanschrift). Eine Datei, die diese Daten enthält, wird dann automatisch generiert und auf einen Server exportiert, von dem aus Ihr Briefpost-Dienstleister sie abrufen und den eigentlichen Versand durchführen kann.

Bevor Sie diese Datei generieren können, müssen Sie Folgendes erstellen:

1. A [Dateirouting-Konfiguration](#file-routing-configuration) , um den Server anzugeben, auf dem die Datei exportiert wird.

1. A [Briefpost-Oberfläche](#direct-mail-surface) , der auf die Dateirouting-Konfiguration verweist.

>[!CAUTION]
>
>Wenn Sie keine Dateirouting-Option konfiguriert haben, können Sie keine Briefpost-Oberfläche erstellen.

## Datei-Routing konfigurieren {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definieren der Dateirouting-Konfiguration"
>abstract="Nach der Erstellung einer Briefpost-Nachricht wird die Datei mit den Zielgruppendaten generiert und an einen Server exportiert. Sie müssen die Serverdetails angeben, damit Ihr Briefpost-Dienstleister auf diese Datei zugreifen und sie für den Versand von Briefpost verwenden kann."

<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/create-direct-mail.html" text="Create a direct mail message"-->

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definieren der Dateirouting-Konfiguration"
>abstract="Sie müssen definieren, wo die Datei exportiert werden soll, damit Ihr Briefpost-Dienstleister sie verwenden kann."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Konfiguration der Dateiweiterleitung"
>abstract="Wählen Sie die gewünschte Konfiguration für das Dateirouting aus, die festlegt, wo die Datei für den zu verwendenden Briefpost-Dienstleister exportiert wird."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Wählen Sie den Servertyp für Ihre Datei aus."
>abstract="Wählen Sie den Servertyp aus, den Sie für den Export Ihrer Briefpost-Dateien verwenden möchten. Derzeit werden nur Amazon S3 und SFTP von Journey Optimizer unterstützt."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="AWS-Region auswählen"
>abstract="Wählen Sie die geografische Region des AWS-Servers aus, auf dem Sie Ihre Briefpost-Dateien exportieren möchten. In der Regel ist es empfehlenswert, die Region auszuwählen, die dem Standort Ihres Briefpost-Dienstleisters am nächsten ist."

So senden Sie eine Briefpost-Nachricht: [!DNL Journey Optimizer] generiert und exportiert die Datei mit den Zielgruppendaten an einen Server.

Sie müssen die Serverdetails angeben, damit Ihr Briefpost-Dienstleister auf diese Datei zugreifen und sie für den Versand von E-Mails verwenden kann.

Gehen Sie wie folgt vor, um das Datei-Routing zu konfigurieren.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL File routing configuration]** > **[!UICONTROL File Routing]** Menü und klicken Sie auf **[!UICONTROL Create routing configuration]**.

   ![](assets/file-routing-config-button.png)

1. Legen Sie einen Namen für Ihre Konfiguration fest.

1. Wählen Sie die **[!UICONTROL Server type]** die Sie zum Exportieren der Briefpost-Dateien verwenden möchten.

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Derzeit werden nur Amazon S3 und SFTP in [!DNL Journey Optimizer].

1. Geben Sie die Details und Anmeldedaten für Ihren Server ein, z. B. Serveradresse, Zugriffsschlüssel usw.

   ![](assets/file-routing-config-sftp-details.png)

1. Wenn Sie **[!UICONTROL Amazon S3]**, wählen Sie die **[!UICONTROL AWS region]** wo sich die Serverinfrastruktur befindet.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >AWS-Regionen sind geografische Gebiete, die AWS zum Hosten seiner Cloud-Infrastrukturen verwendet. In der Regel wird empfohlen, die Region auszuwählen, die dem Standort Ihres Briefpost-Dienstleisters am nächsten ist.

1. Auswählen **[!UICONTROL Submit]**. Die Konfiguration des Datei-Routing wird mit der **[!UICONTROL Active]** Status. Sie kann jetzt in einer [Briefpost-Oberfläche](#direct-mail-surface).

   >[!NOTE]
   >
   >Sie können auch **[!UICONTROL Save as draft]** um die Konfiguration des Datei-Routing zu erstellen, Sie können sie jedoch erst dann auf einer Oberfläche auswählen, wenn sie **[!UICONTROL Active]**.

## Briefpost-Oberfläche erstellen {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Briefpost-Einstellungen definieren"
>abstract="Eine Briefpost-Oberfläche enthält die Formatierungseinstellungen der Datei, die die Zielgruppendaten enthält und vom E-Mail-Anbieter verwendet wird. Sie müssen auch festlegen, wo die Datei exportiert werden soll, indem Sie die Konfiguration für das Datei-Routing auswählen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/direct-mail-configuration.html?lang=en#file-routing-configuration" text="Datei-Routing konfigurieren"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definieren der Schwelle für die Dateiaufteilung"
>abstract="Sie müssen die maximale Datensatzanzahl für jede Datei festlegen, die Zielgruppendaten enthält. Sie können eine beliebige Zahl zwischen 1 und 200.000 Datensätzen auswählen. Nachdem der angegebene Schwellenwert erreicht wurde, wird eine weitere Datei für die verbleibenden Datensätze erstellt."

Um Briefpost mit senden zu können [!DNL Journey Optimizer]müssen Sie eine Kanaloberfläche erstellen, um die Formatierungseinstellungen für die Datei zu definieren, die vom E-Mail-Anbieter verwendet werden soll.

Eine Briefpost-Oberfläche muss auch die Konfiguration des Datei-Routing enthalten, die den Server definiert, auf dem Ihre Briefpost-Datei exportiert wird.

1. Erstellen Sie eine Kanaloberfläche. [Weitere Infos](../configuration/channel-surfaces.md)

1. Wählen Sie die **[!UICONTROL Direct mail]** -Kanal.

   ![](assets/surface-direct-mail-channel.png)

1. Definieren Sie die Briefpost-Einstellungen im entsprechenden Abschnitt der Kanaloberflächenkonfiguration.

   ![](assets/surface-direct-mail-settings.png)

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Wählen Sie das Dateiformat aus: **[!UICONTROL CSV]** oder **[!UICONTROL Text delimited]**.

1. Wählen Sie die **[!UICONTROL File routing configuration]** unter den von Ihnen erstellten. Dadurch wird definiert, wo die Datei für Ihren Briefpost-Dienstleister exportiert wird.

   >[!CAUTION]
   >
   >Wenn Sie keine Dateirouting-Option konfiguriert haben, können Sie keine Briefpost-Oberfläche erstellen. [Weitere Infos](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Senden Sie die Briefpost-Oberfläche.

Sie können jetzt [Briefpost-Nachricht erstellen](../direct-mail/create-direct-mail.md) innerhalb einer Kampagne. Nach dem Start der Kampagne wird die Datei mit den Zielgruppendaten automatisch auf den von Ihnen definierten Server exportiert. Der Briefpost-Dienstleister kann dann diese Datei abrufen und mit dem Briefpost-Versand fortfahren.

>[!NOTE]
>
>Doppelte Zeilen werden automatisch entfernt.
>
>Wenn die maximale Datensatzanzahl (d. h. Zeilen) für jede Datei mit Profildaten zu hoch ist, wird automatisch eine weitere Datei für die verbleibenden Datensätze erstellt.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->