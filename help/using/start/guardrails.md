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
source-git-commit: 284c4896b923eac1d360b61d97cbe560d747ea4f
workflow-type: tm+mt
source-wordcount: '2513'
ht-degree: 99%

---

# Schutzmechanismen und Einschränkungen {#limitations}

Unten finden Sie zusätzliche Leitlinien und Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer].

Berechtigungen, Produkteinschränkungen und Performance-Leitlinien sind auf der Seite [Adobe Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} aufgeführt.


>[!CAUTION]
>
>* [Leitlinien für Echtzeit-Kundenprofildaten und Segmentierung](https://experienceleague.adobe.com/de/docs/experience-platform/profile/guardrails){target="_blank"} gelten auch für Adobe Journey Optimizer.
>
>* Siehe auch [Leitplanken für die Datenaufnahme im Echtzeit-Kundenprofil](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/guardrails){target="_blank"}


## Unterstützte Browser {#browsers}

Die Benutzeroberfläche von Adobe [!DNL Journey Optimizer] wurde für eine optimale Funktionsweise in der neuesten Version von Google Chrome entwickelt. Bei der Verwendung bestimmter Funktionen in älteren Versionen oder anderen Browsern können Probleme auftreten.

## Leitlinien für Datensätze {#datasets-guardrails}

Ab Februar 2025 werden in **neuen Sandboxes und neuen Organisationen** für systemgenerierte Journey Optimizer-Datensätze als Schutzmechanismen die folgenden Limits für die Time-to-Live (TTL) eingeführt:

* 90 Tage für Daten im Profilspeicher,
* 13 Monate für Daten im Data Lake.

Diese Änderung wird in einer nachfolgenden Phase in **bestehende Kunden-Sandboxes** integriert. [Weitere Informationen zu Limits für die Time-to-Live (TTL) als Schutzmechanismen für Datensätze](../data/datasets-ttl.md)

## Schutzmechanismen für Kanäle {#channel-guardrails}

>[!NOTE]
>
>In seltenen Fällen können temporäre Ausfälle in einer bestimmten Region dazu führen, dass gültige Profile von Journeys ausgeschlossen werden oder dass E-Mails fälschlicherweise als Bounces markiert werden. Sobald die Services wiederhergestellt sind, überprüfen Sie die Journey-Protokolle erneut, verifizieren Sie die Einverständnisprofilfelder und veröffentlichen Sie die Journey bei Bedarf erneut. [In diesem Abschnitt](../configuration/manage-suppression-list.md#remove-from-suppression-list) erfahren Sie, wie Sie im Falle eines ISP-Ausfalls Profile aus der Unterdrückungsliste entfernen.
>

### Schutzmechanismen für E-Mails {#message-guardrails}

Für den [E-Mail-Kanal](../email/get-started-email.md) gelten die folgenden Schutzmechanismen:

* Mit [!DNL Journey Optimizer] können Sie keine Anhänge zu einer E-Mail hinzufügen.
* Sie können dieselbe Versand-Domain nicht zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und einem anderen Produkt verwenden, beispielsweise [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage].

### Leitlinien für SMS {#sms-guardrails}

Für den [SMS-Kanal](../sms/get-started-sms.md) gelten die folgenden Schutzmechanismen:

* Mediendateien für MMS können über eine unterstützte URL eingeschlossen werden. Bitte stellen Sie sicher, dass die Mediendatei separat hochgeladen wird.
* Die Synchronisierung von Nachrichten-Feedback ist derzeit nicht für MMS verfügbar.
* Die Einverständnisverwaltung erfolgt auf SMS-Kanalebene für MMS.

### Leitlinien für Web-Kanäle {#web-guardrails}

[!DNL Journey Optimizer]-[Web-Kampagnen](../web/get-started-web.md) zielen auf neue Profile ab, die zuvor noch nicht auf anderen Kanälen kontaktiert wurden. Dadurch erhöht sich die Gesamtzahl der kontaktierbaren Profile. Dies kann sich auf die Kosten auswirken, wenn die vertragliche Anzahl der von Ihnen erworbenen kontaktierbaren Profile überschritten wird.

Lizenzmetriken für jedes Paket finden Sie auf der Seite [Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

### Leitlinien für Code-basierte Kanäle {#code-based-guardrails}

Um Code-basierte Erlebnisaktionen in [!DNL Journey Optimizer] verwenden und die Payload des Code-Inhalts bereitstellen zu können, die von Ihren Anwendungen verwendet werden kann, müssen Sie die Voraussetzungen auf [dieser Seite](../code-based/code-based-prerequisites.md) erfüllen.

## Schutzmechanismen für Landingpages {#lp-guardrails}

Für [Landingpages](../landing-pages/get-started-lp.md) gelten die folgenden Schutzmechanismen:

* Es kann nur eine einzige **Formular**-Komponente auf einer einzelnen primären Seite verwendet werden.
* Die **Formular**-Komponente kann nicht in Unterseiten verwendet werden.
* Sie können keine Preheader zu einer Landingpage hinzufügen.
* Sie können die Option **Eigene Codierung** nicht auswählen, wenn Sie eine primäre Landingpage entwerfen.

## Leitlinien für Subdomains {#subdomain-guardrails}

Standardmäßig können Sie mit [!DNL Journey Optimizer] insgesamt bis zu 10 Subdomains delegieren (die sowohl E-Mail- als auch Web-Kanäle abdecken).

Abhängig von Ihrem Lizenzvertrag können Sie jedoch bis zu 100 Subdomains delegieren. Wenden Sie sich an Ihre Adobe-Kontaktperson, um die Anzahl der Subdomains zu erfahren, für die Sie berechtigt sind.

Auf [dieser Seite](../configuration/delegate-subdomain.md) erfahren Sie mehr über die Domain-Delegierung.

## Schutzmechanismen für Fragmente {#fragments-guardrails}

Für [Fragmente](../content-management/fragments.md) gelten die folgenden Schutzmechanismen:

* Visuelle Fragmente sind nur für den E-Mail-Kanal verfügbar.
* Ausdrucksfragmente sind nicht für den In-App-Kanal verfügbar.

## Leitlinien für Zielgruppen {#audience}

Sie können bis zu 10 Zielgruppenkompositionen in einer Sandbox veröffentlichen. Wenn Sie diesen Schwellenwert erreicht haben, müssen Sie eine Komposition löschen, um Speicherplatz freizumachen, und eine neue veröffentlichen.

Weitere Informationen zu Zielgruppenkompositionen finden Sie auf [dieser Seite](../audience/get-started-audience-orchestration.md).

## Leitlinien für die Entscheidungsfindung und das Entscheidungs-Management {#decisioning-guardrails}

Leitlinien und Einschränkungen, die Sie bei der Arbeit mit der Entscheidungsfindung oder dem Entscheidungs-Management beachten sollten, werden in den folgenden Abschnitten zur Entscheidungsfindung und dem Entscheidungs-Management beschrieben:

* [Leitlinien und Einschränkungen für die Entscheidungsfindung](../experience-decisioning/decisioning-guardrails.md)
* [Leitlinien und Einschränkungen für das Entscheidungs-Management](../offers/decision-management-guardrails.md)


## Leitlinien für Journeys {#journeys-guardrails}

### Allgemeine Limits für Journey {#journeys-guardrails-journeys}

* Die Anzahl der Aktivitäten in einer Journey ist auf maximal 50 begrenzt. Die Anzahl der Aktivitäten wird im oberen linken Bereich der Journey-Arbeitsfläche angezeigt. Dies unterstützt Lesbarkeit, Qualitätssicherung und Fehlerbehebung.
* Während Sie Journeys veröffentlichen, skalieren und passen wir sie automatisch an, um maximalen Durchsatz und maximale Stabilität zu gewährleisten. Wenn Sie den Meilenstein von 100 Live-Journeys gleichzeitig erreichen, wird in der UI eine Benachrichtigung zu dieser Leistung angezeigt. Wenn Sie diese Benachrichtigung sehen, aber die Notwendigkeit besteht, Ihre Journey über 100 Live-Journeys hinaus zu erweitern, erstellen Sie bitte ein Ticket für die Kundenunterstützung, und wir helfen Ihnen bei der Erreichung Ihrer Ziele.
  <!-- DOCAC-10977 * As you publish journeys, we automatically scale and adjust to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time, you will see a notification appear in the UI on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->
* Bei Verwendung einer Zielgruppenqualifizierung in einer Journey kann es bis zu 10 Minuten dauern, bis die Aktivität aktiv ist und die Profile überwacht, die in die Zielgruppe eintreten oder sie verlassen.
* Eine Journey-Instanz für ein Profil hat eine Maximalgröße von 1 MB. Alle Daten, die im Rahmen der Journey-Ausführung gesammelt wurden, werden in dieser Journey-Instanz gespeichert. Daher werden Daten aus einem eingehenden Ereignis, aus Adobe Experience Platform abgerufene Profilinformationen, benutzerdefinierte Aktionsantworten usw. in dieser Journey-Instanz gespeichert und wirken sich auf die Journey-Größe aus. Es wird empfohlen, die Maximalgröße dieser Ereignis-Payload zu begrenzen, wenn eine Journey mit einem Ereignis beginnt (z. B. weniger als 800 KB), um zu verhindern, dass dieses Limit nach wenigen Aktivitäten bei der Ausführung der Journey erreicht wird. Wenn dieses Limit erreicht ist, befindet sich das Profil im Fehlerstatus und wird von der Journey ausgeschlossen.
* Zusätzlich zu der in den Journey-Aktivitäten verwendeten maximalen Wartezeit gibt es auch eine maximale globale Journey-Wartezeit, die nicht auf der Benutzeroberfläche angezeigt wird und nicht geändert werden kann. Diese maximale globale Wartezeit stoppt den Fortschritt von Kontakten in der Journey 91 Tage nach ihrem Eintritt. [Weitere Informationen](../building-journeys/journey-properties.md#global_timeout)

### Allgemeine Aktionen {#general-actions-g}

Für [Aktionen](../building-journeys/about-journey-activities.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung einstellen. Mit Ausnahme von HTTP 401, 403 und 404 werden weitere Zustellversuche für alle HTTP-Fehler durchgeführt.
* Mit dem integrierten Ereignis **Reaktion** können Sie auf vorkonfigurierte Aktionen reagieren. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/reaction-events.md). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wird, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.
* Ein Profil kann nicht mehrmals zur gleichen Zeit in derselben Journey für alle aktiven [Journey-Versionen](../building-journeys/publishing-the-journey.md#create-a-new-version-of-a-journey-journey-create-new-version) vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](../building-journeys/end-journey.md)

### Journey-Versionen {#journey-versions-g}

Für [Journey-Versionen](../start/user-interface.md) gelten die folgenden Schutzmechanismen:

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einem **Zielgruppen-Qualifizierungsereignis** beginnen.
* Eine Journey, die in Version 1 mit einer Aktivität vom Typ **Zielgruppen-Qualifizierung** beginnt, muss in weiteren Versionen immer mit einer **Zielgruppen-Qualifizierung** beginnen.
* Die Zielgruppe und der Namespace, die unter **Zielgruppen-Qualifizierung** (dem ersten Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit **Zielgruppe lesen** beginnt, kann in Folgeversionen nicht mit einem anderen Ereignis beginnen.
* Sie können keine neue Version einer „Zielgruppe lesen“-Journey mit inkrementellem Lesen erstellen. Sie müssen die Journey duplizieren.

### Benutzerdefinierte Aktionen {#custom-actions-g}

Für [benutzerdefinierte Aktionen](../action/action.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Für alle benutzerdefinierten Aktionen ist ein Begrenzung von 300.000 Aufrufen innerhalb von einer Minute pro Host und Sandbox festgelegt. Mehr dazu erfahren Sie auf [dieser Seite](../action/about-custom-action-configuration.md). Diese Beschränkung wurde auf Grundlage der Kundennutzung festgelegt, um externe Endpunkte zu schützen, die von benutzerdefinierten Aktionen angesprochen werden. Sie müssen dies in Ihren zielgruppenbasierten Journeys berücksichtigen, indem Sie eine geeignete Leserate definieren (5000 Profile pro Sekunde, wenn benutzerdefinierte Aktionen verwendet werden). Bei Bedarf können Sie diese Einstellung überschreiben, indem Sie über unsere Begrenzungs- oder Drosselungs-API eine höhere Begrenzung oder Einschränkung definieren. Weitere Informationen finden Sie auf [dieser Seite](../configuration/external-systems.md).
* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter.
* Es werden die Aufrufmethoden POST, PUT und GET unterstützt
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit „.“ oder „$“ beginnen.
* IP-Adressen sind nicht zulässig
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.
* Integrierte benutzerdefinierte Aktionen können nicht entfernt werden.
* Benutzerdefinierte Aktionen unterstützen das JSON-Format nur bei Verwendung von Anfrage- oder Antwort-Payloads. Weitere Informationen finden Sie auf [dieser Seite](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Stellen Sie bei der Auswahl eines mit einer benutzerdefinierten Aktion anzusprechenden Endpunkts sicher, dass:

   * Dieser Endpunkt den Journey-Durchsatz unterstützen kann, indem er ihn mit Konfigurationen aus der [Drosselungs-API](../configuration/throttling.md) oder [Begrenzungs-API](../configuration/capping.md) begrenzt. Vorsicht: Eine Drosselungskonfiguration darf nicht unter 200 TPS liegen. Jeder angesprochene Endpunkt muss mindestens 200 TPS unterstützen.
   * Dieser Endpunkt muss eine so niedrige Antwortzeit wie möglich haben. Abhängig von Ihrem erwarteten Durchsatz kann sich eine hohe Reaktionszeit auf den tatsächlichen Durchsatz auswirken.

### Ereignisse {#events-g}

Für [Ereignisse](../event/about-events.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Journey Optimizer unterstützt ein Spitzenvolumen von 5.000 eingehenden Journey-Ereignissen pro Sekunde.
* Bei von einem Ereignis ausgelösten Journeys kann es bis zu 5 Minuten dauern, bis die erste Aktion in der Journey verarbeitet wird.
* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zum Starten einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
* Geschäftsereignisse können nicht zusammen mit unitären Ereignissen oder Zielgruppen-Qualifizierungaktivitäten verwendet werden.
* Unitäre Journeys (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung) enthalten einen Schutzmechanismus, der verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profileintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.
* Journey Optimizer erfordert, dass Ereignisse an den Data Collection Core Service (DCCS) gestreamt werden, damit eine Journey ausgelöst werden kann. Über Ereignisse, die in Batches aufgenommen werden, oder Ereignisse aus internen Journey Optimizer-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking usw.) kann eine Journey nicht ausgelöst werden. Für Anwendungsfälle, bei denen Sie keine Streaming-Ereignisse empfangen können, müssen Sie stattdessen eine auf diesen Ereignissen basierende Zielgruppe erstellen und die Aktivität **Zielgruppe lesen** verwenden. Die Zielgruppen-Qualifizierung kann zwar theoretisch verwendet werden, wird jedoch nicht empfohlen, da sie aufgrund der verwendeten Aktionen zu nachgelagerten Problemen führen kann.

### Datenquellen  {#data-sources-g}

Für [Datenquellen](../datasource/about-data-sources.md) in Ihren Journeys gelten die folgenden Schutzmechanismen:

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.

>[!NOTE]
>
>Da die Antworten jetzt unterstützt werden, sollten Sie für Anwendungsfälle mit externen Datenquellen benutzerdefinierte Aktionen anstelle von Datenquellen verwenden.

### Journeys und Profilerstellung {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

### Aktualisieren des Profils {#update-profile-g}

Für die Aktivität **[!UICONTROL Profil aktualisieren]** gelten spezifische Schutzmechanismen. Sie sind auf [dieser Seite](../building-journeys/update-profiles.md) aufgeführt.

### Lesen der Zielgruppe {#read-segment-g}

Für die Journey-Aktivität [Zielgruppe lesen](../building-journeys/read-audience.md) gelten die folgenden Schutzmechanismen:

* Streaming-Zielgruppen sind immer auf dem neuesten Stand, Batch-Zielgruppen werden jedoch zum Zeitpunkt des Abrufs nicht berechnet. Sie werden nur jeden Tag zum Zeitpunkt der täglichen Batch-Auswertung berechnet.
* Für Journeys, die eine Aktivität vom Typ **Zielgruppe lesen** verwenden, gibt es eine maximale Anzahl von Journeys, die genau zur gleichen Zeit beginnen können. Es werden zwar weitere Versuche vom System durchgeführt, Sie sollten jedoch vermeiden, dass mehr als fünf Journeys (mit **Zielgruppe lesen**, geplant oder beginnend mit „so bald wie möglich“) exakt zur gleichen Zeit beginnen, indem Sie sie über einen bestimmten Zeitraum verteilen, z. B. im Abstand von 5 bis 10 Minuten.
* Die Aktivität **Zielgruppe lesen** kann nicht mit Adobe Campaign-Aktivitäten verwendet werden.
* Die Aktivität **Zielgruppe lesen** kann nur als erste Aktivität in einer Journey nach einer Aktivität vom Typ „Geschäftsereignis“ verwendet werden.
* Eine Journey kann nur über eine Aktivität **Zielgruppe lesen** verfügen.
* Zusätzliche Empfehlungen zur Verwendung der Aktivität **Zielgruppe lesen** finden Sie auf [dieser Seite](../building-journeys/read-audience.md).
* Beim Abrufen des Exportauftrags werden standardmäßig weitere Versuche bei zielgruppenseitig ausgelösten Journeys durchgeführt (beginnend mit der Aktivität **Zielgruppe lesen** oder einem **Geschäftsereignis**). Tritt bei der Erstellung des Exportauftrags ein Fehler auf, werden alle 10 Minuten, aber höchstens eine Stunde lang, weitere Versuche unternommen. Danach wird von einem Fehler ausgegangen. Diese Journey-Typen können daher bis zu einer Stunde nach der geplanten Zeit ausgeführt werden.

### Zielgruppen-Qualifizierung {#audience-qualif-g}

Für die Journey-Aktivität [Zielgruppen-Qualifizierung](../building-journeys/audience-qualification-events.md) gilt der folgende Schutzmechanismus:

* Die Aktivität „Zielgruppen-Qualifizierung“ kann nicht mit Adobe Campaign-Aktivitäten verwendet werden.

### Ausdruckseditor {#expression-editor}

Für den [Journey-Ausdruckseditor](../building-journeys/expression/expressionadvanced.md) gelten die folgenden Leitlinien:

* Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einer Aktivität vom Typ „Zielgruppe lesen“, „Zielgruppen-Qualifizierung“ oder „Geschäftsereignis“ beginnen. Sie müssen eine neue Zielgruppe erstellen und eine `inaudience` in der Journey verwenden.
* `timeSeriesEvents`-Attribute können nicht im Ausdruckseditor verwendet werden. Um auf Erlebnisereignisse auf Profilebene zuzugreifen, erstellen Sie eine neue Feldergruppe basierend auf einem `XDM ExperienceEvent`-Schema.


### In-App-Aktivität {#in-app-activity-limitations}

Für die Aktion **[!UICONTROL In-App-Nachrichten]** gelten die folgenden Schutzmechanismen: Weitere Informationen zu In-App-Nachrichten finden Sie auf [dieser Seite](../in-app/create-in-app.md).

* Diese Funktion ist derzeit nicht für Kundinnen und Kunden im Gesundheitswesen verfügbar.

* Personalisierung kann nur Profilattribute enthalten.

* Die In-App-Aktivität kann nicht mit Adobe Campaign-Aktivitäten verwendet werden.

* Die In-App-Anzeige ist an die Journey-Lebensdauer gebunden, d. h. wenn die Journey für ein Profil endet, werden alle In-App-Nachrichten innerhalb dieser Journey nicht mehr für dieses Profil angezeigt.  Daher ist es nicht möglich, eine In-App-Nachricht direkt von einer Journey-Aktivität aus zu stoppen. Stattdessen müssen Sie die gesamte Journey beenden, damit die In-App-Nachrichten nicht mehr im Profil angezeigt werden.

* Im Testmodus hängt die In-App-Anzeige von der Journey-Lebensdauer ab. Um zu verhindern, dass die Journey während des Tests zu früh endet, passen Sie den **[!UICONTROL Wartezeit]**-Wert für Ihre **[!UICONTROL Warten]**-Aktivitäten an.

* **[!UICONTROL Reaktion]**-Aktivitäten können nicht verwendet werden, um auf ein Öffnen oder Klicken in der App zu reagieren.

* Es kann eine Aktivierungsverzögerung zwischen dem Zeitpunkt auftreten, zu dem ein Benutzerprofil eine In-App-Aktivität auf der Arbeitsfläche erreicht, und dem Zeitpunkt, zu dem es diese In-App-Nachricht zu sehen beginnt.

* Die Inhaltsgröße von In-App-Nachrichten ist auf 2 MB beschränkt. Das Einschließen großer Bilder kann den Veröffentlichungsprozess behindern.

### Aktivität „Springen“ {#jump-g}

Für die Aktivität **[!UICONTROL Springen]** gelten spezifische Schutzmechanismen. Sie sind auf [dieser Seite](../building-journeys/jump.md#jump-limitations) aufgeführt.

### Kampagnenaktivitäten {#ac-g}

Für die Aktivitäten **[!UICONTROL Campaign v7/v8]** und **[!UICONTROL Campaign Standard]** gelten die folgenden Schutzmechanismen:

* Adobe Campaign-Aktivitäten können nicht mit der Aktivität „Zielgruppe lesen“ oder „Zielgruppen-Qualifizierung“ verwendet werden.
* Kampagnenaktivitäten können nicht mit den anderen Kanalaktivitäten verwendet werden: Karte, Code-basiertes Erlebnis, E-Mail, Push, SMS, In-App-Nachrichten, Web.
