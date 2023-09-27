---
title: Erste Schritte mit APIs für die Angebotsbereitstellung
description: Erfahren Sie mehr über die APIs, die zur Bereitstellung personalisierter Angebote verfügbar sind.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 97%

---

# Erste Schritte mit APIs für die Angebotsbereitstellung {#about-decisioning-apis}

Sie können Angebote entweder mithilfe der **Decisioning**- oder **Edge Decisioning**-API bereitstellen. Darüber hinaus ermöglicht Ihnen die API zur **Batch-Entscheidungsfindung**, Angebote an alle Profile in einer bestimmten Zielgruppe durch einen einzigen Aufruf zu senden. Der Angebotsinhalt für jedes Profil in der Zielgruppe wird in einen Adobe Experience Platform-Datensatz platziert, über den er für benutzerdefinierte Batch-Workflows zur Verfügung steht.

Auf dieser Seite finden Sie Informationen zu spezifischen Funktionen, die mit den **Decisioning**- und **Edge Decisioning**-APIs verfügbar sind. Zwar ermöglichen es Ihnen beide, Ihren Kunden Angebote zu unterbreiten, wir empfehlen jedoch, für eingehende Anwendungsfälle möglichst die **Edge Decisioning**-API zu verwenden, um auf Ihrer Plattform eine bessere Latenz und besseren Durchsatz sicherzustellen.


Weiterführende Informationen zur Verwendung der APIs finden Sie in diesen Abschnitten:
* [Decisioning-API](decisioning-api.md)
* [Edge Decisioning-API](edge-decisioning-api.md)
* [Batch Decisioning-API](batch-decisioning-api.md)

## Zugriff auf einen Container verwalten {#manage-access-to-container}

Ein Container ist ein Isolationsmechanismus, der unterschiedliche Aufgaben voneinander trennt. Die Container-ID ist das erste Pfadelement für alle Repository-APIs. Alle Entscheidungsobjekte befinden sich in einem Container.

Ein Administrator kann ähnliche Prinzipale, Ressourcen und Zugriffsberechtigungen in Profilen anordnen. Dies verringert den Verwaltungsaufwand und wird von der [Adobe Admin Console](https://adminconsole.adobe.com/) unterstützt. Sie müssen in Ihrem Unternehmen ein Produktadministrator für Adobe Experience Platform sein, um Profile erstellen und mit Benutzern verknüpfen zu können. Es reicht aus, in einem einmaligen Schritt Produktprofile einzurichten, die bestimmten Berechtigungen entsprechen, und diesen Profilen dann einfach Benutzer hinzuzufügen. Profile dienen als Gruppen, denen Berechtigungen erteilt wurden; alle echten Benutzer oder technischen Benutzer in dieser Gruppe erben diese Berechtigungen.

Mit Administratorberechtigungen können Sie Benutzern Berechtigungen erteilen oder entziehen, indem Sie [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html){target="_blank"}.

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

## Funktionen der Edge Decisioning-API {#edge}

**Eindeutige Anfrage für Erlebnisereignisse und Entscheidungsanfragen**

Mit der Edge Decisioning-API können Sie das Erlebnisereignis zusammen mit der Entscheidungsanfrage in einer einzigen Anfrage anstatt zwei verschiedenen Anfragen senden.

Wenn beispielsweise ein Kunde Ihre Website besucht, enthält die Anfrage das Erlebnisereignis (den Besuch des Kunden auf der Website) und gibt ein Angebot zurück, das auf der besuchten Seite erscheint.

**Kontextdatenspeicherung in Adobe Experience Platform**

Kontextdaten sind Daten, die Sie nur zum Zeitpunkt kennen, zu dem Sie ein Angebot anfordern. Beispielsweise die Farbe des gekauften Artikels, das Wetter zum Zeitpunkt des Kaufs usw.

Beim Übermitteln von Kontextdaten mit einer Edge Decisioning-API-Anfrage werden Daten im Adobe Experience Platform-Profil gespeichert, sodass sie später wiederverwendet werden können.

>[!NOTE]
>
>Damit Kontextdaten gespeichert werden können, muss ein dediziertes XDM-Schema konfiguriert sein.

## Funktionen der Decisioning-API {#decisioning}

Die folgenden Funktionen sind nur mit der Decisioning-API verfügbar. Wenn Sie eine dieser Funktionen benötigen, verwenden Sie die Decisioning-API. Andernfalls empfehlen wir die Verwendung der Edge Decisioning-API.

* **Erlebnisereignisse**: Nutzen Sie Erlebnisereignisse, um Ihre Entscheidungsregeln zu erstellen.
* **Angebotsinhalt und -merkmale**: Sie können festlegen, dass Inhalt und Merkmale eines Angebots nicht über eine eigene Option zurückgegeben werden.
* **Angebotsmetadaten**: Aktivieren Sie eine Option, um die Metadaten eines Angebots zurückzugeben.
* **Zusammenführungsrichtlinie**: Verwenden Sie in Ihrer Anfrage eine andere Zusammenführungsrichtlinie als die Ihrer Sandbox zugeordnete.
* **Entscheidungsereignisse und Frequenzlimitierung**: Hiermit verhindern Sie, dass Entscheidungsereignisse durch eine Frequenzlimitierung gezählt werden.
* **Vorschläge duplizieren**: Aktivieren Sie diese Option, damit Vorschläge nicht dedupliziert werden.
