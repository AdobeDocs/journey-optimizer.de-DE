---
solution: Journey Optimizer
product: journey optimizer
title: Einschränkungen bei Journeys
description: Erfahren Sie mehr über Journey-Einschränkungen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Einschränkungen {#journey-limitations}

Im Folgenden finden Sie Einschränkungen bezüglich der Verwendung von Journeys.

## Allgemeine Aktionsbeschränkungen

* Es gibt keine Versandbeschränkung. 
* Im Falle eines Fehlers werden systematisch drei weitere Versuche durchgeführt. Die Anzahl weiterer Versuche kann nicht an die erhaltene Fehlermeldung angepasst werden. 
* Die integrierten **Reaktion** -Ereignis ermöglicht es Ihnen, auf vordefinierte Aktionen zu reagieren (siehe dies [page](../building-journeys/reaction-events.md)). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wird, müssen Sie ein dediziertes Ereignis konfigurieren. 
* Es ist nicht möglich, zwei Aktionen parallel zu platzieren. Sie müssen sie nacheinander hinzufügen.

## Einschränkungen bei Journey-Versionen {#journey-versions-limitations}

* Eine Journey, die in v1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einer **Segmentqualifikation** -Ereignis.
* Eine Journey, die mit einer **Segmentqualifikation** -Aktivität in v1 muss immer mit einer **Segmentqualifikation** in weiteren Versionen.
* Das Segment und der Namespace, die in **Segmentqualifikation** (erster Knoten) kann in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit einer **Segment lesen** kann nicht mit einem anderen Ereignis in den nächsten Versionen beginnen.
 

## Einschränkungen für benutzerdefinierte Aktionen

* Die URL der benutzerdefinierten Aktion unterstützt keine dynamischen Parameter. 
* Es werden nur POST- und PUT-Aufrufmethoden unterstützt. 
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit &quot;.&quot;beginnen. oder &quot;$&quot;. 
* IP-Adressen sind nicht zulässig. 
* Interne Adobe-Adressen (.adobe.) sind nicht zulässig.
 

## Ereignisbeschränkungen

* Bei systemgenerierten Ereignissen müssen Streaming-Daten, die zur Initiierung einer Customer Journey verwendet werden, zunächst in Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
 

## Einschränkungen bei Datenquellen

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API verwendet werden, JSON unterstützen und in der Lage sein, das Volumen der Anfragen zu verarbeiten.

## Journeys, die gleichzeitig mit der Erstellung eines Profils beginnen {#journeys-limitation-profile-creation}

Es gibt eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung in Adobe Experience Platform. Das Service Level Target (SLT) in Bezug auf die Latenz beträgt &lt; 1 Minute von der Aufnahme in Unified Profile für das 95. Perzentil der Anforderungen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht ordnungsgemäß.

Sie können aus einer dieser beiden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, damit Adobe Experience Platform die Zeit erhält, die für die Aufnahme in den Profil-Service erforderlich ist.

* Richten Sie eine Journey ein, die das Profil nicht sofort nutzt. Wenn die Journey beispielsweise dazu bestimmt ist, die Erstellung eines Kontos zu bestätigen, kann das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

## Segmentbeschränkungen lesen

* Streaming-Segmente sind immer aktuell, Batch-Segmente werden jedoch nicht zum Zeitpunkt des Abrufs berechnet. Sie werden nur täglich zur täglichen Batch-Auswertungszeit ausgewertet.
