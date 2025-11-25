---
solution: Journey Optimizer
product: journey optimizer
title: Anwendungsfälle für Journeys
description: Anwendungsfälle für Journeys
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: Anwendungsfall, mehrere Kanäle, Nachrichten, Journey, Kanal, Ereignisse, Push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: ht
source-wordcount: '769'
ht-degree: 100%

---

# Senden von Multi-Channel-Nachrichten {#send-multi-channel-messages}

In diesem Abschnitt wird ein Anwendungsfall vorgestellt, der die Aktivität „Zielgruppe lesen“, ein Ereignis, Reaktionsereignisse und E-Mail-/Push-Nachrichten kombiniert.

![Einfacher Journey-Fluss mit den Aktivitäten „Zielgruppe lesen“, „Warten“ und „E-Mail“](assets/jo-uc1.png)

## Beschreibung des Anwendungsfalls

Das Ziel dieses Anwendungsfalls ist das Senden einer ersten E-Mail-Nachricht an alle Kundinnen und Kunden, die zu einer bestimmten Zielgruppe gehören.

Je nach Reaktion auf die erste Nachricht werden bestimmte Folgenachrichten gesendet.

Wenn die Kundin bzw. der Kunde die E-Mail öffnet, wartet das System auf einen Kauf und sendet eine Push-Nachricht, um der Person zu danken.

Wenn keine Reaktion erfolgt, wird eine Folge-E-Mail gesendet.

## Voraussetzungen

Konfigurieren Sie Folgendes, damit dieser Anwendungsfall funktioniert:

* eine Zielgruppe für alle Kundinnen und Kunden, die in Atlanta, San Francisco oder Seattle leben und nach 1980 geboren wurden
* ein Kaufereignis

### Erstellen der Zielgruppe

In dieser Journey wird eine bestimmte Zielgruppe von Kundinnen und Kunden genutzt. Alle dieser Zielgruppe angehörenden Personen treten in die Journey ein und folgen den verschiedenen Schritten. In diesem Beispiel umfasst die Zielgruppe alle Kundinnen und Kunden an, die in Atlanta, San Francisco oder Seattle leben und nach 1980 geboren wurden.

Weitere Informationen zu Zielgruppen [finden Sie auf dieser Seite](../audience/about-audiences.md).

1. Wählen Sie im Menüabschnitt „KUNDE“ die Option **[!UICONTROL Zielgruppen]** aus.
1. Klicken Sie oben rechts von der Zielgruppenliste auf die Schaltfläche **[!UICONTROL Zielgruppe erstellen]**.
1. Geben Sie im Bereich **[!UICONTROL Zielgruppen-Eigenschaften]** einen Namen für die Zielgruppe ein.
1. Ziehen Sie per Drag-and-Drop die gewünschten Felder aus dem linken Bereich in den Arbeitsbereich in der Mitte und konfigurieren Sie die Felder entsprechend Ihren Anforderungen. Verwenden Sie in diesem Beispiel die Attributfelder **Stadt** und **Geburtsjahr**.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Panel mit zusätzlichen Attributen zur Auswahl von Anreicherungsdaten](assets/add-attributes.png)

Die Zielgruppe ist jetzt erstellt und kann in der Journey verwendet werden. Mit einer Aktivität vom Typ **Zielgruppe lesen** können alle der Zielgruppe angehörenden Personen in die Journey eintreten.

### Konfigurieren des Ereignisses

Konfigurieren Sie ein Ereignis, das an die Journey gesendet wird, wenn eine Kundin bzw. ein Kunde einen Kauf tätigt. Wenn die Journey das Ereignis erhält, wird die Nachricht „Vielen Dank“ verschickt.

Verwenden Sie dafür ein [regelbasiertes Ereignis](../event/about-events.md).

1. Wählen Sie im Menüabschnitt ADMINISTRATION die Option **[!UICONTROL Konfigurationen]** und klicken Sie dann auf **[!UICONTROL Ereignisse]**. Klicken Sie auf **[!UICONTROL Ereignis erstellen]**, um ein neues Ereignis zu erstellen.

1. Geben Sie den Namen des Ereignisses ein.

1. Wählen Sie im Feld **[!UICONTROL Ereignis-ID-Typ]** die Option **[!UICONTROL Regelbasiert]** aus.

