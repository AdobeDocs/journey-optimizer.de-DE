---
solution: Journey Optimizer
product: journey optimizer
title: Zusätzliche Schritte zum Senden von Ereignissen an eine Journey
description: Zusätzliche Schritte zum Senden von Ereignissen an eine Journey
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Zusätzliche Schritte zum Senden von Ereignissen {#additional-steps-to-send-events}

So konfigurieren Sie Ereignisse, die an gesendet werden **[!UICONTROL Streaming Ingestion APIs]** und in [!DNL Journey Optimizer]müssen Sie die folgenden Schritte ausführen:

1. Rufen Sie die Inlet-URL von Adobe Experience Platform-APIs ab. Weitere Informationen finden Sie unter [Übersicht über Streaming-Aufnahme-APIs](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target=&quot;_blank&quot;}.
1. Kopieren Sie die Payload aus der Payload-Vorschau in der **[!UICONTROL Event]** Menü. Weitere Informationen finden Sie unter [diese Seite](../event/about-creating.md#define-the-payload-fields).

Anschließend müssen Sie das Datensystem konfigurieren, das Ereignisse mithilfe der kopierten Payload an Streaming-Aufnahme-APIs sendet:

1. Richten Sie einen POST-API-Aufruf an die URL der Streaming-Aufnahme-APIs ein (als Inlet bezeichnet).
1. Verwenden Sie die Payload, aus der Sie kopiert haben [!DNL Journey Optimizer] im Hauptteil (&quot;Datenabschnitt&quot;) des API-Aufrufs zu Streaming-Aufnahme-APIs. Nachfolgend finden Sie ein Beispiel
1. Legen Sie fest, wo alle in der Payload vorhandenen Variablen abgerufen werden sollen. Beispiel: Wenn das Ereignis die Adresse vermitteln soll, zeigt die eingefügte Payload &quot;address&quot;: &quot;string&quot;. &quot;string&quot; sollte durch die Variable ersetzt werden, die automatisch den richtigen Wert enthält, die E-Mail der Person, an die eine Nachricht gesendet werden soll. Beachten Sie, dass in der Payload-Vorschau in der **[!UICONTROL Header]** -Abschnitt, werden viele Werte automatisch ausgefüllt, die Ihre Arbeit erleichtern sollen.
1. Wählen Sie &quot;application/json&quot;als Texttyp aus.
1. Übergeben Sie Ihre Organisations-ID in die Kopfzeile mit dem Schlüssel &quot;x-gw-ims-org-id&quot;. Verwenden Sie für den Wert Ihre Organisations-ID (&quot;XXX@AdobeOrg&quot;).

Im Folgenden finden Sie ein Beispiel für ein Streaming-Aufnahme-APIs -Ereignis:

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

Um die Identifizierung der Stelle zu erleichtern, an der der Teil &quot;Daten&quot;eingefügt werden soll, können Sie ein JSON-Visualisierungs-Tool verwenden, z. B. [JSON-Formatierung](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}.

Informationen zur Fehlerbehebung bei Streaming-Aufnahme-APIs finden Sie unter [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}.
