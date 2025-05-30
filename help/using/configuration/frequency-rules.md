---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von Geschäftsregeln
description: Erfahren Sie, wie Sie Häufigkeitsregeln für Geschäfte definieren
feature: Rules
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
robots: noindex
googlebot: noindex
keywords: Nachricht, Häufigkeit, Regeln, Druck
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: ht
source-wordcount: '1267'
ht-degree: 100%

---

# Konfigurieren von Geschäftsregeln {#frequency-rules}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_message_frequency_rules"
>title="Geschäftsregeln"
>abstract="Regeln zur Nachrichtenhäufigkeit sind eine Art Geschäftsregel, die die Anzahl der Nachrichtenempfänge durch Benutzende bzw. ihre Eintritte in Journeys über einen oder mehrere Kanäle hinweg begrenzt. Diese kanalübergreifenden Regeln schließen Profile, die zu oft angesprochen wurden, automatisch von Nachrichten und Aktionen aus."

Mit [!DNL Journey Optimizer] können Sie steuern, wie oft Benutzende über einen oder mehrere Kanäle eine Nachricht erhalten oder in eine Journey eintreten. Regeln zur Nachrichtenhäufigkeit, mit denen Profile, die zu oft angesprochen wurden, automatisch von Nachrichten und Aktionen ausgeschlossen werden.

Für eine Marke könnte eine Regel beispielsweise lauten, Kundinnen und Kunden pro Monat maximal vier Marketing-Nachrichten zu senden. Hierfür können Sie eine Geschäftsregel verwenden, die die Anzahl der gesendeten Nachrichten über einen oder mehrere Kanäle während eines monatlichen Kalenderzeitraums begrenzt.

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>Geschäftsregeln unterscheiden sich von der Opt-out-Verwaltung, die es den Benutzenden ermöglicht, sich vom Erhalt von Mitteilungen einer Marke abzumelden. [Weitere Informationen](../privacy/opt-out.md#opt-out-management)

➡️ [Entdecken Sie diese Funktion im Video](#video).

## Zugriff auf Geschäftsregeln {#access-rules}

Geschäftsregeln sind über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Geschäftsregeln]** verfügbar. Alle Regeln werden sortiert nach Änderungsdatum aufgelistet. Verwenden Sie das Filtersymbol, um die Regeln nach Kategorie, Status und/oder Kanal zu filtern. Sie können auch nach dem Nachrichtentitel suchen.

![](assets/message-rules-filter.png)

### Berechtigungen{#permissions-frequency-rules}

Um auf Geschäftsregeln für Nachrichten zuzugreifen oder welche anzulegen, zu bearbeiten oder zu löschen, benötigen Sie die Berechtigung **[!UICONTROL Häufigkeitsregeln verwalten]**.

Benutzer*innen mit der Berechtigung **[!UICONTROL Anzeigen von Häufigkeitsregeln]** können Regeln anzeigen, sie jedoch nicht ändern oder löschen.

![](assets/message-rules-access.png)

Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/high-low-permissions.md).

## Erstellen einer Geschäftsregel {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Wählen Sie die Kategorie der Nachrichtenregel aus"
>abstract="Bei Aktivierung und Anwendung auf eine Nachricht werden alle Geschäftsregeln, die der ausgewählten Kategorie entsprechen, automatisch auf diese Nachricht angewendet. Derzeit ist nur die Kategorie „Marketing“ verfügbar."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Festlegen der Begrenzung für Ihre Geschäftsregeln"
>abstract="Geben Sie an, wie viele Nachrichten innerhalb des ausgewählten Zeitrahmens maximal an ein Kundenprofil gesendet werden sollen. Die Frequenzbegrenzung basiert auf dem ausgewählten Kalenderzeitraum und wird am Anfang des entsprechenden Zeitrahmens zurückgesetzt. "

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Definieren der Kanäle, für die die Geschäftsregeln gelten"
>abstract="Wählen Sie mindestens einen Kanal aus. Die Begrenzung gilt als Gesamtanzahl für alle Kanäle."

Gehen Sie wie folgt vor, um eine neue Geschäftsregel zu erstellen.

1. Rufen Sie die Liste **[!UICONTROL Geschäftsregeln]** auf und klicken Sie dann auf **[!UICONTROL Regel erstellen]**.

   ![](assets/message-rules-create.png)

