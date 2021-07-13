---
title: Zusätzliche Schritte zum Senden von Ereignissen an eine Journey
description: Erfahren Sie mehr über die zusätzlichen Schritte zum Senden von Ereignissen an eine Journey
feature: Ereignisse
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 84%

---

# Zusätzliche Schritte zum Senden von Ereignissen {#concept_xrz_n1q_y2b}

Um Ereignisse zu konfigurieren, die an **[!UICONTROL Streaming-Aufnahme-APIs]** gesendet und in [!DNL Journey Optimizer] verwendet werden sollen, müssen Sie die folgenden Schritte ausführen:

1. Rufen Sie die Inlet-URL von Adobe Experience Platform-APIs ab. Weitere Informationen finden Sie unter [Übersicht über Streaming-Aufnahme-APIs](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=de){target=&quot;_blank&quot;}.
1. Kopieren Sie die Payload aus der Payload-Vorschau im Menü **[!UICONTROL Ereignis]**. Weiterführende Informationen finden Sie auf [dieser Seite](../event/about-creating.md#define-the-payload-fields).

Konfigurieren Sie anschließend das Datensystem, das Ereignisse mithilfe der kopierten Payload an die Streaming-Aufnahme-APIs pusht:

1. Richten Sie einen POST-API-Aufruf zur URL der Streaming-Aufnahme-APIs ein (als Inlet bezeichnet).
1. Verwenden Sie die Payload, die Sie im Hauptteil („Datenabschnitt“) des API-Aufrufs aus [!DNL Journey Optimizer] zu den Streaming-Aufnahme-APIs kopiert haben. Unten finden Sie ein Beispiel
1. Legen Sie fest, von wo alle Variablen in der Payload abgerufen werden sollen. Beispiel: Wenn das Ereignis die Adresse vermitteln soll, wird in der eingefügten Payload &quot;address&quot;: &quot;string&quot; angezeigt. „string“ sollte durch die Variable ersetzt werden, die automatisch mit dem richtigen Wert ausgefüllt wird, nämlich mit der E-Mail-Adresse der Person, an die eine Nachricht gesendet werden soll. Beachten Sie, dass in der Payload-Vorschau im Abschnitt **[!UICONTROL Kopfzeile]** viele Werte automatisch ausgefüllt werden, was Ihre Arbeit erleichtern sollte.
1. Wählen Sie „application/json“ als Typ für den Hauptteil aus.
1. Übergeben Sie Ihre IMS-Organisations-ID in der Kopfzeile mit dem Schlüssel „x-gw-ims-org-id“. Verwenden Sie für den Wert Ihre IMS-Organisations-ID („XXX@AdobeOrg“).

Im Folgenden finden Sie ein Beispiel für ein Streaming-Aufnahme-API-Ereignis:

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

Um die Identifizierung des Ortes zu erleichtern, an dem der Teil &quot;Daten&quot;eingefügt werden soll, können Sie ein JSON-Visualisierungs-Tool verwenden, z. B. [JSON-Formatierer](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}.

Informationen zur Fehlerbehebung bei Streaming-Aufnahme-APIs finden Sie in der [Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de){target=&quot;_blank&quot;}.
