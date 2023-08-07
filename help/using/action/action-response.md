---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren einer benutzerdefinierten Aktion
description: Erfahren Sie, wie Sie eine benutzerdefinierte Aktion konfigurieren können
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: Aktion, Drittanbieter, benutzerdefiniert, Journeys, API
hide: true
hidefromtoc: true
source-git-commit: a3c95497fb7304ddd0aa26435f5d0279ff8fdb0f
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 7%

---

# Verbesserungen bei benutzerdefinierten Aktionen

Sie können jetzt API-Aufrufantworten in benutzerdefinierten Aktionen nutzen und Ihre Journey basierend auf diesen Antworten orchestrieren.

Diese Funktion war nur bei Verwendung von Datenquellen verfügbar. Sie können sie jetzt mit benutzerdefinierten Aktionen verwenden.

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit als private Beta-Version verfügbar.

>[!WARNING]
>
>Benutzerdefinierte Aktionen sollten nur mit privaten oder internen Endpunkten verwendet und mit einer entsprechenden Begrenzung oder Einschränkung verwendet werden. Weitere Informationen finden Sie auf [dieser Seite](../configuration/external-systems.md).

## Definieren der benutzerdefinierten Aktion

Bei der Definition der benutzerdefinierten Aktion wurden zwei Verbesserungen vorgenommen: das Hinzufügen der GET-Methode und das neue Payload-Antwortfeld. Die anderen Optionen und Parameter bleiben unverändert. Weitere Informationen finden Sie auf [dieser Seite](../action/about-custom-action-configuration.md).

### Endpunktkonfiguration

Die **URL-Konfiguration** wurde umbenannt. **Endpunktkonfiguration**.

Im **Methode** in der Dropdown-Liste können Sie jetzt **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### Payloads

Die **Aktionsparameter** wurde umbenannt. **Payloads**. Es stehen zwei Felder zur Verfügung:

* Die **Anfrage** -Feld: Dieses Feld ist nur für POST- und PUT-Aufrufmethoden verfügbar.
* Die **Reaktion** -Feld: Dies ist die neue Funktion. Dieses Feld ist für alle Aufrufmethoden verfügbar.

>[!NOTE]
> 
>Beide Felder sind optional.

![](assets/action-response2.png){width="70%" align="left"}

1. Klicken Sie in die **Reaktion** -Feld.

   ![](assets/action-response3.png){width="80%" align="left"}

1. Fügen Sie ein Beispiel der vom Aufruf zurückgegebenen Payload ein. Überprüfen Sie, ob die Feldtypen korrekt sind (Zeichenfolge, Ganzzahl usw.). Hier ist ein Beispiel für die Antwort-Payload, die während des -Aufrufs erfasst wird. Unser lokaler Endpunkt sendet die Anzahl der Treuepunkte und den Status eines Profils.

   ```
   {
   "customerID" : "xY12hye",    
   "status":"gold",
   "points": 1290 }
   ```

   ![](assets/action-response4.png){width="80%" align="left"}

   Jedes Mal, wenn die API aufgerufen wird, ruft das System alle im Payload-Beispiel enthaltenen Felder ab.

1. Fügen wir auch die customerID als Abfrageparameter hinzu.

   ![](assets/action-response9.png){width="80%" align="left"}

1. Klicken Sie auf **Speichern**.

## Verwenden der Antwort in einer Journey

Fügen Sie die benutzerdefinierte Aktion einfach einer Journey hinzu. Anschließend können Sie die Antwort-Payload-Felder in Bedingungen, anderen Aktionen und der Nachrichtenpersonalisierung nutzen.

Sie können beispielsweise eine Bedingung hinzufügen, um die Anzahl der Treuepunkte zu überprüfen. Wenn die Person das Restaurant betritt, sendet Ihr lokaler Endpunkt einen Aufruf mit den Treueinformationen des Profils. Sie können eine Push-Benachrichtigung versenden, wenn das Profil ein Goldkunde ist. Wenn beim Aufruf ein Fehler erkannt wird, senden Sie eine benutzerdefinierte Aktion, um den Systemadministrator zu benachrichtigen.

