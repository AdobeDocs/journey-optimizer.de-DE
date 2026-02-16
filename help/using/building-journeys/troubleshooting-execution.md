---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei der Live-Journey-Ausführung
description: Informationen zum Beheben von Fehlern bei der Live-Journey-Ausführung
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: Problembehebung, Fehlerbehebung, Journey, Überprüfen, Fehler
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: bae446ea38a0cb97487201f7dcf4df751578ad0a
workflow-type: tm+mt
source-wordcount: '1938'
ht-degree: 77%

---

# Fehlerbehebung bei der Live-Journey-Ausführung {#troubleshooting-execution}

In diesem Abschnitt erfahren Sie, wie Sie Fehler bei Journey-Ereignissen beheben und wie Sie prüfen, ob Profile in Ihre Journey eingetreten sind, wie sie diese durchlaufen und ob Nachrichten gesendet werden.

Sie können auch Fehler beheben, bevor Sie eine Journey testen oder veröffentlichen. [Auf dieser Seite](troubleshooting.md) erfahren Sie mehr dazu.

[Auf dieser Seite](troubleshooting-inbound.md) erfahren Sie, wie Sie Fehler bei eingehenden Aktionen beheben.

## Überprüfen, ob Ereignisse ordnungsgemäß gesendet werden {#checking-that-events-are-properly-sent}

Der Ausgangspunkt einer Journey ist stets ein Ereignis. Sie können mithilfe von Tools wie Postman Tests durchführen.

Sie können prüfen, ob der API-Aufruf, den Sie über diese Tools versenden, richtig gesendet wurde oder nicht. Wenn Sie einen Fehler erhalten, bedeutet das, dass es bei Ihrem Aufruf zu einem Fehler kommt. Überprüfen Sie erneut die Payload, die Kopfzeile (insbesondere die Organisations-ID) sowie die Ziel-URL. Sie können Ihren Administrator nach der richtigen URL fragen.

Ereignisse werden von der Quelle nicht direkt an Journeys weitergeleitet. Tatsächlich verlassen sich Journey auf die Streaming-Aufnahme-APIs von [!DNL Adobe Experience Platform]. Darum können Sie bei Problemen mit Ereignissen die Fehlerbehebung für Streaming[[!DNL Adobe Experience Platform] Aufnahme-APIs in der &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de){target="_blank"}Dokumentation“ aufrufen.

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

