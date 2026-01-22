---
solution: Journey Optimizer
product: journey optimizer
title: Journeys testen
description: Erfahren Sie, wie Sie Ihre Journey testen
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: testen, Journey, prüfen, Fehler, Fehlerbehebung
exl-id: 9937d9b5-df5e-4686-83ac-573c4eba983a
version: Journey Orchestration
source-git-commit: 8a1c6ccad1e0ff66bc23b6fbdd873db5f54e3e0a
workflow-type: tm+mt
source-wordcount: '1943'
ht-degree: 95%

---

# Journeys testen{#testing_the_journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_test"
>title="Journeys testen"
>abstract="Verwenden Sie Testprofile, um Ihre Journey vor der Veröffentlichung zu testen. Auf diese Weise können Sie analysieren, wie sich Kontakte in der Journey bewegen, und Fehler vor der Veröffentlichung beheben."

Nachdem Sie Ihre Journey erstellt haben, können Sie sie vor dem Veröffentlichen testen. Journey Optimizer bietet einen „Testmodus“ als Möglichkeit, Testprofile anzuzeigen, die die Journey durchlaufen, um so potenzielle Fehler vor der Aktivierung zu erkennen. Mit Schnelltests können Sie überprüfen, ob die Journeys ordnungsgemäß funktionieren, sodass Sie sie sicher veröffentlichen können.

Nur Testprofile können im Testmodus in eine Journey eintreten. Sie können entweder neue Testprofile erstellen oder vorhandene Profile in Testprofile umwandeln. Weiterführende Informationen zu Testprofilen finden Sie in [diesem Abschnitt](../audience/creating-test-profiles.md).

