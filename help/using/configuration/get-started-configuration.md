---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit der Konfiguration von  [!DNL Journey Optimizer]
description: Weitere Informationen zur Konfiguration von  [!DNL Journey Optimizer]
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 70%

---


# Erste Schritte mit der Konfiguration von [!DNL Journey Optimizer] {#start-optimizer-configuration}

Beim erstmaligen Zugriff auf [!DNL Journey Optimizer] wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

Um Ihre Journey erstellen und Nachrichten senden zu können, müssen Sie die folgenden Konfigurationsschritte ausführen.

## Nachrichten und Kanäle konfigurieren

Definieren Sie Kanaloberflächen, passen Sie die Nachrichten an und passen Sie sie an.

* [An die Adobe der Subdomains delegieren](about-subdomain-delegation.md) Sie möchten zum Senden von E-Mails und [Erstellen von IP-Pools](ip-pools.md) , um IP-Adressen zu gruppieren, die für Ihre Instanz bereitgestellt wurden.

* Verwalten Sie die Anzahl der Tage, in denen weitere Zustellversuche unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](manage-suppression-list.md)

* Definieren Sie Push-Benachrichtigungseinstellungen sowohl in [!DNL Adobe Experience Platform] als auch in [!DNL Adobe Experience Platform Launch]. [Weitere Informationen](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* Konfigurieren Sie Ihre Instanz für den Versand von SMS (derzeit nur für eine Reihe von Organisationen verfügbar – eingeschränkte Verfügbarkeit). [Weitere Informationen](../sms/sms-configuration.md)

* Erstellen Sie Kanaloberflächen, um alle technischen Parameter zu konfigurieren, die zum Versand von Nachrichten erforderlich sind. [Weitere Informationen](channel-surfaces.md)

* Bestimmen Sie, welche E-Mail-Adresse und/oder Telefonnummer für Ihre Empfänger vorrangig verwendet werden soll, wenn in Adobe Experience Platform mehrere Adressen/Nummern verfügbar sind. [Weitere Informationen](primary-email-addresses.md)

## Konfigurieren von Journeys

Um Journey zu erstellen, müssen Sie **[!UICONTROL Data Sources]**, **[!UICONTROL Veranstaltungen]** und **[!UICONTROL Aktionen]**. [Weitere Informationen](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* Mit der Konfiguration von **Datenquellen** können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Journeys abzurufen. [Weitere Informationen](../datasource/about-data-sources.md)

* Mithilfe von **Ereignissen** können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten. In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). [Weitere Informationen](../event/about-events.md)

* [!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen, mit denen Sie Inhalte entwerfen und versenden können. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, erstellen Sie eine **benutzerdefinierte Aktion**. [Weitere Informationen](../action/action.md)