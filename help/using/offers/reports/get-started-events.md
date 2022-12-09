---
title: Erste Schritte mit Entscheidungsverwaltungsereignissen
description: Erfahren Sie, wie Sie in Adobe Experience Platform Entscheidungsverwaltungsberichte erstellen.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Erste Schritte mit Entscheidungsverwaltungsereignissen {#monitor-offer-events}

Jedes Mal, wenn die Entscheidungsverwaltung eine Entscheidung für ein bestimmtes Profil trifft, werden Informationen zu diesen Ereignissen automatisch an Adobe Experience Platform gesendet.

Auf diese Weise können Sie diese Daten exportieren, um sie in Ihr eigenes Berichterstattungssystem zu analysieren. Sie können auch Adobe Experience Platform nutzen [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) in Kombination mit anderen Tools für erweiterte Analyse- und Berichtszwecke.

Auf Datensätze, die Entscheidungsverwaltungsereignisse enthalten, kann über Adobe Experience Platform zugegriffen werden. **[!UICONTROL Datasets]** Menü. Bei der Bereitstellung für jede Ihrer Instanzen wird automatisch ein Datensatz erstellt.

![](../assets/events-datasets-list.png)

Diese Datensätze basieren auf der **[!UICONTROL ODE DecisionEvents]** -Schema, das alle XDM-Felder enthält, die zum Senden von Informationen aus der Entscheidungsverwaltung an Adobe Experience Platform erforderlich sind.

>[!NOTE]
>
>Beachten Sie, dass ODE DecisionEvents -Datensätze **Nicht-Profil-Datensätze**, was bedeutet, dass sie nicht in Experience Platform aufgenommen werden können, um vom Echtzeit-Kundenprofil verwendet zu werden.

**Verwandte Themen:**

* [Wichtige Informationen zu Entscheidungsverwaltungsereignissen](../reports/key-information.md)
* [Zugreifen auf Ereignisse XDM-Felder](../reports/xdm-fields.md)
