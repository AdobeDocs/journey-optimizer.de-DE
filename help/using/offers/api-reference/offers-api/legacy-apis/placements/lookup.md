---
title: Nachschlagen einer Platzierung
description: Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 42fb17a2-842e-4e20-9013-7227adba0105
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 100%

---

# Nachschlagen einer Platzierung {#look-up-placement}

Sie können einzelne Platzierungen nachschlagen, indem Sie eine GET-Anfrage an die [!DNL Offer Library]-API richten, die entweder die Platzierungs-`@id` oder den Namen der Platzierung im Anfragepfad enthält.

**API-Format**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Platzierungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Definiert das Schema, das Platzierungen zugeordnet ist. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `id` | Eine Zeichenfolge, die zum Abgleich der `@id`-Eigenschaft der Entitäten dient. Die Zeichenfolge wird exakt abgeglichen. Die Parameter `id` und `name` können nicht zusammen verwendet werden. | `xcore:offer-placement:124541309805b7e8` |
| `name` | Eine Zeichenfolge, die zum Abgleich der Eigenschaft xdm:name der Entitäten verwendet wird. Die Zeichenfolge wird exakt abgeglichen (mit Groß-/Kleinschreibung), es können jedoch Platzhalter genutzt werden. Die Parameter `id` und `name` können nicht zusammen verwendet werden. | `Sales and Promotions Placement` |

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&name=Sales%20and%20Promotions%20Placement' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema='\''https://ns.adobe.com/experience/xcore/hal/results'\''' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden die Details der Platzierung zurückgegeben, einschließlich Informationen zu Ihrer Container-ID, Instanz-ID und der eindeutigen Platzierungs-`@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2020-10-21T20:04:53.656503Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
    ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-21T19:57:09.837456Z",
                "repo:lastModifiedDate": "2020-10-21T19:59:10.700149Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Sales and Promotions Placement",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "A test placement to contain offers of sales and discounts",
                    "@id": "xcore:offer-placement:124e0be5699743d3"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#9aa58fd0-13d7-11eb-928b-576735ea4db8",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&name=Sales%20and%20Promotions%20Placement",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
