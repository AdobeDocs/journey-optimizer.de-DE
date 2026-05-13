---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Fallback-Angebote auflisten
description: Ein Fallback-Angebot wird an Kunden gesendet, wenn sie für andere Angebote nicht infrage kommen
feature: Decision Management, API
badge: label="Veraltet" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 0eb68312-5567-4728-b184-9d40107676a0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/JEIeF-ImOR4eBpB3oCdF4WDTIl6YcF-Mmh6DbLE9OZo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 302
ht-degree: 0%

---

# Fallback-Angebote auflisten {#list-fallback-offers}

>[!TIP]
>
>Decisioning, [!DNL Adobe Journey Optimizer] neue Entscheidungsfunktion, ist jetzt über die Code-basierten Erlebnis- und E-Mail-Kanäle verfügbar! [Weitere Informationen](../../../../../experience-decisioning/gs-experience-decisioning.md)


Ein Fallback-Angebot wird an Kunden gesendet, wenn sie für andere Angebote nicht infrage kommen. Die Schritte zum Erstellen eines Fallback-Angebots bestehen darin, eine oder mehrere Darstellungen zu erstellen, z. B. beim Erstellen eines Angebots.

Sie können eine Liste aller Fallback-Angebote in einem Container anzeigen, indem Sie eine einzige GET-Anfrage an die [!DNL Offer Library]-API durchführen.

**API-Format**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FALLBACK_OFFER}&{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Fallback-Angebote befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FALLBACK_OFFER}` | Definiert das mit Fallback-Angeboten verknüpfte Schema. | `https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1` |
| `{QUERY_PARAMS}` | Optionale Abfrageparameter zum Filtern der Ergebnisse nach . | `limit=1` |

**Anfrage**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Abfrageparameter verwenden {#using-query-parameters}

Sie können beim Auflisten von Ressourcen Abfrageparameter zum Paging und Filtern von Ergebnissen verwenden.

### Paging {#paging}

Zu den häufigsten Abfrageparametern für Paging gehören:

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `q` | Eine optionale Abfragezeichenfolge, nach der in ausgewählten Feldern gesucht werden soll. Die Abfragezeichenfolge sollte in Kleinbuchstaben geschrieben sein und kann von doppelten Anführungszeichen umgeben sein, um zu verhindern, dass sie mit einem Token versehen wird, und um Sonderzeichen zu umgehen. Die Zeichen `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` eine besondere Bedeutung haben und sollten mit einem umgekehrten Schrägstrich escaped werden, wenn sie in der Abfragezeichenfolge angezeigt werden. | `default` |
| `qop` | Wendet den AND- oder OR-Operator auf Werte in einem Abfragezeichenfolgenparameter an. | `AND`/`OR` |
| `field` | Optionale Liste von Feldern, auf die die Suche beschränkt werden soll. Dieser Parameter kann wie folgt wiederholt werden: field=field1[,field=field2,…] und (Pfadausdrücke haben die Form von punktgetrennten Pfaden wie _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Sortieren Sie die Ergebnisse nach einer bestimmten Eigenschaft. Durch Hinzufügen eines `-` vor Titel (`orderby=-title`) werden Elemente nach Titel in absteigender Reihenfolge sortiert (Z-A). | `-repo:createdDate` |
| `limit` | Anzahl der zurückgegebenen Fallback-Angebote begrenzen. | `limit=5` |

**Antwort**

Bei einer erfolgreichen Antwort wird eine Liste von Fallback-Angeboten zurückgegeben, die in dem Container vorhanden sind, auf den Sie Zugriff haben.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1",
    "requestTime": "2023-10-22T07:12:30.923768Z",
    "_embedded": {
      "results": [
        {
                "instanceId": "053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2023-09-17T15:18:20.657299Z",
                "repo:lastModifiedDate": "2023-10-02T02:34:48.034583Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "F1: Web fallback ",
                    "xdm:representations": [
                {
                            "xdm:components": [
                        {
                                    "xdm:content": "aaa",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json",
                                    "repo:name": "aa"
                        }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201b2150d98c2"
        },
        {
                            "xdm:components": [
                                {
                                    "xdm:content": "bb",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                                    "dc:format": "text/html",
                                    "repo:name": "bb"
                                }
            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201c34354a2b4"
                        },
                {
                            "xdm:components": [
                        {
                                    "xdm:deliveryURL": "https://mysite.com",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-imagelink",
                                    "dc:format": "image/png",
                                    "repo:name": "ll"
                        }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122207eddb05205a"
                }
            ],
                    "xdm:status": "approved",
                    "xdm:tags": [],
                    "@id": "xcore:fallback-offer:122206064e0d98df"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5#053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 5,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=053bc610-f8f9-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
