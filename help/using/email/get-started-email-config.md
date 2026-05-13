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
TQID: https://experienceleague.adobe.com/mVdk2WGb0rL06j1cmNEh4fj0JC-hwuro8ku-0Yv02N8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 84%

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

   * Hier wählen Sie die Subdomain aus, die zum Senden der E-Mails verwendet werden soll, sowie die IP-Pools, die mit der Konfiguration verknüpft werden sollen. [Weitere Informationen](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * Die **[!UICONTROL Von E-Mail]** Präfix und **[!UICONTROL Fehler-E-Mail]** Präfix verwenden die aktuell ausgewählte [delegierte Subdomain](../configuration/about-subdomain-delegation.md). Optional können **[!UICONTROL Absendername]** und **[!UICONTROL Absender-E-Mail]** eine andere übertragende Partei identifizieren (vollständige **Absender**-Adresse, nicht an dieses Subdomain-Suffix gebunden). [Weitere Informationen](header-parameters.md#sender-header)

   ![](assets/preset-header.png)

1. Bestimmen Sie, welche **Ausführungsfelder** für Ihre Empfängerinnen und Empfänger vorrangig verwendet werden sollen, wenn in Adobe Experience Platform mehrere Adressen verfügbar sind. [Weitere Informationen](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Verwalten Sie die Anzahl der Tage, in denen **weitere Zustellversuche** unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
