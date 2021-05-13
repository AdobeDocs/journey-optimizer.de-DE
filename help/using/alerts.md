---
title: Warnungen in Nachrichten
description: Erfahren Sie, wie Sie die Überprüfung des Nachrichteninhalts überprüfen und Fehler beheben können
translation-type: tm+mt
source-git-commit: 03af839084edafbc93188750db1f9f6c8b559d9e
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Warnungen für Ihre Nachrichten {#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## Prüft vor der Veröffentlichung {#message-alerting}

Während Sie Ihre Nachricht erstellen, werden Sie durch Warnhinweise gewarnt, wenn Sie wichtige Aktionen ausführen müssen, bevor Sie die Nachricht veröffentlichen.

Warnungen werden oben rechts im Bildschirm angezeigt, wie unten dargestellt:

![](assets/message-alerts.png)

>[!NOTE]
>
>Wenn diese Schaltfläche nicht angezeigt wird, wurde keine Warnung erkannt.

Es können zwei Arten von Warnungen auftreten:

* **** Warnungen beziehen sich auf Empfehlungen und bewährte Verfahren. Wenn beispielsweise der Ausschluss-Link fehlt, wird eine Meldung angezeigt.

* **Es wird** Fehler behoben, der Sie daran hindert, die Nachricht zu veröffentlichen, solange sie nicht aufgelöst wurde. Beispielsweise wird eine Meldung angezeigt, dass die Betreffzeile fehlt.

Alle möglichen Warnungen und Fehler sind [unten](#alerts-and-warnings) detailliert.

>[!CAUTION]
>
> Sie müssen alle **error**-Warnungen vor der Veröffentlichung auflösen.

## Liste von Warnungen und Fehlern {#alerts-and-warnings}

Die vom System geprüften Einstellungen und Elemente sind unten aufgeführt. Sie finden hier auch Informationen zur Anpassung Ihrer Konfiguration, um die entsprechenden Probleme zu lösen.

**Warnungen**:

* **[!UICONTROL Opt-out Link nicht im E-Mail-Text]** vorhanden: Es empfiehlt sich, einen Link zur Abmeldung in Ihren E-Mail-Textkörper einzufügen. Erfahren Sie, wie Sie es in [diesem Abschnitt](consent.md) konfigurieren.

* **[!UICONTROL Textversion von HTML ist leer]**: Vergessen Sie nicht, eine Textversion Ihres E-Mail-Textkörpers zu definieren, da diese verwendet wird, wenn HTML-Inhalte nicht angezeigt werden können. Erfahren Sie, wie Sie die Textversion in [diesem Abschnitt](create-email-content.md#generate-text-version) erstellen.

* **[!UICONTROL Leerer Link ist im E-Mail-Text]** vorhanden: Überprüfen Sie, ob alle Links in Ihrer E-Mail korrekt sind. Erfahren Sie, wie Sie Inhalte und Links in [diesem Abschnitt](create-email-content.md) verwalten.

* **[!UICONTROL Die E-Mail-Größe überschreitet den Grenzwert von 100 KB]**: stellen Sie sicher, dass die Größe Ihrer E-Mail 100 KB nicht überschreitet, um einen optimalen Versand zu erzielen. Erfahren Sie, wie Sie E-Mail-Inhalte in [diesem Abschnitt](create-email-content.md) bearbeiten.

**Fehler**:

* **[!UICONTROL Betreffzeile nicht vorhanden]**: Betreffzeile per E-Mail ist obligatorisch. In [diesem Abschnitt ](configure-email.md) erfahren Sie, wie Sie es definieren und personalisieren.

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push-Variante ist leer]**: dieser Fehler wird angezeigt, wenn der Text oder Titel der Push-Benachrichtigung fehlt. Erfahren Sie, wie Sie Push-Benachrichtigungsinhalte in [diesem Abschnitt](configure-push.md) definieren.

* **[!UICONTROL E-Mail-Variante ist leer]**: dieser Fehler wird angezeigt, wenn der E-Mail-Inhalt nicht konfiguriert wurde. Erfahren Sie, wie Sie E-Mail-Inhalte in [diesem Abschnitt](design-emails.md) entwerfen.

* **[!UICONTROL Vorgabe ist nicht vorhanden]**: Sie können Ihre Nachricht nicht veröffentlichen, wenn die ausgewählte Vorgabe nach der Erstellung der Nachricht gelöscht wurde. Wenn dieser Fehler auftritt, wählen Sie in der Meldung **[!UICONTROL Eigenschaften]** eine andere Vorgabe aus. Weitere Informationen zum Branding finden Sie in [diesem Abschnitt](administration.md#cjm-branding).

* **[!UICONTROL Die Push-iOS-/Android-Nutzlast überschreitet die Beschränkung von 4 KB]**: Die Größe der Push-Benachrichtigung darf 4 KB nicht überschreiten. Um diese Grenze zu beachten, versuchen Sie, die Verwendung von Bildern oder Emojis zu reduzieren. Erfahren Sie, wie Sie Ihre Push-Benachrichtigungsinhalte in [diesem Abschnitt](configure-push.md) verwalten.

>[!CAUTION]
>
> Um Ihre Nachricht veröffentlichen zu können, müssen Sie alle **error**-Warnungen auflösen.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