>[!NOTE]
>
>Vor dem Testen Ihrer Journey müssen Sie alle Fehler beheben, falls vorhanden. Erfahren Sie in ([&#x200B; Abschnitt), wie Sie Fehler vor dem Testen &#x200B;](../building-journeys/troubleshooting.md). Wenn Testprofile im Testmodus nicht fortschreiten, siehe [Fehlerbehebung bei Testmodusübergängen](troubleshooting-execution.md#troubleshooting-test-transitions).

## Wichtige Hinweise {#important_notes}

### Allgemeine Einschränkungen

* **Nur Testprofile**: Nur Personen, die im Echtzeit-Kundenprofil-Service als „Testprofile“ gekennzeichnet sind, können im Testmodus in eine Journey eintreten. [Erfahren Sie, wie Sie Testprofile erstellen](../audience/creating-test-profiles.md).
* **Namespace-Anforderung**: Der Testmodus ist nur für Entwurfs-Journeys verfügbar, die einen Namespace verwenden. Der Testmodus muss prüfen, ob eine in die Journey eintretende Person ein Testprofil ist oder nicht, und muss daher in der Lage sein, Adobe Experience Platform zu erreichen.
* **Profil-Limit**: Während einer einzelnen Testsitzung können maximal 100 Testprofile in eine Journey eintreten.
* **Ereignisauslösung**: Ereignisse können nur über die Benutzeroberfläche ausgelöst werden. Ereignisse können nicht mithilfe einer API von externen Systemen ausgelöst werden.
* **Benutzerdefinierte Upload-Zielgruppen**: Der Journey-Testmodus unterstützt keine Attributanreicherung von [benutzerdefinierten Upload-Zielgruppen](../audience/custom-upload.md).

### Verhalten während und nach dem Test

* **Deaktivieren des Testmodus**: Wenn Sie den Testmodus deaktivieren, werden alle Profile entfernt, die sich derzeit in der Journey befinden oder zuvor in diese eingetreten sind, und das Reporting wird gelöscht.
* **Flexible Reaktivierung**: Sie können den Testmodus beliebig oft aktivieren/deaktivieren.
* **Automatische Deaktivierung**: Journeys, die im Testmodus **eine Woche lang** inaktiv bleiben, werden automatisch auf den Entwurfsstatus zurückgesetzt, um die Leistung zu optimieren und eine überflüssige Ressourcenlast zu verhindern.
* **Bearbeiten und Veröffentlichen**: Während der Testmodus aktiv ist, können Sie die Journey nicht ändern. Sie können die Journey jedoch direkt veröffentlichen, ohne den Testmodus zuvor deaktivieren zu müssen.

### Ausführung

* **Aufspaltungsverhalten**: Wenn die Journey eine Aufspaltung erreicht, wird immer die oberste Verzweigung ausgewählt. Ordnen Sie Verzweigungen neu an, wenn Sie einen anderen Pfad testen möchten.
* **Ereignis-Timing**: Wenn die Journey mehrere Trigger enthält, lösen Sie die Ereignisse nacheinander aus. Wird ein Ereignis zu früh (bevor der erste Warteknoten abgeschlossen ist) oder zu spät (nach dem konfigurierten Timeout) gesendet, wird das Ereignis verworfen und das Profil wird an einen Timeout-Pfad gesendet. Vergewissern Sie sich stets, dass Verweise auf Ereignis-Payload-Felder gültig bleiben, indem Sie die Payload innerhalb des definierten Fensters senden.
* **Aktives Datumsfenster**: Stellen Sie sicher, dass das für die Journey konfigurierte Fenster für [Start- und Enddatum/-zeit](journey-properties.md#dates) beim Initiieren des Testmodus die aktuelle Zeit enthält. Andernfalls werden ausgelöste Testereignisse im Hintergrund verworfen. Weitere Informationen zur Fehlerbehebung bei diesem Problem [auf dieser Seite](troubleshooting-execution.md#troubleshooting-test-transitions).
* **Reaktionsereignisse**: Für Reaktionsereignisse mit einem Timeout beträgt die minimale und die standardmäßige Wartezeit 40 Sekunden.
* **Testdatensätze**: Im Testmodus ausgelöste Ereignisse werden in dedizierten Datensätzen gespeichert, die wie folgt gekennzeichnet sind: `JOtestmode - <schema of your event>`
* **Freigegebene Infrastruktur** - Der Testmodus wird auf derselben Infrastruktur ausgeführt wie die Produktion. Bei hohem Traffic-Aufkommen kann es zu Verzögerungen beim E-Mail-Versand oder bei der Ereignisverarbeitung kommen. Überprüfen Sie in diesem Fall die Plattform-Traffic-Dashboards oder wiederholen Sie Ihre Tests außerhalb der Spitzenzeiten.

<!--
* Fields from related entities are hidden from the test mode.
-->

## Aktivieren des Testmodus

Gehen Sie wie folgt vor, um den Testmodus zu verwenden:

1. Um den Testmodus zu aktivieren, klicken Sie in der rechten oberen Ecke auf die Schaltfläche **[!UICONTROL Testmodus]**.

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

## Auslösen Ihrer Ereignisse {#firing_events}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_configuration"
>title="Konfigurieren des Testmodus"
>abstract="Wenn Ihre Journey mehrere Ereignisse enthält, wählen Sie ein Ereignis aus der Dropdown-Liste aus. Konfigurieren Sie dann für jedes Ereignis die weitergeleiteten Felder und die Ausführung des Ereignisversands."

Verwenden Sie die Schaltfläche **[!UICONTROL Ereignis auslösen]**, um ein Ereignis zu konfigurieren, das eine Person zum Eintritt in eine Journey veranlasst.


### Voraussetzungen {#trigger-events-prerequisites}

Als Voraussetzung müssen Sie wissen, welche Profile in Adobe Experience Platform als Testprofile gekennzeichnet sind. Der Testmodus lässt nur diese Profile in der Journey zu.

Das Ereignis muss eine ID enthalten. Die erwartete ID hängt von der Ereigniskonfiguration ab. Es kann sich beispielsweise um eine ECID oder eine E-Mail-Adresse handeln. Der Wert dieses Schlüssels muss im Feld **Profilkennung** hinzugefügt werden.

Wenn Ihre Journey den Testmodus nicht aktivieren kann und dabei der Fehler `ERR_MODEL_RULES_16` ausgegeben wird, stellen Sie im Falle von Kanalaktionen sicher, dass das verwendete Ereignis einen [Identity-Namespace](../audience/get-started-identity.md) enthält.

Der Identity-Namespace dient dazu, die Testprofile eindeutig zu identifizieren. Wenn beispielsweise die E-Mail-Adresse zur Identifizierung der Testprofile verwendet wird, sollte der Identity-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identity-Namespace **Telefon** ausgewählt werden.

>[!NOTE]
>
>* Wenn Sie ein Ereignis im Testmodus auslösen, wird ein reales Ereignis generiert, d. h. es beeinflusst auch andere Journeys, die dieses Ereignis überwachen.
>
>* Stellen Sie sicher, dass jedes Ereignis im Testmodus in der richtigen Reihenfolge und innerhalb des konfigurierten Wartefensters ausgelöst wird. Bei einer Wartezeit von beispielsweise 60 Sekunden darf das zweite Ereignis erst nach Ablauf dieser Wartezeit von 60 Sekunden und vor Ablauf des Timeout-Limits ausgelöst werden.
>

### Ereigniskonfiguration {#trigger-events-configuration}

Wenn Ihre Journey mehrere Ereignisse enthält, wählen Sie ein Ereignis aus der Dropdown-Liste aus. Konfigurieren Sie dann für jedes Ereignis die weitergeleiteten Felder und die Ausführung des Ereignisversands. Über die Benutzeroberfläche können Sie die richtigen Informationen in der Ereignis-Payload angeben und prüfen, ob der Informationstyp korrekt ist. Der Testmodus speichert die zuletzt in einer Testsitzung verwendeten Parameter zur späteren Verwendung.

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

Die Anzahl der Kontakte (technisch gesehen handelt es sich um Instanzen), die sich derzeit innerhalb der Journey befinden, wird angezeigt. Außerdem finden Sie hier nützliche Informationen zu jedem Kontakt:

* _ID_: die interne ID des Kontakts in der Journey. Diese kann zum Debugging verwendet werden.
* _currentstep_: der Schritt, in dem sich der Kontakt in der Journey befindet. Es wird empfohlen, Ihren Aktivitäten Labels zu geben, damit Sie sie leichter identifizieren können.
* _currentstep_ > phase: der Status der Journey des Kontakts (Läuft, Abgeschlossen, Fehler, Zeitüberschreitung). Weitere Informationen finden Sie unten.
* _currentstep_ > _extraInfo_: Beschreibung des Fehlers und andere kontextuelle Informationen.
* _currentstep_ > _fetchErrors_: Informationen zu Datenfehlern beim Abrufen, die während dieses Schritts aufgetreten sind.
* _externalKeys_: der Wert für die im Ereignis definierte Schlüsselformel.
* _enrichedData_: die Daten, die die Journey abgerufen hat, falls sie Datenquellen verwendet hat.
* _transitionHistory_: die Schritte, denen der betreffende Kontakt folgte. Bei Ereignissen wird die Payload angezeigt.
* _actionExecutionErrors_: Informationen zu den aufgetretenen Fehlern.

Hier eine Liste der verschiedenen Status der Journey eines Kontakts:

* _Läuft_: der Kontakt befindet sich derzeit in der Journey.
* _Beendet_: der Kontakt befindet sich am Ende der Journey.
* _Fehler_: der Kontakt wird aufgrund eines Fehlers in der Journey gestoppt.
* _Zeitüberschreitung_: der Kontakt wird aufgrund eines Schritts, der zu viel Zeit in Anspruch genommen hat, in der Journey gestoppt.

Wenn ein Ereignis im Testmodus ausgelöst wird, wird automatisch ein Datensatz mit dem Namen der Quelle generiert.

Der Testmodus erstellt automatisch ein Erlebnisereignis und sendet es an Adobe Experience Platform. Der Name der Quelle für dieses Erlebnisereignis lautet „Journey Orchestration Test-Ereignisse“.

