---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen einer integrierten Kanalaktion zu einer Journey
description: Erfahren Sie, wie Sie einer Journey eine integrierte Kanalaktion hinzufügen.
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Nachricht, Push, SMS, E-Mail, In-App, Web, Inhaltskarte, code-basiertes Erlebnis
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 77%

---

# Verwenden integrierter Kanalaktionen {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Integrierte Kanalaktion"
>abstract="Journey Optimizer verfügt über integrierte Kanalaktionsfunktionen. Sie können einfach eine ausgehende (E-Mail, Textnachricht (SMS/MMS), Push-Benachrichtigung) oder eingehende (In-App-, Web-, Code-basierte Erlebnis-, Inhaltskarten-) Aktivität zu Ihrer Journey hinzufügen und Einstellungen und Inhalte definieren. Sie wird dann ausgeführt und innerhalb der Journey gesendet."

[!DNL Journey Optimizer] verfügt über integrierte Aktionsfunktionen für Kanäle. Sie können einfach eine ausgehende (E-Mail, Textnachricht (SMS/MMS), Push-Benachrichtigung) oder eingehende (In-App-, Web-, Code-basierte Erlebnis-, Inhaltskarten-) Aktivität zu Ihrer Journey hinzufügen und Einstellungen und Inhalte definieren. Sie wird dann ausgeführt und innerhalb der Journey gesendet.

