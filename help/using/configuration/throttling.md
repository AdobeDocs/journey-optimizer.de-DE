---
solution: Journey Optimizer
product: journey optimizer
title: Einschränkungs-API
description: Erfahren Sie, wie Sie mit der Einschränkungs-API arbeiten
feature: Journeys, API
role: User
level: Beginner
keywords: extern, API, Optimizer, Begrenzung
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: 60cb5e1ba2b5c8cfd0a306a589c85761be1cf657
workflow-type: ht
source-wordcount: '1025'
ht-degree: 100%

---

# Arbeiten mit der Einschränkungs-API

Mit der Drosselungs-API können Sie Ihre Drosselungskonfigurationen erstellen, konfigurieren und überwachen, um die Anzahl der pro Sekunde gesendeten Ereignisse zu begrenzen.

In diesem Abschnitt finden Sie allgemeine Informationen zur Verwendung der API. Eine detaillierte API-Beschreibung finden Sie in der [Dokumentation zu Adobe Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/).

## Wichtige Informationen

* **Eine Konfiguration pro Organisation:** Pro Organisation ist derzeit nur eine Konfiguration zulässig. Eine Konfiguration muss in einer Produktions-Sandbox definiert werden (in den Headern über `x-sandbox-name` angegeben).
* **Anwendung auf Organisationsebene:** Eine Konfiguration wird auf Organisationsebene angewendet.
* **Umgang mit dem API-Limit:** Wenn das im API festgelegte Limit erreicht ist, werden weitere Ereignisse für bis zu 6 Stunden in die Warteschlange gestellt. Dieser Wert kann nicht geändert werden.
* **`maxHttpConnections`-Parameter:** Der Parameter „maxHttpConnections“ ist ein optionaler Parameter im Begrenzungs-API, mit dem Sie die Anzahl der Verbindungen einschränken können, die Journey Optimizer für das externe System öffnet. [Informationen zum Arbeiten mit dem Begrenzungs-API](../configuration/capping.md)

  Wenn Sie die Anzahl der Verbindungen beschränken, aber auch diese externen Aufrufe drosseln möchten, können Sie zwei Konfigurationen für denselben Endpunkt konfigurieren – eine zur Drosselung und eine zur Begrenzung. Beide Konfigurationen können für einen Endpunkt gleichzeitig bestehen. Um „maxHttpConnections“ für einen gedrosselten Endpunkt festzulegen, verwenden Sie das Drosselungs-API, um den Drosselungsschwellenwert festzulegen, und das Begrenzungs-API, um „maxHttpConnections“ festzulegen. Beim Aufrufen des Begrenzungs-APIs können Sie den Begrenzungsschwellenwert auf einen Wert festlegen, der höher ist als der Drosselungsschwellenwert, sodass die Begrenzungsregel tatsächlich nie zur Anwendung kommt.

## Beschreibung des Drosselungs-APIs und Postman-Sammlung {#description}

