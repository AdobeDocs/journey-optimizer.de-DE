---
title: Warnhinweise in Nachrichten
description: Erfahren Sie, wie Sie die Validierung von Nachrichteninhalten überprüfen und Fehler beheben können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: f5b629d5e413a3ffc037af959c5e16b9a47e8a0e
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 62%

---

# Überprüfen von Warnhinweisen für Ihre Nachrichten {#publish-manage-messages}

## Prüfungen vor der Veröffentlichung {#message-alerting}

Während Sie Ihre Nachricht erstellen, werden Sie durch Warnhinweise informiert, wenn Sie wichtige Aktionen ausführen müssen, bevor Sie die Nachricht veröffentlichen.

Warnhinweise werden oben rechts im Bildschirm angezeigt, wie unten dargestellt:

![](assets/message-alerts.png)

>[!NOTE]
>
>Wenn diese Schaltfläche nicht angezeigt wird, wurde kein Warnhinweis erkannt.

Es können zwei Arten von Warnhinweisen auftreten:

* **Warnhinweise** geben Hinweise auf Empfehlungen und zeigen Best Practices. Wenn beispielsweise der Ausschluss-Link fehlt, wird eine Meldung angezeigt.

* **Fehler** verhindern, dass Sie die Nachricht veröffentlichen, solange sie nicht behoben sind. Beispielsweise wird eine Meldung angezeigt, dass die Betreffzeile fehlt.

Alle möglichen Warnhinweise und Fehler sind [unten](#alerts-and-warnings) genauer beschrieben.

>[!CAUTION]
>
> Sie müssen alle **Fehler**-Warnungen vor der Veröffentlichung auflösen.

## Liste von Warnhinweisen und Fehlern {#alerts-and-warnings}

Die vom System geprüften Einstellungen und Elemente sind unten aufgeführt. Sie finden hier auch Informationen zur Anpassung Ihrer Konfiguration, um die entsprechenden Probleme zu lösen.

**Warnungen**:

* **[!UICONTROL Der Abmelde-Link ist im E-Mail-Textkörper nicht vorhanden.]**: Es empfiehlt sich, einen Abmelde-Link in Ihren E-Mail-Textkörper einzufügen. In [diesem Abschnitt](consent.md) erfahren Sie, wie Sie diesen konfigurieren.

* **[!UICONTROL Textversion von HTML ist leer.]**: Vergessen Sie nicht, eine Textversion Ihres E-Mail-Textkörpers zu definieren, da diese verwendet wird, wenn keine HTML-Inhalte angezeigt werden können. In [diesem Abschnitt](create-email-content.md#generate-text-version) erfahren Sie, wie Sie die Textversion erstellen.

* **[!UICONTROL Leerer Link ist im E-Mail-Textkörper vorhanden.]**: Überprüfen Sie, ob alle Links in Ihrer E-Mail korrekt sind. In [diesem Abschnitt](create-email-content.md) erfahren Sie, wie Sie Inhalte und Links verwalten.

* **[!UICONTROL Die E-Mail-Größe hat die Grenze von 100 KB überschritten.]**: Um einen optimalen Versand zu gewährleisten, sollten Sie sicherstellen, dass die Größe Ihrer E-Mail 100 KB nicht überschreitet. In [diesem Abschnitt](create-email-content.md) erfahren Sie, wie Sie E-Mail-Inhalte bearbeiten.

**Fehler**:

* **[!UICONTROL Die Betreffzeile fehlt.]**: E-Mail-Betreffzeile ist obligatorisch. In [diesem Abschnitt ](create-email.md) erfahren Sie, wie Sie sie definieren und personalisieren.

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Die Push-Version der Nachricht ist leer.]**: Dieser Fehler wird angezeigt, wenn der Text oder Titel der Push-Benachrichtigung fehlt. In [diesem Abschnitt](create-push.md) erfahren Sie, wie Sie Push-Benachrichtigungs-Inhalte definieren.

* **[!UICONTROL Die E-Mail-Version der Nachricht ist leer.]**: wird dieser Fehler angezeigt, wenn der E-Mail-Inhalt nicht konfiguriert wurde. In [diesem Abschnitt](design-emails.md) erfahren Sie, wie Sie E-Mail-Inhalte entwerfen.

* **[!UICONTROL Vorgabe existiert nicht.]**: Sie können Ihre Nachricht nicht veröffentlichen, wenn die ausgewählte Vorgabe nach der Nachrichtenerstellung gelöscht wurde. Wenn dieser Fehler auftritt, wählen Sie in den **[!UICONTROL Eigenschaften]** der Nachricht eine andere Voreinstellung aus. Weitere Informationen zum Branding finden Sie in [diesem Abschnitt](../configuration/about-subdomain-delegation.md).

* **[!UICONTROL Die Push-iOS/Android-Payload hat die Beschränkung von 4 KB überschritten.]**: Die Größe der Push-Benachrichtigung darf 4 KB nicht überschreiten. Um diese Grenze zu beachten, versuchen Sie, die Verwendung von Bildern oder Emojis zu reduzieren. In [diesem Abschnitt](create-push.md) erfahren Sie, wie Sie Ihre Push-Benachrichtigungsinhalte verwalten.

>[!CAUTION]
>
> Um Ihre Nachricht veröffentlichen zu können, müssen Sie alle **Fehler**-Warnungen auflösen.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
