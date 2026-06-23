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
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1276
ht-degree: 39%

---

# Einschränkungen {#journey-limitations}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Überprüfen Sie die Einschränkungen und Leitplanken für Journey, einschließlich Aktionen, Versionen, benutzerdefinierten Aktionen, Ereignissen und Datenquellen.

>[!ENDSHADEBOX]

Im Zusammenhang mit der Verwendung von Journeys gibt es diese Einschränkungen:

## Allgemeine Aktionseinschränkungen {#action-limitations}

* Es gibt keine Nachrichtendrosselung beim Versand.
* Im Falle eines Fehlers werden systematisch drei weitere Zustellversuche durchgeführt. Sie können die Anzahl der weiteren Zustellversuche nicht entsprechend der erhaltenen Fehlermeldung einstellen.
* Mit dem integrierten **Reaktionsereignis** können Sie auf vordefinierte Aktionen reagieren (siehe diese [Seite](../building-journeys/reaction-events.md)). Wenn Sie auf eine Nachricht reagieren möchten, die über eine benutzerdefinierte Aktion gesendet wurde, müssen Sie ein spezielles Ereignis konfigurieren.
* Sie können nicht zwei Aktionen parallel platzieren, sondern müssen sie nacheinander hinzufügen.


## Einschränkungen bei den Journey-Versionen {#journey-versions-limitations}

* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in weiteren Versionen nicht mit etwas anderem als einem Ereignis beginnen. Sie können eine Journey nicht mit einem **Zielgruppen-Qualifizierungsereignis** beginnen.
* Eine Journey, die in Version 1 mit einer Aktivität vom Typ **Zielgruppen-Qualifizierung** beginnt, muss in weiteren Versionen immer mit einer **Zielgruppen-Qualifizierung** beginnen.
* Die Zielgruppe und der Namespace, die unter **Zielgruppen-Qualifizierung** (dem ersten Knoten) ausgewählt wurden, können in neuen Versionen nicht geändert werden.
* Die Regel für den erneuten Eintritt muss in allen Journey-Versionen gleich sein.
* Eine Journey, die mit **Zielgruppe lesen** beginnt, kann in Folgeversionen nicht mit einem anderen Ereignis beginnen.

## Einschränkungen bei benutzerdefinierten Aktionen {#custom-actions-limitations}

* Die URL einer benutzerdefinierten Aktion unterstützt keine dynamischen Parameter. 
* Es werden nur POST- und PUT-Aufrufmethoden unterstützt. 
* Der Name des Abfrageparameters oder der Kopfzeile darf nicht mit &quot;.“ oder &quot;$&quot; beginnen. 
* IP-Adressen sind nicht zulässig. 
* Interne Adobe-Adressen (.adobe.) sind nicht zulässig.

## Einschränkungen bei Ereignissen {#events-limitations}

* Für systemgenerierte Ereignisse müssen Streaming-Daten, die zur Initiierung einer Customer Journey verwendet werden, zunächst innerhalb von Journey Optimizer konfiguriert werden, um eine eindeutige Orchestrierungs-ID zu erhalten. Diese Orchestrierungs-ID muss an die Streaming-Payload angehängt werden, die in [!DNL Adobe Experience Platform] eingeht. Diese Einschränkung gilt nicht für regelbasierte Ereignisse.

## Einschränkungen bei Reaktionsereignissen {#reaction-limitations}

* Aktivitäten des Typs **[!UICONTROL Reaktion]** müssen in der Journey-Arbeitsfläche unmittelbar nach einer [Kanalaktionsaktivität](../building-journeys/journey-action.md) platziert werden. Das Platzieren einer Aktivität **[!UICONTROL Warten]** oder einer anderen Aktivität zwischen der Kanalaktion und der Aktivität des Typs **[!UICONTROL Reaktion]** wird nicht unterstützt und kann dazu führen, dass die Reaktion nicht wie erwartet funktioniert. Weiterführende Informationen finden Sie in [diesem Abschnitt](../building-journeys/reaction-events.md).

## Einschränkungen bei Datenquellen {#data-sources-limitations}

