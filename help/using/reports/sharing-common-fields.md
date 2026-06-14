---
solution: Journey Optimizer
product: journey optimizer
title: Gemeinsame Felder für journeySteps-Ereignisse
description: Gemeinsame Felder für journeySteps-Ereignisse
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 42aec986-2352-456a-a725-7f1585ae01f8
TQID: https://experienceleague.adobe.com/MWcV6FkgtiFJd9Y7q8CvTXQsL68cD5JcvqjmoEyiYhI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 659
ht-degree: 96%

---

# Gemeinsame Felder für journeySteps-Ereignisse {#sharing-common-fields}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Verweisen Sie auf die allgemeinen Journey-Schritt-Ereignisfelder, die Journey Optimizer für jeden auf einer Journey verarbeiteten Schritt an Adobe Experience Platform sendet.

>[!ENDSHADEBOX]

Diese Feldergruppe wird von den folgenden Ereignissen verwendet: **journeyStepEvent** und **journeyStepProfileEvent**.

Dies sind die gängigen XDM-Felder, die [!DNL Journey Optimizer] an Adobe Experience Platform sendet. Gemeinsame Felder werden für jeden Schritt gesendet, der während einer Journey verarbeitet wird. Für benutzerdefinierte Aktionen und Anreicherungen werden spezifischere Felder verwendet.

Einige dieser Felder sind nur in bestimmten Verarbeitungsmustern (Aktionsausführung, Datenabruf usw.) verfügbar, um die Größe von Ereignissen zu begrenzen.


>[!NOTE]
>
>Weitere Informationen über die Attribute von Journey-Eigenschaften finden Sie [in diesem Abschnitt](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## entrance {#entrance-field}

Gibt an, ob der Benutzer in die Journey eingetreten ist. Wenn nicht vorhanden, wird angenommen, dass der Wert „false“ lautet.

Typ: boolesch

Werte: wahr/falsch

## reentrance {#reentrance-field}

Gibt an, ob der Benutzer in die Journey mit derselben Instanz erneut eingetreten ist. Wenn nicht vorhanden, wird angenommen, dass der Wert „false“ lautet.

Typ: boolesch

Werte: wahr/falsch

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
* instanceTimedout: Der Schritt hat die Verarbeitung gestoppt, da die Instanz ihren Zeitüberschreitungswert erreicht hat.

## journeyID {#journeyid-field}

Kennung der Journey.

Typ: Zeichenfolge

## journeyVersionID {#journeyversionid-field}

Kennung der Journey-Version. Diese Kennung stellt bei journeyStepEvent den Identitätsverweis auf die Journey dar.

Typ: Zeichenfolge

>[!NOTE]
>
>Zur Fehlerbehebung empfehlen wir bei der Abfrage von Journeys die Verwendung von journeyVersionID anstelle von journeyVersionName.

## journeyVersionName {#journeyversionname-field}

Name der Journey-Version.

Typ: Zeichenfolge

>[!NOTE]
>
>Zur Fehlerbehebung empfehlen wir bei der Abfrage von Journeys die Verwendung von journeyVersionID anstelle von journeyVersionName.

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

## exitCriteriaID

ID der exitCriteria

Typ: Zeichenfolge

## exitCriteriaName

Name der exitCriteria

Typ: Zeichenfolge