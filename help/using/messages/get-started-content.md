---
title: Erste Schritte mit Nachrichten
description: Erfahren Sie, wie Sie in Journey Optimizer personalisierte Nachrichten erstellen und versenden können
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 100%

---

# Erste Schritte mit Nachrichten {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Kanalaktionen"
>abstract="Verwenden Sie Kanalaktionen, um eine Push-, SMS- oder E-Mail-Nachricht zu senden."

Verwenden Sie [!DNL Journey Optimizer], um personalisierte Push-Benachrichtigungen, SMS und E-Mail-Nachrichten zu erstellen und zu versenden. Alle Nachrichten können im Rahmen einer Aktion auf der Journey-Arbeitsfläche inline bearbeitet werden.  Verwenden Sie die Funktion „Als Vorlage speichern“, um Ihren Inhalt ganz einfach wiederzuverwenden. Sie haben folgende Möglichkeiten:

* Verwenden Sie [!DNL Journey Optimizer] **Funktionen zur E-Mail-Gestaltung**, um responsive E-Mails zu erstellen bzw. zu importieren.

* Nutzen Sie die Möglichkeiten von **Adobe Experience Manager Assets Essentials**, um Ihre E-Mails zu gestalten und um Ihre eigene Asset-Datenbank zu erstellen und verwalten.

* Suchen Sie **Adobe Stock-Fotos**, um Ihre Inhalte zu erstellen und Ihr E-Mail-Design zu verbessern.

* Verbessern Sie das Kundenerlebnis durch die Erstellung personalisierter **Push-Benachrichtigungen, SMS und E-Mails** basierend auf ihren Profilattributen.

* **Versenden Sie Sendungen**, die auf diesen Inhalten basieren, und verfolgen Sie das Kundenverhalten.

>[!NOTE]
>
>Benutzende können je nach ihrem Produktprofil auf Journeys zugreifen und Journeys erstellen, bearbeiten und/oder veröffentlichen. Weitere Informationen zu Benutzerberechtigungen finden Sie in [diesem Abschnitt](../administration/permissions.md).


## Hinzufügen von Nachrichten in Ihren Journeys{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Nachrichtenkategorie"
>abstract="Wählen Sie „Marketing“ für kommerzielle Nachrichten oder „Transaktionsnachrichten“ für nicht kommerzielle Nachrichten wie Bestellbestätigungen, Benachrichtigungen zum Zurücksetzen des Kennworts oder Versandinformationen."

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Kanaloberfläche"
>abstract="Eine Kanaloberfläche ist eine Instanz des betreffenden Kanals, die über alle nötigen Einstellungen verfügt, um eine Aktion erfolgreich über eine Kampagne oder eine Journey bereitzustellen. Sie wird von Systemadmins definiert."

Um Nachrichten in Ihre Journeys einzufügen, fügen Sie ganz einfach eine Push-, SMS- oder E-Mail-Aktivität in die Journey-Arbeitsfläche ein.

1. Beginnen Sie Ihre Journey mit einem [Ereignis](../building-journeys/general-events.md) oder einer Aktivität vom Typ [Segment lesen](../building-journeys/read-segment.md).

1. Ziehen Sie aus dem Abschnitt **Aktionen** der Palette eine Aktivität vom Typ **E-Mail**, **SMS** oder **Push** auf die Arbeitsfläche.

   ![](assets/add-a-message.png)

1. Geben Sie einen Titel und eine Beschreibung ein.

1. Wählen Sie die **[!UICONTROL Kategorie]** der Nachricht: Wählen Sie **Marketing** für kommerzielle Nachrichten oder **Transaktionsnachrichten** für nicht-kommerzielle Nachrichten wie Auftragsbestätigungen, Benachrichtigungen zum Zurücksetzen des Kennworts oder Lieferinformationen.

   >[!CAUTION]
   >
   >Wenn Sie [Häufigkeitsregeln](../configuration/frequency-rules.md) für einen bestimmten Kanal und eine bestimmte Kategorie festgelegt haben, werden diese bei der Auswahl des Kanals und der Kategorie automatisch auf die Nachricht angewendet. Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** für Häufigkeitsregeln verfügbar.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >Nachrichten vom Typ Marketing müssen einen [Ausschluss-Link](../messages/consent.md#opt-out-management) enthalten. Dies ist für Transaktionsnachrichten nicht erforderlich, da diese Nachrichten an Profile gesendet werden können, die sich von Marketing-Nachrichten abgemeldet haben.

1. Wählen Sie die **[!UICONTROL Kanaloberfläche]** (d. h. Nachrichtenvorgabe), die zum Senden Ihrer Nachricht verwendet werden soll.

   Eine Oberfläche ist eine Konfiguration, die durch [Systemadmins](../start/path/administrator.md) definiert worden ist. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Weitere Informationen](../configuration/channel-surfaces.md).

   >[!CAUTION]
   >
   >Sie müssen eine gültige Kanaloberfläche für die ausgewählte Nachrichtenkategorie und den ausgewählten Kanal wählen.

   Sie können Titel, Beschreibung und Oberfläche der Nachricht jederzeit über die Schaltfläche **[!UICONTROL Eigenschaften]** in der Nachrichtenschnittstelle aufrufen und ändern.

1. Nachrichteninhalt erstellen.

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

Erweiterte Parameter werden am unteren Rand des Nachrichtenfensters angezeigt. Diese Parameter werden von den [Systemadmins](../start/path/administrator.md) in der [Kanaloberfläche](../configuration/channel-surfaces.md) (d. h. der Nachrichtenvorgabe) definiert, die mit der Nachricht verbunden ist.

Für Push-Benachrichtigungen können Sie die folgenden Parameter anzeigen: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Für E-Mails können Sie die primäre E-Mail-Adresse anzeigen.

Für bestimmte Zwecke können Sie diese Werte in bestimmten Kontexten überschreiben. Um einen bestimmten Wert zu erzwingen, können Sie das Symbol **Parameterüberschreibung aktivieren** rechts neben dem Feld anklicken. Diese Option kann zum Beispiel für folgende Zwecke nützlich sein:

* Um eine E-Mail zu testen, können Sie Ihre E-Mail-Adresse hinzufügen. Nachdem Sie die Journey veröffentlicht haben, wird die E-Mail an Sie gesendet.
* Sie können auf die E-Mail-Adresse der Abonnenten einer Liste verweisen. Weitere Informationen finden Sie in [diesem Anwendungsbeispiel](../building-journeys/message-to-subscribers-uc.md).

Klicken Sie zum Zurücksetzen auf den Standardparameter auf das gleiche Symbol.


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
