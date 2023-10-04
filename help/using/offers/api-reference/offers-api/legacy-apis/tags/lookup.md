---
title: Nachschlagen eines Sammlungsqualifizierers
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 6156689d9e5d7abedcd612389c5e332c695601f0
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 38%

---


# Nachschlagen eines Sammlungsqualifizierers {#look-up-tag}

Sie können bestimmte Sammlungsbezeichner (zuvor als &quot;Tags&quot;bezeichnet) nachschlagen, indem Sie eine GET-Anfrage an die [!DNL Offer Library] API, die den Sammlungsbezeichner enthält `id` im Anfragepfad.

**API-Format**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie nachschlagen möchten. | `tag1234` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details des Sammlungsqualifizierers zurückgegeben, einschließlich Informationen zu Ihrem eindeutigen Sammlungsbezeichner. `id`.

```json
{
       "created": "2022-09-16T19:00:02.070+00:00",
    "modified": "2022-09-16T19:00:02.070+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "tag1234",
    "name": "Sneakers"
}
```
