---
solution: Journey Optimizer
product: journey optimizer
title: Versenden in Schüben
description: Planen Sie den Versand ausgehender Kampagnennachrichten in kontrollierten Batches im Zeitverlauf. Wave-Versand unterstützt die Zustellbarkeit und hilft, die Reputation des Absenders zu wahren.
feature: Campaigns
topic: Campaign scheduling
role: User
level: Intermediate
keywords: Schübe, Batches, Zeitplan, Kampagne, Journey, Zustellbarkeit
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---

# In Kampagnen mithilfe von Schüben versenden {#send-using-waves}

Sie können den Versand von ausgehenden Kampagnennachrichten in mehrere Batches (Schübe) unterteilen und im Zeitverlauf planen. Der Wave-Versand trägt dazu bei, die Auslastung auszugleichen, überlastete nachgelagerte Systeme (wie Callcenter oder Landingpages) zu vermeiden und die Zustellbarkeit und die Reputation des Absenders zu unterstützen - insbesondere bei Sendungen mit hohem Volumen.

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Mit Journey Optimizer können Sie die Anzahl der Schübe, ihre Größe (als Prozentsatz der Zielgruppe oder als absolute Zahlen) und den Zeitpunkt definieren, zu dem jede Schübe ausgeführt wird.

## Einschränkungen und Leitplanken {#limitations-guardrails}

* Der Wave-Versand gilt nur für **ausgehende** Aktionen (E-Mail, SMS, Push, Briefpost).
* Sie müssen mindestens **2 Schübe definieren** und können bis zu **10 Schübe hinzufügen**.
* Der Mindestabstand zwischen dem Beginn zweier Schübe beträgt **30 Minuten**.
* Ein Wave-Start kann weder vor dem Kampagnenstart noch in der Vergangenheit liegen.

## Wellenversand konfigurieren {#configure-wave-sending}

Gehen Sie wie folgt vor, um zu konfigurieren, wie und wann Wellen in einer Kampagne gesendet werden.

1. Erstellen oder öffnen Sie eine [Aktionskampagne](create-campaign.md) die eine ausgehende Aktion enthält (z. B. E-Mail, SMS, Push).

1. Wählen Sie auf **[!UICONTROL Registerkarte]** Planung“ Ihrer Kampagne die Option **[!UICONTROL Kampagnenaktionen in Schüben versenden]**.

   ![](assets/campaign-wave-option.png){width="100%"}

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Kampagnenaktionen in Schüben versenden]** wird nur angezeigt, wenn auf der Registerkarte **[!UICONTROL Aktionen]** der Kampagne eine ausgehende Aktion ausgewählt wurde. [Weitere Informationen](campaign-action.md)

1. Legen Sie die Anzahl der Schübe fest, die Sie senden möchten (z. B. 4).

   >[!NOTE]
   >
   >Sie müssen mindestens 2 Schübe definieren und können bis zu 10 Schübe hinzufügen.

1. Wählen Sie wie unten beschrieben, wie Wellengröße und Timing definiert werden.

### Gleichmäßige Wellen {#equal-waves}

Standardmäßig wird die Zielgruppe in gleich große Schübe unterteilt. Planen Sie die Zeit für die erste Welle und legen Sie ein festes Intervall zwischen dem Beginn jeder Welle fest (z. B. 2 Stunden).

![](assets/campaign-equal-waves.png){width="80%"}

>[!NOTE]
>
>Der Mindestabstand zwischen dem Beginn zweier Schübe beträgt **30 Minuten**.

Das System plant dann die nachfolgenden Wellen automatisch (z. B. erste Welle um 9 :00 Uhr, zweite um 11 :00 Uhr, dritte um :00 Uhr, vierte um 15 :00 Uhr).

### Benutzerdefinierte Verteilung {#custom-distribution}

Wählen Sie die Option **[!UICONTROL Benutzerdefinierte Verteilung]** aus, um die Größe jeder Welle als Prozentsatz der gesamten Zielgruppe zu definieren (z. B. 15 %, 20 %, 25 %, 40 %).

![](assets/campaign-wave-percentage.png){width="80%"}

>[!NOTE]
>
>Die Summe über alle Wellen hinweg muss 100% betragen. Ist dies nicht der Fall, wird eine Warnmeldung angezeigt.<!--are the waves actually sent or does the system prevent user from saving the campaign?-->

