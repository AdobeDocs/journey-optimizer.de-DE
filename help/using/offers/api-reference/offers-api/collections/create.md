---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erstellen einer Sammlung
description: Sammlungen sind Teilmengen von Angeboten, die auf von Marketing-Fachleuten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.
feature: Decision Management, API, Collections
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 683f8b86-8545-46d0-a4a8-25c5b3c7b9c3
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/1TKc43ym3Vh2wmxKwEn9-YTEDKaXwPD-Un0bR1ojyGc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 150
ht-degree: 100%

---

# Erstellen einer Sammlung {#create-collection}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../experience-decisioning/gs-experience-decisioning.md)


Sammlungen sind Teilmengen von Angeboten, die auf von Marketing-Fachleuten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.

Sie können eine Sammlung erstellen, indem Sie eine POST-Anfrage an die [!DNL Offer Library] API richten.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, die das Feld *Content-Type* im Anfrage-Header enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Inhaltstyp | `application/json` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/offer-collections
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden Informationen zur neu erstellten Sammlung zurückgegeben, einschließlich der zugehörigen `id`. Sie können die `id` in späteren Schritten verwenden, um Ihre Sammlung zu aktualisieren oder zu löschen, oder in einem späteren Tutorial zum Erstellen einer Entscheidung.

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
