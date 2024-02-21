---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer SMS-Nachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine SMS-Nachricht erstellen.
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: f275820c3f79bb4c9aca8593c2c761ccd4283795
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 89%

---

# Erstellen einer Textnachricht {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Erstellen einer Textnachricht"
>abstract="Um eine Textnachricht zu erstellen, fügen Sie eine SMS-Aktion in eine Journey oder Kampagne ein und beginnen Sie mit der Personalisierung mit dem Ausdruckseditor."

Sie können Text (SMS) mit Adobe Journey Optimizer entwerfen und versenden. Sie müssen zunächst eine SMS-Aktion in eine Journey oder eine Kampagne einfügen und dann den Inhalt der Textnachricht definieren, wie unten beschrieben. Adobe Journey Optimizer bietet auch die Möglichkeit, Ihre Textnachrichten vor dem Versand zu testen, sodass Sie das Rendering, die Personalisierungsattribute und alle anderen Einstellungen überprüfen können.

>[!NOTE]
>
>In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketing-Nachrichten eine Möglichkeit für die Empfänger enthalten, ihr Abo einfach zu kündigen. Zu diesem Zweck können SMS-Empfänger mit Keywords zum Opt-in oder Opt-out antworten. [Informationen über die Verwaltung des Opt-outs](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)


## Hinzufügen einer Textnachricht {#create-sms-journey-campaign}

Auf den folgenden Registerkarten erfahren Sie, wie Sie eine Textnachricht zu einer Kampagne oder einer Journey hinzufügen.

>[!BEGINTABS]

>[!TAB Hinzufügen einer Textnachricht zu einer Journey]

1. Öffnen Sie Ihre Journey und ziehen Sie eine SMS-Aktivität aus dem Abschnitt **Aktionen** der Palette.

   ![](assets/sms_create_1.png)

1. Geben Sie allgemeine Informationen (Titel, Beschreibung, Kategorie) zu Ihrer Nachricht ein und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.

   ![](assets/sms_create_2.png)

   Weitere Informationen zur Konfiguration der Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

   Das Feld **[!UICONTROL Oberfläche]** ist standardmäßig mit der letzten Oberfläche für den Kanal vorausgefüllt, den die Benutzerin oder der Benutzer verwendet hat.

Sie können jetzt mit der Erstellung des Inhalts Ihrer SMS-Nachricht beginnen, indem Sie die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** anklicken, wie unten beschrieben.

>[!TAB Hinzufügen einer Textnachricht zu einer Kampagne]

