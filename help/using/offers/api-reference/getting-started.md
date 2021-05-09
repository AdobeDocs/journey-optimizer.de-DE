---
title: Erste Schritte
description: Erfahren Sie, wie Sie mit der Angebot-Bibliotheks-API Beginn ausführen, um wichtige Vorgänge mit der Entscheidungsverwaltungsmodul durchzuführen.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Entwicklerhandbuch für die Entscheidungs-API

In diesem Entwicklerhandbuch finden Sie Anweisungen, wie Sie mit der [!DNL Offer Library]-API Beginn ausführen können. Das Handbuch bietet dann Beispiel-API-Aufrufe für die Ausführung wichtiger Vorgänge mithilfe der Entscheidungsverwaltungsmodul.

![](../assets/do-not-localize/how-to-video.png) [Diese Funktion im Video entdecken](#video)

## Voraussetzungen

Dieses Handbuch erfordert ein Verständnis der folgenden Komponenten von Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html): Das standardisierte Framework, mit dem Kundenerlebnisdaten  [!DNL Experience Platform] organisiert werden.
   * [Grundlagen der Zusammensetzung](https://docs.adobe.com/content/help/en/experience-platform/xdm/schema/composition.html) des Schemas: Erfahren Sie mehr über die grundlegenden Bausteine von XDM-Schemas.
* [Entscheidungsverwaltung](../../../using/offers/get-started/starting-offer-decisioning.md): Erläutert die Konzepte und Komponenten, die für die Experience Decision im Allgemeinen und für die Offer decisioning im Besonderen verwendet werden. Veranschaulicht die Strategien zur Auswahl der besten Option, die während des Kundenerlebnisses angezeigt werden soll.
* [[!DNL Profile Query Language (PQL)]](https://docs.adobe.com/content/help/en/experience-platform/segmentation/pql/overview.html): PQL ist eine leistungsstarke Sprache, um Ausdruck über XDM-Instanzen zu schreiben. PQL wird zur Definition von Entscheidungsregeln verwendet.

## Lesen von Beispiel-API-Aufrufen

In diesem Handbuch finden Sie Beispiele für API-Aufrufe, die zeigen, wie Sie Ihre Anforderungen formatieren. Dazu gehören Pfade, erforderliche Kopfzeilen und ordnungsgemäß formatierte Anforderungs-Nutzdaten. Beispiel-JSON, die in API-Antworten zurückgegeben wird, wird ebenfalls bereitgestellt. Informationen zu den Konventionen, die in der Dokumentation für Beispiel-API-Aufrufe verwendet werden, finden Sie im Abschnitt [Anleitung zum Lesen von Beispiel-API-Aufrufen](https://docs.adobe.com/content/help/en/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request) im Handbuch [!DNL Experience Platform] zur Fehlerbehebung.

## Werte für erforderliche Kopfzeilen sammeln

Um Aufrufe an APIs für [!DNL Platform] durchzuführen, müssen Sie zunächst das [Authentifizierungstutorial](https://docs.adobe.com/content/help/en/experience-platform/tutorials/authentication.html) abschließen. Wenn Sie das Authentifizierungstreutorial abschließen, werden die Werte für die einzelnen erforderlichen Kopfzeilen in allen [!DNL Experience Platform]-API-Aufrufen bereitgestellt, wie unten dargestellt:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Für alle Anforderungen mit einer Nutzlast (POST, PUT, PATCH) ist ein zusätzlicher Header erforderlich:

* `Content-Type: application/json`

## Zugriff auf einen Container verwalten

Ein Container ist ein Isolationsmechanismus, der unterschiedliche Anliegen voneinander trennt. Die Container-ID ist das erste Pfadelement für alle Repository-APIs. Alle Entscheidungsobjekte befinden sich in einem Container.

Ein Administrator kann ähnliche Prinzipale, Ressourcen und Zugriffsberechtigungen in Profilen gruppieren. Dies verringert den Verwaltungsaufwand und wird von [Adobe Admin Console](https://adminconsole.adobe.com/) unterstützt. Sie müssen Produktadministrator für Adobe Experience Platform in Ihrem Unternehmen sein, um Profile zu erstellen und Benutzer zuzuweisen. Es reicht aus, Produktanpassungen zu erstellen, die bestimmten Berechtigungen in einem einmaligen Schritt entsprechen, und diese Profil dann einfach zu diesen Profilen hinzuzufügen. Profil fungieren als Gruppen, denen Berechtigungen erteilt wurden, und alle echten Benutzer oder technischen Benutzer in dieser Gruppe erben diese Berechtigungen.

Mit Administratorberechtigungen können Sie Benutzern über das [Adobe Admin Console](https://adminconsole.adobe.com/) Berechtigungen erteilen oder entziehen. Weitere Informationen finden Sie unter [Übersicht über die Zugriffskontrolle](https://docs.adobe.com/content/help/en/experience-platform/access-control/home.html).

### Benutzerfreundliche Liste-Container und Integrationen

**API-Format**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filter der Liste von Containern durch ihre Verbindung zu den Kontexten der Produkte. | `acp` |
| `{PROPERTY}` | Filter des zurückgegebenen Containers. | `_instance.containerType==decisioning` |

**Anforderung**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reaktion**

Bei einer erfolgreichen Antwort werden Informationen zu Containern des Entscheidungsmanagements zurückgegeben. Dazu gehört ein `instanceId`-Attribut, dessen Wert Ihre Container-ID ist.

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

## Nächste Schritte

Dieses Dokument deckte die erforderlichen Kenntnisse ab, um Aufrufe an die [!DNL Offer Library]-API durchzuführen, einschließlich des Erwerbs Ihrer Container-ID. Sie können nun zu den Beispielaufrufen in diesem Entwicklerhandbuch fortfahren und deren Anweisungen folgen.

## Lernvideo {#video}

Das folgende Video soll Ihnen dabei helfen, die Komponenten von Decision Management besser zu verstehen.

>[!NOTE]
>
>Dieses Video bezieht sich auf den auf Adobe Experience Platform aufbauenden Offer decisioning-Anwendungsdienst. Sie enthält jedoch allgemeine Leitlinien für die Verwendung von Angebot im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