![](assets/action-response5.png)

1. Fügen Sie Ihr Ereignis und die zuvor erstellte benutzerdefinierte Aktion &quot;Treueprogramm&quot;hinzu.

1. Ordnen Sie in der benutzerdefinierten Aktion &quot;Loyalität&quot;den Abfrageparameter der Kunden-ID der Profil-ID zu. Aktivieren Sie die Option **Hinzufügen eines alternativen Pfads im Fall eines Timeouts oder Fehlers**.

   ![](assets/action-response10.png)

1. Fügen Sie im ersten Zweig eine Bedingung hinzu und verwenden Sie den erweiterten Editor, um die Aktionsreaktionsfelder unter dem **Kontext** Knoten.

   ![](assets/action-response6.png)

1. Fügen Sie dann Ihre Push-Benachrichtigung hinzu und personalisieren Sie Ihre Nachricht mithilfe der Antwortfelder. In unserem Beispiel personalisieren wir den Inhalt anhand der Anzahl der Treuepunkte und des Kundenstatus. Die Aktionsreaktionsfelder sind unter verfügbar. **Kontextattribute** > **Journey Orchestration** > **Aktionen**.

   ![](assets/action-response8.png)

   >[!NOTE]
   >
   >Jedes Profil, das die benutzerdefinierte Aktion aufruft, Trigger einen -Aufruf. Auch wenn die Antwort immer gleich ist, führt Journey immer noch einen Aufruf pro Profil durch.

1. Fügen Sie in der Verzweigung Timeout und Fehler eine Bedingung hinzu und nutzen Sie die integrierte **jo_status_code** -Feld. In unserem Beispiel verwenden wir die
   **http_400** Fehlertyp. Weitere Informationen finden Sie in [diesem Abschnitt](#error-status).

   ```
   @action{ActionLoyalty.jo_status_code} == "http_400"
   ```

   ![](assets/action-response7.png)

1. Fügen Sie eine benutzerdefinierte Aktion hinzu, die an Ihre Organisation gesendet wird.

   ![](assets/action-response11.png)

## Fehlerstatus{#error-status}

Die **jo_status_code** -Feld ist immer verfügbar, auch wenn keine Antwort-Payload definiert ist.

Hier finden Sie die möglichen Werte für dieses Feld:

* http status code: http_`<HTTP API call returned code>`, zum Beispiel http_200 oder http_400
* Zeitüberschreitungsfehler: **timedout**
* Begrenzungsfehler: **capped**
* interner Fehler: **internalError**

Ein Aktionsaufruf wird als fehlerhaft betrachtet, wenn der zurückgegebene HTTP-Code größer als 2xx ist oder wenn ein Fehler auftritt. In solchen Fällen wird die Journey an die dedizierte Zeitüberschreitung oder Fehlerverzweigung geleitet.

>[!WARNING]
>
>Nur neu erstellte benutzerdefinierte Aktionen enthalten **jo_status_code** vordefinierten Feld. Wenn Sie sie mit einer vorhandenen benutzerdefinierten Aktion verwenden möchten, müssen Sie die Aktion aktualisieren. Beispielsweise können Sie die Beschreibung aktualisieren und speichern.

## Syntax von Ausdrücken

Die Syntax lautet:

```json
#@action{myAction.myField} 
```

Im Folgenden finden Sie einige Beispiele:

```json
 // action response field
 @action{<action name>.<path to the field>}
 @action{ActionLoyalty.status}
```

```json
 // action response field
 @action{<action name>.<path to the field>, defaultValue: <default value expression>}
 @action{ActionLoyalty.points, defaultValue: 0}
 @action{ActionLoyalty.points, defaultValue: @{myEvent.newPoints}}
```

Weitere Informationen zu Feldverweisen finden Sie unter [diesem Abschnitt](../building-journeys/expression/field-references.md).
