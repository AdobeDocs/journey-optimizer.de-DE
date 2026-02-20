---
solution: Journey Optimizer
product: journey optimizer
title: Senden mit Schüben in Journey
description: Planen Sie den Versand ausgehender Journey-Nachrichten in kontrollierten Batches (Schüben) im Zeitverlauf. Der Wave-Versand in den Journey-Modi für lesbare Zielgruppen hilft, Last zu verteilen und die Zustellbarkeit zu unterstützen.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
keywords: Schübe, Batches, Zeitplan, Journey, Zielgruppe lesen, Zustellbarkeit
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 1%

---

# Senden mit Schüben in Journey {#send-using-waves-journeys}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Sie können ausgehende Nachrichten von einer Journey im Zeitverlauf stapelweise (in Schüben) statt alle gleichzeitig versenden. Der Wave-Versand trägt dazu bei, die Auslastung auszugleichen, überlastete nachgelagerte Systeme (wie Callcenter oder Landingpages) zu vermeiden und die Zustellbarkeit und die Reputation des Absenders zu unterstützen - insbesondere für Journey mit großen Lesemengen.

<!--
>[!CAUTION]
>
>Wave sending is available for read audience journeys only and applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Sie konfigurieren ihn auf Journey-Ebene, wenn Sie definieren, wie die Zielgruppe eintritt und wie Aktionen geplant werden. Sie definieren die Anzahl der Schübe, ihre Größe (als Prozentsatz der Zielgruppe oder als absolute Zahlen) und den Zeitpunkt, zu dem jede Schübe ausgeführt wird.

## Einschränkungen und Leitplanken {#limitations-guardrails}

