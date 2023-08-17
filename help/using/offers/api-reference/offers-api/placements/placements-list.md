---
title: Auflisten von Platzierungen
description: Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: 40cd9df5b41fd622b8e447d7fc672502e9e29787
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 100%

---

# Auflisten von Platzierungen {#list-placements}

Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden. Eine Platzierung hilft sicherzustellen, dass der richtige Angebotsinhalt an der richtigen Stelle Ihrer Nachricht angezeigt wird. Wenn Sie Inhalte zu einem Angebot hinzufügen, werden Sie aufgefordert, eine Platzierung auszuwählen, an der diese Inhalte angezeigt werden können.

Durch Ausführung einer einzelnen GET-Anfrage an die [!DNL Offer Library]-API können Sie eine Liste aller Platzierungen in einem Container anzeigen.

**API-Format**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Platzierungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Definiert das Schema, das Platzierungen zugeordnet ist. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `{QUERY_PARAMS}` | Optionale Abfrageparameter zum Filtern der Ergebnisse. | `limit=2` |

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
| `limit` | Schränken Sie die Anzahl der zurückgegebenen Platzierungen ein. | `limit=5` |

**Anfrage**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2' \
  -H 'Accept: *,application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird eine Liste von Platzierungen zurückgegeben, die in dem Container vorhanden sind, auf den Sie Zugriff haben.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2020-10-21T19:48:51.843067Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0feb6a80-0f32-11eb-8110-e17787c335b5",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-15T22:02:05.480449Z",
                "repo:lastModifiedDate": "2020-10-15T22:13:00.278175Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "New placement name",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "Updated placement description",
                    "@id": "xcore:offer-placement:12466ef35fc5baa0"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                }
            },
            {
                "instanceId": "269192b0-f8f2-11ea-8723-916b9fbadc53",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-17T14:29:10.107121Z",
                "repo:lastModifiedDate": "2020-09-17T14:29:10.107121Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:name": "demo placement",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "@id": "xcore:offer-placement:1221fac4e7340521"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 17,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=269192b0-f8f2-11ea-8723-916b9fbadc53&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
