---
title: Hinzufügen einer Nachricht zu einer Journey
description: Hinzufügen einer Nachricht zu einer Journey
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 8a859af9ad09ca3f240ff6f355d4e5f34d2e4eac
workflow-type: ht
source-wordcount: '830'
ht-degree: 100%

---

# Hinzufügen einer Nachricht zu einer Journey{#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Aktivität „Nachricht“"
>abstract="Die Aktivität „Nachricht“ ermöglicht den Versand von Push- oder E-Mail-Nachrichten. Journey Optimizer verfügt über integrierte Nachrichtenfunktionen. Die Erstellung und Veröffentlichung von Nachrichten erfolgt in Journey Optimizer im Menü „Nachrichten“."

[!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen. Sie müssen nur den Inhalt gestalten und Ihre Nachricht veröffentlichen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../messages/get-started-content.md). Anschließend fügen Sie einfach eine Push- oder E-Mail-Nachricht in Ihre Journey ein, die mit Journey Optimizer entworfen wurde.

Wenn Sie für den Versand Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../action/action.md).

## Hinzufügen einer Nachrichtenaktivität

1. Beginnen Sie Ihre Journey immer mit einem Ereignis oder einer Aktivität vom Typ **Segment lesen**.

   ![](assets/jo-message0.png)

1. Ziehen Sie aus dem Bereich **Aktionen** der Palette eine **Nachrichtenaktivität** auf die Arbeitsfläche.

   ![](assets/jo-message1.png)

1. Fügen Sie einen Titel und eine Beschreibung hinzu.

   ![](assets/jo-message2.png)

1. Klicken Sie in das Feld **Nachricht**. Eine Liste der in Journey Optimizer entworfenen verfügbaren Nachrichten wird angezeigt. Die Elemente dieser Liste können Sie nach ihrem Status filtern.

   ![](assets/jo-message3.png)

1. Wählen Sie eine Nachricht aus und klicken Sie auf **Auswählen**. Außerdem können Sie eine neue Nachricht direkt über diesen Bildschirm erstellen, indem Sie auf **Nachricht erstellen** klicken.

   ![](assets/jo-message4-ter.png)

   Wenn Sie Ihre Nachricht überprüfen möchten, können Sie auf das Symbol **Nachricht öffnen** im Feld **Nachricht** klicken. Die Nachricht wird in einer neuen Registerkarte geöffnet.

   ![](assets/jo-message4-bis.png)

1. Fügen Sie die nächsten Schritte zu Ihrer Journey hinzu.

## E-Mail-Parameter und Push-Parameter

In den Abschnitten **[!UICONTROL E-Mail-Parameter]** und **[!UICONTROL Push-Parameter]** finden Sie schreibgeschützte Felder. Diese Konfiguration wird normalerweise beim Erstellen der Nachricht durchgeführt. Weiterführende Informationen finden Sie in diesem [Abschnitt](../messages/get-started-content.md).

![](assets/jo-message4.png)

Um einen bestimmten Wert zu erzwingen, können Sie das Symbol **Parameterüberschreibung aktivieren** rechts neben dem Feld verwenden. Diese Option kann für verschiedene Zwecke nützlich sein:

* Beispielsweise können Sie zum Testen einer E-Mail Ihre eigene E-Mail-Adresse hinzufügen. Nachdem Sie die Journey veröffentlicht haben, wird die E-Mail an Sie gesendet.
* Sie können auf die E-Mail-Adresse der Abonnenten einer Liste verweisen. Siehe diesen [Anwendungsfall](message-to-subscribers-uc.md).

## Optimierung des Versandzeitpunkts{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Über die Optimierung des Versandzeitpunkts"
>abstract="Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den KI-Services von Adobe und kann die beste Versandzeit für E-Mails oder Push-Benachrichtigungen vorhersagen, um die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren."

Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den KI-Services von Adobe und kann die beste Versandzeit für E-Mails oder Push-Benachrichtigungen vorhersagen, um die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. Verwenden Sie unser Modell für maschinelles Lernen, um personalisierte Versandzeitpunkte für jeden Benutzer zu planen, um die Öffnungs- und Klickraten Ihrer Nachrichten zu erhöhen.

