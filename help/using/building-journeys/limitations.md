---
title: Einschränkungen beim Journey
description: Weitere Informationen zu Einschränkungen beim Journey
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 0%

---

# Einschränkungen {#journey-limitations}

![](../assets/do-not-localize/badge.png)

Hier sind Einschränkungen hinsichtlich der Verwendung von Journey.

## Einschränkungen bei Journey Liste

* In der Liste &quot;Journey&quot;werden Filter, Suchvorgänge und Spaltenauswahl bei der Seitenaktualisierung zurückgesetzt.

## Allgemeine Aktionseinschränkungen

* Es gibt keine Einschränkung beim Versand. 
* Im Falle eines Fehlers werden systematisch zwei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung anpassen. 
* Mit dem integrierten **Reaktionsereignis** können Sie auf vordefinierte Aktionen reagieren (siehe diese [Seite](../building-journeys/reaction-events.md)). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wird, müssen Sie ein spezielles Ereignis konfigurieren. 
* Die Integration von Adobe Campaign Classic ist nicht als Produkt verfügbar.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.

## Einschränkungen der Nachrichtenaktion

* Die **Message**-Aktivität erlaubt Ihnen nicht, Kontextdaten aus der Journey zu verwenden. Die Personalisierung von Nachrichten wird direkt beim Entwerfen der Nachricht in Journey Optimizer durchgeführt.

* Wenn Sie eine Mehrkanal-Nachricht hinzufügen, werden zwei Nachrichten gesendet.

## Einschränkungen bei den Journey-Versionen {#journey-versions-limitations}

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen.
Sie können eine Journey nicht mit einem **Segmentqualifikationsereignis** starten.
* Eine Journey, die in Version 1 mit einer **Segmentqualifikationsaktivität** beginnt, muss in weiteren Versionen immer mit einer **Segmentqualifikation** beginnen.
* Das Segment und der Namespace, die unter **Segmentqualifikation** (erster Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den Wiedereintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit einem **Read-Segment** beginnt, kann in den nächsten Versionen nicht mit einem anderen Ereignis Beginn werden.
 

## Einschränkungen bei benutzerdefinierten Aktionen

* Die URL der benutzerdefinierten Aktion unterstützt keine dynamischen Parameter. 
* Es werden nur POST- und PUT-Aufrufmethoden unterstützt. 
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit „.“ or &quot;$&quot;. 
* IP-Adressen sind nicht zulässig. 
* Interne Adobe-Adressen (.adobe.) sind nicht zulässig.
 

## Einschränkungen bei Ereignissen

* Bei systemgenerierten Ereignissen müssen Streaming-Daten, die zum Initiieren einer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Organisations-ID zu erhalten.Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
 

## Einschränkungen bei Datenquellen

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.

## Journeys, die gleichzeitig mit der Erstellung eines Profils beginnen {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

## Segmentbeschränkungen lesen

* Es ist nicht möglich, eine segmentbasierte Journey innerhalb eines kürzeren Zeitrahmens als 1 Stunde Trigger.
* Streaming-Segmente sind stets auf dem neuesten Stand, Batch-Segmente werden jedoch nicht zum Zeitpunkt des Abrufs berechnet. Sie werden nur jeden Tag zur täglichen Batch-Auswertung ausgewertet.
