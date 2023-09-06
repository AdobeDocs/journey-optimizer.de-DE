---
title: Entscheidungsregel nachschlagen
description: Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 54368710-1021-43c0-87b7-5176cc6c72f7
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 35%

---

# Nach einer Entscheidungsregel suchen {#lookup-decision-rule}
Sie können eine bestimmte Entscheidungsregel nachschlagen, indem Sie eine GET-Anfrage an die [!DNL Offer Library] API, die die Entscheidungsregel enthält `id` im Anfragepfad.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Entität, die Sie nachschlagen möchten. | `offerRule1234` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt die Details der jeweiligen Entscheidungsregel zurück, die Sie nachgeschlagen haben, einschließlich Informationen zur eindeutigen Entscheidungsregel `@id`.

```json
  {
    "created": "2022-09-16T18:59:53.651+00:00",
    "modified": "2022-09-16T18:59:53.651+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerRule1234",
    "name": "Californians with one or more purchases greater than $1000",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
    }
}
```
