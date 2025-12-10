---
title: Nachschlagen einer Rangfolgenformel
description: Mithilfe von Rangfolgenformeln können Sie die Funktionen für die Bewertung definieren, die zum Ordnen von Elementen verwendet werden.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: f048b2d1-d26b-4987-8acb-3558df506ec2
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 100%

---

# Nachschlagen einer  {#list-ranking-formula}

Sie können nach einer bestimmten Rangfolgenformel suchen, indem Sie eine GET-Anfrage an die Angebotsbibliothek-API richten, die die ID im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Identität, die Sie nachschlagen möchten. | `rankingFormula1234` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt die Details der Rangfolgenformel zurück.

```json
{
    "created": "2024-08-08T23:45:15.380Z",
    "modified": "2024-10-22T18:15:05.909Z",
    "etag": 36,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/ranking-function"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:ranking-function:1947f5372cc4ed74",
    "name": "[Do not delete] - Cypress e2e - edit",
    "description": "some description",
    "returnType": {
        "type": "INTEGER"
    },
    "exdFunction": true,
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "42 = 11"
    }
}
```
