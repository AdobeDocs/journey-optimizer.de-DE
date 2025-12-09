---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer Live-Aktivitätsnachricht
description: Informationen zum Erstellen einer Live-Aktivität in Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bfd36dddb5795cd8b6eeb164f70b6cf3fdcb5750
workflow-type: ht
source-wordcount: '317'
ht-degree: 100%

---

# Erstellen einer Live-Aktivität {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Erste Schritte mit Live-Aktivitäten](get-started-mobile-live.md)
* [Konfiguration von Live-Aktivitäten](mobile-live-configuration.md)
* [Integration von Live-Aktivitäten mit Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* **[Erstellen einer Live-Aktivität](create-mobile-live.md)**
* [Häufig gestellte Fragen](mobile-live-faq.md)
* [Bericht zu Kampagnen mit Live-Aktivitäten](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Nachdem Sie Ihre Mobile-Konfiguration konfiguriert und Ihr Adobe Experience Platform Mobile SDK implementiert haben, können Sie mit der Erstellung Ihrer Live-Aktivität in Journey Optimizer beginnen:

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Wählen Sie den Kampagnentyp **Durch API ausgelöst** aus.

   * Wählen Sie **API-ausgelöst (Marketing)** für zielgruppenbasierte Kampagnen aus.

   * Wählen Sie **API-ausgelöst (Transaktion)** für einzelne Kampagnen aus.

   >[!IMPORTANT]
   >
   > Beachten Sie, dass für **API-ausgelöst (Transaktion)** die Option **[!UICONTROL Hoher Durchsatz]** nicht aktiviert werden sollte.

   ![](assets/create-live-1.png)

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Wählen Sie im Abschnitt **[!UICONTROL Aktionen]** die Option **[!UICONTROL Live-Aktivität]** und eine Konfiguration aus oder erstellen Sie eine neue Konfiguration.

   Weitere Informationen zur Konfiguration von Live-Aktivitäten finden Sie auf [dieser Seite](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Klicken Sie auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen und Abwandlungen zu erstellen, deren Performance zu messen und die beste Option für Ihre Zielgruppe zu ermitteln. [Weitere Informationen](../content-management/content-experiment.md)

1. Wählen Sie auf der Registerkarte **[!UICONTROL Zielgruppe]** Ihren **[!UICONTROL Identitätstyp]** aus. [Weitere Informationen](../audience/about-audiences.md).

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

1. Klicken Sie nach der Konfiguration auf **[!UICONTROL Zum Aktivieren überprüfen]** und dann auf **[!UICONTROL Aktivieren]**.

1. Verwenden Sie nach dem Aktivieren der Kampagne die bereitgestellte **cURL-Anfrage** als Vorlage, um Start-, Aktualisierungs- und Endereignisse für Live-Aktivitäten auszulösen. Aktualisieren Sie die Beispiel-Payload vor der Ausführung mit Ihren konkreten Daten.

   Stellen Sie sicher, dass Sie auch die **[!UICONTROL Kampagnen-ID]**-Kennungen kopieren, die in Ihre Payload aufgenommen werden sollen.

   ➡️ Informationen zu Authentifizierungspflichten, einschließlich OAuth-Token und API-Schlüsseln, finden Sie der [Dokumentation zu durch API ausgelösten Kampagnen](https://developer.adobe.com/journey-optimizer-apis/references/messaging/).

   ![](assets/create-live-3.png)

   +++ Beispiel einer einzelnen Payload

   Beachten Sie, dass die meisten Felder aus dem folgenden Payload-Beispiel obligatorisch sind. Nur `requestId`, `dismissal-date` und `alert` sind optional.

   ```json
   {
       "requestId": "your-request-id",
       "campaignId": "your-campaign-id",
       "recipients": [
   {
       "type": "aep",
       "userId": "testemail@gmail.com",
       "namespace": "email",
       "context": {
        "requestPayload": {
       "aps": {
       "content-available": 1,
       "timestamp": 1756984054,              // current epoch time
       "dismissal-date": 1756984084,         // optional – auto remove when event="end"
       "event": "update",                    // start | update | end
   
       // Fields from FoodDeliveryLiveActivityAttributes
       "content-state": {
         "orderStatus": "Delivered"
       },
   
       "attributes-type": "FoodDeliveryLiveActivityAttributes",
       "attributes": {
         "restaurantName": "Pizza",
         "liveActivityData": {
           "liveActivityID": "orderId1"       // customer reference ID
         }
       },
   
       "alert": {
         "title": "Order Delivered!",
         "body": "Your pizza has arrived."
       }
     }
   }
   }
   }
   ]
   }
   ```

   +++

Nachdem Sie Ihre Live-Aktivität entworfen haben, können Sie mit [integrierten Berichten](../reports/campaign-global-report-cja-activity.md) die Wirkung Ihrer Live-Aktivität messen.
