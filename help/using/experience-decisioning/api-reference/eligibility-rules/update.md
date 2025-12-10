---
title: Aktualisieren von Eignungsregeln
description: Mit Eignungsregeln können Sie die geeigneten Kandidatinnen und Kandidaten basierend auf dem definieren, was Sie ansprechen möchten, z. B. Profilattribute und Zielgruppen.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 8d82b4db-2ba8-4692-a63e-9cb3c6c434c3
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 100%

---

# Aktualisieren einer Eignungsregel {#update-eligibility-rule}

Sie können eine Regel ändern oder aktualisieren, indem Sie eine PUT-Anfrage an die Angebotsbibliothek-API richten.

Weitere Informationen zu JSON PUT, einschließlich der verfügbaren Vorgänge, finden Sie in der offiziellen [Dokumentation zu JSON PUT](https://jsonpatch.com/).

**Header „Akzeptieren“ und „Content-Typ“**

Folgende Tabelle zeigt die gültigen Werte mit den Feldern „Content-Typ“ im Anfrage-Header:

| Header-Name | Wert |
| --------- | ----------- | 
| Inhaltstyp | `application/json` |

**API-Format**

```http
PUT /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie aktualisieren möchten. | `rule1234` |

**Anfrage**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Offer Rule DPS",
    "description": "Offer Rule description",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
    },
    "definedOn": {
        "": {
            "schema": {
                "altId": "_xdm.context.profile",
                "version": "1"
            },
            "referencePaths": [
                "homeAddress.stateProvince"
            ]
        },
        "xEvent": {
            "schema": {
                "altId": "_xdm.context.experienceevent",
                "version": "1"
            },
            "referencePaths": [
                "eventType",
                "commerce.order.priceTotal",
                "commerce.order.currencyCode"
            ]
        }
    }
}'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Die Vorgänge umfassen: `add`, `replace`, `remove`, `copy` und `test`. |

**Antwort**

Bei einer erfolgreichen Antwort werden die aktualisierten Details der Eignungsregel einschließlich der ID zurückgegeben.

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
