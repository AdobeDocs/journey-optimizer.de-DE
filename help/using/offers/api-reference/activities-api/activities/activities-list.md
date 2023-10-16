---
title: Auflisten von Entscheidungen
description: Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 123ed057-e15f-4110-9fc6-df0e9cb5b038
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 85%

---

# Auflisten von Entscheidungen {#list-decisions}

Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.

Durch Ausführung einer einzelnen GET-Anfrage an die [!DNL Offer Library]-API können Sie eine Liste aller Entscheidungen anzeigen.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offer-decisions?{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
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
| `property` | Ein optionaler Eigenschaftenfilter: <ul><li>Die Eigenschaften werden nach UND-Vorgang gruppiert.</li><li>Parameter können wie folgt wiederholt werden: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] oder property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Eigenschaftenausdrücke haben das Format `[!]field[op]value`, mit `op` in `[==,!=,<=,>=,<,>,~]`, die reguläre Ausdrücke unterstützen.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Durch Hinzufügen eines „-“ vor dem Namen (orderby=-name) werden Elemente nach Namen in absteigender Reihenfolge sortiert (Z–A). Pfadausdrücke haben die Form von durch Punkte getrennten Pfaden. Dieser Parameter kann wie folgt wiederholt werden: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Begrenzt die Anzahl der zurückgegebenen Entitäten. | `limit=5` |


**Antwort**

Bei einer erfolgreichen Antwort wird eine Liste von Entscheidungen zurückgegeben, auf die Sie Zugriff haben.

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
