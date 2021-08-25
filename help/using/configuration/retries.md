---
title: Weitere Zustellversuche
description: Erfahren Sie, wie weitere Zustellversuche durchgeführt werden, bevor eine Adresse an die Unterdrückungsliste gesendet wird.
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 38%

---


# Weitere Zustellversuche {#retries}

Wenn eine E-Mail-Nachricht aufgrund eines temporären **Softbounce**- oder **Ignoriert**-Fehlers fehlschlägt, werden mehrere weitere Zustellversuche unternommen. Jeder Fehler erhöht einen Fehlerzähler. Wenn dieser Zähler den Schwellenwert erreicht, wird die Adresse der Unterdrückungsliste hinzugefügt.

>[!NOTE]
>
>Weitere Informationen zu Fehlertypen finden Sie im Abschnitt [Typen für fehlgeschlagene Sendungen](../suppression-list.md#delivery-failures) .

In der Standardkonfiguration ist der Schwellenwert auf drei Fehler festgelegt:

* Im selben Versand wird die Adresse nach dem dritten fehlgeschlagenen Versuch unterdrückt.

* Wenn es unterschiedliche Sendungen gibt und zwei Fehler im Abstand von mindestens 24 Stunden auftreten, wird der Fehlerzähler bei jedem Fehler erhöht und die E-Mail-Adresse wird ebenfalls beim dritten Versuch unterdrückt.

Wenn ein Versand nach einem erneuten Zustellversuch erfolgreich war, wird der Fehlerzähler der E-Mail-Adresse auf null zurückgesetzt.

Sie können den Schwellenwert mithilfe der Schaltfläche **[!UICONTROL Bearbeiten]** im Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Allgemein]** ändern.

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## Zeitraum für Wiederholung {#retry-duration}

Der **Zeitraum für den erneuten Versuch** ist der Zeitraum, in dem alle E-Mail-Nachrichten des Versands, bei denen ein temporärer Fehler oder ein Softbounce aufgetreten ist, wiederholt werden.

Standardmäßig werden für **3,5 Tage** (oder **84 Stunden**) ab dem Zeitpunkt, zu dem die Nachricht zur E-Mail-Warteschlange hinzugefügt wurde, weitere Zustellversuche unternommen.

Um jedoch sicherzustellen, dass Wiederholungsversuche nicht mehr durchgeführt werden, wenn sie nicht mehr benötigt werden, können Sie diese Einstellung Ihren Anforderungen entsprechend ändern, wenn Sie eine [Nachrichtenvorgabe](message-presets.md) erstellen oder bearbeiten, die auf den E-Mail-Kanal angewendet wird.

Beispielsweise können Sie die Wiederholungsfrist für eine Transaktions-E-Mail, die sich auf das Zurücksetzen des Kennworts bezieht und einen nur für einen Tag gültigen Link enthält, auf 24 Stunden festlegen. In ähnlicher Weise können Sie für einen Verkauf um Mitternacht eine Wiederholungszeit von 6 Stunden festlegen.

>[!NOTE]
>
>Der Wiederholungszeitraum darf 84 Stunden nicht überschreiten. Die Wiederholungsdauer beträgt mindestens 6 Stunden für Marketing-E-Mails und 10 Minuten für Transaktions-E-Mails.

Erfahren Sie, wie Sie die E-Mail-Wiederholungsparameter beim Erstellen einer Nachrichtenvorgabe in [diesem Abschnitt](message-presets.md#create-message-preset) anpassen.

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->