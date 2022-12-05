---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen von Nachrichten in Journeys
description: Erfahren Sie, wie Sie Nachrichten zu einer Journey hinzufügen
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: acb5b65b-8787-4428-9924-36aa0a115926
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 98%

---

# Hinzufügen von Nachrichten in Journeys{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Nachrichtenkategorie"
>abstract="Wählen Sie „Marketing“ für kommerzielle Nachrichten oder „Transaktionsnachrichten“ für nicht kommerzielle Nachrichten wie Bestellbestätigungen, Benachrichtigungen zum Zurücksetzen des Kennworts oder Versandinformationen."

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Kanaloberfläche"
>abstract="Eine Kanaloberfläche ist eine Instanz des betreffenden Kanals, die über alle nötigen Einstellungen verfügt, um eine Aktion erfolgreich über eine Kampagne oder eine Journey bereitzustellen. Sie wird von Systemadmins definiert."

Verwenden Sie in Ihren Journeys die Kanalaktionen, um die Nachricht, die Sie an Ihre Audience senden möchten, zu gestalten und zu personalisieren. Wenn Sie eine E-Mail-, eine SMS- oder eine Push-Aktion zur Journey-Arbeitsfläche hinzufügen, erstellen Sie einen ausgelösten Versand. Wenn Kontakte diese Kanalaktion erreichen, sendet Adobe Journey Optimizer die Nachricht automatisch.


>[!NOTE]
>Sie können auch Kampagnen erstellen, um geplante Nachrichten zu senden. Weiterführende Informationen finden Sie [in diesem Abschnitt](../campaigns/get-started-with-campaigns.md).


Um Nachrichten in eine Journey einzufügen, fügen Sie eine Push-, SMS- oder E-Mail-Aktivität in die Journey-Arbeitsfläche ein.

1. Beginnen Sie Ihre Journey mit einem [Ereignis](../building-journeys/general-events.md) oder einer Aktivität vom Typ [Segment lesen](../building-journeys/read-segment.md).

1. Ziehen Sie aus dem Abschnitt **Aktionen** der Palette eine Aktivität vom Typ **E-Mail**, **SMS** oder **Push** auf die Arbeitsfläche.

   ![](assets/add-a-message.png)

1. Geben Sie einen Titel und eine Beschreibung ein.

1. Wählen Sie die **[!UICONTROL Kategorie]** der Nachricht: Wählen Sie **Marketing** für kommerzielle Nachrichten oder **Transaktionsnachrichten** für nicht-kommerzielle Nachrichten wie Auftragsbestätigungen, Benachrichtigungen zum Zurücksetzen des Kennworts oder Versandinformationen.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >* Wenn Sie [Häufigkeitsregeln](../configuration/frequency-rules.md) für einen bestimmten Kanal und eine bestimmte Kategorie festgelegt haben, werden diese bei der Auswahl des Kanals und der Kategorie automatisch auf die Nachricht angewendet. Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** für Häufigkeitsregeln verfügbar.
   >
   >* Nachrichten vom Typ Marketing müssen einen [Ausschluss-Link](../privacy/opt-out.md#opt-out-management) enthalten. Dies ist für Transaktionsnachrichten nicht erforderlich, da diese Nachrichten an Profile gesendet werden können, die sich von Marketing-Nachrichten abgemeldet haben.


1. Wählen Sie die **[!UICONTROL Kanaloberfläche]** (d. h. Nachrichtenvoreinstellung), die zum Senden Ihrer Nachricht verwendet werden soll.

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

Um auf erweiterte Parameter zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Schreibgeschützte Felder anzeigen]** im oberen Bereich des Nachrichtenfensters. Klicken Sie auf dasselbe Symbol erneut, um erweiterte Einstellungen auszublenden.

![](assets/show-read-only.png)

Erweiterte Parameter werden am unteren Rand des Nachrichtenfensters angezeigt. Diese Parameter werden von den [Systemadmins](../start/path/administrator.md) in der [Kanaloberfläche](../configuration/channel-surfaces.md) (d. h. der Nachrichtenvoreinstellung) definiert, die mit der Nachricht verbunden ist.

Für Push-Benachrichtigungen können Sie die folgenden Parameter anzeigen: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

>[!NOTE]
>
>Wenn Sie eines dieser Attribute überschreiben, müssen auch alle drei überschrieben werden.

Für E-Mails können Sie die [primäre E-Mail-Adresse](../configuration/primary-email-addresses.md) anzeigen.

In bestimmten Kontexten können Sie diese Werte für eine bestimmte Verwendung überschreiben. Um einen bestimmten Wert zu erzwingen, können Sie das Symbol **[!UICONTROL Parameterüberschreibung aktivieren]** rechts neben dem Feld anklicken.

![](assets/email-adv-parameters.png)

Diese Option kann zum Beispiel für folgende Zwecke nützlich sein:

* Testen einer E-Mail-Adresse. Sie können Ihre eigene E-Mail-Adresse hinzufügen, und nachdem Sie die Journey veröffentlicht haben, wird die E-Mail an Sie gesendet.
* Sie können auf die E-Mail-Adresse der Abonnenten einer Liste verweisen. Weitere Informationen finden Sie in [diesem Anwendungsbeispiel](../building-journeys/message-to-subscribers-uc.md).

>[!NOTE]
>
>Das Überschreiben von E-Mail-Adressen sollte nur für bestimmte Anwendungsfälle verwendet werden. Meistens müssen Sie die E-Mail-Adresse nicht ändern, da der Wert, der als die primäre Adresse in den **[!UICONTROL Ausführungsfeldern]** definiert ist, derjenige ist, der verwendet werden sollte. [Weitere Informationen](../configuration/primary-email-addresses.md)

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

1. Benennen Sie die Nachricht um, damit Sie die ursprüngliche Nachricht von der Kopie unterscheiden können, beispielsweise bei der Bearbeitung von Nachrichten, wie unten dargestellt:

   ![](assets/multi-message.png)


>[!NOTE]
>
>Bei E-Mails können Sie auch eine vorhandene Nachricht in eine Vorlage umwandeln. [Weitere Informationen](../design/email-templates.md).

## Eine Nachricht löschen{#delete-message}

Um eine Nachricht zu löschen, verwenden Sie das Papierkorbsymbol oben im Aktivitätsbereich für die Kanalaktivität.

![](assets/delete-message.png)

Verwenden Sie die Taste **[!UICONTROL Bestätigen]**, um zu bestätigen.
