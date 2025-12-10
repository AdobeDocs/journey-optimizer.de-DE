---
title: Nachschlagen einer Elementsammlung
description: Sammlungen sind Teilmengen von Angeboten, die auf von Marketing-Fachleuten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 60b2990e-e3a6-4d4b-8851-889cf91b0eef
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Nachschlagen einer Elementsammlung {#lookup-item-collection}

Sie können nach einer bestimmten Elementsammlung suchen, indem Sie eine GET-Anfrage an die Angebotsbibliothek-API richten, die die ID im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Identität, die Sie nachschlagen möchten. | `itemCollections1234` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt die Details der Elementsammlungen zurück.

```json
{
    "created": "2024-01-31T18:28:52.888Z",
    "modified": "2024-06-28T19:44:13.112Z",
    "etag": 7,
    "schemas": [
        "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "itemCollection1234",
    "name": "Item collection One",
    "description": "Item collection",
    "constraints": [
        {
            "itemCatalogId": "itemCatalog1234",
            "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
        }
    ]
}
```
