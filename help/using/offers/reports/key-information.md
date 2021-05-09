---
title: Wichtige Informationen zu Entscheidungs-Management-Ereignissen
description: Erfahren Sie mehr über die wichtigen Informationen, die mit den einzelnen Entscheidungs-Management-Ereignissen gesendet werden.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Entscheidungsverwaltung - Ereignis - Schlüsselinformationen {#events-key-information}

Jedes Ereignis, das bei einer Entscheidungsfindung gesendet wird, enthält vier wichtige Datenpunkte, die Sie für Analyse und Berichte nutzen können.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Name und ID des Ausweichzeichens, falls kein personalisiertes Angebot ausgewählt wurde,
* **[!UICONTROL Platzierung]**: Name, ID und Kanal der Platzierung, die zur Bereitstellung des Angebots verwendet wird,
* **[!UICONTROL Auswahl]**: Name und ID des für das Profil ausgewählten Angebots,
* **[!UICONTROL Aktivität]**: Name und ID der Entscheidung (früher Angebot Aktivität).

Darüber hinaus können Sie auch die Felder **[!UICONTROL identityMap]** und **[!UICONTROL Zeitstempel]** nutzen, um Informationen zum Profil und zum Zeitpunkt der Auslieferung des Angebots abzurufen.

Weitere Informationen zu allen XDM-Feldern, die mit jeder Entscheidung gesendet werden, finden Sie in [diesem Abschnitt](xdm-fields.md).
