---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei der Live-Journey-Ausführung
description: Erfahren Sie, wie Sie Fehler bei der Live-Journey-Ausführung beheben können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Problembehebung, Fehlerbehebung, Journey, Überprüfen, Fehler
source-git-commit: 61498b61f7f05e0553fe575c980fd1bee08500a3
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 78%

---

# Fehlerbehebung bei der Live-Journey-Ausführung {#troubleshooting-execution}

In diesem Abschnitt erfahren Sie, wie Sie Probleme beim Journey von Ereignissen beheben, prüfen, ob Profile auf Ihre Journey gelangt sind, wie sie darin navigieren und ob Nachrichten gesendet werden.

Sie können auch Fehler beheben, bevor Sie eine Journey testen oder veröffentlichen. Erfahren Sie mehr [auf dieser Seite](troubleshooting.md).

Wenn Sie eingehende Aktionen verwenden, erfahren Sie auf [ Seite ](troubleshooting-inbound.md), wie Sie diese beheben können.

## Überprüfen, ob Ereignisse ordnungsgemäß gesendet werden {#checking-that-events-are-properly-sent}

Der Ausgangspunkt einer Journey ist stets ein Ereignis. Sie können mithilfe von Tools wie Postman Tests durchführen.

Sie können prüfen, ob der API-Aufruf, den Sie über diese Tools versenden, richtig gesendet wurde oder nicht. Wenn Sie einen Fehler erhalten, bedeutet das, dass es bei Ihrem Aufruf zu einem Fehler kommt. Überprüfen Sie erneut die Payload, die Kopfzeile (insbesondere die Organisations-ID) sowie die Ziel-URL. Sie können Ihren Administrator nach der richtigen URL fragen.

Ereignisse werden von der Quelle nicht direkt an Journeys weitergeleitet. Journeys benötigen dazu stattdessen die Streaming-Aufnahme-APIs von Adobe Experience Platform. Darum können Sie bei Problemen mit Ereignissen die Fehlerbehebung für Streaming-Aufnahme-APIs in der [Dokumentation ](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de){target="_blank"} Adobe Experience Platform aufrufen.

Wenn Ihre Journey den Testmodus nicht aktivieren kann und dabei der Fehler `ERR_MODEL_RULES_16` ausgegeben wird, stellen Sie im Falle von Kanalaktionen sicher, dass das verwendete Ereignis einen [Identity-Namespace](../audience/get-started-identity.md) enthält.

Der Identity-Namespace dient dazu, die Testprofile eindeutig zu identifizieren. Wenn beispielsweise die E-Mail-Adresse zur Identifizierung der Testprofile verwendet wird, sollte der Identity-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identity-Namespace **Telefon** ausgewählt werden.

## Überprüfen, ob Personen in die Journey eintreten {#checking-if-people-enter-the-journey}

Berichte zu Journey messen den Eintritt von Personen in eine Journey auf Echtzeitbasis.

Wenn Sie das Ereignis erfolgreich versenden, aber keinen Eintritt auf der Journey sehen, bedeutet dies, dass zwischen dem Ereignisversand und dem Ereignisempfang auf der Journey etwas schief läuft.

Sie können die Fehlerbehebung mit den folgenden Fragen beginnen:

* Sind Sie sicher, dass sich die Journey, bei der Sie das eingehende Ereignis erwarten, im Testmodus befindet oder live ist?
* Haben Sie das Ereignis gespeichert, bevor Sie die Payload aus der Payload-Vorschau kopiert haben?
* Enthält die Payload des Ereignisses eine Ereignis-ID?
* Haben Sie die richtige URL aufgerufen?
* Haben Sie die Payload-Struktur der Streaming-Aufnahme-APIs mithilfe der Payload-Strukturvorschau im Ereigniskonfigurationsbereich beachtet? Weitere Informationen finden Sie auf [dieser Seite](../event/about-creating.md#preview-the-payload).
* Haben Sie im Header Ihres Ereignisses die richtigen Schlüssel-Wert-Paare verwendet?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## Überprüfen, wie Personen durch die Journey navigieren {#checking-how-people-navigate-through-the-journey}

Berichte zu Journey messen den Fortschritt von Kontakten innerhalb einer Journey. So können Sie leicht ermitteln, wo und warum eine Person gestoppt wurde.

Prüfen Sie folgende Punkte:

* Ist das Problem auf eine Bedingung zurückzuführen, mit der die Person ausgeschlossen wird? Beispiel: Die Bedingung lautet „Geschlecht = männlich“, während die Person eine Frau ist. Die Prüfung kann von einem Business-Anwender vorgenommen werden, solange die Bedingung nicht zu komplex ist.
* Ist das Problem auf einen Aufruf einer Datenquelle zurückzuführen, die nicht reagiert? Wenn sich die Journey im Test befindet, können diese Informationen in Testmodusprotokollen angezeigt werden. Wenn die Journey live ist, kann ein Administrator direkte Aufrufe an die Datenquelle testen und die erhaltene Antwort überprüfen. Alternativ kann ein Administrator die Journey duplizieren und dann testen.

## Überprüfen, ob Nachrichten erfolgreich gesendet werden {#checking-that-messages-are-sent-successfully}

Wenn Personen zwar den richtigen Weg zum Journey gehen, aber keine Nachrichten erhalten, die sie erhalten sollten, können Sie Folgendes überprüfen:

* [!DNL Journey Optimizer] hat die Anfrage zum Senden der Nachricht korrekt berücksichtigt. Ein Business-Anwender kann auf die zu sendende Nachricht zugreifen und prüfen, ob der Zeitpunkt der letzten Ausführung mit der Ausführungszeit Ihrer Journey übereinstimmt. Außerdem kann er die neuesten eingegangenen API-Aufrufe/-Ereignisse prüfen.
* [!DNL Journey Optimizer] hat die Nachricht erfolgreich gesendet. Überprüfen Sie die Journey-Berichte, um sicherzustellen, dass keine Fehler aufgetreten sind.

Bei einer Nachricht, die über eine benutzerdefinierte Aktion gesendet wird, kann während des Journey-Tests nur geprüft werden, ob der Systemaufruf der benutzerdefinierten Aktion zu einem Fehler führt oder nicht.  Wenn der Aufruf an das externe System, das mit der benutzerdefinierten Aktion verknüpft ist, nicht zu einem Fehler führt, aber auch nicht zum Senden der Nachricht, sollten Sie das externe System überprüfen.
