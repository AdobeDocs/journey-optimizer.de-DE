---
title: Anwendungsfälle für Journeys
description: Anwendungsfälle für Journeys
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
source-git-commit: 8a68d1e6d498ef3055c703d4e73471ab6d7bff40
workflow-type: ht
source-wordcount: '857'
ht-degree: 100%

---

# Anwendungsfall: Senden von Multi-Channel-Nachrichten{#send-multi-channel-messages}

In diesem Abschnitt wird ein Anwendungsfall vorgestellt, der „Segment lesen“, ein Ereignis, Reaktionsereignisse und E-Mail-/Push-Nachrichten kombiniert.

![](assets/jo-uc1.png)

## Beschreibung des Anwendungsfalls

Bei diesem Anwendungsfall möchten wir eine erste Nachricht (E-Mail und Push) an alle Kunden senden, die zu einem bestimmten Segment gehören.

Abhängig von ihrer jeweiligen Reaktion auf die erste Nachricht möchten wir spezifische Nachrichten senden.

Nach der ersten Nachricht warten wir einen Tag lang, bis Kunden die Push- oder E-Mail-Nachricht öffnen. Wenn keine Reaktion erfolgt, senden wir eine Follow-up-E-Mail.

Dann warten wir auf einen Kauf und senden eine Push-Nachricht, um dem Kunden zu danken.

## Voraussetzungen 

Damit dieser Anwendungsfall funktioniert, müssen Sie Folgendes konfigurieren:

* Ein Segment für alle Kunden, die in Atlanta, San Francisco oder Seattle leben und nach 1980 geboren wurden
* Ein Ereignis
* Drei Nachrichten

### Erstellen des Segments

In unserer Journey möchten wir ein bestimmtes Kundensegment verwenden. Alle diesem Segment angehörenden Einzelpersonen treten in die Journey ein und folgen den verschiedenen Schritten. In unserem Beispiel benötigen wir ein Segment, das alle Kunden enthält, die in Atlanta, San Francisco oder Seattle leben und nach 1980 geboren wurden.

Weiterführende Informationen zu Segmenten finden Sie auf dieser [Seite](../segment/about-segments.md).

1. Wählen Sie im Menüabschnitt KUNDE die Option **[!UICONTROL Segmente]** aus.

1. Klicken Sie oben rechts in der Segmentliste auf den Button **[!UICONTROL Segment erstellen]**.

1. Geben Sie im Bereich **[!UICONTROL Segmenteigenschaften]** einen Namen für das Segment ein.

1. Ziehen Sie die gewünschten Felder aus dem linken Bereich in den mittleren Arbeitsbereich und konfigurieren Sie die Felder dann entsprechend Ihren Anforderungen. In diesem Beispiel verwenden wir die Attributfelder **Stadt** und **Geburtsjahr**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/add-attributes.png)

Das Segment ist jetzt erstellt und kann in Ihrer Journey verwendet werden. Mit der Aktivität **Segment lesen** können Sie alle Einzelpersonen des Segments in die Journey eintreten lassen.

### Konfigurieren des Ereignisses

Sie müssen ein Ereignis konfigurieren, das an Ihre Journey gesendet wird, wenn ein Kunde einen Kauf tätigt. Wenn die Journey das Ereignis erhält, wird die Nachricht „Vielen Dank“ verschickt.

Für diesen Zweck verwenden wir ein regelbasiertes Ereignis. Weiterführende Informationen zu Ereignissen finden Sie auf dieser [Seite](../event/about-events.md).

1. Wählen Sie im Menüabschnitt ADMINISTRATION die Option **[!UICONTROL Konfigurationen]** und klicken Sie dann auf **[!UICONTROL Ereignisse]**. Klicken Sie auf **[!UICONTROL Ereignis erstellen]**, um ein neues Ereignis zu erstellen.

1. Geben Sie den Namen Ihres Ereignisses ein.

1. Wählen Sie im Feld **[!UICONTROL Ereignis-ID-Typ]** die Option **[!UICONTROL Regelbasiert]** aus.

1. Definieren Sie die Felder **[!UICONTROL Schema]** und **[!UICONTROL Payload]**. Sie können mehrere Felder verwenden, beispielsweise das erworbene Produkt, das Kaufdatum und die Kauf-ID.

1. Definieren Sie im Feld **[!UICONTROL Ereignis-ID-Bedingung]** die vom System verwendete Bedingung, um die Ereignisse zu identifizieren, die einen Trigger an Ihre Journey übermitteln. Sie können beispielsweise ein Feld `purchaseMessage` hinzufügen und die folgende Regel definieren: `purchaseMessage="thank you"`

