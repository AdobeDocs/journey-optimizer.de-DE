---
solution: Journey Optimizer
product: journey optimizer
title: Häufigkeitsregeln
description: Erfahren Sie, wie Sie Häufigkeitsregeln definieren
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: Nachricht, Häufigkeit, Regeln, Druck
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 718854c5ab51ad55fde7629415b954a079647c0b
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 80%

---

# Häufigkeitsregeln für Nachrichten {#frequency-rules}

Mit [!DNL Journey Optimizer] können Sie steuern, wie oft Benutzer eine Nachricht erhalten oder in eine Journey eintreten, indem Sie kanalübergreifende Regeln festlegen, mit denen zu oft angesprochene Profile automatisch von Nachrichten und Aktionen ausgeschlossen werden.

So könnte es beispielsweise für eine Marke eine Regel sein, ihren Kundinnen und Kunden pro Monat maximal drei Marketing-Nachrichten zu senden. Hierfür können Sie eine Häufigkeitsregel verwenden, die die Anzahl der gesendeten Nachrichten über einen oder mehrere Kanäle während eines monatlichen Kalenderzeitraums begrenzt.

>[!NOTE]
>
>Die Regeln zur Nachrichtenhäufigkeit unterscheiden sich von der Opt-out-Verwaltung, die es Benutzern ermöglicht, sich vom Erhalt von Nachrichten einer Marke abzumelden. [Weitere Informationen](../privacy/opt-out.md#opt-out-management)

➡️ [Entdecken Sie diese Funktion im Video](#video).

## Zugriff auf Regeln {#access-rules}

Sie können auf Regeln über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Regeln]** zugreifen. Alle Regeln werden sortiert nach Änderungsdatum aufgelistet.

Verwenden Sie das Filtersymbol, um die Regeln nach Kategorie, Status und/oder Kanal zu filtern. Sie können auch nach dem Nachrichtentitel suchen.

![](assets/message-rules-filter.png)

### Berechtigungen{#permissions-frequency-rules}

Zum Zugreifen auf, Erstellen, Bearbeiten oder Löschen von Häufigkeitsregeln für Nachrichten benötigen Sie die Berechtigung **[!UICONTROL Häufigkeitsregeln verwalten]**.

Benutzer*innen mit der Berechtigung **[!UICONTROL Anzeigen von Häufigkeitsregeln]** können Regeln anzeigen, sie jedoch nicht ändern oder löschen.

![](assets/message-rules-access.png)

Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/high-low-permissions.md).

## Erstellen einer Regel {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Wählen Sie die Kategorie der Nachrichtenregel aus"
>abstract="Bei Aktivierung und Anwendung auf eine Nachricht werden alle Häufigkeitsregeln, die der ausgewählten Kategorie entsprechen, automatisch auf diese Nachricht angewendet. Derzeit ist nur die Kategorie Marketing verfügbar."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Festlegen der Begrenzung für Ihre Regel"
>abstract="Geben Sie an, wie viele Nachrichten maximal jeden Monat an ein Kundenprofil gesendet werden sollen. Die Begrenzung der Häufigkeit basiert auf dem Zeitraum eines Kalendermonats und wird am Anfang jedes Monats zurückgesetzt."

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Definieren der Kanäle, für die die Regel gilt"
>abstract="Wählen Sie mindestens einen Kanal aus. Die Begrenzung gilt als Gesamtanzahl für alle Kanäle."

Gehen Sie wie folgt vor, um eine neue Regel zu erstellen.

1. Öffnen Sie die Liste **[!UICONTROL Häufigkeitsregeln für Nachrichten]** und klicken Sie auf **[!UICONTROL Regel erstellen]**.

   ![](assets/message-rules-create.png)

1. Definieren Sie den Namen der Regel.

   ![](assets/message-rules-details.png)

1. Wählen Sie die Kategorie der Nachrichtenregel aus.

   >[!NOTE]
   >
   >Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** verfügbar.

