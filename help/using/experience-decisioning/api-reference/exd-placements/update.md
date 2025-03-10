---
title: Platzierung aktualisieren
description: Die erweiterte Platzierung besteht aus Sammlungen, die mit Einschränkungen und Ranking-Methoden verknüpft sind, um Angebote zu bestimmen.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 39%

---

# Aktualisieren einer erweiterten Platzierung {#update-exd-placement}

Sie können eine Platzierung ändern oder aktualisieren, indem Sie eine PUT-Anfrage an die Angebotsbibliotheks-API richten.

Weitere Informationen zu JSON PUT, einschließlich verfügbarer Vorgänge, finden Sie in der offiziellen JSON-PUT-Dokumentation.

**Accept- und Content-Type-Kopfzeilen**

In der folgenden Tabelle sind die gültigen Werte aus den Feldern des Inhaltstyps im Anfrage-Header aufgeführt:

| Parameter | Beschreibung |
| --------- | ----------- |
| Inhaltstyp | `application/json` |

**API-Format**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
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
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Operationen umfassen: `add`, `replace`, `remove`, `copy` und `test`. |

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
