---
title: Auflisten von Entscheidungsregeln
description: Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: c4c3e415-bc57-45db-b27f-4a5e9fc1f02c
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 54%

---

# Auflisten von Entscheidungsregeln {#list-decision-rules}

Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen. Durch Ausführung einer einzelnen GET-Anfrage an die [!DNL Offer Library]-API können Sie eine Liste der Entscheidungsregeln in einem Container anzeigen.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionale Abfrageparameter zum Filtern der Ergebnisse. | `limit=2` |

## Verwenden von Abfrageparametern {#using-query-parameters}

Beim Auflisten von Ressourcen können Sie Abfrageparameter nutzen, um Ergebnisse zu sortieren und zu filtern.

### Paging {#paging}

Zu den häufigsten Abfrageparametern für das Paging gehören:

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `property` | Ein optionaler Eigenschaftenfilter: <br> <ul> - Die Eigenschaften werden nach UND-Vorgang gruppiert. <br><br> - Parameter können wie folgt wiederholt werden: property=<property-expr>[&amp;property=<property-expr2>...] oder property=<property-expr1>[,<property-expr2>...] <br><br> - Eigenschaftenausdrücke haben das Format [!]field[op]Wert, mit op in [==,!=,&lt;=,>=,&lt;,>,~]unterstützt reguläre Ausdrücke | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Durch Hinzufügen eines - vor dem Namen (orderby=-name) werden Elemente nach Namen in absteigender Reihenfolge sortiert (Z-A). Pfadausdrücke haben die Form von durch Punkte getrennten Pfaden. Dieser Parameter kann wie folgt wiederholt werden: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Schränken Sie die Anzahl der zurückgegebenen Entitäten ein. | `limit=5` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt eine Liste von Entscheidungsregeln zurück, auf die Sie Zugriff haben.

```json
{
     "results": [
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
        },
        {
            "created": "2023-03-06T15:11:42.178+00:00",
            "modified": "2023-03-06T15:11:42.178+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerRule5678",
            "name": "People born after 1981",
            "description": "Persons with the birth date after 1981",
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "person.birthDate occurs after date(1981, 1, 1)"
            }
        }
    ],
    "count": 2,
    "total": 25,
    "_links": {
        "self": {
            "href": "/offer-rules?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
