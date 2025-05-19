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
source-git-commit: e435a4bf9d284845f27021b3d36c555def749fbe
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 50%

---

# Beenden einer Journey {#journey-ending}

## Ende einer Live-Journey

Journey werden geschlossen, wenn die globale Journey-Zeitüberschreitung erreicht wird oder nach dem letzten Auftreten einer wiederkehrenden zielgruppenbasierten Journey. [Erfahren Sie, wie Journey geschlossen werden](#close-journey).

Wenn Sie eine Live-Journey beenden müssen, empfehlen wir, [Sie sie schließen](#close-to-new-entrances) manuell zu schließen. Das Eintreffen neuer Kunden auf der Journey wird dann blockiert. Profile, die sich bereits auf der Journey befinden, können diese bis zu ihrem Ende erleben.

Sie können auch [Journey stoppen](#stop-journey) nur im Notfall und wenn die gesamte Journey-Verarbeitung sofort beendet werden muss. Personen, die bereits eine Journey betreten haben, werden alle in ihrem Fortschritt angehalten.

>[!IMPORTANT]
>
>* Sie können eine [geschlossene“ oder [gestoppte](#close-journey) Journey nicht ](#stop-journey) oder löschen. Stattdessen können Sie eine neue Version davon erstellen oder sie duplizieren.
>
>* Nur abgeschlossene Journeys können gelöscht werden.

## Wie Profile eine Journey beenden

Eine Journey endet für eine Person in zwei bestimmten Kontexten:

* Der Kontakt erreicht die letzte Aktivität eines Pfads und wechselt dann zum [Ende-Tag](#end-tag).
* Der Kontakt erreicht bei einer **Bedingung**-Aktivität (oder einer **Warte**-Aktivität mit einer Bedingung) und erfüllt keine der Bedingungen.

Die Person kann dann die Journey erneut betreten, wenn der erneute Eintritt erlaubt ist. [Erfahren Sie mehr über die Verwaltung von Ein- und Wiedereintritten](../building-journeys/journey-properties.md#entrance)

## Journey-End-Tag {#end-tag}

Beim Bearbeiten einer Journey wird am Ende jedes Pfads ein End-Tag angezeigt. Dieser Knoten kann nicht manuell hinzugefügt oder entfernt werden, und lediglich bei seiner Kennzeichnung sind Änderungen möglich. Er markiert das Ende jedes Pfades der Journey.

Wenn die Journey mehrere Pfade hat, empfehlen wir, für jedes Ende eine Kennzeichnung hinzuzufügen, damit Berichte leichter verständlich sind. Weitere Informationen zu [Journey-Berichten](../reports/live-report.md).

![](assets/journey-end.png)

## Schließen einer Journey {#close-journey}

Eine Journey kann aus den folgenden Gründen geschlossen werden:

* Eine einmalige segmentbasierte Journey, deren Ausführung beendet ist und die das globale Timeout von 91 Tagen erreicht hat.
* Nach dem letzten Vorkommen eines wiederkehrenden zielgruppenbasierten Journey.
* Die Journey wird manuell über die Schaltfläche [**[!UICONTROL Für neue Eintritte schließen]**](#close-to-new-entrances) geschlossen.

Nach dem **91-tägigen globalen Journey-Timeout** wechselt eine Journey des Typs Zielgruppe lesen in den **Beendet**-Status. Dieses Verhalten ist nur für 91 Tage festgelegt, da alle Informationen über Profile, die die Journey betreten haben, 91 Tage nach ihrem Betreten entfernt werden. Personen, die sich noch in der Journey befinden, sind automatisch betroffen. Nach Ablauf der 91-tägigen maximalen Wartezeit verlassen sie die Journey.  Weitere Informationen zu [globalen Journey-Zeitüberschreitung](../building-journeys/journey-properties.md#global_timeout).

>[!TIP]
>
>Eine segmentbasierte Journey mit einer einzigen Aufnahme behält den **Live**-Status auch bei einmaliger Ausführung bei. Profile können nach Abschluss nicht erneut eintreten, aber die Journey verbleibt im **Live**-Status, bis die standardmäßige globale Zeitüberschreitung abläuft. Sie können sie mit der Option **Für neue Eintritte schließen** früher manuell schließen.

### Für neue Eintritte schließen {#close-to-new-entrances}

Sie können eine Journey manuell schließen. In diesem Fall können Kunden, die sich bereits in der Journey befinden, ihren Pfad bis zum Ende verfolgen, neue Benutzende können jedoch nicht in die Journey eintreten. Wenn eine Journey geschlossen wird (aus einem der oben genannten Gründe), weist sie den Status **[!UICONTROL Geschlossen]** auf. Die Journey stoppt den Eintritt neuer Personen in die Journey.  Profile, die sich bereits auf der Journey befinden, können die Journey normal beenden. Nach der standardmäßigen globalen maximalen Wartezeit von 91 Tagen wechselt der Journey in den Status **Beendet**.

Um eine Journey in der Liste der Journeys zu schließen, klicken Sie auf den Button mit den **[!UICONTROL Auslassungszeichen]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Für neue Eintritte schließen]** aus.

![](assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie schließen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

   ![](assets/finish_drop_down_list.png){width="50%" align="left" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Für neue Eintritte schließen]** und bestätigen Sie diese Auswahl im Dialogfeld.




## Stoppen einer Journey {#stop-journey}

Sie können nötigenfalls den Fortschritt aller Personen in einer Journey stoppen. Anhalten der Journey-Zeitüberschreitung für alle Personen auf der Journey. Wenn Sie eine Journey stoppen, wird der Fortschritt der bereits in der Journey befindlichen Personen angehalten. Die Journey wird praktisch deaktiviert. Wenn Sie eine Journey beenden möchten, empfiehlt es sich, sie [ schließen](#close-journey).


Sie können beispielsweise eine Journey stoppen, wenn ein Marketer erkennt, dass die Journey die falsche Zielgruppe anspricht, oder wenn eine benutzerdefinierte Aktion, mit der Nachrichten gesendet werden sollen, nicht ordnungsgemäß funktioniert. Um eine Journey aus der Liste der Journeys zu entfernen, klicken Sie auf den Button mit den **[!UICONTROL Auslassungszeichen]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Stoppen]** aus.

![](assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie stoppen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

   ![](assets/finish_drop_down_list2.png){width="50%" align="left" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Stoppen]** und bestätigen Sie diese Auswahl im Dialogfeld.

Beim Stoppen wird der Journey-Status auf **[!UICONTROL Gestoppt]** gesetzt.
