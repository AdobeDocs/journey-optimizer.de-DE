---
title: Wichtige Informationen zu Entscheidungsverwaltungsereignissen
description: Erfahren Sie mehr über die wichtigsten Informationen, die mit jedem Entscheidungsverwaltungsereignis gesendet werden.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 07be59e8-e994-4854-8089-25614d005dbe
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Wichtige Informationen zu Entscheidungsverwaltungsereignissen {#events-key-information}

Jedes Ereignis, das bei einer Entscheidung gesendet wird, enthält vier wichtige Datenpunkte, die Sie für Analyse- und Berichtszwecke nutzen können.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Name und ID des Fallback-Angebots, wenn kein personalisiertes Angebot ausgewählt wurde,
* **[!UICONTROL Placement]**: Name, ID und Kanal der Platzierung, die zur Bereitstellung des Angebots verwendet wird,
* **[!UICONTROL Selections]**: Name und Kennung des für das Profil ausgewählten Angebots,
* **[!UICONTROL Activity]**: Name und ID der Entscheidung.

Darüber hinaus können Sie auch die **[!UICONTROL identityMap]** und **[!UICONTROL Timestamp]** -Felder, um Informationen zum Profil und zum Zeitpunkt der Bereitstellung des Angebots abzurufen.

Weitere Informationen zu allen XDM-Feldern, die mit jeder Entscheidung gesendet werden, finden Sie unter [diesem Abschnitt](xdm-fields.md).
