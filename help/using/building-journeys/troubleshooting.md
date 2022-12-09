---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei Journeys
description: Erfahren Sie, wie Sie Fehler in Journeys beheben können.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---

# Fehlerbehebung für Ihre Journey{#troubleshooting}

In diesem Abschnitt finden Sie Informationen zur Fehlerbehebung bei Journeys vor dem Testen oder Veröffentlichen. Alle unten aufgeführten Prüfungen können durchgeführt werden, wenn sich die Journey im Testmodus befindet oder wenn die Journey live ist. Es wird empfohlen, alle unten aufgeführten Prüfungen im Testmodus durchzuführen und dann mit der Veröffentlichung fortzufahren. Siehe [diese Seite](../building-journeys/testing-the-journey.md).

## Vor dem Testen auf Fehler prüfen{#checking-for-errors-before-testing}

Bevor Sie Ihre Journey testen und veröffentlichen, überprüfen Sie, ob alle Aktivitäten ordnungsgemäß konfiguriert sind. Sie können keine Tests oder Veröffentlichungen durchführen, wenn das System weiterhin Fehler erkennt.

Fehler werden mit einem Warnsymbol auf den Aktivitäten selbst auf der Arbeitsfläche angezeigt. Platzieren Sie den Cursor auf das Ausrufezeichen, um die Fehlermeldung anzuzeigen. Wenn Sie auf die Aktivität klicken, sollte die fehlerhafte Zeile mit einer Warnung angezeigt werden. Wenn beispielsweise ein Pflichtfeld leer ist, wird ein Fehler angezeigt.

![](assets/journey63.png)

Wenn beispielsweise auf der Arbeitsfläche zwei Aktivitäten getrennt werden, wird eine Warnung angezeigt.

![](assets/canvas-disconnected.png)

Neben dem **[!UICONTROL Test]** umschalten und **[!UICONTROL Publish]** -Schaltfläche, kann ein Warnzeichen angezeigt werden. Dieses Warnzeichen zeigt vom System erkannte Fehler an und verhindert die Aktivierung des Testmodus oder die Veröffentlichung der Journey. Meistens werden vom System erkannte Fehler mit in den Aktivitäten sichtbaren Fehlern verknüpft, manchmal aber mit anderen Problemen. In diesem Fall können Sie sie anzeigen und versuchen, das Problem anhand der Fehlerbeschreibung zu identifizieren. Wenn Sie das Problem nicht identifizieren können, können Sie die Details kopieren und an den Administrator oder den Support senden. Beachten Sie, dass Fehler, die den Test blockieren, und Fehler, die die Veröffentlichung blockieren, ähnlich sind.

Das System erkennt zwei Arten von Problemen: Fehler und Warnungen. Fehler blockieren die Veröffentlichung und Testaktivierung. Warnungen weisen auf potenzielle Probleme hin, die die Testaktivierung oder Veröffentlichung nicht blockieren. Sie sehen eine Beschreibung des Problems und eine Problem-Log-ID des Typs ERR_XXX_XXX. Dies hilft dem technischen Support bei der Identifizierung des Problems.

Auf dem Zeichen neben dem **[!UICONTROL Test]** umschalten und **[!UICONTROL Publish]** Schaltfläche. Bei Fehlern wird das Zeichen rot angezeigt. Bei Warnungen wird sie in orangefarbenem Format angezeigt.

![](assets/journey75.png)

Fehler und Warnungen, die für die Journey global sind, werden zuerst in der Liste angezeigt. Fehler und Warnungen im Zusammenhang mit bestimmten Aktivitäten werden nach, nach der Aktivitätsreihenfolge oder dem Auftreten in der Journey von links nach rechts aufgelistet. Die **[!UICONTROL Copy details]** button kopiert technische Informationen über die Journey, die das Supportteam zur Fehlerbehebung verwenden kann.

