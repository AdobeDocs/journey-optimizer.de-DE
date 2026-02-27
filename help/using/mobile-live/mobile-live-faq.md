---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zu Live-Aktivitäten
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e7e994ca-aa0c-4e86-8710-c87430b74188
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 48%

---

# Häufig gestellte Fragen {#mobile-live-faq}

## Allgemeine Fragen

+++Was ist der Unterschied zwischen einer Live -Aktivität und einer Push-Benachrichtigung?

Live-Aktivität bietet beständige Echtzeit-Updates auf dem Sperrbildschirm und auf Dynamic Island, ohne dass Benutzer ihr Gerät entsperren müssen. Push-Benachrichtigungen sind temporäre Warnhinweise, die nach dem Verwerfen ausgeblendet werden. Live-Aktivität bleibt sichtbar und kann mehrmals aktualisiert werden, bis sie explizit beendet wird.

+++

+++Wie viele Live-Aktivitätsinstanzen können gleichzeitig aktiv sein?

Eine iOS-App kann mehrere Live-Aktivitätsinstanzen gleichzeitig ausführen, darunter mehrere, die denselben `ActivityAttributes` verwenden.

Es gibt keine feste Grenze, die von Entwicklerinnen und Entwicklern dafür vorgegeben wird, wie viele Live-Aktivitätsinstanzen eines bestimmten Attributtyps vorhanden sein können. Sie können so viele starten, wie Ihre App-Logik erfordert, beispielsweise eine pro laufendem Versand oder pro laufender Ausführung. IOS erzwingt jedoch eine Beschränkung auf Systemebene, die angibt, wie viele Live-Aktivitätsinstanzen gleichzeitig aktiv oder sichtbar sein können.

In der Praxis gilt Folgendes:

* iOS unterstützt in der Regel bis zu fünf gleichzeitige Live-Aktivitätsinstanzen pro App.

* Wenn Sie diese Zahl überschreiten, kann das System die Anzeige einiger Aktivitätsinstanzen einstellen oder ältere beenden, um Ressourcen zu sparen.

* Jede Live-Aktivitätsinstanz verfügt über eine eindeutige `Activity.id`, mit der Sie sie einzeln aktualisieren oder beenden können.

+++

+++Müssen Benutzer die App öffnen, um Live-Aktivitätsaktualisierungen zu erhalten?

Nein. Eine Live-Aktivität kann auch dann gestartet, aktualisiert und remote beendet werden, wenn die App vollständig geschlossen ist. Dies ist einer der wichtigsten Vorteile der Funktion.

+++

+++Welche iOS-Versionen unterstützen Live-Aktivitäten?

* iOS 16.1+: Grundlegende Unterstützung für Live-Aktivitäten
* iOS 17.2 und höher: Push-to-Start-Funktion (Remote-Start ohne Öffnen des Programms)
* iOS 18+: Unterstützung von Broadcast-Kanälen für zielgruppenbasierte Live-Aktivitäten
+++

+++Wie lange kann eine Live-Aktivität aktiv bleiben?

Apple beschränkt die Live-Aktivität auf **8 Stunden aktive Updates**. Danach beendet das System die Aktivität automatisch, sie kann aber bis zu **12 weitere Stunden** in einem statischen Zustand angezeigt werden, bevor sie entfernt wird. Sie können eine Live-Aktivität auch früher beenden, indem Sie eine `dismissalDate` festlegen oder `activity.end()` in Ihrer App explizit aufrufen.

+++

### Fragen von Entwickelnden

+++Muss ich eine separate Widget-Erweiterung für die Live -Aktivität erstellen?

Ja. Die Live-Aktivität wird über WidgetKit angezeigt. Daher müssen Sie eine Widget-Erweiterung in Ihrem Xcode-Projekt erstellen und die `ActivityConfiguration` implementieren.
[Weitere Informationen zur Widget-Konfiguration](mobile-live-configuration-sdk.md)

+++

+++Kann ich dieselbe `LiveActivityAttributes` für lokale und Remote-Live-Aktivitäten verwenden?

Ja. Dieselbe Attributklasse funktioniert sowohl für lokal gestartete als auch für remote gestartete (Push-to-Start) Live-Aktivitäten. Sie müssen sicherstellen, dass Sie sie mit `Messaging.registerLiveActivity()` registrieren.

+++

+++Was passiert, wenn ich eine Aktualisierung für eine Live-Aktivität sende, die nicht existiert?

Wenn Sie eine Aktualisierung oder ein Ereignis zum Beenden für eine nicht vorhandene `liveActivityID` oder `channelID` senden, schlägt die Anfrage auf dem Gerät im Hintergrund fehl. Vergewissern Sie sich immer, dass Sie verfolgen, welche Live-Aktivitätsinstanzen für jeden Benutzer aktiv sind.

