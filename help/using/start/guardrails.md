---
solution: Journey Optimizer
product: journey optimizer
title: Leitplanken und Einschränkungen von Journey Optimizer
description: Weitere Informationen zu Leitplanken bei Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 0d010bbb46887546d524726606764b564c352064
workflow-type: tm+mt
source-wordcount: '1960'
ht-degree: 89%

---

# Leitlinien und Einschränkungen {#limitations}

Berechtigungen, Produkteinschränkungen und die Performance betreffende Leitplanken sind auf der Seite [Adobe Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} aufgeführt.

Beachten Sie auch die [Leitplanken für Echtzeit-Kundenprofildaten](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=de){target="_blank"}, bevor Sie beginnen.

Unten finden Sie zusätzliche Leitlinien und Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer].

## Unterstützte Browser {#browsers}

Die Benutzeroberfläche von Adobe [!DNL Journey Optimizer] wurde für eine optimale Funktionsweise in der neuesten Version von Google Chrome entwickelt. Bei der Verwendung bestimmter Funktionen in älteren Versionen oder anderen Browsern können Probleme auftreten.

## Schutzmaßnahmen bei Nachrichten {#message-guardrails}

* Mit [!DNL Journey Optimizer] können Sie keine Anhänge zu einer E-Mail hinzufügen.
* Sie können dieselbe Versand-Domain nicht zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und einem anderen Produkt verwenden, beispielsweise [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage].


## Schutzmaßnahmen bei Landingpages {#lp-guardrails}

* Es kann nur eine einzige **Formular**-Komponente auf einer einzelnen primären Seite verwendet werden.
* Die **Formular**-Komponente kann nicht in Unterseiten verwendet werden.
* Sie können keine Preheader zu einer Landingpage hinzufügen.
* Sie können die Option **Eigene Codierung** nicht auswählen, wenn Sie eine primäre Landingpage entwerfen.

## SMS-Leitlinien {#sms-guardrails}

* Die MMS-Funktion ist nur für Sinch verfügbar.
* Mediendateien für MMS können über eine unterstützte URL eingeschlossen werden. Bitte stellen Sie sicher, dass die Mediendatei separat hochgeladen wird.
* Die Synchronisierung von Nachrichten-Feedback ist derzeit nicht für MMS verfügbar.
* Die Einverständnisverwaltung erfolgt auf SMS-Kanalebene für MMS.

## Fragmentleitlinien {#fragments-guardrails}

* Visuelle Fragmente sind nur für den E-Mail-Kanal verfügbar.
* Ausdrucksfragmente sind nicht für den Web- und den In-App-Kanal verfügbar.

## Leitlinien für Journeys {#journeys-guardrails}

### Allgemeine Limits für Journey {#journeys-guardrails-journeys}

* Die Anzahl der Aktivitäten in einer Journey ist auf maximal 50 begrenzt. Die Anzahl der Aktivitäten wird im oberen linken Bereich der Journey-Arbeitsfläche angezeigt. Dies unterstützt Lesbarkeit, Qualitätssicherung und Fehlerbehebung.
* Während Sie Journeys veröffentlichen, skalieren und passen wir sie automatisch an, um maximalen Durchsatz und maximale Stabilität zu gewährleisten. Wenn Sie den Meilenstein von 100 Live-Journeys gleichzeitig erreichen, wird in der UI eine Benachrichtigung zu dieser Leistung angezeigt. Wenn Sie diese Benachrichtigung sehen, aber die Notwendigkeit besteht, Ihre Journey über 100 Live-Journeys hinaus zu erweitern, erstellen Sie bitte ein Ticket für die Kundenunterstützung, und wir helfen Ihnen bei der Erreichung Ihrer Ziele.
* Bei Verwendung einer Zielgruppenqualifizierung in einer Journey kann es bis zu 10 Minuten dauern, bis die Aktivität aktiv ist und die Profile überwacht, die in die Zielgruppe eintreten oder sie verlassen.
* Eine Journey-Instanz für ein Profil hat eine Maximalgröße von 1 MB. Alle Daten, die im Rahmen der Journey-Ausführung gesammelt wurden, werden in dieser Journey-Instanz gespeichert. Daher sind Daten aus einem eingehenden Ereignis, aus Adobe Experience Platform abgerufene Profilinformationen, benutzerdefinierte Aktionsantworten usw. werden in dieser Journey-Instanz gespeichert und wirken sich auf die Journey-Größe aus. Es wird empfohlen, die maximale Größe dieser Ereignis-Payload zu begrenzen, wenn eine Journey mit einem Ereignis beginnt (z. B. unter 800 KB), um zu verhindern, dass diese Grenze nach einigen Aktivitäten bei der Ausführung der Journey erreicht wird. Wenn diese Grenze erreicht ist, befindet sich das Profil im Fehlerstatus und wird von der Journey ausgeschlossen.


