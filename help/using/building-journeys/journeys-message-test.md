---
title: Hinzufügen einer Nachricht zu einer Journey
description: Hinzufügen einer Nachricht zu einer Journey
feature: Journeys
topic: Content-Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3530a600a4c842ff99bc23354b2d158c6d41f902
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 34%

---


# Hinzufügen einer Nachricht zu einer Journey

[!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen. Sie müssen nur den Inhalt gestalten und Ihre Nachricht veröffentlichen. Weitere Informationen finden Sie in [diesem Abschnitt](../get-started-content.md). Anschließend fügen Sie einfach eine Push- oder E-Mail-Nachricht in Ihre Journey ein, die mit Journey Optimizer entworfen wurde.

Wenn Sie für den Versand Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weitere Informationen finden Sie in diesem [Abschnitt](../action/action.md).

## Hinzufügen einer Nachrichtenaktivität

1. Beginnen Sie Ihre Journey immer mit einem Ereignis oder einer Aktivität vom Typ **Segment lesen**.

   ![](../assets/jo-message0.png)

1. Ziehen Sie aus dem Bereich **Aktionen** der Palette eine **Nachrichtenaktivität** auf die Arbeitsfläche.

   ![](../assets/jo-message1.png)

1. Fügen Sie einen Titel und eine Beschreibung hinzu.

   ![](../assets/jo-message2.png)

1. Klicken Sie in das Feld **Nachricht**. Eine Liste der in Journey Optimizer entworfenen verfügbaren Nachrichten wird angezeigt. Die Elemente dieser Liste können Sie nach ihrem Status filtern.

   ![](../assets/jo-message3.png)

1. Wählen Sie eine Nachricht aus und klicken Sie auf **Auswählen**. Außerdem können Sie eine neue Nachricht direkt über diesen Bildschirm erstellen, indem Sie auf **Nachricht erstellen** klicken.

   ![](../assets/jo-message4-ter.png)

   Wenn Sie Ihre Nachricht überprüfen möchten, können Sie auf das Symbol **Nachricht öffnen** im Feld **Nachricht** klicken. Die Nachricht wird in einer neuen Registerkarte geöffnet.

   ![](../assets/jo-message4-bis.png)

1. Fügen Sie die nächsten Schritte zu Ihrer Journey hinzu.

## E-Mail-Parameter und Push-Parameter

In den Abschnitten **[!UICONTROL E-Mail-Parameter]** und **[!UICONTROL Push-Parameter]** finden Sie schreibgeschützte Felder. Diese Konfiguration wird normalerweise beim Erstellen der Nachricht durchgeführt. Weitere Informationen dazu finden Sie in [diesem Abschnitt](../get-started-content.md).

![](../assets/jo-message4.png)

Um einen bestimmten Wert zu erzwingen, können Sie das Symbol **Parameterüberschreibung aktivieren** rechts neben dem Feld verwenden. Diese Option kann im Rahmen von Tests nützlich sein. Beispielsweise können Sie als E-Mail-Adresse Ihre eigene E-Mail-Adresse hinzufügen. Nachdem Sie die Journey veröffentlicht haben, wird die E-Mail an Sie gesendet.

## Versandzeitpunkt optimieren{#send-time-optimization}

### Über die Optimierung der Versandzeit{#about-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Über die Optimierung der Versandzeit"
>abstract="Die Funktion zur Sendezeitoptimierung von Adobe Journey Optimizer basiert auf den KI-Diensten von Adobe und kann die beste Sendezeit für E-Mails oder Push-Nachrichten vorhersagen, um die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren."

Die Funktion zur Sendezeitoptimierung von Adobe Journey Optimizer basiert auf den KI-Diensten von Adobe und kann die beste Sendezeit für E-Mails oder Push-Nachrichten vorhersagen, um die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. Verwenden Sie unser Modell für maschinelles Lernen, um personalisierte Sendezeiten für jeden Benutzer zu planen, um die Öffnungs- und Klickraten Ihrer Nachrichten zu erhöhen.

Das Modell &quot;Sendezeitoptimierung&quot;erfasst Ihre Adobe Journey Optimizer-Daten, betrachtet die Öffnungsraten (für E-Mail und Push-Benachrichtigungen) auf Benutzerebene und klickt (für E-Mails), um zu bestimmen, wann Ihre Kunden mit der größten Wahrscheinlichkeit mit Ihrer Nachricht interagieren. Die Sendezeitoptimierung erfordert für fundierte Empfehlungen mindestens einen Monat an Nachrichten-Tracking-Daten. Für jeden Benutzer gibt das Modell die folgenden prädiktiven Daten aus:

* Die beste Stunde jedes Wochentags, um die Interaktion zu maximieren
* Der beste Wochentag zur Maximierung der Interaktion
* Die beste Stunde des besten Wochentags, um die Interaktion zu maximieren

Das Modell variiert, ob Sie über Scoring oder Training sprechen. Die Schulung wird wöchentlich und danach vierteljährlich durchgeführt. Die Auswertung erfolgt zunächst wöchentlich und dann monatlich.

* Training - die Entwicklung des Algorithmus für die Ermittlung des Werts
* Scoring - die Anwendung eines Punkts auf einzelne Profile basierend auf dem trainierten Modell

Diese Informationen werden mit dem Benutzerprofil gespeichert und bei der Ausführung des Journey referenziert, um Adobe Journey Optimizer mitzuteilen, wann Ihre Nachricht gesendet werden soll.

## Wichtige Hinweise{#send-time-optimization-notes}

* Diese Funktion ist nur für kanalübergreifende Nachrichten in E-Mails und Push-Benachrichtigungen mit aktiviertem Tracking verfügbar.
* Die Nachricht muss veröffentlicht werden.
* Diese Funktion ist nicht mit dem Burst-Modus kompatibel.

## Optimierung der Versandzeit aktivieren{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Optimierung der Versandzeit aktivieren"
>abstract="Wählen Sie mithilfe der entsprechenden Optionsschaltfläche aus, ob E-Mail-Öffnungen oder E-Mail-Clickthroughs optimiert werden sollen. Sie können die vom System verwendeten Versandzeiten auch vereinheitlichen, indem Sie innerhalb der nächsten Option einen Wert für die Option Senden eingeben."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Optimierung der Versandzeit aktivieren"
>abstract="Bei Push-Nachrichten wird standardmäßig die Option &quot;Öffnungen&quot;verwendet, da Klicks nicht für Push-Nachrichten gelten. Sie können die vom System verwendeten Versandzeiten auch vereinheitlichen, indem Sie innerhalb der nächsten Option einen Wert für die Option Senden eingeben."

Aktivieren Sie die Sendezeitoptimierung für eine E-Mail oder Push-Nachricht, indem Sie den Schalter **Sendezeitoptimierung** aus den Parametern der Nachrichtenaktivität auswählen.

![](../assets/jo-message5.png)

Wählen Sie für E-Mail-Nachrichten durch Auswahl des entsprechenden Optionsfeldes aus, ob die E-Mail-Öffnungen oder der E-Mail-Clickthrough optimiert werden sollen. Bei Push-Nachrichten wird standardmäßig die Option &quot;Öffnungen&quot;verwendet, da Klicks nicht für Push-Nachrichten gelten.

Sie können die vom System verwendeten Sendezeiten auch vereinheitlichen, indem Sie einen Wert für die Option **Senden innerhalb der nächsten**-Option eingeben. Wenn Sie als Wert &quot;sechs Stunden&quot;wählen, prüft Adobe Journey Optimizer jedes Benutzerprofil, ob die optimale Sendezeit innerhalb von sechs Stunden ab der Journey-Ausführungszeit eintritt, und wählt die für die Sendezeitoptimierung festgelegte Zeit aus. Wenn diese Uhrzeit nicht innerhalb der nächsten sechs Stunden liegt, sendet Adobe Journey Optimizer die Nachricht standardmäßig zur Journey-Ausführungszeit.
