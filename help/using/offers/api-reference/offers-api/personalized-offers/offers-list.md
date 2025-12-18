---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Auflisten personalisierter Angebote
description: Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 45d51918-1106-4b6b-b383-8ab4d9a4f7af
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Auflisten personalisierter Angebote {#list-personalized-offers}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)


Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.

Durch Ausführung einer einzelnen GET-Anfrage an die [!DNL Offer Library]-API können Sie eine Liste aller personalisierten Angebote anzeigen.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=personalized&{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Optionale Abfrageparameter zum Filtern der Ergebnisse. | `limit=2` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized&limit=2' \
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
| `property` | Ein optionaler Eigenschaftenfilter: <ul><li>Die Eigenschaften werden nach UND-Vorgang gruppiert.</li><li>Parameter können wie folgt wiederholt werden: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}…] oder property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}…]</li><li>Eigenschaftenausdrücke haben das Format `[ !]field[op]value`, mit `op` in `[==,!=,<=,>=,<,>,~]`, wobei reguläre Ausdrücke unterstützt werden.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Durch Hinzufügen eines „-“ vor dem Namen (orderby=-name) werden Elemente nach Namen in absteigender Reihenfolge sortiert (Z–A). Pfadausdrücke haben die Form von durch Punkte getrennten Pfaden. Dieser Parameter kann wie folgt wiederholt werden: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Einschränken der Anzahl der zurückgegebenen Platzierungen. | `limit=5` |

**Antwort**

Bei einer erfolgreichen Antwort wird eine Liste mit personalisierten Angeboten zurückgegeben, die vorhanden sind, sowie den Angeboten, auf die Sie Zugriff haben.

```json
{
    "results": [
        {
            "created": "2023-05-15T14:35:16.781+00:00",
            "modified": "2023-05-15T14:38:26.691+00:00",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.15"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "personalizedOffer1234",
            "name": "Test personalized offer with frequency constraint",
            "status": "draft",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "placement": "offerPlacement1234",
                    "components": [
                        {
                            "type": "html",
                            "format": "text/html",
                            "language": [
                                "en-us"
                            ],
                            "content": "Hello You qualify for our Discount of 60%"
                        }
                    ]
                }
            ],
            "selectionConstraint": {
                "startDate": "2022-07-27T05:00:00.000+00:00",
                "endDate": "2023-07-29T05:00:00.000+00:00",
                "profileConstraintType": "none"
            },
            "rank": {
                "priority": 0
            },
            "cappingConstraint": {},
            "frequencyCappingConstraints": [
                {
                    "enabled": false,
                    "limit": 1,
                    "startDate": "2023-05-15T14:25:49.622+00:00",
                    "endDate": "2023-05-25T14:25:49.622+00:00",
                    "scope": "global",
                    "entity": "offer",
                    "repeat": {
                        "enabled": false,
                        "unit": "month",
                        "unitCount": 1
                    }
                }
            ]
        }
    ],
    "count": 1,
    "total": 1,
    "_links": {
        "self": {
            "href": "/offers?offer-type=personalized&href={SELF_HREF}",
            "type": "application/json"
        }
    }
}
```

Führen Sie eine Paginierung durch, wenn in der Antwort mehrere personalisierte Angebote fehlen.

**Antwort**

```json
{
    "results": [...],
    "count": 2,
    "total": 43,
    "_links": {
        "self": {
        "href": "/offers?orderby=-modified&limit=2&offer-type=PERSONALIZED",
        "type": "application/json"
        },
        "next": {
        "href": "/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED",
        "type": "application/json"
        }
    }
    }
```

| Metrik | Beschreibung |
|---------|-------------|
| `total` | Die Anzahl der personalisierten Angebote. |
| `count` | Die Anzahl der in dieser Antwort zurückgegebenen Angebote. |

Rufen Sie den Endpunkt aus `_links.next.href` ab, z. B. `/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED`, und fügen Sie ihn an das API an.

**API-Format**

```http
GET /{ENDPOINT_PATH}/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED
```

```json
{
    "results": [...],
    "count": 2,
    "total": 43,
    "_links": {
        "self": {...},
        "next": {
        "href": "/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED",
        "type": "application/json"
        }
    }
}
```

Wenn Sie nicht auf der ersten Seite sind und die vorherige Seite mit personalisierten Angeboten abrufen müssen, verwenden Sie den `href`-Wert aus `_links.prev`. Fordern Sie eine URL an, um die vorherigen Ergebnisse abzurufen, wie im folgenden Beispiel gezeigt.

**Antwort**

```json
{
    "results": [...],
    "count": 2,
    "total": 43,
    "_links": {
        "self": {...},
        "next": {...},
        "prev": {
        "href": "/offers?orderby=-modified&limit=2&start={TIMESTAMP}&offer-type=PERSONALIZED",
        "type": "application/json"
        }
    }
}
```
