---
title: Administration und Einstellungen
description: Richtlinien zu Administration und Einstellungen
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
translation-type: tm+mt
source-git-commit: 289d73da78f369854c851d7822ea69849c9ebd2d
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 8%

---


# Erste Schritte

Beim erstmaligen Zugriff auf Journey Optimizer erhalten Sie eine Produktions-Sandbox und je nach Vertrag eine bestimmte Anzahl von IPs.

Um Journey erstellen und Nachrichten senden zu können, müssen Sie die folgenden Konfigurationsschritte ausführen:

1. **Subdomänen** delegieren.

   Für jede neue Subdomäne, die in Journey Optimizer verwendet werden soll, besteht der erste Schritt darin, sie zu delegieren. [Mehr dazu](about-subdomain-delegation.md)

2. **Erstellen Sie IP-Pools.**

   Verbessern Sie die Zustellbarkeit und den Ruf Ihrer E-Mail, indem Sie IP-Adressen gruppieren, die mit Ihrer Instanz bereitgestellt wurden. [Mehr dazu](ip-pools.md)

3. **Konfigurieren Sie E-Mail- und Push-Nachrichten**.

   1. Bevor Sie mit dem Senden von Push-Benachrichtigungen mit [!DNL Journey Optimizer] beginnen, müssen Sie die Einstellungen in [!DNL Adobe Experience Platform] und [!DNL Adobe Experience Platform Launch] definieren. [Mehr dazu](../push-configuration.md)

   1. Erstellen Sie Nachrichtenvorgaben, um alle technischen Parameter zu konfigurieren, die für E-Mail- und Push-Benachrichtigungen erforderlich sind. [Mehr dazu](message-presets.md)

   1. Bestimmen Sie, welche E-Mail-Adresse vorrangig für Ihre Empfänger verwendet werden soll, wenn in Adobe Experience Platform mehrere Adressen verfügbar sind. [Mehr dazu](primary-email-addresses.md)

   1. Verwalten Sie die Anzahl der Tage, in denen weitere Zustellversuche ausgeführt werden, bevor Sie E-Mail-Adressen an die Unterdrückungs-Liste senden. [Mehr dazu](get-started-quarantines.md)

1. **Konfigurieren Sie Journey**.

   Um Journey zu erstellen, müssen Sie **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignis]** und **[!UICONTROL Aktionen]** konfigurieren. [Mehr dazu](about-data-sources-events-actions.md)
