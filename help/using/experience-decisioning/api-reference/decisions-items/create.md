---
title: Erstellen eines Entscheidungselements
description: Erfahren Sie, wie Sie mit der Angebotsbibliothek-API ein Entscheidungselement erstellen.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: e60b0eec-29bc-4411-9eab-08eaf738fc79
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 100%

---

# Erstellen eines Entscheidungselements {#create-decision-items}

Sie können ein Entscheidungselement erstellen, indem Sie eine POST-Anfrage an die Angebotsbibliothek-API richten.

**API-Format**

```http
POST /{ENDPOINT_PATH}/offer-items
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-items' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '{
    "_experience": {
        "decisioning": {
            "offeritem": {
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
                "itemName": "Offer Item One",
                "itemPriority": 1
            }
        }
    },
    "_<imsOrg>": {
        "foo": "bar"
    }
}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details des neu erstellten Entscheidungselements zurückgegeben, einschließlich der ID. Sie können die ID in späteren Schritten verwenden, um Ihr Entscheidungselement zu aktualisieren oder zu löschen. 

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