### Allgemeine Aktionen {#general-actions-g}

* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung einstellen. Mit Ausnahme von HTTP 401, 403 und 404 werden weitere Zustellversuche für alle HTTP-Fehler durchgeführt.
* Mit dem integrierten Ereignis **Reaktion** können Sie auf vorkonfigurierte Aktionen reagieren. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/reaction-events.md). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wurde, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.
* Ein Profil kann nicht mehrmals zur gleichen Zeit in derselben Journey vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](../building-journeys/end-journey.md)

### Journey-Versionen {#journey-versions-g}

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einem **Zielgruppen-Qualifizierungsereignis** beginnen.
* Eine Journey, die in Version 1 mit einer Aktivität vom Typ **Zielgruppen-Qualifizierung** beginnt, muss in weiteren Versionen immer mit einer **Zielgruppen-Qualifizierung** beginnen.
* Die Zielgruppe und der Namespace, die unter **Zielgruppen-Qualifizierung** (dem ersten Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit **Zielgruppe lesen** beginnt, kann in Folgeversionen nicht mit einem anderen Ereignis beginnen.
* Sie können keine neue Version einer „Zielgruppe lesen“-Journey mit inkrementellem Lesen erstellen. Sie müssen die Journey duplizieren.

### Benutzerdefinierte Aktionen {#custom-actions-g}

* Für alle benutzerdefinierten Aktionen ist ein Begrenzung von 300.000 Aufrufen innerhalb von einer Minute pro Host und Sandbox festgelegt. Mehr dazu erfahren Sie auf [dieser Seite](../action/about-custom-action-configuration.md). Diese Beschränkung wurde auf der Grundlage der Kundennutzung festgelegt, um externe Endpunkte zu schützen, die von benutzerdefinierten Aktionen angesprochen werden. Sie müssen dies in Ihren zielgruppenbasierten Journeys berücksichtigen, indem Sie eine geeignete Leserate definieren (5000 Profile pro Sekunde, wenn benutzerdefinierte Aktionen verwendet werden). Bei Bedarf können Sie diese Einstellung überschreiben, indem Sie über unsere Begrenzungs- oder Drosselungs-API eine höhere Begrenzung oder Einschränkung definieren. Weitere Informationen finden Sie auf [dieser Seite](../configuration/external-systems.md).
* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter.
* Es werden die Aufrufmethoden POST, PUT und GET unterstützt
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit „.“ oder „$“ beginnen.
* IP-Adressen sind nicht zulässig
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.
* Integrierte benutzerdefinierte Aktionen können nicht entfernt werden.
* Stellen Sie bei der Auswahl eines Endpunkts für das Targeting mithilfe einer benutzerdefinierten Aktion sicher, dass:

   * Dieser Endpunkt kann mithilfe von Konfigurationen aus dem Journey-Durchsatz unterstützen. [Einschränkungs-API](../configuration/throttling.md) oder [Capping-API](../configuration/capping.md) , um sie zu begrenzen. Seien Sie vorsichtig, wenn eine Einschränkungskonfiguration nicht unter 200 TPS liegen darf. Jeder Zielpunkt muss mindestens 200 TPS unterstützen.
   * Dieser Endpunkt muss eine so niedrige Antwortzeit wie möglich haben. Abhängig von Ihrem erwarteten Durchsatz kann sich eine hohe Reaktionszeit auf den tatsächlichen Durchsatz auswirken.

### Ereignisse {#events-g}

* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zum Starten einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
* Geschäftsereignisse können nicht zusammen mit unitären Ereignissen oder Zielgruppen-Qualifizierungaktivitäten verwendet werden.
* Unitäre Journeys (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung) enthalten einen Schutzmechanismus, der verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.
* Journey Optimizer erfordert, dass Ereignisse an den Data Collection Core Service (DCCS) gestreamt werden, damit eine Journey ausgelöst werden kann. Ereignisse, die in Batches aufgenommen werden, oder Ereignissen aus internen Journey Optimizer-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking usw.) können nicht zum Auslösen einer Journey verwendet werden. Für Anwendungsfälle, bei denen Sie keine Streaming-Ereignisse empfangen können, erstellen Sie stattdessen eine auf diesen Ereignissen basierende Zielgruppe und verwenden Sie die Aktivität **Zielgruppe lesen**. Die Zielgruppen-Qualifizierung kann zwar theoretisch verwendet werden, kann aber im späteren Verlauf abhängig von den verwendeten Aktionen zu Problemen führen.

