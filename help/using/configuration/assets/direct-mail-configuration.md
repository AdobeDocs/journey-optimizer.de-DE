---
title: Briefpost-Nachricht erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer eine Briefpost-Nachricht erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: e3ae60321aac340328e1fcd7b1060192fbc7ee06
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 3%

---

# Briefpost-Konfiguration {#create-direct}

[!DNL Journey Optimizer] ermöglicht Ihnen, die von Briefpost-Dienstleistern benötigten Dateien zu personalisieren und zu generieren, um E-Mails an Ihre Kunden zu senden.

Wenn Sie einen Briefpost-Versand vorbereiten, [!DNL Journey Optimizer] erzeugt eine Datei mit allen Zielgruppenprofilen und den ausgewählten Kontaktinformationen (z. B. Postanschrift). Dann senden Sie diese Datei an Ihren Briefpost-Dienstleister, der den tatsächlichen Versand vornimmt.

Um eine Briefpost-Nachricht zu senden, müssen Sie eine Datei erstellen und auf einen Server hochladen. Bevor Sie dazu in der Lage sind, müssen Sie eine [Dateirouting-Konfiguration](#file-routing-configuration) und [Briefpost-Oberfläche](#direct-mail-surface) , der auf die Dateirouting-Konfiguration verweist.

## Datei-Routing konfigurieren {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Definieren der Einstellungen der Dateirouting-Konfiguration"
>abstract="Sie müssen definieren, wo die Datei exportiert und hochgeladen werden soll, damit Ihr Briefpost-Dienstleister sie verwenden kann."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Definieren der Einstellungen der Dateirouting-Konfiguration"
>abstract="Bei der Erstellung der Briefpost-Nachricht generieren Sie die Datei, die alle erforderlichen Profilinformationen enthält. Diese Datei muss exportiert und auf einen Server hochgeladen werden, damit Ihr Briefpost-Dienstleister auf diese Datei zugreifen und sie für den Versand von Briefpost verwenden kann."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Konfiguration der Dateiweiterleitung"
>abstract="Wählen Sie die gewünschte Konfiguration für das Dateirouting aus, die festlegt, wo die Datei exportiert und für Ihren Briefpost-Dienstleister hochgeladen werden soll."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Wählen Sie den Servertyp für Ihr Datei-Routing aus."
>abstract="Wählen Sie den Server aus, den Sie zum Hochladen und Speichern der Briefpost-Dateien verwenden möchten."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="AWS-Region auswählen"
>abstract="Wählen Sie den Server aus, den Sie zum Hochladen und Speichern der Briefpost-Dateien verwenden möchten. Derzeit werden nur Amazon S3 und SFTP unterstützt."

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Konfiguration der Dateiweiterleitung]** > **[!UICONTROL Datei-Routing]** Menü und klicken Sie auf **[!UICONTROL Routing-Konfiguration erstellen]**.

   ![](assets/file-routing-config-button.png)

1. Legen Sie einen Namen für Ihre Konfiguration fest.

1. Wählen Sie die Konfiguration aus **[!UICONTROL Typ]**, d. h. der Server, den Sie zum Hochladen und Speichern der Briefpost-Dateien verwenden möchten.<!--why is it Type and not Server or Server type? asked to PM-->

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Derzeit sind nur Amazon S3 und SFTP verfügbar.

   Bei der Erstellung der Briefpost-Nachricht generieren Sie die Datei, die alle erforderlichen Profilinformationen enthält. Diese Datei muss exportiert und auf einen Server hochgeladen werden, damit Ihr Briefpost-Dienstleister auf diese Datei zugreifen und sie für den Versand von Briefpost verwenden kann.

1. Füllen Sie die Details und Anmeldeinformationen aus, die für den ausgewählten Konfigurationstyp spezifisch sind, z. B. Serveradresse, Zugriffsschlüssel usw. <!--need to detail more?-->

   <!--![](assets/file-routing-config-aws-details.png)-->

   ![](assets/file-routing-config-sftp-details.png)

