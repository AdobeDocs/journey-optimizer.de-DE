---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei der Live-Journey-Ausführung
description: Informationen zum Beheben von Fehlern bei der Live-Journey-Ausführung
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Problembehebung, Fehlerbehebung, Journey, Überprüfen, Fehler
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: acf73fbce4a8ebfc6f228c92480a5e597e0bfe53
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 53%

---

# Fehlerbehebung bei der Live-Journey-Ausführung {#troubleshooting-execution}

In diesem Abschnitt erfahren Sie, wie Sie Probleme beim Journey von Ereignissen beheben, prüfen, ob Profile auf Ihre Journey gelangt sind, wie sie darin navigieren und ob Nachrichten gesendet werden.

Sie können auch Fehler beheben, bevor Sie eine Journey testen oder veröffentlichen. [Auf dieser Seite](troubleshooting.md) erfahren Sie mehr dazu.

[Auf dieser Seite](troubleshooting-inbound.md) erfahren Sie, wie Sie Fehler bei eingehenden Aktionen beheben.

## Überprüfen, ob Ereignisse ordnungsgemäß gesendet werden {#checking-that-events-are-properly-sent}

Der Ausgangspunkt einer Journey ist stets ein Ereignis. Sie können mithilfe von Tools wie Postman Tests durchführen.

Sie können prüfen, ob der API-Aufruf, den Sie über diese Tools versenden, richtig gesendet wurde oder nicht. Wenn Sie einen Fehler erhalten, bedeutet das, dass es bei Ihrem Aufruf zu einem Fehler kommt. Überprüfen Sie erneut die Payload, die Kopfzeile (insbesondere die Organisations-ID) sowie die Ziel-URL. Sie können Ihren Administrator nach der richtigen URL fragen.

Ereignisse werden von der Quelle nicht direkt an Journeys weitergeleitet. Journeys benötigen dazu stattdessen die Streaming-Aufnahme-APIs von Adobe Experience Platform. Darum können Sie bei Problemen mit Ereignissen die Fehlerbehebung für Streaming-Aufnahme-APIs in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de){target="_blank"} nutzen.

Wenn Ihre Journey den Testmodus nicht aktivieren kann und dabei der Fehler `ERR_MODEL_RULES_16` ausgegeben wird, stellen Sie im Falle von Kanalaktionen sicher, dass das verwendete Ereignis einen [Identity-Namespace](../audience/get-started-identity.md) enthält.

Der Identity-Namespace dient dazu, die Testprofile eindeutig zu identifizieren. Wenn beispielsweise die E-Mail-Adresse zur Identifizierung der Testprofile verwendet wird, sollte der Identity-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identity-Namespace **Telefon** ausgewählt werden.

## Überprüfen, ob Personen in die Journey eintreten {#checking-if-people-enter-the-journey}

Berichte zu Journey messen den Eintritt von Personen in eine Journey auf Echtzeitbasis.

Wenn Sie das Ereignis erfolgreich versenden, aber keinen Eintritt in die Journey sehen können, bedeutet das, dass es zwischen dem Senden und Empfangen des Ereignisses in der Journey zu Problemen kommt.

Sie können die Fehlerbehebung mit den folgenden Fragen beginnen:

