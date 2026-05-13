---
title: Aktualisieren einer Elementsammlung
description: Sammlungen sind Teilmengen von Angeboten, die auf von Marketing-Fachleuten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: a2b7779d-8c2e-4ff9-8cc3-90846f100c98
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qYudO0NFgw9zjq843wK8zVMwr-nk29HPdXAHLBUc7qg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 100%

---

# Aktualisieren einer Elementsammlung {#update-item-collection}

Sie können eine Elementsammlung ändern oder aktualisieren, indem Sie eine PATCH-Anfrage an die Angebotsbibliothek-API richten.

Weitere Informationen zu JSON Patch, einschließlich der verfügbaren Vorgänge, finden Sie in der offiziellen [JSON-Patch-Dokumentation](https://jsonpatch.com/).

**API-Format**

```http
PATCH /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie aktualisieren möchten. | `itemCollections1234` |

**Anfrage**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated item collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated item collection description"
    }
]'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Die Operationen umfassen: `add`, `replace`, `remove`, `copy` und `test`. |

**Antwort**

Bei einer erfolgreichen Antwort werden die aktualisierten Details der Elementsammlung zurückgegeben, einschließlich der `id`.

```json
{
    "etag": 2,
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