+++

+++Kann ich die Live -Aktivität im iOS-Simulator testen?

Ja, Sie können im iOS-Simulator sowohl lokal gestartete als auch remote gestartete Live-Aktivitäten testen.

* **Lokal**: Dazu gehört das Erstellen, Aktualisieren und Beenden von Live-Aktivitäten direkt in Ihrer App mithilfe von **ActivityKit-APIs**.

* **Remote**: Um die Live-Aktivitätsfunktion remote zu testen, integrieren Sie unsere Messaging-SDK in Ihre App und verwenden Sie die bereitgestellten Ausführungs-APIs, um Remote-Start, -Update und -Ende an Ihr Testgerät oder Ihren iOS-Simulator zu senden. Dies funktioniert ähnlich, wie Push-Benachrichtigungen derzeit mit der Adobe SDK-Integration getestet werden können.

+++

+++Wie gehe ich mit Aktualisierungen um, wenn sich die App im Hintergrund befindet?

Das SDK übernimmt dies automatisch. Nach der Registrierung erhält die Live-Aktivität Aktualisierungen, selbst wenn die App beendet wird. Es sind keine zusätzlichen Hintergrundmodi erforderlich.
+++

+++Was ist der Unterschied zwischen `liveActivityID` und `channelID`?

* `liveActivityID`: Wird für individuelle (unitäre) Live-Aktivitäten verwendet, die auf bestimmte Benutzende abzielen. Jede ID stellt eine eindeutige Live-Aktivitätsinstanz dar.
* `channelID`: Wird für die Übertragung einer Live-Aktivität an Zielgruppen verwendet. Alle Benutzenden in der Zielgruppe erhalten dieselben Aktualisierungen über denselben Kanal.
+++

+++Kann ich das Erscheinungsbild der Dynamic Island separat vom Sperrbildschirm anpassen?

Ja. `ActivityConfiguration` verfügt über eigene Anzeigeoptionen für Sperrbildschirminhalte und Dynamic Island-Inhalte (erweiterte, kompakte und minimierte Zustände), deren Design jeweils unabhängig voneinander ist.
+++

+++Muss ich Push-Token manuell speichern?

Nein. Wenn Sie einen Typ einer Live-Aktivität mit `Messaging.registerLiveActivity()` registrieren, erfasst und verwaltet das SDK automatisch Push-Token für Sie.
+++

+++Gibt es Beschränkungen für Remote-Starts von Live-Aktivitäten?

Ja. Remote-Starts über `ActivityKit` unterliegen den vom System erzwungenen Einschränkungen. Wenn Sie mehrere Startanfragen in schneller Folge ausführen, kann iOS weitere Startanfragen aufgrund von Live-Aktivitätsquoten oder Budgetbeschränkungen ablehnen. Nach etwa 5 aufeinander folgenden Startversuchen schlagen nachfolgende Anfragen fehl, bis eine kurze Abklingzeit vergeht.

+++

+++Wie hoch ist das Budget für Updates mit hoher Priorität?

Apple gibt keine exakte numerische Begrenzung für Live-Aktivitätsaktualisierungen mit hoher Priorität `(priority: 10)`. Das System verwaltet ein dynamisches internes Budget, das begrenzt, wie oft solche Aktualisierungen gesendet werden können. Wenn innerhalb eines kurzen Zeitraums zu viele Updates mit hoher Priorität ausgegeben werden, kann iOS nachfolgende Updates drosseln oder verzögern.

So minimieren Sie Einschränkungen:

* **Prioritätsstufen ausgleichen**: Je nach Wichtigkeit werden sowohl Aktualisierungen des `(priority: 5)` als auch des hohen `(priority: 10)` kombiniert.
* **Sparsam mit hoher Priorität verwenden**: Bewahren Sie hohe Priorität für zeitkritische Updates auf, z. B. den Versandfortschritt, den Bestellstatus oder Live-Sportergebnisse.
* **Häufige Updates unterstützen**: Nehmen Sie `NSSupportsLiveActivitiesFrequentUpdates` in die `Info.plist` Ihrer App auf und setzen Sie sie auf **JA**, wenn Sie häufige Updates benötigen.

+++

### Fragen von Marketing-Fachleuten

+++Kann ich den Inhalt der Live-Aktivität für jeden Benutzer in einer Broadcast-Kampagne personalisieren?

Übertragungskampagnen senden dieselben Inhalte an alle Benutzenden in der Zielgruppe. Verwenden Sie für personalisierte Inhalte einheitliche (Transaktions-)Kampagnen, die auf einzelne Benutzende abzielen.
+++

+++Woher weiß ich, ob meine Live-Aktivität erfolgreich bereitgestellt wurde?

