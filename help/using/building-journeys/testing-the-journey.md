---
solution: Journey Optimizer
product: journey optimizer
title: Testen der Journey
description: Erfahren Sie, wie Sie Ihre Journey testen
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: testen, Journey, prüfen, Fehler, Fehlerbehebung
exl-id: 9937d9b5-df5e-4686-83ac-573c4eba983a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/J9pg9Bw--ksizTh2itQnPu3uo54eoPj9ocgxwTgrLhE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c3f67a94-f1ff-4f5e-bf6f-bc22405930a3
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 8d9c09a7be3757624c72a0a9d2739d0dbb48adeb
workflow-type: tm+mt
source-wordcount: 3541
ht-degree: 47%

---


# Testen der Journey{#testing_the_journey}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Ihren Journey vor der Veröffentlichung überprüfen können, indem Sie eine Simulation mit simulierten Benutzenden oder einen Testmodus mit Testprofilen verwenden, um Fehler frühzeitig zu erkennen.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_test"
>title="Journeys testen"
>abstract="Verwenden Sie Testprofile, um Ihre Journey vor der Veröffentlichung zu testen. Auf diese Weise können Sie analysieren, wie sich Kontakte in der Journey bewegen, und Fehler vor der Veröffentlichung beheben."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/create-journey/journey-dry-run" text="Journey-Probelauf"

Nachdem Sie Ihre Journey erstellt haben, können Sie sie vor dem Veröffentlichen testen. [!DNL Adobe Journey Optimizer] bietet den „Testmodus“ als Möglichkeit, Testprofile anzuzeigen, während sie sich auf der Journey bewegen, und potenzielle Fehler vor der Aktivierung zu erkennen. Mit Schnelltests können Sie überprüfen, ob die Journeys ordnungsgemäß funktionieren, sodass Sie sie sicher veröffentlichen können.

Nur Testprofile können im Testmodus in eine Journey eintreten. Sie können entweder neue Testprofile erstellen oder vorhandene Profile in Testprofile umwandeln. Weiterführende Informationen zu Testprofilen finden Sie in [diesem Abschnitt](../audience/creating-test-profiles.md).

Adobe Journey Optimizer bietet zwei Möglichkeiten zum Testen und Validieren Ihres Journey:

