---
solution: Journey Optimizer
product: journey optimizer
title: Capping-API
description: Erfahren Sie, wie man mit der Capping-API arbeitet.
feature: Journeys, API
role: User
level: Beginner
keywords: extern, API, Optimizer, Begrenzung
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 9f801b1fdcab38bffff851675eca5e2fb61dfbf9
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 93%

---

# Arbeiten mit der Capping-API {#work}

Mit der Capping-API können Sie Begrenzungskonfigurationen erstellen, konfigurieren und überwachen.

In diesem Abschnitt finden Sie allgemeine Informationen zur Verwendung der API. Eine detaillierte API-Beschreibung finden Sie in der [Dokumentation zu Adobe Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/).

## Beschreibung des Begrenzungs-APIs und Postman-Sammlung {#description}

In der folgenden Tabelle sind die verfügbaren Befehle für das Begrenzungs-API aufgeführt. Ausführliche Informationen, einschließlich Anfragebeispielen, Parametern und Antwortformaten, finden Sie in der [Dokumentation zu den Adobe Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

| Methode | Pfad | Beschreibung |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | Liste der Endpunktbegrenzungskonfigurationen abrufen |
| [!DNL POST] | /endpointConfigs | Endpunktbegrenzungskonfiguration erstellen |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | Endpunktbegrenzungskonfiguration bereitstellen |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | Bereitstellung einer Endpunktbegrenzungskonfiguration aufheben |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | Überprüfen, ob eine Endpunktbegrenzungskonfiguration bereitgestellt werden kann oder nicht |
| [!DNL PUT] | /endpointConfigs/`{uid}` | Endpunktbegrenzungskonfiguration aktualisieren |
| [!DNL GET] | /endpointConfigs/`{uid}` | Endpunktbegrenzungskonfiguration abrufen |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | Endpunktbegrenzungskonfiguration löschen |

Bei der Erstellung oder Aktualisierung einer Konfiguration wird automatisch eine Überprüfung durchgeführt, um die Syntax und Integrität der Payload sicherzustellen.
Wenn Probleme auftreten, gibt der Vorgang eine Warnung oder Fehler zurück, die Ihnen beim Korrigieren der Konfiguration helfen.

Darüber hinaus steht Ihnen [hier](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) – zur Unterstützung bei Ihrer Testkonfiguration – eine Postman-Sammlung zur Verfügung.

Diese Sammlung wurde eingerichtet, um die Postman-Variablensammlung freizugeben, die über __[Integrationen der Adobe I/O-Konsole](https://console.adobe.io/integrations) > Testen > Für Postman herunterladen__ generiert wurde. Dadurch wird eine Postman-Umgebungsdatei mit den ausgewählten Integrationswerten erzeugt.

Nach dem Herunterladen und Hochladen in Postman müssen Sie drei Variablen hinzufügen: `{JO_HOST}`, `{BASE_PATH}` und `{SANDBOX_NAME}`.
* `{JO_HOST}`: [!DNL Journey Optimizer]-Gateway-URL.
* `{BASE_PATH}` : Einstiegspunkt für die API.
* `{SANDBOX_NAME}`: der Header **x-sandbox-name** (z. B. „prod“), der dem Sandbox-Namen entspricht, in dem die API-Vorgänge stattfinden. Weiterführende Informationen dazu finden Sie unter [Sandbox-Übersicht](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=de).

## Endpunktkonfiguration

Die grundlegende Struktur einer Endpunktkonfiguration sieht wie folgt aus:

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>Der Parameter **maxHttpConnections** ist optional. Dadurch können Sie die Anzahl der Verbindungen einschränken, die Journey Optimizer für das externe System öffnet.
>
>Der maximale Wert, der festgelegt werden kann, ist 400. Wenn nichts angegeben ist, kann das System abhängig von seiner dynamischen Skalierung bis zu mehreren tausend Verbindungen öffnen.
>
>Wenn bei der Bereitstellung der Begrenzungskonfiguration kein Wert für „maxHttpConnection“ angegeben wurde, wird der bereitgestellten Konfiguration der Standardwert „maxHttpConnection = -1“ hinzugefügt, was bedeutet, dass Journey Optimizer den Standardwert des Systems verwendet.

Beispiel:

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>Die Konfiguration ist erst aktiv, nachdem der Endpunkt **Bereitstellen** aufgerufen wurde.

## Warnung und Fehler

Wenn eine **canDeploy**-Methode aufgerufen wird, validiert der Prozess die Konfiguration und gibt den durch seine eindeutige Kennung identifizierten Validierungsstatus zurück:

```
"ok" or "error"
```

Mögliche Fehler sind:

* **ERR_ENDPOINTCONFIG_100**: capping config: missing or invalid url
* **ERR_ENDPOINTCONFIG_101**: capping config: malformed url
* **ERR_ENDPOINTCONFIG_102**: Begrenzungskonfiguration: fehlerhafte URL: Platzhalter in URL im Host nicht zulässig:port
* **ERR_ENDPOINTCONFIG_103**: capping config: missing HTTP methods
* **ERR_ENDPOINTCONFIG_104**: capping config: no call rating defined
* **ERR_ENDPOINTCONFIG_107**: capping config: invalid max calls count (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: capping config: invalid max calls count (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: capping config: can&#39;t create endpoint config: invalid payload
* **ERR_ENDPOINTCONFIG_112**: capping config: can&#39;t create endpoint config: expecting a JSON payload
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: invalid service name `<!--<given value>-->`: must be &#39;dataSource&#39; or &#39;action&#39;

Die potenzielle Warnung lautet:

**ERR_ENDPOINTCONFIG_106**: capping config: max HTTP connections not defined: no limitation by default

## Anwendungsfälle

In diesem Abschnitt werden wichtige Anwendungsfälle für die Verwaltung von Begrenzungskonfigurationen in [!DNL Journey Optimizer] und die zugehörigen API-Befehle aufgelistet, die zur Implementierung des jeweiligen Anwendungsfalls erforderlich sind.

Details zu den einzelnen API-Befehlen finden Sie unter [API-Beschreibung und Postman-Sammlung](#description).

+++Erstellen und Bereitstellen einer neuen Begrenzungskonfiguration

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`create`**: Erstellt eine neue Konfiguration.
1. **`candeploy`**: Prüft, ob die Konfiguration bereitgestellt werden kann.
1. **`deploy`**: Stellt die Konfiguration bereit.

+++

+++Aktualisieren und Bereitstellen einer Begrenzungskonfiguration (noch nicht bereitgestellt)

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`get`**: Ruft Details zu einer bestimmten Konfiguration ab.
1. **`update`**: Ändert die Konfiguration.
1. **`candeploy`**: Prüft die Eignung der Bereitstellung.
1. **`deploy`**: Stellt die Konfiguration bereit.

+++

+++Aufheben der Bereitstellung und Löschen einer bereitgestellten Begrenzungskonfiguration

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`undeploy`**: Hebt die Bereitstellung der Konfiguration auf.
1. **`delete`**: Entfernt die Konfiguration.

+++

+++Löschen einer bereitgestellten Begrenzungskonfiguration in einem Schritt

In nur einem API-Aufruf können Sie mithilfe des Parameters `forceDelete` die Bereitstellung aufheben und die Konfiguration löschen.

Zu verwendende API-Aufrufe:

1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`delete`(mit dem Parameter `forceDelete`)**: Erzwingt die Löschung einer bereitgestellten Konfiguration in einem einzigen Schritt.

+++

+++Aktualisieren einer bereits bereitgestellten Begrenzungskonfiguration

>[!NOTE]
>
>Nach dem Aktualisieren einer bereits bereitgestellten Konfiguration ist eine erneute Bereitstellung erforderlich.

Zu verwendende API-Aufrufe:
1. **`list`**: Ruft vorhandene Konfigurationen ab.
1. **`get`**: Ruft Details zu einer bestimmten Konfiguration ab.
1. **`update`**: Ändert die Konfiguration.
1. **`undeploy`**: Hebt die Bereitstellung der Konfiguration auf, bevor Änderungen angewendet werden.
1. **`candeploy`**: Prüft die Eignung der Bereitstellung.
1. **`deploy`**: Stellt die aktualisierte Konfiguration bereit.

+++