In der folgenden Tabelle sind die verfügbaren Befehle für das Drosselungs-API aufgeführt. Ausführliche Informationen, einschließlich Anfragebeispielen, Parametern und Antwortformaten, finden Sie in der [Dokumentation zu den Adobe Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

| Methode | Pfad | Beschreibung |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | Abrufen einer Liste der Drosselungskonfigurationen |
| [!DNL POST] | /throttlingConfigs | Erstellen einer Drosselungskonfiguration |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | Bereitstellen einer Drosselungskonfiguration |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | Bereitstellung einer Drosselungskonfiguration aufheben |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | Überprüfen, ob eine Drosselungskonfiguration bereitgestellt werden kann oder nicht |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | Aktualisieren einer Drosselungskonfiguration |
| [!DNL GET] | /throttlingConfigs/`{uid}` | Abrufen einer Drosselungskonfiguration |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | Löschen einer Drosselungskonfiguration |

Darüber hinaus steht Ihnen [hier](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json) – zur Unterstützung bei Ihrer Testkonfiguration – eine Postman-Sammlung zur Verfügung.

Diese Sammlung wurde eingerichtet, um die Postman-Variablensammlung freizugeben, die über __[Integrationen der Adobe I/O-Konsole](https://console.adobe.io/integrations) > Testen > Für Postman herunterladen__ generiert wurde. Dadurch wird eine Postman-Umgebungsdatei mit den ausgewählten Integrationswerten erzeugt.

Nach dem Herunterladen und Hochladen in Postman müssen Sie drei Variablen hinzufügen: `{JO_HOST}`, `{BASE_PATH}` und `{SANDBOX_NAME}`.
* `{JO_HOST}`: [!DNL Journey Optimizer]-Gateway-URL.
* `{BASE_PATH}` : Einstiegspunkt für die API.
* `{SANDBOX_NAME}`: der Header **x-sandbox-name** (z. B. „prod“), der dem Sandbox-Namen entspricht, in dem die API-Vorgänge stattfinden. Weiterführende Informationen dazu finden Sie unter [Sandbox-Übersicht](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=de).

## Drosselungskonfiguration{#configuration}

Hier finden Sie die Struktur einer Drosselungskonfiguration. Die Attribute **name** und **description** sind optional.

```
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

Beispiel:

```
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

>[!IMPORTANT]
>
>Die Konfiguration ist erst aktiv, nachdem der Endpunkt **Bereitstellen** aufgerufen wurde.

## Fehler

Beim Erstellen oder Aktualisieren einer Konfiguration validiert der Prozess die angegebene Konfiguration und gibt den Validierungsstatus zurück, der durch seine eindeutige ID identifiziert wird, entweder:

```
"ok" or "error"
```

>[!IMPORTANT]
>
>Die Attribute **maxThroughput**, **urlPattern** und **methods** sind zwingend erforderlich.
>
>Der Wert für **maxThroughput** muss zwischen 200 und 5000 liegen.

Beim Erstellen, Löschen oder Bereitstellen einer Drosselungskonfiguration können die folgenden Fehler auftreten:

* **ERR_THROTTLING_CONFIG_100**: Drosselungskonfiguration: `<mandatory attribute>` erforderlich
* **ERR_THROTTLING_CONFIG_101**: Drosselungskonfiguration: maxThroughput ist erforderlich und muss größer oder gleich 200 und kleiner oder gleich 5.000 sein.
* **ERR_THROTTLING_CONFIG_104**: Drosselungskonfiguration: fehlerhaftes URL-Muster
* **ERR_THROTTLING_CONFIG_105**: Drosselungskonfiguration: Platzhalter sind im Host-Teil des URL-Musters nicht zulässig
* **ERR_THROTTLING_CONFIG_106**: Drosselungskonfiguration: ungültige Payload
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456**, „Eine bereitgestellte Drosselungskonfiguration kann nicht gelöscht werden. Bitte die Bereitstellung vor dem Löschen aufheben“
* **THROTTLING_CONFIG_DELETE_ERROR: 1457**, „Die Drosselungskonfiguration kann nicht gelöscht werden: unerwarteter Fehler“
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458**, „Die Drosselungskonfiguration kann nicht bereitgestellt werden: unerwarteter Fehler“
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459**, „Die Bereitstellung der Drosselungskonfiguration kann nicht aufgehoben werden: unerwarteter Fehler“
* **THROTTLING_CONFIG_GET_ERROR: 1460**, „Drosselungskonfiguration kann nicht abgerufen werden: unerwarteter Fehler“
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461**, „Drosselungskonfiguration kann nicht aktualisiert werden: Laufzeitversion ist nicht aktiv“
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462**, „Drosselungskonfiguration kann nicht aktualisiert werden: unerwarteter Fehler“
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463**, „Vorgang bei Drosselungskonfiguration nicht zulässig: Nicht-Produktions-Sandbox“
* **THROTTLING_CONFIG_CREATE_ERROR: 1464**, „Drosselungskonfiguration kann nicht erstellt werden: unerwarteter Fehler“
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465**, „Drosselungskonfiguration kann nicht erstellt werden: nur eine Konfiguration pro Organisation zulässig“
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 14466**, „Drosselungskonfiguration kann nicht bereitgestellt werden: bereits bereitgestellt“
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 14467**, „Drosselungskonfiguration nicht gefunden“
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 14468**, „Bereitstellung der Drosselungskonfiguration kann nicht aufgehoben werden: noch nicht bereitgestellt“

**Fehlerbeispiele**

Beim Versuch, eine Konfiguration für Nicht-Produktions-Sandboxes zu erstellen:

```
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

Falls eine angegebene Sandbox nicht vorhanden ist:

```
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

Beim Versuch, eine weitere Konfiguration zu erstellen:

```
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## Lebenszyklus der Konfiguration auf Laufzeitebene {#config}

Wenn die Bereitstellung einer Konfiguration aufgehoben wird, wird sie auf Laufzeitebene als inaktiv markiert und ausstehende Ereignisse werden 24 Stunden lang weiter verarbeitet. Sie wird dann im Laufzeit-Service gelöscht.

Nachdem die Bereitstellung einer Konfiguration aufgehoben wurde, ist es möglich, die Konfiguration zu aktualisieren und erneut bereitzustellen. Dadurch wird eine neue Laufzeitkonfiguration erstellt, die bei der bevorstehenden Aktionsausführung berücksichtigt wird.

Beim Aktualisieren einer bereits bereitgestellten Konfiguration werden die neuen Werte sofort berücksichtigt. Die zugrunde liegenden Systemressourcen werden automatisch angepasst. Dies ist im Vergleich zum Aufheben der Bereitstellung und dem erneuten Bereitstellen der Konfiguration optimal.

## Beispiele für Antworten {#responses}

**Erstellung – POST**

```
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**Aktualisieren – PUT**

```
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**Lesen (nach Aktualisierung) – GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**Lesen (nach Bereitstellung) – GET**

```
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## Anwendungsfälle {#uc}

In diesem Abschnitt werden wichtige Anwendungsfälle für die Verwaltung von Drosselungskonfigurationen in [!DNL Journey Optimizer] und die zugehörigen API-Befehle aufgelistet, die zur Implementierung des jeweiligen Anwendungsfalls erforderlich sind.

Details zu den einzelnen API-Befehlen finden Sie unter [API-Beschreibung und Postman-Sammlung](#description).

+++Erstellen und Bereitstellen einer neuen Drosselungskonfiguration

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`create`**: Erstellt eine neue Konfiguration.
1. **`candeploy`**: Prüft, ob die Konfiguration bereitgestellt werden kann.
1. **`deploy`**: Stellt die Konfiguration bereit.

+++

+++Aktualisieren und Bereitstellen einer (noch nicht bereitgestellten) Drosselungskonfiguration

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`get`**: Ruft Details zu einer bestimmten Konfiguration ab.
1. **`update`**: Ändert die Konfiguration.
1. **`candeploy`**: Prüft die Eignung der Bereitstellung.
1. **`deploy`**: Stellt die Konfiguration bereit.

+++

+++Aufheben der Bereitstellung und Löschen einer bereitgestellten Drosselungskonfiguration

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`undeploy`**: Hebt die Bereitstellung der Konfiguration auf.
1. **`delete`**: Entfernt die Konfiguration.

+++

+++Löschen einer bereitgestellten Drosselungskonfiguration

In nur einem API-Aufruf können Sie mithilfe des Parameters `forceDelete` die Bereitstellung aufheben und die Konfiguration löschen.

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`delete`(mit dem Parameter `forceDelete`)**: Erzwingt die Löschung einer bereitgestellten Konfiguration in einem einzigen Schritt.

+++

+++Aktualisieren einer bereits bereitgestellten Drosselungskonfiguration

>[!NOTE]
>
>Es ist nicht erforderlich, die Bereitstellung der Konfiguration vor der Aktualisierung aufzuheben

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`get`**: Ruft Details zu einer bestimmten Konfiguration ab.
1. **`update`**: Ändert die Konfiguration.

+++