### Datenquellen {#data-sources-g}

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.

>[!NOTE]
>
>Da die Antworten jetzt unterstützt werden, sollten Sie für Anwendungsfälle aus externen Datenquellen benutzerdefinierte Aktionen anstelle von Datenquellen verwenden.

### Journeys und Profilerstellung {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

### Zielgruppe lesen {#read-segment-g}

* Streaming-Zielgruppen sind immer auf dem neuesten Stand, Batch-Zielgruppen werden jedoch zum Zeitpunkt des Abrufs nicht berechnet. Sie werden nur jeden Tag zum Zeitpunkt der täglichen Batch-Auswertung berechnet.
* Bei Journeys, die eine Aktivität vom Typ „Zielgruppe lesen“ verwenden, gibt es eine maximale Anzahl von Journeys, die exakt zur gleichen Zeit beginnen können. Es werden zwar weitere Wiederholungsversuche vom System durchgeführt, Sie sollten jedoch vermeiden, dass mehr als fünf Journeys (mit „Zielgruppe lesen“, geplant oder „so bald wie möglich“) exakt zur gleichen Zeit beginnen, indem Sie sie über einen bestimmten Zeitraum verteilen, z. B. mit 5 bis 10 Minuten Abstand.

### Ausdruckseditor {#expression-editor}

* Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einer Aktivität vom Typ „Zielgruppe lesen“, „Zielgruppen-Qualifizierung“ oder „Geschäftsereignis“ beginnen. Sie müssen eine neue Zielgruppe erstellen und eine inaudience-Bedingung in der Journey verwenden.


### Einschränkungen bei In-App-Aktivitäten {#in-app-activity-limitations}

* Diese Funktion ist derzeit nicht für Kundinnen und Kunden im Gesundheitswesen verfügbar.

* Personalisierung kann nur Profilattribute enthalten.

* Die In-App-Anzeige ist an die Journey-Lebensdauer gebunden, d. h. wenn die Journey für ein Profil endet, werden alle In-App-Nachrichten innerhalb dieser Journey nicht mehr für dieses Profil angezeigt.  Daher ist es nicht möglich, eine In-App-Nachricht direkt von einer Journey-Aktivität aus zu stoppen. Stattdessen müssen Sie die gesamte Journey beenden, um zu verhindern, dass die In-App-Nachrichten dem Profil angezeigt werden.

