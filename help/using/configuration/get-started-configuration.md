---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit der Konfiguration  [!DNL Journey Optimizer]  Kanälen
description: Weitere Informationen zur Konfiguration  [!DNL Journey Optimizer]  Kanälen
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: Konfiguration, Konfigurieren, Nachrichten, Kanal, Sandbox, Optimizer
source-git-commit: e052cf9bcd42cecbaaeb9047990ed603dd0730a0
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 64%

---


# Erste Schritte mit der Konfiguration von Kanälen {#start-optimizer-configuration}

Beim erstmaligen Zugriff auf [!DNL Journey Optimizer] wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.


Um Nachrichten senden zu können, müssen Sie die unten aufgeführten Konfigurationsschritte durchlaufen:

1. Definieren Sie als [Adobe Journey Optimizer-](../start/path/administrator.md) Ihre Kanalkonfigurationen. Auf den folgenden Seiten erfahren Sie, wie Sie diese Konfigurationen einrichten:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/get-started-email-config.md"><img alt="E-Mail" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/get-started-email-config.md"><strong>E-Mail</strong></a></div></td>
<td><a href="../sms/sms-configuration.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/push-configuration.md"><img alt="Push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/push-configuration.md"><strong>Push-Benachrichtigung</strong></a></div></td>
<td><a href="../direct-mail/direct-mail-configuration.md"><img alt="Direkt-Mail" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>Direkt-Mail</strong></a></div></td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../in-app/inapp-configuration.md"><img alt="In-App" src="../channels/assets/do-not-localize/inapp.jpg"></a>
<div align="center"><a href="../in-app/inapp-configuration.md"><strong>In-App</strong></a></div></td>
<td><a href="../web/web-configuration.md"><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></a>
<div align="center"><a href="../web/web-configuration.md"><strong>Web</strong></a></div></td>
<td><a href="../code-based/code-based-configuration.md"><img alt="Code-basiertes Erlebnis" src="../channels/assets/do-not-localize/code.png"></a>
<div align="center"><a href="../code-based/code-based-configuration.md"><strong>Code-basiertes Erlebnis</strong></a></div></td>
<td><a href="../content-card/content-card-configuration-prereq.md"><img alt="Inhaltskarten" src="../channels/assets/do-not-localize/cards.png"></a>
<div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>Inhaltskarten</strong></a></div></td>
</tr></table>

>[!NOTE]
>
>Bei mobilen Kanälen erleichtert die [Einrichtung von ](set-mobile-config.md)) die schnelle Konfiguration von Marketing-Kanälen, sodass alle erforderlichen Ressourcen sofort in Experience Platform, Journey Optimizer und der Datenerfassung verfügbar sind. Dadurch kann Ihr Marketing-Team sofort mit der Erstellung von Kampagnen und Journeys beginnen.

1. Anschließend müssen Sie **Kanalkonfigurationen** erstellen, um alle technischen Parameter zu konfigurieren, die für den Nachrichtenversand erforderlich sind. [Erfahren Sie mehr über Kanalkonfigurationen](channel-surfaces.md)

1. Alternativ können Sie auch folgendermaßen vorgehen:

   * Verwalten Sie die Anzahl der Tage, in denen weitere Zustellversuche unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](manage-suppression-list.md)

   * Aktivieren Sie die **BBC-E-Mail-Option**, um eine Kopie der an Einzelpersonen gesendeten Nachrichten aufzubewahren. [Weitere Informationen](archiving-support.md#enable-bcc)

   * Konfigurieren Sie **Geschäftsregeln**, um zu vermeiden, dass Ihre Empfängerinnen und Empfänger übermäßig viele Nachrichten erhalten. [Weitere Informationen](../configuration/rule-sets.md)

   * Bestimmen Sie, welche E-Mail-Adresse und/oder Telefonnummer für Ihre Empfänger vorrangig verwendet werden soll, wenn in Adobe Experience Platform mehrere Adressen/Nummern verfügbar sind. [Weitere Informationen](primary-email-addresses.md)