1. Definieren Sie die Felder **[!UICONTROL Schema]** und **[!UICONTROL Payload]**. Verwenden Sie mehrere Felder, beispielsweise das erworbene Produkt, das Kaufdatum und die Kauf-ID.

1. Definieren Sie im Feld **[!UICONTROL Ereignis-ID-Bedingung]** die vom System verwendete Bedingung zur Identifizierung der Ereignisse, die die Journey auslösen. Fügen Sie beispielsweise ein Feld `purchaseMessage` hinzu und definieren Sie die folgende Regel: `purchaseMessage="thank you"`

1. Definieren Sie den **[!UICONTROL Namespace]** und die **[!UICONTROL Profilkennung]**.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

   ![Journey mit Bedingungsaktivität, die zu Gold-Mitgliedern und anderen Pfaden verzweigt](assets/jo-uc2.png)

Das Ereignis ist jetzt konfiguriert und kann in der Journey verwendet werden. Mit der entsprechenden Ereignisaktivität kann jedes Mal eine Aktion ausgelöst werden, wenn eine Person einen Kauf tätigt.

## Entwerfen der Journey

1. Beginnen Sie die Journey mit einer Aktivität vom Typ **Zielgruppe lesen**. Wählen Sie die zuvor erstellte Zielgruppe aus. Alle der Zielgruppe angehörenden Personen treten in die Journey ein.

   ![Prüfen der Wetterbedingungen, ob die Temperatur unter 10 Grad liegt](assets/jo-uc4.png)

1. Legen Sie eine Aktionsaktivität vom Typ **E-Mail** ab und definieren Sie den Inhalt der „ersten Nachricht“. Diese Nachricht wird an alle Personen in der Journey gesendet. In diesem [Abschnitt](../email/create-email.md) erfahren Sie, wie Sie eine E-Mail konfigurieren und gestalten können.

   ![Vollständige wetterbasierte Journey mit Temperaturbedingungs- und E-Mail-Aktionen](assets/jo-uc5.png)

1. Fügen Sie ein Ereignis vom Typ **Reaktion** hinzu und wählen Sie **E-Mail geöffnet**. Das Ereignis wird ausgelöst, sobald ein zur Zielgruppe gehörender Kontakt die E-Mail öffnet.

1. Aktivieren Sie das Kontrollkästchen **Maximale Wartezeit für das Ereignis definieren**, definieren Sie eine Dauer (in diesem Beispiel 1 Tag) und aktivieren Sie **Zeitüberschreitungspfad einrichten**. Dadurch wird ein weiterer Pfad für Einzelpersonen erstellt, die die erste Push- oder E-Mail-Nachricht nicht öffnen.

1. Legen Sie im Pfad der maximalen Wartezeit die Aktionsaktivität **E-Mail** ab und definieren Sie den Inhalt der Folgenachricht. Diese Nachricht wird an Personen gesendet, die die erste E-Mail- oder Push-Nachricht nicht innerhalb des nächsten Tages öffnen. [Erfahren Sie, wie Sie eine E-Mail konfigurieren und gestalten](../email/create-email.md).

1. Fügen Sie im ersten Pfad das zuvor erstellte Kaufereignis hinzu. Dieses Ereignis wird ausgelöst, wenn ein Kontakt einen Kauf tätigt.

1. Legen Sie nach dem Ereignis die Aktionsaktivität **Push** im Arbeitsbereich ab und definieren Sie den Inhalt der Dankesnachricht. In diesem [Abschnitt](../push/create-push.md) erfahren Sie, wie Sie eine Push-Benachrichtigung konfigurieren und gestalten können.

## Testen und Veröffentlichen der Journey

1. Stellen Sie vor dem Testen der Journey sicher, dass sie gültig ist und kein Fehler vorliegt. 

1. Verwenden Sie den Umschalter **Test** in der oberen rechten Ecke, um den Testmodus zu aktivieren. In diesem [Abschnitt](testing-the-journey.md) erfahren Sie, wie Sie den Testmodus verwenden.

1. Wenn die Journey fertig ist, veröffentlichen Sie diese mit der Schaltfläche **Veröffentlichen** rechts oben.
