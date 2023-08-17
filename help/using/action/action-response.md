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
ht-degree: 100%

---

# Verbesserungen bei benutzerdefinierten Aktionen

Sie können jetzt API-Aufrufantworten in benutzerdefinierten Aktionen nutzen und Ihre Journeys basierend auf diesen Antworten orchestrieren.

Diese Funktion war nur bei Verwendung von Datenquellen verfügbar. Sie können sie jetzt mit benutzerdefinierten Aktionen verwenden.

>[!AVAILABILITY]
>
>Diese Funktion ist als private Betaversion verfügbar.

>[!WARNING]
>
>Benutzerdefinierte Aktionen sollten nur mit privaten oder internen Endpunkten und mit einer entsprechenden Begrenzung oder Drosselung verwendet werden. Weitere Informationen finden Sie auf [dieser Seite](../configuration/external-systems.md).

## Definieren der benutzerdefinierten Aktion

Bei der Definition der benutzerdefinierten Aktion wurden zwei Verbesserungen vorgenommen: die GET-Methode und das neue Payload-Antwortfeld wurden hinzugefügt. Die anderen Optionen und Parameter bleiben unverändert. Weitere Informationen finden Sie auf [dieser Seite](../action/about-custom-action-configuration.md).

### Endpunktkonfiguration

Der Abschnitt **URL-Konfiguration** wurde in **Endpunktkonfiguration** umbenannt.

Im Dropdown-Menü **Methode** können Sie jetzt **GET** auswählen.

![](assets/action-response1.png){width="70%" align="left"}

### Payloads

Der Abschnitt **Aktionsparameter** wurde in **Payloads** umbenannt. Es sind zwei Felder verfügbar:

* Das Feld **Anfrage**: Dieses Feld ist nur für die Aufrufmethoden POST und PUT verfügbar.
* Das Feld **Antwort**: Dies ist die neue Funktion. Dieses Feld ist für alle Aufrufmethoden verfügbar.

>[!NOTE]
> 
>Beide Felder sind optional.

![](assets/action-response2.png){width="70%" align="left"}

1. Klicken Sie in das Feld **Antwort**.

   ![](assets/action-response3.png){width="80%" align="left"}

1. Fügen Sie ein Beispiel der vom Aufruf zurückgegebenen Payload ein. Überprüfen Sie, ob die Feldtypen korrekt sind (Zeichenfolge, Ganzzahl usw.). Hier ist ein Beispiel für die Antwort-Payload, die während des Aufrufs erfasst wird. Unser lokaler Endpunkt sendet die Anzahl der Treuepunkte und den Status eines Profils.

   ```
   {
   "customerID" : "xY12hye",    
   "status":"gold",
   "points": 1290 }
   ```

   ![](assets/action-response4.png){width="80%" align="left"}

   Jedes Mal, wenn die API aufgerufen wird, ruft das System alle im Payload-Beispiel enthaltenen Felder ab.

1. Fügen Sie außerdem die customerID als Abfrageparameter hinzu.

   ![](assets/action-response9.png){width="80%" align="left"}

1. Klicken Sie auf **Speichern**.

## Nutzen der Antwort in einer Journey

Fügen Sie die benutzerdefinierte Aktion einfach einer Journey hinzu. Anschließend können Sie die Felder der Antwort-Payload in Bedingungen, anderen Aktionen und der Nachrichtenpersonalisierung nutzen.

Sie können beispielsweise eine Bedingung hinzufügen, um die Anzahl der Treuepunkte zu überprüfen. Wenn die Person das Restaurant betritt, sendet Ihr lokaler Endpunkt einen Aufruf mit den Treueinformationen des Profils. Sie können eine Push-Benachrichtigung versenden, wenn das Profil zu den Goldkundinnen und -kunden gehört. Wenn beim Aufruf ein Fehler erkannt wird, senden Sie eine benutzerdefinierte Aktion, um die Systemadmins zu benachrichtigen.

![](assets/action-response5.png)

1. Fügen Sie Ihr Ereignis und die zuvor erstellte benutzerdefinierte Treue-Aktion hinzu.

1. Ordnen Sie in der benutzerdefinierten Treue-Aktion den Abfrageparameter der Kunden-ID der Profil-ID zu. Aktivieren Sie die Option **Alternativen Pfad im Fall eines Timeouts oder Fehlers hinzufügen**.

   ![](assets/action-response10.png)

1. Fügen Sie im ersten Zweig eine Bedingung hinzu und verwenden Sie den erweiterten Editor, um die Aktionsreaktionsfelder unter dem **Kontext**-Knoten zu nutzen.

   ![](assets/action-response6.png)

1. Fügen Sie dann Ihre Push-Benachrichtigung hinzu und personalisieren Sie Ihre Nachricht mithilfe der Antwortfelder. In unserem Beispiel personalisieren wir den Inhalt anhand der Anzahl der Treuepunkte und des Kundenstatus. Die Aktionsreaktionsfelder sind verfügbar unter **Kontextattribute** > **Journey Orchestration** > **Aktionen**.

   ![](assets/action-response8.png)

   >[!NOTE]
   >
   >Jedes Profil, das die benutzerdefinierte Aktion durchführt, löst einen Aufruf aus. Auch wenn die Antwort immer gleich ist, führt die Journey immer noch einen Aufruf pro Profil durch.

1. Fügen Sie in den Verzweigungen „Timeout“ und „Fehler“ eine Bedingung hinzu und nutzen Sie das integrierte Feld **jo_status_code**. In unserem Beispiel verwenden wir den Fehlertyp
   **http_400**. Weitere Informationen finden Sie in [diesem Abschnitt](#error-status).

   ```
   @action{ActionLoyalty.jo_status_code} == "http_400"
   ```

   ![](assets/action-response7.png)

1. Fügen Sie eine benutzerdefinierte Aktion hinzu, die an Ihre Organisation gesendet wird.

   ![](assets/action-response11.png)

## Fehlerstatus{#error-status}

Das Feld **jo_status_code** ist immer verfügbar, auch wenn keine Antwort-Payload definiert ist.

Hier finden Sie die möglichen Werte für dieses Feld:

* HTTP-Status-Code: http_`<HTTP API call returned code>`, zum Beispiel http_200 oder http_400
* Zeitüberschreitungsfehler: **timedout**
* Begrenzungsfehler: **capped**
* Interner Fehler: **internalError**

Ein Aktionsaufruf wird als fehlerhaft betrachtet, wenn der zurückgegebene HTTP-Code größer als 2xx ist oder wenn ein Fehler auftritt. In solchen Fällen wird die Journey an die dedizierte Verzweigung „Timeout“ oder „Fehler“ geleitet.

>[!WARNING]
>
>Nur neu erstellte benutzerdefinierte Aktionen enthalten das vordefinierte Feld **jo_status_code**. Wenn Sie sie mit einer vorhandenen benutzerdefinierten Aktion verwenden möchten, müssen Sie die Aktion aktualisieren. Beispielsweise können Sie die Beschreibung aktualisieren und speichern.

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

Weitere Informationen zu den Feldverweisen finden Sie in [diesem Abschnitt](../building-journeys/expression/field-references.md).