* Das Senden von Wellen ist nur für Journey mit dem Typ „Zielgruppe lesen“ mit dem **[!DNL As soon as possible]** und **[!UICONTROL Einmal]** verfügbar. Weitere Informationen zum [Journey-Zeitplan](read-audience.md#schedule).
* Das Senden von Wellen ist für wiederkehrende, ereignisgesteuerte, Geschäftsereignis-, Testmodus- oder Probelauf-Journey nicht verfügbar.
* Sie müssen mindestens **2 Schübe definieren** und können bis zu **10 Schübe hinzufügen**.
* Der Mindestabstand zwischen dem Beginn zweier Schübe beträgt **30 Minuten**.
* Ein Wellenstart kann nicht vor dem Journey-Start oder in der Vergangenheit erfolgen.
* Die Aufteilung der Zielgruppe in Wellen kann bis zu 1 Stunde dauern. Die Profile dürfen die Journey erst dann betreten.
* Innerhalb einer Journey-Version laufen nie zwei Schübe gleichzeitig. Die nächste Welle beginnt erst, nachdem die vorherige Welle beendet wurde. Wenn beispielsweise Wellen in einem Abstand von 1 Stunde geplant werden, die erste Welle jedoch 2 Stunden lang läuft, beginnt die zweite Welle mit dem Ende der ersten Welle, nicht zu ihrer geplanten Zeit.
* Wellenstarts können verzögert werden, wenn die Plattform Quotenbegrenzungen anwendet oder wenn die Systemkapazität stark ausgelastet ist.

## Konfigurieren des Wave-Sendens auf einer Journey {#configure-wave-sending}

1. Starten Sie Ihren Journey mit einer Aktivität [Zielgruppe lesen](read-audience.md).

1. Doppelklicken Sie auf die Aktivität **[!UICONTROL Zielgruppe lesen]**, um ihre Eigenschaften zu öffnen, und wählen Sie die Option **[!UICONTROL Journey-Aktion in Schüben]**.

   ![](assets/journey-wave-option.png){width="100%"}

1. Legen Sie die **Anzahl der Schübe** fest (z. B. 4).

   ![](assets/journey-wave-number.png){width="80%"}

   >[!NOTE]
   >
   >Sie müssen mindestens 2 Schübe definieren und können bis zu 10 Schübe hinzufügen.

1. Wählen Sie wie unten beschrieben, wie Wellengröße und Timing definiert werden.

### Gleichmäßige Wellen {#equal-waves}

Standardmäßig wird die Zielgruppe in gleich große Schübe unterteilt. Legen Sie ein festes Intervall zwischen dem Beginn jeder Welle fest (z. B. 2 Stunden).

![](assets/journey-equal-waves.png){width="70%"}

>[!NOTE]
>
>Der Mindestabstand zwischen dem Beginn zweier Schübe beträgt **30 Minuten**.

Das System plant dann die nachfolgenden Wellen automatisch (z. B. erste Welle um 9 :00 Uhr, zweite um 11 :00 Uhr, dritte um :00 Uhr, vierte um 15 :00 Uhr).

### Benutzerdefinierte Verteilung {#custom-distribution}

Wählen Sie die Option **[!UICONTROL Benutzerdefinierte Verteilung]** aus, um die Größe jeder Welle als Prozentsatz der gesamten Zielgruppe zu definieren (z. B. 15 %, 20 %, 25 %, 40 %).

![](assets/journey-wave-percentage.png){width="70%"}

>[!NOTE]
>
>Die Summe über alle Wellen hinweg muss 100% betragen. Ist dies nicht der Fall, wird eine Warnmeldung angezeigt.<!--are the waves actually sent or does the system prevent user from saving the journey?-->

Wählen Sie **[!UICONTROL Zahlen]** aus, um die Größe jeder Welle als absolute Anzahl von Profilen zu definieren (z. B. 10.000; 50.000).

![](assets/journey-wave-numbers.png){width="70%"}

>[!NOTE]
>
>Bei der Verwendung von Zahlen überprüft das System nicht, ob die Summe die gesamte Zielgruppe abdeckt. Sie müssen sicherstellen, dass Ihre Wellengrößen die Zielgruppe abdecken, die Sie senden möchten. Weitere Informationen finden Sie unter [Häufig gestellte Fragen](#faq).

### Benutzerdefinierter Zeitplan {#custom-schedule}

Wählen Sie **[!UICONTROL Planen jeder Welle]**, um ein spezifisches Startdatum und eine spezifische Startzeit für jede Welle zu definieren. Die Wellen müssen nicht gleichmäßig verteilt sein (z. B:00 9.00, 11:0000, 17:0000, 20:30).

![](assets/journey-wave-custom-schedule.png){width="70%"}

>[!NOTE]
>
>Der Mindestabstand zwischen dem Beginn zweier Schübe beträgt **30 Minuten**.

## Anwendungsfälle {#use-cases}

Mit dem Wave-Versand können Sie steuern, wann und wie viele Nachrichten gesendet werden. Dies kann die Zustellbarkeit verbessern, die Reputation des Absenders schützen und die Sendungen an Ihre betriebliche Kapazität anpassen. Erwägen Sie die Verwendung von Wellen in diesen Szenarien:

* **Callcenter- oder Reaktionsverwaltung:** begrenzen Sie, wie viele Nachrichten pro Tag oder pro Stunde gesendet werden, damit nachgelagerte Teams (z. B. die Kundenunterstützung) mit Antworten umgehen können. Senden Sie beispielsweise 20 Nachrichten pro Tag, um die Callcenter-Kapazität anzupassen.

  ![](assets/journey-waves-ex-call-center.png){width="55%"}

* **Hohes Volumen und Zustellbarkeit:** Vermeiden Sie den Versand eines sehr großen Journey-Versands in einem Schuss. Verteilen Sie den Versand über einen längeren Zeitraum, um die Reputation des Absenders zu wahren und das Risiko zu reduzieren, als Spam gekennzeichnet zu werden.

  ![](assets/journey-waves-ex-high-volume.png){width="55%"}

* **Ramp-up:** Wenn Sie eine neue Plattform oder IP verwenden, erhöhen Sie das Volumen progressiv (z. B. 10 % in der ersten Welle, dann 15 %, 20 % usw.), um die Reputation schrittweise aufzubauen.

  ![](assets/journey-waves-ex-ramp-up.png){width="55%"}

## Häufig gestellte Fragen {#faq}

+++ Was passiert, wenn die Summe der Wellengrößen nicht der Gesamtzielgruppe entspricht?

* Wenn die Summe Ihrer Wellengrößen **die Zielgruppe übersteigt** (Sie planen z. B. 100.000 in der ersten Welle für eine Zielgruppe von 100.000), wird die erste Welle an die gesamte Zielgruppe gesendet und die verbleibenden Wellen haben niemanden mehr, an den sie senden können - sie werden nicht ausgeführt.
* Wenn die Summe **geringer ist** als die Zielgruppe (Sie definieren beispielsweise vier Schübe mit insgesamt 40.000 Profilen für eine Zielgruppe von 100.000), erhalten nur die in diesen Schüben enthaltenen Profile die Nachricht. Der Rest der Zielgruppe erhält die Kommunikation nicht und wird in späteren Schüben nicht erneut versucht.

+++

+++ Kann ich einzelnen Schüben unterschiedliche Segmente oder Kriterien zuweisen?

Sie können nur die Größe und den Zeitpunkt von Wellen definieren. Die Journey wird von derselben Zielgruppe durchlaufen. Sie können den einzelnen Schüben keine unterschiedlichen Segmente oder Kriterien zuweisen.

+++

## Siehe auch {#see-also}

* [Zielgruppe auf einer Journey verwenden](read-audience.md) Konfigurieren Sie die Aktivität „Zielgruppe lesen“.
