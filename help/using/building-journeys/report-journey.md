---
solution: Journey Optimizer
product: journey optimizer
title: Veröffentlichen der Journey
description: Erfahren Sie, wie Sie Berichte auf Ihrer Journey erstellen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: veröffentlichen, Journey, live, Gültigkeit, prüfen
source-git-commit: 59a597a563074fa4daa74c64e97f6bb5c0f6834d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 3%

---

# Live-Bericht auf der Journey-Arbeitsfläche {#report-journey}

>[!NOTE]
>
>Wenn keine Daten in Ihrem Journey-Live-Bericht angezeigt werden, müssen Ihre Zugriffsberechtigungen um die Berechtigung **[!UICONTROL Journey-Bericht anzeigen]** erweitert werden. [Weitere Informationen](../administration/permissions.md)

Nach der Veröffentlichung Ihrer Journey stellt **Live Reporting** Metriken aus den letzten 24 Stunden direkt auf der Arbeitsfläche des Journey bereit.

Die angezeigten Ereignisse traten innerhalb der letzten 24 Stunden auf, wobei das Intervall zwischen dem Ereignis und seiner Anzeige mindestens zwei Minuten beträgt (in der Regel innerhalb von fünf Minuten).

![](assets/journey_live_report.png)

Für Ihre Live-Journey haben Sie Zugriff auf:

* **[!UICONTROL Eingegebene Profile]**: Gesamtzahl der Kontakte, die an dieser Aktivität teilgenommen haben.
* **[!UICONTROL Ausstieg profiled]**: Gesamtzahl der Kontakte, die die Journey aufgrund eines Ausstiegskriteriums aus dieser Aktivität beendet haben.
* **[!UICONTROL Fehler-Profile]**: Gesamtzahl der Kontakte, bei denen während des Journey ein Fehler aufgetreten ist.
* **[!UICONTROL Verworfene Profile]**: Gesamtzahl der Kontakte, die aus einem der folgenden Gründe von der Journey verworfen wurden:

   * Bei Aktivitäten mit **Zielgruppenqualifikation** kann ein Verwerfen auftreten, wenn das erwartete Verb für die Zielgruppenqualifikation nicht mit dem übereinstimmt, was Journey erhalten hat (z. B. &quot;beendet&quot; statt &quot;realisiert&quot;).
   * Bei Journey mit **ereignisausgelöstem** kann ein Rückwurf auftreten, wenn der Kontakt versucht hat, die Journey zu früh erneut aufzurufen, oder wenn eine erneute Einsendung nicht zulässig war.
   * Bei **wiederkehrenden** Journey wird ein Rückwurf bei jedem erneuten Eintritt gezählt, wenn der Kontakt bereits im Journey ist und die Wiedereintrittspolitik nicht auf &quot;Wiedereintritt erzwingen&quot;gesetzt ist.
   * Bei Aktivitäten vom Typ **Audience lesen** tritt ein Fehler auf, wenn für die exportierte Person keine Identität festgelegt wurde oder wenn der empfangene Identitäts-Namespace nicht mit dem erwarteten für die Journey übereinstimmt.

Für jede Aktivität innerhalb jeder Live-Journey haben Sie Zugriff auf:

* **[!UICONTROL Eingegebene Profile]**: Gesamtzahl der Kontakte, die an dieser Aktivität teilgenommen haben.
* **[!UICONTROL Ausstiegsprofil]**: Gesamtzahl der Kontakte, die die Journey aufgrund eines Ausstiegskriteriums aus dieser Aktivität beendet haben.
* **[!UICONTROL Fehler]**: Gesamtzahl der Kontakte, bei denen ein Fehler bei dieser Aktivität aufgetreten ist.
