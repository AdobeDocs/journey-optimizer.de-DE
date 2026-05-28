---
title: Aktualisieren von Auswahlstrategien
description: Auswahlstrategien bestehen aus Sammlungen, die mit Begrenzungen und Rangfolgenmethoden zur Bestimmung von Angeboten verknüpft sind.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 060f8c5f-4750-44dc-83aa-630afbc180eb
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/zQ3pwcP7MPdwGKxOLwKfkBo54zW0HkNqTts179HRfnQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 100%

---

# Aktualisieren einer Auswahlstrategie {#update-selection-strategy}

Sie können eine Auswahlstrategie ändern oder aktualisieren, indem Sie eine PATCH-Anfrage an die Angebotsbibliothek-API richten.

Weitere Informationen zu JSON Patch, einschließlich der verfügbaren Vorgänge, finden Sie in der offiziellen [JSON-Patch-Dokumentation](https://jsonpatch.com/).

**API-Format**

```http
PATCH /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie aktualisieren möchten. | `selectionStrategy1234` |

**Anfrage**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated selection strategy"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated selection strategy description"
    }
]'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Die Operationen umfassen: `add`, `replace`, `remove`, `copy` und `test`. |

**Antwort**

Bei einer erfolgreichen Antwort werden die aktualisierten Details der Auswahlstrategie zurückgegeben, einschließlich der ID.

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
