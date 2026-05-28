---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erstellen einer Entscheidungsregel
description: Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/wpVQ64pwXQz9So3T8MLgooq3gmwEBC28lEq3UllDDL8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 100%

---

# Erstellen einer Entscheidungsregel {#create-decision-rule}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../experience-decisioning/gs-experience-decisioning.md)


Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, die das Feld *Content-Type* im Anfrage-Header enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Inhaltstyp | `application/json` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/offer-rules
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |

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

Bei einer erfolgreichen Antwort werden Informationen zur `id` der neu erstellten Entscheidungsregel zurückgegeben. Sie können die `id` in späteren Schritten verwenden, um die Entscheidungsregel zu aktualisieren oder zu löschen oder sie in einer späteren Anleitung zum Erstellen von Entscheidungen, Entscheidungsregeln und Fallback-Angeboten zu verwenden.

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
