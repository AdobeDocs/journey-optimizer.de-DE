---
solution: Journey Optimizer
product: journey optimizer
title: Gemeinsame Felder für journeyStep-Ereignisse
description: Gemeinsame Felder für journeyStep-Ereignisse
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Gemeinsame Felder für journeyStep-Ereignisse {#sharing-common-fields}

Diese Feldergruppe wird von journeyStepEvent und journeyStepProfileEvent gemeinsam genutzt.

Dies sind die gängigen XDM-Felder, die [!DNL Journey Optimizer] sendet an Adobe Experience Platform. Gemeinsame Felder werden für jeden Schritt gesendet, der in einer Journey verarbeitet wird. Für benutzerdefinierte Aktionen und Anreicherungen werden spezifischere Felder verwendet.

Einige dieser Felder sind nur in bestimmten Verarbeitungsmustern verfügbar (Aktionsausführung, Datenabruf usw.) um die Größe von Ereignissen zu begrenzen.

## Eintritt {#entrance-field}

Gibt an, ob der Benutzer in die Journey eingestiegen ist. Wenn der Wert nicht vorhanden ist, gehen wir davon aus, dass er &quot;false&quot;ist.

Typ: boolean

Werte: true/false

## reeingang {#reentrance-field}

Gibt an, ob der Benutzer die Journey mit derselben Instanz erneut betreten hat. Wenn der Wert nicht vorhanden ist, gehen wir davon aus, dass er &quot;false&quot;ist.

Typ: boolean

Werte: true/false

## instanceEnded {#instance-ended-field}

Gibt an, ob die Instanz beendet wurde (erfolgreich oder nicht).

Typ: boolean

## eventID {#eventid-field}

Ereignis-ID in der Verarbeitung für die Schrittverarbeitung. Wenn es sich bei dem Ereignis um ein externes Ereignis handelt, ist der Wert dessen eventId. Wenn es sich bei dem Ereignis um ein internes Ereignis handelt, ist der Wert die interne eventId (z. B. scheduledNotificationReceived, executeAction usw.).

Typ: Zeichenfolge

## nodeID {#nodeid-field}

Client-Knoten-ID (von der Arbeitsfläche).

Typ: Zeichenfolge

## stepID {#stepdid-field}

Eindeutige ID des Schritts, der derzeit verarbeitet wird.

Typ: Zeichenfolge

## stepName {#stepname-field}

Name des Schritts, der derzeit verarbeitet wird.

Typ: Zeichenfolge

## stepType {#steptype-field}

Typ des Schritts.

Typ: Zeichenfolge

Mögliche Werte:

* Bedingung
* Aktion
* Planung
* Timer

## stepStatus {#stepstatus-field}

Status des Schritts, der den Status des Schritts darstellt, wenn die Verarbeitung abgeschlossen ist (und das Schrittereignis ausgelöst wurde).

Typ: Zeichenfolge

Der Status kann wie folgt lauten:

* ended: der Schritt keine Transition aufweist und die Verarbeitung erfolgreich beendet wurde.
* error: bei der Schrittverarbeitung ist ein Fehler aufgetreten.
* Transitionen: Der Schritt wartet darauf, dass ein Ereignis zu einem anderen Schritt übergeht.
* capped: der Schritt ist aufgrund eines Begrenzungsfehlers fehlgeschlagen, der während einer Aktion oder Anreicherung ausgelöst wurde.
* timedout: der Schritt ist aufgrund eines Zeitüberschreitungsfehlers fehlgeschlagen, der während einer Aktion oder Anreicherung ausgelöst wurde.
* instanceTimedout: Der Schritt hat die Verarbeitung beendet, da die Instanz ihren Timeout erreicht hat.

## journeyID {#journeyid-field}

Kennung der Journey.

Typ: Zeichenfolge

## journeyVersionID {#journeyversionid-field}

Kennung der Journey-Version. Diese ID stellt den Identitätsverweis auf die Journey im Fall von journeyStepEvent dar.

Typ: Zeichenfolge

## journeyVersionName {#journeyversionname-field}

Name der Journey-Version.

Typ: Zeichenfolge

## journeyVersion {#journeyversion-field}

Version der Journey-Version.

Typ: Zeichenfolge

## instanceID {#instanceid-field}

Interne Kennung der Journey-Instanz.

Typ: Zeichenfolge

## externalKey {#externalkey-field}

Externer Schlüssel, der aus dem Ereignis zur Verarbeitung extrahiert wurde.

Typ: Zeichenfolge

## parentStepID {#parenstepid-field}

Schritt-ID des übergeordneten Schritts des aktuellen verarbeiteten Schritts in der Instanz.

Typ: Zeichenfolge

## parentStepName {#parentstepname-field}

Schrittname des übergeordneten Schritts des aktuellen Schritts.

Typ: Zeichenfolge

## parentTransitionID {#parenttransitionid-field}

Kennung der Transition, die die Instanz zum verarbeiteten Schritt geführt hat.

Typ: Zeichenfolge

## parentTransitionName {#parenttransitionname-field}

Name der Transition, die die Instanz zum verarbeiteten Schritt geführt hat.

Typ: Zeichenfolge

## inTest {#intest-field}

Gibt an, ob sich diese Journey im Testmodus befindet oder nicht.

Typ: boolean

## processingTime {#processingtime-field}

Gesamtdauer vom Eintritt des Instanzschritts bis zum Ende der Verarbeitung in Millisekunden.

Typ: long

## instanceType {#instancetype-field}

Gibt den Instanztyp an, ob es sich um einen Batch- oder einen Einzelfall handelt.

Typ: Zeichenfolge

Werte: batch/unitary

## recurrenceIndex {#recurrenceindex-field}

Index der Wiederholung, wenn es sich bei der Journey um eine Batch- und eine wiederkehrende Journey handelt (erste Ausführung hat recurrenceIndex = 1).

Typ: long

## isBatchToUnitary {#isbatchtounitary-field}

Gibt an, ob diese Einzelinstanz von einer Batch-Instanz ausgelöst wurde.

Typ: boolean

## batchExternalKey {#batchexternalkey-field}

Externer Schlüssel für Batch-Ereignis.

Typ: Zeichenfolge

## batchInstanceID {#batchinstanceid-field}

Dies ist die Kennung der Batch-Instanz.

Typ: Zeichenfolge

## batchUnitaryBranchID {#batchunitarybranchid-field}

Wenn die Instanz von einer Batch-Instanz ausgelöst wurde, die eindeutige Verzweigungs-ID.

Typ: Zeichenfolge
