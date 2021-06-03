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
source-git-commit: 80c307a349a8ca7449639e7819683bf1f3ec3d13
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 39%

---


# Weitere Zustellversuche {#retries}

Wenn eine Nachricht aufgrund eines temporären **Softbounce**- oder **Ignoriert**-Fehlers fehlschlägt, werden mehrere weitere Zustellversuche unternommen. Jeder Fehler erhöht einen Fehlerzähler. Wenn dieser Zähler den Grenzwert erreicht, wird die Adresse der Unterdrückungsliste hinzugefügt.

In der Standardkonfiguration<!--so can you edit this setting or not?? contradictory information was given--> ist der Schwellenwert auf drei Fehler festgelegt:

* Für denselben Versand wird beim dritten aufgetretenen Fehler die Adresse unterdrückt.

* Wenn es unterschiedliche Versände gibt und zwei Fehler im Abstand von mindestens 24 Stunden auftreten, wird der Fehlerzähler bei jedem Fehler erhöht und die E-Mail-Adresse wird ebenfalls beim dritten Versuch unterdrückt.

Wenn ein Versand nach einem erneuten Versuch erfolgreich war, wird der Fehlerzähler der Adresse neu initialisiert.

Sie können den Schwellenwert mithilfe der Schaltfläche **[!UICONTROL Bearbeiten]** im Menü **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Allgemein]**<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4--> ändern.

![](../assets/retries-edition.png)

## Dauer der Wiederholung von Nachrichten {#retry-duration}

Wiederholungen werden für **3,5 Tage** ab dem Zeitpunkt durchgeführt, zu dem die Nachricht zur E-Mail-Warteschlange hinzugefügt wurde.

Das Mindestintervall zwischen erneuten Zustellversuchen und die maximale Anzahl weiterer Zustellversuche <!--managed by the Enhanced MTA,--> basieren sowohl auf der historischen als auch aktuellen Leistung einer IP-Adresse in einer bestimmten Domain.

Nach 3,5 Tagen wird jede Nachricht aus der Warteschlange für weitere Versuche entfernt und als Bounce zurückgesendet.<!--???-->