* Externe Datenquellen können in einer Customer Journey genutzt werden, um externe Daten in Echtzeit zu suchen. Diese Quellen müssen über die REST-API nutzbar sein, JSON unterstützen und in der Lage sein, das Anfragevolumen zu verarbeiten.

## Journeys, die gleichzeitig mit der Erstellung eines Profils beginnen {#journeys-limitation-profile-creation}

In [!DNL Adobe Experience Platform] gibt es eine Verzögerung bei der API-basierten Profilerstellung/-aktualisierung. Das Service Level Target (SLT) in Bezug auf die Latenzzeit ist &lt; 1 Minute von der Aufnahme bis zum Unified Profile für das 95. Perzentil der Anfragen bei einem Volumen von 20.000 Anfragen pro Sekunde (RPS).

Wenn eine Journey gleichzeitig mit einer Profilerstellung ausgelöst wird und sofort Informationen vom Profil-Service prüft/abruft, funktioniert sie möglicherweise nicht richtig.

Sie können aus einer der beiden folgenden Lösungen wählen:

* Fügen Sie nach dem ersten Ereignis eine Warteaktivität hinzu, um [!DNL Adobe Experience Platform] die Zeit zu geben, die sie benötigt, um die Aufnahme in den Profil-Service durchzuführen.

* Richten Sie eine Journey ein, bei der das Profil nicht sofort genutzt wird. Wenn die Journey beispielsweise dazu dient, eine Kontoerstellung zu bestätigen, könnte das Erlebnisereignis Informationen enthalten, die zum Senden der ersten Bestätigungsnachricht benötigt werden (Vorname, Nachname, E-Mail-Adresse usw).

## Einschränkungen beim Lesen von Zielgruppen {#read-audiences-limitations}

* Streaming-Zielgruppen sind immer auf dem neuesten Stand, Batch-Zielgruppen werden jedoch zum Zeitpunkt des Abrufs nicht berechnet. Sie werden nur jeden Tag zum Zeitpunkt der täglichen Batch-Auswertung berechnet.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden die harten technischen Einschränkungen aufgelistet, die für Journey-Aktionen, Journey-Versionen, benutzerdefinierte Aktionen, Ereignisse, Reaktionsereignisse, Datenquellen und das Lesen von Zielgruppen in Adobe Journey Optimizer gelten.

**intents:**

* Informationen zu den Beschränkungen für das Senden und Wiederholen von Journey-Aktionen
* Erfahren Sie, welche Journey-Versionsübergänge zulässig oder blockiert sind
* Identifizieren von Einschränkungen für URL, Methode und Header-Konfiguration benutzerdefinierter Aktionen
* Datenquellenanforderungen für die Integration externer Systeme verstehen
* Vermeiden Sie zeitliche Probleme beim Starten einer Journey zum gleichen Zeitpunkt wie bei der Profilerstellung

**Glossar:**

* **Reaktionsereignis**: Eine Journey-Aktivität, die auf die Interaktion eines Profils mit einer Kanalaktion wartet (z. B. E-Mail-Öffnen oder Klicken). Sie muss unmittelbar nach der Kanalaktionsaktivität platziert werden. *(produktspezifisch)*
* **Regelbasiertes Ereignis**: Ein Ereignistyp, bei dem der Trigger durch eine logische Bedingung und nicht durch eine systemgenerierte Orchestrierungs-ID definiert wird. *(produktspezifisch)*
* **SLT (Service Level Target)**: Der Latenz-Benchmark für die API-basierte Profilerstellung/-aktualisierung in Adobe Experience Platform - weniger als 1 Minute von der Aufnahme bis zum Unified Profile im 95. Perzentil für 20.000 RPS.

**Leitplanken:**

