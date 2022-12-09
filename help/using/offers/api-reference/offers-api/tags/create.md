---
title: Tag erstellen
description: Mit Tags können Sie Ihre Angebote besser organisieren und sortieren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Tag erstellen {#create-tag}

Sie können ein Tag erstellen, indem Sie eine POST-Anfrage an die [!DNL Offer Library] -API verwenden, während Sie Ihre Container-ID angeben.

## Kopfzeilen &quot;Accept&quot;und &quot;Content-Type&quot; {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, aus denen die *Content-Type* und *Accept* -Felder in der Anfragekopfzeile:

| Kopfzeilenname | Wert |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Tags befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anfrage**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Holiday sales and promotions"
    }'
```

**Reaktion**

Bei einer erfolgreichen Antwort werden Informationen zum neu erstellten Tag zurückgegeben, einschließlich der eindeutigen Instanz-ID und der Platzierungs- `@id`. Sie können die Instanz-ID in späteren Schritten verwenden, um Ihr Tag zu aktualisieren oder zu löschen. Sie können Ihr eindeutiges Tag verwenden `@id` in späteren Tutorials zum Erstellen von Kollektionen und personalisierten Angeboten.

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:34:34.486296Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
