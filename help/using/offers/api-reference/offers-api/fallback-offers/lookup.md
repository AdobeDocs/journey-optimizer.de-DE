---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Fallback-Angebote nachschlagen
description: Ein Fallback-Angebot wird an Kunden gesendet, wenn keine anderen Angebote für sie geeignet sind.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 8f1fa116-30d2-4732-8973-bbce0dc66dec
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Z5tERXgh6YE9BWBwi-6Ok1tECp5SFJQUJj0MXMemt7Y
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 100%

---

# Suchen von Fallback-Angeboten {#look-up-fallback-offers}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../experience-decisioning/gs-experience-decisioning.md)


Sie können nach bestimmten Fallback-Angeboten suchen, indem Sie eine GET-Anfrage an die [!DNL Offer Library]-API richten, die die Fallback-Angebots-ID im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Identität, die Sie nachschlagen möchten. | `fallbackOffer1234` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details des Fallback-Angebots zurückgegeben, einschließlich Informationen zu Ihrem Fallback-Angebot und der eindeutigen Fallback-Angebots-ID.

```json
{
    "created": "2023-06-08T14:04:41.011+00:00",
    "modified": "2023-06-08T14:04:41.011+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "fallbackOffer1234",
    "name": "Fallback Offer Web",
    "description": "Fallback Offer Web Description",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "imagelink",
                    "format": "image/png",
                    "deliveryURL": "https://mysite.com"
                }
            ]
        }
    ]
}
```
