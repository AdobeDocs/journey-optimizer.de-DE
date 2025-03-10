---
title: Rangfolgeformeln aktualisieren
description: Mithilfe von Rangfolgeformeln können Sie die Funktionen für die Bewertung definieren, die zum Sortieren von Elementen verwendet werden.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 33%

---

# Aktualisieren einer Rangfolgenformel {#update-ranking-formula}

Sie können eine Rangfolgenformel ändern oder aktualisieren, indem Sie eine PUT-Anfrage an die Angebotsbibliotheks-API richten.

Weitere Informationen zu JSON PUT, einschließlich verfügbarer Vorgänge, finden Sie in der offiziellen [JSON PUT-Dokumentation](http://jsonpatch.com/).

**Accept- und Content-Type-Kopfzeilen**

In der folgenden Tabelle sind die gültigen Werte aus den Feldern des Inhaltstyps im Anfrage-Header aufgeführt:

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
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Operationen umfassen: `add`, `replace`, `remove`, `copy` und `test`. |

**Antwort**

Eine erfolgreiche Antwort gibt die aktualisierten Details der Rangfolgenformel zurück, einschließlich der ID.

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