[Überwachen Sie Ihre Kampagnenanalysen](../reports/campaign-global-report-cja-activity.md) in Adobe Journey Optimizer. Sie können Versandraten, Fehler und Interaktionsmetriken nachverfolgen. Erwägen Sie auch, benutzerdefinierte Analyseereignisse in Ihrer App zu implementieren.
+++

+++Kann ich Live-Aktivitäten im Voraus planen?

Durch den API-Aufruf wird die Live-Aktivität sofort Trigger. Sie können Ihre API-Aufrufe jedoch über Ihre Backend-Systeme planen oder die Orchestrierungsfunktionen von Journey Optimizer verwenden, um sie zeitlich passend festzulegen.
+++

+++Was passiert, wenn ich ein „Start“-Ereignis für eine bereits vorhandene Live-Aktivität sende?

Beim Remote-Start von Live-Aktivitäten über die Ausführungs-APIs von Adobe:

* Sie können der Anfrage einen `x-request-id`-Header hinzufügen. Idealerweise sollte eine Eins-zu-eins-Beziehung zwischen jeder `liveActivityID` und der entsprechenden `x-request-id` bestehen. Dadurch wird sichergestellt, dass bei mehreren Anfragen mit derselben `x-request-id` und `liveActivityID` Kombination nur eine Live-Aktivitätsinstanz auf dem Gerät gestartet und doppelte Anfragen ignoriert werden.

* Wenn der `x-request-id`-Header ausgelassen wird, wird jede Anfrage unabhängig behandelt, was dazu führen kann, dass mehrere Live-Aktivitätsinstanzen mit demselben `liveActivityID` erstellt werden. In solchen Fällen können zukünftige Aktualisierungen fehlschlagen oder nur für eine der aktiven Instanzen gelten.

* Der `x-request-id`-Wert sollte nicht in verschiedenen `liveActivityIDs` in separaten API-Anfragen wiederverwendet werden.

+++

+++Kann ich verschiedene Live-Aktivitätserlebnisse in A/B testen?

Ja. Erstellen Sie mehrere Kampagnen mit unterschiedlichen Inhaltsstrukturen und verwenden Sie die Experimentierfunktionen von Adobe Journey Optimizer, um zu testen, welche besser funktioniert. Stellen Sie sicher, dass Ihre App alle Inhaltszustandsvarianten unterstützt.

+++

+++Wie oft sollte ich eine Live-Aktivität aktualisieren?

Aktualisieren Sie sie nur, wenn sich wichtige Informationen ändern, da zu häufige Aktualisierungen den Akku entladen und die Qualität des Anwendererlebnisses beeinträchtigen können. Bei Echtzeit-Szenarien wie dem Versand-Tracking ist in der Regel ein Abstand von 30 bis 60 Sekunden akzeptabel. Bei sich langsamer ändernden Inhalten wie Zwischenständen von Sportereignissen werden nur Aktualisierungen bei wichtigen Geschehnissen vorgenommen.

+++

+++Kann ich Benutzende darauf ansprechen, ob sie Live-Aktivität aktiviert haben?

Sie müssen mit Ihrem Entwicklungs-Team zusammenarbeiten, um diese Voreinstellung als Benutzerattribut nachzuverfolgen und an Adobe Experience Platform zu übergeben. Anschließend können Sie basierend auf diesem Attribut segmentieren.

+++

### API-Fragen

+++Was ist der Unterschied zwischen `timestamp` und `dismissal-date`?

* `timestamp`: Die aktuelle Epochenzeit, zu der das Ereignis auftritt. Wird für alle Ereignisse benötigt.
* `dismissal-date`: Ein zukünftiger Zeitraum, in dem die Live-Aktivität automatisch beendet werden soll. Dies ist nur für „Ende“-Ereignisse erforderlich.

+++

+++Muss ich bei jedem Aktualisierungsaufruf alle `attributes`-Felder senden?

Ja, basierend auf Ihrer `LiveActivityAttribute`-Klasse.

* Alle Felder aus Ihrem Attributobjekt, einschließlich `liveActivityData`, sollten in jedem Aufruf für Start, Aktualisierungen und Ende enthalten sein.
* Nur die `content-state`-Felder stellen dar, was sich tatsächlich dynamisch bei einer laufenden Live-Aktivität ändert.
* Schließen Sie auch ein Warnhinweisobjekt ein. Dadurch wird sichergestellt, dass die Push-Benachrichtigung als für Benutzende sichtbare Benachrichtigung und nicht als stille Hintergrundbenachrichtigung behandelt wird. Nur für „Start“-Fälle erforderlich, ansonsten optional.

+++

+++In welchem Format sollten Epochenzeitstempel vorliegen?

