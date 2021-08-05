---
title: Über Adobe Experience Platform-Segmente
description: Erfahren Sie, wie Sie ein Adobe Experience Platformen-Segment konfigurieren
feature: Journeys
topic: Content-Management
role: User
level: Intermediate
source-git-commit: 2d882b8d10cc642b04705dd924fd2b129f4f78ac
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 100%

---

# Erste Schritte mit Segmenten {#about-segments}

Mit [!DNL Journey Optimizer] können Sie Adobe Experience Platform-Segmente mithilfe von Echtzeit-Kundenprofildaten direkt im Menü **[!UICONTROL Segmente]** erstellen und diese Segmente in Ihre Journeys einbinden.

Beachten Sie, dass Segmente auch vom Segmentierungs-Service selbst erstellt werden können. Weitere Informationen finden Sie in der [Dokumentation zum Adobe Experience Platform-Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de){target=&quot;_blank&quot;}.

Sie können die Segmente in Journeys auf verschiedene Weise nutzen:

* Verwenden Sie eine Orchestrierungsaktivität **Segment lesen**, um alle dem angegebenen Segment angehörenden Personen in die Journey eintreten zu lassen. Die in Ihrer Journey enthaltenen Nachrichten werden an die dem Segment angehörenden Personen gesendet. Nehmen wir an, Sie verfügen über ein Segment für „Silber-Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle Silber-Kunden in eine Journey eintreten, und ihnen eine Reihe personalisierter Nachrichten senden.

   Weiterführende Informationen zur Verwendung der Aktivität **[!UICONTROL Segment lesen]** finden Sie in [diesem Abschnitt](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Verwenden Sie die Ereignisaktivität **Segmentqualifizierung**, um Personen auf der Grundlage von Adobe Experience Platform-Segmenteintritten und -austritten zu veranlassen, in eine Journey einzutreten oder in einer Journey fortzufahren. So können Sie z. B. alle neuen Silber-Kunden in eine Journey eintreten lassen und ihnen Nachrichten senden. Weiterführende Informationen zur Verwendung der Aktivität finden Sie in [diesem Abschnitt](../building-journeys/segment-qualification-events.md).

* Erstellen Sie mithilfe des einfachen oder erweiterten Ausdruckseditors **komplexe Bedingungen** in Ihren Journeys. Weiterführende Informationen finden Sie in diesem [Abschnitt](../building-journeys/condition-activity.md#using-a-segment).
