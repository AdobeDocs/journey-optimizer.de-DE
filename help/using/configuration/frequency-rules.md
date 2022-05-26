---
title: Häufigkeitsregeln
description: Erfahren Sie, wie Sie Häufigkeitsregeln definieren
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: dd60e576aaded21efd9718341d1c4f26267ae001
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 84%

---

# Häufigkeitsregeln für Nachrichten {#frequency-rules}

Mit [!DNL Journey Optimizer] können Sie steuern, wie oft Benutzer eine Nachricht erhalten oder in eine Journey eintreten, indem Sie kanalübergreifende Regeln festlegen, mit denen zu oft angesprochene Profile automatisch von Nachrichten und Aktionen ausgeschlossen werden.

Nehmen wir an, Sie möchten verhindern, dass Ihre Marke monatlich mehr als drei Marketing-Nachrichten an Ihre Kunden sendet.

Hierfür können Sie eine Häufigkeitsregel verwenden, die die Anzahl der gesendeten Nachrichten über einen oder mehrere Kanäle während eines monatlichen Kalenderzeitraums begrenzt.

>[!NOTE]
>
>Die Regeln zur Nachrichtenhäufigkeit unterscheiden sich von der Opt-out-Verwaltung, die es Benutzern ermöglicht, sich vom Erhalt von Nachrichten einer Marke abzumelden. [Weitere Informationen](../messages/consent.md#opt-out-management)

## Zugriff auf Regeln {#access-rules}

Sie können auf Regeln über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Regeln]** zugreifen. Alle Regeln werden sortiert nach Änderungsdatum aufgelistet.

Verwenden Sie das Filtersymbol, um die Regeln nach Kategorie, Status und/oder Kanal zu filtern. Sie können auch nach dem Nachrichtentitel suchen.

![](assets/message-rules-filter.png)

### Berechtigungen{#permissions-frequency-rules}

Zum Zugreifen auf, Erstellen, Bearbeiten oder Löschen von Häufigkeitsregeln für Nachrichten benötigen Sie die Berechtigung **[!UICONTROL Häufigkeitsregeln verwalten]**.

Benutzer mit **[!UICONTROL Anzeigen von Häufigkeitsregeln]** -Berechtigungen können Regeln anzeigen, sie jedoch nicht ändern oder löschen.

![](assets/message-rules-access.png)

Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/high-low-permissions.md).

## Erstellen einer Regel {#create-new-rule}

Gehen Sie wie folgt vor, um eine neue Regel zu erstellen.

1. Öffnen Sie die Liste **[!UICONTROL Häufigkeitsregeln für Nachrichten]** und klicken Sie auf **[!UICONTROL Regel erstellen]**.

   ![](assets/message-rules-create.png)

1. Definieren Sie den Namen der Regel.

   ![](assets/message-rules-details.png)

1. Wählen Sie die Kategorie der Nachrichtenregel aus.

   >[!NOTE]
   >
   >Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** verfügbar.

1. Legen Sie die Begrenzung für Ihre Regel fest, d. h. die maximale Anzahl von Nachrichten, die monatlich an ein einzelnes Benutzerprofil gesendet werden kann.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >Die Häufigkeitsbegrenzung basiert auf einem monatlichen Kalenderzeitraum. Sie wird zu Beginn jedes Monats zurückgesetzt.

1. Wählen Sie den Kanal aus, den Sie für diese Regel verwenden möchten: **[!UICONTROL E-Mail]** oder **[!UICONTROL Push-Benachrichtigung]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Sie müssen mindestens einen Kanal auswählen, um die Regel erstellen zu können.

1. Wählen Sie mehrere Kanäle aus, wenn Sie für alle ausgewählten Kanäle gemeinsam eine Begrenzung festlegen möchten.

   Legen Sie beispielsweise die Begrenzung auf 15 fest und wählen Sie sowohl den E-Mail- als auch den Push-Kanal aus. Wenn ein Profil bereits 10 Marketing-E-Mails und 5 Marketing-Push-Benachrichtigungen erhalten hat, wird dieses Profil vom nächsten Versand einer Marketing-E-Mail oder Push-Benachrichtigung ausgeschlossen.

1. Klicken Sie auf **[!UICONTROL Als Entwurf speichern]**, um die Regelerstellung zu bestätigen. Ihre Nachricht wird zur Regelliste hinzugefügt, wobei die **[!UICONTROL Entwurf]** Status.

   ![](assets/message-rules-created.png)

## Aktivieren einer Regel {#activate-rule}

Bei der Erstellung einer Meldungsregel enthält die Regel **[!UICONTROL Entwurf]** -Status und hat noch keine Auswirkungen auf eine Nachricht. Um die Regel zu aktivieren, klicken Sie auf die Auslassungszeichen neben der Regel und wählen Sie **[!UICONTROL Aktivieren]** aus.

![](assets/message-rules-activate.png)

