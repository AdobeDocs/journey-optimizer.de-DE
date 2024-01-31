---
title: Erstellen eines Sammlungskennzeichners
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: ba7d065523116c12e22eec300df13c29d92a54fb
workflow-type: ht
source-wordcount: '121'
ht-degree: 100%

---


# Erstellen eines Sammlungskennzeichners {#create-tag}

Sie können einen Sammlungskennzeichner (ehemals als „Tag“ bezeichnet) erstellen, indem Sie eine POST-Anfrage an die Angebotsbibliotheks-API richten.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Folgende Tabelle zeigt die gültigen Werte mit den Felder *Inhaltstyp* im Anfrageheader:

| Header-Name | Wert |
| ----------- | ----- |
| Inhaltstyp | `application/json` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/tags
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/tags' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{        
    "name": "Black Friday",
    "description": "Tag for black friday"
}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden Informationen zum neu erstellten Sammlungskennzeichner zurückgegeben, einschließlich der eindeutigen `id`. Sie können die `id` in späteren Schritten verwenden, um Ihren Sammlungskennzeichner zu aktualisieren oder zu löschen. Sie können die eindeutige `id` Ihres Sammlungsqualifizierers in späteren Tutorials zum Erstellen von Sammlungen und personalisierten Angeboten nutzen.

```json
{
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 1,
    "createdDate": "2023-09-07T12:36:26.602Z",
    "lastModifiedDate": "2023-09-07T12:36:26.602Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
