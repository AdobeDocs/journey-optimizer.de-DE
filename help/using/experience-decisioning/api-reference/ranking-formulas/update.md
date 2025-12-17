---
title: Aktualisieren von Rangfolgenformeln
description: Mithilfe von Rangfolgenformeln können Sie die Funktionen für die Bewertung definieren, die zum Ordnen von Elementen verwendet werden.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 4ef1bfc2-e74f-4b44-b3b5-8a4f2fbd6438
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: ht
source-wordcount: '153'
ht-degree: 100%

---

# Aktualisieren einer Rangfolgenformel {#update-ranking-formula}

Sie können eine Rangfolgenformel ändern oder aktualisieren, indem Sie eine PUT-Anfrage an die Angebotsbibliothek-API richten.

Weitere Informationen zu JSON PUT, einschließlich der verfügbaren Vorgänge, finden Sie in der offiziellen [Dokumentation zu JSON PUT](http://jsonpatch.com/).

**Header „Akzeptieren“ und „Content-Typ“**

Folgende Tabelle zeigt die gültigen Werte mit den Feldern „Content-Typ“ im Anfrage-Header:

| Header-Name | Wert |
| --------- | ----------- |
| Inhaltstyp | `application/json` |

**API-Format**

```http
PUT /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie aktualisieren möchten. | `rankingFormula1234` |

**Anfrage**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Ranking Function DPS",
    "description": "Ranking  function description",
    "isPure": true,
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Die Vorgänge umfassen: `add`, `replace`, `remove`, `copy` und `test`. |

**Antwort**

Bei einer erfolgreichen Antwort werden die aktualisierten Details der Rangfolgenformel einschließlich der ID zurückgegeben.

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
