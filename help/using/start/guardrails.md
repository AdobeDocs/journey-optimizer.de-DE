---
solution: Journey Optimizer
product: journey optimizer
title: Limits und Einschränkungen von Journey Optimizer
description: Erfahren Sie mehr über die Limits von Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 9b4ab81a362c38dce5ff4b10fb301c81ed117688
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# Limits und Einschränkungen {#limitations}

Berechtigungen, Produktbeschränkungen und Leistungsgarantien finden Sie unter [Produktbeschreibungsseite für Adobe Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

Unten finden Sie zusätzliche Limits und Einschränkungen bei der Verwendung von [!DNL Adobe Journey Optimizer].

## Limits bei Nachrichten {#message-guardrails}

* Sie können keine Anlagen zu einer E-Mail hinzufügen mit [!DNL Journey Optimizer].
* Dieselbe Versanddomäne kann nicht zum Senden von Nachrichten von verwendet werden [!DNL Adobe Journey Optimizer] und von einem anderen Produkt, z. B. [!DNL Adobe Campaign] oder [!DNL Adobe Marketo Engage] zum Beispiel.


## Limits bei der Entscheidungsverwaltung {#offer-guardrails}

Leistungsgarantien und statische Beschränkungen für Entscheidungen werden im Abschnitt [Produktbeschreibungsseite für Adobe Offer Decisioning App Service](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Limits bei Landingpages {#lp-guardrails}

* Nur eine **Formular** -Komponente kann auf einer einzelnen primären Seite verwendet werden.
* Die **Formular** -Komponente kann nicht in Unterseiten verwendet werden.
* Sie können einer Landingpage keine Preheader hinzufügen.
* Sie können die **Eigene Code** bei der Erstellung einer primären Landingpage.

## Limits bei Journeys {#journeys-guardrails}

### Allgemeine Maßnahmen {#general-actions-g}

* Es gibt keine Versandbeschränkung.
* Im Falle eines Fehlers werden systematisch drei weitere Versuche durchgeführt. Die Anzahl weiterer Versuche kann nicht an die erhaltene Fehlermeldung angepasst werden.
* Die integrierten **Reaktion** -Ereignis ermöglicht es Ihnen, auf vordefinierte Aktionen zu reagieren. Weitere Informationen finden Sie unter [diese Seite](../building-journeys/reaction-events.md). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wird, müssen Sie ein dediziertes Ereignis konfigurieren.
* Es ist nicht möglich, zwei Aktionen parallel zu platzieren. Sie müssen sie nacheinander hinzufügen.
* Normalerweise kann ein Profil nicht mehrmals in derselben Journey gleichzeitig vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, dies jedoch erst tun, wenn er die vorherige Instanz der Journey vollständig verlassen hat. [Mehr dazu](../building-journeys/end-journey.md)

### Journey-Versionen {#journey-versions-g}

* Eine Journey, die in v1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einer **Segmentqualifikation** -Ereignis.
* Eine Journey, die mit einer **Segmentqualifikation** -Aktivität in v1 muss immer mit einer **Segmentqualifikation** in weiteren Versionen.
* Das Segment und der Namespace, die in **Segmentqualifikation** (erster Knoten) kann in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit einer **Segment lesen** kann nicht mit einem anderen Ereignis in den nächsten Versionen beginnen.

### Benutzerdefinierte Aktionen {#custom-actions-g}

* Die URL der benutzerdefinierten Aktion unterstützt keine dynamischen Parameter.
* Nur POST- und PUT-Aufrufmethoden werden unterstützt
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit &quot;.&quot;beginnen. oder &quot;$&quot;
* IP-Adressen sind nicht zulässig
* Interne Adobe-Adressen (.adobe.) sind nicht zulässig.

### Veranstaltungen {#events-g}

* Bei systemgenerierten Ereignissen müssen Streaming-Daten, die zur Initiierung einer Customer Journey verwendet werden, zunächst in Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in Adobe Experience Platform eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.
* Geschäftsereignisse können nicht zusammen mit Einzelereignissen oder Segmentqualifikationsaktivitäten verwendet werden.
* Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzmaßnahme, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Eintritt in das Profil wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis eine Journey um 12:01 Uhr für ein bestimmtes Profil auslöst und ein anderes um 12:03 Uhr eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), startet die Journey für dieses Profil nicht erneut.

### Datenquellen {#data-sources-g}

* Externe Datenquellen können innerhalb einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API verwendet werden, JSON unterstützen und in der Lage sein, das Volumen der Anfragen zu verarbeiten.

### Journeys und Profilerstellung {#journeys-limitation-profile-creation}

Es gibt eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung in Adobe Experience Platform. Das Service Level Target (SLT) in Bezug auf die Latenz beträgt &lt; 1 Minute von der Aufnahme in Unified Profile für das 95. Perzentil der Anforderungen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen aus dem Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht ordnungsgemäß.

Sie können aus einer dieser beiden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, damit Adobe Experience Platform die Zeit erhält, die für die Aufnahme in den Profil-Service erforderlich ist.

* Richten Sie eine Journey ein, die das Profil nicht sofort nutzt. Wenn die Journey beispielsweise dazu bestimmt ist, die Erstellung eines Kontos zu bestätigen, kann das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw.).

### Segment lesen {#read-segment-g}

* Streaming-Segmente sind immer aktuell, Batch-Segmente werden jedoch nicht zum Zeitpunkt des Abrufs berechnet. Sie werden nur täglich zur täglichen Batch-Auswertungszeit ausgewertet.
* Für Journeys mit der Aktivität Segment lesen gibt es eine maximale Anzahl von Journeys, die exakt zur gleichen Zeit beginnen können. Weitere Zustellversuche werden vom System durchgeführt. Vermeiden Sie jedoch, dass mehr als fünf Journeys (mit Segment lesen, geplant oder &quot;so bald wie möglich&quot;gestartet werden) exakt zur gleichen Zeit beginnen, indem sie über einen bestimmten Zeitraum verteilt werden, z. B. zwischen 5 und 10 Minuten.

### Ausdruckseditor {#expression-editor}

* Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einem Segment lesen, einer Segmentqualifizierung oder einer Geschäftsereignisaktivität beginnen.

