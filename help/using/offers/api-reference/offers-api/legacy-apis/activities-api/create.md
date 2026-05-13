---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Erstellen einer Entscheidung
description: Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 7cb906b9-8925-4482-9915-448a41e11d9d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ZSGnM6ab3lRA3tFax09mDx7Aaw32b01Mxduq-MrMDrQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 100%

---

# Erstellen einer Entscheidung {#create-decision}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../../experience-decisioning/gs-experience-decisioning.md)


Sie können eine Entscheidung erstellen, indem Sie eine POST-Anfrage an die [!DNL Offer Library]-API richten und dabei Ihre Container-ID angeben.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, die die Felder *Content-Type* und *Accept* im Anfrage-Header enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Inhaltstyp | `application/json` |

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

Bei einer erfolgreichen Antwort werden Informationen zur neu erstellten Entscheidung zurückgegeben, einschließlich der einzigartigen `id`. Sie können die `id` in späteren Schritten verwenden, um Ihre Entscheidung zu aktualisieren oder zu löschen.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2023-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
