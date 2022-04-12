---
title: Frequenzregeln
description: Erfahren Sie, wie Sie Häufigkeitsregeln definieren
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 1%

---

# Häufigkeitsregeln {#frequency-rules}

[!DNL Journey Optimizer] Sie können steuern, wie oft Benutzer eine Nachricht erhalten oder eine Journey eingeben, indem Sie kanalübergreifende Regeln festlegen, mit denen Profile, die zu oft angesprochen wurden, automatisch von Nachrichten und Aktionen ausgeschlossen werden.

Sie möchten beispielsweise nicht, dass Ihre Marke monatlich mehr als drei Marketing-Nachrichten an ihre Kunden sendet.

Hierfür können Sie eine Häufigkeitsregel verwenden, die die Anzahl der gesendeten Nachrichten auf der Basis eines oder mehrerer Kanäle während eines monatlichen Kalenderzeitraums begrenzt.

>[!NOTE]
>
>Die Regeln zur Nachrichtenhäufigkeit unterscheiden sich von der Opt-out-Verwaltung, die es Benutzern ermöglicht, sich vom Erhalt von Nachrichten einer Marke abzumelden. [Weitere Informationen](../messages/consent.md#opt-out-management)

## Zugriffsregeln {#access-rules}

Regeln sind im Abschnitt **[!UICONTROL Administration]** > **[!UICONTROL Regeln]** Menü. Alle Regeln werden aufgelistet, sortiert nach Änderungsdatum.

>[!NOTE]
>
>Zum Zugreifen auf, Erstellen, Bearbeiten oder Löschen von Regeln für die Häufigkeit von Nachrichten benötigen Sie die [Häufigkeitsregeln verwalten](../administration/high-low-permissions.md#manage-frequency-rules) Berechtigung.

![](assets/message-rules-access.png)

Verwenden Sie das Filtersymbol, um nach Kategorie, Status und/oder Kanal zu filtern. Sie können auch nach dem Titel der Nachricht suchen.

![](assets/message-rules-filter.png)

## Erstellen einer Regel {#create-new-rule}

Gehen Sie wie folgt vor, um eine neue Regel zu erstellen.

1. Zugriff auf **[!UICONTROL Häufigkeitsregeln]** Liste und klicken Sie auf **[!UICONTROL Regel erstellen]**.

   ![](assets/message-rules-create.png)

1. Definieren Sie den Regelnamen.

   ![](assets/message-rules-details.png)

1. Wählen Sie die Kategorie der Nachrichtenregel aus.

   >[!NOTE]
   >
   >Derzeit ist nur der **[!UICONTROL Marketing]** -Kategorie verfügbar ist.

1. Legen Sie die Begrenzung für Ihre Regel fest, d. h. die maximale Anzahl von Nachrichten, die monatlich an ein einzelnes Benutzerprofil gesendet werden können.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >Die Begrenzung der Häufigkeit basiert auf einem monatlichen Kalenderzeitraum. Er wird zu Beginn jedes Monats zurückgesetzt.

1. Wählen Sie den Kanal aus, den Sie für diese Regel verwenden möchten: **[!UICONTROL Email]** oder **[!UICONTROL Push-Benachrichtigung]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Sie müssen mindestens einen Kanal auswählen, um die Regel erstellen zu können.

1. Wählen Sie mehrere Kanäle aus, wenn Sie eine Begrenzung für alle ausgewählten Kanäle als Gesamtanzahl anwenden möchten.

   Legen Sie beispielsweise die Begrenzung auf 15 fest und wählen Sie sowohl den E-Mail- als auch den Push-Kanal aus. Wenn ein Profil bereits 10 Marketing-E-Mails und 5 Marketing-Push-Benachrichtigungen erhalten hat, wird dieses Profil vom nächsten Versand einer Marketing-E-Mail oder Push-Benachrichtigung ausgeschlossen.

1. Klicken **[!UICONTROL Als Entwurf speichern]** , um die Regelerstellung zu bestätigen. Ihre Nachricht wird in der Regelliste mit dem **[!UICONTROL Entwurf]** Status.

   ![](assets/message-rules-created.png)

## Aktivieren einer Regel {#activate-rule}

Bei der Erstellung einer Meldungsregel enthält die Regel **[!UICONTROL Entwurf]** -Status und hat noch keine Auswirkungen auf eine Nachricht. Um sie zu aktivieren, klicken Sie auf das Auslassungszeichen neben der Regel und wählen Sie **[!UICONTROL Aktivieren]**.

![](assets/message-rules-activate.png)

Das Aktivieren einer Regel wirkt sich auf alle Nachrichten aus, für die sie gilt, auf die nächste Ausführung aus. Erfahren Sie, wie Sie [Frequenzregel auf eine Nachricht anwenden](#apply-frequency-rule).

>[!NOTE]
>
>Sie müssen keine Nachrichten oder Journey ändern oder erneut veröffentlichen, damit eine Regel wirksam wird.

Um eine Meldungsregel zu deaktivieren, klicken Sie auf das Auslassungszeichen neben der Regel und wählen Sie **[!UICONTROL Deaktivieren]**.

![](assets/message-rules-deactivate.png)

Der Status der Regel ändert sich in **[!UICONTROL Inaktiv]** und die Regel gilt nicht für zukünftige Nachrichtenausführungen. Die aktuell ausgeführten Nachrichten sind nicht betroffen.

>[!NOTE]
>
>Das Deaktivieren einer Regel wirkt sich nicht auf die Zählung einzelner Profile aus oder setzt sie zurück.

## Häufigkeitsregel auf eine Nachricht anwenden {#apply-frequency-rule}

Gehen Sie wie folgt vor, um eine Häufigkeitsregel auf eine Nachricht anzuwenden.

1. Erstellen einer Nachricht. [Weitere Informationen](../messages/get-started-content.md#create-new-message)

1. Wählen Sie die Kategorie aus, die Sie für die [von Ihnen erstellte Regel](#create-new-rule).

   ![](assets/message-rules-msg-properties.png)

   >[!NOTE]
   >
   >Derzeit ist nur der **[!UICONTROL Marketing]** -Kategorie für Regeln zur Nachrichtenhäufigkeit verfügbar.

1. Wählen Sie die gewünschten Kanäle für Ihre Nachricht aus.

   ![](assets/message-rules-msg-channels.png)

1. Sie können auf die **[!UICONTROL Frequenzregel]** -Link, um die Häufigkeitsregeln anzuzeigen, die für die ausgewählte Kategorie und die ausgewählten Kanäle gelten.

   ![](assets/message-rules-msg-link.png)

   Daraufhin wird ein neuer Tab geöffnet, auf dem die entsprechenden Regeln zur Nachrichtenfrequenz angezeigt werden.

1. [Design](../design/design-emails.md) und [publish](../messages/publish-manage-message.md) Ihre Nachricht.

Alle Häufigkeitsregeln, die mit der ausgewählten Kategorie und den ausgewählten Kanälen übereinstimmen, werden automatisch auf diese Nachricht angewendet.

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

Die Anzahl der vom Versand ausgeschlossenen Profile können Sie im Abschnitt [Live- und globale Ansichten](../reports/message-monitoring.md)und im [E-Mail-Live-Bericht](../reports/email-live-report.md), wobei Häufigkeitsregeln als möglicher Grund für Benutzer aufgeführt werden, die vom Versand ausgeschlossen sind.

>[!NOTE]
>
>Für denselben Kanal können mehrere Regeln gelten, aber sobald die untere Begrenzung erreicht ist, wird das Profil von den nächsten Sendungen ausgeschlossen.

## Beispiel: mehrere Regeln kombinieren {#frequency-rule-example}

Sie können mehrere Regeln zur Nachrichtenhäufigkeit kombinieren, wie im folgenden Beispiel beschrieben.

1. [Regel erstellen](#create-new-rule) aufgerufen *Marketing-Gesamtbegrenzung*:

   * Wählen Sie alle Kanäle aus (E-Mail, Push).
   * Legen Sie die Begrenzung auf 12 fest.

   ![](assets/message-rules-ex-overall-cap.png)

1. Erstellen Sie eine zweite Regel namens *Push Marketing Cap*:

   * Wählen Sie Push-Kanal aus.
   * Legen Sie die Begrenzung auf 4 fest.

   ![](assets/message-rules-ex-push-cap.png)

1. Speichern und [Aktivieren](#activate-rule) die Regel.

1. Erstellen einer Nachricht. [Weitere Informationen](../messages/get-started-content.md#create-new-message)

1. Wählen Sie die **[!UICONTROL Marketing]** Kategorie.

   ![](assets/message-rules-ex-category-maktg.png)

1. Wählen Sie die **[!UICONTROL Email]** und **[!UICONTROL Push-Benachrichtigung]** Kanäle.

   ![](assets/message-rules-ex-channels.png)

1. Sie können auf die **[!UICONTROL Frequenzregel]** -Link, um die Häufigkeitsregeln anzuzeigen, die für die ausgewählte Kategorie und die ausgewählten Kanäle gelten.

1. [Design](../design/design-emails.md) und [publish](../messages/publish-manage-message.md) Ihre Nachricht.

In diesem Szenario ein einzelnes Profil:
* kann monatlich bis zu 12 Marketingnachrichten erhalten;
* jedoch von Marketing-Push-Benachrichtigungen ausgeschlossen, nachdem sie 4 Push-Benachrichtigungen erhalten haben.
