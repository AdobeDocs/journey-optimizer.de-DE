---
title: Journey Optimizer-Einstellungen und Konfigurationsrichtlinien
description: Informationen zu den Konfigurationsrichtlinien für Nachrichten und Journey
audience: administrators
content-type: reference
role: Administrator
level: Intermediate
product: Adobe Journey Optimizer
solution: Journey Optimizer
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
source-git-commit: 03d003682d796906fcf89af02aa98d549b5214a3
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 29%

---


# Erste Schritte mit der [!DNL Journey Optimizer]-Konfiguration

Beim erstmaligen Zugriff auf [!DNL Journey Optimizer] wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

Um Journey erstellen und Nachrichten senden zu können, gehen Sie wie folgt vor:

1. **Konfigurieren von Nachrichten und Kanälen**: Vorgaben definieren, E-Mail- und Push-Nachrichten anpassen

   * Definieren Sie Push-Benachrichtigungseinstellungen sowohl in [!DNL Adobe Experience Platform] als auch in [!DNL Adobe Experience Platform Launch]. [Weitere Infos](../push-gs.md)

   * Erstellen Sie Nachrichtenvorgaben, um alle technischen Parameter zu konfigurieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind. [Weitere Infos](message-presets.md)

   * Bestimmen Sie, welche E-Mail-Adresse für Ihre Empfänger vorrangig verwendet werden soll, wenn in Adobe Experience Platform mehrere Adressen verfügbar sind. [Weitere Infos](primary-email-addresses.md)

   * Verwalten Sie die Anzahl der Tage, in denen erneute Zustellversuche unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Infos](manage-suppression-list.md)

   <!--
    * Understand push notification flow. [Learn more](../push-gs.md)
    -->

1. **Zuweisen von Subdomains**: für jede neue Subdomain, die in Journey Optimizer verwendet werden soll, besteht der erste Schritt darin, sie zu delegieren. [Weitere Infos](about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Erstellen von IP-Pools**: Verbessern Sie die Zustellbarkeit und Reputation Ihrer E-Mail, indem Sie IP-Adressen gruppieren, die mit Ihrer Instanz bereitgestellt wurden. [Weitere Infos](ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Journey konfigurieren**: Um Journey zu erstellen, müssen Sie  **[!UICONTROL Data Sources]**,  **** Ereignisse und  **[!UICONTROL Aktionen]** konfigurieren. [Weitere Infos](about-data-sources-events-actions.md)

   ![](../assets/admin-menu.png)

   * Mit der **Datenquelle**-Konfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journey verwendet werden. Weitere Informationen zu Datenquellen finden Sie in diesem [Abschnitt](../datasource/about-data-sources.md).

   * **Mit Hilfe von Ereignissen können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Personen zu senden, die in die Journey hineinkommen.** In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). Weitere Informationen zu Ereignissen finden Sie in [diesem Abschnitt](../event/about-events.md).

   * [!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen: Sie können Ihren Inhalt entwerfen und Ihre Nachricht veröffentlichen. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, erstellen Sie eine **benutzerdefinierte Aktion**. Weitere Informationen zu Aktionen finden Sie in [diesem Abschnitt](../action/action.md).