1. Erstellen Sie eine neue geplante oder durch eine API ausgelöste Kampagne. Wählen Sie **[!UICONTROL SMS]** als Aktion und anschließend die **[!UICONTROL Anwendungsoberfläche]**, die verwendet werden soll. Auf [dieser Seite](sms-configuration.md) erfahren Sie mehr über die SMS-Konfiguration.

   ![](assets/sms_create_3.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

   ![](assets/sms_create_4.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen zu definieren. [Weitere Informationen](../audience/about-audiences.md).

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen in der ausgewählten Zielgruppe verwendet werden soll. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Klicken Sie auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen und Abwandlungen zu erstellen, deren Performance zu messen und die beste Option für Ihre Zielgruppe zu ermitteln. [Weitere Informationen](../campaigns/content-experiment.md)

1. Im Bereich **[!UICONTROL Tracking von Aktionen]** können Sie angeben, ob Sie Klicks auf Links in Ihrer SMS-Nachricht verfolgen möchten.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

1. Wählen Sie aus dem Menü **[!UICONTROL Aktions-Trigger]** die **[!UICONTROL Häufigkeit]** Ihrer SMS-Nachricht:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monat

Sie können jetzt mit der Erstellung des Inhalts Ihrer Textnachricht beginnen, indem Sie die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** anklicken, wie unten beschrieben.

>[!ENDTABS]

## Definieren Ihres SMS-Inhalts{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Definieren Ihres SMS-Inhalts"
>abstract="Passen Sie Ihre Textnachrichten mithilfe des Ausdruckseditors an und personalisieren Sie sie, indem Sie den Inhalt definieren und dynamische Elemente einfügen."

Gehen Sie wie folgt vor, um Ihren SMS-Inhalt zu konfigurieren.

1. Klicken Sie auf dem Bildschirm der Journey- oder Kampagnenkonfiguration auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um den Inhalt der Textnachricht zu konfigurieren.

1. Klicken Sie auf das Feld **[!UICONTROL Nachricht]**, um den Ausdruckseditor zu öffnen.

   ![](assets/sms-content.png)

1. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren und Personalisierung sowie dynamischen Inhalt hinzuzufügen. Sie können jedes Attribut verwenden, wie etwa Profilname oder Stadt. Sie können auch bedingte Regeln definieren. Auf den folgenden Seiten erfahren Sie mehr über [Personalisierung](../personalization/personalize.md) und [dynamische Inhalte](../personalization/get-started-dynamic-content.md) im Ausdruckseditor.

1. Nach dem Definieren Ihres Inhalts können Sie das Verfolgen von URLs für Ihre Nachricht aktivieren. Rufen Sie dazu das Menü **[!UICONTROL Hilfsfunktionen]** auf und wählen Sie **[!UICONTROL Helfer]** aus.

   Beachten Sie, dass Sie zur Verwendung der URL-Kürzungsfunktion zunächst eine Subdomain konfigurieren müssen, die dann mit Ihrer Oberfläche verknüpft wird. [Weitere Informationen](sms-subdomains.md)

   >[!CAUTION]
   >
   > Um auf SMS-Subdomains zuzugreifen und sie zu bearbeiten, benötigen Sie die Berechtigung zum **[!UICONTROL Verwalten von SMS-Subdomains]** für die Produktions-Sandbox. Weitere Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/high-low-permissions.md).

   ![](assets/sms_tracking_1.png)

1. Klicken Sie innerhalb des Menüs **[!UICONTROL Hilfsfunktionen]** auf **[!UICONTROL URL-Funktion]** und wählen Sie dann **[!UICONTROL URL hinzufügen]** aus.

   ![](assets/sms_tracking_2.png)

1. Fügen Sie in das Feld `originalUrl` die URL ein, die gekürzt werden soll, und klicken Sie auf **[!UICONTROL Speichern]**.

1. Klicken Sie auf **[!UICONTROL Speichern]** und überprüfen Sie Ihre Nachricht in der Vorschau. Sie können nun den Inhalt Ihrer Nachricht testen und überprüfen, wie in [diesem Abschnitt](#sms-mms-test) beschrieben.

<!--
## Define your MMS content{#mms-content}

You can enhance your communication by sending Multimedia Message Service (MMS) messages, enabling the sharing of media such as videos, pictures, audio clips and GIFs, and more. Additionally, MMS allows for up to 1600 characters of text in your message.


>[!NOTE]
>
>* This feature is currently available with **Sinch** only.
>
>* MMS channel comes with a few limitations listed in [this page](../start/guardrails.md#sms-guardrails).
>

To create MMS content, follow these steps:

1. Create a SMS as described in [this section](#create-sms-journey-campaign).

1. Edit your SMS content as detailed in [this section](#sms-content).

1. Enable the MMS option to add media to your SMS content.

    ![](assets/sms_create_6.png)

1. Add a **[!UICONTROL Title]** to your media.

1. Enter the URL of your media in the **[!UICONTROL Media]** field.

    ![](assets/sms_create_7.png)

1. Click **[!UICONTROL Save]** and check your message in the preview. You can now test and check your message content as detailed below.
-->

## Testen und senden Ihrer Nachrichten {#sms-mms-test}

Verwenden Sie die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um eine Vorschau des Inhalts Ihrer Textnachrichten, der gekürzten URLs und der personalisierten Inhalte anzuzeigen.

![](assets/sms-content-preview.png)

Sobald Sie Ihre Tests durchgeführt und den Inhalt validiert haben, können Sie Ihre Textnachricht an Ihre Zielgruppe senden. Diese Schritte werden auf [dieser Seite](send-sms.md) im Detail beschrieben.

Nach dem Versand können Sie die Wirkung Ihrer SMS in den Kampagnen- oder Journey-Berichten messen. Weiterführende Informationen zum Reporting finden Sie in [diesem Abschnitt](../reports/campaign-global-report.md#sms-tab).

**Verwandte Themen**

* [Vorschau, Test und Versand Ihrer Textnachricht](send-sms.md)
* [Konfigurieren des SMS-Kanals](sms-configuration.md)
* [SMS-Berichte](../reports/journey-global-report.md#sms-global)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
* [Hinzufügen einer Nachricht in einer Kampagne](../campaigns/create-campaign.md)
