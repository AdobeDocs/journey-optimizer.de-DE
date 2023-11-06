---
title: Personalisiertes Angebot erstellen
description: Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 234bee17-c830-4bc0-b258-182804df4cb3
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 100%

---

# Personalisiertes Angebot erstellen {#create-personalized-offer}

Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.

Sie können ein personalisiertes Angebot erstellen, indem Sie eine POST-Anfrage an die [!DNL Offer Library]-API richten und dabei Ihre Container-ID angeben.

## Header „Accept“ und „Content-Type“ {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, die die Felder *Content-Type* und *Accept* im Anfrage-Header enthalten:

| Header-Name | Wert |
| ----------- | ----- |
| Akzeptieren | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Inhaltstyp | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API-Format**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die personalisierten Angebote befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anfrage**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
        "xdm:representations": [
        {
                "xdm:components": [
                {
                        "dc:language": [
                            "en"
                    ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                }
                ],
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
        }
    ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2020-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
    },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
    },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
    ]
}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden Informationen zum neu erstellten personalisierten Angebot zurückgegeben, einschließlich der eindeutigen Instanz-ID und der Platzierungs-`@id`. Sie können die Instanz-ID in späteren Schritten verwenden, um Ihr personalisiertes Angebot zu aktualisieren oder zu löschen.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2020-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Einschränkungen {#limitations}

Angebotsdarstellungen und einige Angebotsbeschränkungen werden derzeit nicht mit den mobilen [!DNL Experience Edge]-Workflows unterstützt, zum Beispiel `Capping`. Der Wert des Feldes `Capping` gibt an, wie oft ein Angebot allen Benutzern angezeigt werden kann. Weitere Informationen finden Sie in der [Dokumentation zu Angebotseignungsregeln und Einschränkungen](../../../../offer-library/creating-personalized-offers.md).
