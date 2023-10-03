---
title: Erstellen von Entscheidungen
description: Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 553501b0-30a9-4795-9a9d-f42df5f4f2ea
source-git-commit: ef22b6183c7646cca8636f4a7e4dd87c8f88e8ce
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 61%

---


# Erstellen von Entscheidungen {#create-decision}

Sie können eine Entscheidung erstellen, indem Sie eine POST-Anfrage an die [!DNL Offer Library]-API richten und dabei Ihre Container-ID angeben.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

    @@ -22,61 +22,67 @@ Die folgende Tabelle zeigt die gültigen Werte, die den *Content-Type* und
**API-Format**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anfrage**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
      "_instance": {
          "xdm:name": "Test API",
          "xdm:startDate": "2022-01-20T16:00:00Z",
          "xdm:endDate": "2022-01-27T16:00:00Z",
          "xdm:status": "live",
          "xdm:criteria": [
        {
                  "xdm:placements": [
                      "xcore:offer-placement:1457f9322f005194"
            ],
                  "xdm:optionSelection": {
                      "xdm:filter": "xcore:offer-filter:1457f93227d0b6f0"
                }
              }
          ],
          "xdm:fallback": "xcore:fallback-offer:13c259399d8bf013"
            },
      "_links": {}
}'
```

**Antwort**

Eine erfolgreiche Antwort gibt Informationen zur neu erstellten Entscheidung zurück, einschließlich der eindeutigen `id`. Sie können `id` in späteren Schritten, um Ihre Entscheidung zu aktualisieren oder zu löschen.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
