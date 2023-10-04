---
title: Erstellen von Sammlungen
description: Sammlungen sind Untergruppen von Angeboten, die auf von einem Marketing-Experten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 6156689d9e5d7abedcd612389c5e332c695601f0
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 70%

---

# Erstellen von Sammlungen {#create-collection}

Sammlungen sind Untergruppen von Angeboten, die auf von einem Marketing-Experten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.

Sie können eine Sammlung erstellen, indem Sie eine POST-Anfrage an die [!DNL Offer Library]-API richten und dabei Ihre Container-ID angeben.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, die die Felder *Content-Type* und *Accept* im Anfrage-Header enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Akzeptieren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhaltstyp | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps/` |

**Anfrage**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Offer Collection 1",
        "xdm:filterType": "anyTags",
        "xdm:ids": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**Antwort**

Bei einer erfolgreichen Antwort werden Informationen zur neu erstellten Kollektion zurückgegeben, einschließlich der zugehörigen `id`. Sie können die `id` in späteren Schritten, um Ihre Sammlung zu aktualisieren oder zu löschen, oder in einem späteren Tutorial zum Erstellen einer Entscheidung.

```json
{
   "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
