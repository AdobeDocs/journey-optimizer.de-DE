---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Kontextdaten und Entscheidungsanfragen
description: Erfahren Sie, wie Sie Kontextdaten in Entscheidungsanfragen übergeben.
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/QQgN8UHq26U37o902TwS4p33TMYEUPg5A-i2AYLbOwI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: c132d929-fa62-4271-803e-b823be07b914
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 100%

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
