---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte bei der [!DNL Journey Optimizer] Kanalkonfiguration
description: 'Erfahren Sie mehr über die Kanalkonfiguration mit [!DNL Journey Optimizer] '
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: Konfiguration, Konfigurieren, Nachrichten, Kanal, Sandbox, Optimizer
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: ht
source-wordcount: '397'
ht-degree: 100%

---


# Erste Schritte bei der Kanalkonfiguration {#start-optimizer-configuration}

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="Ratensteuerung für Kanäle"
>abstract="Ratensteuerung für Kanäle"

Beim erstmaligen Zugriff auf [!DNL Journey Optimizer] wird Ihnen eine Produktions-Sandbox bereitgestellt und je nach Vertrag eine bestimmte Anzahl von IPs zugewiesen.

Um Nachrichten zu versenden, müssen Sie die folgenden Konfigurationsschritte durchlaufen:

1. [Adobe Journey Optimizer-Systemadministrierende](../start/path/administrator.md) können kanalspezifische Konfigurationen definieren. Auf den folgenden Seiten erfahren Sie, wie Sie diese Konfigurationen einrichten:

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="E-Mail" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>E-Mail</strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
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
   >Bei Mobile-Kanälen erleichtert die [geführte Kanaleinrichtung](set-mobile-config.md) die schnelle Konfiguration von Marketing-Kanälen, sodass alle erforderlichen Ressourcen in Experience Platform, Journey Optimizer und der Datenerfassung sofort verfügbar sind. Dadurch kann Ihr Marketing-Team sofort mit der Erstellung von Kampagnen und Journeys beginnen.

1. Anschließend müssen Sie alle technischen Parameter konfigurieren, die zum Versand von Nachrichten erforderlich sind, indem Sie **Kanalkonfigurationen** erstellen. [Weitere Informationen zu Kanalkonfigurationen](channel-surfaces.md)

1. Je nach den verwendeten Kanälen, Umgebungen und Anforderungen müssen auch die folgenden Schritte ausgeführt werden:

   * Nehmen sie Subdomain-Konfiguration und -Delegierung für Kanäle wie [E-Mails](about-subdomain-delegation.md), [SMS](../sms/sms-subdomains.md), [Landingpages](../landing-pages/lp-subdomains.md) und [Web-Erlebnisse](../web/web-delegated-subdomains.md) vor.

   * Richten Sie IP-Aufwärmplänen für eine optimale Zustellbarkeit ein. [Weitere Informationen](ip-warmup-gs.md)

   * Definieren Sie eine Zulassungsliste für den E-Mail-Versand. [Weitere Informationen](allow-list.md)

   * Verwalten Sie die Anzahl der Tage, in denen weitere Zustellversuche unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](manage-suppression-list.md)

   * Aktivieren Sie die **BBC-E-Mail-Option**, um eine Kopie der an Kontakte gesendeten Nachrichten aufzubewahren. [Weitere Informationen](archiving-support.md#enable-bcc)

   * Konfigurieren Sie **Geschäftsregeln**, um zu vermeiden, dass Ihre Empfängerinnen und Empfänger übermäßig viele Nachrichten erhalten. [Weitere Informationen](../conflict-prioritization/rule-sets.md)

   * Bestimmen Sie, welche E-Mail-Adresse und/oder Telefonnummer für Ihre Empfänger vorrangig verwendet werden soll, wenn in Adobe Experience Platform mehrere Adressen/Nummern verfügbar sind. [Weitere Informationen](primary-email-addresses.md)

## Weitere Ressourcen

* **[Konfigurieren von Kanaloberflächen](channel-surfaces.md)**: Erfahren Sie, wie Sie Kanaloberflächen für E-Mail, Push, SMS und andere Kanäle einrichten und verwalten.
* **[Subdomain-Delegierung](delegate-subdomain.md)**: Erfahren Sie, wie Sie Subdomains für E-Mail-Zustellbarkeit und Branding an Adobe delegieren.
* **[IP-Aufwärmen](ip-warmup-gs.md)**: Entdecken Sie Best Practices für das Aufwärmen von IP-Adressen, um die E-Mail-Zustellbarkeit und den Ruf der absendenden Partei zu verbessern.
* **[Verwalten der Unterdrückungsliste](manage-suppression-list.md)**: Erfahren Sie, wie Sie Unterdrückungslisten verwalten, um mit Bounces umzugehen und die Listenhygiene zu gewährleisten.
* **[Konfigurieren von Apps](set-mobile-config.md)**: Richten Sie App-Konfigurationen für Push-Benachrichtigungen und In-App-Messaging ein.
* **[Tutorials zu Konfigurationen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/configure-channels){target="_blank"}**: Sehen Sie sich detaillierte Video-Tutorials zur Kanalkonfiguration und Best Practices an.
