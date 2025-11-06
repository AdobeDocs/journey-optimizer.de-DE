---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte bei der E-Mail-Konfiguration
description: Weitere Informationen zur E-Mail-Konfiguration in  [!DNL Journey Optimizer]
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: E-Mail, Konfiguration, Oberfläche, Subdomains
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: ea8f77c2821bfae7b853b3ac39ea22f0d19ae43d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 100%

---

# Erste Schritte bei der E-Mail-Konfiguration {#get-starte-email-config}

Damit während Journeys und Kampagnen E-Mails aus [!DNL Journey Optimizer] versendet werden zu können, müssen Sie eine Reihe von Konfigurationsschritten durchlaufen.

1. Um eine optimale Zustellbarkeit zu gewährleisten und Ihre Reputation zu schützen, **delegieren Sie zunächst die Subdomains an Adobe**, die Sie für den Versand Ihrer E-Mails mit [!DNL Journey Optimizer] verwenden möchten. Diese Subdomains bestimmen Elemente wie etwa die zu verfolgenden Web-Seiten und die URLs von Mirrorseiten. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Erstellen Sie IP-Pools, um **IP-Adressen zu gruppieren**, die mit Ihrer Instanz bereitgestellt wurden. [Weitere Informationen](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Erstellen Sie **Kanalkonfigurationen** und wählen Sie den Kanal **[!UICONTROL E-Mail]** aus. [Weitere Informationen](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. Konfigurieren Sie in jeder E-Mail-Kanalkonfiguration alle **technischen Parameter**, die für den Versand von E-Mails erforderlich sind. [Weitere Informationen](email-settings.md)

   * Hier wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll, sowie die IP-Pools, die mit der Konfiguration verknüpft werden sollen. [Weitere Informationen](email-settings.md#subdomains-and-ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * Die **[!UICONTROL Absender-E-Mail-Adresse]** und **[!UICONTROL Fehler-E-Mail]**-Adressen müssen die aktuell ausgewählte delegierte Subdomain verwenden. [Weitere Informationen](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Bestimmen Sie, welche **Ausführungsfelder** für Ihre Empfängerinnen und Empfänger vorrangig verwendet werden sollen, wenn in Adobe Experience Platform mehrere Adressen verfügbar sind. [Weitere Informationen](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Verwalten Sie die Anzahl der Tage, in denen **weitere Zustellversuche** unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
