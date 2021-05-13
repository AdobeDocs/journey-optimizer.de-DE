---
title: Erste Schritte mit den Ereignissen zur Entscheidungsverwaltung
description: Erfahren Sie, wie Sie in Adobe Experience Platform Entscheidungsverwaltungsberichte erstellen.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 46%

---

# Erste Schritte mit den Ereignissen für die Entscheidungsverwaltung {#monitor-offer-events}

Jedes Mal, wenn die Entscheidungsverwaltung eine Entscheidung für ein bestimmtes Profil trifft, werden Informationen zu diesen Ereignissen automatisch an Adobe Experience Platform gesendet.

Dies ermöglicht Ihnen, diese Daten zu exportieren, um sie in Ihrem eigenen Berichtssystem zu analysieren. Sie können den Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=de) auch in Kombination mit anderen Tools für erweiterte Analyse- und Berichtszwecke nutzen.

Auf die Datensätze mit Entscheidungsverwaltungs-Ereignissen kann über das Menü Adobe Experience Platform **[!UICONTROL Datensätze]** zugegriffen werden. Für jede Ihrer Instanzen wird bei der Bereitstellung automatisch ein Datensatz erstellt.

![](../../assets/events-datasets-list.png)

Diese Datensätze basieren auf dem Schema **[!UICONTROL ODE DecisionEvents]**, das alle XDM-Felder enthält, die zum Senden von Informationen aus der Entscheidungsverwaltung an Adobe Experience Platform erforderlich sind.

>[!NOTE]
>
>Beachten Sie, dass es sich bei ODE DecisionEvents-Datensätzen um **Nicht-Profil-Datensätze** handelt, d. h. sie können nicht in Experience Platform aufgenommen werden, um vom Echtzeit-Kundenprofil verwendet zu werden.

**Verwandte Themen:**

* [Wichtige Informationen zu Entscheidungs-Management-Ereignissen](../reports/key-information.md)
* [Zugriff auf XDM-Felder von Ereignissen](../reports/xdm-fields.md)
