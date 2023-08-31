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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: ht
source-wordcount: '378'
ht-degree: 100%

---

# Erste Schritte mit Warnhinweisen {#alerts}

Journey Optimizer nutzt die Warnfunktionen von Adobe Experience Platform. Damit können Sie über die Benutzeroberfläche auf Systemwarnhinweise zugreifen. Sie können die verfügbaren Warnhinweise einsehen und abonnieren.

Wenn eine bestimmte Reihe von Bedingungen in Ihren Vorgängen erreicht wird (wie beispielsweise ein mögliches Problem, wenn das System einen Schwellenwert überschreitet), werden Warnmeldungen an alle Benutzerinnen und Benutzer in Ihrem Unternehmen gesendet, die diese abonniert haben.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Weitere Informationen zu Warnhinweisen in Adobe Experience Platform finden Sie in der [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=de).

Informationen zum Abonnieren und Konfigurieren von Warnhinweisen finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=de).

>[!AVAILABILITY]
>
>Einige Design-Änderungen werden derzeit für den Warnhinweis „Lesen des Zielgruppen-Triggers erfolglos“ eingepflegt. Daher wird dieser Warnhinweis vorerst ausgesetzt und vorübergehend aus der Benutzeroberfläche entfernt. Sobald diese Änderungen veröffentlicht werden, wird der Warnhinweis erneut angezeigt und kann abonniert werden.

Klicken Sie im linken Menü unter **Administration** auf **Warnhinweise**. Für Journey Optimizer ist ein vorkonfigurierter Warnhinweis verfügbar. Dieser Warnhinweis warnt Sie, wenn eine benutzerdefinierte Aktion fehlschlägt. Wir gehen davon aus, dass die Aktion fehlgeschlagen ist, wenn in den letzten 5 Minuten bei einer bestimmten benutzerdefinierten Aktion mehr als 1 % Fehler aufgetreten sind. Dies wird alle 30 Sekunden ausgewertet.

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Wenn ein unerwartetes Verhalten auftritt, wird den Abonnentinnen und Abonnenten des Warnhinweises basierend auf den Benutzereinstellungen per E-Mail oder direkt in Journey Optimizer in der oberen rechten Ecke der Benutzeroberfläche eine Benachrichtigung gesendet.

Wenn ein Warnhinweis aufgelöst wurde, erhalten Sie die Benachrichtigung „Aufgelöst“. Für den Warnhinweis zur benutzerdefinierten Aktion kann dies aus zwei Gründen passieren:
* In den letzten 5 Minuten ist kein Fehler bei dieser benutzerdefinierten Aktion aufgetreten (oder nur Fehler unter dem Schwellenwert von 1 %).
* Kein Profil hat diese benutzerdefinierte Aktion erreicht.

Wenn [Warnhinweisregeln in der Adobe Experience Platform-Benutzeroberfläche angezeigt werden](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=de), kann jede Regel einzeln abonniert werden. Beim Abonnieren von Warnhinweisen über [E/A-Ereignisbenachrichtigungen](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=de) sind Warnhinweisregeln jedoch in verschiedene Abonnementpakete unterteilt. Der Abonnementname des E/A-Ereignisses, das dem Warnhinweis für benutzerdefinierte Aktionen entspricht, lautet: „Benutzerdefinierte Journey-Aktion fehlgeschlagen“.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>Diese Warnhinweise gelten nur für Live-Journeys. Warnhinweise werden für Journeys im Testmodus nicht ausgelöst.

