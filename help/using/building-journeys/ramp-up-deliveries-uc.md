---
title: Sendungen vorantreiben
description: Hier erfahren Sie, wie Sie Ihre Sendungen vorantreiben.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 980aedcd0fb4dba161dc0041a77e0f8d06d6fe68
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---


# Anwendungsfall: Sendungen vorantreiben

Wenn Sie kürzlich zu einem anderen E-Mail-Dienstleister, einer IP-Adresse, einer E-Mail-Domain oder einer Subdomäne gewechselt haben, müssen Sie Ihre Reputation als Absender nachweisen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden. Erfahren Sie, wie Sie Ihre E-Mail-Reputation mit IP-Warming im [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Um Ihre IP-Adresse aufzuwärmen, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Mehr dazu [Zustellbarkeit in Journey Optimizer optimieren](../deliverability.md).

In diesem Anwendungsbeispiel wird eine Journey erstellt, um den E-Mail-Versand zu beschleunigen. Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen einer Journey. [Mehr dazu](journey-gs.md).

1. Hinzufügen einer **[!UICONTROL Bedingung]** -Aktivität auf die Journey. [Mehr dazu](condition-activity.md).

1. Im **[!UICONTROL Bedingung]** in den Aktivitätseinstellungen die maximale Empfängeranzahl für Ihren Versand festlegen:

   1. Im **[!UICONTROL Bedingung]** Aktivitätseinstellungen festlegen, legen Sie die **[!UICONTROL Typ]** -Feld zu **[!UICONTROL Profilbegrenzung]**. [Mehr dazu](condition-activity.md#profile_cap).

   1. Legen Sie die **[!UICONTROL Limit]** zur maximalen Anzahl an Empfängern für diesen Versand.

   ![](../assets/profile-cap-condition.png)

   Sie können diese Begrenzung schrittweise auf die Gesamtzahl Ihrer Abonnenten erhöhen.

1. Hinzufügen einer **[!UICONTROL Nachricht]** Aktivität zum nominalen Pfad nach **[!UICONTROL Bedingung]** Aktivität.

   ![](../assets/ramp-up-deliveries-message.png)

   Wenn die Journey ausgeführt wird, wird die Nachricht an die Eingabeprofile gesendet, bis zu der von Ihnen angegebenen Höchstzahl an Profilen. Wenn diese Grenze erreicht ist, nehmen die Eingabeprofile den alternativen Pfad an.

1. Füllen Sie die Journey mit den Aktivitäten Ihrer Wahl aus.

Nachdem sich Ihre IP erwärmt hat, können Sie diese Bedingung entfernen.





