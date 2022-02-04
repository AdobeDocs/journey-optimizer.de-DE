---
title: Einschränkungen bei Journey Optimizer
description: Weitere Informationen zu Einschränkungen bei Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 3c8c059e5e3953807b9fc2d8d0eded0d00e49003
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 93%

---

# Einschränkungen {#limitations}

Berechtigungen, Produktbeschränkungen und die Leistung betreffende Sicherheitsmechanismen sind auf der Seite[ Adobe Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;} aufgeführt.

Unten finden Sie zusätzliche Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer].

## Einschränkungen bei Nachrichten {#limitations-messages}

* Mit [!DNL Journey Optimizer] können Sie keine Anlagen zu einer E-Mail  hinzufügen.
* E-Mail-BCC wird in [!DNL Journey Optimizer] nicht unterstützt.
* Dieselbe Versanddomäne kann nicht zum Senden von Nachrichten von verwendet werden [!DNL Adobe Journey Optimizer] und von einem anderen Produkt, z. B. [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage] zum Beispiel.

## Einschränkungen bei Journeys {#limitations-journeys}

### Allgemeine Aktionen {#general-actions}

* Es gibt keine Einschränkung beim Versand.
* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung anpassen.
* Mit dem integrierten Ereignis **Reaktion** können Sie auf vorkonfigurierte Aktionen reagieren. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/reaction-events.md). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wird, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.

### Nachrichtenaktion {#message-action}

* Wenn Sie eine Multi-Channel-Nachricht hinzufügen, werden zwei Nachrichten gesendet.

### Journey-Versionen {#journey-versions-limitations}

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einem **Segmentqualifizierungsereignis** starten.
* Eine Journey, die in Version 1 mit einer **Segmentqualifizierungsaktivität** beginnt, muss in weiteren Versionen immer mit einer **Segmentqualifizierung** beginnen.
* Das Segment und der Namespace, die unter **Segmentqualifizierung** (erster Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den Wiedereintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit einer **Segment lesen** kann nicht mit einem anderen Ereignis in den nächsten Versionen beginnen.

### Benutzerdefinierte Aktionen {#custom-actions}

* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter.
* Es werden nur POST- und PUT-Aufrufmethoden unterstützt
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit „.“ oder &quot;$&quot;
* IP-Adressen sind nicht zulässig
* Interne Adobe-Adressen (.adobe.) sind nicht zulässig.

### Events {#events}

* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zur Initiierung einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingehen. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.

### Datenquellen {#data-sources}

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.

### Journeys, die gleichzeitig mit der Erstellung eines Profils beginnen {#journeys-limitation-profile-creation}

In Adobe Experience Platform gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um Adobe Experience Platform ausreichend Zeit zu geben, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

### Segment lesen {#read-segment}

* Streaming-Segmente sind stets auf dem neuesten Stand, Batch-Segmente werden jedoch zum Zeitpunkt des Abrufs nicht berechnet. Sie werden nur jeden Tag zur täglichen Batch-Auswertung berechnet.
