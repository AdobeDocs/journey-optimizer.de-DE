---
title: Fallback-Angebote nachschlagen
description: Ein Fallback-Angebot wird an Kunden gesendet, wenn keine anderen Angebote für sie geeignet sind.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8f1fa116-30d2-4732-8973-bbce0dc66dec
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 32%

---

# Fallback-Angebote nachschlagen {#look-up-fallback-offers}

Sie können nach bestimmten Fallback-Angeboten suchen, indem Sie eine GET-Anfrage an die [!DNL Offer Library] API, die die Fallback-Angebots-ID im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Entität, die Sie nachschlagen möchten. | `fallbackOffer1234` |

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
