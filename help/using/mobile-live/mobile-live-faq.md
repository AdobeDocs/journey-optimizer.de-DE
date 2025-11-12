---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zur Live-Aktivität
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '1603'
ht-degree: 1%

---

# Häufig gestellte Fragen {#mobile-live-faq}

>[!BEGINSHADEBOX]

* [Erste Schritte mit Live-Aktivitäten](get-started-mobile-live.md)
* [Konfiguration der Live-Aktivität](mobile-live-configuration.md)
* [Live-Aktivitätsintegration mit Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* [Erstellen einer Live-Aktivität](create-mobile-live.md)
* **[Häufig gestellte Fragen](mobile-live-faq.md)**
* [Live-Kampagnenbericht](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

## Allgemeine Fragen

+++Was ist der Unterschied zwischen einer Live-Aktivität und einer Push-Benachrichtigung?

Live-Aktivitäten bieten dauerhafte Echtzeit-Aktualisierungen auf dem Sperrbildschirm und auf Dynamic Island, ohne dass Benutzer ihr Gerät entsperren müssen. Push-Benachrichtigungen sind temporäre Warnhinweise, die nach dem Verwerfen ausgeblendet werden. Live-Aktivitäten bleiben sichtbar und können mehrmals aktualisiert werden, bis sie explizit beendet werden.

+++

+++Wie viele Live-Aktivitäten können gleichzeitig aktiv sein?

Eine iOS-App kann mehrere Live-Aktivitäten gleichzeitig ausführen, darunter mehrere, die denselben `ActivityAttributes` verwenden.

Es gibt keine feste Grenze, die von Entwicklern dafür vorgegeben wird, wie viele Live-Aktivitäten eines bestimmten Attributtyps vorhanden sein können. Sie können so viele Abfragen starten, wie Ihre App-Logik erfordert, z. B. einen pro laufendem Versand oder Fahrt. IOS erzwingt jedoch eine Begrenzung auf Systemebene, wie viele Live-Aktivitäten gleichzeitig aktiv oder sichtbar sein können.

In der Praxis:

* iOS unterstützt in der Regel bis zu fünf gleichzeitige Live-Aktivitäten pro App.

* Wenn Sie diese Zahl überschreiten, zeigt das System möglicherweise nicht mehr einige Aktivitäten an oder beendet ältere, um Ressourcen zu sparen.

* Jede Live-Aktivität verfügt über eine eindeutige `Activity.id`, mit der Sie sie einzeln aktualisieren oder beenden können.

+++

+++Müssen Benutzer die App öffnen, um Live-Aktivitäts-Updates zu erhalten?

Nein. Live-Aktivitäten können remote gestartet, aktualisiert und beendet werden, auch wenn die App vollständig geschlossen ist. Dies ist einer der wichtigsten Vorteile der Funktion.

+++

+++Welche iOS-Versionen unterstützen Live-Aktivitäten?

* iOS 16.1+: Grundlegende Unterstützung für Live-Aktivitäten
* iOS 17.2+: Push-to-Start-Funktion (Remote-Start, ohne das Programm zu öffnen)
* iOS 18+: Unterstützung von Broadcast-Kanälen für zielgruppenbasierte Live-Aktivitäten
+++

+++Wie lange kann eine Live-Aktivität aktiv bleiben?

Apple beschränkt die Live-Aktivitäten auf **8 Stunden aktive Updates**. Danach beendet das System die Aktivität automatisch, kann aber bis zu 12 weitere **in einem statischen Zustand sichtbar bleiben** bevor sie entfernt wird. Sie können eine Live-Aktivität auch früher beenden, indem Sie eine `dismissalDate` festlegen oder `activity.end()` explizit in Ihrer App aufrufen.

+++

### Fragen an Entwickler

+++Muss ich eine separate Widget-Erweiterung für Live-Aktivitäten erstellen?

Ja. Live-Aktivitäten werden über WidgetKit angezeigt. Daher müssen Sie eine Widget-Erweiterung in Ihrem Xcode-Projekt erstellen und die `ActivityConfiguration` implementieren.
[Weitere Informationen zur Widget-Konfiguration](mobile-live-configuration-sdk.md)

+++

+++Kann ich dieselbe `LiveActivityAttributes` für lokale und Remote-Live-Aktivitäten verwenden?

Ja. Dieselbe Attributklasse funktioniert sowohl für lokal gestartete als auch für remote gestartete (Push-to-Start) Live-Aktivitäten. Sie müssen sicherstellen, dass Sie es bei `Messaging.registerLiveActivity()` registrieren.

+++

+++Was passiert, wenn ich eine Aktualisierung für eine Live-Aktivität sende, die nicht existiert?

Wenn Sie ein Update- oder End-Ereignis für ein nicht vorhandenes `liveActivityID` oder `channelID` senden, schlägt die Anfrage auf dem Gerät im Hintergrund fehl. Vergewissern Sie sich immer, dass Sie verfolgen, welche Live-Aktivitäten für jeden Benutzer aktiv sind.

+++

+++Kann ich Live-Aktivitäten im iOS-Simulator testen?

Ja, Sie können im iOS-Simulator sowohl lokal gestartete als auch remote gestartete Live-Aktivitäten testen.

* **Lokal**: Dazu gehört das Erstellen, Aktualisieren und Beenden von Live-Aktivitäten direkt in Ihrer App mithilfe von **ActivityKit-APIs**.

* **Remote**: Um die Live-Aktivitätsfunktion remote zu testen, integrieren Sie unsere Messaging-SDK in Ihre App und verwenden Sie die bereitgestellten Ausführungs-APIs, um Remote-Start, -Update und -Ende an Ihr Testgerät oder Ihren iOS-Simulator zu senden. Ähnlich wie Push-Benachrichtigungen derzeit mit der Adobe SDK-Integration getestet werden können.

+++

+++Wie gehe ich mit Aktualisierungen um, wenn sich die App im Hintergrund befindet?

Die SDK übernimmt dies automatisch. Nach der Registrierung erhalten Live-Aktivitäten Aktualisierungen, selbst wenn die App beendet wird. Es sind keine zusätzlichen Hintergrundmodi erforderlich.
+++

+++Was ist der Unterschied zwischen `liveActivityID` und `channelID`?

* `liveActivityID`: Wird für einzelne (unitäre) Live-Aktivitäten verwendet, die auf bestimmte Benutzende abzielen. Jede ID stellt eine eindeutige Live-Aktivitätsinstanz dar.
* `channelID`: Wird für die Übertragung von Live-Aktivitäten verwendet, die an Zielgruppen gesendet werden. Alle Benutzenden in der Zielgruppe erhalten dieselben Updates über denselben Kanal.
+++

+++Kann ich das Erscheinungsbild von Dynamic Island separat vom Sperrbildschirm anpassen?

Ja. Das `ActivityConfiguration` verfügt über separate Verschlüsse für Lock Screen-Inhalte und Dynamic Island-Inhalte (erweiterte, kompakte und minimale Zustände), die jeweils unabhängig voneinander gestaltet werden.
+++

+++Muss ich Push-Token manuell speichern?

Nein. Wenn Sie einen Live-Aktivitätstyp bei `Messaging.registerLiveActivity()` registrieren, erfasst und verwaltet die SDK automatisch Push-Token für Sie.
+++

### Fragen von Marketingexperten

+++Kann ich den Inhalt der Live-Aktivität für jeden Benutzer in einer Broadcast-Kampagne personalisieren?

Broadcast-Kampagnen senden dieselben Inhalte an alle Benutzenden in der Audience. Verwenden Sie für personalisierte Inhalte einheitliche (Transaktions-)Kampagnen, die auf einzelne Benutzer abzielen.
+++

+++Woher weiß ich, ob meine Live-Aktivität erfolgreich bereitgestellt wurde?

[Überwachen Sie Ihre Campaign-](../reports/campaign-global-report-cja-activity.md) in Adobe Journey Optimizer. Sie können Versandraten, Fehler und Interaktionsmetriken verfolgen. Erwägen Sie auch, benutzerdefinierte Analyseereignisse in Ihrer App zu implementieren.
+++

+++Kann ich Live-Aktivitäten im Voraus planen?

Durch den API-Aufruf wird die Live-Aktivität sofort Trigger. Sie können Ihre API-Aufrufe jedoch über Ihre Backend-Systeme planen oder die Orchestrierungsfunktionen von Journey Optimizer verwenden, um sie angemessen zu zeitlich zu planen.
+++

+++Was passiert, wenn ich ein „Start“-Ereignis für eine bereits vorhandene Live-Aktivität sende?

Beim Remote-Start von Live-Aktivitäten über die Ausführungs-APIs von Adobe:

* Sie können der Anfrage einen `x-request-id`-Header hinzufügen. Idealerweise sollte eine Eins-zu-eins-Beziehung zwischen jedem `liveActivityID` und den entsprechenden `x-request-id` bestehen. Dadurch wird sichergestellt, dass bei mehreren Anfragen mit derselben `x-request-id` und `liveActivityID` Kombination nur eine Live-Aktivität auf dem Gerät gestartet und doppelte Anfragen ignoriert werden.

* Wenn der `x-request-id`-Header ausgelassen wird, wird jede Anfrage unabhängig behandelt, was dazu führen kann, dass mehrere Live-Aktivitäten mit demselben `liveActivityID` erstellt werden. In solchen Fällen können zukünftige Aktualisierungen fehlschlagen oder nur für eine der aktiven Instanzen gelten.

* Der `x-request-id` sollte nicht über verschiedene `liveActivityIDs` hinweg in separaten API-Anfragen wiederverwendet werden.

+++

+++Kann ich verschiedene Live-Aktivitätserlebnisse in A/B-Tests testen?

Ja. Erstellen Sie mehrere Kampagnen mit unterschiedlichen Inhaltsstrukturen und verwenden Sie die Experimentierfunktionen von Adobe Journey Optimizer, um zu testen, welche besser funktioniert. Stellen Sie sicher, dass Ihre App alle Inhaltsstatusvarianten unterstützt.

+++

+++Wie oft sollte ich eine Live-Aktivität aktualisieren?

Nur aktualisieren, wenn sich wichtige Informationen ändern, da zu häufige Aktualisierungen den Akku entladen und die Benutzererlebnisqualität beeinträchtigen können. In Echtzeit-Szenarien, wie z. B. dem Versand-Tracking, ist in der Regel der Abstand von 30 bis 60 Sekunden akzeptabel. Bei sich langsamer ändernden Inhalten, wie z. B. Sportbewertungen, werden nur Aktualisierungen zu wichtigen Ereignissen vorgenommen.

+++

+++Kann ich Benutzende darauf ansprechen, ob sie Live-Aktivitäten aktiviert haben?

Sie müssen mit Ihrem Entwicklungs-Team zusammenarbeiten, um diese Voreinstellung zu verfolgen und als Benutzerattribut an Adobe Experience Platform zu übergeben und dann basierend auf diesem Attribut zu segmentieren.

+++

### API-Fragen

+++Was ist der Unterschied zwischen `timestamp` und `dismissal-date`?

* `timestamp`: Die aktuelle Epochenzeit, zu der das Ereignis auftritt. Wird für alle Ereignisse benötigt.
* `dismissal-date`: Ein zukünftiger Zeitraum, in dem die Live-Aktivität automatisch beendet werden soll. Dies ist nur für „Ende“-Ereignisse erforderlich.

+++

+++Muss ich bei jedem Aktualisierungsaufruf alle `attributes` Felder senden?

Ja, basierend auf Ihrer `LiveActivityAttribute`.

* Alle Felder aus Ihrem Attributobjekt, einschließlich `liveActivityData`, sollten in jedem Aufruf enthalten sein, zum Start, für Aktualisierungen oder für das Ende.
* Nur die `content-state` stellen dar, was sich tatsächlich dynamisch bei einer laufenden Live-Aktivität ändert.
* Schließen Sie auch ein Benachrichtigungsobjekt ein. Dadurch wird sichergestellt, dass die Push-Benachrichtigung als für den Benutzer sichtbare Benachrichtigung und nicht als stille Hintergrundbenachrichtigung behandelt wird. Nur für „start“-Fälle erforderlich, ansonsten optional.

+++

+++In welchem Format sollten Epochenzeitstempel vorliegen?

Unix-Epochenzeit in **Sekunden** statt Millisekunden verwenden. Beispiel: `1759937682`

+++

+++Kann ich dieselbe `requestId` für mehrere API-Aufrufe verwenden?

Nein. Jede API-Anfrage sollte über eine eindeutige `requestId` verfügen, um die Idempotenz und ein ordnungsgemäßes Tracking sicherzustellen. Verwenden Sie UUIDs oder ähnliche eindeutige Kennungen.

+++

+++Welche Authentifizierung ist für die Headless-API erforderlich?

Authentifizierungspflichten, einschließlich OAuth[Token und API-Schlüsseln, finden Sie ](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) der Dokumentation zu API-ausgelösten Kampagnen .

+++

+++Was passiert, wenn mein API-Aufruf fehlschlägt?

Implementieren Sie eine Wiederholungslogik mit exponentiellem Backoff. Überprüfen Sie die API-Antwort auf Fehler-Codes und Meldungen, um Probleme zu diagnostizieren. Häufige Fehler sind ungültige Kampagnen-IDs, falsch formatierte Payloads oder Authentifizierungsprobleme.

+++

+++Kann ich Live-Aktivitäts-Updates von meinen eigenen Backend-Servern senden?

Ja, das ist das beabsichtigte Verhalten. Ihr Backend ruft die Adobe Journey Optimizer Headless-API auf, um Trigger-Live-Aktivitätsereignisse zu senden, wenn Ihre Geschäftslogik dies erfordert.

+++

+++Benötige ich eine andere Kampagne für Start-, Update- und End-Ereignisse?

Nein. Sie können dieselbe Kampagne verwenden und das Feld `event` in der Payload ändern. Einige Organisationen bevorzugen jedoch separate Kampagnen, um das Analytics-Tracking zu verbessern.

+++

### Fragen zur Fehlerbehebung

+++Meine Live-Aktivität beginnt, wird aber nicht aktualisiert. Was könnte das Problem sein?

Häufige Ursachen:

* `liveActivityID` oder `channelID` zwischen Start- und Update-Aufrufen stimmen nicht überein.
* `content-state` Felder stimmen nicht mit Ihrer `ContentState` überein.
* Die Live-Aktivität wurde bereits beendet.
* Probleme mit der Netzwerkverbindung auf dem Gerät.

+++

+++Das `attributes-type` Feld wird nicht erkannt. Was soll ich überprüfen?

* Stellen Sie sicher, dass der Klassenname **exakt)** Ihrem Swift-Strukturnamen (unter Berücksichtigung der Groß-/Kleinschreibung) entspricht
* Überprüfen, ob die Struktur ordnungsgemäß definiert und registriert ist
* Überprüfen der JSON-Payload auf Tippfehler
* Vergewissern Sie sich, dass die installierte App-Version die Live Activity-Implementierung aufweist

+++

+++Benutzende sehen nur die Live-Aktivitäts-Aktualisierung und nicht die Warnmeldung. Ist dieses Problem bekannt?

Nein. Das Feld `alert` ist optional und kann unter bestimmten Bedingungen von iOS unterdrückt werden, z. B. im Modus „Nicht stören“. Live-Aktivitäten können im Hintergrund aktualisiert werden, was häufig das beabsichtigte Verhalten ist. Das Feld Warnhinweis ist obligatorisch für das Senden von Remote-Starts, andernfalls behandelt Apple es wie eine stille Hintergrundbenachrichtigung.

+++

+++Kann ich alle Live-Aktivitäten eines Benutzers löschen oder löschen?

Sie müssen für jede aktive Live-Aktivität ein „Ende“-Ereignis senden. Verfolgen Sie, welche Live-Aktivitäten für jeden Benutzer in Ihren Systemen aktiv sind, damit Sie ihn ordnungsgemäß bereinigen können.

+++

+++Mein Widget zeigt „Keine Daten“ an, obwohl ich eine Aktualisierung gesendet habe. Was könnte das Problem sein?

* Überprüfen Sie, ob Ihre Widget-Implementierung ordnungsgemäß auf `context.state` und `context.attributes` zugreift.
* Vergewissern Sie sich, dass in Ihrer Widget-Oberfläche Standardwerte oder Fehlerzustände verarbeitet werden.
* Verwenden Sie das `LiveActivityAssuranceDebuggable` Protokoll, um das Schema zu debuggen.
* Testen Sie mit Adobe Assurance, um festzustellen, ob Daten empfangen werden.
+++
