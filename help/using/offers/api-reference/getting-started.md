---
title: Erste Schritte
description: Beginn der Nutzung der API einer Angebotsbibliothek, um wichtige Operationen unter Verwendung der Decisioning-Engine durchzuführen.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 100%

---

# Entwicklerhandbuch für die Entscheidungs-Management-API {#decision-management-api-developer-guide}

In diesem Entwicklerhandbuch finden Sie Anweisungen, wie Sie mit der Verwendung der [!DNL Offer Library]-API beginnen können. Das Handbuch enthält Beispiel-API-Aufrufe für die Durchführung wichtiger Operationen mit der Decisioning-Engine.

➡️ [Weitere Informationen zu den Komponenten des Entscheidungs-Managements finden Sie in diesem Video](#video)

## Voraussetzungen {#prerequisites}

Dieses Handbuch setzt ein Verständnis der folgenden Komponenten von Adobe Experience Platform voraus:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target=&quot;_blank&quot;}: Das standardisierte Framework, mit dem [!DNL Experience Platform] Kundenerlebnisdaten organisiert.
   * [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de){target=&quot;_blank&quot;}: Erfahren Sie mehr über die Grundbausteine von XDM-Schemas.
* [Entscheidungs-Management](../../../using/offers/get-started/starting-offer-decisioning.md): Beschreibt die Konzepte und Komponenten der Erlebnis-Entscheidungsfindung im Allgemeinen und insbesondere des Entscheidungs-Managements. Veranschaulicht die Strategien zur Auswahl der besten Option, die während eines Kundenerlebnisses angezeigt wird.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=de){target=&quot;_blank&quot;}: PQL ist eine leistungsstarke Sprache zum Schreiben von Ausdrücken auf XDM-Instanzen. Zur Definition von Entscheidungsregeln wird PQL verwendet.

## Lesen von Beispiel-API-Aufrufen {#reading-sample-api-calls}

In diesem Handbuch wird anhand von Beispielen für API-Aufrufe die korrekte Formatierung von Anfragen aufgezeigt. Dazu gehören Pfade, erforderliche Kopfzeilen und ordnungsgemäß formatierte Anfrage-Payloads. Außerdem wird ein Beispiel für eine von der API im JSON-Format zurückgegebene Antwort bereitgestellt. Informationen zu den Konventionen, die in der Dokumentation für Beispiel-API-Aufrufe verwendet werden, finden Sie im Abschnitt zum [Lesen von Beispiel-API-Aufrufen](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=de#how-do-i-format-an-api-request){target=&quot;_blank&quot;} im Fehlerbehebungshandbuch für [!DNL Experience Platform].

## Sammeln von Werten für erforderliche Kopfzeilen {#gather-values-for-required-headers}

Um [!DNL Adobe Experience Platform]-APIs aufzurufen, müssen Sie zunächst das [Authentifizierungs-Tutorial](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=de){target=&quot;_blank&quot;} abschließen. Durch Abschluss des Authentifizierungs-Tutorials werden die Werte für die einzelnen erforderlichen Header in allen [!DNL Experience Platform]-API-Aufrufen bereitgestellt, wie unten dargestellt:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Bei allen Anfragen mit einer Payload (POST, PUT, PATCH) ist eine zusätzliche Kopfzeile erforderlich:

* `Content-Type: application/json`

## Zugriff auf einen Container verwalten {#manage-access-to-container}

Ein Container ist ein Isolationsmechanismus, der unterschiedliche Aufgaben voneinander trennt. Die Container-ID ist das erste Pfadelement für alle Repository-APIs. Alle Entscheidungsobjekte befinden sich in einem Container.

Ein Administrator kann ähnliche Prinzipale, Ressourcen und Zugriffsberechtigungen in Profilen anordnen. Dies verringert den Verwaltungsaufwand und wird von der [Adobe Admin Console](https://adminconsole.adobe.com/) unterstützt. Sie müssen in Ihrem Unternehmen ein Produktadministrator für Adobe Experience Platform sein, um Profile erstellen und mit Benutzern verknüpfen zu können. Es reicht aus, in einem einmaligen Schritt Produktprofile einzurichten, die bestimmten Berechtigungen entsprechen, und diesen Profilen dann einfach Benutzer hinzuzufügen. Profile dienen als Gruppen, denen Berechtigungen erteilt wurden; alle echten Benutzer oder technischen Benutzer in dieser Gruppe erben diese Berechtigungen.

Mit Administratorberechtigungen können Sie Benutzern über die [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} Berechtigungen erteilen oder entziehen. Weiterführende Informationen finden Sie in der [Übersicht zur Zugriffskontrolle](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=de){target=&quot;_blank&quot;}.

### Container auflisten, die für Benutzer und Integrationen zugänglich sind {#list-containers-accessible-to-users-and-integrations}

**API-Format**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtert die Liste mit Containern anhand ihrer Verknüpfung mit Produktkontexten. | `acp` |
| `{PROPERTY}` | Filtert die Art des zurückgegebenen Containers. | `_instance.containerType==decisioning` |

**Anfrage**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort werden Informationen zu Entscheidungs-Management-Containern zurückgegeben. Dazu gehört ein `instanceId`-Attribut, dessen Wert Ihre Container-ID ist.

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

In diesem Dokument ging es um die vorausgesetzten Kenntnisse, die zum Ausführen von Aufrufen an die [!DNL Offer Library]-API benötigt werden, einschließlich der Beschaffung Ihrer Container-ID. Sie können nun mit den Beispielaufrufen in diesem Entwicklerhandbuch fortfahren und den entsprechenden Anweisungen folgen.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Anleitungsvideo {#video}

Im folgenden Video werden die Komponenten des Entscheidungs-Managements erklärt.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

