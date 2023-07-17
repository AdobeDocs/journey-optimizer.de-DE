---
title: Auflisten von Sammlungskennzeichnern
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: 40cd9df5b41fd622b8e447d7fc672502e9e29787
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 100%

---

# Auflisten von Sammlungskennzeichnern {#list-tags}

Mit Sammlungsqualifizierern (ehemals als „Tags“ bezeichnet) können Sie Ihre Angebote besser organisieren und sortieren. Beispielsweise könnten Sie Ihre Black Friday-Angebote mit dem Sammlungsqualifizierer „Black Friday“ kennzeichnen. Anschließend können Sie die Suchfunktion in der Angebotsbibliothek nutzen, um alle Angebote mit diesem Sammlungsqualifizierer einfach zu finden.

Sammlungsqualifizierer können auch dazu dienen, Angebote in Sammlungen zu gruppieren. Weitere Informationen finden Sie im Tutorial zum [Erstellen von Sammlungen](../../../offer-library/creating-collections.md).

Sie können eine Liste aller Sammlungsqualifizierer in einem Container anzeigen, indem Sie eine einzelne GET-Anfrage an die [!DNL Offer Library]-API durchführen.

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
| `q` | Eine optionale Abfragezeichenfolge, nach der in ausgewählten Feldern gesucht werden soll. Die Abfragezeichenfolge sollte in Kleinbuchstaben verfasst werden und kann von doppelten Anführungszeichen umgeben sein, um eine Tokenisierung zu verhindern und Sonderzeichen zu umgehen (Escape). Die Zeichen `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` haben eine besondere Bedeutung und sollten bei der Darstellung in der Abfragezeichenfolge mit einem umgekehrten Schrägstrich als Escape-Zeichen versehen werden. | Website JSON |
| `qop` | Wendet den AND- oder OR-Operator auf Werte im Abfragezeichenfolgen-Parameter an. | `AND` / `OR` |
| `field` | Optionale Liste der Felder, auf die die Suche beschränkt werden soll. Dieser Parameter kann wie folgt wiederholt werden: field=field1[,field=field2,...] und (Pfadausdrücke haben die Form von durch Punkte getrennten Pfaden wie _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Das Hinzufügen von `-` vor dem Titel (`orderby=-title`) sortiert die Ergebnisse nach Titel in absteigender Reihenfolge (Z-A). | `-repo:createdDate` |
| `limit` | Beschränkt die Anzahl der zurückgegebenen Sammlungsqualifizierer. | `limit=5` |

**Antwort**

Bei einer erfolgreichen Antwort wird eine Liste von Sammlungsqualifizierern zurückgegeben, die in dem Container vorhanden sind, auf den Sie Zugriff haben.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/tag;version=0.1",
    "requestTime": "2020-10-21T20:28:21.521267Z",
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
                "repo:createdDate": "2020-10-16T05:11:26.815213Z",
                "repo:lastModifiedDate": "2020-10-16T22:20:20.190006Z",
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
                "repo:createdDate": "2020-09-25T18:44:02.109748Z",
                "repo:lastModifiedDate": "2020-09-25T18:44:02.109748Z",
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
