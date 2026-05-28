---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erstellen eines Sammlungsqualifizierers
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/4maXlu1c16Y0-7KNahbe9k69R0g6TShJkhG-dYJVzKQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 100%

---

# Erstellen eines Sammlungsqualifizierers {#create-tag}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../experience-decisioning/gs-experience-decisioning.md)


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
