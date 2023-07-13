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
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 74%

---

# Leitlinien und Einschränkungen {#limitations}

Berechtigungen, Produkteinschränkungen und die Leistung betreffende Leitplanken sind auf der Seite [Adobe Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} aufgeführt.

Beachten Sie auch die [Leitplanken für Echtzeit-Kundenprofildaten](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=de){target="_blank"}, bevor Sie beginnen.

Unten finden Sie zusätzliche Leitlinien und Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer].

## Unterstützte Browser {#browsers}

Die Benutzeroberfläche von Adobe [!DNL Journey Optimizer] wurde für eine optimale Funktionsweise in der neuesten Version von Google Chrome entwickelt. Bei der Verwendung bestimmter Funktionen in älteren Versionen oder anderen Browsern können Probleme auftreten.

## Schutzmaßnahmen bei Nachrichten {#message-guardrails}

* Mit [!DNL Journey Optimizer] können Sie keine Anlagen zu einer E-Mail hinzufügen.
* Sie können dieselbe Versand-Domain nicht zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und einem anderen Produkt verwenden, beispielsweise [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage].


## Schutzmaßnahmen bei Landingpages {#lp-guardrails}

* Es kann nur eine einzige **Formular**-Komponente auf einer einzelnen primären Seite verwendet werden.
* Die **Formular**-Komponente kann nicht in Unterseiten verwendet werden.
* Sie können keine Preheader zu einer Landingpage hinzufügen.
* Sie können die Option **Eigene Codierung** nicht auswählen, wenn Sie eine primäre Landingpage entwerfen.

## Schutzmaßnahmen bei Journeys {#journeys-guardrails}

### Allgemeine Limits für Journey {#journeys-guardrails-journeys}

* Die Anzahl der Aktivitäten in einer Journey ist auf maximal 50 begrenzt. Die Anzahl der Aktivitäten wird im oberen linken Bereich der Journey-Arbeitsfläche angezeigt. Dies unterstützt Lesbarkeit, Qualitätssicherung und Fehlerbehebung.

### Allgemeine Aktionen {#general-actions-g}

* Es gibt keine Nachrichtendrosselung beim Versand.
* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung anpassen.
* Mit dem integrierten Ereignis **Reaktion** können Sie auf vorkonfigurierte Aktionen reagieren. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/reaction-events.md). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wurde, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.
* In der Regel kann ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](../building-journeys/end-journey.md)

### Journey-Versionen {#journey-versions-g}

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können keine Journey mit einer **Zielgruppenqualifikation** -Ereignis.
* Eine Journey, die mit einer **Zielgruppenqualifikation** -Aktivität in v1 muss immer mit einer **Zielgruppenqualifikation** in weiteren Versionen.
* Die in **Zielgruppenqualifikation** (erster Knoten) kann in neuen Versionen nicht geändert werden.
* Die Regel für den Wiedereintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit einer **Audience lesen** kann nicht mit einem anderen Ereignis in den nächsten Versionen beginnen.
* Es ist nicht möglich, eine neue Journey-Version einer gelesenen Audience mit inkrementellem Lesen zu erstellen. Sie müssen die Journey duplizieren.

### Benutzerdefinierte Aktionen {#custom-actions-g}

* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter.
* Es werden nur POST- und PUT-Aufrufmethoden unterstützt
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit „.“ oder „$“ beginnen.
* IP-Adressen sind nicht zulässig
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.
* Integrierte benutzerdefinierte Aktionen können nicht entfernt werden.

### Ereignisse {#events-g}

* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zum Starten einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
* Geschäftsereignisse können nicht zusammen mit Einzelereignissen oder Zielgruppenqualifikationsaktivitäten verwendet werden.
* Einzelne Journey (beginnend mit einem Ereignis oder einer Zielgruppenqualifikation) enthalten eine Schutzmaßnahme, die verhindert, dass Journey fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.
* Journey Optimizer erfordert, dass Ereignisse an den Data Collection Core Service (DCCS) gestreamt werden, damit eine Journey ausgelöst werden kann. Ereignisse, die in Batches aufgenommen werden, oder Ereignissen aus internen Journey Optimizer-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking usw.) können nicht zum Auslösen einer Journey verwendet werden. Für Anwendungsfälle, in denen Sie keine Streaming-Ereignisse erhalten können, erstellen Sie eine Zielgruppe, die auf diesen Ereignissen basiert, und verwenden Sie die **Audience lesen** Aktivität. Die Zielgruppenqualifizierung kann technisch verwendet werden, kann aber basierend auf den verwendeten Aktionen zu nachgelagerten Herausforderungen führen.

### Datenquellen {#data-sources-g}

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.
* Interne Adobe-Adressen (`.adobe.*`) sind in URLs und APIs nicht zulässig.

### Journeys und Profilerstellung {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

### Audience lesen {#read-segment-g}

* Streaming-Zielgruppen sind immer aktuell, Batch-Zielgruppen werden jedoch nicht zum Zeitpunkt des Abrufs berechnet. Sie werden nur jeden Tag zur täglichen Batch-Auswertung berechnet.
* Bei Journey, die die Aktivität Audience lesen verwenden, gibt es eine maximale Anzahl von Journey, die exakt zur gleichen Zeit beginnen können. Weitere Zustellversuche werden vom System durchgeführt. Vermeiden Sie jedoch, dass mehr als fünf Journey (mit &quot;Audience lesen&quot;, geplant oder &quot;so bald wie möglich&quot; gestartet werden) exakt gleichzeitig beginnen, indem sie über einen bestimmten Zeitraum verteilt werden, z. B. zwischen 5 und 10 Minuten.

### Ausdruckseditor {#expression-editor}

* Feldergruppen für Erlebnisereignisse können nicht in Journey verwendet werden, die mit der Aktivität Lesen der Zielgruppe, Zielgruppenqualifizierung oder Geschäftsereignis beginnen. Sie müssen eine neue Zielgruppe erstellen und eine Segmentbedingung in der Journey verwenden.


