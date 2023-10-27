---
title: Nachschlagen eines Sammlungsqualifizierers
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '90'
ht-degree: 100%

---

# Nachschlagen eines Sammlungsqualifizierers {#look-up-tag}

Sie können einzelne Sammlungsqualifizierer (ehemals als „Tags“ bezeichnet) nachschlagen, indem Sie eine GET-Anfrage an die [!DNL Offer Library]-API richten, die die `id` des Sammlungsqualifizierers im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Identität, die Sie nachschlagen möchten. | `tag1234` |

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

Bei einer erfolgreichen Antwort werden die Details des Sammlungsqualifizierers zurückgegeben, einschließlich Informationen zu Ihrer eindeutigen `id` des Sammlungsqualifizierers.

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