Wenn in einer Aktion oder Bedingung ein Fehler auftritt, stoppt die Journey eines Kontakts. Die einzige Möglichkeit, den Vorgang fortzusetzen, besteht darin, das Kontrollkästchen zu aktivieren **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Siehe [diesem Abschnitt](../building-journeys/using-the-journey-designer.md#paths).

## Überprüfen, ob Ereignisse ordnungsgemäß gesendet werden{#checking-that-events-are-properly-sent}

Der Ausgangspunkt einer Journey ist immer ein Ereignis. Sie können Tests mit Tools wie Postman durchführen.

Sie können überprüfen, ob der API-Aufruf, den Sie über diese Tools senden, korrekt gesendet wurde oder nicht. Wenn Sie einen Fehler zurückerhalten, bedeutet dies, dass Ihr Aufruf ein Problem aufweist. Überprüfen Sie erneut die Payload, den Header (und insbesondere die Organisations-ID) und die Ziel-URL. Sie können Ihren Administrator nach der richtigen URL fragen.

Ereignisse werden nicht direkt von der Quelle an Journeys gesendet. Journeys basieren auf den Streaming-Aufnahme-APIs von Adobe Experience Platform. Im Falle von Problemen mit Ereignissen können Sie daher auf [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;} zur Fehlerbehebung bei Streaming-Aufnahme-APIs.

## Überprüfen, ob Personen in die Journey eintreten{#checking-if-people-enter-the-journey}

Die Journey-Berichterstellung misst den Eintritt von Personen in eine Journey in Echtzeit.

Wenn Sie das Ereignis erfolgreich senden, aber keinen Eintritt in die Journey sehen, bedeutet dies, dass zwischen dem Senden des Ereignisses und dem Empfang des Ereignisses in der Journey etwas schiefgeht.

Im Folgenden finden Sie einige Punkte, die der Administrator überprüfen sollte:

* Sind Sie sicher, dass sich die Journey, bei der Sie das eingehende Ereignis erwarten, im Testmodus befindet oder live ist?
* Haben Sie Ihr Ereignis gespeichert, bevor Sie die Payload aus der Payload-Vorschau kopiert haben?
* Enthält Ihre Ereignis-Payload eine Ereignis-ID?
* Haben Sie die richtige URL erreicht?
* Haben Sie die Payload-Struktur der Streaming-Aufnahme-APIs mithilfe der Payload-Strukturvorschau im Ereigniskonfigurationsbereich befolgt? Siehe [diese Seite](../event/about-creating.md#preview-the-payload).
* Haben Sie die richtigen Schlüssel-Wert-Paare in der Kopfzeile Ihres Ereignisses verwendet?

   ```
   X-gw-ims-org-id - your organization's ID
   Content-type - application/json
   ```

## Überprüfen, wie Benutzer durch die Journey navigieren{#checking-how-people-navigate-through-the-journey}

Die Journey-Berichterstellung misst den Fortschritt von Kontakten innerhalb einer Journey. Es ist einfach zu erkennen, wo und warum eine Person gestoppt wurde.

Im Folgenden finden Sie einige zu prüfende Punkte:

* Ist dies auf eine Bedingung zurückzuführen, die die Person ausschließt? Beispielsweise lautet die Bedingung &quot;Geschlecht = männlich&quot;und die Person eine Frau. Diese Prüfung kann von einem Business-Anwender durchgeführt werden, wenn die Bedingung nicht zu komplex ist.
* Ist dies auf einen Aufruf an eine Datenquelle zurückzuführen, der nicht reagiert? Wenn die Journey im Test ist, können diese Informationen in Testmodusprotokollen angezeigt werden. Wenn die Journey live ist, kann ein Administrator direkte Aufrufe an die Datenquelle testen und die erhaltene Antwort überprüfen. Ein Administrator kann die Journey auch duplizieren und testen.

## Überprüfen, ob Nachrichten erfolgreich gesendet wurden{#checking-that-messages-are-sent-successfully}

Wenn Kontakte den richtigen Weg in der Journey gehen, aber keine Nachrichten erhalten, die sie erhalten sollten, können Sie überprüfen, ob:

* [!DNL Journey Optimizer] hat die Anfrage zum Senden der Nachricht korrekt berücksichtigt. Geschäftsbenutzer können auf die Nachricht zugreifen, die gesendet werden soll, und überprüfen, ob der Zeitpunkt der letzten Ausführung mit der Ausführungszeit Ihrer Journey übereinstimmt. Sie können auch die neuesten API-Aufrufe/Ereignisse überprüfen, die empfangen wurden.
* [!DNL Journey Optimizer] hat die Nachricht erfolgreich gesendet. Überprüfen Sie die Journey-Berichte, um sicherzustellen, dass keine Fehler auftreten.

Bei einer über eine benutzerdefinierte Aktion gesendeten Nachricht kann während des Journey-Tests nur geprüft werden, ob der Aufruf des Systems der benutzerdefinierten Aktion zu einem Fehler führt oder nicht. Wenn der Aufruf an das mit der benutzerdefinierten Aktion verknüpfte externe System nicht zu einem Fehler führt, aber nicht zum Senden einer Nachricht führt, sollten einige Untersuchungen auf der Seite des externen Systems durchgeführt werden.
