---
solution: Journey Optimizer
product: journey optimizer
title: Nachrichtenexport in Journey Optimizer
description: Erfahren Sie, wie Sie Nachrichten exportieren
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Export, Nachrichten, HIPAA, E-Mails, SMS, Konfiguration
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 9e76bfb65865ec7814493ad6e08834d367a9417a
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 4%

---

# Nachrichteninhalt exportieren {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Gesendete Inhalte aufbewahren und exportieren"
>abstract="Wenn Sie diese Option auswählen, können Sie den Inhalt der gesendeten E-Mails oder SMS-Nachrichten mit dieser Konfiguration in einen [!DNL Experience Platform] Datensatz schreiben. Die Datensätze werden 3 Kalendertage lang aufbewahrt, während derer Sie sie in Ihren eigenen Speicher exportieren können."

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie beim Adobe-Support.

**Nachrichtenexport** ermöglicht es Ihnen, gesendete E-Mail- und SMS-Nachrichteninhalte über [!DNL Journey Optimizer] Ziele von [!DNL Adobe Experience Platform] an Ihren eigenen Speicher zu übertragen.

>[!NOTE]
>
>[!DNL Experience Platform] Ziele bestehen aus einem Framework, das die Bereitstellung von Daten aus Experience Platform an externe Endpunkte ermöglicht. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/experience-platform/destinations/home){target="_blank"}

Mit dieser Funktion wird der Inhalt von E-Mail- und SMS-Nachrichten, die über [!DNL Journey Optimizer] gesendet werden und für den Export markiert wurden, in den [!DNL Experience Platform] **AJO-Nachrichtenexportdatensatz**.

Die Datensätze werden dann drei Kalendertage lang im AJO-**** aufbewahrt, um sie in ein externes System Ihrer Wahl zu exportieren.
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## Schutzmechanismen

* Diese Funktion unterstützt nur die Kanäle E-Mail und SMS.
* Datensätze im AJO-Nachrichtenexport-Datensatz werden drei Kalendertage nach der Aufnahme aufbewahrt.
* Die Aufstockung wird nicht für Nachrichten unterstützt, die vor dem Aktivieren des Nachrichtenexports gesendet wurden, wie unten beschrieben.

## Nachrichtenexport aktivieren {#enable-message-export}

Der Onboarding-Prozess für die Funktion Nachrichtenexport besteht aus zwei Schritten:

1. [Einrichten des Datenflusses für den Export](#set-up-export-dataflow) in [!DNL Experience Platform]
1. [Nachrichtenexport aktivieren](#config-message-export) in der Kanalkonfiguration in [!DNL Journey Optimizer].

>[!WARNING]
>
>Nach der Aktivierung von Exporten und dem Nachrichtenversand werden nur neue Datensätze angezeigt. Aufstockungen für Inhalte werden vor der Einrichtung des Exportvorgangs und der Aktivierung der Option „Nachricht exportieren“ nicht unterstützt.

### Einrichten des Datenflusses für den Export {#set-up-export-dataflow}

Bevor Sie Ihre Daten exportieren können, müssen Sie den Exportvorgang einrichten, indem Sie das [!DNL Experience Platform] Ziel und den zu verwendenden Datensatz definieren. Gehen Sie wie folgt vor.

>[!NOTE]
>
>Diese Einrichtung muss für jede Sandbox konfiguriert werden.

1. Wählen Sie einen Experience Platform [Zieltyp](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/destination-types). Eine Liste der verfügbaren Zielplattformen, die für den Empfang von Daten bereit sind, finden Sie auf [dieser Seite](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. Konfigurieren Sie in [!DNL Experience Platform] Ihr Ziel, indem Sie Anmeldeinformationen, einen Bucket/Container, ein Pfadpräfix und Sicherheitsoptionen definieren. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Erstellen Sie einen Datensatz-Exportfluss mit den folgenden Daten:

   * Source-Datensatz: **AJO-Nachrichtenexport-Datensatz auswählen**.
   * Dateiformat: Wählen Sie JSON oder Parquet (wählen Sie eines, das auf nachgelagerten Tools basiert).
   * Zeitplan: Stellen Sie sicher, dass die Ausführung innerhalb des 3-tägigen Aufbewahrungsfensters erfolgt.

### Aktivieren des Nachrichtenexports in der Kanalkonfiguration {#config-message-export}

Um den Nachrichtenexport auf Ihre Kampagnen und Journey anzuwenden, müssen Sie die entsprechende Option auf der Kanalkonfigurationsebene aktivieren. Gehen Sie wie folgt vor.

1. Bearbeiten oder erstellen Sie [!DNL Journey Optimizer] die gewünschte E-Mail- oder SMS-[Kanalkonfiguration](channel-surfaces.md#create-channel-surface).

1. Wählen Sie die Option **[!UICONTROL Nachrichtenexport aktivieren]** aus.

   ![](assets/config-message-export.png)

1. Speichern Sie Ihre Änderungen und senden Sie Ihre Kanalkonfiguration.

E-Mail- und SMS-Nachrichten, die über Kampagnen oder Journey mit dieser Kanalkonfiguration gesendet werden, werden in den **AJO-Nachrichtenexport-Datensatz geschrieben**. Die Datensätze werden dann basierend auf dem von Ihnen definierten Exportdatenfluss an das ausgewählte Speicherziel exportiert.

Wenn Sie den Umschalter **[!UICONTROL Nachrichtenexport aktivieren]** deaktivieren, werden keine neuen Datensätze für diese Kanalkonfiguration in den Datensatz aufgenommen. Vorhandene Datensätze bleiben bis zum Ablauf der Aufbewahrung erhalten.


