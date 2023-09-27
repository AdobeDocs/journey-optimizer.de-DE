---
title: Entscheidungsregel erstellen
description: Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 55%

---

# Entscheidungsregel erstellen {#create-decision-rule}

Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, aus denen die *Content-Type* -Feld in der Anfragekopfzeile:

| Header-Name | Wert |
| ----------- | ----- |
| Inhaltstyp | `application/json` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/offer-rules
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungsregeln befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Sales rule",
    "description": "Decisioning rule for sales",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "definedOn": {
        "profile": {
            "schema": {
                "ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**Antwort**

Eine erfolgreiche Antwort gibt Informationen zur neu erstellten Entscheidungsregel zurück, einschließlich Platzierung `id`. Sie können die `id` in späteren Schritten, um Ihre Entscheidungsregel zu aktualisieren oder zu löschen oder sie in einem späteren Tutorial zum Erstellen von Entscheidungen, Entscheidungsregeln und Fallback-Angeboten zu verwenden.

```json
{
   "etag": 1,
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
