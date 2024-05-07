---
solution: Journey Optimizer
product: journey optimizer
title: Verfahrensregeln
description: Informationen zum Erstellen und Anwenden von Verfahrensregeln
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: Nachricht, Häufigkeit, Regeln, Druck
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 07f5f0b4-417e-408e-8d9e-86615c8a3fbf
source-git-commit: f8d257b04d8682bb16fcccd3fd0ef9d5389a058d
workflow-type: ht
source-wordcount: '1426'
ht-degree: 100%

---

# Verfahrensregeln {#business-rules}

>[!AVAILABILITY]
>
>Verfahrensregeln sind derzeit als Beta-Version nur für ausgewählte Benutzende verfügbar.

[!DNL Journey Optimizer] ermöglicht es Ihnen, zu kontrollieren, wie oft die Benutzenden eine Nachricht erhalten, indem Sie kanalübergreifende Regeln festlegen, die übermäßig umworbene Profile automatisch von Nachrichten und Aktionen ausschließen.

Eine Regel für eine Marke könnte zum Beispiel lauten: nicht mehr als 4 Marketing-Nachrichten pro Monat an ihre Kundinnen und Kunden zu senden. Hierfür können Sie eine Häufigkeitsregel verwenden, die die Anzahl der gesendeten Nachrichten über einen oder mehrere Kanäle während des Zeitraums eines Kalendermonats begrenzt.

Durch die Erstellung verschiedener Regelsätze für eine bessere Granularität ermöglicht [!DNL Journey Optimizer] Ihnen die Anwendung von Frequenzbegrenzungen auf verschiedene Arten von Marketing-Kommunikation. Sie können beispielsweise eine Regel festlegen, um die Anzahl der **Werbemitteilungen** zu begrenzen, die an Ihre Kundinnen und Kunden gesendet werden, und eine weitere Regel festlegen, um die Anzahl der **Newsletter** zu begrenzen, die an sie gesendet werden.

>[!NOTE]
>
>Verfahrensregeln unterscheiden sich von der Opt-out-Verwaltung, die es den Benutzenden ermöglicht, sich vom Erhalt von Mitteilungen einer Marke abzumelden. [Weitere Informationen](../privacy/opt-out.md#opt-out-management)

## Zugriffsregelsätze {#access-rule-sets}

Regelsätze sind über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Verfahrensregeln (Beta)]** verfügbar. Alle Regeln werden sortiert nach dem Erstellungsdatum aufgelistet.

![](assets/rule-sets-list.png)

Klicken Sie auf den Namen eines Regelsatzes, um dessen Inhalt anzuzeigen und zu bearbeiten. Alle Regeln, die in diesem Regelsatz enthalten sind, werden aufgelistet.

Über das Kontextmenü oben rechts können Sie Folgendes tun:

