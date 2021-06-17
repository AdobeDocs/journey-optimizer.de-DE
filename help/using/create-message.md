---
title: Erstellen einer Nachricht
description: Erfahren Sie, wie Sie eine Nachricht erstellen
feature: Übersicht
topic: Content Management
role: User
level: Beginner
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 96%

---

# Erstellen einer Nachricht {#create-message}

Nachrichten sind über den Tastaturbefehl **[!UICONTROL Nachrichten]** im linken Navigationsbereich verfügbar. Alle Nachrichten werden aufgelistet und nach Veröffentlichungsdatum (bei veröffentlichten Nachrichten) oder Erstellungsdatum (bei Nachrichtenentwürfen) sortiert.

>[!NOTE]
>
>Jeder Benutzer kann auf Nachrichten zugreifen, Nachrichten erstellen, bearbeiten und veröffentlichen. Weitere Informationen zu Benutzerberechtigungen finden Sie in [diesem Abschnitt](../using/administration/permissions.md).

![](assets/messages-list.png)

Verwenden Sie den Umschalter **[!UICONTROL Aktuelle Nachrichten anzeigen]**, um den Nachrichten, die Sie in den letzten 5 Tagen geöffnet haben, direkte Links hinzuzufügen.

![](assets/show-recent-messages.png)

Klicken Sie auf das Filtersymbol, um nur Entwürfe, bereits veröffentlichte Nachrichten oder in Veröffentlichung befindliche Nachrichten anzuzeigen. Außerdem können Sie nach Nachrichtenbezeichnungen suchen:

![](assets/filter-messages.png)

## Erstellen einer neuen Nachricht

Gehen Sie wie folgt vor, um eine neue Nachricht zu erstellen:

1. Rufen Sie die Nachrichtenliste auf und klicken Sie anschließend auf **[!UICONTROL Nachricht erstellen]**.

1. Definieren Sie die Nachrichteneigenschaften.

   ![](assets/create-message-properties.png)

   * Geben Sie einen **[!UICONTROL Titel]** (obligatorisch) und eine **[!UICONTROL Beschreibung]** ein.

   * Wählen Sie die **[!UICONTROL Voreinstellung]** aus, die für die Nachricht verwendet werden soll.

      Voreinstellungen enthalten alle Parameter, die erforderlich sind, damit eine E-Mail- und/oder Push-Benachrichtigung markenkonform gesendet werden kann. [Weitere Informationen zu Vorgaben](../using/configuration/message-presets.md).

   * Wählen Sie den oder die Kanäle aus, die Sie für diese Nachricht nutzen möchten: E-Mail und/oder Push-Benachrichtigung. Sie müssen mindestens einen Kanal auswählen, um die Nachricht erstellen zu können.
   Beachten Sie, dass Sie über die Schaltfläche **[!UICONTROL Eigenschaften]** jederzeit auf Titel, Beschreibung und Voreinstellung der Nachricht zugreifen und diese ändern können.

   ![](assets/message-properties.png)


1. Klicken Sie auf **[!UICONTROL Erstellen]**, um die Nachrichtenerstellung zu bestätigen. Ihre Nachricht wird mit dem Status **[!UICONTROL Entwurf]** der Nachrichtenliste hinzugefügt.

   Für jeden ausgewählten Kanal steht eine Registerkarte zur Verfügung. Mit diesen Registerkarten können Sie den Inhalt für jeden Kanal konfigurieren. Um eine Registerkarte zu entfernen, wählen sie diese aus und klicken auf der rechten Seite auf die Schaltfläche **[!UICONTROL Kanal löschen]**.

   ![](assets/create-messages-content.png)

   Nun können Sie den Inhalt für die Nachricht erstellen und die Einstellungen anpassen. Detaillierte Informationen zur Konfiguration von E-Mails und Push-Benachrichtigungen finden Sie in den folgenden Abschnitten:

   * [Erstellen einer E-Mail](create-email.md)
   * [Push-Benachrichtigungen erstellen](create-push.md)

   >[!NOTE]
   >   
   >Sie können Ihre Nachrichten im Ausdruckseditor anhand der Profildaten personalisieren. Weiterführende Informationen zur Personalisierung finden Sie in [diesem Abschnitt](personalization/personalize.md).


1. Im Abschnitt „Vorschau“ auf der linken Seite können Sie das Nachrichten-Rendering anpassen und die Personalisierungseinstellungen mithilfe der Testprofile überprüfen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](preview.md).

   ![](assets/messages-simple-preview.png)

1. Überprüfen Sie Warnhinweise im oberen Abschnitt des Editors.  Einige davon sind einfache Warnhinweise, andere können die Veröffentlichung der Nachricht verhindern. Weiterführende Informationen finden Sie in diesem [Abschnitt](alerts.md).

1. Sie können Ihre Nachricht jetzt veröffentlichen, indem Sie auf die Schaltfläche **[!UICONTROL Veröffentlichen]** klicken, oder die Nachricht als Entwurf speichern und zu einem späteren Zeitpunkt veröffentlichen. Weiterführende Informationen zur Veröffentlichung von Nachrichten finden Sie in [diesem Abschnitt](publish-manage-message.md).

## Duplizieren einer Nachricht

Um eine Nachricht aus einer bestehenden Nachricht zu erstellen, verwenden Sie die Schaltfläche **[!UICONTROL Duplizieren]** im Nachrichtenbereich. Alle Einstellungen und Konfigurationen werden für die neue Nachricht übernommen.

![](assets/message-duplicate.png)

Sie können die Nachricht umbenennen, bevor Sie die Duplizierung bestätigen.

![](assets/message-duplicate-confirm.png)

Eine Bestätigungsmeldung wird am unteren Rand des Fensters angezeigt, sobald die neue Nachricht erstellt wurde.

Sie können eine Nachricht auch über die Nachrichtenliste durch Klicken auf das entsprechende Symbol duplizieren.

![](assets/message-duplicate-from-list.png)

Darauf folgt der gleiche Bestätigungsprozess.
