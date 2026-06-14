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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 563
ht-degree: 73%

---

# Erste Schritte bei der E-Mail-Konfiguration {#get-starte-email-config}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie mehr über die wichtigsten Schritte zur Konfiguration des E-Mail-Kanals in Adobe Journey Optimizer, von der Zuweisung von Subdomains und der Erstellung von IP-Pools bis zur Einrichtung von Kanalkonfigurationen, Ausführungsfeldern und weiteren Zustellversuchen.

>[!ENDSHADEBOX]

Durch das Konfigurieren des E-Mail-Kanals in Adobe Journey Optimizer können Sie wirkungsvolle, personalisierte E-Mail-Erlebnisse schaffen, die Ihre Zielgruppe effektiv ansprechen.

Dieser Abschnitt führt Sie durch die wichtigsten Konfigurationsschritte, die Sie ausführen müssen, um E-Mails über [!DNL Journey Optimizer] zu senden. Außerdem erfahren Sie, wie Sie E-Mail-Kopfzeilen einrichten, Einstellungen für mehrere Marken personalisieren, das URL-Tracking für Analysen aktivieren und sogar einen Link zur Abmeldung mit einem Klick hinzufügen, um das Abonnieren für den Benutzer zu vereinfachen. Jedes Thema baut auf dem vorherigen auf und gibt Ihnen die Tools an die Hand, mit denen Sie Ihre E-Mail-Strategie optimieren und gleichzeitig die Kontrolle behalten und Präzision sicherstellen können.

Damit während Journeys und Kampagnen E-Mails aus [!DNL Journey Optimizer] versendet werden zu können, müssen Sie eine Reihe von Konfigurationsschritten durchlaufen. Diese Schritte sind unten aufgeführt:

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

1. Schließen Sie die Konfiguration des E-Mail-Kanals ab, indem Sie andere erweiterte Parameter einrichten, z. B. BCC aktivieren, URL-Tracking für Analytics definieren oder Links zum Abmelden mit einem Klick hinzufügen, um den Benutzenden das Arbeiten zu erleichtern. [Weitere Informationen](email-settings.md)

1. Bestimmen Sie, welche **Ausführungsfelder** für Ihre Empfängerinnen und Empfänger vorrangig verwendet werden sollen, wenn in Adobe Experience Platform mehrere Adressen verfügbar sind. [Weitere Informationen](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Verwalten Sie die Anzahl der Tage, in denen **weitere Zustellversuche** unternommen werden, bevor E-Mail-Adressen an die Unterdrückungsliste gesendet werden. [Weitere Informationen](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)


:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=de)

Erste Schritte bei der E-Mail-Konfiguration

Erfahren Sie mehr über die wichtigsten Schritte zur Konfiguration von E-Mail-Funktionen, einschließlich Subdomain-Delegierung, IP-Pools und Verwaltung von Unterdrückungslisten.

[Mit der Konfiguration von E-Mails beginnen](get-started-email-config.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=de)

Definieren von E-Mail-Konfigurationseinstellungen

Richten Sie E-Mail-Konfigurationen für Zustellbarkeit, Compliance und Anpassung mit erweiterten Funktionen wie BCC, Unterdrückungsüberschreibungen und URL-Tracking ein.

[Einstellungen konfigurieren](email-settings.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=de)

Erstellen und Konfigurieren der Listen-Abmeldung

Erfahren Sie, wie Sie die Funktion zur Listen-Abmeldung aktivieren, um für das Opt-out von Empfängerinnen und Empfängern URLs zum Abmelden mit einem Klick in E-Mail-Header einzufügen.

[Listen-Abmeldung einrichten](list-unsubscribe.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=de)

Konfigurieren von Header-Parametern für E-Mails

Passen Sie Absender- und Antwort-E-Mail-Adressen an, behandeln Sie Fehler und leiten Sie E-Mails weiter, um eine effektive Kommunikation zu gewährleisten.

[Header-Parameter einrichten](header-parameters.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=de)

Konfigurieren des URL-Trackings für den E-Mail-Kanal

Richten Sie URL-Tracking-Parameter ein, um die Effektivität von E-Mail-Kampagnen zu messen und sie in Analyse-Tools zu integrieren.

[URL-Tracking einrichten](url-tracking.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=de)

Personalisierte Einstellungen der E-Mail-Konfiguration

Richten Sie dynamische Subdomains, personalisierte Header und URL-Tracking ein, um maßgeschneiderte E-Mail-Erlebnisse zu bieten.

[Personalisierte E-Mails konfigurieren](surface-personalization.md)
:::

::::
