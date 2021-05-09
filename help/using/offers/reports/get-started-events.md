---
title: Erste Schritte mit den Ereignissen zur Entscheidungsverwaltung
description: Erfahren Sie, wie Sie in Adobe Experience Platform Entscheidungsverwaltungsberichte erstellen.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Erste Schritte mit den Ereignissen für die Entscheidungsverwaltung {#monitor-offer-events}

Jedes Mal, wenn die Entscheidungsverwaltung eine Entscheidung für ein bestimmtes Profil trifft, werden Informationen zu diesen Ereignissen automatisch an Adobe Experience Platform gesendet.

Auf diese Weise können Sie diese Daten exportieren, um sie in Ihr eigenes Berichte-System zu analysieren. Sie können den Adobe Experience Platform [Abfrage Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) auch in Kombination mit anderen Tools nutzen, um die Analyse und den Berichte zu verbessern.

Auf die Datensätze mit Entscheidungsverwaltungs-Ereignissen kann über das Menü Adobe Experience Platform **[!UICONTROL Datensätze]** zugegriffen werden. Bei der Bereitstellung für jede Ihrer Instanzen wird automatisch ein Datensatz erstellt.

![](../assets/events-datasets-list.png)

Diese Datensätze basieren auf dem Schema **[!UICONTROL ODE DecisionEvents]**, das alle XDM-Felder enthält, die zum Senden von Informationen aus der Entscheidungsverwaltung an Adobe Experience Platform erforderlich sind.

>[!NOTE]
>
>Beachten Sie, dass ODE-DecisionEvents-Datasets **Nicht-Profil-Datensätze** sind, d. h., dass sie nicht in die Experience Platform aufgenommen werden können, um sie vom Echtzeit-Kunden-Profil zu verwenden.

**Verwandte Themen:**

* [Wichtige Informationen zu Entscheidungs-Management-Ereignissen](../reports/key-information.md)
* [Zugriff auf Ereignis-XDM-Felder](../reports/xdm-fields.md)
