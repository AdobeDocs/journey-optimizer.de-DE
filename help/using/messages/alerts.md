---
title: Warnhinweise in Nachrichten
description: Erfahren Sie, wie Sie die Validierung von Nachrichteninhalten überprüfen und Fehler beheben können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 72%

---

# Überprüfen von Warnhinweisen für Ihre Nachrichten {#messages-alerts}

## Prüfungen vor dem Senden {#message-alerting}

Während Sie Ihre Nachrichten entwerfen, werden Warnhinweise auf der Benutzeroberfläche angezeigt, wenn wichtige Einstellungen fehlen.

Warnhinweise werden bei der Bearbeitung des Nachrichteninhalts oben rechts im Bildschirm angezeigt.

![](assets/alerts-details.png)

>[!NOTE]
>
>Wenn diese Schaltfläche nicht angezeigt wird, wurde kein Warnhinweis erkannt.

Es können zwei Arten von Warnhinweisen auftreten:

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. Wenn beispielsweise der Ausschluss-Link fehlt, wird eine Meldung angezeigt.

* **Fehler** verhindern, dass Sie die Journey testen oder aktivieren, solange sie nicht aufgelöst sind. Beispielsweise wird eine Meldung angezeigt, dass die Betreffzeile fehlt.

Alle möglichen Warnhinweise und Fehler sind [unten](#alerts-and-warnings) genauer beschrieben.

>[!CAUTION]
>
> Sie müssen alle **error** Warnhinweise vor dem Testen oder Aktivieren der Journey mithilfe der Nachricht.

## Liste von Warnhinweisen und Fehlern {#alerts-and-warnings}

Die vom System geprüften Einstellungen und Elemente sind unten aufgeführt. Sie finden hier auch Informationen zur Anpassung Ihrer Konfiguration, um die entsprechenden Probleme zu lösen.

**Warnungen**:

* **[!UICONTROL Der Ausschluss-Link ist nicht im E-Mail-Text vorhanden]**: Es empfiehlt sich, einen Link zur Abmeldung in Ihren E-Mail-Textkörper einzufügen. In [diesem Abschnitt](consent.md#opt-out-management) erfahren Sie, wie Sie diesen konfigurieren.

   >[!NOTE]
   >
   >E-Mail-Nachrichten vom Typ Marketing müssen einen Ausschluss-Link enthalten, der für Transaktionsnachrichten nicht erforderlich ist. Die Kategorie der Nachricht (**[!UICONTROL Marketing]** oder **[!UICONTROL Transactional]**) definiert wird unter [Kanaloberfläche](../configuration/message-presets.md#email-type) (d. h. Nachrichtenvorgabe) und wann [Nachricht erstellen](get-started-content.md#create-new-message).

* **[!UICONTROL Textversion von HTML ist leer]**: Vergessen Sie nicht, eine Textversion Ihres E-Mail-Textkörpers zu definieren, da diese verwendet wird, wenn HTML-Inhalte nicht angezeigt werden können. In [diesem Abschnitt](../design/text-version-email.md) erfahren Sie, wie Sie die Textversion erstellen.

* **[!UICONTROL Leerer Link ist im E-Mail-Text vorhanden]**: Überprüfen Sie, ob alle Links in Ihrer E-Mail korrekt sind. In [diesem Abschnitt](../design/create-email-content.md) erfahren Sie, wie Sie Inhalte und Links verwalten.

* **[!UICONTROL Die E-Mail-Größe überschreitet den Grenzwert von 100 KB]**: Stellen Sie sicher, dass die Größe Ihrer E-Mail 100 KB nicht überschreitet, um einen optimalen Versand zu erzielen. In [diesem Abschnitt](../design/create-email-content.md) erfahren Sie, wie Sie E-Mail-Inhalte bearbeiten.

**Fehler**:

* **[!UICONTROL Die Betreffzeile fehlt]**: Die E-Mail-Betreffzeile ist obligatorisch. In [diesem Abschnitt](create-email.md) erfahren Sie, wie Sie sie definieren und personalisieren.

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Die Push-Version der Nachricht ist leer]**: Dieser Fehler wird angezeigt, wenn der Text oder Titel der Push-Benachrichtigung fehlt. In [diesem Abschnitt](create-push.md) erfahren Sie, wie Sie den Inhalt einer Push-Benachrichtigung definieren.

* **[!UICONTROL Die E-Mail-Version der Nachricht ist leer]**: Dieser Fehler wird angezeigt, wenn der E-Mail-Inhalt nicht konfiguriert wurde. In [diesem Abschnitt](../design/design-emails.md) erfahren Sie, wie Sie E-Mail-Inhalte entwerfen.

* **[!UICONTROL Oberfläche existiert nicht]**: Sie können Ihre Nachricht nicht verwenden, wenn die ausgewählte Oberfläche nach der Nachrichtenerstellung gelöscht wird. Wenn dieser Fehler auftritt, wählen Sie eine andere Stelle in der Nachricht aus **[!UICONTROL Eigenschaften]**. Weitere Informationen zu Kanaloberflächen in [diesem Abschnitt](../configuration/message-presets.md).

* **[!UICONTROL Die Payload für Push-Benachrichtigungen an iOS-/Android überschreitet die Beschränkung von 4 KB]**: Die Größe der Push-Benachrichtigung darf 4 KB nicht überschreiten. Um diese Grenze zu beachten, versuchen Sie, die Verwendung von Bildern oder Emojis zu reduzieren. In [diesem Abschnitt](create-push.md) erfahren Sie, wie Sie Ihre Push-Benachrichtigungsinhalte verwalten.

>[!CAUTION]
>
> Um Ihre Nachricht verwenden zu können, müssen Sie alle **error** Warnhinweise.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
