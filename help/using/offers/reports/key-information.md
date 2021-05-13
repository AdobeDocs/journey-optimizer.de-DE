---
title: Wichtige Informationen zu Entscheidungs-Management-Ereignissen
description: Erfahren Sie mehr über die wichtigen Informationen, die mit den einzelnen Entscheidungs-Management-Ereignissen gesendet werden.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 75%

---

# Entscheidungsverwaltung - Ereignis - Schlüsselinformationen {#events-key-information}

Jedes Ereignis, das gesendet wird, wenn eine Entscheidung getroffen wird, enthält vier wichtige Datenpunkte, die Sie für Analyse- und Reporting-Zwecke nutzen können.

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Name und ID des Fallback-Angebots, wenn kein personalisiertes Angebot ausgewählt wurde,
* **[!UICONTROL Placement]**: Name, ID und Kanal der Platzierung, über die das Angebot gesendet wird,
* **[!UICONTROL Selections]**: Name und ID des für das Profil ausgewählten Angebots,
* **[!UICONTROL Aktivität]**: Name und ID der Entscheidung (früher Angebot Aktivität).

Zusätzlich können Sie auch die Felder **[!UICONTROL identityMap]** und **[!UICONTROL Timestamp]** nutzen, um Informationen über das Profil und den Zeitpunkt, zu dem das Angebot zugestellt wurde, abzurufen.

Weitere Informationen zu allen XDM-Feldern, die mit jeder Entscheidung gesendet werden, finden Sie in [diesem Abschnitt](xdm-fields.md).
