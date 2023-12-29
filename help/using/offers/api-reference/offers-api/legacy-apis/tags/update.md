---
title: Aktualisieren von Sammlungsqualifizierern
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ef95a51b-1f14-470e-8229-3564bff9c67b
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 100%

---

# Aktualisieren eines Sammlungsqualifizierers {#update-collection-qualifier}

Sie können einen Sammlungsqualifizierer (ehemals als „Tag“ bezeichnet) in Ihrem Container ändern oder aktualisieren, indem Sie eine PATCH-Anfrage an die [!DNL Offer Library]-API richten.

Weitere Informationen zu JSON Patch, einschließlich der verfügbaren Vorgänge, finden Sie in der offiziellen [JSON-Patch-Dokumentation](https://jsonpatch.com/).

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, die die Felder *Content-Type* und *Accept* im Anfrage-Header enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Akzeptieren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhaltstyp | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API-Format**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Tags befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID des Tags, das Sie aktualisieren möchten. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Anfrage**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
          "op": "replace",
          "path": "/_instance/xdm:name",
          "value": "Sales and promotions for the holidays"
        }
    ]'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Die Operationen umfassen `add`, `replace` und `remove`. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |

**Antwort**

Bei einer erfolgreichen Antwort werden die aktualisierten Details des Sammlungsqualifizierers zurückgegeben, einschließlich der eindeutigen Instanz-ID und der Sammlungsqualifizierer-`@id`.

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:36:31.782607Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