1. Definieren Sie den **[!UICONTROL Namespace]** und die **[!UICONTROL Profilkennung]**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/jo-uc2.png)

Das Ereignis ist jetzt konfiguriert und kann in Ihrer Journey verwendet werden. Mit der entsprechenden Ereignisaktivität können Sie eine Aktion jedes Mal auslösen, wenn ein Kunde einen Einkauf tätigt.

### Erstellen der Nachrichten

Für diesen Anwendungsfall müssen wir drei Nachrichten erstellen:

* Eine erste Push- und E-Mail-Nachricht
* Eine Push-Nachricht „Vielen Dank“
* Eine E-Mail-Folgenachricht

![](assets/jo-uc3.png)

In diesem [Abschnitt](../segment/about-segments.md) erfahren Sie, wie Sie diese Nachrichten entwerfen und veröffentlichen.

## Entwerfen der Journey

1. Beginnen Sie die Journey mit einer Aktivität vom Typ **Segment lesen**. Wählen Sie das zuvor erstellte Segment aus. Alle dem Segment angehörenden Einzelpersonen treten in die Journey ein.

   ![](assets/jo-uc4.png)

1. Fügen Sie per Drag-and-Drop eine Aktivität vom Typ **Nachricht** ein und wählen Sie die erste Push- und E-Mail-Nachricht aus. Diese Nachricht wird an alle Personen in der Journey gesendet.

   ![](assets/jo-uc5.png)

1. Platzieren Sie den Cursor auf der Nachrichten-Aktivität und klicken Sie auf das Pluszeichen „+“, um einen neuen Pfad zu erstellen.

1. Fügen Sie im ersten Pfad ein Ereignis **Reaktion** hinzu und wählen Sie **Push-Benachrichtigung geöffnet**. Das Ereignis wird ausgelöst, sobald ein zum Segment gehörender Kontaktdie Push-Version der ersten Nachricht öffnet.

1. Fügen Sie im zweiten Pfad ein Ereignis vom Typ **Reaktion** hinzu und wählen Sie **E-Mail geöffnet**. Das Ereignis wird ausgelöst, sobald der Kontakt die E-Mail öffnet.

1. Markieren Sie in einer der Reaktionsaktivitäten die Option **Maximale Wartezeit für das Ereignis definieren**, definieren Sie die Dauer (1 Tag in unserem Beispiel) und aktivieren Sie **Zeitüberschreitungspfad einrichten**. Dadurch wird ein weiterer Pfad für Einzelpersonen erstellt, die die erste Push- oder E-Mail-Nachricht nicht öffnen.

   >[!NOTE]
   >
   >Beim Konfigurieren der maximalen Wartezeit für mehrere Ereignisse (in diesem Fall die beiden Reaktionen) müssen Sie die maximale Wartezeit nur für eines dieser Ereignisse konfigurieren.

1. Fügen Sie im Pfad für Personen, bei denen die maximale Wartezeit ohne Kauf verstreicht, eine Aktivität vom Typ **Nachricht** ein und wählen Sie die E-Mail-Folgenachricht aus. Diese Nachricht wird an Personen gesendet, die am nächsten Tag weder die erste E-Mail noch die erste Push-Nachricht öffnen.

1. Verbinden Sie die drei Pfade mit dem zuvor erstellten Kaufereignis. Dieses Ereignis wird ausgelöst, wenn ein Kontakt einen Kauf tätigt.

1. Fügen Sie nach dem Ereignis eine Aktivität vom Typ **Nachricht** per Drag-and-Drop ein und wählen Sie die E-Mail-Nachricht „Vielen Dank“.

## Testen und Veröffentlichen der Journey

1. Bevor Sie Ihre Journey testen, überprüfen Sie, ob sie gültig ist und keine Fehler vorliegen.

1. Klicken Sie auf den Umschalter **Test** in der oberen rechten Ecke, um den Testmodus zu aktivieren. Legen Sie fest, wie die Testprofile in den Testlauf eintreten sollen: als einzelnes Profil oder bis zu 100 gleichzeitig. In diesem [Abschnitt](testing-the-journey.md) erfahren Sie, wie Sie den Testmodus verwenden.

1. Wenn die Journey fertig ist, veröffentlichen Sie diese mit der Schaltfläche **Veröffentlichen** rechts oben.
