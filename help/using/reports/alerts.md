---
solution: Journey Optimizer
product: journey optimizer
title: Warnhinweise
description: Erfahren Sie, wie Sie Warnhinweise verwalten.
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 94%

---

# Erste Schritte mit Warnhinweisen {#alerts}

Journey Optimizer nutzt die Warnfunktionen von Adobe Experience Platform. Damit können Sie über die Benutzeroberfläche auf Systemwarnhinweise zugreifen. Sie können die verfügbaren Warnhinweise anzeigen und abonnieren. Wenn bestimmte Bedingungen in Ihren Arbeitsablauf erfüllt sind (z. B. ein potenzielles Problem, wenn das System einen Schwellenwert überschreitet), werden allen Benutzern in Ihrer Organisation, die sich dafür angemeldet haben, Warnhinweise zugesendet. Diese Nachrichten können sich über einen vordefinierten Zeitraum wiederholen, bis der Warnhinweis behoben wurde.

Weitere Informationen zu Warnhinweisen in Adobe Experience Platform finden Sie in der [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=de).
Informationen zum Abonnieren und Konfigurieren von Warnhinweisen finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=de).

Klicken Sie im linken Menü unter **Administration** auf **Warnhinweise**. Für Journey Optimizer ist ein vorkonfigurierter Warnhinweis verfügbar. Dieser Warnhinweis warnt Sie, wenn ein Knoten vom Typ „Segment lesen“ innerhalb des festgelegten Zeitrahmens kein Profil verarbeitet hat.

![](assets/alerts1.png)

Tritt ein solches unerwartetes Verhalten auf, wird eine Warnmeldung per E-Mail an Abonnenten von Warnhinweisen gesendet und als In-App-Benachrichtigung in der rechten oberen Ecke der Benutzeroberfläche angezeigt.

![](assets/alerts2.png)

Wann [Anzeigen von Warnregeln in der Adobe Experience Platform-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)können Sie jede Regel einzeln abonnieren. Beim Abonnieren von Warnhinweisen über [E/A-Ereignisbenachrichtigungen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=de) sind Warnhinweisregeln jedoch in verschiedene Abonnementpakete unterteilt. Der I/O-Ereignis-Abonnementname, der dem Warnhinweis für „Segment lesen“ entspricht, lautet: „Verzögerungen, Fehler und Fehler für Segment lesen in Journey“.

>[!WARNING]
>
>Diese Warnhinweise gelten nur für Live-Journeys. Warnhinweise werden für Journeys im Testmodus nicht ausgelöst.
