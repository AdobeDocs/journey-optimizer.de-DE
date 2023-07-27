---
title: Erstellen einer In-App-Benachrichtigung
description: Erfahren Sie, wie Sie in Journey Optimizer eine In-App-Nachricht
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: In-App, Nachricht, Erstellung, Starten
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 57%

---

# Erstellen einer In-App-Nachricht {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Wählen Sie im Abschnitt **[!UICONTROL Eigenschaften]** den Ausführungstyp der Kampagne aus: Geplant oder API-ausgelöst. Weitere Informationen zu Kampagnentypen finden Sie auf [dieser Seite](../campaigns/create-campaign.md#campaigntype).

1. Wählen Sie im Bereich **[!UICONTROL Aktionen]** die **[!UICONTROL In-App-Nachricht]** und die **[!UICONTROL Programmoberfläche]** aus, die Sie zuvor für Ihre In-App-Nachricht konfiguriert haben. Klicken Sie dann auf **[!UICONTROL Erstellen]**.

   Erfahren Sie mehr über In-App-Konfiguration auf [dieser Seite](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Geben Sie im Abschnitt **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** ein.

1. Um der In-App-Nachricht benutzerdefinierte oder Core-Datennutzungskennzeichnungen zuzuweisen, wählen Sie **[!UICONTROL Zugang verwalten]** aus. [Weitere Informationen](../administration/object-based-access.md).

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Zielgruppen zu definieren. [Weitere Informationen](../audience/about-audiences.md).

   ![](assets/in_app_create_2.png)

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen in der ausgewählten Zielgruppe verwendet werden soll. [Weitere Informationen](../event/about-creating.md#select-the-namespace).

1. Klicken Sie auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen und Abwandlungen zu erstellen, deren Leistung zu messen und die beste Option für Ihre Zielgruppe zu ermitteln. [Weitere Informationen](../campaigns/content-experiment.md)

1. Klicken Sie auf **[!UICONTROL Trigger bearbeiten]**, um die Ereignisse und Kriterien auszuwählen, die Ihre Nachricht auslösen sollen. Mit Rule Builder können Benutzer Kriterien und Werte angeben, die, wenn sie erfüllt sind, eine Reihe von Aktionen Trigger geben, z. B. das Senden einer In-App-Nachricht.

   1. Klicken Sie auf die Ereignis-Dropdown-Liste, um Ihren Trigger bei Bedarf zu ändern.

   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Bedingung hinzufügen]**, wenn Sie möchten, dass der Trigger mehrere Ereignisse oder Kriterien berücksichtigt.

   1. Wählen Sie die **[!UICONTROL Oder]** -Bedingung, wenn Sie weitere hinzufügen möchten **[!UICONTROL Trigger]** , um Ihre Regel weiter zu erweitern.

      ![](assets/in_app_create_3.png)

   1. Wählen Sie die **[!UICONTROL und]** -Bedingung, wenn Sie **[!UICONTROL Eigenschaften]** und passen Sie Ihre Regel besser an.

      ++ + Anzeigen der verfügbaren Eigenschaften.

      | Package | Eigenschaften  | Definition |
      |---|---|---|
      | Geräteinformationen | Betreibername | Wird ausgelöst, wenn einer der Betreibernamen aus der Liste erfüllt ist. |
      | Geräteinformationen | Gerätename | Wird ausgelöst, wenn einer der Gerätenamen erfüllt ist. |
      | Geräteinformationen | Gebietsschema | Wird ausgelöst, wenn eine der Sprachen aus der Liste erfüllt ist. |
      | Geräteinformationen | Betriebssystemversion | Wird ausgelöst, wenn eine der angegebenen Betriebssystemversionen erfüllt ist. |
      | Geräteinformationen | Vorherige Betriebssystemversion | Wird ausgelöst, wenn eine der angegebenen vorherigen Betriebssystemversionen erfüllt ist. |
      | Geräteinformationen | Ausführungsmodus | Wird ausgelöst, wenn der Ausführungsmodus entweder eine Anwendung oder eine Erweiterung ist. |
      | Anwendungslebenszyklus | App-ID | Wird ausgelöst, wenn die angegebene App-ID erfüllt ist. |
      | Anwendungslebenszyklus | Wochentag | Wird ausgelöst, wenn der angegebene Wochentag erfüllt ist. |
      | Anwendungslebenszyklus | Tag seit der ersten Benutzung | Wird ausgelöst, wenn die angegebene Anzahl von Tagen seit der ersten Verwendung erreicht ist. |
      | Anwendungslebenszyklus | Tag seit der letzten Verwendung | Wird ausgelöst, wenn die angegebene Anzahl von Tagen seit der letzten Verwendung erreicht ist. |
      | Anwendungslebenszyklus | Tag seit der Aktualisierung | Wird ausgelöst, wenn die angegebene Anzahl von Tagen seit der letzten Aktualisierung erreicht ist. |
      | Anwendungslebenszyklus | Installationsdatum | Wird ausgelöst, wenn das angegebene Installationsdatum erreicht ist. |
      | Anwendungslebenszyklus | Starts | Wird ausgelöst, wenn die angegebene Anzahl von Launches erreicht ist. |
      | Anwendungslebenszyklus | Tageszeit | Wird ausgelöst, wenn die angegebene Tageszeit erreicht ist. |
      | Places | Aktueller POI | Wird vom Places-SDK ausgelöst, wenn Ihr Kunde den festgelegten Zielpunkt (Point of Interest, POI) aufruft. |
      | Places | Zuletzt eingegebener POI | Wird vom Places SDK ausgelöst, je nachdem, welcher Zielpunkt (Point of Interest, POI) zuletzt von Ihrem Kunden eingegeben wurde. |
      | Places | Letzter ausgenommener POI | Wird vom Places-SDK ausgelöst, je nachdem, welcher Zielpunkt (Point of Interest, POI) vom Kunden zuletzt verlassen wurde. |

+++

      ![](assets/in_app_create_8.png)

   1. Klicken Sie auf **[!UICONTROL Gruppe erstellen]**, um Trigger zu gruppieren.

1. Wählen Sie die Häufigkeit Ihres Auslösers aus, wenn Ihre In-App-Nachricht aktiv ist. Die folgenden Optionen sind verfügbar:

   * **[!UICONTROL Immer]**: Die Nachricht wird immer angezeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten.
   * **[!UICONTROL Einmal anzeigen]**: Die Nachricht wird nur beim ersten Mal angezeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten.
   * **[!UICONTROL Bis zu Clickthrough]**: Diese Nachricht wird anzeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten, bis vom SDK ein Interaktionsereignis mit der Aktion „Angeklickt“ übermittelt wird.
   * **[!UICONTROL X-mal]**: Diese Nachricht wird X-mal angezeigt.

1. Wählen Sie bei Bedarf aus, an welchem **[!UICONTROL Wochentag]** oder zu welcher **[!UICONTROL Tageszeit]** die In-App-Nachricht angezeigt wird.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

   ![](assets/in-app-schedule.png)

1. Sie können jetzt über die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** mit der Erstellung Ihrer Inhalte beginnen. [Weitere Informationen](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## Anleitungsvideos{#video}

* Das folgende Video zeigt, wie Sie In-App-Nachrichten in Ihren Kampagnen erstellen, konfigurieren und veröffentlichen können.

  +++Siehe Video
  >[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)
+++

* Erfahren Sie im folgenden Video, wie Sie Inhaltsexperimente konfigurieren und analysieren, um In-App-Nachrichten mit A/B-Tests zu testen.

  +++Siehe Video
  >[!VIDEO](https://video.tv.adobe.com/v/3419898)
+++


**Verwandte Themen:**

* [Entwerfen der In-App-Nachricht](design-in-app.md)
* [Testen und Senden der In-App-Nachricht](send-in-app.md)
* [In-App-Bericht](../reports/campaign-global-report.md#inapp-report)
* [In-App-Konfiguration](inapp-configuration.md)