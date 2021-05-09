---
title: Zusätzliche Schritte zum Senden von Ereignissen an eine Journey
description: Weitere Schritte zum Senden von Ereignissen an eine Journey
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Zusätzliche Schritte zum Senden von Ereignissen {#concept_xrz_n1q_y2b}

![](../assets/do-not-localize/badge.png)

Um Ereignis zu konfigurieren, die an **[!UICONTROL Streaming Ingestion APIs]** gesendet und in [!DNL Journey Optimizer] verwendet werden sollen, müssen Sie die folgenden Schritte ausführen:

1. Rufen Sie die Einlass-URL von Adobe Experience Platform-APIs ab. Weitere Informationen finden Sie unter [Übersicht über Streaming Ingestion APIs](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html).
1. Kopieren Sie die Nutzlast aus der Payload-Vorschau im Menü **[!UICONTROL Ereignis]**. Weitere Informationen finden Sie auf [dieser Seite](../event/about-creating.md#define-the-payload-fields).

Anschließend müssen Sie das Datensystem konfigurieren, das Ereignis mithilfe der kopierten Nutzlast an Streaming Ingestion APIs sendet:

1. Richten Sie einen POST-API-Aufruf an die Streaming-Einschluss-APIs-URL ein (als Einlass bezeichnet).
1. Verwenden Sie die Nutzlast, die Sie von [!DNL Journey Optimizer] im Hauptteil (&quot;Datenabschnitt&quot;) des API-Aufrufs für Streaming Ingestion APIs kopiert haben. Beispiel siehe unten
1. Legen Sie fest, wo alle Variablen in der Nutzlast abgelegt werden sollen. Beispiel: Wenn das Ereignis die Adresse übermitteln soll, zeigt die eingefügte Nutzlast &quot;Adresse&quot; an: &quot;string&quot;. &quot;string&quot; sollte durch die Variable ersetzt werden, die automatisch den richtigen Wert ausfüllt, die E-Mail der Person, an die eine Nachricht gesendet werden soll. Beachten Sie, dass in der Payload-Vorschau im Abschnitt **[!UICONTROL Kopfzeile]** viele Werte automatisch ausgefüllt werden, die Ihre Arbeit erleichtern sollen.
1. Wählen Sie &quot;application/json&quot;als Texttyp.
1. Geben Sie Ihre IMS-Organisations-ID im Header mit dem Schlüssel &quot;x-gw-ims-org-id&quot;weiter. Verwenden Sie für diesen Wert Ihre IMS-Organisations-ID (&quot;XXX@AdobeOrg&quot;).

Im Folgenden finden Sie ein Ereignis zu Streaming Ingestion APIs:

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

Um die Identifizierung des Ortes zu erleichtern, an dem der Teil &quot;Daten&quot;eingefügt werden soll, können Sie ein JSON-Visualisierungstool wie [https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com) verwenden.

Informationen zur Fehlerbehebung bei Streaming Ingestion APIs finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html).