* **Ereignisbedingung und Schemadatentypen** - Stellen Sie sicher, dass die in Ihrer Ereignisbedingung (Regel) verwendeten Datentypen mit dem Ereignisschema übereinstimmen. Nicht übereinstimmende Typen (z. B. Zeichenfolge vs. Ganzzahl) führen dazu, dass die Regelauswertung fehlschlägt und Ereignisse gelöscht werden. Siehe [Überprüfen der &#x200B;](#verify-event-identity-and-rule-data-types).

* **Ereignis verworfen - Qualifizierungsbedingung nicht erfüllt** - Bei regelbasierten Ereignissen wird das Ereignis **empfangen, aber verworfen** und das Journey wird nicht ausgelöst, wenn die `isNotEmpty`Qualifizierungsbedingung **von der Ereignis-Payload nicht erfüllt wird (z. B. wenn ein erforderliches Feld leer ist oder fehlt oder eine Bedingung wie &quot;** eines Felds fehlschlägt„). Protokolle und Splunk-Traces können zeigen, dass das Ereignis empfangen, aber verworfen wurde, weil es die Qualifizierungsbedingung nicht erfüllte, einschließlich Verwerfen-Codes wie `notSuitableInitialEvent`. Dies ist das erwartete Verhalten: Wenn die Qualifizierungsbedingung nicht erfüllt ist, wird das Ereignis verworfen und das Journey wird für dieses Profil nicht ausgelöst. Überprüfen Sie, ob die Ereignis-Payload die erwarteten Felder und Werte enthält und ob die Regel in der Ereigniskonfiguration mit den gesendeten Daten übereinstimmt. Wenn das Ereignis durch eine **benutzerdefinierte Aktion** einer anderen Journey ausgelöst wird, finden Sie weitere Informationen unter [Umgang mit Verwerfungsereignissen und Leerlauf-Timeouts](../action/troubleshoot-custom-action.md#handling-discard-events-and-idle-timeouts) in Fehlerbehebung bei benutzerdefinierten Aktionen.

&#x200B;>>
**Für Journeys zur Zielgruppenqualifizierung mit Streaming-Zielgruppen**: Wenn Sie eine Aktivität zur Zielgruppenqualifizierung als Eintrittspunkt für die Journey verwenden, beachten Sie, dass nicht unbedingt alle für die Zielgruppe qualifizierten Profile auch in die Journey eintreten. Dies kann an Zeitfaktoren oder kurzfristigen Ausstiegen aus der Zielgruppe liegen oder daran, dass sich Profile bereits vor der Veröffentlichung in der Zielgruppe befanden. Erfahren Sie mehr zu [Überlegungen zum Timing bei der Qualifizierung von Streaming-Zielgruppen](audience-qualification-events.md#streaming-entry-caveats).

### Überprüfen der Ereignisidentität {#verify-event-identity-and-rule-data-types}

Stellen Sie beim Konfigurieren einer ereignisbasierten Journey sicher, dass das Identitätsfeld der Payload mit dem [im Ereignis ausgewählten Namespace) &#x200B;](../event/about-creating.md#select-the-namespace). Wenn das Ereignis Felder zum Abgleichen von Profilen enthält, überprüfen Sie **ob** Groß-/Kleinschreibung) und **Datentyp** in der Ereignisbedingung genau mit den eingehenden Daten übereinstimmen. Wenn das Ereignisschema beispielsweise `roStatus` als Zeichenfolge definiert, muss die Journey-Regel sie auch als Zeichenfolge auswerten. Nicht übereinstimmende Datentypen (z. B. Zeichenfolge vs. Ganzzahl) führen dazu, dass die Regelauswertung fehlschlägt und gültige Ereignisse gelöscht werden. Wenn das Ereignis eine **Qualifizierungsbedingung“ aufweist** z. B. ein Feld darf nicht leer sein), werden Ereignisse, die diese Bedingung nicht erfüllen, **verworfen** und enthalten keinen Trigger zum Journey. In Protokollen können Verwerfungscodes wie `notSuitableInitialEvent` angezeigt werden.

Um Ihre Ereignisbedingung in [!DNL Journey Optimizer] zu überprüfen, verwenden Sie die Payload-Vorschau in der Ereigniskonfiguration und stellen Sie sicher, dass die Typen und Werte in der Regel mit der Payload-Struktur übereinstimmen. Erfahren Sie[&#x200B; wie Sie die Payload &#x200B;](../event/about-creating.md#preview-the-payload) und [regelbasierte Ereignisse konfigurieren](../event/about-creating.md).

## Fehlerbehebung bei Transitionen im Testmodus {#troubleshooting-test-transitions}

Wenn Testprofile im Testmodus in Ihrer Journey nicht vorankommen oder der visuelle Fluss keine grünen Pfeile anzeigt, die den Fortschritt durch die Schritte angeben, kann das Problem mit der Transitionsvalidierung zusammenhängen. Dieser Abschnitt enthält Anleitungen zur Diagnose und Behebung gängiger Testmodusprobleme.

### Testprofile schreiten nicht voran

Wenn Testprofile in die Journey eintreten, aber nicht über den ursprünglichen Schritt hinausgehen, überprüfen Sie Folgendes:

* **Journey-Startdatum** – Die häufigste Ursache ist, dass das Startdatum der Journey in der Zukunft liegt. Testprofile werden sofort verworfen, wenn die aktuelle Zeit außerhalb des konfigurierten Fensters [Start- und Enddatum/-zeit](journey-properties.md#dates) für die Journey liegt. Behebung:
   * Stellen Sie sicher, dass das Startdatum der Journey nicht in der Zukunft liegt
   * Stellen Sie sicher, dass die aktuelle Uhrzeit in das aktive Datumsfenster der Journey fällt
   * Aktualisieren Sie bei Bedarf die Journey-Eigenschaften, um das Startdatum anzupassen

* **Testprofilkonfiguration** - Vergewissern Sie sich, dass das Profil in [!DNL Adobe Experience Platform] korrekt als Testprofil gekennzeichnet ist. Weitere Informationen finden Sie unter [So erstellen Sie Testprofile](../audience/creating-test-profiles.md).

* **Identity-Namespace** – Stellen Sie sicher, dass der in der Ereigniskonfiguration verwendete Identity-Namespace mit dem Namespace Ihres Testprofils übereinstimmt.

### Null-Transitionsindikatoren

Bei der technischen Fehlerbehebung kann eine `isValidTransition`-Eigenschaft auftreten, die in den technischen Details der Journey auf null gesetzt ist. Diese Eigenschaft betrifft ausschließlich die Benutzeroberfläche und hat keine Auswirkungen auf die Backend-Verarbeitung oder die Journey-Leistung. Ein Nullwert kann jedoch auf Folgendes hinweisen:

* **Fehlerhafte Journey-Konfiguration** – Das Journey-Startdatum ist für die Zukunft festgelegt, sodass Testereignisse im Hintergrund verworfen werden
* **Beschädigte Transition** – In seltenen Fällen müssen Journey-Knoten möglicherweise erneut verbunden werden

Wenn dauerhafte Probleme mit der Transition auftreten:

1. Überprüfen Sie, ob das Startdatum der Journey aktuell ist
1. Deaktivieren und reaktivieren Sie den Testmodus
1. Wenn das Problem weiterhin besteht, duplizieren Sie die betroffenen Journey-Knoten und verbinden Sie sie erneut
1. Wenden Sie sich bei ungelösten Problemen mit Journey-Protokollen, den betroffenen Profil-IDs und Details zur Nulltransition an den Support

>[!NOTE]
>
>Beachten Sie, dass Ereignisse, die außerhalb des aktiven Datumsfensters der Journey gesendet werden, ohne Fehlermeldung im Hintergrund verworfen werden. Überprüfen Sie bei der Fehlerbehebung im Zusammenhang mit dem Fortschritt des Testprofils immer zuerst die Timing-Konfiguration Ihrer Journey.

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

## Informationen zu doppelten Einträgen in Journey-Schrittereignissen {#duplicate-step-events}

In diesem Abschnitt erfahren Sie, warum doppelte Zeilen beim Journey von Schrittereignissen angezeigt werden können.

### Warum sehe ich mehrere Einträge mit derselben Journey-Instanz, demselben Profil, demselben Knoten und denselben Anfrage-IDs?

Beim Abfragen von Daten zu Journey-Schrittereignissen werden Ihnen gelegentlich anscheinend doppelte Protokolleinträge für dieselbe Journey-Ausführung auffallen. Diese Einträge haben identische Werte bei:

* `profileID` – der Profilidentität
* `instanceID` – der Journey-Instanzkennung
* `nodeID` – dem spezifischen Journey-Knoten
* `requestID` – der Anfragekennung

Diese Einträge weisen jedoch **unterschiedliche `_id`-Werte** auf, was der Schlüsselindikator ist, der dieses Szenario von tatsächlicher Datenduplizierung unterscheidet.

### Was verursacht dieses Verhalten?

Dies geschieht aufgrund der automatischen Backend-Skalierung (auch als „Rebalancing“ bezeichnet) in der [!DNL Adobe Journey Optimizer]-Microservice-Architektur. In Zeiten von hoher Auslastung oder Systemoptimierung gilt Folgendes:

1. Ein Journey-Schrittereignis beginnt mit der Verarbeitung und wird im Datensatz für Journey-Schrittereignisse protokolliert
2. Durch einen automatischen Skalierungsvorgang wird die Workload auf verschiedene Dienstinstanzen verteilt
3. Dasselbe Ereignis kann von einer anderen Dienstinstanz erneut verarbeitet werden, wodurch ein zweiter Protokolleintrag mit einer anderen `_id` erstellt wird

Dies ist ein erwartetes Systemverhalten und **funktioniert wie vorgesehen**.

### Hat dies Auswirkungen auf die Ausführung von Journeys oder den Nachrichtenversand?

**Nein.** Die Auswirkungen sind auf die Protokollierung beschränkt. [!DNL Adobe Journey Optimizer] verfügt über integrierte Deduplizierungsmechanismen auf der Nachrichtenausführungsebene, die Folgendes sicherstellen:

* An jedes Profil wird nur eine Nachricht (E-Mail, SMS, Push-Benachrichtigung usw.) gesendet
* Aktionen werden nur einmal ausgeführt
* Journey-Ausführung läuft korrekt ab

Sie können dies prüfen, indem Sie den `ajo_message_feedback_event_dataset` abfragen oder die Aktionsausführungsprotokolle konsultieren. Sie werden sehen, dass trotz der doppelten Journey-Schrittereigniseinträge tatsächlich nur eine Nachricht gesendet wurde.

### Wie kann ich diese Fälle in meinen Abfragen erkennen?

Gehen Sie beim Analysieren von Daten zu Journey-Schrittereignissen wie folgt vor:

1. **Prüfen Sie das `_id`-Feld**: Echte Duplikate auf Systemebene würden denselben Wert für `_id` aufweisen. Unterschiedliche Werte für `_id` weisen auf separate Protokolleinträge aus dem oben beschriebenen Rebalancing-Szenario hin.

2. **Prüfen Sie den Nachrichtenversand**: Sehen Sie sich auch die Daten zum Nachrichten-Feedback an, um sich zu vergewissern, dass nur eine Nachricht gesendet wurde:

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

3. **Gruppieren Sie nach eindeutigen Kennungen**: Verwenden Sie beim Zählen von Ausführungen `_id`, um genaue Zahlen zu erhalten:

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### Was sollte ich tun, wenn mir das auffällt?

Dies ist ein normales Systemverhalten. Es ist **keine Aktion erforderlich**. Die Duplikatprotokollierung weist nicht auf ein Problem mit Ihrer Journey-Konfiguration oder dem Nachrichtenversand hin.

Wenn Sie Berichte oder Analysen auf der Grundlage von Journey-Schrittereignissen erstellen:

* Verwenden Sie `_id` als Primärschlüssel für die Zählung eindeutiger Ereignisse
* Sehen Sie sich bei der Analyse des Nachrichtenversands auch Datensätze mit Nachrichten-Feedback an
* Beachten Sie, dass die Zeitplanungsanalyse Einträge innerhalb weniger Sekunden gruppiert anzeigen kann

Weitere Informationen zum Abfragen von Journey-Schrittereignissen finden Sie unter [Beispiele für Abfragen](../reports/query-examples.md).

## Fehlerbehebung bei Diskrepanzen der Dashboard-Metriken {#dashboard-metrics}

Wenn die im Dashboard **Übersicht** angezeigten Metriken nicht mit der tatsächlichen Anzahl der Journeys auf der Registerkarte **Durchsuchen** übereinstimmen, überprüfen Sie Folgendes:

* Stellen Sie sicher, dass in den betreffenden Journeys in den letzten 24 Stunden Traffic aufgetreten ist, da Journeys ohne aktuelle Aktivität nicht im Dashboard angezeigt werden.
* Vergewissern Sie sich, dass Sie über die entsprechenden Zugriffsberechtigungen verfügen, um alle Journeys in Ihrem Unternehmen anzuzeigen.
* Nach Änderungen an Ihren Journeys kann es bis zu 30 Minuten dauern, bis die Metriken aktualisiert werden.

Wenn Diskrepanzen bestehen bleiben, wenden Sie sich zur Untersuchung an den Adobe-Support und fügen Sie Screenshots der Registerkarten „Übersicht“ und „Durchsuchen“ bei.
