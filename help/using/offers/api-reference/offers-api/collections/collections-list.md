---
title: Auflisten von Sammlungen
description: Sammlungen sind Untergruppen von Angeboten, die auf von einem Marketing-Experten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f27ffbe0-a61a-428a-bc37-db6b56e38a83
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 53%

---

# Auflisten von Sammlungen {#list-collections}

Sammlungen sind Untergruppen von Angeboten, die auf von einem Marketing-Experten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.

Sie können eine Liste aller Sammlungen anzeigen, indem Sie eine einzige GET an die [!DNL Offer Library] API.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offer-collections?{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionale Abfrageparameter zum Filtern der Ergebnisse. | `limit=2` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections?limit=2' \
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

Eine erfolgreiche Antwort gibt eine Liste von Sammlungen zurück, die in dem Container vorhanden sind, auf den Sie Zugriff haben.

```json
{
    "results": [
        {
            "created": "2022-09-16T18:59:23.063+00:00",
            "modified": "2022-09-16T18:59:23.063+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerCollection1234",
            "name": "Test Collection with tags",
            "filterType": "any-tags",
            "ids": [
                "tag1234"
            ],
            "labels": [
                "core/C5",
                "custom/myLabel"
            ]
        },
        {
            "created": "2023-05-15T12:50:49.887+00:00",
            "modified": "2023-05-15T12:50:49.887+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerCollection5678",
            "name": "Test Collection with offers",
            "filterType": "offers",
            "ids": [
                "personalizedOffer1234",
                "personalizedOffer5678"
            ]
        }
    ],
    "count": 2,
    "total": 9,
    "_links": {
        "self": {
            "href": "/offer-collections?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-collections?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
