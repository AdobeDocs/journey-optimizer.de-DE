---
title: Platzierung aktualisieren
description: Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6990918c-e736-4f28-9ac6-9ac3101b069f
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 100%

---

# Platzierung aktualisieren {#update-placement}

Sie können eine Platzierung in Ihrem Container ändern oder aktualisieren, indem Sie eine PATCH-Anfrage an die [!DNL Offer Library]-API richten.

Weitere Informationen zu JSON Patch, einschließlich der verfügbaren Vorgänge, finden Sie in der offiziellen [JSON-Patch-Dokumentation](https://jsonpatch.com/).

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, die die Felder *Content-Type* und *Accept* im Anfrage-Header enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Akzeptieren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhaltstyp | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"` |

**API-Format**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Platzierungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID der Platzierung, die Sie aktualisieren möchten. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Anfrage**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:name",
            "value": "Sales and Promotions Placement"
        },
        {
            "op": "replace",
            "path": "/_instance/xdm:description",
            "value": "A test placement to contain offers of sales and discounts"
        }
    ]'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `op` | Der Operationsaufruf, der für die Definition der zum Aktualisieren der Verbindung erforderlichen Aktion verwendet wird. Die Operationen umfassen `add`, `replace` und `remove`. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |

**Antwort**

Bei einer erfolgreichen Antwort werden die aktualisierten Details der Platzierung zurückgegeben, einschließlich der eindeutigen Instanz-ID und der Platzierungs-`@id`.

```json
{
    "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "@id": "xcore:offer-placement:124e0be5699743d3",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T19:57:09.837456Z",
    "repo:lastModifiedDate": "2020-10-21T19:59:10.700149Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
