---
solution: Journey Optimizer
product: journey optimizer
title: Limits und Einschränkungen von Journey Optimizer
description: Weitere Informationen zu Limits bei Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 9b4ab81a362c38dce5ff4b10fb301c81ed117688
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 100%

---

# Limits und Einschränkungen {#limitations}

Berechtigungen, Produkteinschränkungen und die Leistung betreffende Limits sind auf der Seite [Adobe Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;} aufgeführt.

Unten finden Sie zusätzliche Limits und Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer].

## Beschränkungen bei Nachrichten {#message-guardrails}

* Mit [!DNL Journey Optimizer] können Sie keine Anlagen zu einer E-Mail hinzufügen.
* Sie können dieselbe Versand-Domain nicht zum Senden von Nachrichten von [!DNL Adobe Journey Optimizer] und einem anderen Produkt verwenden, beispielsweise [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage].


## Beschränkungen beim Entscheidungs-Management {#offer-guardrails}

Leistungsbeschränkungen und statische Beschränkungen für das Decisioning werden auf der [Produktbeschreibungsseite für den Adobe Offer Decisioning App Service](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;} aufgeführt.


## Beschränkungen bei Landingpages {#lp-guardrails}

* Es kann nur eine einzige **Formular**-Komponente auf einer einzelnen primären Seite verwendet werden.
* Die **Formular**-Komponente kann nicht in Unterseiten verwendet werden.
* Sie können keine Preheader zu einer Landingpage hinzufügen.
* Sie können die Option **Eigene Codierung** nicht auswählen, wenn Sie eine primäre Landingpage entwerfen.

## Beschränkungen bei Journeys {#journeys-guardrails}

### Allgemeine Aktionen {#general-actions-g}

* Es gibt keine Nachrichtendrosselung beim Versand.
* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung anpassen.
* Mit dem integrierten Ereignis **Reaktion** können Sie auf vorkonfigurierte Aktionen reagieren. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/reaction-events.md). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wurde, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.
* In der Regel kann ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](../building-journeys/end-journey.md)

### Journey-Versionen {#journey-versions-g}

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einem **Segmentqualifizierungsereignis** starten.
* Eine Journey, die in Version 1 mit einer **Segmentqualifizierungsaktivität** beginnt, muss in weiteren Versionen immer mit einer **Segmentqualifizierung** beginnen.
* Das Segment und der Namespace, die unter **Segmentqualifikation** (erster Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit **Segment lesen** beginnt, kann in den nächsten Versionen nicht mit einem anderen Ereignis beginnen.

### Benutzerdefinierte Aktionen {#custom-actions-g}

* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter.
* Es werden nur POST- und PUT-Aufrufmethoden unterstützt
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit „.“ oder „$“ beginnen.
* IP-Adressen sind nicht zulässig
* Interne Adobe-Adressen (.adobe.) sind nicht zulässig.

### Ereignisse {#events-g}

* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zum Starten einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
* Geschäftsereignisse können nicht zusammen mit unitären Ereignissen oder Segmentqualifikationsaktivitäten verwendet werden.
* Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzvorkehrung, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.

### Datenquellen {#data-sources-g}

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.

### Journeys und Profilerstellung {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

### Segment lesen {#read-segment-g}

* Streaming-Segmente sind stets auf dem neuesten Stand, Batch-Segmente werden jedoch zum Zeitpunkt des Abrufs nicht berechnet. Sie werden nur jeden Tag zur täglichen Batch-Auswertung berechnet.
* Bei Journeys, die die Aktivität „Segment lesen“ verwenden, gibt es eine maximale Anzahl von Journeys, die exakt zur gleichen Zeit beginnen können. Weitere Zustellversuche werden zwar vom System durchgeführt, Sie sollten jedoch vermeiden, dass mehr als fünf Journeys (mit „Segment lesen“, geplant oder „so bald wie möglich“) exakt gleichzeitig beginnen, indem Sie sie über einen bestimmten Zeitraum verteilen, z. B. mit 5 bis 10 Minuten Abstand.

### Ausdruckseditor {#expression-editor}

* Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einer Aktivität vom Typ „Segment lesen“, „Segmentqualifikation“ oder „Geschäftsereignis“ beginnen.

