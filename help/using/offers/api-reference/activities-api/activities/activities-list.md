---
title: Auflisten von Entscheidungen
description: Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 123ed057-e15f-4110-9fc6-df0e9cb5b038
source-git-commit: a554786f15144923cb5b76c624960c2a602be020
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 41%

---

# Auflisten von Entscheidungen {#list-decisions}

Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.

Sie können eine Liste aller Entscheidungen anzeigen, indem Sie eine einzige GET an die [!DNL Offer Library] API.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offer-decisions?{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionale Abfrageparameter zum Filtern der Ergebnisse. | `limit=2` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Verwenden von Abfrageparametern {#using-query-parameters}

Beim Auflisten von Ressourcen können Sie Abfrageparameter nutzen, um Ergebnisse zu sortieren und zu filtern.

### Paging {#paging}

Zu den häufigsten Abfrageparametern für das Paging gehören:

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `property` | Ein optionaler Eigenschaftenfilter: <br> <ul> - Die Eigenschaften werden nach UND-Vorgang gruppiert. <br><br> - Parameter können wie folgt wiederholt werden: property=<property-expr>[&amp;property=<property-expr2>...] oder property=<property-expr1>[,<property-expr2>...] <br><br> - Eigenschaftenausdrücke haben das Format [!]field[op]Wert, mit op in [==,!=,&lt;=,>=,&lt;,>,~]unterstützt reguläre Ausdrücke | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Durch Hinzufügen eines - vor dem Namen (orderby=-name) werden Elemente nach Namen in absteigender Reihenfolge sortiert (Z-A). Pfadausdrücke haben die Form von durch Punkte getrennten Pfaden. Dieser Parameter kann wie folgt wiederholt werden: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Schränken Sie die Anzahl der zurückgegebenen Entitäten ein. | `limit=5` |

**Antwort**

Eine erfolgreiche Antwort gibt eine Liste von Entscheidungen zurück, auf die Sie Zugriff haben.

```json
{
    "results": [
        {
            "created": "2022-07-05T09:02:02.835+00:00",
            "modified": "2022-08-16T21:40:58.573+00:00",
            "etag": 12,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision1234",
            "name": "Test Decision One",
            "status": "live",
            "startDate": "2022-05-18T00:09:57.706+00:00",
            "endDate": "2032-08-13T21:40:58.235+00:00",
            "fallback": "fallbackOffer1234",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234",
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 0,
                        "order": {
                            "orderEvaluationType": "ranking-strategy",
                            "rankingStrategy": "123456789123"
                        }
                    },
                    "profileConstraint": {
                        "profileConstraintType": "none"
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }
            ]
        },
        {
            "created": "2022-09-05T14:12:13.773+00:00",
            "modified": "2022-09-05T14:12:13.773+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision5678",
            "name": "Test Decision Two",
            "status": "live",
            "startDate": "2022-08-31T21:00:00.000+00:00",
            "endDate": "2023-02-03T22:00:00.000+00:00",
            "fallback": "fallbackOffer5678",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234"
                    ],
                    "rank": {
                        "priority": 2
                    },
                    "optionSelection": {
                        "filter": "offerCollection5678"
                    }
                },
                {
                    "placements": [
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 1
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }          
            ]
        }
    ],
    "count": 2,
    "total": 21,
    "_links": {
        "self": {
            "href": "/offer-decisions?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-decisions?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