* Es wird keine Sendungsdrosselung angewendet. Bei einem Fehler werden automatisch drei weitere Zustellversuche unternommen und sie können nicht angepasst werden
* Zwei Aktionen können nicht parallel ausgeführt werden. Sie müssen sequenziell hinzugefügt werden
* Eine Journey, die in Version 1 mit einer Ereignisaktivität beginnt, kann in späteren Versionen nicht mit einer Nicht-Ereignisaktivität beginnen
* Eine Journey, die in Version 1 mit einer Zielgruppen-Qualifizierung beginnt, muss in allen nachfolgenden Versionen immer mit der Zielgruppen-Qualifizierung beginnen. Die Zielgruppe und der Namespace können nicht geändert werden
* Eine Journey, die mit „Zielgruppe lesen“ beginnt, kann in den nächsten Versionen nicht mit einem anderen Ereignis beginnen.
* Die URL für benutzerdefinierte Aktionen unterstützt keine dynamischen Parameter, sondern nur POST- und PUT-Aufrufmethoden
* Abfrageparameter und Kopfzeilennamen für benutzerdefinierte Aktionen dürfen nicht mit &quot;.“ beginnen. oder &quot;$&quot;; IP-Adressen und interne Adobe-Adressen (.adobe.) sind nicht zulässig
* Reaktionsaktivitäten müssen sofort nach einer Kanalaktionsaktivität platziert werden. Das Einfügen einer Warte- oder anderen Aktivität zwischen ihnen wird nicht unterstützt
* Externe Datenquellen müssen über die REST-API zugänglich sein, JSON unterstützen und das Anfragevolumen verarbeiten
* Batch-Zielgruppen werden nur einmal täglich zur täglichen Batch-Auswertungszeit ausgewertet. Sie werden zum Abrufzeitpunkt nicht neu berechnet
* Wenn ein Journey gleichzeitig mit einer Profilerstellung ausgelöst wird, sind aufgrund der Platform-Aufnahmelatenz möglicherweise noch keine Profildaten verfügbar

**Terminologie:**

* Kanonischer Name: Journey Einschränkungen — Akronym: none — Varianten: Journey-Schutzmechanismen, Journey Einschränkungen
* Verwechseln Sie nicht: „Begrenzung des Reaktionsereignisses“ ≠ „allgemeine Aktionsbegrenzung“ - Das Reaktionsereignis muss direkt nach einer Kanalaktion platziert werden. Die allgemeine Aktionsbegrenzung umfasst Wiederholungen, Parallelität und Drosselung

**FAQ:**

* **F: Wie oft versucht Journey Optimizer eine fehlgeschlagene Aktion erneut?** — Drei weitere Zustellversuche werden automatisch durchgeführt; die Anzahl der weiteren Zustellversuche kann nicht konfiguriert werden.
* **F: Kann ich eine Warteaktivität zwischen einer Kanalaktion und einem Reaktionsereignis platzieren?** — Nein. Das Reaktionsereignis muss unmittelbar nach der Kanalaktionsaktivität platziert werden. Das Hinzufügen von Aktivitäten zwischen wird nicht unterstützt und kann dazu führen, dass das Reaktionsereignis nicht wie erwartet funktioniert.
* **F: Kann ich den ersten Ereignistyp bei der Erstellung einer neuen Journey-Version ändern?** — Nein; der in v1 festgelegte Eingabemechanismus muss in allen nachfolgenden Versionen beibehalten werden. Eine Journey, die mit einem Ereignis beginnt, muss weiterhin mit einem Ereignis beginnen, und eine Journey, die mit Zielgruppen-Qualifizierung beginnt, muss immer mit Zielgruppen-Qualifizierung beginnen.
* **F: Warum funktioniert mein Journey nicht, wenn er gleichzeitig mit der Profilerstellung ausgelöst wird?** — Die Profilerstellung über die API hat eine Latenz, bevor Daten im einheitlichen Profil verfügbar sind (SLT &lt; 1 Minute bei 95. Perzentil). Durch Hinzufügen einer Warteaktivität nach dem ersten Ereignis hat Platform Zeit, die Aufnahme abzuschließen.
* **F: Sind Streaming-Zielgruppen in Journey immer aktuell?** — Ja; Streaming-Zielgruppen sind immer auf dem neuesten Stand. Batch-Zielgruppen werden jedoch nur einmal täglich zur täglichen Batch-Auswertungszeit ausgewertet, nicht zum Zeitpunkt des Abrufs.

+++
