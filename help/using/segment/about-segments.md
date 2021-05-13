---
title: Über Adobe Experience Platform-Segmente
description: Erfahren Sie, wie Sie ein Adobe Experience Platformen-Segment konfigurieren
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 22%

---

# Über Adobe Experience Platform-Segmente {#about-segments}

![](../assets/do-not-localize/badge.png)

Mit Journey Optimizer können Sie Adobe Experience Platform-Profil-Daten mit Echtzeit-Kundendaten direkt aus dem Menü **[!UICONTROL Segmente]** erstellen und diese in Ihre Journey nutzen.

Beachten Sie, dass Segmente auch vom Segmentierungsdienst selbst erstellt werden können. Weitere Informationen finden Sie in der Dokumentation zum Adobe Experience Platform-Segmentdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).[

Sie können Segmente auf unterschiedliche Weise in Journey nutzen:

* Verwenden Sie eine **Aktivität zum Lesen**-Orchester, um alle dem angegebenen Segment angehörenden Personen in die Journey einzutragen. Die in Ihrer Journey enthaltenen Nachrichten werden an die dem Segment angehörenden Personen gesendet. Nehmen wir an, Sie verfügen über ein Segment für „Silber-Kunden“. Mit dieser Aktivität können Sie alle Silber-Kunden in eine Journey einbinden und ihnen eine Reihe personalisierter Nachrichten senden.

   Weitere Informationen zur Verwendung der Aktivität **[!UICONTROL Read segment]** finden Sie in [diesem Abschnitt](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Verwenden Sie die Aktivität **Segmentqualifizierung**, um Einzelpersonen basierend auf den Ein- und Ausstiegen des Adobe Experience Platform-Segments in eine Journey einzusteigen oder vorwärts zu bewegen. So können Sie z.B. alle Neukunden von Silber in eine Journey eintragen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung der Aktivität finden Sie in [diesem Abschnitt](../building-journeys/segment-qualification-events.md).

* Erstellen Sie mithilfe des einfachen oder erweiterten Ausdruck-Editors **komplexe Bedingungen** in Ihren Journey. Weiterführende Informationen finden Sie in diesem [Abschnitt](../building-journeys/condition-activity.md#using-a-segment).
