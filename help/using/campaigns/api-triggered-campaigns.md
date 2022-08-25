---
title: Auslösen von Kampagnen mit APIs
description: Erfahren Sie, wie Sie mit einer  [!DNL Journey Optimizer] API Kampagnen auslösen können.
hide: true
hidefromtoc: true
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 96%

---

# Auslösen von Kampagnen mit APIs {#trigger-campaigns}

## Über von einer API ausgelöste Kampagnen {#about}

>[!NOTE]
>
>Die Interactive Message Execution API befindet sich derzeit in der Betaphase und kann ohne vorherige Ankündigung häufig aktualisiert werden.

Mit [!DNL Journey Optimizer] können Sie Kampagnen erstellen und diese dann in einem externen System über eine [Interactive Message Execution REST-API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) auslösen. Auf diese Weise können Sie Nutzungsszenarien mit verschiedenen operativen und Transaktionsnachrichten abdecken, wie z. B. das Zurücksetzen von Kennwörtern, OTP-Token usw.

Dazu müssen Sie zunächst in Journey Optimizer eine von einer API ausgelöste Kampagne erstellen und deren Ausführung dann über einen API-Aufruf starten.

Für von einer API ausgelöste Kampagnen stehen die Kanäle E-Mail, SMS und Push-Benachrichtigungen zur Verfügung.

## Erstellen einer von einer API ausgelösten Kampagne {#create}

Der Prozess zum Erstellen API-gesteuerter Kampagnen bleibt identisch mit geplanten Kampagnen, mit Ausnahme der Zielgruppenauswahl, die in der API-Payload durchgeführt wird. Detaillierte Informationen zum Erstellen einer Kampagne finden Sie in [diesem Abschnitt](create-campaign.md).

Gehen Sie wie folgt vor, um eine von einer API ausgelöste Kampagne zu erstellen:

1. Erstellen Sie eine neue Kampagne vom Typ **[!UICONTROL API-ausgelöst]**.

1. Wählen Sie den Kanal und die Kanaloberfläche für den Nachrichtenversand aus und klicken Sie auf **[!UICONTROL Erstellen]**.

   ![](assets/api-triggered-type.png)

1. Geben Sie für die Kampagne einen Titel und eine Beschreibung an und konfigurieren Sie dann die zu sendende Nachricht.

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >Sie können an die API-Payload zusätzliche Daten zur Nachrichtenpersonalisierung übergeben. [Weitere Informationen](#contextual)

1. Geben Sie den Namespace an, anhand dessen Personen aus dem Segment identifiziert werden sollen.

1. Konfigurieren Sie das Start- und Enddatum der Kampagne.

   Wenn Sie ein bestimmtes Start- und/oder Enddatum für eine Kampagne konfigurieren, wird diese nicht außerhalb dieses Zeitraums ausgeführt und API-Aufrufe schlagen fehl, wenn eine Kampagne durch APIs ausgelöst wird.

1. Rufen Sie im Bereich **[!UICONTROL cURL-Anfrage]** die **[!UICONTROL Kampagnen-ID]** auf, um sie in der API-Payload zu verwenden.

   ![](assets/api-triggered-curl.png)

1. Klicken Sie auf **[!UICONTROL Zum Aktivieren überprüfen]**, um sicherzustellen, dass Ihre Kampagne korrekt konfiguriert ist, und aktivieren Sie sie.

## Verwenden von kontextbezogenen Attributen in von einer API ausgelösten Kampagnen {#contextual}

Bei von einer API ausgelösten Kampagnen können Sie zusätzliche Daten in die API-Payload übertragen und innerhalb der Kampagne nutzen, um Ihre Nachricht zu personalisieren.

In diesem Beispiel möchten Kunden ihr Kennwort zurücksetzen. Sie senden ihnen deshalb zum Zurücksetzen des Kennworts eine URL, die in einem Drittanbieter-Tool generiert wird. Bei von einer API ausgelösten Kampagnen können Sie diese generierte URL in die API-Payload übergeben und in der Kampagne in die Nachricht einfügen.

>[!NOTE]
>
>Im Gegensatz zu profilaktivierten Ereignissen werden die in der REST-API übergebenen Kontextdaten für die einmalige Kommunikation verwendet und nicht im Profil gespeichert. Das Profil wird nur mit den Namespace-Details erstellt, falls es nicht vorhanden ist.

Um diese Daten in Ihren Kampagnen verwenden zu können, müssen Sie sie an die API-Payload übergeben und mithilfe des Ausdruckseditors zu Ihrer Nachricht hinzufügen. Verwenden Sie dazu die Syntax `{{context.<contextualAttribute>}}`, wobei `<contextualAttribute>` mit dem Namen der Variablen in Ihrer API-Payload, die die zu übergebenden Daten enthält, übereinstimmen muss.

Die Syntax `{{context.<contextualAttribute>}}` ist nur einem Zeichenfolgen-Datentyp zugeordnet.

![](assets/api-triggered-context.png)

>[!IMPORTANT]
>
>Die Syntax `context.system` ist auf die interne Nutzung bei Adobe beschränkt und sollte nicht zur Weitergabe von kontextbezogenen Attributen verwendet werden.
Beachten Sie, dass im Menü in der linken Leiste derzeit kein kontextbezogenes Attribut verfügbar ist. Attribute müssen direkt in Ihren Personalisierungsausdruck eingegeben werden, ohne dass eine Überprüfung durch [!DNL Journey Optimizer] durchgeführt wird.

## Ausführen der Kampagne {#execute}

Um eine von APIs ausgelöste Kampagne auszuführen, müssen Sie zunächst deren ID abrufen und an die API-Payload übergeben. Öffnen Sie dazu die Kampagne und kopieren Sie die ID aus dem Bereich **[!UICONTROL cURL-Anfrage]**.

![](assets/api-triggered-id.png)

Anschließend können Sie diese ID in Ihrer API-Payload verwenden, um die Kampagne auszulösen. Weitere Informationen finden Sie in der [Dokumentation zur Interactive Message Execution API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

Beachten Sie, dass, wenn Sie bei der Erstellung der Kampagne ein bestimmtes Start- und/oder Enddatum konfiguriert haben, die Kampagne außerhalb dieses Zeitraums nicht ausgeführt wird und API-Aufrufe fehlschlagen.

>[!NOTE]
>
>In einigen Fällen müssen Sie möglicherweise Transaktionsnachrichten an Profile senden, die nicht im System sind. Beispiel: Ein unbekannter Benutzer versucht, sich bei Ihrer Website anzumelden. In diesem Fall wird das entsprechende Profil automatisch in Adobe Experience Platform im Datensatz **AJO Interactive Messaging Profile Dataset** erstellt.
