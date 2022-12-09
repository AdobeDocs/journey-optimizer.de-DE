---
solution: Journey Optimizer
product: journey optimizer
title: Warnhinweise
description: Erfahren Sie, wie Sie Warnhinweise verwalten
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Erste Schritte mit Warnhinweisen {#alerts}

Journey Optimizer nutzt die Warnfunktionen von Adobe Experience Platform. Auf diese Weise können Sie über die Benutzeroberfläche auf Systemwarnungen zugreifen. Sie können die verfügbaren Warnungen anzeigen und abonnieren. Wenn bestimmte Bedingungen in Ihren Vorgängen erreicht werden (z. B. ein potenzielles Problem, wenn das System einen Schwellenwert überschreitet), werden Warnhinweise an alle Benutzer in Ihrer Organisation gesendet, die sich für sie angemeldet haben. Diese Nachrichten können sich über einen vordefinierten Zeitraum wiederholen, bis der Warnhinweis behoben wurde.

Weitere Informationen zu Warnhinweisen in Adobe Experience Platform [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html).
Informationen zum Abonnieren und Konfigurieren von Warnungen finden Sie in diesem Abschnitt [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

Im linken Menü unter **Administration** klicken **Warnhinweise**. Ein vorkonfigurierter Warnhinweis für Journey Optimizer ist verfügbar. Dieser Warnhinweis warnt Sie, wenn ein Knoten des gelesenen Segments während des definierten Zeitraums kein Profil verarbeitet hat.

![](assets/alerts1.png)

Tritt ein solches unerwartetes Verhalten auf, wird den Abonnenten des Warnhinweises per E-Mail oben rechts in der Benutzeroberfläche eine Warnmeldung gesendet.

![](assets/alerts2.png)

Wann [Anzeigen von Warnregeln in der Benutzeroberfläche von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)können Sie jede Regel einzeln abonnieren. Beim Abonnieren von Warnhinweisen über [E/A-Ereignisbenachrichtigungen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)Warnhinweisregeln sind jedoch in verschiedene Abonnementpakete unterteilt. Der E/A-Ereignis-Abonnementname, der dem Warnhinweis zum Lesen des Segments entspricht, lautet: &quot;Journey liest Segment-Verzögerungen, Fehler und Fehler&quot;.

>[!WARNING]
>
>Diese Warnhinweise gelten nur für Live-Journeys. Warnhinweise werden für Journeys im Testmodus nicht ausgelöst.
