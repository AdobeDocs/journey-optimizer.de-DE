---
title: Nachschlagen eines Entscheidungselements
description: Entscheidungselemente sind Marketing-Angebote, die Sie erstellen und in Sammlungen und Katalogen organisieren können.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 8a4e09ec-57bc-48ad-b626-6a15ba987791
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 100%

---

# Nachschlagen eines Entscheidungselements {#lookup-decision-items}

Um nach bestimmten Entscheidungselementen zu suchen, stellen Sie eine GET-Anfrage an die Angebotsbibliothek-API, die die ID im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Identität, die Sie nachschlagen möchten. | `offerItem1234` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details des Entscheidungselements zurückgegeben.

```json
{
    "created": "2024-06-10T16:00:34.014Z",
    "modified": "2024-07-09T22:59:21.507Z",
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerItem5678",
    "_experience": {
        "decisioning": {
            "offeritem": {
                "fCapConstraintsLastIndex": 0,
                "lifecycleStatus": "approved"
            },
            "decisionitem": {
                "itemCalendarConstraints": {
                    "endDate": "2030-12-31T08:00:00.000Z",
                    "startDate": "2024-06-10T04:00:00.000Z"
                },
                "itemCatalogID": "itemCatalong1234",
                "itemConstraints": {
                    "eligibilityRule": "rule1234",
                    "profileConstraintType": "eligibilityRule"
                },
                "itemDescription": "Offer item description",
                "itemID": "offerItem5678",
                "itemLabels": [],
                "itemName": "Offer Item One",
                "itemPriority": 1,
                "itemTags": []
            }
        }
    },
    "_<imsOrg>": {
        "some_field": "some value"
    }
}
```
