---
title: Erstellen einer Rangfolgenformel
description: Mithilfe von Rangfolgenformeln können Sie die Funktionen für die Bewertung definieren, die zum Ordnen von Elementen verwendet werden.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eb3ca65-f9f2-4483-ac6a-7bd896b0e516
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: ht
source-wordcount: '107'
ht-degree: 100%

---

# Erstellen einer Rangfolgenformel {#create-ranking-formula}

Sie können eine Rangfolgenformel erstellen, indem Sie eine POST-Anfrage an die Angebotsbibliothek-API richten.

**Header „Akzeptieren“ und „Content-Typ“**

Folgende Tabelle zeigt die gültigen Werte mit den Feldern „Content-Typ“ im Anfrage-Header:

| Header-Name | Wert |
| --------- | ----------- | 
| Inhaltstyp | application/json |

**API-Format**

```http
POST /{ENDPOINT_PATH}/ranking-formulas 
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/ranking-formulas' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Ranking Function DPS",
    "description": "Ranking  function description",
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details der neu erstellten Rangfolgenformel einschließlich der `id` zurückgegeben. Sie können die `id` in späteren Schritten verwenden, um Ihre Rangfolgenformel zu aktualisieren oder zu löschen. 

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
