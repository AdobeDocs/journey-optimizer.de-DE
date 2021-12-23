---
title: Steigern Sie Ihre Versandaktivität
description: Hier erfahren Sie, wie Sie Ihre Versandaktivität steigern können.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 980aedcd0fb4dba161dc0041a77e0f8d06d6fe68
workflow-type: ht
source-wordcount: '266'
ht-degree: 100%

---


# Anwendungsfall: Steigern der Versandaktivität

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden. Im [Handbuch für Best Practices der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de){target=&quot;_blank&quot;} erfahren Sie, wie Sie Ihre E-Mail-Reputation mit IP-Warming verbessern können.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Erfahren Sie mehr zum [Optimieren der Zustellbarkeit in Journey Optimizer](../deliverability.md).

In diesem Anwendungsbeispiel wird eine Journey erstellt, um die Versandaktivität Ihrer E-Mails zu steigern. Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen Sie eine Journey. [Weitere Informationen](journey-gs.md).

1. Fügen Sie zur Journey eine Aktivität vom Typ **[!UICONTROL Bedingung]** hinzu. [Weitere Informationen](condition-activity.md).

1. Legen Sie in den Einstellungen der **[!UICONTROL Bedingung]** die maximale Anzahl an Empfängern für den Versand fest.

   1. Legen Sie in den Einstellungen der **[!UICONTROL Bedingung]** für das Feld **[!UICONTROL Typ]** den Wert **[!UICONTROL Profilbegrenzung]** fest. [Weitere Informationen](condition-activity.md#profile_cap).

   1. Legen Sie im Feld **[!UICONTROL Limit]** die maximale Anzahl an Empfängern für diesen Versand fest.

   ![](../assets/profile-cap-condition.png)

   Sie können dieses Limit schrittweise auf die Gesamtzahl Ihrer Abonnenten erhöhen.

1. Fügen Sie nach der Aktivität vom Typ **[!UICONTROL Bedingung]** zum nominalen Pfad eine Aktivität vom Typ **[!UICONTROL Nachricht]** hinzu.

   ![](../assets/ramp-up-deliveries-message.png)

   Wenn die Journey ausgeführt wird, wird die Nachricht bis zu der von Ihnen angegebenen Höchstzahl an Profilen an die eingehenden Profile gesendet. Wenn dieses Limit erreicht ist, nehmen die eingehenden Profile den alternativen Pfad.

1. Vervollständigen Sie die Journey mit den Aktivitäten Ihrer Wahl.

Nach dem Aufwärmen Ihrer IP können Sie diese Bedingung entfernen.





