---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer Live-Aktivitätsnachricht
description: Erfahren Sie, wie Sie eine Live-Aktivität in Journey Optimizer erstellen
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bfd36dddb5795cd8b6eeb164f70b6cf3fdcb5750
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 23%

---

# Erstellen einer Live-Aktivität {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Erste Schritte mit Live-Aktivitäten](get-started-mobile-live.md)
* [Konfiguration der Live-Aktivität](mobile-live-configuration.md)
* [Live-Aktivitätsintegration mit Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* **[Live-Aktivität erstellen](create-mobile-live.md)**
* [Häufig gestellte Fragen](mobile-live-faq.md)
* [Live-Kampagnenbericht](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Nachdem Sie Ihre Mobile-Konfiguration konfiguriert und Ihre Adobe Experience Platform Mobile SDK implementiert haben, können Sie mit der Erstellung Ihrer Live-Aktivität in Journey Optimizer beginnen:

1. Rufen Sie das Menü **[!UICONTROL Kampagnen]** auf und klicken Sie auf **[!UICONTROL Kampagne erstellen]**.

1. Wählen Sie den Kampagnentyp **API-ausgelöst** aus.

   * Wählen Sie **API-ausgelöstes Marketing** für zielgruppenbasierte Kampagnen aus.

   * Wählen Sie **API-ausgelöste Transaktion** für einzelne Kampagnen aus.

   >[!IMPORTANT]
   >
   > Beachten Sie, dass für **API-ausgelöste Transaktion** die Option **[!UICONTROL Hoher Durchsatz]** nicht aktiviert werden sollte.

   ![](assets/create-live-1.png)

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Wählen Sie im **[!UICONTROL Aktionen]** die Option **[!UICONTROL Live-Aktivität]** und wählen oder erstellen Sie eine neue Konfiguration.

   Weitere Informationen zur Konfiguration von Live-Aktivitäten finden Sie [&#x200B; (dieser Seite](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Klicken Sie auf **[!UICONTROL Experiment erstellen]**, um mit der Konfiguration Ihres Inhaltsexperiments zu beginnen und Abwandlungen zu erstellen, deren Performance zu messen und die beste Option für Ihre Zielgruppe zu ermitteln. [Weitere Informationen](../content-management/content-experiment.md)

1. Wählen Sie auf der Registerkarte **[!UICONTROL Audience]** Ihren **[!UICONTROL Identitätstyp]** [Weitere Informationen](../audience/about-audiences.md).

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie in [diesem Abschnitt](../campaigns/create-campaign.md#schedule), wie Sie den **[!UICONTROL Zeitplan]** der Kampagne konfigurieren können.

1. Klicken Sie nach der Konfiguration **[!UICONTROL Zum Aktivieren überprüfen]** und klicken Sie dann auf **[!UICONTROL Aktivieren]**.

1. Nachdem die Kampagne aktiviert wurde, verwenden Sie die bereitgestellte **cURL-Anfrage** als Vorlage für den Trigger von Live-Aktivitätsereignissen zum Starten, Aktualisieren oder Beenden. Aktualisieren Sie die Beispiel-Payload vor der Ausführung mit Ihren spezifischen Daten.

   Stellen Sie sicher, dass Sie auch die **[!UICONTROL Kampagnen-ID]**-Kennungen kopieren, die in Ihre Payload aufgenommen werden sollen.

   ➡️ Informationen zu Authentifizierungsanforderungen, einschließlich OAuth[Token und API-Schlüsseln, finden Sie in der Dokumentation &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) API-ausgelöste Kampagnen .

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

Nachdem Sie Ihre Live-Aktivität entworfen haben, können Sie mit integrierten Berichten [&#x200B; Wirkung Ihrer Live-Aktivität &#x200B;](../reports/campaign-global-report-cja-activity.md).