1. Definieren Sie den Regelnamen und wählen Sie die Kategorie der Nachrichtenregel aus.

   >[!NOTE]
   >
   >Es ist nur die Kategorie **[!UICONTROL Marketing]** verfügbar.

   ![](assets/message-rules-details.png)

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Dauer]** einen Zeitrahmen aus, auf den die Begrenzung angewendet werden soll. [Weitere Informationen](#frequency-cap)

1. Legen Sie die Begrenzung für Ihre Regel fest, d. h. die maximale Anzahl der Nachrichten, die pro Monat oder Woche <!--or day--> an ein einzelnes Benutzerprofil gesendet werden können – je nach Ihrer Auswahl oben.

   <!--![](assets/message-rules-capping.png)-->

1. Wählen Sie den Kanal aus, den Sie für diese Regel verwenden möchten: **[!UICONTROL E-Mail]**, **[!UICONTROL Push-Benachrichtigung]**, **[!UICONTROL SMS]** oder **[!UICONTROL Briefpost]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Sie müssen mindestens einen Kanal auswählen, um die Regel erstellen zu können.

1. Wählen Sie mehrere Kanäle aus, wenn Sie für alle ausgewählten Kanäle gemeinsam eine Begrenzung festlegen möchten.

   Legen Sie beispielsweise die Begrenzung auf 15 fest und wählen Sie dann den E-Mail- und Push-Kanal aus. Wenn ein Profil im ausgewählten Zeitraum bereits 10 Marketing-E-Mails und 5 Marketing-Push-Benachrichtigungen erhalten hat, wird dieses Profil vom nächsten Versand einer Marketing-E-Mail oder Push-Benachrichtigung ausgeschlossen.

1. Klicken Sie auf **[!UICONTROL Als Entwurf speichern]**, um die Regelerstellung zu bestätigen. Ihre Nachricht wird der Regelliste mit dem Status **[!UICONTROL Entwurf]** hinzugefügt.

   ![](assets/message-rules-created.png)

### Frequenzbegrenzung {#frequency-cap}

Legen Sie über die Dropdown-Liste **[!UICONTROL Dauer]** fest, ob die Begrenzung monatlich oder wöchentlich angewendet werden soll.

>[!NOTE]
>
>Auf Anfrage ist auch eine tägliche Frequenzbegrenzung möglich. [Weitere Informationen](#daily-frequency-cap)

Die Häufigkeitsbegrenzung basiert auf dem ausgewählten Kalenderzeitraum. Sie wird am Anfang des entsprechenden Zeitrahmens zurückgesetzt.

![](assets/message-rules-capping-duration.png)

Der Zähler läuft für jeden Zeitraum wie folgt ab:

* **[!UICONTROL Monatlich]**: Die Häufigkeitsbegrenzung ist bis zum letzten Tag des Monats um 23:59:59 UTC gültig. Beispielsweise beträgt die monatliche Gültigkeit für den 31.01.23:59:59 UTC.

* **[!UICONTROL Wöchentlich]**: Die Frequenzbegrenzung gilt bis Samstag 23:59:59 UTC der betreffenden Woche, da die Kalenderwoche am Sonntag beginnt. Das Ablaufdatum ist unabhängig von der Regelerstellung. Wenn die Regel beispielsweise am Donnerstag erstellt wird, gilt diese Regel bis Samstag um 23 Uhr:59:59.

### Tägliche Frequenzbegrenzung {#daily-frequency-cap}

Neben der monatlichen und wöchentlichen Frequenzbegrenzung ist auf Anfrage auch eine tägliche Frequenzbegrenzung verfügbar. Weiterführende Informationen dazu erhalten Sie beim Adobe-Support.

Die tägliche Frequenzbegrenzung ist für den Tag bis 23:59:59 Uhr (UTC) gültig und wird zu Beginn des nächsten Tages auf 0 zurückgesetzt.

>[!NOTE]
>
>Um die Genauigkeit der Regeln für die tägliche Frequenzbegrenzung sicherzustellen, wird eine [Streaming-Segmentierung](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/streaming-segmentation){target="_blank"} empfohlen. Weitere Informationen zu Methoden zur Zielgruppenauswertung finden Sie in [diesem Abschnitt](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

## Aktivieren einer Geschäftsregel {#activate-rule}

Wenn eine Geschäftsregel erstellt wird, verfügt sie über den Status **[!UICONTROL Entwurf]** und hat noch keine Auswirkungen auf eine Nachricht. Um die Regel zu aktivieren, klicken Sie auf die Auslassungszeichen neben der Regel und wählen Sie **[!UICONTROL Aktivieren]** aus.

![](assets/message-rules-activate.png)

Das Aktivieren einer Regel wirkt sich auf alle Nachrichten, für die sie gilt, bei ihrer nächsten Ausführung aus. Erfahren Sie, wie Sie [eine Geschäftsregel auf eine Nachricht anwenden](#apply-frequency-rule).

>[!NOTE]
>
>Es kann bis zu 10 Minuten dauern, bis eine Regel vollständig aktiviert ist. Sie müssen keine Nachrichten ändern oder Journeys erneut veröffentlichen, damit eine Regel wirksam wird.

Um eine Geschäftsregel zu deaktivieren, klicken Sie auf die Auslassungspunkte neben der Regel und wählen Sie **[!UICONTROL Deaktivieren]**.

![](assets/message-rules-deactivate.png)

Der Status der Regel ändert sich in **[!UICONTROL Inaktiv]** und die Regel wird nicht mehr auf zukünftige Nachrichtenausführungen angewendet. Alle aktuell ausgeführten Nachrichten sind davon nicht betroffen.

>[!NOTE]
>
>Das Deaktivieren einer Regel wirkt sich weder auf die Zählung für einzelne Profile aus, noch wird die Zählung zurückgesetzt.

## Anwenden einer Geschäftsregel auf eine Nachricht {#apply-frequency-rule}

Gehen Sie wie folgt vor, um eine Geschäftsregel auf eine Nachricht anzuwenden.

1. Fügen Sie beim Erstellen einer [Journey](../building-journeys/journey-gs.md) eine Nachricht hinzu, indem Sie einen der Kanäle auswählen, die Sie für Ihre Regel definiert haben.

1. Wählen Sie die Kategorie aus, die Sie für die [von Ihnen erstellte Regel](#create-new-rule) definiert haben.

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** für Geschäftsregeln verfügbar.

1. Sie können auf den Link für die **[!UICONTROL Frequenzregel]** klicken, um den Bildschirm mit den Häufigkeitsregeln in einer neuen Registerkarte anzuzeigen. [Weitere Informationen](#access-rules)

   Alle Verfahrensregeln, die mit der ausgewählten Kategorie und den ausgewählten Kanälen übereinstimmen, werden automatisch auf diese Nachricht angewendet.

   >[!NOTE]
   >
   >Nachrichten, bei denen die ausgewählte Kategorie **[!UICONTROL Transaktion]** ist, werden nicht mit den Häufigkeitsregeln ausgewertet.

1. Die Anzahl der vom Versand ausgeschlossenen Profile können Sie im [Customer Journey Analytics-Bericht](../reports/report-gs-cja.md) und im [Live-Bericht](../reports/live-report.md) ansehen, wo die Geschäftsregeln als möglicher Grund für den Ausschluss von Benutzenden vom Versand angegeben sind.

>[!NOTE]
>
>Für denselben Kanal können mehrere Regeln angewendet werden, aber sobald die untere Begrenzung erreicht ist, wird das Profil von den nächsten Sendungen ausgeschlossen.

## Beispiel: Kombinieren mehrerer Regeln {#frequency-rule-example}

Sie können mehrere Geschäftsregeln für Nachrichten kombinieren, wie im folgenden Beispiel beschrieben.

1. [Erstellen Sie eine Geschäftsregel](#create-new-rule) mit der Bezeichnung *Marketing-Gesamtbegrenzung*:

   * Wählen Sie alle Kanäle aus.
   * Legen Sie die Begrenzung auf 12 x monatlich fest.

   ![](assets/message-rules-ex-overall-cap.png)

1. Erstellen Sie eine zweite Regel namens *Begrenzung von Push-Marketing*, um die Anzahl der an einen Benutzer gesendeten Marketing-Push-Benachrichtigungen weiter einzuschränken:

   * Wählen Sie den Push-Kanal aus.
   * Legen Sie die Begrenzung auf 4 x monatlich fest.

   ![](assets/message-rules-ex-push-cap.png)

1. Speichern und [aktivieren](#activate-rule) Sie die Regel.

1. [Erstellen Sie eine Nachricht](../building-journeys/journeys-message.md) für jeden Kanal, über den Sie kommunizieren möchten, und wählen Sie für jede Nachricht die Kategorie **[!UICONTROL Marketing]** aus. [Erfahren Sie, wie Sie eine Geschäftsregel anwenden](#apply-frequency-rule)

   ![](assets/journey-message-category.png)


<!--
Learn how to create a message for the different channels in the following sections:
* [Create an email](../email/create-email.md)
* [Create a push notification](../push/create-push.md)
* [Create an SMS](../sms/create-sms.md)
* [Create a direct mail](../direct-mail/create-direct-mail.md)

Create an email and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../email/create-email.md)

Create a push notification and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../push/create-push.md)

Create an SMS and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../sms/create-sms.md)

Create a direct mail and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../direct-mail/create-direct-mail.md)
-->

In diesem Szenario kann ein einzelnes Profil:
* monatlich bis zu 12 Marketing-Nachrichten erhalten;
* es wird jedoch von Marketing-Push-Benachrichtigungen ausgeschlossen, nachdem es 4 Push-Benachrichtigungen erhalten hat.

>[!NOTE]
>
>Beim Testen von Geschäftsregeln kann es hilfreich sein, mit einem neu erstellten [Testprofil](../audience/creating-test-profiles.md) zu beginnen, da es nach Erreichen der Frequenzbegrenzung eines Profils bis zum nächsten Monat nicht mehr möglich ist, den Zähler zurückzusetzen. Wenn Sie eine Regel deaktivieren, können Profile, für die die Begrenzung gilt, zwar Nachrichten empfangen, es werden aber keine Zählerschritte entfernt oder gelöscht.

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie Geschäftsregeln erstellen, aktivieren, testen und Berichte dazu erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
