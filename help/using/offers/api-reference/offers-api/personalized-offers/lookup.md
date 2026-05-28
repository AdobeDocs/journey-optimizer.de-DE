---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Suchen eines personalisierten Angebots
description: Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 2e30b155-688b-432b-a703-d09de12ebdfd
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/fo34tWzFmKLEChraPGv6MppJq0hp6u2HhrUUXpXjpZA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 100%

---

# Suchen eines personalisierten Angebots {#look-up-personalized-offer}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../experience-decisioning/gs-experience-decisioning.md)


Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.

Sie können spezifische personalisierte Angebote nachschlagen, indem Sie eine GET-Anfrage an die [!DNL Offer Library]-API richten, die die personalisierte Angebots-ID im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Identität, die Sie nachschlagen möchten. | `personalizedOffer1234` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details des personalisierten Angebots zurückgegeben, einschließlich Informationen zu Ihrem einzigartigen personalisierten Angebot `id`.

```json
{
    "created": "2023-05-15T14:35:16.781+00:00",
    "modified": "2023-05-15T14:38:26.691+00:00",
    "etag": 2,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.15"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "personalizedOffer1234",
    "name": "Test personalized offer with frequency constraint",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "html",
                    "format": "text/html",
                    "language": [
                        "en-us"
                    ],
                    "content": "Hello You qualify for our Discount of 60%"
                }
            ]
        }
    ],
    "selectionConstraint": {
        "startDate": "2022-07-27T05:00:00.000+00:00",
        "endDate": "2023-07-29T05:00:00.000+00:00",
        "profileConstraintType": "none"
    },
    "rank": {
        "priority": 0
    },
    "cappingConstraint": {},
    "frequencyCappingConstraints": [
        {
            "enabled": false,
            "limit": 1,
            "startDate": "2023-05-15T14:25:49.622+00:00",
            "endDate": "2023-05-25T14:25:49.622+00:00",
            "scope": "global",
            "entity": "offer",
            "repeat": {
                "enabled": false,
                "unit": "month",
                "unitCount": 1
            }
        }
    ]
}
```
