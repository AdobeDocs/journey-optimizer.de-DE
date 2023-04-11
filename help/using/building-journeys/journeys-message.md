---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen einer Nachricht zu einer Journey
description: Erfahren Sie, wie Sie ein Nachricht zu einer Journey hinzufügen können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Nachricht, Push, SMS, E-Mail
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 45d508b284c23235518fab37095413091208e497
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# E-Mail, SMS, Push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen. Sie können einfach eine Push-, SMS- oder E-Mail-Nachrichtenaktivität zu Ihrer Journey hinzufügen und Einstellungen und Inhalte definieren. Sie wird dann ausgeführt und innerhalb der Journey gesendet.

Sie können auch bestimmte Aktionen zum Senden von Nachrichten einrichten:

* Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../action/action.md).

* Wenn Sie mit Campaign und Journey Optimizer arbeiten, lesen Sie diese Abschnitte:

   * [[!DNL Journey Optimizer] und Campaign Classic v7 / Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] und Campaign Standard](../action/acs-action.md)

Gehen Sie wie folgt vor, um eine Nachricht zu einer Journey hinzuzufügen:

1. Beginnen Sie Ihre Journey mit einem [Ereignis](general-events.md) oder einer Aktivität vom Typ [Segment lesen](read-segment.md).

1. Ziehen Sie aus dem Abschnitt **Aktionen** der Palette eine **E-Mail**-, **SMS**- oder **Push**-Aktivität auf die Arbeitsfläche und legen Sie sie dort ab.

1. Konfigurieren Sie Ihre Aktivität. Auf den folgenden Seiten erfahren Sie, wie Sie Ihren Nachrichteninhalt erstellen:

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="Lead" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>Erstellen von E-Mails</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="Gelegentlich" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>Push-Benachrichtigungen erstellen<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="Validierung" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>SMS-Nachrichten erstellen</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## Live-Inhalt aktualisieren{#update-live-content}

Sie können den Inhalt einer Nachricht (E-Mail, SMS, Push) in einer Live-Journey aktualisieren.

Öffnen Sie dazu Ihre Live-Journey, wählen Sie die Nachrichtenaktivität aus und klicken Sie auf **Inhalt bearbeiten**.

![](assets/add-a-message2.png)

Sie können jedoch nicht die Attribute ändern, die bei der Personalisierung verwendet wurden, egal, ob es sich um Profilattribute oder kontextuelle Daten (aus Ereignis- oder Journey-Eigenschaften) handelt.

## Optimierung des Versandzeitpunkts{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Über die Optimierung des Versandzeitpunkts"
>abstract="Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den KI-Services von Adobe. Sie kann basierend auf vergangenen Öffnungs- und Klickraten die beste Versandzeit für E-Mails oder Push-Benachrichtigungen vorhersagen, um die Interaktion zu maximieren."

### Anmerkungen zur Optimierung des Versandzeitpunkts {#about-send-time}

Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den KI-Services von Adobe. Sie kann basierend auf vergangenen Öffnungs- und Klickraten die beste Versandzeit für E-Mails oder Push-Benachrichtigungen vorhersagen, um die Interaktion zu maximieren. Verwenden Sie unser Modell für maschinelles Lernen, um personalisierte Versandzeitpunkte für jeden Benutzer zu planen, um die Öffnungs- und Klickraten Ihrer Nachrichten zu erhöhen.

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
>Diese Funktion ist nicht mit dem Burst-Modus kompatibel.

### Aktivieren der Optimierung des Versandzeitpunkts{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Aktivieren der Optimierung des Versandzeitpunkts"
>abstract="Wählen Sie mithilfe des entsprechenden Radiobuttons aus, ob E-Mail-Öffnungen oder E-Mail-Click-Throughs optimiert werden sollen. Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option „Senden innerhalb der nächsten“ eingeben."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Aktivieren der Optimierung des Versandzeitpunkts"
>abstract="Bei Push-Benachrichtigungen wird standardmäßig die Option „Öffnungen“ verwendet, da Klicks für Push-Benachrichtigungen zutreffen. Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option „Senden innerhalb der nächsten“ eingeben."

Aktivieren Sie die Versandzeitpunktoptimierung für eine E-Mail oder Push-Benachrichtigung, indem Sie den Umschalter **Versandzeitpunktoptimierung** aus den Parametern der Aktivität auswählen.

![](../building-journeys/assets/jo-message5.png)

Wählen Sie für E-Mail-Nachrichten durch Auswahl des entsprechenden Radiobuttons aus, ob die E-Mail-Öffnungen oder die E-Mail-Click-Throughs optimiert werden sollen. Bei Push-Benachrichtigungen wird standardmäßig die Option „Öffnungen“ verwendet, da Klicks für Push-Benachrichtigungen zutreffen.

Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option **Senden innerhalb der nächsten** eingeben. Wenn Sie als Wert „sechs Stunden“ wählen, prüft [!DNL Journey Optimizer] jedes Benutzerprofil und wählt den optimalen Versandzeitpunkt innerhalb von sechs Stunden ab der Journey-Ausführungszeit aus.

**Was passiert, wenn der optimale Zeitpunkt außerhalb des Zeitfensters liegt?**

Nehmen wir ein Beispiel mit dem folgenden Setup:

* Optimierung der Klicks
* Die Aktion soll um 10 Uhr beginnen
* Das Zeitfenster beträgt 3 Stunden

Ein Profil kann eine optimale Öffnungszeit haben, die außerhalb des Fensters liegt. Zum Beispiel ist für John der optimale Öffnungszeitpunkt um 17 Uhr.

Auf Profilebene gibt es Bewertungen für jede Stunde der Woche. In diesem Beispiel wird die E-Mail immer innerhalb des Fensters gesendet. Zur Laufzeit prüft das System die Liste der Bewertungen innerhalb dieses Fensters (3-Stunden-Fenster ab 10 Uhr). Das System vergleicht dann die Bewertungen für 10 Uhr, 11 Uhr und Mittag und wählt die höchste aus. Die E-Mail wird zu diesem Zeitpunkt gesendet.