1. Wenn Sie **[!UICONTROL Amazon S3]** können Sie die AWS-Region auswählen, in die Sie Ihre Briefpost-Dateien exportieren und hochladen möchten.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >AWS-Regionen sind separate geografische Gebiete auf der ganzen Welt, die AWS für die Unterbringung seiner Infrastruktur nutzt. Für eine optimale Nutzung wird empfohlen, die nächstgelegene Region für das Hosten Ihrer Cloud-Infrastruktur auszuwählen.

1. Klicken Sie auf **[!UICONTROL Übermitteln]**. Die Konfiguration des Datei-Routing wird mit der **[!UICONTROL Aktiv]** Status. Es kann jetzt auf einer Briefpost-Oberfläche verwendet werden, um Briefpost von zu senden. [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >Sie können auch **[!UICONTROL Als Entwurf speichern]** um die Konfiguration des Datei-Routing zu erstellen, Sie können sie jedoch erst dann auf einer Oberfläche auswählen, wenn sie **[!UICONTROL Aktiv]**.

## Briefpost-Oberfläche erstellen {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Briefpost-Einstellungen definieren"
>abstract="Eine Briefpost-Oberfläche enthält die Einstellungen für die Formatierung der Datei mit Profildaten für Briefpost. Sie können (die Sortierkonfiguration definieren), doppelte Zeilen entfernen, Datensätze in mehrere Dateien aufteilen und die Konfiguration der Dateiweiterleitung auswählen."

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Sortierreihenfolge definieren"
>abstract="Wenn Sie diese Option auswählen, wird die Sortierung nach Profil-ID (aufsteigend oder absteigend) vorgenommen. Wenn Sie die Auswahl aufheben, wird die beim Erstellen der Briefpost-Nachricht in einer Journey oder Kampagne definierte Sortierkonfiguration verwendet."

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Definieren der Schwelle für die Dateiaufteilung"
>abstract="Sie müssen die maximale Datensatzanzahl für jede Datei festlegen, die Profildaten enthält. Nachdem der angegebene Schwellenwert erreicht wurde, wird eine weitere Datei für die verbleibenden Datensätze erstellt."

Nachdem das Datei-Routing konfiguriert wurde, müssen Sie eine Kanaloberfläche erstellen, um Briefpost aus senden zu können. [!DNL Journey Optimizer]. Auf jeder Oberfläche müssen Sie eine Dateirouting-Konfiguration auswählen.

1. Erstellen einer Kanaloberfläche. [Weitere Informationen](channel-surfaces.md)

1. Wählen Sie die **[!UICONTROL Briefpost]** -Kanal.

   ![](assets/surface-direct-mail-channel.png)

1. Definieren Sie die Briefpost-Einstellungen im entsprechenden Abschnitt der Kanaloberflächenkonfiguration.

   ![](assets/surface-direct-mail-settings.png)

1. Wählen Sie das Dateiformat aus: **[!UICONTROL CSV]** oder **[!UICONTROL Textgetrennt]**.

1. Im **[!UICONTROL Einfügen]** können Sie auswählen, ob Sie automatisch doppelte Zeilen entfernen möchten.

1. Definieren Sie die maximale Anzahl von Datensätzen (d. h. Zeilen) für jede Datei, die Profildaten enthält. Nachdem der angegebene Schwellenwert erreicht wurde, wird eine weitere Datei für die verbleibenden Datensätze erstellt.

   ![](assets/surface-direct-mail-split.png)

   Wenn die Datei beispielsweise 100.000 Datensätze enthält und der Schwellenwert auf 60.000 festgelegt ist, werden die Datensätze in zwei Dateien aufgeteilt. Die erste Datei enthält 60.000 Zeilen, die zweite die restlichen 40.000 Zeilen.

   >[!NOTE]
   >
   >Sie können eine beliebige Zahl zwischen 1 und 200.000 Datensätzen festlegen, d. h. jede Datei muss mindestens 1 Zeile und höchstens 200.000 Zeilen enthalten.

1. Wählen Sie abschließend die [Dateirouting-Konfiguration](#file-routing-configuration) unter den von Ihnen erstellten. Dadurch wird definiert, wo die Datei exportiert und hochgeladen wird, damit sie von Ihrem Briefpost-Dienstleister verwendet werden kann.

   >[!CAUTION]
   >
   >Wenn Sie keine Dateirouting-Option konfiguriert haben, können Sie keine Briefpost-Oberfläche erstellen. [Weitere Informationen](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)