* **[Simulation](simulate-journey.md#test-users)**: Setzen Sie die Journey auf **[!UICONTROL Simulation]** und verwenden Sie simulierte Benutzende (temporäre Profile, die Sie ohne vorab erstellte Profile in Adobe Experience Platform erstellen oder im laufenden Betrieb generieren).

* **[Testmodus](#test-profiles)**: Persistente Profile, die in Adobe Experience Platform explizit als Testprofile gekennzeichnet sind. Sie können in mehreren Testsitzungen wiederverwendet werden. Diese Methode wird für Tests mit konsistenten, vordefinierten Profildaten empfohlen. [Erfahren Sie, wie Sie Testprofile erstellen](../audience/creating-test-profiles.md).

>[!NOTE]
>
>Vor dem Testen Ihrer Journey müssen Sie alle Fehler beheben, falls vorhanden. Wie Sie Fehler vor dem Testen feststellen können, erfahren Sie [in diesem Abschnitt](../building-journeys/troubleshooting.md). Wenn Testprofile im Testmodus nicht fortgesetzt werden, finden Sie weitere Informationen unter [Fehlerbehebung bei Transitionen im Testmodus](troubleshooting-execution.md#troubleshooting-test-transitions).

## Wichtige Hinweise {#important_notes}

Lesen Sie diese Hinweise, bevor Sie Tests auf Ihrem Journey durchführen.

### Allgemeine Einschränkungen

* **Nur Testprofile**: Nur Personen, die im Echtzeit-Kundenprofil-Service als „Testprofile“ gekennzeichnet sind, können im Testmodus in eine Journey eintreten. [Erfahren Sie, wie Sie Testprofile erstellen](../audience/creating-test-profiles.md).
* **Namespace-Anforderung**: Der Testmodus ist nur für Entwurfs-Journeys verfügbar, die einen Namespace verwenden. Der Testmodus muss überprüfen, ob eine Person, die die Journey betritt, ein Testprofil ist oder nicht, und muss daher in der Lage sein, [!DNL Adobe Experience Platform] zu erreichen.
* **Profil-Limit**: Während einer einzelnen Testsitzung können maximal 100 Testprofile in eine Journey eintreten.
* **Ereignisauslösung**: Ereignisse können nur über die Benutzeroberfläche ausgelöst werden. Ereignisse können nicht mithilfe einer API von externen Systemen ausgelöst werden.
* **Benutzerdefinierte Upload-Zielgruppen**: Der Journey-Testmodus unterstützt keine Attributanreicherung von [benutzerdefinierten Upload-Zielgruppen](../audience/custom-upload.md).

### Verhalten während und nach dem Test

* **Deaktivieren des Testmodus**: Wenn Sie den Testmodus deaktivieren, werden alle Profile entfernt, die sich derzeit in der Journey befinden oder zuvor in diese eingetreten sind, und das Reporting wird gelöscht.
* **Flexible Reaktivierung**: Sie können den Testmodus beliebig oft aktivieren/deaktivieren.
* **Automatische Deaktivierung** - Journey, die im Testmodus über eine **Woche lang inaktiv bleiben** beenden den Testmodus automatisch und kehren zum Entwurfsstatus zurück. Es geht kein Journey-Inhalt verloren; nur die Testmodussitzung endet.
* **Bearbeiten und Veröffentlichen**: Während der Testmodus aktiv ist, können Sie die Journey nicht ändern. Sie können die Journey jedoch direkt veröffentlichen, ohne den Testmodus zuvor deaktivieren zu müssen.
* **Nachrichtenversand** - Im Testmodus werden Nachrichten an die tatsächlichen Posteingänge von Testprofilen gesendet, wobei dieselbe Versand-Pipeline wie die Produktion verwendet wird. Dies unterscheidet sich vom [Journey-Probelauf](journey-dry-run.md) der die Journey-Ausführung simuliert, ohne Nachrichten zu senden oder echte Kanalaktionen auszulösen. Keine der Methoden repliziert jeden Aspekt eines Live-Versands. Verwenden Sie eine Staging-Umgebung für die vollständige End-to-End-Validierung.

### Ausführung

* **Aufspaltungsverhalten** - Wenn die Journey eine Aufspaltung erreicht, wird die obere Verzweigung immer im Testmodus ausgewählt. Dies spiegelt nicht den statistisch ausgewählten Pfad während der Live-Ausführung wider. Ordnen Sie Verzweigungen neu an, wenn Sie einen anderen Pfad testen möchten.
* **Ereigniszeitplanung** - Wenn die Journey mehrere Ereignisse enthält, jedes Ereignis der Reihe nach mit einem Trigger versehen. Wird ein Ereignis zu früh (bevor der erste Warteknoten abgeschlossen ist) oder zu spät (nach der konfigurierten maximalen Wartezeit) gesendet, wird das Ereignis verworfen. Das Profil wird dann an einen Zeitüberschreitungspfad gesendet. Bestätigen Sie immer, dass alle Verweise auf Ereignis-Payload-Felder gültig bleiben, indem Sie die Payload im definierten Fenster senden.
* **Aktives Datumsfenster** - Stellen Sie sicher, dass das konfigurierte Fenster [Start- und Enddatum/-](journey-properties.md#dates)) die aktuelle Zeit enthält, wenn Sie den Testmodus starten. Andernfalls werden ausgelöste Testereignisse mit der `DISPATCHER DISCARD #16 — unqualified on journey version enablements` der Protokollmeldung im Hintergrund verworfen. Um dies während des Tests zu umgehen, legen Sie das Journey-Startdatum vorübergehend auf einen Zeitpunkt vor dem aktuellen Zeitpunkt fest und stellen Sie es dann vor der Veröffentlichung wieder her. Weitere Informationen zur Behebung dieses Problems finden Sie [auf dieser Seite](troubleshooting-execution.md#troubleshooting-test-transitions).
* **Reaktionsereignisse**: Für Reaktionsereignisse mit einem Timeout beträgt die minimale und die standardmäßige Wartezeit 40 Sekunden.
* **Testdatensätze**: Im Testmodus ausgelöste Ereignisse werden in dedizierten Datensätzen gespeichert, die wie folgt gekennzeichnet sind: `JOtestmode - <schema of your event>`
* **Freigegebene Infrastruktur**: Der Testmodus wird auf derselben Infrastruktur ausgeführt wie die Produktion. Bei hohem Traffic-Aufkommen kann es zu Verzögerungen beim E-Mail-Versand oder bei der Ereignisverarbeitung kommen. Prüfen Sie in diesem Fall die Plattform-Traffic-Dashboards oder wiederholen Sie Ihre Tests außerhalb der Spitzenzeiten.

<!--
* Fields from related entities are hidden from the test mode.
-->

## Aktivieren des Testmodus

Verwenden Sie die **[!UICONTROL Testmodus]**-Methode, wenn Sie Ihren Journey mit bereits in Adobe Experience Platform erstellten Testprofilen testen möchten.

1. Um den Testmodus zu aktivieren, klicken Sie auf die Schaltfläche **[!UICONTROL Simulieren]** und wählen Sie **[!UICONTROL Testmodus]**.

   ![Schaltfläche „Testmodus“ in der Journey-Oberfläche](assets/journeytest1.png)

1. Wenn die Journey mindestens eine Aktivität vom Typ **Warten** enthält, stellen Sie den Parameter **[!UICONTROL Wartezeit]** ein, um die Dauer jeder Warteaktivität und jedes Timeouts bei einem Ereignis im Testmodus festzulegen. Die Standardzeit für Wartezeiten und der Timeout für Ereignisse beträgt 10 Sekunden. Dadurch erhalten Sie die Testergebnisse schnell.

   ![Konfiguration des Wartezeit-Parameters im Testmodus](assets/journeytest_wait.png)

   >[!NOTE]
   >
   >Wenn in einer Journey ein Reaktionsereignis mit einem Timeout verwendet wird, beträgt der Standard- und Mindestwert für die Wartezeit 40 Sekunden. Weitere Informationen finden Sie in diesem [Abschnitt](../building-journeys/reaction-events.md).

1. Verwenden Sie die Schaltfläche **[!UICONTROL Ereignis auslösen]**, um Ereignisse zu konfigurieren und an die Journey zu senden.

   ![Schaltfläche „Ereignis auslösen“ im Testmodus](assets/journeyuctest1.png)

1. Konfigurieren Sie die verschiedenen erwarteten Felder. Geben Sie im Feld **Profilkennung** den Wert des Felds ein, das zum Identifizieren des Testprofils verwendet wird. Das kann beispielsweise die E-Mail-Adresse sein. Vergewissern Sie sich, dass Ereignisse gesendet werden, die im Zusammenhang mit Testprofilen stehen. Weitere Informationen finden Sie in [diesem Abschnitt](#firing_events).

   ![Ereigniskonfigurationsfelder mit Eingabe der Profilkennung](assets/journeyuctest1-bis.png)

1. Nachdem die Ereignisse eingegangen sind, klicken Sie auf die Schaltfläche **[!UICONTROL Protokoll anzeigen]**, um das Testergebnis anzuzeigen und zu überprüfen. Weitere Informationen finden Sie in [diesem Abschnitt](#viewing_logs).

   ![Schaltfläche „Protokoll anzeigen“ zum Anzeigen von Testergebnissen](assets/journeyuctest2.png)

1. Wenn ein Fehler auftritt, deaktivieren Sie den Testmodus, ändern Sie Ihre Journey und testen Sie sie erneut. Nach Abschluss der Tests können Sie Ihre Journey veröffentlichen. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/publish-journey.md).

## Arbeitsbeispiel: Validieren einer einfachen Journey {#test-walkthrough}

Im folgenden Beispiel wird erläutert, wie Sie eine Journey testen, die mit einem unitären Ereignis beginnt, eine E-Mail sendet, 10 Minuten wartet und dann eine Push-Benachrichtigung sendet.

So validieren Sie das Journey End-to-End:

1. Aktivieren Sie den Testmodus, indem Sie **[!UICONTROL Testmodus]** in der oberen rechten Ecke klicken. Die Arbeitsfläche wechselt in den Testmodus und die Schaltfläche **[!UICONTROL Trigger an event]** wird angezeigt.
1. Stellen Sie **[!UICONTROL Wartezeit]** auf **10 Sekunden** ein, damit der Warteknoten während des Tests schnell abgeschlossen wird.
1. Klicken Sie auf **[!UICONTROL Trigger eines Ereignisses]**, wählen Sie Ihr Ereignis aus und geben Sie eine Testprofilkennung ein (z. B. die E-Mail-Adresse eines Profils, das in Adobe Experience Platform als Testprofil gekennzeichnet ist).
1. Klicken Sie auf **[!UICONTROL Senden]**. Der visuelle Fluss wird auf der Arbeitsfläche angezeigt und färbt sich grün, wenn das Profil die einzelnen Schritte durchläuft.
1. Klicken Sie **[!UICONTROL Protokoll anzeigen]** und bestätigen Sie Folgendes in der JSON-Ausgabe:
   * `currentstep` entspricht der Aktivität, die das Profil erwartungsgemäß aufweist.
   * `phase` zeigt `running` an, während sich das Profil in einem Warteknoten befindet, und `finished`, wann es das Ende erreicht.
   * Es sind keine `actionExecutionErrors` Einträge vorhanden.
1. Aktualisieren Sie das Protokoll nach 10 Sekunden. Das Profil sollte über den Warteknoten hinaus fortgeschritten sein und die Push-Aktion ausgelöst haben.
1. Wenn alle Schritte `finished` anzeigen und keine Fehler protokolliert werden, deaktivieren Sie den Testmodus und veröffentlichen Sie die Journey.

>[!TIP]
>
>Wenn das Profil überhaupt nicht im Protokoll aufgeführt wird, überprüfen Sie Folgendes:
>* Die eingegebene Profilkennung wird in [!DNL Adobe Experience Platform] als Testprofil gekennzeichnet.
>* Das konfigurierte Start- und Enddatum der Journey enthält die aktuelle Zeit. Außerhalb dieses Fensters ausgelöste Ereignisse werden im Hintergrund verworfen. [Weitere Informationen](troubleshooting-execution.md#troubleshooting-test-transitions).

## Fehlerbehebung im Testmodus {#troubleshoot-test-mode}

Verwenden Sie diese Tabelle, um häufige Fehler im Testmodus selbst zu diagnostizieren, bevor Sie ein Support-Ticket öffnen.

| Symptom | Wahrscheinliche Ursache | Lösung |
| --- | --- | --- |
| Das Ereignis wurde erfolgreich gesendet, das Profil wird jedoch nie im Journey-Protokoll angezeigt | Namespace-Übereinstimmung in der Profilkennung - Der Namespace-Wert stimmt nicht mit dem im Ereignisschema definierten Namespace überein | Überprüfen Sie das Kennungsformat: `@{<EventName>.identityMap.entry('<NamespaceName>').first().id}`. `<NamespaceName>` muss genau mit dem Ereignisschema übereinstimmen (Groß-/Kleinschreibung beachten). Siehe [Voraussetzungen](#trigger-events-prerequisites). |
| Akzeptierte Ereignisse (200 Antworten), Journey-Trigger jedoch nicht; Protokoll `DISPATCHER DISCARD #16 — unqualified on journey version enablements` angezeigt | Das Startdatum des Journey wird in der Zukunft liegen. Testereignisse werden außerhalb des aktuellen Datumsfensters im Hintergrund verworfen | Stellen Sie das Startdatum der Journey vorübergehend auf einen Zeitpunkt vor der aktuellen Zeit ein. Stellen Sie sie vor der Veröffentlichung wieder her. Siehe [Journey-Daten](journey-properties.md#dates). |
| Zielgruppe lesen Journey zeigt ein Batch-Segmentbewertungsprotokoll, aber keine Profileinträge an | Die Batch-Segmentauswertung wird getrennt von der jeweiligen Profileingabe protokolliert. Im Batch-Protokoll wird nicht bestätigt, dass Profile auf die Journey gelangt sind | Warten Sie, bis das Stapelverarbeitungsfenster abgeschlossen ist. Testen Sie für Echtzeit-Protokoll-Feedback mit einer unitären Ereignis-Journey. |
| Testmodus kann nicht aktiviert werden; Fehler `ERR_MODEL_RULES_16` | Das Ereignis enthält keinen Identity-Namespace, der erforderlich ist, wenn die Journey eine Kanalaktion verwendet | Fügen Sie [&#x200B; Ereigniskonfiguration einen &#x200B;](../audience/get-started-identity.md)Identity-Namespace“ hinzu. |

## Auslösen Ihrer Ereignisse {#firing_events}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_configuration"
>title="Konfigurieren des Testmodus"
>abstract="Wenn Ihre Journey mehrere Ereignisse enthält, wählen Sie ein Ereignis aus der Dropdown-Liste aus. Für jedes Ereignis werden die weitergeleiteten Felder und die Ausführung des Ereignisversands konfiguriert."

Verwenden Sie die Schaltfläche **[!UICONTROL Ereignis auslösen]**, um ein Ereignis zu konfigurieren, das eine Person zum Eintritt in eine Journey veranlasst.


### Voraussetzungen {#trigger-events-prerequisites}

Als Voraussetzung müssen Sie wissen, welche Profile in [!DNL Adobe Experience Platform] als Testprofile gekennzeichnet sind. Der Testmodus lässt nur diese Profile in der Journey zu.

Das Ereignis muss eine ID enthalten. Die erwartete ID hängt von der Ereigniskonfiguration ab. Es kann sich beispielsweise um eine ECID oder eine E-Mail-Adresse handeln. Der Wert dieses Schlüssels muss im Feld **Profilkennung** hinzugefügt werden.

Der **Profilkennung**-Wert muss exakt mit der im Ereignisschema gespeicherten Identität übereinstimmen. Das Format, das zum Verweisen auf eine Identität in der Ereignis-Payload verwendet wird, ist:

`@{<EventName>.identityMap.entry('<NamespaceName>').first().id}`

Ersetzen Sie `<NamespaceName>` durch den Namespace, der genau wie in Ihrem Ereignisschema definiert ist (z. B. `Email` oder `Phone`). Eine nicht übereinstimmende Namespaces verursacht eine **stille Ablage**: Das Ereignis wird akzeptiert und gibt eine Erfolgsantwort zurück, aber das Profil gelangt nie auf die Journey und es wird kein Fehler in der Benutzeroberfläche angezeigt. Wenn ein Profil nach dem Auslösen eines Ereignisses nicht in den Testprotokollen angezeigt wird, stellen Sie sicher, dass der Namespace in Ihrer **Profilkennung** mit dem Namespace des Ereignisschemas genau übereinstimmt.

Wenn Ihre Journey den Testmodus nicht aktivieren kann und dabei der Fehler `ERR_MODEL_RULES_16` ausgegeben wird, stellen Sie im Falle von Kanalaktionen sicher, dass das verwendete Ereignis einen [Identity-Namespace](../audience/get-started-identity.md) enthält.

Der Identity-Namespace dient dazu, die Testprofile eindeutig zu identifizieren. Wenn beispielsweise die E-Mail-Adresse zur Identifizierung der Testprofile verwendet wird, sollte der Identity-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identity-Namespace **Telefon** ausgewählt werden.

>[!NOTE]
>
>* Beim Trigger eines Ereignisses im Testmodus wird ein reales Ereignis generiert, d. h. es treffen auch andere Journey, die dieses Ereignis überwachen.
>
>* Stellen Sie sicher, dass jedes Ereignis im Testmodus in der richtigen Reihenfolge und innerhalb des konfigurierten Wartefensters ausgelöst wird. Bei einer Wartezeit von beispielsweise 60 Sekunden darf das zweite Ereignis erst nach Ablauf dieser Wartezeit von 60 Sekunden und vor Ablauf des Timeout-Limits ausgelöst werden.
>

### Ereigniskonfiguration {#trigger-events-configuration}

Wenn Ihre Journey mehrere Ereignisse enthält, wählen Sie ein Ereignis aus der Dropdown-Liste aus. Konfigurieren Sie dann für jedes Ereignis die weitergeleiteten Felder und die Ausführung des Ereignisversands. Über die Benutzeroberfläche können Sie die richtigen Informationen in die Ereignis-Payload eingeben und sicherstellen, dass der Informationstyp korrekt ist. Der Testmodus speichert die zuletzt in einer Testsitzung verwendeten Parameter zur späteren Verwendung.

![Benutzeroberfläche für die Ereigniskonfiguration mit Feldern und Dropdown-Liste für die Ereignisauswahl](assets/journeytest4.png)

Über die Benutzeroberfläche können Sie einfache Ereignisparameter übergeben. Wenn Sie Sammlungen oder andere erweiterte Objekte in dem Ereignis übergeben möchten, können Sie **[!UICONTROL Code-Ansicht]** auswählen, um den gesamten Code der Payload anzuzeigen und ihn zu ändern. Beispielsweise können Sie die von technischen Anwendenden erstellten Ereignisinformationen kopieren und einfügen.

![Code-Ansicht der Ereignis-Payload im JSON-Format für die erweiterte Konfiguration](assets/journeytest5.png)

Ein technischer Anwender kann diese Benutzeroberfläche auch verwenden, um Payloads für Ereignisse zu erstellen und Ereignisse auszulösen, ohne ein Tool eines Drittanbieters verwenden zu müssen.

Wenn Sie auf die Schaltfläche **[!UICONTROL Senden]** klicken, beginnt der Test. Der Fortschritt des Kontakts in der Journey wird durch einen visuellen Verlauf dargestellt. Der Pfad wird immer grüner, je weiter sich der Kontakt in der Journey bewegt. Tritt ein Fehler auf, wird auf dem entsprechenden Schritt ein Warnsymbol angezeigt. Sie können den Cursor darauf platzieren, um weitere Informationen zum Fehler anzuzeigen und genaue Details aufzurufen (sofern verfügbar).

![Visueller Fluss des Journey-Tests mit Anzeige des Profilfortschritts und etwaiger Fehler](assets/journeytest6.png)

Wenn Sie im Bildschirm für die Ereigniskonfiguration ein anderes Testprofil auswählen und den Test erneut ausführen, wird der visuelle Verlauf geleert und stattdessen der Pfad des neuen Kontakts angezeigt.

Beim Öffnen einer Journey im Test ist der angezeigte Pfad der des zuletzt durchgeführten Tests

## Testmodus für regelbasierte Journeys {#test-rule-based}

Der Testmodus ist für Journeys, bei denen ein regelbasiertes Ereignis verwendet wird, ebenfalls verfügbar. Weitere Informationen zu regelbasierten Ereignissen finden Sie auf [dieser Seite](../event/about-events.md).

Beim Auslösen eines Ereignisses können Sie im Bildschirm **Ereigniskonfiguration** die Ereignisparameter definieren, nach denen der Test als bestanden gilt. Durch Klicken auf das QuickInfo-Symbol oben rechts können Sie die Ereignis-ID-Bedingung anzeigen. Außerdem ist neben jedem Feld, das Teil der Regelauswertung ist, ebenfalls eine QuickInfo verfügbar.

![Bildschirm für die Ereigniskonfiguration mit QuickInfos für die Regelauswertung](assets/jo-event8.png)

## Testmodus für Geschäftsereignisse {#test-business}

Nutzen Sie bei Verwendung von [Geschäftsereignis](../event/about-events.md) den Testmodus, um einen einzelnen Testprofileintritt in die Journey auszulösen, das Ereignis zu simulieren und die richtige Profil-ID zu übergeben. Sie müssen die Ereignisparameter und die Kennung des Testprofils übergeben, das während des Tests in die Journey eintritt. Im Testmodus ist kein Modus „Code-Ansicht“ für Journeys auf der Basis von Geschäftsereignissen verfügbar.

Beachten Sie, dass Sie beim ersten Trigger eines Geschäftsereignisses die Definition des Geschäftsereignisses nicht in derselben Testsitzung ändern können. Sie können nur festlegen, dass derselbe Kontakt oder eine andere Einzelperson in die Journey eintritt, die dieselbe oder eine andere Kennung übergibt. Wenn Sie die Geschäftsereignis-Parameter ändern möchten, müssen Sie den Testmodus stoppen und erneut beginnen.

## Anzeigen von Protokollen {#viewing_logs}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_logs"
>title="Testmodusprotokolle"
>abstract="Mit der Schaltfläche **Protokoll anzeigen** können Sie Testergebnisse im JSON-Format anzeigen. Diese Ergebnisse geben die Anzahl der Kontakte innerhalb der Journey sowie ihren Status an."

Mit der Schaltfläche **[!UICONTROL Protokoll anzeigen]** können Sie die Testergebnisse anzeigen. Auf dieser Seite werden die aktuellen Informationen der Journey im JSON-Format angezeigt. Mit einer Schaltfläche können Sie ganze Knoten kopieren. Sie müssen die Seite manuell aktualisieren, um die Testergebnisse der Journey zu aktualisieren.

![Testprotokolle mit Journey-Ausführungsergebnissen im JSON-Format](assets/journeytest3.png)


>[!NOTE]
>
>In den Testprotokollen werden bei einem fehlerhaften Aufruf eines Drittanbietersystems (Datenquelle oder Aktion) der Fehlercode und die Fehlerantwort angezeigt.

Die Anzahl der Kontakte (technisch als Instanzen bezeichnet), die sich derzeit auf der Journey befinden, wird angezeigt. Für jede Person werden die folgenden Informationen angezeigt:

* _ID_: die interne ID des Kontakts in der Journey. Diese kann zum Debugging verwendet werden.
* _currentstep_: der Schritt, in dem sich der Kontakt in der Journey befindet. Es wird empfohlen, Ihren Aktivitäten Labels zu geben, damit Sie sie leichter identifizieren können.
* _currentstep_ > phase: der Status der Journey des Kontakts (Läuft, Abgeschlossen, Fehler, Zeitüberschreitung). Weitere Informationen finden Sie unten.
* _currentstep_ > _extraInfo_: Beschreibung des Fehlers und andere kontextuelle Informationen.
* _currentstep_ > _fetchErrors_: Informationen zu Datenfehlern beim Abrufen, die während dieses Schritts aufgetreten sind.
* _externalKeys_: der Wert für die im Ereignis definierte Schlüsselformel.
* _enrichedData_: die Daten, die die Journey abgerufen hat, falls sie Datenquellen verwendet hat.
* _transitionHistory_: die Schritte, denen der betreffende Kontakt folgte. Bei Ereignissen wird die Payload angezeigt.
* _actionExecutionErrors_: Informationen zu den aufgetretenen Fehlern.

>[!NOTE]
>
>Das Testprotokoll zeigt nur Einträge für **unitäre Profileintrittsereignisse** an. Wenn Sie eine Journey mit dem Schritt „Zielgruppe lesen“ testen, ist das Batch-Segmentauswertungsprotokoll vom jeweiligen Profileintragsprotokoll getrennt. Ein ausgewertetes Batch-Segment bestätigt nicht, dass einzelne Profile die Journey-Schritte durchlaufen haben. Wenn nach dem Auslösen einer „Zielgruppe lesen“-Journey keine Profileinträge angezeigt werden, warten Sie, bis das Stapelverarbeitungsfenster abgeschlossen ist, bevor Sie Schlussfolgerungen ziehen.

Hier eine Liste der verschiedenen Status der Journey eines Kontakts:

* _Läuft_: der Kontakt befindet sich derzeit in der Journey.
* _Beendet_: der Kontakt befindet sich am Ende der Journey.
* _Fehler_: der Kontakt wird aufgrund eines Fehlers in der Journey gestoppt.
* _Zeitüberschreitung_: der Kontakt wird aufgrund eines Schritts, der zu viel Zeit in Anspruch genommen hat, in der Journey gestoppt.

Wenn ein Ereignis im Testmodus ausgelöst wird, wird automatisch ein Datensatz mit dem Namen der Quelle generiert.

Der Testmodus erstellt automatisch ein Erlebnisereignis und sendet es an [!DNL Adobe Experience Platform]. Der Name der Quelle für dieses Erlebnis-Ereignis lautet „Journey Orchestration Test-Ereignisse“.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird erläutert, wie Sie den Testmodus in Adobe Journey Optimizer verwenden können, um eine Journey vor der Veröffentlichung mit persistenten Testprofilen zu validieren, einschließlich der Aktivierung des Testmodus, des Auslösens von Ereignissen, des Lesens von Protokollen und der Verarbeitung von Geschäfts- und regelbasierten Ereignissen.

**intents:**
* Aktivieren des Testmodus auf einer Entwurfs-Journey, um sie mit bereits vorhandenen AEP-Testprofilen zu validieren
* Konfigurieren und Trigger von Ereignissen für Testprofile mithilfe der Benutzeroberfläche für Trigger und Ereignisse
* Warteaktivitätsdauern im Testmodus überschreiben, um den Journey-Fortschritt zu beschleunigen
* Lesen und Interpretieren der JSON-Protokollausgabe , um den Profilfortschritt zu überprüfen und Fehler zu identifizieren
* Testen von regelbasierten Journey- und Geschäftsereignis-Journey im Testmodus
* Machen Sie sich mit den Einschränkungen und Verhaltensunterschieden des Testmodus im Vergleich zur Simulation vertraut

**Glossar:**
* **Testmodus**: Ein Journey-Validierungsstatus, der es persistenten AEP-Testprofilen ermöglicht, eine Entwurfs-Journey zu durchlaufen, bevor sie veröffentlicht wird *(produktspezifisch)*
* **Testprofile**: Profile, die im Echtzeit-Kundenprofil-Service von Adobe Experience Platform explizit als Testprofile gekennzeichnet sind. Der einzige Profiltyp, der im Testmodus auf eine Journey zugreifen darf *(produktspezifisch)*
* **Visueller Fluss**: Die grüne Arbeitsflächen-Darstellung, die den Pfad anzeigt, dem ein Testprofil durch das Journey gefolgt ist
* **Protokoll anzeigen** Eine Testmodusfunktion, die den Journey-Ausführungsstatus für jede Testprofilinstanz im JSON-Format anzeigt *produktspezifisch)*
* **Journey Orchestration-Testereignisse**: Der Quellname, unter dem Testmodus-Erlebnisereignisse in Adobe Experience Platform gespeichert werden

**Leitplanken:**
* Nur Profile, die in AEP als Testprofile gekennzeichnet sind, können im Testmodus auf eine Journey zugreifen
* Für den Testmodus muss der Journey einen Namespace verwenden, um die Identität des Testprofils zu überprüfen
* Maximal 100 Testprofile pro einzelner Testsitzung
* Ereignisse können nur über die Benutzeroberfläche des Testmodus ausgelöst werden. Das Auslösen externer APIs wird nicht unterstützt
* Das benutzerdefinierte Hochladen von Zielgruppenattributen wird im Testmodus nicht unterstützt
* Die im Testmodus ausgelösten Ereignisse generieren echte Erlebnisereignisse, die auch Trigger für andere Journey verursachen können, die dasselbe Ereignis überwachen
* Im Testmodus beträgt der Standardwert für Warteaktivitäten und die meisten Ereignis-Timeouts 10 Sekunden. Für Reaktionsereignis-Timeouts wird ein Standardwert von mindestens 40 Sekunden festgelegt
* Automatische Deaktivierung - Journey, die länger als eine Woche im Testmodus inaktiv bleiben, beenden automatisch den Testmodus und kehren zum Entwurfsstatus zurück. Es geht kein Journey-Inhalt verloren; nur die Testmodussitzung endet.
* Journey-Bearbeitungen werden blockiert, wenn der Testmodus aktiv ist, aber direkte Veröffentlichung ist erlaubt
* Bei einer Aufspaltung wird immer die obere Verzweigung ausgewählt. Ordnen Sie die Verzweigungen neu an, um verschiedene Pfade zu testen
* Maximale Wartezeit für Reaktionsereignis und Standardwartezeit sind 40 Sekunden
* Ereignisse, die außerhalb des konfigurierten Start-/Enddatumsfensters der Journey gesendet werden, werden im Hintergrund verworfen
* Durch Deaktivieren des Testmodus werden alle Profile aus der Journey entfernt und die Berichte gelöscht

**Terminologie:**
* Kanonischer Name: Testmodus — Akronym: none — Varianten: Testmodus, Journey-Testmodus
* Kanonischer Name: Testprofile — Akronym: none — Varianten: Testbenutzer (nur Beschriftung der Simulationsoberfläche)
* Synonyme: „Protokoll anzeigen“ = Protokoll der Testergebnisse; „Visueller Fluss“ = Visualisierung des Canvas-Pfads
* Verwechseln Sie nicht: „Testmodus“ ≠ „Simulation“ — Der Testmodus verwendet persistente AEP-Testprofile; die Simulation verwendet temporäre simulierte Benutzende, die spontan generiert werden

**FAQ:**
* **F: Wer kann im Testmodus auf eine Journey zugreifen?** — Nur Profile, die im Echtzeit-Kundenprofil-Service von Adobe Experience Platform explizit als Testprofile gekennzeichnet sind.
* **F: Wie viele Testprofile können in einer einzelnen Testsitzung ausgeführt werden?** — Maximal 100 Testprofile pro Testsitzung.
* **F: Was passiert, wenn ich den Testmodus deaktiviere?** — Alle Profile, die sich derzeit in der Journey befinden oder zuvor darin eingegeben wurden, werden entfernt und das Reporting wird gelöscht.
* **F: Kann ich eine Journey bearbeiten, während der Testmodus aktiv ist?** — Nein. Der Journey kann nicht geändert werden, während der Testmodus aktiv ist. Sie können ihn jedoch direkt veröffentlichen, ohne zunächst den Testmodus zu deaktivieren.
* **F: Warum werden meine Testereignisse im Hintergrund verworfen?** — Ereignisse, die außerhalb des konfigurierten aktiven Datums-/Zeitfensters der Journey ausgelöst werden, werden im Hintergrund verworfen. Stellen Sie sicher, dass das Start- und Enddatum der Journey die aktuelle Uhrzeit enthalten.
* **F: Was bedeutet das Phasenfeld im Testprotokoll?** - Zeigt den aktuellen Status des Profils an: Wird ausgeführt (im Journey aktiv), Beendet (Ende erreicht), Fehler (aufgrund eines Fehlers angehalten) oder Zeitüberschreitung (aufgrund einer Zeitüberschreitung angehalten).

+++
