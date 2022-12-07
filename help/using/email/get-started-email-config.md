---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit der E-Mail-Konfiguration
description: Weitere Informationen zur E-Mail-Konfiguration finden Sie in [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 32%

---


# Erste Schritte mit der E-Mail-Konfiguration {#get-starte-email-config}

So können Sie E-Mails über Journey und Kampagnen in senden [!DNL Journey Optimizer]müssen Sie eine Reihe von Konfigurationsschritten durchlaufen.

1. Um eine optimale Zustellbarkeit zu gewährleisten und Ihre Reputation zu schützen, delegieren Sie zunächst an Adobe die Subdomains, mit denen Sie Ihre E-Mails senden möchten [!DNL Journey Optimizer]. Diese Subdomains bestimmen Elemente wie die zu verfolgenden Webseiten und die Mirrorseiten-URLs. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Verbessern Sie die Zustellbarkeit und Reputation Ihrer E-Mail, indem Sie IP-Adressen gruppieren, die mit Ihrer Instanz bereitgestellt wurden. [Weitere Informationen](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Erstellen Sie Kanaloberflächen und wählen Sie die **[!UICONTROL Email]** -Kanal. [Weitere Informationen](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. Konfigurieren Sie auf jeder E-Mail-Kanal-Oberfläche alle technischen Parameter, die für den Versand von E-Mails erforderlich sind. [Weitere Informationen](email-settings.md)

   * Hier wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll, sowie die IP-Pools, die mit der Oberfläche verknüpft werden sollen. [Weitere Informationen](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * Die **[!UICONTROL Absender-E-Mail-Adresse]** und **[!UICONTROL Fehler-E-Mail]**-Adressen müssen die aktuell ausgewählte delegierte Subdomain verwenden. [Weitere Informationen](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Bestimmen Sie, welche E-Mail-Adresse für Ihre Empfänger vorrangig verwendet werden soll, wenn in Adobe Experience Platform mehrere Adressen verfügbar sind. [Weitere Informationen](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Verwalten Sie die Anzahl der Tage, in denen weitere Zustellversuche unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
