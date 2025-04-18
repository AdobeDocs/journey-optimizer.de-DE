---
solution: Journey Optimizer
product: journey optimizer
title: Ende einer Journey
description: So endet eine Journey in Journey Optimizer
feature: Journeys
role: User
level: Intermediate
keywords: Erneut eintreten, Journey, Beenden, live, Stoppen
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: a536336ec7b37ffa0cd860c2c7479c75365eff00
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 66%

---

# Beenden einer Journey {#journey-ending}

Eine Journey kann für eine Person auf zwei Weisen enden:

* Der Kontakt erreicht die letzte Aktivität eines Pfads und wechselt dann zum [Ende-Tag](#end-tag).
* Der Kontakt erreicht bei einer **Bedingung**-Aktivität (oder einer **Warte**-Aktivität mit einer Bedingung) und erfüllt keine der Bedingungen.

Die Person kann dann die Journey erneut betreten, wenn der erneute Eintritt erlaubt ist. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/journey-properties.md#entrance)

Um eine Live-Journey zu beenden, empfehlen wir, sie zu schließen. Der Eintritt neuer Kunden und Kundinnen in die Journey wird dann blockiert. Profile, die sich bereits auf der Journey befinden, können diese bis zu ihrem Ende erleben. Weiterführende Informationen finden Sie in diesem [Abschnitt](#close-journey)

Sie können eine Journey nur stoppen, wenn ein unerwartetes Ereignis eintritt und die gesamte Verarbeitung der Journey unverzüglich abgebrochen werden muss. Personen, die bereits in eine Journey eingetreten sind, sind alle in ihrem Fortschritt angehalten. Weiterführende Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey.md#stop-journey).

>[!IMPORTANT]
>
>Sie können einen [geschlossenen](#close-journey) oder [gestoppten](#stop-journey) Journey nicht neu starten.


## Journey-End-Tag {#end-tag}

Beim Bearbeiten einer Journey wird am Ende jedes Pfads ein End-Tag angezeigt. Dieser Knoten kann nicht manuell hinzugefügt oder entfernt werden, und lediglich bei seiner Kennzeichnung sind Änderungen möglich. Er markiert das Ende jedes Pfads der Journey. Wenn die Journey mehrere Pfade hat, empfehlen wir, für jedes Ende eine Kennzeichnung hinzuzufügen, damit Berichte leichter verständlich sind. Weitere Informationen zu [Journey-Berichten](../reports/live-report.md).

![](assets/journey-end.png)

## Schließen einer Journey {#close-journey}

Eine Journey kann aus den folgenden Gründen geschlossen werden:

* Die Journey wird manuell über die Schaltfläche [**[!UICONTROL Für neue Eintritte schließen]**](#close-to-new-entrances) geschlossen.
* Eine einmalige segmentbasierte Journey, deren Ausführung beendet ist und die das globale Timeout von 91 Tagen erreicht hat.
* Nach dem letzten Vorkommen einer wiederkehrenden zielgruppenbasierten Journey.

Sie können eine Journey manuell schließen. In diesem Fall können Kunden, die sich bereits in der Journey befinden, ihren Pfad bis zum Ende verfolgen, neue Benutzende können jedoch nicht in die Journey eintreten. Wenn eine Journey geschlossen wird (aus einem der oben genannten Gründe), weist sie den Status **[!UICONTROL Geschlossen]** auf. Die Journey stoppt den Eintritt neuer Personen in die Journey.  Profile, die sich bereits auf der Journey befinden, können die Journey normal beenden. Nach der standardmäßigen globalen maximalen Wartezeit von 91 Tagen wechselt der Journey in den Status **Beendet**.

Nach dem **91-tägigen globalen Journey-Timeout** wechselt eine Journey des Typs Zielgruppe lesen in den **Beendet**-Status. Dieses Verhalten ist nur für 91 Tage festgelegt, da alle Informationen über Profile, die die Journey betreten haben, 91 Tage nach ihrem Betreten entfernt werden. Personen, die sich noch in der Journey befinden, sind automatisch betroffen. Nach Ablauf der 91-tägigen maximalen Wartezeit verlassen sie die Journey.  Weitere Informationen zu [globalen Journey-Zeitüberschreitung](../building-journeys/journey-properties.md#global_timeout).

Eine geschlossene Journey-Version kann weder neu gestartet noch gelöscht werden. Stattdessen können Sie eine neue Version davon erstellen oder sie duplizieren. Nur abgeschlossene Journeys können gelöscht werden.

### Für neue Eintritte schließen {#close-to-new-entrances}

Um eine Journey in der Liste der Journeys zu schließen, klicken Sie auf den Button mit den **[!UICONTROL Auslassungszeichen]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Für neue Eintritte schließen]** aus.

![](assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie schließen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

   ![](assets/finish_drop_down_list.png)

1. Klicken Sie auf **[!UICONTROL Für neue Eintritte schließen]** und bestätigen Sie diese Auswahl im Dialogfeld.

>[!TIP]
>
>Eine segmentbasierte Journey mit einer einzigen Aufnahme behält den **Live**-Status auch bei einmaliger Ausführung bei. Die Profile treten nach Abschluss nicht erneut ein, aber die Journey verbleibt im **Live**-Status, bis die standardmäßige globale Zeitüberschreitung abläuft. Sie können sie mit der Option **Für neue Eintritte schließen** früher manuell schließen.


## Stoppen einer Journey {#stop-journey}

Sie können nötigenfalls den Fortschritt aller Personen in einer Journey stoppen. Anhalten der Journey-Zeitüberschreitung für alle Personen auf der Journey. Wenn Sie eine Journey stoppen, wird der Fortschritt der bereits in der Journey befindlichen Personen angehalten. Die Journey wird praktisch deaktiviert. Wenn Sie eine Journey beenden möchten, empfiehlt es sich, sie [ schließen](#close-journey).

Beim Stoppen wird der Journey-Status auf **[!UICONTROL Gestoppt]** gesetzt.

Sie können beispielsweise eine Journey stoppen, wenn ein Marketer erkennt, dass die Journey die falsche Zielgruppe anspricht, oder wenn eine benutzerdefinierte Aktion, mit der Nachrichten gesendet werden sollen, nicht ordnungsgemäß funktioniert. Um eine Journey aus der Liste der Journeys zu entfernen, klicken Sie auf den Button mit den **[!UICONTROL Auslassungszeichen]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Stoppen]** aus.

![](assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie stoppen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

   ![](assets/finish_drop_down_list2.png)

1. Klicken Sie auf **[!UICONTROL Stoppen]** und bestätigen Sie diese Auswahl im Dialogfeld.
