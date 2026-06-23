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
TQID: https://experienceleague.adobe.com/2YZ6Cjph9Le-HtwKdz4GBgEdhwIMPpVtj9yWKlV3hQ4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 2993
ht-degree: 48%

---

# Fehlerbehebung bei der Live-Journey-Ausführung {#troubleshooting-execution}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie die Ausführung einer Live-Journey beheben können, indem Sie beispielsweise überprüfen, ob Ereignisse gesendet werden, Profile bestätigen, die über die Journey eintreten und weiterlaufen, und überprüfen, ob Nachrichten zugestellt werden.

>[!ENDSHADEBOX]

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

* **Ereignis verworfen - Qualifizierungsbedingung nicht erfüllt** - Bei regelbasierten Ereignissen wird das Ereignis **empfangen, aber verworfen** und das Journey wird nicht ausgelöst, wenn die **Qualifizierungsbedingung** von der Ereignis-Payload nicht erfüllt wird (z. B. wenn ein erforderliches Feld leer ist oder fehlt oder eine Bedingung wie &quot;`isNotEmpty` eines Felds fehlschlägt„). Protokolle und Splunk-Traces können zeigen, dass das Ereignis empfangen, aber verworfen wurde, weil es die Qualifizierungsbedingung nicht erfüllte, einschließlich Verwerfen-Codes wie `notSuitableInitialEvent`. Dies ist das erwartete Verhalten: Wenn die Qualifizierungsbedingung nicht erfüllt ist, wird das Ereignis verworfen und das Journey wird für dieses Profil nicht ausgelöst. Überprüfen Sie, ob die Ereignis-Payload die erwarteten Felder und Werte enthält und ob die Regel in der Ereigniskonfiguration mit den gesendeten Daten übereinstimmt. Wenn das Ereignis durch eine **benutzerdefinierte Aktion** einer anderen Journey ausgelöst wird, finden Sie weitere Informationen unter [Umgang mit Verwerfungsereignissen und Leerlauf-Timeouts](../action/troubleshoot-custom-action.md#handling-discard-events-and-idle-timeouts) in Fehlerbehebung bei benutzerdefinierten Aktionen.

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
1. Bei ungelösten Fällen [Support kontaktieren](../start/user-interface.md#support-ticket-guidelines) mit Journey-Protokollen, den betroffenen Profil-IDs und Details zur Null-Transition

>[!NOTE]
>
>Beachten Sie, dass Ereignisse, die außerhalb des aktiven Datumsfensters der Journey gesendet werden, ohne Fehlermeldung im Hintergrund verworfen werden. Überprüfen Sie bei der Fehlerbehebung im Zusammenhang mit dem Fortschritt des Testprofils immer zuerst die Timing-Konfiguration Ihrer Journey.

## Überprüfen, wie Personen durch die Journey navigieren {#checking-how-people-navigate-through-the-journey}

Berichte zu Journey messen den Fortschritt von Kontakten innerhalb einer Journey. So können Sie leicht ermitteln, wo und warum eine Person gestoppt wurde.

Prüfen Sie folgende Punkte:

* Ist das Problem auf eine Bedingung zurückzuführen, mit der die Person ausgeschlossen wird? Beispiel: Die Bedingung lautet „Geschlecht = männlich“, während die Person eine Frau ist. Die Prüfung kann von einem Business-Anwender vorgenommen werden, solange die Bedingung nicht zu komplex ist.
* Ist das Problem auf einen Aufruf einer Datenquelle zurückzuführen, die nicht reagiert? Wenn sich die Journey im Test befindet, können diese Informationen in Testmodusprotokollen angezeigt werden. Wenn die Journey live ist, kann ein Administrator direkte Aufrufe an die Datenquelle testen und die erhaltene Antwort überprüfen. Alternativ kann ein Administrator die Journey duplizieren und dann testen.

## Ereignisse, die aufgrund einer blockierten Journey-Instanz verworfen wurden {#max-instance-stack-events-reached}

Wenn Ereignisse angezeigt werden, die aus `maxInstanceStackEventsReached` Grund verworfen wurden, hat die Journey-Laufzeit das interne Ereignisstapellimit pro Profil von 10 Ereignissen für eine bestimmte Journey-Version erreicht. Dies ist ein Schutzmechanismus, der verhindert, dass zu viele ausstehende Ereignisse gestapelt werden, während ein anderes Ereignis für dasselbe Profil noch verarbeitet wird.

Dies **weder** Zeitfenster noch ein Durchsatzlimit. Dies tritt auf, wenn die Journey-Instanz des Profils bei einem lang andauernden Schritt blockiert wird (z. B. bei langer Wartezeit, Anreicherung oder erneuten benutzerdefinierten Aktionsversuchen) und wenn Ereignisse für dasselbe, die auch auf dieser Journey verwendet werden, über das Limit von 10 Ereignissen hinaus angesammelt werden.

Um sie zu identifizieren, fragen Sie Journey-Schrittereignisse ab, bei denen der Verwerfungsgrund `maxInstanceStackEventsReached` ist (z. B. in `serviceEvents.stateMachine.eventType` oder ähnlichen Feldern). Weitere Informationen über verworfene Ereignistypen finden Sie in der [Liste der Schrittereignisfelder](../reports/sharing-field-list.md#discarded-events).

**Was können Sie tun**

* Verringern Sie lange Wartezeiten oder langsame Schritte auf Pfaden, auf denen häufig ein neuer Trigger durchgeführt werden kann.
* Upstream-Ereignisse nach Möglichkeit deduplizieren oder entschärfen.
* Teilen Sie Szenarien mit langer Laufzeit in mehrere Journey auf, um das Stapeln zu vermeiden.

## Überprüfen, ob Nachrichten erfolgreich gesendet werden {#checking-that-messages-are-sent-successfully}

Wenn Personen die Journey zwar richtig durchlaufen, aber nicht die vorgesehenen Nachrichten erhalten, können Sie Folgendes prüfen:

* [!DNL Journey Optimizer] hat die Anfrage zum Senden der Nachricht korrekt berücksichtigt. Ein Business-Anwender kann auf die zu sendende Nachricht zugreifen und prüfen, ob der Zeitpunkt der letzten Ausführung mit der Ausführungszeit Ihrer Journey übereinstimmt. Außerdem kann er die neuesten eingegangenen API-Aufrufe/-Ereignisse prüfen.
* [!DNL Journey Optimizer] hat die Nachricht erfolgreich gesendet. Überprüfen Sie die Journey-Berichte, um sicherzustellen, dass keine Fehler aufgetreten sind.

Bei einer Nachricht, die über eine benutzerdefinierte Aktion gesendet wird, kann während des Journey-Tests nur geprüft werden, ob der Systemaufruf der benutzerdefinierten Aktion zu einem Fehler führt oder nicht. Wenn der Aufruf an das externe System, das mit der benutzerdefinierten Aktion verknüpft ist, nicht zu einem Fehler führt, aber auch nicht zum Senden der Nachricht, sollten Sie das externe System überprüfen.

## Grundlegendes zu doppelten Einträgen beim Journey von Schrittereignissen {#duplicate-step-events}

In diesem Abschnitt erfahren Sie, warum doppelte Zeilen beim Journey von Schrittereignissen angezeigt werden können.

### Warum sehe ich mehrere Einträge mit derselben Journey-Instanz, demselben Profil, demselben Knoten und derselben Anfrage-ID?

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

**Nr.** Die Auswirkungen sind auf die Protokollierung beschränkt. [!DNL Adobe Journey Optimizer] verfügt über integrierte Deduplizierungsmechanismen auf der Nachrichtenausführungsebene, die Folgendes sicherstellen:

* Nur eine Nachricht (E-Mail, SMS, Push-Benachrichtigung usw.) wird an jedes Profil gesendet
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

### Was sollte ich tun, wenn ich dies feststelle?

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

Wenn Diskrepanzen bestehen bleiben, [&#x200B; Sie sich an den Adobe-Support](../start/user-interface.md#support-ticket-guidelines) und sehen Sie sich die Screenshots der Registerkarten Übersicht und Durchsuchen an, um eine Untersuchung durchzuführen.

## Tracking-Parameter mit leeren Platzhaltern in geschlossenen Journey {#tracking-parameters-closed-journeys}

Wenn Tracking-URLs in gesendeten E-Mails leere Platzhalter wie `cid=em-acou-adob{}` enthalten, kann dies darauf hinweisen, dass ein Kontextfeld wie `context.system.source.actionId` nicht aufgelöst werden konnte. Dies geschieht in der Regel, wenn eine Journey geschlossen wurde und nach einer entsprechenden Produktänderung nicht erneut veröffentlicht wurde - nur erneut veröffentlichte Journey füllen diese Kontextfelder in Tracking-URLs korrekt aus.

Um dies zu beheben, veröffentlichen Sie entweder die Journey erneut ([erstellen Sie eine neue Version und veröffentlichen Sie sie](publish-journey.md#journey-create-new-version)) oder entfernen Sie den Verweis auf das betroffene Kontextfeld aus den [URL-Tracking-Parametern](../email/url-tracking.md) in der Kanalkonfiguration oder im E-Mail-Inhalt.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Diese Seite bietet eine umfassende Referenz zur Fehlerbehebung bei der Live-Journey-Ausführung in Adobe Journey Optimizer und behandelt die Ereignisbereitstellung, Fehler bei Profileinträgen, Übergangsprobleme beim Testmodus, verworfene-Ereignisse, doppelte Step-Ereignisprotokolle, Nachrichtenversand-Prüfungen und Diskrepanzen bei Dashboard-Metriken.

**intents:**
* Diagnostizieren Sie, warum Ereignisse keinen Journey-Eintrag auslösen, indem Sie die Payload-Struktur, die Kopfzeilen und die Qualifizierungsbedingungen überprüfen
* Überprüfen, ob Profile in den Live- oder Testmodus-Journey eintreten und diesen durchlaufen
* Beheben von Fehlern beim Übergang zum Testmodus, die durch zukünftige Startdaten oder falsch konfigurierte Identity-Namespaces verursacht wurden
* Verstehen und Verarbeiten des `maxInstanceStackEventsReached` Verwerfen-Grundes für blockierte Journey-Instanzen
* Identifizieren und korrektes Abfragen doppelter Journey-Schritt-Ereignisprotokolleinträge, die durch die automatische Skalierung im Backend verursacht werden
* Untersuchen fehlender Nachrichten durch Überprüfen der Ergebnisse von Journey-Berichten und benutzerdefinierten Aktionsaufrufen
* Beheben leerer Platzhalter für Tracking-URLs in E-Mails aus geschlossenen Journey

**Glossar:**
* **Journey-Schrittereignisse**: Ein Datensatz, in dem jeder Schritt protokolliert wird, den ein Profil innerhalb einer Journey ausführt. Wird zum Erstellen von Berichten und zum Debugging von *(produktspezifisch) verwendet*
* **notApplyInitialEvent**: Ein Discard-Code, der angibt, dass ein Ereignis empfangen, aber gelöscht wurde, da die Qualifizierungsbedingung nicht erfüllt wurde *(produktspezifisch)*
* **maxInstanceStackEventsReached**: Ein Verwerfen-Code, der das pro Profil geltende Journey-Instanzereignis-Stacklimit von 10 angibt, wurde überschritten *(produktspezifisch)*
* **isValidTransition**: Eine Eigenschaft, die nur die Benutzeroberfläche enthält, um technische Details zu Journey. Ein Nullwert kann ein künftiges Startdatum oder eine beschädigte Knotenverbindung angeben, hat jedoch keinen Einfluss auf die Backend-*(produktspezifisch)*
* **Qualifizierungsbedingung** Eine Regel, die für ein Ereignis definiert wurde, das erfüllt sein muss, damit das Ereignis eine Journey zum Trigger bringt. Ereignisse, die diese Bedingung nicht erfüllen, werden verworfen
* **Neugewichtung**: Ein Backend-Vorgang zur automatischen Skalierung in AJO-Microservices, der doppelte Journey-Schritt-Ereignisprotokolleinträge mit unterschiedlichen `_id` erstellen kann

**Leitplanken:**
* Ereignisse, die außerhalb des aktiven Datums-/Zeitfensters der Journey gesendet werden, werden ohne Fehlermeldung im Hintergrund verworfen
* Das Ereignisstapellimit pro Profil für Journey-Instanzen beträgt 10 Ereignisse. Wird dieses Limit überschritten, werden Ereignisse mit `maxInstanceStackEventsReached` verworfen
* Doppelte Journey-Schritt-Ereigniseinträge mit unterschiedlichen `_id` werden erwartet und weisen nicht auf eine Duplizierung der Nachricht hin
* Übersichtsmetriken des Dashboards umfassen nur Journey mit Traffic in den letzten 24 Stunden. Die Aktualisierung von Metriken kann bis zu 30 Minuten dauern
* Geschlossene Journey, die nach einer Produktänderung nicht erneut veröffentlicht wurden, können leere Platzhalter in Tracking-URLs erzeugen

**Terminologie:**
* Kanonischer Name: Journey Step Events — Akronym: none — Varianten: Step Events, Journey Execution Logs
* Kanonischer Name: Qualifizierungsbedingung — Akronym: none — Varianten: Ereignisqualifizierungsregel, Ereignisbedingung
* Synonyme: „rebalancing“ = „automatische Skalierung“ (Backend-Vorgang, der doppelte Protokolleinträge verursacht)
* Verwechseln Sie nicht: „Duplizierte `_id`&quot; ≠ „Duplizierte Protokolleinträge aus der Neuausrichtung“ — echte Duplikate verwenden dieselbe `_id`; Duplikate, die neu ausgeglichen werden, haben unterschiedliche `_id`

**FAQ:**
* **F: Warum lösen meine Ereignisse keine Journey aus, obwohl sie erfolgreich versendet werden?** — Überprüfen Sie, ob die Journey live oder im Testmodus ist, die Payload mit der Ereignisschemastruktur übereinstimmt, die Qualifizierungsbedingung erfüllt ist und die richtigen Kopfzeilen (`X-gw-ims-org-id`, `Content-type`) enthalten sind.
* **F: Warum treten Testprofile in die Journey ein, ohne den ersten Schritt zu überwinden?** — Die häufigste Ursache ist ein in der Zukunft festgelegtes Journey-Startdatum. Ereignisse werden außerhalb des aktiven Datumsfensters im Hintergrund verworfen. Überprüfen Sie außerdem, ob das Testprofil-Flag und der Identity-Namespace übereinstimmen.
* **Q: Was bedeutet `maxInstanceStackEventsReached`?** - Die Journey-Laufzeit hat das interne 10-Ereignis-Stack-Limit für eine bestimmte Profilinstanz erreicht, in der Regel, weil ein langwieriger Schritt die Verarbeitung blockiert. Verringern Sie lange Wartezeiten, deduplizieren Sie Upstream-Ereignisse oder teilen Sie das Szenario in mehrere Journey auf.
* **F: Ich sehe doppelte Zeilen beim Journey von Schrittereignissen - stimmt etwas nicht?** — Nein. Es werden doppelte Einträge mit unterschiedlichen `_id` erwartet, die durch die automatische Skalierung im Backend entstehen. Es wird nur eine Nachricht gesendet. Überprüfen Sie mit dem `ajo_message_feedback_event_dataset`.
* **F: Warum werden in E-Mails Tracking-URLs leere Platzhalter wie `cid=em-acou-adob{}` angezeigt?** — Die Journey wurde geschlossen und nach einer Produktänderung nicht erneut veröffentlicht. Kontextfelder können nicht aufgelöst werden. Veröffentlichen Sie die Journey erneut oder entfernen Sie den Verweis auf das betroffene Kontextfeld aus den URL-Tracking-Parametern.
* **F: Warum zeigt das Dashboard „Übersicht“ andere Zahlen an als die Registerkarte „Durchsuchen“?** - Das Dashboard zählt nur Journey mit Traffic in den letzten 24 Stunden, die Aktualisierung von Metriken kann bis zu 30 Minuten dauern und Zugriffsberechtigungen können die Sichtbarkeit einschränken.

+++