>[!NOTE]
>
>Diese Funktion befindet sich derzeit in der Beta-Version und steht nur Beta-Kunden zur Verfügung. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Das Modell „Optimierung des Versandzeitpunkts“ nimmt Ihre Adobe Journey Optimizer-Daten auf, betrachtet die Öffnungsraten (für E-Mail und Push-Benachrichtigungen) und Klicks (für E-Mails) auf Benutzerebene, um zu bestimmen, wann Ihre Kunden mit der größten Wahrscheinlichkeit mit Ihrer Nachricht interagieren. Für fundierte Empfehlungen erfordert die Optimierung des Versandzeitpunkts mindestens einen Monat an Tracking-Daten zu Nachrichten. Mithilfe der folgenden Punktwerte wählt das System für jeden Benutzer automatisch die beste Zeit aus:

* Die beste Stunde jedes Wochentags zur Maximierung der Interaktion
* Der beste Wochentag zur Maximierung der Interaktion
* Die beste Stunde des besten Wochentags zur Maximierung der Interaktion

Das Modell variiert je nachdem, ob es sich um Scoring oder Training handelt. Das Training wird zu Beginn wöchentlich und später vierteljährlich durchgeführt. Das Scoring erfolgt zu Beginn wöchentlich und später monatlich.

* Training – die Entwicklung des Algorithmus für die Ermittlung des Punktwerts
* Scoring – die Anwendung eines Punktwerts auf einzelne Profile, basierend auf dem trainierten Modell

Diese Informationen werden beim Benutzerprofil gespeichert und bei der Ausführung der Journey referenziert, um Adobe Journey Optimizer mitzuteilen, wann Ihre Nachricht gesendet werden soll.

>[!CAUTION]
>
>* Diese Funktion ist nur für E-Mails und Push-Benachrichtigungen über einen einzelnen Kanal verfügbar, wobei das Tracking aktiviert ist.
>* Die Nachricht muss veröffentlicht sein.
>* Diese Funktion ist nicht mit dem Burst-Modus kompatibel.


### Aktivieren der Optimierung des Versandzeitpunkts{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Aktivieren der Optimierung des Versandzeitpunkts"
>abstract="Wählen Sie mithilfe des entsprechenden Radiobuttons aus, ob E-Mail-Öffnungen oder E-Mail-Click-Throughs optimiert werden sollen. Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option „Senden innerhalb der nächsten“ eingeben."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Aktivieren der Optimierung des Versandzeitpunkts"
>abstract="Bei Push-Benachrichtigungen wird standardmäßig die Option „Öffnungen“ verwendet, da Klicks für Push-Benachrichtigungen zutreffen. Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option „Senden innerhalb der nächsten“ eingeben."

Aktivieren Sie die Optimierung des Versandzeitpunkts für eine E-Mail oder Push-Benachrichtigung, indem Sie den Umschalter **Optimierung des Versandzeitpunkts** aus den Parametern der Nachrichtenaktivität auswählen.

![](assets/jo-message5.png)

Wählen Sie für E-Mail-Nachrichten durch Auswahl des entsprechenden Radiobuttons aus, ob die E-Mail-Öffnungen oder die E-Mail-Click-Throughs optimiert werden sollen. Bei Push-Benachrichtigungen wird standardmäßig die Option „Öffnungen“ verwendet, da Klicks für Push-Benachrichtigungen zutreffen.

Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option **Senden innerhalb der nächsten** eingeben. Wenn Sie als Wert „sechs Stunden“ wählen, prüft [!DNL Journey Optimizer] jedes Benutzerprofil und wählt den optimalen Versandzeitpunkt innerhalb von sechs Stunden ab der Journey-Ausführungszeit aus.