Wählen Sie **[!UICONTROL Zahlen]** aus, um die Größe jeder Welle als absolute Anzahl von Profilen zu definieren (z. B. 10.000; 50.000).

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>
>Bei der Verwendung von Zahlen überprüft das System nicht, ob die Summe die gesamte Zielgruppe abdeckt. Sie müssen sicherstellen, dass Ihre Wellengrößen die Zielgruppe abdecken, die Sie senden möchten. Weitere Informationen finden Sie unter [Häufig gestellte Fragen](#faq).

### Benutzerdefinierter Zeitplan {#custom-schedule}

Wählen Sie **[!UICONTROL Planen jeder Welle]**, um ein spezifisches Startdatum und eine spezifische Startzeit für jede Welle zu definieren. Die Wellen müssen nicht gleichmäßig verteilt sein (z. B:00 9.00, 11:0000, 17:0000, 20:30).

![](assets/campaign-wave-custom-schedule.png){width="80%"}

>[!NOTE]
>
>Der Mindestabstand zwischen dem Beginn zweier Schübe beträgt **30 Minuten**.

## Anwendungsfälle {#use-cases}

Mit dem Wave-Versand können Sie steuern, wann und wie viele Nachrichten gesendet werden. Dies kann die Zustellbarkeit verbessern, die Reputation des Absenders schützen und die Sendungen an Ihre betriebliche Kapazität anpassen. Erwägen Sie die Verwendung von Wellen in diesen Szenarien:

* **Callcenter- oder Reaktionsverwaltung:** begrenzen Sie, wie viele Nachrichten pro Tag oder pro Stunde gesendet werden, damit nachgelagerte Teams (z. B. die Kundenunterstützung) mit Antworten umgehen können. Senden Sie beispielsweise 20 Nachrichten pro Tag, um die Callcenter-Kapazität anzupassen.

  ![](assets/campaign-waves-ex-call-center.png){width="75%"}

* **Hohes Volumen und Zustellbarkeit:** Sie es, eine sehr große Kampagne nicht in einem Durchgang zu versenden. Verteilen Sie den Versand über einen längeren Zeitraum, um die Reputation des Absenders zu wahren und das Risiko zu reduzieren, als Spam gekennzeichnet zu werden.

  ![](assets/campaign-waves-ex-high-volume.png){width="75%"}

* **Ramp-up:** Wenn Sie eine neue Plattform oder IP verwenden, erhöhen Sie das Volumen progressiv (z. B. 10 % in der ersten Welle, dann 15 %, 20 % usw.), um die Reputation schrittweise aufzubauen.

  ![](assets/campaign-waves-ex-ramp-up.png){width="75%"}

## Häufig gestellte Fragen {#faq}

+++ Was passiert, wenn die Summe der Wellengrößen nicht der Gesamtzielgruppe entspricht?

* Wenn die Summe Ihrer Wellengrößen **die Zielgruppe übersteigt** (Sie planen z. B. 100.000 in der ersten Welle für eine Zielgruppe von 100.000), wird die erste Welle an die gesamte Zielgruppe gesendet und die verbleibenden Wellen haben niemanden mehr, an den sie senden können - sie werden nicht ausgeführt.
* Wenn die Summe **geringer ist** als die Zielgruppe (Sie definieren beispielsweise vier Schübe mit insgesamt 40.000 Profilen für eine Zielgruppe von 100.000), erhalten nur die in diesen Schüben enthaltenen Profile die Nachricht. Der Rest der Zielgruppe erhält die Kommunikation nicht und wird in späteren Schüben nicht erneut versucht.

+++

+++ Kann ich einzelnen Schüben unterschiedliche Segmente oder Kriterien zuweisen?

Sie können nur die Größe und den Zeitpunkt von Wellen definieren. Die Empfängerauswahl ist für die gesamte Kampagne identisch. Sie können einzelnen Schüben keine unterschiedlichen Segmente oder Kriterien zuweisen.

+++

## Nächste Schritte {#next}

* [Planen der Aktionskampagne](campaign-schedule.md) - Festlegen von Startdatum, Enddatum, Häufigkeit und Kurssteuerung.
* [Kampagne überprüfen und aktivieren](review-activate-campaign.md) - Kampagne überprüfen und live schalten.