1. Wählen Sie einen Zeitraum für die Anwendung der Begrenzung aus.

   ![](assets/message-rules-capping-duration.png)

   Die Begrenzung der Häufigkeit basiert auf dem ausgewählten Kalenderzeitraum. Er wird am Anfang des entsprechenden Zeitrahmens zurückgesetzt.

   Der Zähler läuft für jeden Zeitraum wie folgt ab:

   * **[!UICONTROL Täglich]**: Die Frequenzlimitierung gilt für den Tag bis 23.:59:59 UTC und wird zu Beginn des nächsten Tages auf 0 zurückgesetzt.

   * **[!UICONTROL Wöchentlich]**: Die Frequenzlimitierung gilt bis Samstag, 23.:59:59 UTC dieser Woche, da die Kalenderwoche am Sonntag beginnt. Das Ablaufdatum ist unabhängig von der Regelerstellung. Wenn die Regel beispielsweise am Donnerstag erstellt wird, gilt diese Regel bis Samstag um 23 Uhr:59:59.

   * **[!UICONTROL Monatlich]**: Die Frequenzlimitierung gilt bis zum letzten Tag des Monats bei 23:59:59 UTC. Beispielsweise beträgt die monatliche Ablauffrist für den 31. Januar 23.:59:59 UTC.

   >[!NOTE]
   >
   >Wenn Sie [Stapelsegmentierung](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de#batch){target="_blank"}, the daily counters may not accurately reflect the current values as the daily counter snapshot is taken at midnight UTC the night before. Consequently, relying on daily counters in this scenario becomes impractical, as the snapshot does not reflect the most up-to-date counter values on the profile. To ensure accuracy for daily frequency capping rules, the use of [streaming segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=de){target="_blank"} wird empfohlen. <!--Learn more on audience evaluation methods in [this section](using/audience/about-audiences.md#evaluation-method-in-journey-optimizer).-->

1. Legen Sie die Begrenzung für Ihre Regel fest, d. h. die maximale Anzahl von Nachrichten, die an ein einzelnes Benutzerprofil jeden Monat, jede Woche oder jeden Tag gesendet werden können - entsprechend Ihrer obigen Auswahl.

   ![](assets/message-rules-capping.png)

1. Wählen Sie den Kanal aus, den Sie für diese Regel verwenden möchten: **[!UICONTROL E-Mail]** oder **[!UICONTROL Push-Benachrichtigung]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Sie müssen mindestens einen Kanal auswählen, um die Regel erstellen zu können.

1. Wählen Sie mehrere Kanäle aus, wenn Sie für alle ausgewählten Kanäle gemeinsam eine Begrenzung festlegen möchten.

   Legen Sie beispielsweise die Begrenzung auf 15 fest und wählen Sie dann den E-Mail- und Push-Kanal aus. Wenn ein Profil im ausgewählten Zeitraum bereits 10 Marketing-E-Mails und 5 Marketing-Push-Benachrichtigungen erhalten hat, wird dieses Profil vom nächsten Versand einer Marketing-E-Mail oder Push-Benachrichtigung ausgeschlossen.

1. Klicken Sie auf **[!UICONTROL Als Entwurf speichern]**, um die Regelerstellung zu bestätigen. Ihre Nachricht wird der Regelliste mit dem Status **[!UICONTROL Entwurf]** hinzugefügt.

   ![](assets/message-rules-created.png)

## Aktivieren einer Regel {#activate-rule}

Bei der Erstellung einer Häufigkeitsregel für Nachrichten hat die Regel den Status **[!UICONTROL Entwurf]** und wirkt sich noch auf keine Nachricht aus. Um die Regel zu aktivieren, klicken Sie auf die Auslassungszeichen neben der Regel und wählen Sie **[!UICONTROL Aktivieren]** aus.

![](assets/message-rules-activate.png)

Das Aktivieren einer Regel wirkt sich auf alle Nachrichten, für die sie gilt, bei ihrer nächsten Ausführung aus. Erfahren Sie, wie Sie [eine Häufigkeitsregel auf eine Nachricht anwenden](#apply-frequency-rule).

>[!NOTE]
>
>Es kann bis zu 10 Minuten dauern, bis eine Regel vollständig aktiviert ist. Sie müssen keine Nachrichten ändern oder Journeys erneut veröffentlichen, damit eine Regel wirksam wird.

Um eine Häufigkeitsregel für Nachrichten zu deaktivieren, klicken Sie auf das Auslassungszeichen neben der Regel und wählen Sie **[!UICONTROL Deaktivieren]**.

![](assets/message-rules-deactivate.png)

Der Status der Regel ändert sich in **[!UICONTROL Inaktiv]** und die Regel wird nicht mehr auf zukünftige Nachrichtenausführungen angewendet. Alle aktuell ausgeführten Nachrichten sind davon nicht betroffen.

>[!NOTE]
>
>Das Deaktivieren einer Regel wirkt sich weder auf die Zählung für einzelne Profile aus, noch wird die Zählung zurückgesetzt.

## Anwenden einer Häufigkeitsregel auf eine Nachricht {#apply-frequency-rule}

Gehen Sie wie folgt vor, um eine Häufigkeitsregel auf eine Nachricht anzuwenden.

1. Fügen Sie beim Erstellen einer [Journey](../building-journeys/journey-gs.md) eine Nachricht hinzu, indem Sie einen der Kanäle auswählen, die Sie für Ihre Regel definiert haben.

1. Wählen Sie die Kategorie aus, die Sie für die [von Ihnen erstellte Regel](#create-new-rule) definiert haben.

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** für Häufigkeitsregeln für Nachrichten verfügbar.

1. Sie können auf den Link für die **[!UICONTROL Frequenzregel]** klicken, um den Bildschirm mit den Häufigkeitsregeln in einer neuen Registerkarte anzuzeigen. [Weitere Informationen](#access-rules)

   Alle Häufigkeitsregeln, die mit der ausgewählten Kategorie und den ausgewählten Kanälen übereinstimmen, werden automatisch auf diese Nachricht angewendet.

   >[!NOTE]
   >
   >Nachrichten, bei denen die ausgewählte Kategorie **[!UICONTROL Transaktion]** ist, werden nicht mit den Häufigkeitsregeln ausgewertet.

1. Die Anzahl der vom Versand ausgeschlossenen Profile können Sie im [globalen Bericht](../reports/global-report.md) und im [Live-Bericht](../reports/live-report.md) ansehen, wo die Häufigkeitsregeln als möglicher Grund für den Ausschluss von Benutzenden vom Versand angegeben sind.

>[!NOTE]
>
>Für denselben Kanal können mehrere Regeln angewendet werden, aber sobald die untere Begrenzung erreicht ist, wird das Profil von den nächsten Sendungen ausgeschlossen.

## Beispiel: Kombinieren mehrerer Regeln {#frequency-rule-example}

Sie können mehrere Häufigkeitsregeln für Nachrichten kombinieren, wie im folgenden Beispiel beschrieben.

1. [](#create-new-rule)Erstellen Sie eine Regel mit der Bezeichnung *Marketing-Gesamtbegrenzung*:

   * Wählen Sie die Kanäle „E-Mail“ und „Push“ aus.
   * Legen Sie die Begrenzung auf 12 Monate fest.

   ![](assets/message-rules-ex-overall-cap.png)

1. Erstellen Sie eine zweite Regel namens *Begrenzung von Push-Marketing*, um die Anzahl der an einen Benutzer gesendeten Marketing-Push-Benachrichtigungen weiter einzuschränken:

   * Wählen Sie den Push-Kanal aus.
   * Legen Sie die Begrenzung auf 4 Monate fest.

   ![](assets/message-rules-ex-push-cap.png)

1. Speichern und [aktivieren](#activate-rule) Sie die Regel.

1. Erstellen Sie eine E-Mail und wählen Sie die Kategorie **[!UICONTROL Marketing]** für diese Nachricht aus. [Weitere Informationen](../email/create-email.md)

1. Erstellen Sie eine Push-Benachrichtigung und wählen Sie die Kategorie **[!UICONTROL Marketing]** für diese Nachricht aus. [Weitere Informationen](../push/create-push.md)

In diesem Szenario kann ein einzelnes Profil:
* monatlich bis zu 12 Marketing-Nachrichten erhalten;
* es wird jedoch von Marketing-Push-Benachrichtigungen ausgeschlossen, nachdem es 4 Push-Benachrichtigungen erhalten hat.

>[!NOTE]
>
>Beim Testen von Häufigkeitsregeln kann es hilfreich sein, mit einem neu erstellten [Testprofil](../audience/creating-test-profiles.md) zu beginnen, da es nach Erreichen des Häufigkeitslimits eines Profils bis zum nächsten Monat nicht mehr möglich ist, den Zähler zurückzusetzen. Wenn Sie eine Regel deaktivieren, können Profile, für die die Begrenzung gilt, zwar Nachrichten empfangen, es werden aber keine Zählerschritte entfernt oder gelöscht.

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie Häufigkeitsregeln erstellen, aktivieren, testen und Berichte dazu erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