* Im Testmodus hängt die In-App-Anzeige von der Journey-Lebensdauer ab. Um zu verhindern, dass die Journey während des Tests zu früh endet, passen Sie den **[!UICONTROL Wartezeit]**-Wert für Ihre **[!UICONTROL Warten]**-Aktivitäten an.

* **[!UICONTROL Reaktion]**-Aktivitäten können nicht verwendet werden, um auf ein Öffnen oder Klicken in der App zu reagieren.

* Es kann eine Aktivierungsverzögerung zwischen dem Zeitpunkt auftreten, zu dem ein Benutzerprofil eine In-App-Aktivität auf der Arbeitsfläche erreicht, und dem Zeitpunkt, zu dem es diese In-App-Nachricht zu sehen beginnt.

* Die Inhaltsgröße von In-App-Nachrichten ist auf 2 MB beschränkt. Das Einschließen großer Bilder kann den Veröffentlichungsprozess behindern.

## Leitlinien für Zielgruppen {#audience}

* Sie können bis zu 10 Zielgruppenkompositionen in einer Sandbox veröffentlichen. Wenn Sie diesen Schwellenwert erreicht haben, müssen Sie eine Komposition löschen, um Speicherplatz freizumachen, und eine neue veröffentlichen.

## Leitlinien beim Entscheidungs-Management {#decision-management}

### Performance-Garantien {#performance-guardrails}

Der Versanddurchsatz entspricht der Anzahl der Entscheidungsantworten, die vom Entscheidungs-Management-App-Dienst innerhalb einer bestimmten Zeit bereitgestellt werden können. Die Anzahl der Entscheidungen pro Sekunde ist in der nachstehenden Tabelle aufgeführt.

| API | Entscheidungen pro Sekunde |
|---------|----------|
| Decisioning-API-Anfragen | 500 pro Sekunde |
| Edge Decisioning-API-Anfragen | 5.000 pro Sekunde |

### Einschränkungen {#offers-limitations}

Die Einschränkungen des Entscheidungs-Managements sind unten aufgeführt.

* **Genehmigte personalisierte Angebote + Fallback-Angebote** – Bis zu 10.000 kombinierte genehmigte personalisierte Angebote und genehmigte Fallback-Angebote.
* **Entscheidungen** – bis zu 10.000 Entscheidungen.
* **Live-Entscheidungen** – Der Offer Decisioning App-Dienst unterstützt bis zu 1.000 Live-Entscheidungen.
* **Angebote, die pro Antwort zurückgegeben werden** – Offer Decisioning unterstützt bis zu 100 Angebote, die pro Anfrage über alle Entscheidungsbereiche in der Anfrage zurückgegeben werden.
* **Sammlungen** – Bis zu 10.000 Sammlungen.
* **Sammlungen pro Entscheidung** – Bis zu 30 Sammlungen pro Entscheidung.
* **Entscheidungsregeln + Rangfolgefunktionen** – Bis zu 10.000 kombinierte Entscheidungsregeln und Rangfolgefunktionen.
* **Platzierungen** – Bis zu 1.000 Platzierungen.
* **Platzierungen pro Entscheidung** – Bis zu 30 Platzierungen pro Entscheidung.
* **Rangfolgemethode pro Entscheidung** – Der Offer Decisioning App-Dienst unterstützt bis zu 30 Rangfolgefunktionen pro Entscheidung.
* **KI-Rangfolgemodell** – Der Offer Decisioning App-Dienst unterstützt bis zu 5 KI-Rangfolgemodelle.
* **Sammlungsqualifikatoren pro Angebot oder Sammlung** – Der Offer Decisioning App-Dienst unterstützt bis zu 20 Sammlungsqualifikatoren in jedem einzelnen personalisierten Angebot oder jeder einzelnen Sammlung.
* **Gesamtanzahl der Sammlungsqualifikatoren** – Der Offer Decisioning App-Dienst unterstützt bis zu 1.000 Sammlungsqualifikatoren.