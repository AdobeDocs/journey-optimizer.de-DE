---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit [!DNL Journey Optimizer] Konfiguration
description: Weitere Informationen [!DNL Journey Optimizer] Konfiguration
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---


# Erste Schritte mit [!DNL Journey Optimizer] Konfiguration {#start-optimizer-configuration}

Beim Zugriff auf [!DNL Journey Optimizer] Zum ersten Mal wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

Um Ihre Journeys erstellen und Nachrichten senden zu können, müssen Sie die folgenden Konfigurationsschritte durchlaufen.

## Nachrichten und Kanäle konfigurieren

1. Um Nachrichten erstellen und senden zu können, müssen Sie je nach Kanal bestimmte Konfigurationen durchführen.

   * Für **Email** -Kanal verwenden, müssen Sie Adobe Subdomains zuweisen und IP-Pools erstellen, um IP-Adressen zu gruppieren. [Weitere Infos](../email/get-started-email-config.md)

   * Für **Push** -Kanal, müssen Sie Push-Benachrichtigungseinstellungen in beiden [!DNL Adobe Experience Platform] und [!DNL Adobe Experience Platform Launch]. [Weitere Infos](../push/push-configuration.md)

   * Für **SMS** -Kanal, müssen Sie Ihre Instanz so konfigurieren, dass SMS gesendet wird, einschließlich der Integration der Provider-Einstellungen in [!DNL Journey Optimizer]. [Weitere Infos](../sms/sms-configuration.md)

1. Anschließend müssen Sie **Kanaloberflächen** um alle technischen Parameter zu konfigurieren, die für den Nachrichtenversand erforderlich sind. [Weitere Infos](channel-surfaces.md)

1. Sie können auch:

   * Verwalten Sie die Anzahl der Tage, in denen erneute Zustellversuche unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Infos](manage-suppression-list.md)

   * Aktivieren Sie die **BBC-E-Mail-Option** , um eine Kopie der an Einzelpersonen gesendeten Nachrichten aufzubewahren. [Weitere Infos](archiving-support.md#enable-bcc)

   * Konfigurieren **Frequenzregeln** um zu vermeiden, dass Ihre Empfänger überfordert werden. [Weitere Infos](frequency-rules.md)

   * Bestimmen Sie, welche E-Mail-Adresse und/oder Telefonnummer für Ihre Empfänger vorrangig verwendet werden soll, wenn in Adobe Experience Platform mehrere Adressen/Nummern verfügbar sind. [Weitere Infos](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Diese Schritte müssen von einem [Adobe Journey Optimizer-Systemadministrator](../start/path/administrator.md).

## Journeys konfigurieren

Um Journeys zu erstellen, müssen Sie **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** und **[!UICONTROL Actions]**. [Weitere Infos](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* Die **Datenquelle** Mit der -Konfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden. [Weitere Infos](../datasource/about-data-sources.md)

* **Veranstaltungen** ermöglichen es Ihnen, Ihre Journeys einheitlich auszulösen, um in Echtzeit Nachrichten an den Kontakt zu senden, der in die Journey gelangt. In der Ereigniskonfiguration konfigurieren Sie die Ereignisse, die in den Journeys erwartet werden. Die Daten der eingehenden Ereignisse werden nach dem Adobe Experience-Datenmodell (XDM) normalisiert. Ereignisse stammen aus Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). [Weitere Infos](../event/about-events.md)

* [!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen, mit denen Sie Inhalte entwerfen und versenden können. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, erstellen Sie eine **benutzerdefinierte Aktion**. [Weitere Infos](../action/action.md)