* Sind Sie sicher, dass sich die Journey, bei der Sie das eingehende Ereignis erwarten, im Testmodus befindet oder live ist?
* Haben Sie das Ereignis gespeichert, bevor Sie die Payload aus der Payload-Vorschau kopiert haben?
* Enthält die Payload des Ereignisses eine Ereignis-ID?
* Haben Sie die richtige URL aufgerufen?
* Haben Sie die Payload-Struktur der Streaming-Aufnahme-APIs mithilfe der Payload-Strukturvorschau im Ereigniskonfigurationsbereich beachtet? Weitere Informationen finden Sie auf [dieser Seite](../event/about-creating.md#preview-the-payload).
* Haben Sie im Header Ihres Ereignisses die richtigen Schlüssel-Wert-Paare verwendet?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

>[!NOTE]
>
>**Für Journey zur Zielgruppenqualifizierung mit Streaming-Zielgruppen**: Wenn Sie eine Aktivität zur Zielgruppenqualifizierung als Einstiegspunkt für das Journey verwenden, beachten Sie, dass nicht alle Profile, die sich für die Zielgruppe qualifizieren, aufgrund von Zeitfaktoren, Schnellabbrüchen aus der Zielgruppe oder wenn sich Profile bereits vor der Veröffentlichung in der Zielgruppe befanden, notwendigerweise auf die Journey zugreifen. Weitere Informationen zu [Überlegungen zur Qualifizierung von Streaming-Zielgruppen](audience-qualification-events.md#streaming-entry-caveats).

## Überprüfen, wie Personen durch die Journey navigieren {#checking-how-people-navigate-through-the-journey}

Berichte zu Journey messen den Fortschritt von Kontakten innerhalb einer Journey. So können Sie leicht ermitteln, wo und warum eine Person gestoppt wurde.

Prüfen Sie folgende Punkte:

* Ist das Problem auf eine Bedingung zurückzuführen, mit der die Person ausgeschlossen wird? Beispiel: Die Bedingung lautet „Geschlecht = männlich“, während die Person eine Frau ist. Die Prüfung kann von einem Business-Anwender vorgenommen werden, solange die Bedingung nicht zu komplex ist.
* Ist das Problem auf einen Aufruf einer Datenquelle zurückzuführen, die nicht reagiert? Wenn sich die Journey im Test befindet, können diese Informationen in Testmodusprotokollen angezeigt werden. Wenn die Journey live ist, kann ein Administrator direkte Aufrufe an die Datenquelle testen und die erhaltene Antwort überprüfen. Alternativ kann ein Administrator die Journey duplizieren und dann testen.

## Überprüfen, ob Nachrichten erfolgreich gesendet werden {#checking-that-messages-are-sent-successfully}

Wenn Personen die Journey zwar richtig durchlaufen, aber nicht die vorgesehenen Nachrichten erhalten, können Sie Folgendes prüfen:

* [!DNL Journey Optimizer] hat die Anfrage zum Senden der Nachricht korrekt berücksichtigt. Ein Business-Anwender kann auf die zu sendende Nachricht zugreifen und prüfen, ob der Zeitpunkt der letzten Ausführung mit der Ausführungszeit Ihrer Journey übereinstimmt. Außerdem kann er die neuesten eingegangenen API-Aufrufe/-Ereignisse prüfen.
* [!DNL Journey Optimizer] hat die Nachricht erfolgreich gesendet. Überprüfen Sie die Journey-Berichte, um sicherzustellen, dass keine Fehler aufgetreten sind.

Bei einer Nachricht, die über eine benutzerdefinierte Aktion gesendet wird, kann während des Journey-Tests nur geprüft werden, ob der Systemaufruf der benutzerdefinierten Aktion zu einem Fehler führt oder nicht.  Wenn der Aufruf an das externe System, das mit der benutzerdefinierten Aktion verknüpft ist, nicht zu einem Fehler führt, aber auch nicht zum Senden der Nachricht, sollten Sie das externe System überprüfen.

## Doppelte Einträge in Journey-Schrittereignissen {#duplicate-step-events}

### Warum sehe ich mehrere Einträge mit derselben Journey-Instanz, demselben Profil, demselben Knoten und derselben Anfrage-IDs?

Bei der Abfrage von Journey-Schritt-Ereignisdaten können Sie gelegentlich feststellen, was doppelte Protokolleinträge für dieselbe Journey-Ausführung zu sein scheinen. Diese Einträge haben identische Werte für:

* `profileID` - Die Profilidentität
* `instanceID` - Die Journey-Instanzkennung
* `nodeID` - Der spezifische Journey-Knoten
* `requestID` - Die Anforderungskennung

Diese Einträge haben jedoch **unterschiedliche `_id`-Werte** was der Schlüsselindikator ist, der dieses Szenario von der tatsächlichen Datenduplizierung unterscheidet.

### Was verursacht dieses Verhalten?

Dies geschieht aufgrund von Backend-Skalierungsvorgängen (auch als „Rebalancing“ bezeichnet) in der Microservices-Architektur von Adobe Journey Optimizer. In Zeiten hoher Auslastung oder Systemoptimierung:

1. Ein Journey-Schrittereignis beginnt mit der Verarbeitung und wird im Journey-Schritt-Ereignisdatensatz protokolliert.
2. Durch einen Vorgang mit automatischer Skalierung wird die Arbeitslast auf die Dienstinstanzen verteilt
3. Dasselbe Ereignis kann von einer anderen Service-Instanz erneut verarbeitet werden, wodurch ein zweiter Protokolleintrag mit einem anderen `_id` erstellt wird

Dies ist ein erwartetes Systemverhalten und funktioniert **wie vorgesehen**.

### Hat dies Auswirkungen auf die Ausführung von Journey oder den Nachrichtenversand?

**Nein.** Die Auswirkungen sind auf die Protokollierung beschränkt. Adobe Journey Optimizer verfügt über integrierte Deduplizierungsmechanismen auf der Nachrichtenausführungsebene, die Folgendes sicherstellen:

* An jedes Profil wird nur eine Nachricht (E-Mail, SMS, Push-Benachrichtigung usw.) gesendet
* Aktionen werden nur einmal ausgeführt
* Journey-Ausführung läuft korrekt ab

Sie können dies überprüfen, indem Sie die `ajo_message_feedback_event_dataset` abfragen oder die Ausführungsprotokolle der Aktion überprüfen. Sie sehen, dass trotz der doppelten Journey-Schritt-Ereigniseinträge nur eine Nachricht tatsächlich gesendet wurde.

### Wie kann ich diese Fälle in meinen Abfragen identifizieren?

Beim Analysieren von Journey-Schritt-Ereignisdaten:

1. **Überprüfen Sie das Feld `_id`**: True-Duplikate auf Systemebene hätten denselben `_id`. Unterschiedliche `_id` weisen auf separate Protokolleinträge aus dem oben beschriebenen Neuausrichtungsszenario hin.

2. **Nachrichtenversand überprüfen**: Querverweis mit den Feedback-Daten der Nachricht, um zu bestätigen, dass nur eine Nachricht gesendet wurde:

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **Nach eindeutigen Kennungen gruppieren**: Beim Zählen von Ausführungen `_id` verwenden, um genaue Zählungen zu erhalten:

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### Was sollte ich tun, wenn ich dies feststelle?

Dies ist ein normales Systemverhalten und **keine Aktion erforderlich**. Die Duplikatprotokollierung weist nicht auf ein Problem mit Ihrer Journey-Konfiguration oder dem Nachrichtenversand hin.

Wenn Sie Berichte oder Analysen auf der Grundlage von Journey-Schrittereignissen erstellen:

* `_id` als Primärschlüssel für die Zählung eindeutiger Ereignisse verwenden
* Querverweis mit Nachrichten-Feedback-Datensätzen bei der Analyse des Nachrichtenversands
* Beachten Sie, dass die Zeitanalyse Einträge innerhalb weniger Sekunden gruppiert anzeigen kann

Weitere Informationen zum Abfragen von Journey-Schrittereignissen finden Sie unter [Beispiele für Abfragen](../reports/query-examples.md).

## Fehlerbehebung bei Diskrepanzen bei Dashboard-Metriken {#dashboard-metrics}

Wenn die im Dashboard **Übersicht** angezeigten Metriken nicht mit der tatsächlichen Anzahl der Journey auf der Registerkarte **Durchsuchen** übereinstimmen, überprüfen Sie Folgendes:

* Stellen Sie sicher, dass die betreffenden Journey in den letzten 24 Stunden Traffic hatten, da Journey ohne aktuelle Aktivität aus dem Dashboard ausgeschlossen werden.
* Vergewissern Sie sich, dass Sie über die entsprechenden Zugriffsberechtigungen verfügen, um alle Journey in Ihrem Unternehmen anzuzeigen.
* Warten Sie bis zu 30 Minuten, bis die Metriken aktualisiert sind, nachdem Sie Änderungen an Ihren Journey vorgenommen haben.

Wenn Diskrepanzen bestehen bleiben, wenden Sie sich zur Untersuchung an den Adobe-Support und zeigen Sie Screenshots der Registerkarten Übersicht und Durchsuchen an.
