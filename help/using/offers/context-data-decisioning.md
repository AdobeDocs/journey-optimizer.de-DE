---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Kontextdaten und Entscheidungsanfragen
description: Erfahren Sie, wie Sie Kontextdaten in Entscheidungsanfragen übergeben.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Kontextdaten und Entscheidungsanfragen {#context-data-decisioning}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md)

Dieser Abschnitt erläutert das Übergeben von Kontextdaten in Entscheidungsanfragen und deren Verwendung in Eignungsregeln.

>[!BEGINSHADEBOX]

Darüber hinaus können Sie auch den Kontext in **Rangfolgeformeln** nutzen, um Ihre Angebote zu verstärken. Detaillierte Beispiele für Rangfolgeformeln, die Kontextdaten nutzen, finden Sie in [diesem Abschnitt](../offers/ranking/create-ranking-formulas.md#context-data).

>[!ENDSHADEBOX]

## Übergeben von Kontextdaten in Entscheidungsanfragen

Kontextdaten in Entscheidungsanfragen werden mithilfe des Schlüssels `xdm:ContextData` definiert.

Kontextdatenattribute werden nicht vom XDM-Schema gesteuert. Sie können beliebige Kontextdaten in JSON als Teil der Payload der Entscheidungsanfrage übergeben.

Im Folgenden finden Sie ein Beispiel für eine Entscheidungsanfrage mit Kontextdaten (siehe `xdm:ContextData`):

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## Verwenden von Kontextdaten in Eignungsregeln

Im Folgenden finden Sie Beispiele, die veranschaulichen, wie Kontextdaten verwendet werden, die in Entscheidungsanfragen in Eignungsregeln übergeben werden.

* Geeignet, wenn die Kontextdatenfunktionen einen bestimmten Wert enthalten:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* Geeignet, wenn der Kanal nicht leer und mit „Mobile“ identisch ist:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
