---
title: Gemeinsame Felder für journeyStep-Ereignisse
description: Wegeysteps Ereignisse gemeinsame Felder
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Gemeinsame Felder für journeyStep-Ereignisse {#sharing-common-fields}

![](../assets/do-not-localize/badge.png)

Dieses Mixin wird von journeyStepEvent und journeyStepProfileEvent geteilt.

Dies sind die gängigen XDM-Felder, die [!DNL Journey Optimizer] an Adobe Experience Platform sendet. Gemeinsame Felder werden für jeden Schritt gesendet, der während einer Journey verarbeitet wird. Für benutzerdefinierte Aktionen und Anreicherungen werden spezifischere Felder verwendet.

Einige dieser Felder sind nur bei bestimmten Verarbeitungsmustern verfügbar (Aktionsausführung, Datenabruf usw.), um die Größe von Ereignissen zu begrenzen.

## entrance

Gibt an, ob der Benutzer in die Journey eingetreten ist. Wenn nicht vorhanden, wird angenommen, dass der Wert „false“ lautet.

Typ: boolesch

Werte: true/false

## reentrance

Gibt an, ob der Benutzer in die Journey mit derselben Instanz erneut eingetreten ist. Ist der Wert nicht vorhanden, wird angenommen, dass er &quot;false&quot;ist.

Typ: boolean

Werte: true/false

## instanceEnded

Gibt an, ob die Instanz beendet wurde (erfolgreich oder nicht).

Typ: boolean

## eventID

Ereigniskennung in der Verarbeitung für die Schrittverarbeitung. Wenn es sich bei dem Ereignis um ein externes Ereignis handelt, ist der Wert dessen Ereignis-ID eventId. Wenn es sich bei dem Ereignis um ein internes Ereignis handelt, ist der Wert die interne eventId (wie z. B. scheduledNotificationReceived, executedAction).

Typ: Zeichenfolge

## nodeID

Kennung des Client-Knotens (von der Arbeitsfläche).

Typ: string

## stepID

Eindeutige Kennung des Schritts, der gerade verarbeitet wird.

Typ: string

## stepName

Name des Schritts, der derzeit verarbeitet wird.

Typ: string

## stepType

Art des Schritts.

Typ: string

Mögliche Werte:

* Bedingung
* Aktion
* Planung
* Timer

## stepStatus

Status des Schritts, der den Status des Schritts darstellt, nachdem die Verarbeitung abgeschlossen (und das Schrittereignis ausgelöst) wurde.

Typ: string

Der Status kann folgendermaßen lauten:

* ended: Der Schritt weist keine Transition auf und seine Verarbeitung wurde erfolgreich beendet.
* error: Bei der Schrittverarbeitung ist ein Fehler aufgetreten.
* transitions: Der Schritt wartet darauf, bis ein Ereignis durch Transition in einen anderen Schritt gelangt.
* capped: Der Schritt ist aufgrund eines Begrenzungsfehlers fehlgeschlagen, der während einer Aktion oder Anreicherung ausgelöst wurde.
* timedout: der Schritt bei einem Timeout-Fehler, der während einer Aktion oder Anreicherung ausgelöst wurde, fehlgeschlagen ist.
* instanceTimedout: Der Schritt hat die Verarbeitung beendet, da die Instanz ihren Zeitüberschreitungswert erreicht hat.

## journeyID

Kennung der Journey.

Typ: string

## journeyVersionID

ID der Journey. Diese Kennung stellt bei journeyStepEvent den Identitätsverweis auf die Journey dar.

Typ: string

## journeyVersionName

Name der Journey-Version.

Typ: string

## journeyVersion

Version der Journey.

Typ: string

## instanceID

Interne Kennung der Journey-Instanz.

Typ: string

## externalKey

Externer Schlüssel, der aus dem Ereignis zur Verarbeitung extrahiert wurde.

Typ: string

## parentStepID

Kennung des übergeordneten Schritts des in der Instanz gerade verarbeiteten Schritts.

Typ: string

## parentStepName

Name des übergeordneten Schritts des aktuellen Schritts.

Typ: string

## parentTransitionID

Kennung der Transition, die die Instanz zum verarbeiteten Schritt geführt hat.

Typ: string

## parentTransitionName

Name der Transition, die die Instanz zum verarbeiteten Schritt gebracht hat.

Typ: string

## inTest

Gibt an, ob sich die Journey im Testmodus befindet oder nicht.

Typ: boolean

## processingTime

Gesamtdauer vom Eintritt des Instanzschritts bis zum Ende der Verarbeitung (in Millisekunden).

Typ: lang

## instanceType

Gibt den Instanztyp an (Batch oder unitär).

Typ: string

Werte: batch/unitary

## recurrenceIndex

Index des Intervalls, wenn es sich bei der Journey um einen wiederkehrenden Batch-Vorgang handelt (erste Ausführung führt zu recurrenceIndex = 1).

Typ: long

## isBatchToUnitary

Gibt an, ob diese unitäre Instanz von einer Batch-Instanz ausgelöst wurde.

Typ: boolean

## batchExternalKey

Externer Schlüssel für das Batch-Ereignis.

Typ: string

## batchInstanceID

Dies ist die Kennung der Batch-Instanz.

Typ: string

## batchUnitaryBranchID

Wenn die Instanz von einer Batch-Instanz ausgelöst wurde, unitäre Verzweigungs-ID.

Typ: string
