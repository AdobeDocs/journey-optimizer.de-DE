---
solution: Journey Optimizer
product: journey optimizer
title: Begrenzungs-API
description: Erfahren Sie, wie Sie mit der Begrenzungs-API arbeiten
feature: Journeys, API
role: Developer
level: Beginner
keywords: extern, API, Optimizer, Begrenzung
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
TQID: https://experienceleague.adobe.com/004R6qxDnmHDaqIT7IJ1mm2yp-s6RvsJFeElaXwRg9A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 0%

---

# Arbeiten mit der Begrenzungs-API {#work}

Mit der Begrenzungs-API können Sie Begrenzungskonfigurationen erstellen, konfigurieren und überwachen.

Dieser Abschnitt enthält allgemeine Informationen zur Arbeit mit der -API. Eine detaillierte API-Beschreibung finden Sie in der Dokumentation zu [Adobe Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}.

## Beschreibung der Begrenzungs-API und Postman-Sammlung {#description}

In der folgenden Tabelle sind die verfügbaren Befehle für die Begrenzungs-API aufgeführt. Detaillierte Informationen, einschließlich Anfragebeispielen, Parametern und Antwortformaten, finden Sie in der Dokumentation zu den [Adobe Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"}.

| Methode | Pfad | Beschreibung |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | Abrufen einer Liste der Endpunkt-Begrenzungskonfigurationen |
| [!DNL POST] | /endpointConfigs | Erstellen einer Endpunkt-Begrenzungskonfiguration |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | Bereitstellen einer Endpunkt-Begrenzungskonfiguration |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | Bereitstellung einer Endpunkt-Begrenzungskonfiguration aufheben |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | Überprüfen, ob eine Endpunktbegrenzungskonfiguration bereitgestellt werden kann oder nicht |
| [!DNL PUT] | /endpointConfigs/`{uid}` | Aktualisieren einer Endpunkt-Begrenzungskonfiguration |
| [!DNL GET] | /endpointConfigs/`{uid}` | Abrufen einer Endpunkt-Begrenzungskonfiguration |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | Löschen einer Endpunkt-Begrenzungskonfiguration |

Wenn eine Konfiguration erstellt oder aktualisiert wird, wird automatisch eine Prüfung durchgeführt, um die Syntax und Integrität der Payload zu gewährleisten.
Wenn Probleme auftreten, gibt der Vorgang eine Warnung oder Fehler zurück, die Sie bei der Korrektur der Konfiguration unterstützen.

Darüber hinaus ist eine Postman-Sammlung [hier](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) verfügbar, die Sie bei Ihrer Testkonfiguration unterstützt.

Diese Sammlung wurde eingerichtet, um die Postman-Variablensammlung freizugeben, die über die Integrationen der __[Adobe I/O-Konsole](https://console.adobe.io/integrations) > Ausprobieren > Für Postman herunterladen__ generiert wurde. Dadurch wird eine Postman-Umgebungsdatei mit den ausgewählten Integrationswerten generiert.

Nach dem Herunterladen und Hochladen in Postman müssen Sie drei Variablen hinzufügen: `{JO_HOST}`, `{BASE_PATH}` und `{SANDBOX_NAME}`.

* `{JO_HOST}` : [!DNL Journey Optimizer] Gateway-URL.
* `{BASE_PATH}` : Einstiegspunkt für die API.
* `{SANDBOX_NAME}` : die Kopfzeile **x-sandbox-name** (z. B. „prod„), die dem Sandbox-Namen entspricht, in dem die API-Vorgänge ausgeführt werden. Weitere Informationen finden Sie [&#x200B; „Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=de){target="_blank"}Übersicht“.

## Endpunktkonfiguration

Im Folgenden finden Sie die grundlegende Struktur einer Endpunktkonfiguration:

```json
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
>Der **maxHttpConnections**-Parameter ist optional. Damit können Sie die Anzahl der Verbindungen einschränken, die Journey Optimizer mit dem externen System herstellen soll.
>
>Der maximal einstellbare Wert ist 400. Wenn nichts angegeben ist, kann sich das System je nach dynamischer Skalierung des Systems für mehrere Tausend Verbindungen öffnen.
>
>Wenn bei der Bereitstellung der Begrenzungskonfiguration kein `maxHttpConnections` festgelegt wurde, wird der bereitgestellten Konfiguration ein `maxHttpConnections = -1` hinzugefügt, und Journey Optimizer verwendet den standardmäßigen Systemwert.

Beispiel:

```json
{
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
>Die Konfiguration ist erst aktiv, nachdem der Endpunkt **deploy“ aufgerufen**.

## Warnung und Fehler

Wenn eine **canDeploy**-Methode aufgerufen wird, validiert der Prozess die Konfiguration und gibt den Validierungsstatus zurück, der durch seine eindeutige ID identifiziert wird, entweder:

```json
"ok" or "error"
```

Mögliche Fehler sind:

* **ERR_ENDPOINTCONFIG_100**: Begrenzungskonfiguration: fehlende oder ungültige URL
* **ERR_ENDPOINTCONFIG_101**: Begrenzungskonfiguration: fehlerhafte URL
* **ERR_ENDPOINTCONFIG_102**: Begrenzungskonfiguration: fehlerhafte URL: Platzhalter in URL im Host nicht zulässig:port
* **ERR_ENDPOINTCONFIG_103**: Begrenzungskonfiguration: fehlende HTTP-Methoden
* **ERR_ENDPOINTCONFIG_104**: Begrenzungskonfiguration: Keine Aufrufbewertung definiert
* **ERR_ENDPOINTCONFIG_107**: Begrenzungskonfiguration: Ungültige maximale Anzahl von Aufrufen (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: Begrenzungskonfiguration: Ungültige maximale Anzahl von Aufrufen (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: Begrenzungskonfiguration: Endpunktkonfiguration kann nicht erstellt werden: ungültige Payload
* **ERR_ENDPOINTCONFIG_112**: Begrenzungskonfiguration: Endpunktkonfiguration kann nicht erstellt werden: JSON-Payload wird erwartet
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: Ungültiger Dienstname `<!--<given value>-->`: muss &#39;dataSource&#39; oder &#39;action&#39; sein

Die potenzielle Warnung lautet:

**ERR_ENDPOINTCONFIG_106**: Begrenzungskonfiguration: Max. HTTP-Verbindungen nicht definiert: Standardmäßig keine Einschränkung

## Anwendungsbeispiele

In diesem Abschnitt werden wichtige Anwendungsfälle für die Verwaltung von Begrenzungskonfigurationen in [!DNL Journey Optimizer] und die zugehörigen API-Befehle aufgelistet, die zur Implementierung des Anwendungsfalls erforderlich sind.

Details zu den einzelnen API-Befehlen finden Sie unter [API-Beschreibung und Postman-Sammlung](#description).

+++Erstellen und Bereitstellen einer neuen Begrenzungskonfiguration

Zu verwendende API-Aufrufe:

1. **`list`** - Ruft vorhandene Konfigurationen ab.
1. **`create`** - Erstellt eine neue Konfiguration.
1. **`candeploy`** - Prüft, ob die Konfiguration bereitgestellt werden kann.
1. **`deploy`** : Stellt die Konfiguration bereit.

+++

+++Aktualisieren und Bereitstellen einer Begrenzungskonfiguration (noch nicht bereitgestellt)

Zu verwendende API-Aufrufe:

1. **`list`** - Ruft vorhandene Konfigurationen ab.
1. **`get`** : Ruft Details zu einer bestimmten Konfiguration ab.
1. **`update`** - Ändert die Konfiguration.
1. **`candeploy`** - Überprüft die Bereitstellungseignung.
1. **`deploy`** : Stellt die Konfiguration bereit.

+++

+++Aufheben der Bereitstellung und Löschen einer bereitgestellten Begrenzungskonfiguration

Zu verwendende API-Aufrufe:

1. **`list`** - Ruft vorhandene Konfigurationen ab.
1. **`undeploy`** - Hebt die Bereitstellung der Konfiguration auf.
1. **`delete`** - Entfernt die Konfiguration.

+++

+++Löschen einer bereitgestellten Begrenzungskonfiguration in einem Schritt

In nur einem API-Aufruf können Sie die Bereitstellung aufheben und die Konfiguration mithilfe des `forceDelete` löschen.

Zu verwendende API-Aufrufe:

1. **`list`** - Ruft vorhandene Konfigurationen ab.
1. **`delete`(mit `forceDelete` Parameter)** Erzwingt das Löschen einer bereitgestellten Konfiguration in einem einzigen Schritt.

+++

+++Aktualisieren einer bereits bereitgestellten Begrenzungskonfiguration

>[!NOTE]
>
>Nach dem Aktualisieren einer bereits bereitgestellten Konfiguration ist eine erneute Bereitstellung erforderlich.

Zu verwendende API-Aufrufe:

1. **`list`** - Ruft vorhandene Konfigurationen ab.
1. **`get`** : Ruft Details zu einer bestimmten Konfiguration ab.
1. **`update`** - Ändert die Konfiguration.
1. **`undeploy`** - Hebt die Bereitstellung der Konfiguration auf, bevor Änderungen angewendet werden.
1. **`candeploy`** - Überprüft die Bereitstellungseignung.
1. **`deploy`** - Stellt die aktualisierte Konfiguration bereit.

+++
