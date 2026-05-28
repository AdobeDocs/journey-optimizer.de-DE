---
solution: Journey Optimizer
product: journey optimizer
title: Zusätzliche Schritte zum Senden von Ereignissen an eine Journey
description: Erfahren Sie mehr über die zusätzlichen Schritte zum Senden von Ereignissen an eine Journey
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: Schritte, Konfiguration, Journey, Ereignisse, Stream, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
TQID: https://experienceleague.adobe.com/SiUXmerz2D-TYmIEXvaYk4usjRq67Y0v7V7sGVN-4vo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 95%

---

# Zusätzliche Schritte zum Senden von Ereignissen {#additional-steps-to-send-events}

Um Ereignisse zu konfigurieren, die an **[!UICONTROL Streaming-Aufnahme-APIs]** gesendet und in [!DNL Journey Optimizer] verwendet werden sollen, müssen Sie die folgenden Schritte ausführen:

1. Rufen Sie die Inlet-URL von Adobe Experience Platform-APIs ab. Weitere Informationen finden Sie unter [Übersicht über Streaming-Aufnahme-APIs](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=de){target="_blank"}.
1. Kopieren Sie die Payload aus der Payload-Vorschau im Menü **[!UICONTROL Ereignis]**. Weitere Informationen finden Sie auf [dieser Seite](../event/about-creating.md#define-the-payload-fields).

>[!IMPORTANT]
>
>Ereignisanforderungen und -beschränkungen (Streaming, Abfrage-Service, Batch-Aufnahme) finden Sie unter [Journey-Leitplanken - Ereignisse](../start/guardrails.md#events-g).

Konfigurieren Sie anschließend das Datensystem, das Ereignisse mithilfe der kopierten Payload an die Streaming-Aufnahme-APIs pusht:

1. Richten Sie einen POST-API-Aufruf zur URL der Streaming-Aufnahme-APIs ein (als Inlet bezeichnet).
1. Verwenden Sie die Payload, die Sie im Hauptteil („Datenabschnitt“) des API-Aufrufs aus [!DNL Journey Optimizer] zu den Streaming-Aufnahme-APIs kopiert haben. Unten finden Sie ein Beispiel
1. Legen Sie fest, von wo alle Variablen in der Payload abgerufen werden sollen. Beispiel: Wenn das Ereignis die Adresse vermitteln soll, wird in der eingefügten Payload &quot;address&quot;: &quot;string&quot; angezeigt. „string“ sollte durch die Variable ersetzt werden, die automatisch mit dem richtigen Wert ausgefüllt wird, nämlich mit der E-Mail-Adresse der Person, an die eine Nachricht gesendet werden soll. Beachten Sie, dass in der Payload-Vorschau im Abschnitt **[!UICONTROL Kopfzeile]** viele Werte automatisch ausgefüllt werden, was Ihre Arbeit erleichtern sollte.
1. Wählen Sie „application/json“ als Typ für den Hauptteil aus.
1. Übergeben Sie Ihre Organisations-ID in der Kopfzeile mit dem Schlüssel „x-gw-ims-org-id“. Verwenden Sie für den Wert Ihre Organisations-ID („XXX@AdobeOrg“).

Es folgt ein Beispiel für ein Streaming-Aufnahme-API-Ereignis:

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
            "timestamp": "2023-05-29T00:00:00.000Z",
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

Um die Identifikation der Stelle zu erleichtern, an der der „Daten“-Teil eingefügt werden soll, kann ein JSON-Visualisierungs-Tool verwendet werden, z. B. [JSON Formatter](https://jsonformatter.curiousconcept.com){target="_blank"}.

Informationen zur Fehlerbehebung bei Streaming-Aufnahme-APIs finden sich in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de){target="_blank"}.