Verwenden Sie Unix-Epochenzeit in **Sekunden**, nicht Millisekunden. Beispiel: `1759937682`

+++

+++Kann ich dieselbe `requestId` für mehrere API-Aufrufe verwenden?

Nein. Jede API-Anfrage sollte über eine eindeutige `requestId` verfügen, um die Idempotenz und ein ordnungsgemäßes Tracking sicherzustellen. Verwenden Sie UUIDs oder ähnliche eindeutige Kennungen.

+++

+++Welche Authentifizierung ist für die Headless-API erforderlich?

Informationen zu Authentifizierungspflichten, einschließlich OAuth-Token und API-Schlüsseln, finden Sie der [Dokumentation zu durch API ausgelösten Kampagnen](https://developer.adobe.com/journey-optimizer-apis/references/messaging/).

+++

+++Was passiert, wenn mein API-Aufruf fehlschlägt?

Implementieren Sie eine Wiederholungslogik mit exponentiellem Backoff. Überprüfen Sie die API-Antwort auf Fehler-Codes und Meldungen, um Probleme zu diagnostizieren. Häufige Fehler sind ungültige Kampagnen-IDs, falsch formatierte Payloads oder Authentifizierungsprobleme.

+++

+++Kann ich Live-Aktivitäts-Updates von meinen eigenen Backend-Servern senden?

Ja, das ist das beabsichtigte Verhalten. Ihr Backend ruft die Adobe Journey Optimizer Headless-API auf, um Trigger-Live-Aktivitätsereignisse zu senden, wenn Ihre Geschäftslogik dies erfordert.

+++

+++Benötige ich eine andere Kampagne für Start-, Aktualisierungs- und Endereignisse?

Nein. Sie können dieselbe Kampagne verwenden und das Feld `event` in der Payload ändern. Einige Organisationen bevorzugen jedoch separate Kampagnen, um das Analyse-Tracking zu verbessern.

+++

### Fragen zur Fehlerbehebung

+++Meine Live-Aktivität beginnt, wird aber nicht aktualisiert. Was könnte das Problem sein?

Häufige Ursachen:

* `liveActivityID` oder `channelID` von Start- und Auktualisierungsaufrufen stimmen nicht überein.
* `content-state`-Felder stimmen nicht mit Ihrer `ContentState`-Struktur überein.
* Die Live-Aktivität wurde bereits beendet.
* Probleme mit der Netzwerkverbindung auf dem Gerät.
* Die als Zeitstempel verwendete Epochenzeit ist nicht aktuell.

+++

+++Das Feld `attributes-type` wird nicht erkannt. Was soll ich überprüfen?

* Stellen Sie sicher, dass der Klassenname **exakt** (unter Berücksichtigung der Groß-/Kleinschreibung) Ihrem Swift-Strukturnamen entspricht
* Überprüfen Sie, ob die Struktur ordnungsgemäß definiert und registriert ist
* Überprüfen Sie die JSON-Payload auf Tippfehler
* Vergewissern Sie sich, dass die installierte App-Version über die Implementierung der Live-Aktivität verfügt

+++

+++Benutzende sehen nur die Live-Aktivitäts-Aktualisierung und nicht die Warnmeldung. Ist dieses Problem bekannt?

Nein. Das Feld `alert` ist optional und kann unter bestimmten Bedingungen von iOS unterdrückt werden, z. B. im Modus „Nicht stören“. Live-Aktivitäten können im Hintergrund aktualisiert werden, was häufig das beabsichtigte Verhalten ist. Das Feld für Warnhinweise ist obligatorisch für das Senden von Remote-Starts, andernfalls behandelt Apple es wie eine stille Hintergrundbenachrichtigung.

+++

+++Kann ich alle Live-Aktivitätsinstanzen für einen Benutzer löschen oder löschen?

Sie müssen für jede aktive Live-Aktivitätsinstanz ein „Ende“-Ereignis senden. Verfolgen Sie, welche Live-Aktivitätsinstanzen für jede Benutzerin und jeden Benutzer in Ihren Systemen aktiv sind, damit Sie sie ordnungsgemäß bereinigen können.

+++

+++Mein Widget zeigt „Keine Daten“ an, obwohl ich eine Aktualisierung gesendet habe. Was könnte das Problem sein?

* Überprüfen Sie, ob Ihre Widget-Implementierung ordnungsgemäß auf `context.state` und `context.attributes` zugreifen kann.
* Vergewissern Sie sich, dass in Ihrer Widget-Oberfläche Standardwerte oder Fehlerstatus verarbeitet werden.
* Verwenden Sie das Protokoll `LiveActivityAssuranceDebuggable`, um das Schema zu debuggen.
* Testen Sie mit Adobe Assurance, ob Daten empfangen werden.
+++