* Bearbeiten des Namens und der Beschreibung des Regelsatzes
* Aktivieren des Regelsatzes – [mehr erfahren](#activate-rule)
* Löschen des Regelsatzes

![](assets/rule-set-example.png)

Für jede Regel im Regelsatz können Sie über die Schaltfläche **[!UICONTROL Weitere Aktionen]** folgende Aktionen durchführen:

* Bearbeiten der Regel
* Aktivieren der Regel – [mehr erfahren](#activate-rule)
* Löschen der Regel

![](assets/rule-set-example-rules.png)

<!--### Permissions{#permissions-frequency-rules}

To access, create, edit or delete message frequency rules, you must have the **[!UICONTROL Manage frequency rules]** permission. 

Users with the **[!UICONTROL View frequency rules]** permission are able to view rules, but not to modify or delete them.

![](assets/message-rules-access.png)

Learn more about permissions in [this section](../administration/high-low-permissions.md).-->

## Erstellen eines Regelsatzes {#create-rule-set}

Gehen Sie wie folgt vor, um einen Regelsatz zu erstellen:

1. Rufen Sie die Liste **[!UICONTROL Regelsätze]** auf und klicken Sie dann auf **[!UICONTROL Regelsatz erstellen]**.

   ![](assets/rule-sets-create-button.png)

1. Legen Sie den Namen des Regelsatzes fest, fügen Sie bei Bedarf eine Beschreibung hinzu und klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >Der Regelsatzname muss eindeutig sein.

1. Jetzt können Sie [die Regeln](#create-new-rule) festlegen, die Sie zu diesem Regelsatz hinzufügen möchten, und [ihn aktivieren](#activate-rule).

   >[!NOTE]
   >
   >Vergewissern Sie sich, dass alle Regeln, die Sie auf Ihre Nachrichten anwenden wollen, auch im Regelsatz aktiviert sind.

## Erstellen einer Regel {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="Wählen Sie die Kategorie der Nachrichtenregel aus"
>abstract="Bei Aktivierung und Anwendung auf eine Nachricht werden alle Häufigkeitsregeln, die der ausgewählten Kategorie entsprechen, automatisch auf diese Nachricht angewendet. Derzeit ist nur die Kategorie Marketing verfügbar."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="Festlegen der Begrenzung für Ihre Regel"
>abstract="Geben Sie an, wie viele Nachrichten innerhalb des ausgewählten Zeitrahmens maximal an ein Kundenprofil gesendet werden sollen. Die Frequenzbegrenzung basiert auf dem ausgewählten Kalenderzeitraum und wird am Anfang des entsprechenden Zeitrahmens zurückgesetzt. "

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Definieren der Kanäle, für die die Regel gilt"
>abstract="Wählen Sie mindestens einen Kanal aus. Die Begrenzung gilt als Gesamtanzahl für alle Kanäle."

Gehen Sie wie folgt vor, um eine Regel zu einem Regelsatz hinzuzufügen:

1. Klicken Sie in dem soeben erstellten Regelsatz auf **[!UICONTROL Regel hinzufügen]**.

   ![](assets/rule-sets-create-rule-button.png)

1. Definieren Sie den Namen der Regel.

   >[!NOTE]
   >
   >Der Regelsatzname muss eindeutig sein.

1. Wählen Sie die Kategorie der Nachrichtenregel aus.

   >[!NOTE]
   >
   >Derzeit ist nur die Kategorie **[!UICONTROL Marketing]** verfügbar.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Dauer]** einen Zeitrahmen aus, auf den die Begrenzung angewendet werden soll. [Weitere Informationen](#frequency-cap)

1. Legen Sie die Begrenzung für Ihre Regel fest, d. h. die maximale Anzahl der Nachrichten, die pro Monat, Woche oder Tag – entsprechend Ihrer Auswahl oben – an ein individuelles Benutzerprofil gesendet werden können.

1. Wählen Sie den Kanal, den Sie für diese Regel verwenden möchten: **[!UICONTROL E-Mail]**, **[!UICONTROL SMS]**, **[!UICONTROL Push-Benachrichtigung]** oder **[!UICONTROL Briefpost]**.

   ![](assets/rule-set-channels.png)

   >[!NOTE]
   >
   >Sie müssen mindestens einen Kanal auswählen, um die Regel erstellen zu können.

1. Wählen Sie mehrere Kanäle aus, wenn Sie für alle ausgewählten Kanäle gemeinsam eine Begrenzung festlegen möchten.

   Legen Sie beispielsweise die Begrenzung auf 5 fest und wählen Sie dann den E-Mail- und SMS-Kanal aus. Wenn ein Profil im ausgewählten Zeitraum bereits 3 Marketing-E-Mails und 2 SMS erhalten hat, wird dieses Profil vom nächsten Versand einer Marketing-E-Mail oder SMS ausgeschlossen.

1. Klicken Sie auf **[!UICONTROL Speichern]**, um die Erstellung der Regel zu bestätigen. Ihre Nachricht wird dem Regelsatz mit dem Status **[!UICONTROL Entwurf]** hinzugefügt.

   ![](assets/rule-set-rule-created.png)

1. Wiederholen Sie die obigen Schritte, um dem Regelsatz so viele Regeln wie nötig hinzuzufügen.

Nun müssen Sie jede Regel aktivieren, bevor sie auf eine Nachricht angewendet werden kann. [Weitere Informationen](#activate-rule)

>[!NOTE]
>
>Vergewissern Sie sich, dass der Regelsatz auch aktiviert ist, um ihn in Ihren Nachrichten auswählen zu können.

### Frequenzbegrenzung {#frequency-cap}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="Wählen Sie die Kategorie der Nachrichtenregel aus"
>abstract="Bei Aktivierung und Anwendung auf eine Nachricht werden alle Häufigkeitsregeln, die der ausgewählten Kategorie entsprechen, automatisch auf diese Nachricht angewendet. Derzeit ist nur die Kategorie Marketing verfügbar."

Legen Sie über die Dropdown-Liste **[!UICONTROL Dauer]** fest, ob die Begrenzung monatlich, wöchentlich oder täglich angewendet werden soll.

Die Häufigkeitsbegrenzung basiert auf dem ausgewählten Kalenderzeitraum. Sie wird am Anfang des entsprechenden Zeitrahmens zurückgesetzt.

![](assets/rule-set-capping-duration.png)

Der Zähler läuft für jeden Zeitraum wie folgt ab:

* **[!UICONTROL Monatlich]**: Die Häufigkeitsbegrenzung ist bis zum letzten Tag des Monats um 23:59:59 UTC gültig. Beispielsweise beträgt die monatliche Gültigkeit für den 31.01. 23:59:59 UTC.

* **[!UICONTROL Wöchentlich]**: Die Häufigkeitsbegrenzung gilt bis Samstag 23:59:59 UTC der betreffenden Woche, da die Kalenderwoche am Sonntag beginnt. Das Ablaufdatum ist unabhängig von der Regelerstellung. Wenn die Regel beispielsweise am Donnerstag erstellt wird, gilt diese Regel bis Samstag um 23 Uhr:59:59.

* **[!UICONTROL Täglich]**: Die tägliche Frequenzbegrenzung ist für den Tag bis 23:59:59 UTC gültig und wird zu Beginn des nächsten Tages auf 0 zurückgesetzt.

### Tägliche Frequenzbegrenzung {#daily-frequency-cap}

>[!CAUTION]
>
>Um die Genauigkeit der Regeln für die tägliche Frequenzbegrenzung zu gewährleisten, ist die Verwendung der [Streaming-Segmentierung](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=de){target="_blank"} obligatorisch. Weitere Informationen über Methoden zur Zielgruppenauswertung finden Sie in [diesem Abschnitt](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

Stellen Sie bei jeder Segmentgröße bis zur Grenze von 60 Millionen Nachrichten pro Stunde<!--not clear--> sicher, dass Ihre Kampagnen mindestens 2 Stunden auseinander liegen.


<!-- Journey example:

* If customer sets a Daily rule under the Global Ruleset for email <= 2/day:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for noon)
   * Journey 789 (scheduled for 1 pm)

   In this example, the Daily Frequency cap will not guarantee <= 2/day. The rule will only be guaranteed when Journeys are at least 2 hours apart:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for 2 pm)
   * Journey 789 (scheduled for 4 pm)-->

Nehmen wir an, dass Sie z. B. unter einem Regelsatz für den E-Mail-Kanal eine tägliche Regel festlegen, die kleiner oder gleich 2 Tage ist, und die folgenden Kampagnen erstellen:
* Kampagne A (geplant für Mittag)
* Kampagne A (geplant für 15 Uhr)
* Kampagne B (geplant für 13 Uhr)

Diese Vorgehensweise funktioniert aus zwei Gründen nicht:
* Die tägliche Frequenzbegrenzung ist nicht garantiert, da die Kampagnen nicht im Abstand von 2 Stunden stattfinden.
* Es ist nicht empfehlenswert, dieselbe Kampagne mehrmals an einem Tag zu planen, um die tägliche Begrenzung auszunutzen.

Das nachstehende Beispiel sollte die Frequenzbegrenzung einhalten:
* Kampagne A (geplant für Mittag)
* Kampagne B (geplant für 14 Uhr)

<!--* To use the Daily Cap with a Journey, customers can use either an Event Triggered Journey or an Audience Qualified Journey. If customers wish to use the Daily Cap with a Read Audience Journey, they should use a Campaign instead and associate a Local Ruleset with the campaign, following the example given above.-->

## Aktivieren von Regeln und Regelsätzen {#activate-rule}

Wenn eine Regel erstellt wird, verfügt sie über den Status **[!UICONTROL Entwurf]** und wirkt sich noch auf keine Nachricht aus. Um sie zu aktivieren, klicken Sie auf die Schaltfläche **[!UICONTROL Weitere Aktionen]** neben der Regel und wählen Sie **[!UICONTROL Aktivieren]**.

![](assets/rule-set-activate-rule.png)

Außerdem müssen Sie den Regelsatz aktivieren, damit Sie in Kampagnen/Journeys darauf zugreifen und ihn auf Ihre Nachrichten anwenden können.

![](assets/rule-set-activate-set.png)

Die Aktivierung eines Regelsatzes wirkt sich bei der nächsten Ausführung auf alle Nachrichten aus, für die dieser Regelsatz gilt. Erfahren Sie, wie Sie [einen Regelsatz auf eine Nachricht anwenden](#apply-rule-set).

>[!NOTE]
>
>Es kann bis zu 10 Minuten dauern, bis eine Regel oder ein Regelsatz vollständig aktiviert ist. Sie müssen keine Nachrichten ändern oder Journeys erneut veröffentlichen, damit eine Regel wirksam wird.

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

## Deaktivieren von Regeln und Regelsätzen {#deactivate-rule}

Um eine Regel oder einen Regelsatz zu deaktivieren, klicken Sie auf die Schaltfläche **[!UICONTROL Weitere Aktionen]** neben dem gewünschten Element und wählen Sie **[!UICONTROL Deaktivieren]**.

![](assets/rule-set-inactive-rule.png)

Der Status ändert sich in **[!UICONTROL Inaktiv]** und die Regel wird nicht mehr auf zukünftige Nachrichtenausführungen angewendet. Alle aktuell ausgeführten Nachrichten sind davon nicht betroffen.

>[!NOTE]
>
>Das Deaktivieren eines Regelsatzes wirkt sich weder auf die Zählung für einzelne Profile aus, noch wird die Zählung zurückgesetzt.

## Anwenden einer Häufigkeitsregel auf eine Nachricht {#apply-frequency-rule}

Gehen Sie wie folgt vor, um eine Häufigkeitsregel auf eine Nachricht anzuwenden.

1. Wenn Sie eine [Kampagne](../campaigns/create-campaign.md) erstellen, wählen Sie einen der Kanäle, die Sie für Ihren Regelsatz festgelegt haben, und bearbeiten Sie den Inhalt Ihrer Nachricht.

1. Klicken Sie im Bildschirm für die Bearbeitung von Inhalten auf die Schaltfläche **[!UICONTROL Verfahrensregel hinzufügen]**.

1. Wählen Sie den [Regelsatz, den Sie festgelegt haben](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >In der Liste werden nur [aktivierte](#activate-rule) Regelsätze angezeigt.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. Die Anzahl der vom Versand ausgeschlossenen Profile können Sie im [globalen Bericht](../reports/global-report.md) und im [Live-Bericht](../reports/live-report.md) ansehen, wo die Häufigkeitsregeln als möglicher Grund für den Ausschluss von Benutzenden vom Versand angegeben sind.

>[!NOTE]
>
>Für denselben Kanal können mehrere Regeln angewendet werden, aber sobald die untere Begrenzung erreicht ist, wird das Profil von den nächsten Sendungen ausgeschlossen.

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

Beim Testen von Häufigkeitsregeln kann es hilfreich sein, mit einem neu erstellten [Testprofil](../audience/creating-test-profiles.md) zu beginnen, da es nach Erreichen der Frequenzbegrenzung eines Profils bis zur nächsten Periode nicht mehr möglich ist, den Zähler zurückzusetzen. Wenn Sie eine Regel deaktivieren, können Profile, für die die Begrenzung gilt, zwar Nachrichten empfangen, es werden aber keine Zählerschritte entfernt oder gelöscht.
