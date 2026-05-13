---
title: Platzierung aktualisieren
description: Die erweiterte Platzierung besteht aus Sammlungen, die mit Einschränkungen und Ranking-Methoden verknüpft sind, um Angebote zu bestimmen.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: 74e090e1-4dbe-484b-a482-ef43e082e7b1
TQID: https://experienceleague.adobe.com/6RpNeMQUn2qEfAzQ-Q7f7PgBRJCLqp7WnsoKx0xr12s
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 0%

---

# Aktualisieren einer erweiterten Platzierung {#update-exd-placement}

Sie können eine Platzierung ändern oder aktualisieren, indem Sie eine PUT-Anfrage an die Angebotsbibliotheks-API richten.

Weitere Informationen zu JSON PUT, einschließlich verfügbarer Vorgänge, finden Sie in der offiziellen JSON-PUT-Dokumentation.

**Accept- und Content-Type-Kopfzeilen**

In der folgenden Tabelle sind die gültigen Werte aus den Feldern des Inhaltstyps im Anfrage-Header aufgeführt:

| Parameter | Beschreibung |
| --------- | ----------- |
| content-type | `application/json` |

**API-Format**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie aktualisieren möchten. | `placement1234` |

**Anfrage**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `op` | Der Operationsaufruf, der verwendet wird, um die Aktion zu definieren, die zum Aktualisieren der Verbindung erforderlich ist. Operationen umfassen: `add`, `replace`, `remove`, `copy` und `test`. |

**Antwort**

Eine erfolgreiche Antwort gibt die aktualisierten Details der erweiterten Platzierung zurück, einschließlich der ID.

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
