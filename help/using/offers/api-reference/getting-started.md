---
title: Erste Schritte
description: Erfahren Sie, wie Sie mit der Verwendung der Angebotsbibliothek-API beginnen, um wichtige Vorgänge mithilfe der Entscheidungs-Engine durchzuführen.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# Entwicklerhandbuch zur Entscheidungs-API {#decision-management-api-developer-guide}

Dieses Entwicklerhandbuch enthält Schritte, die Sie bei der Verwendung der [!DNL Offer Library] API. Das Handbuch enthält dann Beispiel-API-Aufrufe für die Ausführung wichtiger Vorgänge mithilfe der Entscheidungs-Engine.

➡️ [Weitere Informationen zu den Komponenten der Entscheidungsverwaltung finden Sie in diesem Video](#video)

## Voraussetzungen {#prerequisites}

Dieses Handbuch setzt ein Verständnis der folgenden Komponenten von Adobe Experience Platform voraus:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}: Der standardisierte Rahmen, durch den [!DNL Experience Platform] organisiert Kundenerlebnisdaten.
   * [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html){target=&quot;_blank&quot;}: Erfahren Sie mehr über die grundlegenden Bausteine von XDM-Schemas.
* [Entscheidungsverwaltung](../../../using/offers/get-started/starting-offer-decisioning.md): Erläutert die Konzepte und Komponenten, die für Erlebnisentscheidungen im Allgemeinen und für das Entscheidungsmanagement im Speziellen verwendet werden. Veranschaulicht die Strategien zur Auswahl der besten Option, die während des Kundenerlebnisses angezeigt werden soll.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;}: PQL ist eine leistungsstarke Sprache zum Schreiben von Ausdrücken über XDM-Instanzen. PQL wird zur Definition von Entscheidungsregeln verwendet.

## Beispiel-API-Aufrufe lesen {#reading-sample-api-calls}

In diesem Handbuch finden Sie Beispiel-API-Aufrufe, die zeigen, wie Sie Ihre Anfragen formatieren. Dazu gehören Pfade, erforderliche Kopfzeilen und ordnungsgemäß formatierte Anfrage-Payloads. Beispiel-JSON, die in API-Antworten zurückgegeben wird, wird ebenfalls bereitgestellt. Informationen zu den Konventionen, die in der Dokumentation für Beispiel-API-Aufrufe verwendet werden, finden Sie im Abschnitt zu [So lesen Sie Beispiel-API-Aufrufe](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;} im [!DNL Experience Platform] Handbuch zur Fehlerbehebung.

## Werte für erforderliche Kopfzeilen sammeln {#gather-values-for-required-headers}

Um Aufrufe an [!DNL Adobe Experience Platform] APIs verwenden, müssen Sie zunächst die [Authentifizierungs-Tutorial](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}. Durch Abschluss des Authentifizierungs-Tutorials werden die Werte für die einzelnen erforderlichen Kopfzeilen in allen [!DNL Experience Platform] API-Aufrufe, wie unten dargestellt:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Für alle Anfragen, die eine Payload enthalten (POST, PUT, PATCH), ist eine zusätzliche Kopfzeile erforderlich:

* `Content-Type: application/json`

## Zugriff auf einen Container verwalten {#manage-access-to-container}

Ein Container ist ein Isolationsmechanismus, der unterschiedliche Anliegen voneinander trennt. Die Container-ID ist das erste Pfadelement für alle Repository-APIs. Alle Entscheidungsobjekte befinden sich in einem Container.

Ein Administrator kann ähnliche Prinzipale, Ressourcen und Zugriffsberechtigungen in Profilen gruppieren. Dies verringert den Verwaltungsaufwand und wird durch [Adobe Admin Console](https://adminconsole.adobe.com/). Sie müssen Produktadministrator für Adobe Experience Platform in Ihrer Organisation sein, um Profile zu erstellen und ihnen Benutzer zuzuweisen. Es reicht aus, in einem einmaligen Schritt Produktprofile zu erstellen, die bestimmten Berechtigungen entsprechen, und diesen Profilen dann einfach Benutzer hinzuzufügen. Profile fungieren als Gruppen, denen Berechtigungen erteilt wurden, und alle echten Benutzer oder technischen Benutzer in dieser Gruppe erben diese Berechtigungen.

Mit Administratorberechtigungen können Sie Benutzern Berechtigungen erteilen oder entziehen, indem Sie [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Weitere Informationen finden Sie unter [Zugriffskontrolle - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html){target=&quot;_blank&quot;}.

### Container auflisten, auf die Benutzer und Integrationen zugreifen können {#list-containers-accessible-to-users-and-integrations}

**API-Format**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtert die Liste der Container nach ihrer Zuordnung zu Produktkontexten. | `acp` |
| `{PROPERTY}` | Filtert den Typ des zurückgegebenen Containers. | `_instance.containerType==decisioning` |

**Anfrage**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reaktion**

Eine erfolgreiche Antwort gibt Informationen zu Entscheidungs-Management-Containern zurück. Dazu gehört eine `instanceId` -Attribut, dessen Wert Ihre Container-ID ist.

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Nächste Schritte {#next-steps}

In diesem Dokument wurden die erforderlichen Kenntnisse zum Aufrufen der [!DNL Offer Library] API, einschließlich der Beschaffung Ihrer Container-ID. Sie können nun mit den Beispielaufrufen in diesem Entwicklerhandbuch fortfahren und den entsprechenden Anweisungen folgen.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Anleitungsvideo {#video}

Das folgende Video soll Ihr Verständnis der Komponenten der Entscheidungsverwaltung unterstützen.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

