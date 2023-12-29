---
solution: Journey Optimizer
product: journey optimizer
title: Steigern der Versandaktivität
description: Hier erfahren Sie, wie Sie Ihre Versandaktivität steigern können.
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: Zustellbarkeit, Journey, Anwendungsfall, E-Mail, Reputation
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 100%

---

# Anwendungsfall: Steigern der Versandaktivität{#use-case-ramp-up-your-deliveries}

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden. Im Handbuch zu [Best Practices bei der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de){target="_blank"} finden sich Informationen dazu, wie die E-Mail-Reputation mit IP-Warming verbessert werden kann.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Mehr dazu erfahren Sie unter [Zustellbarkeit in Journey Optimizer optimieren](../reports/deliverability.md).

In diesem Anwendungsbeispiel wird eine Journey erstellt, um die Versandaktivität Ihrer E-Mails zu steigern. Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen Sie eine Journey. [Weitere Informationen](journey-gs.md).

1. Fügen Sie zur Journey die Aktivität **[!UICONTROL Bedingung]** hinzu. [Weitere Informationen](condition-activity.md).

1. Legen Sie in den Einstellungen für die Aktivität **[!UICONTROL Bedingung]** die maximale Empfängeranzahl für Ihren Versand fest:

   1. Wählen Sie in den Einstellungen für die Aktivität **[!UICONTROL Bedingung]** für das Feld **[!UICONTROL Typ]** die Option **[!UICONTROL Profilbegrenzung]** aus. [Weitere Informationen](condition-activity.md#profile_cap).

   1. Legen Sie das Feld **[!UICONTROL Limit]** auf die maximale Anzahl an Empfängern für diesen Versand fest.

   ![](assets/profile-cap-condition.png)

   Sie können dieses Limit schrittweise auf die Gesamtzahl Ihrer Abonnenten erhöhen.

1. Fügen Sie im nominalen Pfad nach der Aktivität **[!UICONTROL Bedingung]** die Aktionsaktivität **[!UICONTROL E-Mail]** hinzu.

   ![](assets/ramp-up-deliveries-message.png)

   Wenn die Journey ausgeführt wird, wird die Nachricht bis zu der von Ihnen angegebenen Höchstzahl an Profilen an die eingehenden Profile gesendet. Wenn dieses Limit erreicht ist, nehmen die eingehenden Profile den alternativen Pfad.

1. Vervollständigen Sie die Journey mit den Aktivitäten Ihrer Wahl.

Nach dem Aufwärmen Ihrer IP können Sie diese Bedingung entfernen.
