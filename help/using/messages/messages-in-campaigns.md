---
title: Hinzufügen von Nachrichten in Kampagnen
description: Erfahren Sie, wie Sie Nachrichten zu einer Kampagne hinzufügen
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 81%

---


# Hinzufügen von Nachrichten in Kampagnen{#messages-in- campaigns}

Wählen Sie in Ihren Kampagnen den Kanal aus, den Sie entwerfen und personalisieren möchten, welche Nachricht Sie an Ihre Audience senden möchten. Wenn Sie eine E-Mail, eine SMS oder eine Push-Benachrichtigung zu Ihrer Kampagne hinzufügen, können Sie sie sofort senden oder die Nachricht planen.

>[!NOTE]
>Sie können auch Journey erstellen, um ausgelöste Nachrichten zu senden. Weiterführende Informationen finden Sie [in diesem Abschnitt](messages-in-journeys.md).

Erfahren Sie, wie Sie Nachrichten in einer Kampagne hinzufügen und konfigurieren [in diesem Abschnitt](../campaigns/create-campaign.md)

Auf der folgenden Seite erfahren Sie mit detaillierten Schritten, wie Sie Ihren Nachrichteninhalt erstellen:

* [Erstellen einer E-Mail](create-email.md)
* [Erstellen einer Push-Benachrichtigung](create-push.md)
* [Erstellen einer SMS-Nachricht](create-sms.md)

## Aktivieren der Sendezeitoptimierung{#sto-in-journeys}

Für E-Mail- und Push-Benachrichtigungen können Sie die **[!UICONTROL Sendezeitoptimierung]** aktivieren.

Verwenden Sie die **[!UICONTROL Sendezeitoptimierung]**, um jeweils personalisierte Sendezeiten für Benutzende zu planen und die Öffnungs- und Klickraten Ihrer Nachrichten zu erhöhen. [Weitere Informationen](../messages/send-time-optimization.md).

## Erweiterte Parameter{#adv-settings}

Erweiterte Parameter sind schreibgeschützt und standardmäßig ausgeblendet.

Um auf erweiterte Parameter zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Schreibgeschützte Felder anzeigen]** im oberen Bereich des Nachrichtenfensters.

![](assets/show-read-only.png)

Erweiterte Parameter werden am unteren Rand des Nachrichtenfensters angezeigt. Diese Parameter werden von den [Systemadmins](../start/path/administrator.md) in der [Kanaloberfläche](../configuration/channel-surfaces.md) (d. h. der Nachrichtenvoreinstellung) definiert, die mit der Nachricht verbunden ist.

Für Push-Benachrichtigungen können Sie die folgenden Parameter anzeigen: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Für E-Mails können Sie die primäre E-Mail-Adresse anzeigen.

Für bestimmte Zwecke können Sie diese Werte in bestimmten Kontexten überschreiben. Um einen bestimmten Wert zu erzwingen, können Sie das Symbol **Parameterüberschreibung aktivieren** rechts neben dem Feld anklicken. Diese Option kann zum Beispiel für folgende Zwecke nützlich sein:

* Um eine E-Mail zu testen, können Sie Ihre E-Mail-Adresse hinzufügen. Nachdem Sie die Journey veröffentlicht haben, wird die E-Mail an Sie gesendet.
* Sie können auf die E-Mail-Adresse der Abonnenten einer Liste verweisen. Weitere Informationen finden Sie in [diesem Anwendungsbeispiel](../building-journeys/message-to-subscribers-uc.md).

Klicken Sie auf dasselbe Symbol, um erweiterte Einstellungen auszublenden.

## Nachrichten durchsuchen{#browse-message}

Wenn mehrere Nachrichten in einer Journey verwendet werden, können Sie auf dem Bildschirm **Inhalt bearbeiten** von einer zur anderen wechseln.

![](assets/inline-messages-multi-content.png)

Sie können dann [Warnungen überprüfen](alerts.md) und jeden Inhalt in einer einzigen Ansicht [simulieren](../design/preview.md).

## Duplizieren einer Nachricht {#duplicate-message}

Sie können eine vorhandene Nachricht von der Journey-Arbeitsfläche kopieren.

Gehen Sie dazu wie folgt vor:

1. Wählen Sie die Nachricht aus, die Sie kopieren möchten.

1. Verwenden Sie die Schaltfläche **[!UICONTROL Kopieren]** im Bereich **[!UICONTROL Aktion]**.

   ![](assets/message-duplicate.png)

1. Geben Sie **Strg+V** ein, um die Nachricht einzufügen.

   Die Nachricht wird der Journey-Arbeitsfläche hinzugefügt. Alle Einstellungen und Konfigurationen werden für die neue Nachricht übernommen.

   ![](assets/message-duplicated.png)

1. Benennen Sie die Nachricht um, um die ursprüngliche Nachricht von der Kopie zu unterscheiden, beispielsweise bei der Bearbeitung von Nachrichten, wie im Folgenden beschrieben:

   ![](assets/multi-message.png)


>[!NOTE]
>
>Bei E-Mails können Sie auch eine vorhandene Nachricht in eine Vorlage umwandeln. [Weitere Informationen](../design/email-templates.md).

## Eine Nachricht löschen{#delete-message}

Um eine Nachricht zu löschen, verwenden Sie das Papierkorbsymbol oben im Aktivitätsbereich für die Kanalaktivität.

![](assets/delete-message.png)

Verwenden Sie die Taste **[!UICONTROL Bestätigen]**, um zu bestätigen.
