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
feature: Anwendungskonfiguration
topic: Administration.
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: ht
source-wordcount: '215'
ht-degree: 100%

---


# Weitere Zustellversuche {#retries}

Wenn eine Nachricht aufgrund eines temporären Fehlers des Typs **Softbounce** oder **Ignoriert** fehlschlägt, werden mehrere weitere Zustellversuche unternommen. Jeder Fehler erhöht einen Fehlerzähler. Wenn dieser Zähler den Schwellenwert erreicht, wird die Adresse der Unterdrückungsliste hinzugefügt.

In der Standardkonfiguration<!--so can you edit this setting or not?? contradictory information was given--> ist der Schwellenwert auf drei Fehler festgelegt:

* Im selben Versand wird die Adresse nach dem dritten fehlgeschlagenen Versuch unterdrückt.

* Wenn es unterschiedliche Sendungen gibt und zwei Fehler im Abstand von mindestens 24 Stunden auftreten, wird der Fehlerzähler bei jedem Fehler erhöht und die E-Mail-Adresse wird ebenfalls beim dritten Versuch unterdrückt.

Wenn ein Versand nach einem erneuten Zustellversuch erfolgreich war, wird der Fehlerzähler der E-Mail-Adresse auf null zurückgesetzt.

Sie können den Schwellenwert mithilfe der Schaltfläche **[!UICONTROL Bearbeiten]** im Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Allgemein]** ändern.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Dauer der Wiederholung von Zustellversuchen für Nachrichten {#retry-duration}

Weitere Zustellversuche werden für **3,5 Tage** ab dem Zeitpunkt durchgeführt, zu dem die Nachricht zur E-Mail-Warteschlange hinzugefügt wurde.

Das Mindestintervall zwischen erneuten Zustellversuchen und die maximale Anzahl weiterer Zustellversuche <!--managed by the Enhanced MTA,--> basieren sowohl auf der historischen als auch aktuellen Leistung einer IP-Adresse in einer bestimmten Domain.

Nach 3,5 Tagen wird jede Nachricht aus der Warteschlange für weitere Versuche entfernt und als Bounce zurückgesendet.<!--???-->