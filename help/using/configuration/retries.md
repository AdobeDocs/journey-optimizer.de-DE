---
solution: Journey Optimizer
product: journey optimizer
title: Weitere Zustellversuche
description: Erfahren Sie, wie weitere Zustellversuche durchgeführt werden, bevor eine Adresse an die Unterdrückungsliste gesendet wird.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: weitere Zustellversuche, Bounce, soft, Optimizer, Fehler
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 0db7f514a2604ad09fbd9863a51d3c86d69eac41
workflow-type: ht
source-wordcount: '567'
ht-degree: 100%

---

# Weitere Zustellversuche {#retries}

Wenn die Zustellung einer E-Mai-Nachricht an eine bestimmte Adresse aufgrund eines temporären Fehlers vom Typ **Softbounce** fehlschlägt, werden mehrere weitere Zustellversuche unternommen. Jeder Fehler erhöht einen Fehlerzähler. Wenn dieser Zähler den Schwellenwert erreicht, wird die E-Mail-Adresse der Unterdrückungsliste hinzugefügt.

>[!NOTE]
>
>Weitere Informationen zu Fehlertypen finden Sie im Abschnitt [Typen von fehlgeschlagenem Versand](../reports/suppression-list.md#delivery-failures).

In der Standardkonfiguration ist der Schwellenwert auf fünf Fehler festgelegt.

* Beim fünften Fehler bei demselben Versand innerhalb des [Wiederholungszeitraums](#retry-duration) wird die Adresse unterdrückt.

* Wenn es unterschiedliche Sendungen gibt und zwei Fehler im Abstand von mindestens 24 Stunden auftreten, wird der Fehlerzähler bei jedem Fehler erhöht und die E-Mail-Adresse wird zudem beim fünften Versuch unterdrückt. Fehler sind pro Adresse kumulativ, d. h., sie werden addiert.

Wenn ein Versand nach einem erneuten Zustellversuch erfolgreich ist, wird der Fehlerzähler der E-Mail-Adresse auf null zurückgesetzt.

Beispiel:

* Am Montag senden Sie eine E-Mail mit einem Wiederholungszeitraum von 24 Stunden. Die Sendung kann der Adresse `emma.jones@mail.com` nicht zugestellt werden. Die E-Mail-Zustellung wird bis zu dreimal wiederholt und nach Ablauf des 24-Stunden-Wiederholungszeitraums angehalten.

* Am Mittwoch senden Sie eine weitere E-Mail, unter anderem wieder an die E-Mail-Adresse `emma.jones@mail.com`, bei der es bereits zu drei Fehlversuchen gekommen ist. Die Zustellung schlägt auch in diesem Fall zweimal fehl. Es kommen also zwei weitere Fehlversuche hinzu.

Wenn zwischen diesen beiden E-Mails kein anderer Versand erfolgreich durchgeführt wurde, wird die Adresse `emma.jones@mail.com`, aufgrund der kumulativen Wirkung von 3 + 2 Fehlern, der Unterdrückungsliste hinzugefügt.

## Bearbeitung des Schwellenwerts für Wiederholungsversuche {#edit-retry-threshold}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_bounces"
>title="Aktualisieren des Schwellenwerts für Wiederholungsversuche"
>abstract="Wenn der Standardwert nicht den Anforderungen entspricht, kann die zulässige Anzahl aufeinander folgender Softbounces geändert werden. Wenn die Wiederholungsanzahl den Fehlerschwellenwert für eine bestimmte E-Mail-Adresse erreicht, wird diese Adresse der Unterdrückungsliste hinzugefügt."
<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/deliverability/suppression-list.html" text="Understand the suppresion list"-->

Falls der Standardwert 5 Ihren Anforderungen nicht entspricht, können Sie den Fehlerschwellenwert wie unten beschrieben ändern.

1. Gehen Sie zu **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL Unterdrückungsliste]**.

1. Klicken Sie auf den Button **[!UICONTROL Unterdrückungsregeln bearbeiten]**.

   ![](assets/suppression-list-edit-retries.png)

1. Bearbeiten Sie die zulässige Anzahl aufeinanderfolgender Softbounces entsprechend Ihren Anforderungen.

   ![](assets/suppression-list-edit-soft-bounces.png)

   Sie müssen einen ganzzahligen Wert zwischen 1 und 20 eingeben, d. h. die Mindestanzahl weiterer Zustellversuche ist 1 und die maximale Anzahl ist 20.

   >[!CAUTION]
   >
   >Ein Wert von mehr als 10 kann Zustellbarkeitsprobleme hinsichtlich der Reputation sowie eine IP-Drosselung oder eine Blockierungsauflistung durch ISPs verursachen. [Weitere Informationen zur Zustellbarkeit](../reports/deliverability.md)

## Zeitraum für weitere Zustellversuche {#retry-duration}

Der **Zeitraum für weitere Zustellversuche** ist der Zeitraum, in dem alle E-Mail-Nachrichten des Versands, bei denen ein temporärer Fehler oder ein Softbounce aufgetreten ist, erneut gesendet werden.

Standardmäßig werden weitere Zustellversuche **3,5 Tage** (oder **84 Stunden**) lang ab dem Zeitpunkt durchgeführt, zu dem die Nachricht zur E-Mail-Warteschlange hinzugefügt wurde.

Um jedoch sicherzustellen, dass keine weiteren Zustellversuche durchgeführt werden, wenn sie nicht mehr benötigt werden, können Sie diese Einstellung Ihren Anforderungen entsprechend ändern, wenn Sie eine [Kanalkonfiguration](channel-surfaces.md) erstellen oder bearbeiten, die auf den E-Mail-Kanal angewendet wird.

Beispielsweise können Sie den Zeitraum für weitere Zustellversuche einer Transaktions-E-Mail, die sich auf das Zurücksetzen eines Passworts bezieht und einen nur für einen Tag gültigen Link enthält, auf 24 Stunden festlegen. Analog dazu könnten Sie für einen Midnight Sale den Zeitraum für weitere Zustellversuche auf 6 Stunden festlegen.

>[!NOTE]
>
>Der Zeitraum für weitere Zustellversuche darf 84 Stunden nicht überschreiten. Der Mindestzeitraum für weitere Zustellversuche beträgt 6 Stunden für Marketing-E-Mails und 10 Minuten für Transaktions-E-Mails.

In [diesem Abschnitt](../email/email-settings.md#email-retry) erfahren Sie, wie Sie die Parameter für weitere Zustellversuche für E-Mails anpassen, während Sie eine Kanalkonfiguration definieren.

