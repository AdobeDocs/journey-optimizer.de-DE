---
title: Erstellen einer Elementsammlung
description: Mit Sammlungen können Entscheidungselemente nach Ihren eigenen Vorstellungen kategorisiert und gruppiert werden.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: e4f2ab34-2af2-49b5-9164-b129e922fe59
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Nfh8NOmID91zoGJ6sORLX5Ij4SDYnQ5S78ZsrGzqDzc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 100%

---

# Erstellen einer Elementsammlung {#create-decision-items}

Sie können eine Elementsammlung erstellen, indem Sie eine POST-Anfrage an die Angebotsbibliothek-API richten.

**API-Format**

```http
POST /{ENDPOINT_PATH}/item-collections
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/item-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{     
    "name": "Item collection One",
    "description": "Item collection",
    "constraints": [
        {
            "itemCatalogId": "itemCatalog1234",
            "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
        }
    ]
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
