---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei der Live-Journey-Ausführung
description: Informationen zum Beheben von Fehlern bei der Live-Journey-Ausführung
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Problembehebung, Fehlerbehebung, Journey, Überprüfen, Fehler
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
source-git-commit: e3b0bf6594e15f2d80d1e6782ec513c93f18c649
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 100%

---

# Fehlerbehebung bei der Live-Journey-Ausführung {#troubleshooting-execution}

In diesem Abschnitt erfahren Sie, wie Sie Fehler bei Journey-Ereignissen beheben und wie Sie prüfen, ob Profile in Ihre Journey eingetreten sind, wie sie diese durchlaufen und ob Nachrichten gesendet werden.

Sie können auch Fehler beheben, bevor Sie eine Journey testen oder veröffentlichen. [Auf dieser Seite](troubleshooting.md) erfahren Sie mehr dazu.

[Auf dieser Seite](troubleshooting-inbound.md) erfahren Sie, wie Sie Fehler bei eingehenden Aktionen beheben.

## Überprüfen, ob Ereignisse ordnungsgemäß gesendet werden {#checking-that-events-are-properly-sent}

Der Ausgangspunkt einer Journey ist stets ein Ereignis. Sie können mithilfe von Tools wie Postman Tests durchführen.

Sie können prüfen, ob der API-Aufruf, den Sie über diese Tools versenden, richtig gesendet wurde oder nicht. Wenn Sie einen Fehler erhalten, bedeutet das, dass es bei Ihrem Aufruf zu einem Fehler kommt. Überprüfen Sie erneut die Payload, die Kopfzeile (insbesondere die Organisations-ID) sowie die Ziel-URL. Sie können Ihren Administrator nach der richtigen URL fragen.

Ereignisse werden von der Quelle nicht direkt an Journeys weitergeleitet. Journeys benötigen dazu stattdessen die Streaming-Aufnahme-APIs von Adobe Experience Platform. Darum können Sie bei Problemen mit Ereignissen die Fehlerbehebung für Streaming-Aufnahme-APIs in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de){target="_blank"} nutzen.

Wenn Ihre Journey den Testmodus nicht aktivieren kann und dabei der Fehler `ERR_MODEL_RULES_16` ausgegeben wird, stellen Sie im Falle von Kanalaktionen sicher, dass das verwendete Ereignis einen [Identity-Namespace](../audience/get-started-identity.md) enthält.

Der Identity-Namespace dient dazu, die Testprofile eindeutig zu identifizieren. Wenn beispielsweise die E-Mail-Adresse zur Identifizierung der Testprofile verwendet wird, sollte der Identity-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identity-Namespace **Telefon** ausgewählt werden.

## Überprüfen, ob Personen in die Journey eintreten {#checking-if-people-enter-the-journey}

Berichte zu Journey messen den Eintritt von Personen in eine Journey auf Echtzeitbasis.

Wenn Sie das Ereignis erfolgreich versenden, aber keinen Eintritt in die Journey sehen können, bedeutet das, dass es zwischen dem Senden und Empfangen des Ereignisses in der Journey zu Problemen kommt.

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

Wenn Personen die Journey zwar richtig durchlaufen, aber nicht die vorgesehenen Nachrichten erhalten, können Sie Folgendes prüfen:

* [!DNL Journey Optimizer] hat die Anfrage zum Senden der Nachricht korrekt berücksichtigt. Ein Business-Anwender kann auf die zu sendende Nachricht zugreifen und prüfen, ob der Zeitpunkt der letzten Ausführung mit der Ausführungszeit Ihrer Journey übereinstimmt. Außerdem kann er die neuesten eingegangenen API-Aufrufe/-Ereignisse prüfen.
* [!DNL Journey Optimizer] hat die Nachricht erfolgreich gesendet. Überprüfen Sie die Journey-Berichte, um sicherzustellen, dass keine Fehler aufgetreten sind.

Bei einer Nachricht, die über eine benutzerdefinierte Aktion gesendet wird, kann während des Journey-Tests nur geprüft werden, ob der Systemaufruf der benutzerdefinierten Aktion zu einem Fehler führt oder nicht.  Wenn der Aufruf an das externe System, das mit der benutzerdefinierten Aktion verknüpft ist, nicht zu einem Fehler führt, aber auch nicht zum Senden der Nachricht, sollten Sie das externe System überprüfen.
