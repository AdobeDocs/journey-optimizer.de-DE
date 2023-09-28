---
title: Auflisten von Sammlungskennzeichnern
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: bee5e067e70e065c9db14448c42224a9ec09c5bf
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 55%

---

# Auflisten von Sammlungskennzeichnern {#list-tags}

Mit Sammlungsqualifizierern (ehemals als „Tags“ bezeichnet) können Sie Ihre Angebote besser organisieren und sortieren. Beispielsweise könnten Sie Ihre Black Friday-Angebote mit dem Sammlungsqualifizierer „Black Friday“ kennzeichnen. Anschließend können Sie die Suchfunktion in der Angebotsbibliothek nutzen, um alle Angebote mit diesem Sammlungsqualifizierer einfach zu finden.

Sammlungsqualifizierer können auch dazu dienen, Angebote in Sammlungen zu gruppieren. Weitere Informationen finden Sie im Tutorial zum [Erstellen von Sammlungen](../../../offer-library/creating-collections.md).

Sie können eine Liste aller Sammlungsbezeichner anzeigen, indem Sie eine einzige GET-Anfrage an die [!DNL Offer Library] API.

**API-Format**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
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
| `property` | Ein optionaler Eigenschaftenfilter: <ul><li> Die Eigenschaften werden nach UND-Vorgang gruppiert. <br><br> - Parameter können wie folgt wiederholt werden: property=`<property-expr>`[&amp;property=`<property-expr2>`...] oder property=`<property-expr1>`[&amp;`<property-expr2>`...] <br><br> - Eigenschaftenausdrücke haben das Format `[!]field[op]` Wert, mit op in `[==,!=,'<=',>=,<,>,~]`unterstützt reguläre Ausdrücke  </li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Durch Hinzufügen eines - vor dem Namen (orderby=-name) werden Elemente nach Namen in absteigender Reihenfolge sortiert (Z-A). Pfadausdrücke haben die Form von durch Punkte getrennten Pfaden. Dieser Parameter kann wie folgt wiederholt werden: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Schränken Sie die Anzahl der zurückgegebenen Entitäten ein. | `limit=5` |

**Antwort**

Bei einer erfolgreichen Antwort wird eine Liste von Kollektionskennungen zurückgegeben, die vorhanden sind.

```json
{
                "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
