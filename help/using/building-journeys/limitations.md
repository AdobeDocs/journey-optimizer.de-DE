---
solution: Journey Optimizer
product: journey optimizer
title: Einschränkungen von Journeys
description: Weitere Informationen zu Einschränkungen von Journeys
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Einschränkung
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '511'
ht-degree: 100%

---

# Einschränkungen {#journey-limitations}

Im Zusammenhang mit der Verwendung von Journeys gibt es diese Einschränkungen:

## Allgemeine Aktionseinschränkungen {#action-limitations}

* Es gibt keine Nachrichtendrosselung beim Versand. 
* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung einstellen. 
* Mit dem integrierten **Reaktionsereignis** können Sie auf vordefinierte Aktionen reagieren (siehe diese [Seite](../building-journeys/reaction-events.md)). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wird, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.

## Einschränkungen bei den Journey-Versionen {#journey-versions-limitations}

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einem **Zielgruppen-Qualifizierungsereignis** beginnen.
* Eine Journey, die in Version 1 mit einer Aktivität vom Typ **Zielgruppen-Qualifizierung** beginnt, muss in weiteren Versionen immer mit einer **Zielgruppen-Qualifizierung** beginnen.
* Die Zielgruppe und der Namespace, die unter **Zielgruppen-Qualifizierung** (dem ersten Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit **Zielgruppe lesen** beginnt, kann in Folgeversionen nicht mit einem anderen Ereignis beginnen.

## Benutzerdefinierte Aktionen  Einschränkungen {#custom-actions-limitations}

* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter. 
* Es werden nur POST- und PUT-Aufrufmethoden unterstützt. 
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit &quot;.&quot; beginnen oder &quot;$&quot;. 
* IP-Adressen sind nicht zulässig. 
* Interne Adobe-Adressen (.adobe.) sind nicht zulässig.

## Einschränkungen bei Ereignissen {#events-limitations}

* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zur Initiierung einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.

## Datenquellen  Einschränkungen {#data-sources-limitations}

* Externe Datenquellen können in einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.

## Journeys, die gleichzeitig mit der Erstellung eines Profils beginnen {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw).

## Einschränkungen beim Lesen von Zielgruppen {#read-audiences-limitations}

* Streaming-Zielgruppen sind immer auf dem neuesten Stand, Batch-Zielgruppen werden jedoch zum Zeitpunkt des Abrufs nicht berechnet. Sie werden nur jeden Tag zum Zeitpunkt der täglichen Batch-Auswertung berechnet.
