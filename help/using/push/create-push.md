---
solution: Journey Optimizer
product: journey optimizer
title: Push-Benachrichtigung konfigurieren
description: Erfahren Sie, wie Sie in Journey Optimizer eine Push-Benachrichtigung erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Push-Benachrichtigung erstellen {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="Erstellung von Push-Nachrichten"
>abstract="Fügen Sie Ihre Push-Nachricht hinzu und personalisieren Sie sie mit dem Ausdruckseditor."

## Push-Benachrichtigung in einer Journey oder Kampagne erstellen {#create}

Gehen Sie wie folgt vor, um eine Push-Benachrichtigung zu erstellen:

>[!BEGINTABS]

>[!TAB Hinzufügen eines Push zu einer Journey]

1. Öffnen Sie Ihre Journey und ziehen Sie eine Push-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.

   ![](assets/push_create_1.png)

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >Wenn Sie eine Push-Benachrichtigung von einer Journey aus senden, können Sie die Sendezeitoptimierungsfunktion von Adobe Journey Optimizer nutzen, um die beste Sendezeit für die Nachricht vorherzusagen und so die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. [Erfahren Sie, wie Sie mit der Sendezeitoptimierung arbeiten.](../building-journeys/journeys-message.md#send-time-optimization)

   Weitere Informationen zum Konfigurieren einer Journey finden Sie unter [diese Seite](../building-journeys/journey-gs.md)

1. Klicken Sie im Bildschirm für die Journey-Konfiguration auf die **[!UICONTROL Edit content]** Schaltfläche zum Konfigurieren des Push-Inhalts. [Push-Benachrichtigung erstellen](design-push.md)

1. Sobald der Nachrichteninhalt definiert wurde, können Sie mithilfe von Testprofilen die Vorschau anzeigen und testen.

1. Wenn Ihre Push-Benachrichtigung fertig ist, schließen Sie die Konfiguration Ihrer [Journey](../building-journeys/journey-gs.md) , um es zu versenden.

   Um das Verhalten Ihrer Empfänger über Push-Öffnungen und/oder Interaktionen zu verfolgen, stellen Sie sicher, dass die dedizierten Optionen im Tracking-Abschnitt im Abschnitt [E-Mail-Aktivität](../building-journeys/journeys-message.md).

>[!TAB Hinzufügen einer Push-Benachrichtigung zu einer Kampagne]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL Push notification]** als Aktion und wählen Sie die **[!UICONTROL App surface]** verwendet werden. [Weitere Informationen zur Push-Konfiguration](push-configuration.md).

   ![](assets/push_create_3.png)

1. Klicken **[!UICONTROL Create]**.

1. Aus dem **[!UICONTROL Properties]** bearbeiten, bearbeiten Sie die **[!UICONTROL Title]** und **[!UICONTROL Description]**.

   ![](assets/push_create_4.png)

1. Klicken Sie auf **[!UICONTROL Select audience]** -Schaltfläche, um die Zielgruppe zu definieren, die aus der Liste der verfügbaren Adobe Experience Platform-Segmente ausgewählt werden soll. [Weitere Infos](../segment/about-segments.md).

1. Im **[!UICONTROL Identity namespace]** wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren. [Weitere Infos](../event/about-creating.md#select-the-namespace).

   ![](assets/push_create_5.png)

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie die **[!UICONTROL Schedule]** der Kampagne in [diesem Abschnitt](../campaigns/create-campaign.md#schedule).

1. Aus dem **[!UICONTROL Action triggers]** Menü, wählen Sie die **[!UICONTROL Frequency]** Ihrer Push-Benachrichtigung:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monatlich

1. Klicken Sie im Konfigurationsbildschirm der Kampagne auf die Schaltfläche **[!UICONTROL Edit content]** Schaltfläche zum Konfigurieren des Push-Inhalts. [Push-Benachrichtigung erstellen](design-push.md)

1. Sobald der Nachrichteninhalt definiert wurde, können Sie mithilfe von Testprofilen die Vorschau anzeigen und testen.

1. Wenn Ihre Push-Benachrichtigung fertig ist, schließen Sie die Konfiguration Ihrer [Kampagne](../campaigns/create-campaign.md) , um es zu versenden.

   Um das Verhalten Ihrer Empfänger über Push-Öffnungen und/oder Interaktionen zu verfolgen, stellen Sie sicher, dass die dedizierten Optionen im Tracking-Abschnitt im Abschnitt [Kampagne](../campaigns/create-campaign.md).

>[!ENDTABS]

**Verwandte Themen**

* [Push-Kanal konfigurieren](push-gs.md)
* [Hinzufügen einer Nachricht in einer Journey](../building-journeys/journeys-message.md)

## Schnellbereitstellungsmodus {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="Schnellbereitstellungsmodus"
>abstract="Im Modus Schnellversand können Sie Hochgeschwindigkeits-Nachrichten an Push-Kanäle mit einer Zielgruppengröße von unter 30 M senden."

Der Modus für den schnellen Versand, der in Journeys zuvor als Burst-Modus bezeichnet wurde, ist ein [!DNL Journey Optimizer] -Add-on, das den sehr schnellen Versand von Push-Nachrichten in großen Mengen durch Kampagnen ermöglicht.

Schneller Versand wird verwendet, wenn eine Verzögerung beim Nachrichtenversand geschäftskritisch ist, wenn Sie eine dringende Push-Benachrichtigung auf Mobiltelefone senden möchten, z. B. eine brechende Nachricht an Benutzer, die Ihre News-Kanal-App installiert haben.

Weitere Informationen zur Leistung bei Verwendung des Rapid-Versandmodus finden Sie unter [Produktbeschreibung für Adobe Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

### Voraussetzungen {#prerequisites}

Der schnelle Versand von Nachrichten umfasst die folgenden Anforderungen:

* Eine schnelle Bereitstellung ist verfügbar für **[!UICONTROL Scheduled]** nur Kampagnen und nicht für API-gesteuerte Kampagnen verfügbar sind,
* In der Push-Nachricht ist keine Personalisierung zulässig.
* Die Zielgruppe muss weniger als 30 Millionen Profile enthalten.
* Im Modus Schneller Versand können Sie bis zu fünf Kampagnen gleichzeitig ausführen.

### Aktivieren des Modus für schnelle Bereitstellung

1. Erstellen Sie eine Push-Benachrichtigungskampagne und aktivieren Sie die **[!UICONTROL Rapid delivery]** -Option.

![](assets/create-campaign-burst.png)

1. Konfigurieren Sie den Nachrichteninhalt und wählen Sie die Zielgruppe aus. [Erfahren Sie, wie Sie eine Kampagne erstellen](#create)

   >[!IMPORTANT]
   >
   >Stellen Sie sicher, dass der Nachrichteninhalt keine Personalisierung enthält und dass die Audience weniger als 30 Millionen Profile enthält.

1. Überprüfen und aktivieren Sie Ihre Kampagne wie gewohnt. Beachten Sie, dass Nachrichten im Testmodus nicht über den Modus Schneller Versand gesendet werden.