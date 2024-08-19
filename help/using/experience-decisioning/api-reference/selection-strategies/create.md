---
title: Erstellen einer Auswahlstrategie
description: Auswahlstrategien bestehen aus Kollektionen, die mit Begrenzungen und Rangmethoden zur Bestimmung von Angeboten verknüpft sind.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dcff8803404228bbed40e998d802bb6c0f4ac67e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 23%

---


# Erstellen einer Auswahlstrategie {#create-selection-strategy}

Sie können eine Auswahlstrategie erstellen, indem Sie eine POST-Anfrage an die Angebotsbibliothek-API richten.

**Accept- und Content-Type-Kopfzeilen**

Die folgende Tabelle zeigt die gültigen Werte, die die Felder Content-Type im Anfrageheader enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Inhaltstyp | `application/json` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/selection-strategies 
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/selection-strategies' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{    
    "name": "Selection Strategy One",
    "description": "Selection Strategy",
    "rank": {
        "priority": 1,
        "order": {
            "orderEvaluationType": "static"
        }
    },
    "profileConstraint": {
        "profileConstraintType": "eligibilityRule",
        "eligibilityRule": "offerRule1234"
    },
    "optionSelection": {
        "filter": "itemCollection1234",
    }
}'
```

**Antwort**

Eine erfolgreiche Antwort gibt die Details der neu erstellten Auswahlstrategie einschließlich der ID zurück. Sie können die ID in späteren Schritten verwenden, um Ihre Auswahlstrategie zu aktualisieren oder zu löschen.

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
