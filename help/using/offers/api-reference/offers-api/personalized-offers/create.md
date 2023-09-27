---
title: Personalisiertes Angebot erstellen
description: Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 60%

---

# Personalisiertes Angebot erstellen {#create-personalized-offer}

Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.

Sie können ein personalisiertes Angebot erstellen, indem Sie eine POST-Anfrage an die [!DNL Offer Library] API.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, aus denen die *Content-Type* -Feld in der Anfragekopfzeile:

| Header-Name | Wert |
| ----------- | ----- |
| Inhaltstyp | `application/json` |
| Inhaltstyp | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps/` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
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
}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details des neu erstellten personalisierten Angebots zurückgegeben, einschließlich der ID. Sie können die `id` in späteren Schritten, um Ihr personalisiertes Angebot zu aktualisieren oder zu löschen.

```json
{
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Einschränkungen {#limitations}

Angebotsdarstellungen und einige Angebotsbeschränkungen werden derzeit nicht mit den mobilen [!DNL Experience Edge]-Workflows unterstützt, zum Beispiel `Capping`. Der Wert des Feldes `Capping` gibt an, wie oft ein Angebot allen Benutzern angezeigt werden kann. Weitere Informationen finden Sie in der [Dokumentation zu Angebotseignungsregeln und Einschränkungen](../../../offer-library/creating-personalized-offers.md).