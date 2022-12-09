---
solution: Journey Optimizer
product: journey optimizer
title: SMS erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer eine SMS-Nachricht erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 34ab78408981d2b53736b31c94412da06cb860c4
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# SMS erstellen {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS-Erstellung"
>abstract="Fügen Sie Ihre Textnachricht hinzu und beginnen Sie mit der Personalisierung mit dem Ausdruckseditor."

>[!NOTE]
>
>In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketingnachrichten eine Möglichkeit für die Empfänger enthalten, sich einfach abzumelden. Zu diesem Zweck können SMS-Empfänger mit Opt-in- und Opt-out-Keywords antworten. [Erfahren Sie, wie Sie das Opt-out verwalten](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

## SMS-Nachrichten in einer Journey oder Kampagne erstellen {#create-sms-journey-campaign}

Gehen Sie wie folgt vor, um mit der Personalisierung Ihrer SMS zu beginnen:

>[!BEGINTABS]

>[!TAB Hinzufügen einer SMS-Nachricht zu einer Journey]

1. Öffnen Sie Ihre Journey und ziehen Sie eine SMS-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.

   ![](assets/sms_create_1.png)

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.

   ![](assets/sms_create_2.png)

   Weitere Informationen zum Konfigurieren einer Journey finden Sie unter [diese Seite](../building-journeys/journey-gs.md)

Sie können jetzt mit der Erstellung des Inhalts Ihrer SMS-Nachricht beginnen, indem Sie **[!UICONTROL Edit content]** Schaltfläche. [SMS-Inhalt gestalten](#sms-content)

>[!TAB Eine SMS zu einer Kampagne hinzufügen]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL SMS]** als Aktion und wählen Sie die **[!UICONTROL App surface]** verwendet werden. [Weitere Informationen zur SMS-Konfiguration](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Klicken **[!UICONTROL Create]**.

1. Aus dem **[!UICONTROL Properties]** bearbeiten, bearbeiten Sie die **[!UICONTROL Title]** und **[!UICONTROL Description]**.

   ![](assets/sms_create_4.png)

1. Im **[!UICONTROL Actions tracking]** angeben, ob Sie Klicks auf Links in Ihrer SMS-Nachricht verfolgen möchten.

1. Klicken Sie auf **[!UICONTROL Select audience]** -Schaltfläche, um die Zielgruppe zu definieren, die aus der Liste der verfügbaren Adobe Experience Platform-Segmente ausgewählt werden soll. [Weitere Infos](../segment/about-segments.md).

1. Im **[!UICONTROL Identity namespace]** wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren. [Weitere Infos](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie die **[!UICONTROL Schedule]** der Kampagne in [diesem Abschnitt](../campaigns/create-campaign.md#schedule).

1. Aus dem **[!UICONTROL Action triggers]** Menü, wählen Sie die **[!UICONTROL Frequency]** Ihrer SMS-Nachricht:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monat

Sie können jetzt mit der Erstellung des Inhalts Ihrer SMS-Nachricht beginnen, indem Sie **[!UICONTROL Edit content]** Schaltfläche. [SMS-Inhalt gestalten](#sms-content)

>[!ENDTABS]

## SMS-Inhalt definieren{#sms-content}

1. Klicken Sie im Konfigurationsbildschirm der Journey oder Kampagne auf das **[!UICONTROL Edit content]** Schaltfläche zum Konfigurieren des SMS-Inhalts.

1. Klicken Sie auf **[!UICONTROL Message]** -Feld, um den Ausdruckseditor zu öffnen.

   ![](assets/sms-content.png)

1. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren und dynamische Inhalte hinzuzufügen. Sie können jedes beliebige Attribut verwenden, z. B. den Profilnamen oder die Stadt. Weitere Informationen [Personalisierung](../personalization/personalize.md) und [dynamischer Inhalt](../personalization/get-started-dynamic-content.md) im Ausdruckseditor.

1. Klicken **[!UICONTROL Save]** und überprüfen Sie Ihre Nachricht in der Vorschau. [Weitere Infos](send-sms.md)

   ![](assets/sms-content-preview.png)

**Verwandte Themen**

* [SMS-Kanal konfigurieren](sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Hinzufügen einer Nachricht in einer Journey](../building-journeys/journeys-message.md)