>[!NOTE]
>
>Sie können auch bestimmte Aktionen zum Senden von Nachrichten einrichten. [Weitere Informationen](#recommendation)

Gehen Sie wie folgt vor, um einer Journey eine integrierte Kanalaktion hinzuzufügen.

1. Beginnen Sie Ihre Journey mit einem [Ereignis](general-events.md) oder einer Aktivität vom Typ [Zielgruppe lesen](read-audience.md).

1. Ziehen Sie aus dem Bereich **Aktionen** der Palette ein ausgehendes (**E-Mail**, **Push**, **SMS**) oder ein eingehendes (**In-App**, **Web**, **code-basiertes Erlebnis**, **Inhaltskarte**). -Aktivität in die Arbeitsfläche.

   ![](assets/journey-web-activity.png)

1. Konfigurieren Sie Ihre Aktivität. 

   * Gehen Sie wie folgt vor, um den Inhalt einer Nachricht detailliert zu erstellen:

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
      <a href="../sms/create-sms.md"><strong>Erstellen von Textnachrichten (SMS/MMS)</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * Gehen Sie wie folgt vor, um eine eingehende Aktion zu erstellen:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="Lead" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>Erstellen von In-App-Nachrichten</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="Lead" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>Erstellen von Web-Erlebnissen</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="Lead" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>Erstellen von Inhaltskarten</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="Gelegentlich" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>Erstellen von Code-basierten Erlebnissen<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

     >[!NOTE]
     >
     >Jede eingehende Nachrichtenaktivität verfügt über eine 3-tägige **Warten** -Aktivität. [Weitere Informationen](../building-journeys/wait-activity.md#auto-wait-node)

## Empfehlung {#recommendation}

[!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen. Mit benutzerdefinierten Aktionen können Sie jedoch die Verbindung eines Drittanbietersystems konfigurieren, um Nachrichten oder API-Aufrufe zu senden.

* Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. [Weitere Informationen](../action/action.md)

* Wenn Sie mit Campaign und Journey Optimizer arbeiten, lesen Sie diese Abschnitte:

   * [[!DNL Journey Optimizer] und Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] und Campaign Standard](../action/acs-action.md)

## Aktualisieren von Live-Inhalten{#update-live-content}

Sie können den Inhalt einer integrierten Kanalaktion in einer Live-Journey aktualisieren.

Öffnen Sie dazu die Live-Journey, wählen Sie die Kanalaktivität aus und klicken Sie auf **Inhalt bearbeiten**.

![](assets/add-a-message2.png)

Sie können jedoch nicht die Attribute ändern, die bei der Personalisierung verwendet wurden, egal, ob es sich um Profilattribute oder kontextuelle Daten (aus Ereignis- oder Journey-Eigenschaften) handelt.

Wenn Sie Kontextdaten geändert haben, wird die folgende Fehlermeldung angezeigt: ERR_AUTHORING_JOURNEYVERSION_201

Wenn Sie Profilattribute geändert haben, wird die folgende Fehlermeldung angezeigt: ERR_AUTHORING_JOURNEYVERSION_202

Beachten Sie, dass für die In-App-Aktivität alle Änderungen am Inhalt vorgenommen werden können, während die Journey live ist. In-App-Trigger können jedoch nicht geändert werden.

## Optimierung des Versandzeitpunkts{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Über die Optimierung des Versandzeitpunkts"
>abstract="Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den KI-Services von Adobe. Sie kann basierend auf vergangenen Öffnungs- und Klickraten die beste Versandzeit für E-Mails oder Push-Benachrichtigungen vorhersagen, um die Interaktion zu maximieren."

>[!NOTE]
>
>Diese Funktion ist standardmäßig nicht aktiviert. Sie können sich an den Adobe-Support wenden, um sie zu aktivieren.
>
>Die Funktion zur Sendezeitoptimierung gilt nur für E-Mail- und Push-Kanäle.

### Anmerkungen zur Optimierung des Versandzeitpunkts {#about-send-time}

Die Sendezeitoptimierungs-Funktion von Adobe Journey Optimizer, unterstützt von Adobe Optimization AI-Diensten, kann die beste Sendezeit für den Versand einer **E-Mail** oder **Push-Nachricht** vorhersagen, um die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. Verwenden Sie unser Modell für maschinelles Lernen, um personalisierte Versandzeitpunkte für jeden Benutzer zu planen, um die Öffnungs- und Klickraten Ihrer Nachrichten zu erhöhen.

Das Modell „Optimierung des Versandzeitpunkts“ nimmt Ihre Adobe Journey Optimizer-Daten auf, betrachtet die Öffnungsraten (für E-Mail und Push-Benachrichtigungen) und Klicks (für E-Mails) auf Benutzerebene, um zu bestimmen, wann Ihre Kunden mit der größten Wahrscheinlichkeit mit Ihrer Nachricht interagieren. Für fundierte Empfehlungen erfordert die Optimierung des Versandzeitpunkts mindestens einen Monat an Tracking-Daten zu Nachrichten. Mithilfe der folgenden Punktwerte wählt das System für jeden Benutzer automatisch die beste Zeit aus:

* Die beste Stunde jedes Wochentags zur Maximierung der Interaktion
* Der beste Wochentag zur Maximierung der Interaktion
* Die beste Stunde des besten Wochentags zur Maximierung der Interaktion

Das Modell variiert je nachdem, ob es sich um Scoring oder Training handelt. Das Training wird zu Beginn wöchentlich und später vierteljährlich durchgeführt. Das Scoring erfolgt zu Beginn wöchentlich und später monatlich.

* Training – die Entwicklung des Algorithmus für die Ermittlung des Punktwerts
* Scoring – die Anwendung eines Punktwerts auf einzelne Profile, basierend auf dem trainierten Modell

Diese Informationen werden beim Benutzerprofil gespeichert und bei der Ausführung der Journey referenziert, um Adobe Journey Optimizer mitzuteilen, wann Ihre Nachricht gesendet werden soll.

### Häufig gestellte Fragen {#faq-send-time}

+++ Was kann mit der Optimierung des Versandzeitpunkts erreicht werden? Wie werden neue Profile behandelt? Wird das Senden über ein 6/12/24-Stunden-Fenster verteilt?

Bei der Optimierung des Versandzeitpunkts wird versucht, den besten Zeitpunkt für die Interaktion mit Kundinnen oder Kunden vorherzusagen und die Öffnungs-/Klickraten von E-Mails zu optimieren. Die Punktzahl entspricht dem Format von `3*7*24`-Attributen für jedes Profil. Die `7*24`-Attribute beschreiben die Rangfolge der prognostizierten besten Zeit für den Versand von E-Mails an den Empfänger, und „3“ dient der Optimierung der E-Mail-Öffnungsrate, der E-Mail-Klickrate und der Push-Öffnungsrate.

+++

+++Wo kann ich die erwartete Sendezeit für jedes Profil sehen?

Sie können das Gesamtergebnis in der Schnittstelle **Profile** einsehen. Für jeden der drei Sätze mit 168 Punktzahlen liegt die Rangliste zwischen -83 und 84. Je höher der Rang ist, desto besser wurde die Zeit für die Interaktion mit der Empfängerin bzw. dem Empfänger ausgewählt. Da Sie den Start und die Dauer einer Journey frei bestimmen können, fällt der beste Rang (84) möglicherweise nicht in dieses Zeitfenster. In diesem Fall wird empfohlen, eine Stunde mit dem höchsten Rangwert auszuwählen.

+++


+++Welche Berichte stehen zur Verfügung?

Wählen Sie die Journey aus, klicken Sie auf die Schaltfläche **Bericht anzeigen** rechts oben und wählen Sie abschließend die Registerkarte **Journey** auf der linken Seite aus. [Weitere Informationen](../reports/journey-global-report-cja.md)

+++

+++Wie wirken sich die Daten der Optimierung des Versandzeitpunkts auf den Profilumfang aus?

Bei einer Optimierung des Versandzeitpunkts werden die Punktzahl/Attribute zu jedem Profil hinzugefügt, es wird jedoch kein neues Profil erstellt.

+++

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
