---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei Journeys
description: Erfahren Sie, wie Sie Probleme bei Journey beheben können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Problembehebung, Fehlerbehebung, Journey, Überprüfen, Fehler
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: e47c95ac8981356bcfb742105cbf1faa5d53c189
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 96%

---

# Beheben von Fehlern in einer Journey {#troubleshooting}

In diesem Abschnitt erfahren Sie, wie Sie Probleme bei Journeys vor dem Testen oder Veröffentlichen beheben können.  Alle unten aufgeführten Prüfungen können durchgeführt werden, wenn sich die Journey im Testmodus befindet oder live ist. Wir empfehlen, alle unten aufgeführten Prüfungen im Testmodus vorzunehmen und dann mit der Veröffentlichung fortzufahren. Weitere Informationen zum Testmodus finden Sie auf [dieser Seite](../building-journeys/testing-the-journey.md).

Als Admin können Sie Ihre benutzerdefinierten Aktionskonfigurationen auch testen, indem Sie echte API-Aufrufe direkt über die Benutzeroberfläche durchführen. Weiterführende Informationen finden Sie auf [dieser Seite](../action/troubleshoot-custom-action.md).

## Fehlersuche vor dem Testen {#checking-for-errors-before-testing}

Überprüfen Sie vor dem Testen und Veröffentlichen Ihrer Journey, ob alle Aktivitäten ordnungsgemäß konfiguriert sind. Es können keine Tests oder Veröffentlichungen vorgenommen werden, solange das System noch Fehler findet.


### Fehler in Aktivitäten {#activity-errors}

Fehler werden in der Arbeitsfläche mit einem Warnsymbol auf den Aktivitäten selbst angezeigt. Platzieren Sie den Cursor auf dem Ausrufezeichen, um die entsprechende Fehlermeldung anzuzeigen. Wenn Sie auf die Aktivität klicken, sollte die fehlerhafte Zeile mit einer Warnung angezeigt werden. Zum Beispiel:

* wird ein Fehler angezeigt, wenn ein Pflichtfeld leer ist.

  ![](assets/journey63.png)

* Wenn zwei Aktivitäten auf der Arbeitsfläche getrennt werden, wird eine Warnung angezeigt.

  ![](assets/canvas-disconnected.png)

### Fehler in der Journey {#canvas-errors}

Fehler werden auch über die Schaltfläche **[!UICONTROL Warnungen]** oberhalb der Arbeitsfläche angezeigt. Über diese Schaltfläche können Sie Fehler anzeigen, die vom System erkannt wurden und die Aktivierung des Testmodus oder die Veröffentlichung der Journey verhindern.

Das System erkennt zwei Arten von Problemen: **Fehler** und **Warnungen**. Fehler blockieren die Veröffentlichung und Testaktivierung. Warnungen weisen auf mögliche Probleme hin, blockieren aber nicht die Testaktivierung oder Veröffentlichung. Angezeigt werden eine Beschreibung des Problems sowie eine Problem-Protokoll-ID vom Typ ERR_XXX_XXX. Dies kann dazu beitragen, das Problem zu identifizieren.

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Fehler und Warnungen, die die gesamte Journey betreffen, werden in der Liste zuerst aufgeführt. Fehler und Warnungen, die einzelne Aktivitäten betreffen, werden danach aufgeführt (anhand der Aktivitätsreihenfolge oder des Auftretens in der Journey von links nach rechts). Unten in der Liste der Warnungen können Sie über die Schaltfläche **[!UICONTROL Details kopieren]** technische Informationen über die Journey kopieren, die zur Fehlerbehebung nützlich sind.

### Hinzufügen eines alternativen Pfads {#canvas-add-path}

Für den Fall eines Fehlers können Sie eine Ausweichaktion für die folgenden Journey-Aktivitäten definieren: **[!UICONTROL Bedingung]** und **[!UICONTROL Aktion]**.

Wenn in einer Aktion oder einer Bedingung ein Fehler auftritt, wird die Journey des Kontakts gestoppt. Die einzige Möglichkeit zur Fortsetzung der Journey besteht in der Behebung des Problems. Um eine Unterbrechung der Journey zu vermeiden, können Sie auch die Option **[!UICONTROL Alternativen Pfad hinzufügen, falls eine Zeitüberschreitung oder ein Fehler auftritt]** in den Eigenschaften der Aktivität aktivieren. Weiterführende Informationen finden Sie in [diesem Abschnitt](../building-journeys/using-the-journey-designer.md#paths).


## Überprüfen, ob Ereignisse ordnungsgemäß gesendet werden {#checking-that-events-are-properly-sent}

Der Ausgangspunkt einer Journey ist stets ein Ereignis. Sie können mithilfe von Tools wie Postman Tests durchführen.

Sie können prüfen, ob der API-Aufruf, den Sie über diese Tools versenden, richtig gesendet wurde oder nicht. Wenn Sie einen Fehler erhalten, bedeutet das, dass es bei Ihrem Aufruf zu einem Fehler kommt. Überprüfen Sie erneut die Payload, die Kopfzeile (insbesondere die Organisations-ID) sowie die Ziel-URL. Sie können Ihren Administrator nach der richtigen URL fragen.

Ereignisse werden von der Quelle nicht direkt an Journeys weitergeleitet. Journeys benötigen dazu stattdessen die Streaming-Aufnahme-APIs von Adobe Experience Platform. Darum können Sie bei Problemen mit Ereignissen die Fehlerbehebung für Streaming-Aufnahme-APIs in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=de){target="_blank"} nutzen.

## Überprüfen, ob Personen in die Journey eintreten {#checking-if-people-enter-the-journey}

Berichte zu Journey messen den Eintritt von Personen in eine Journey auf Echtzeitbasis.

Wenn Sie das Ereignis erfolgreich versenden, aber keinen Eintritt in die Journey erkennen können, bedeutet das, dass es zwischen dem Senden und Empfangen des Ereignisses in der Journey zu Problemen kommt.

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

Wenn Personen zwar der Journey folgen, aber nicht die vorgesehen Nachrichten erhalten, können Sie Folgendes prüfen:

* [!DNL Journey Optimizer] hat die Anfrage zum Senden der Nachricht korrekt berücksichtigt. Ein Business-Anwender kann auf die zu sendende Nachricht zugreifen und prüfen, ob der Zeitpunkt der letzten Ausführung mit der Ausführungszeit Ihrer Journey übereinstimmt. Außerdem kann er die neuesten eingegangenen API-Aufrufe/-Ereignisse prüfen.
* [!DNL Journey Optimizer] hat die Nachricht erfolgreich gesendet. Überprüfen Sie die Journey-Berichte, um sicherzustellen, dass keine Fehler aufgetreten sind.

Bei einer Nachricht, die über eine benutzerdefinierte Aktion gesendet wird, kann während des Journey-Tests nur geprüft werden, ob der Systemaufruf der benutzerdefinierten Aktion zu einem Fehler führt oder nicht.  Wenn der Aufruf an das externe System, das mit der benutzerdefinierten Aktion verknüpft ist, nicht zu einem Fehler führt, aber auch nicht zum Senden der Nachricht, sollten Sie das externe System überprüfen.
