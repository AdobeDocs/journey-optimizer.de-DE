---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Auflisten von Sammlungsqualifizierern
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: cc577989-198c-4e21-80e7-32ebb7a60606
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/KZ7JHtHfbuTtVkd-A3-vMrZoYcsTt1Ru62o8Sqy1Bww
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 287
ht-degree: 100%

---

# Auflisten von Sammlungsqualifizierern {#list-tags}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../../experience-decisioning/gs-experience-decisioning.md)


Mit Sammlungsqualifizierern (ehemals als „Tags“ bezeichnet) können Sie Ihre Angebote besser organisieren und sortieren. Beispielsweise könnten Sie Ihre Black Friday-Angebote mit dem Sammlungsqualifizierer „Black Friday“ kennzeichnen. Anschließend können Sie die Suchfunktion in der Angebotsbibliothek nutzen, um alle Angebote mit diesem Sammlungsqualifizierer einfach zu finden.

Sammlungsqualifizierer können auch dazu dienen, Angebote in Sammlungen zu gruppieren. Weitere Informationen finden Sie im Tutorial zum [Erstellen von Sammlungen](../../../../offer-library/creating-collections.md).

Durch Ausführung einer einzelnen GET-Anfrage an die [!DNL Offer Library]-API können Sie eine Liste aller Sammlungsqualifizierer anzeigen.

**API-Format**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_TAG}&{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Sammlungsqualifizierer befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_TAG}` | Definiert das Schema, das mit Sammlungsqualifizierern verknüpft ist. | `https://ns.adobe.com/experience/offer-management/tag;version=0.1` |
| `{QUERY_PARAMS}` | Optionale Abfrageparameter zum Filtern der Ergebnisse. | `limit=2` |

**Anfrage**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
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
| `property` | Ein optionaler Eigenschaftenfilter: <ul><li>Die Eigenschaften werden nach UND-Vorgang gruppiert.</li><li>Parameter können wie folgt wiederholt werden: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}…] oder property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}…]</li><li>Eigenschaftenausdrücke haben das Format `[!]field[op]value`, mit `op` in `[==,!=,<=,>=,<,>,~]`, wobei reguläre Ausdrücke unterstützt werden.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Durch Hinzufügen eines „-“ vor dem Namen (orderby=-name) werden Elemente nach Namen in absteigender Reihenfolge sortiert (Z–A). Pfadausdrücke haben die Form von durch Punkte getrennten Pfaden. Dieser Parameter kann wie folgt wiederholt werden: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Begrenzt die Anzahl der zurückgegebenen Entitäten. | `limit=5` |

**Antwort**

Bei einer erfolgreichen Antwort wird eine Liste von Sammlungsqualifizierern zurückgegeben, die in dem Container vorhanden sind, auf den Sie Zugriff haben.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2023-10-21T20:28:21.521267Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2023-10-16T05:11:26.815213Z",
                "repo:lastModifiedDate": "2023-10-16T22:20:20.190006Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Sneakers",
                    "@id": "xcore:tag:1246d138ec8cca1f"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0adf2ef0-0f6e-11eb-b3be-9b775f952952",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                }
            },
            {
                "instanceId": "149e0de0-ff5f-11ea-b017-f98866426d43",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-09-25T18:44:02.109748Z",
                "repo:lastModifiedDate": "2023-09-25T18:44:02.109748Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "retirement",
                    "@id": "xcore:tag:122c81d2804e69e3"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/tag;version=0.1#149e0de0-ff5f-11ea-b017-f98866426d43",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/149e0de0-ff5f-11ea-b017-f98866426d43",
                        "@type": "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 11,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=149e0de0-ff5f-11ea-b017-f98866426d43&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/tag;version=0.1&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
