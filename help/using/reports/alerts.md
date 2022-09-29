---
title: Warnhinweise
description: Erfahren Sie, wie Sie Warnhinweise verwalten
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 3d0d1b7d092ffae48ded337d5a1b14a5f5c4653b
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 20%

---

# Erste Schritte mit Warnhinweisen {#alerts}

Journey Optimizer nutzt die Warnfunktionen von Adobe Experience Platform. Auf diese Weise können Sie über die Benutzeroberfläche auf Systemwarnungen zugreifen. Sie können die verfügbaren Warnungen anzeigen und abonnieren. Wenn bestimmte Bedingungen in Ihren Vorgängen erreicht werden (z. B. ein potenzielles Problem, wenn das System einen Schwellenwert überschreitet), werden Warnhinweise an alle Benutzer in Ihrer Organisation gesendet, die sich für sie angemeldet haben. Diese Nachrichten können sich über einen vordefinierten Zeitraum wiederholen, bis der Warnhinweis behoben wurde.

Weitere Informationen zu Warnhinweisen in Adobe Experience Platform [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=de).
Informationen zum Abonnieren und Konfigurieren von Warnungen finden Sie in diesem Abschnitt [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

Im linken Menü unter **Administration** klicken **Warnhinweise**. Ein vorkonfigurierter Warnhinweis für Journey Optimizer ist verfügbar. Dieser Warnhinweis warnt Sie, wenn ein Knoten des gelesenen Segments während des definierten Zeitraums kein Profil verarbeitet hat.

![](assets/alerts1.png)

Tritt ein solches unerwartetes Verhalten auf, wird eine Warnmeldung an Abonnenten des Warnhinweises per E-Mail und In-App-Benachrichtigung in der oberen rechten Ecke der Benutzeroberfläche gesendet.

![](assets/alerts2.png)

Wenn Sie [Warnhinweisregeln in der Platform-Benutzeroberfläche anzeigen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), können Sie jede Regel einzeln abonnieren. Beim Abonnieren von Warnhinweisen über [E/A-Ereignisbenachrichtigungen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html) sind Warnhinweisregeln jedoch in verschiedene Abonnementpakete unterteilt. Der E/A-Ereignis-Abonnementname, der dem Warnhinweis zum Lesen des Segments entspricht, lautet: &quot;Journey liest Segment-Verzögerungen, Fehler und Fehler&quot;.

>[!WARNING]
>
>Diese Warnhinweise gelten nur für lebende Journey. Warnhinweise werden für Journey im Testmodus nicht ausgelöst.