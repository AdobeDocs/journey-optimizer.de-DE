---
solution: Journey Optimizer
product: journey optimizer
title: Gemeinsame Felder für journeySteps-Ereignisse
description: Gemeinsame Felder für journeySteps-Ereignisse
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gemeinsame Felder für journeySteps-Ereignisse {#sharing-common-fields}

Diese Feldergruppe wird sowohl von journeyStepEvent als auch journeyStepProfileEvent verwendet.

Dies sind die gängigen XDM-Felder, die [!DNL Journey Optimizer] an Adobe Experience Platform sendet. Gemeinsame Felder werden für jeden Schritt gesendet, der während einer Journey verarbeitet wird. Für benutzerdefinierte Aktionen und Anreicherungen werden spezifischere Felder verwendet.

Einige dieser Felder sind nur bei bestimmten Verarbeitungsmustern verfügbar (Aktionsausführung, Datenabruf usw.), um die Größe von Ereignissen zu begrenzen.

## entrance {#entrance-field}

Gibt an, ob der Benutzer in die Journey eingetreten ist. Wenn nicht vorhanden, wird angenommen, dass der Wert „false“ lautet.

Typ: boolesch

Werte: true/false

## reentrance {#reentrance-field}

Gibt an, ob der Benutzer in die Journey mit derselben Instanz erneut eingetreten ist. Wenn nicht vorhanden, wird angenommen, dass der Wert „false“ lautet.

Typ: boolesch

Werte: true/false

## instanceEnded {#instance-ended-field}

Gibt an, ob die Instanz beendet wurde (erfolgreich oder nicht).

Typ: boolesch

## eventID {#eventid-field}

Ereigniskennung in der Verarbeitung für die Schrittverarbeitung. Wenn es sich bei dem Ereignis um ein externes Ereignis handelt, ist der Wert dessen Ereignis-ID eventId. Wenn es sich bei dem Ereignis um ein internes Ereignis handelt, ist der Wert die interne eventId (wie z. B. scheduledNotificationReceived, executedAction).

Typ: Zeichenfolge

## nodeID {#nodeid-field}

Kennung des Client-Knotens (von der Arbeitsfläche).

Typ: Zeichenfolge

## stepID {#stepdid-field}

Eindeutige Kennung des Schritts, der gerade verarbeitet wird.

Typ: Zeichenfolge

## stepName {#stepname-field}

Name des Schritts, der gerade verarbeitet wird.

Typ: Zeichenfolge

## stepType {#steptype-field}

Art des Schritts.

Typ: Zeichenfolge

Mögliche Werte:

* Bedingung
* Aktion
* Planung
* Timer

## stepStatus {#stepstatus-field}

Status des Schritts, der den Status des Schritts darstellt, nachdem die Verarbeitung abgeschlossen (und das Schrittereignis ausgelöst) wurde.

Typ: Zeichenfolge

Der Status kann wie folgt lauten:

* ended: Der Schritt weist keine Transition auf und seine Verarbeitung wurde erfolgreich beendet.
* error: Bei der Schrittverarbeitung ist ein Fehler aufgetreten.
* transitions: Der Schritt wartet darauf, bis ein Ereignis durch Transition in einen anderen Schritt gelangt.
* capped: Der Schritt ist aufgrund eines Begrenzungsfehlers fehlgeschlagen, der während einer Aktion oder Anreicherung ausgelöst wurde.
* timedout: Der Schritt ist aufgrund eines Zeitüberschreitungsfehlers fehlgeschlagen, der während einer Aktion oder Anreicherung ausgelöst wurde.
* instanceTimedout: Der Schritt hat die Verarbeitung beendet, da die Instanz ihren Zeitüberschreitungswert erreicht hat.

## journeyID {#journeyid-field}

Kennung der Journey.

Typ: Zeichenfolge

## journeyVersionID {#journeyversionid-field}

Kennung der Journey-Version. Diese Kennung stellt bei journeyStepEvent den Identitätsverweis auf die Journey dar.

Typ: Zeichenfolge

>[!NOTE]
>
>Zur Fehlerbehebung empfehlen wir bei der Abfrage von Journey die Verwendung von journeyVersionID anstelle von journeyVersionName .

## journeyVersionName {#journeyversionname-field}

Name der Journey-Version.

Typ: Zeichenfolge

>[!NOTE]
>
>Zur Fehlerbehebung empfehlen wir bei der Abfrage von Journey die Verwendung von journeyVersionID anstelle von journeyVersionName .

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

Kennung des übergeordneten Schritts des in der Instanz gerade verarbeiteten Schritts.

Typ: Zeichenfolge

## parentStepName {#parentstepname-field}

Name des übergeordneten Schritts des aktuellen Schritts.

Typ: Zeichenfolge

## parentTransitionID {#parenttransitionid-field}

Kennung der Transition, die die Instanz zum verarbeiteten Schritt geführt hat.

Typ: Zeichenfolge

## parentTransitionName {#parenttransitionname-field}

Name der Transition, die die Instanz zum verarbeiteten Schritt geführt hat.

Typ: Zeichenfolge

## inTest {#intest-field}

Gibt an, ob sich die Journey im Testmodus befindet oder nicht.

Typ: boolesch

## processingTime {#processingtime-field}

Gesamtdauer vom Eintritt des Instanzschritts bis zum Ende der Verarbeitung (in Millisekunden).

Typ: lang

## instanceType {#instancetype-field}

Gibt den Instanztyp an (Batch oder unitär).

Typ: Zeichenfolge

Werte: batch/unitary

## recurrenceIndex {#recurrenceindex-field}

Index des Intervalls, wenn es sich bei der Journey um einen wiederkehrenden Batch-Vorgang handelt (erste Ausführung führt zu recurrenceIndex = 1).

Typ: lang

## isBatchToUnitary {#isbatchtounitary-field}

Gibt an, ob diese unitäre Instanz von einer Batch-Instanz ausgelöst wurde.

Typ: boolesch

## batchExternalKey {#batchexternalkey-field}

Externer Schlüssel für das Batch-Ereignis.

Typ: Zeichenfolge

## batchInstanceID {#batchinstanceid-field}

Dies ist die Kennung der Batch-Instanz.

Typ: Zeichenfolge

## batchUnitaryBranchID {#batchunitarybranchid-field}

Wenn die Instanz von einer Batch-Instanz ausgelöst wurde, unitäre Verzweigungs-ID.

Typ: Zeichenfolge