Das Aktivieren einer Regel wirkt sich auf alle Nachrichten, für die sie gilt, bei ihrer nächsten Ausführung aus. Erfahren Sie, wie Sie [eine Häufigkeitsregel auf eine Nachricht anwenden](#apply-frequency-rule).

>[!NOTE]
>
>Es kann bis zu 10 Minuten dauern, bis eine Regel vollständig aktiviert ist. Sie müssen keine Nachrichten oder Journeys ändern oder erneut veröffentlichen, damit eine Regel wirksam wird.

Um eine Häufigkeitsregel für Nachrichten zu deaktivieren, klicken Sie auf das Auslassungszeichen neben der Regel und wählen Sie **[!UICONTROL Deaktivieren]**.

![](assets/message-rules-deactivate.png)

Der Status der Regel ändert sich in **[!UICONTROL Inaktiv]** und die Regel wird nicht mehr auf zukünftige Nachrichtenausführungen angewendet. Alle aktuell ausgeführten Nachrichten sind davon nicht betroffen.

>[!NOTE]
>
>Das Deaktivieren einer Regel wirkt sich weder auf die Zählung für einzelne Profile aus, noch wird die Zählung zurückgesetzt.

## Anwenden einer Häufigkeitsregel auf eine Nachricht {#apply-frequency-rule}

Gehen Sie wie folgt vor, um eine Häufigkeitsregel auf eine Nachricht anzuwenden.

1. Erstellen einer Nachricht. [Weitere Informationen](../messages/get-started-content.md#create-new-message)

1. Wählen Sie die Kategorie aus, die Sie für die [von Ihnen erstellte Regel](#create-new-rule) definiert haben.

   ![](assets/message-rules-msg-properties.png)

   >[!NOTE]
   >
   >Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** für Häufigkeitsregeln für Nachrichten verfügbar.

1. Wählen Sie die gewünschten Kanäle für Ihre Nachricht aus.

   ![](assets/message-rules-msg-channels.png)

1. Sie können auf den Link **[!UICONTROL Häufigkeitsregel]** klicken, um die Häufigkeitsregeln anzuzeigen, die für die ausgewählte Kategorie und die ausgewählten Kanäle gelten.

   ![](assets/message-rules-msg-link.png)

   Daraufhin öffnet sich eine neue Registerkarte, auf der die entsprechenden Häufigkeitsregeln für Nachrichten angezeigt werden.

1. [Gestalten](../design/design-emails.md) und [veröffentlichen](../messages/publish-manage-message.md) Sie Ihre Nachricht.

Alle Häufigkeitsregeln, die mit der ausgewählten Kategorie und den ausgewählten Kanälen übereinstimmen, werden automatisch auf diese Nachricht angewendet.

>[!NOTE]
>
>Nachrichten <!--that do not have any selected category or messages -->wobei die ausgewählte Kategorie **[!UICONTROL Transactional]** wird nicht mit den Frequenzregeln bewertet.

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

Die Anzahl der vom Versand ausgeschlossenen Profile können Sie in der [Live- und globalen Ansicht](../reports/message-monitoring.md) und im [E-Mail-Live-Bericht](../reports/email-live-report.md) ansehen, wo die Häufigkeitsregeln als möglicher Grund für den Ausschluss von Benutzern vom Versand angegeben sind.

>[!NOTE]
>
>Für denselben Kanal können mehrere Regeln angewendet werden, aber sobald die untere Begrenzung erreicht ist, wird das Profil von den nächsten Sendungen ausgeschlossen.

## Beispiel: Kombinieren mehrerer Regeln {#frequency-rule-example}

Sie können mehrere Häufigkeitsregeln für Nachrichten kombinieren, wie im folgenden Beispiel beschrieben.

1. [](#create-new-rule)Erstellen Sie eine Regel mit der Bezeichnung *Marketing-Gesamtbegrenzung*:

   * Wählen Sie alle Kanäle aus (E-Mail, Push).
   * Legen Sie die Begrenzung auf 12 fest.

   ![](assets/message-rules-ex-overall-cap.png)

1. Erstellen Sie eine zweite Regel namens *Begrenzung von Push-Marketing*, um die Anzahl der an einen Benutzer gesendeten Marketing-Push-Benachrichtigungen weiter einzuschränken:

   * Wählen Sie den Push-Kanal aus.
   * Legen Sie die Begrenzung auf 4 fest.

   ![](assets/message-rules-ex-push-cap.png)

1. Speichern und [aktivieren](#activate-rule) Sie die Regel.

1. Erstellen einer Nachricht. [Weitere Informationen](../messages/get-started-content.md#create-new-message)

1. Wählen Sie die Kategorie **[!UICONTROL Marketing]** aus.

   ![](assets/message-rules-ex-category-maktg.png)

1. Wählen Sie die Kanäle **[!UICONTROL E-Mail]** und **[!UICONTROL Push-Benachrichtigung]** aus.

   ![](assets/message-rules-ex-channels.png)

1. Sie können auf den Link **[!UICONTROL Häufigkeitsregel]** klicken, um die Häufigkeitsregeln anzuzeigen, die für die ausgewählte Kategorie und die ausgewählten Kanäle gelten.

1. [Gestalten](../design/design-emails.md) und [veröffentlichen](../messages/publish-manage-message.md) Sie Ihre Nachricht.

In diesem Szenario kann ein einzelnes Profil:
* monatlich bis zu 12 Marketing-Nachrichten erhalten;
* es wird jedoch von Marketing-Push-Benachrichtigungen ausgeschlossen, nachdem es 4 Push-Benachrichtigungen erhalten hat.

>[!NOTE]
>
>Beim Testen von Frequenzregeln kann es hilfreich sein, mit einem neu erstellten [Testprofil](../segment/creating-test-profiles.md), da es nach Erreichen der Frequenzgrenze eines Profils nicht mehr möglich ist, den Zähler auf den nächsten Monat zurückzusetzen. Durch die Deaktivierung einer Regel können Profile mit einer begrenzten Anzahl an Nachrichten empfangen, jedoch werden keine Zählerinkremente entfernt oder gelöscht.
