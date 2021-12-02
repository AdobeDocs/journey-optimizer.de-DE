---
title: Profilbegrenzung
description: Profilbegrenzung
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 1%

---


# Reputation als Absender etablieren

Wenn Sie kürzlich zu einem anderen E-Mail-Dienstleister, einer IP-Adresse, einer E-Mail-Domain oder einer Subdomäne gewechselt haben, müssen Sie Ihre Reputation als Absender nachweisen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden.

Um Ihre IP-Adresse aufzuwärmen, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Siehe dies [Anwendungsfall](../building-journeys/ramp-up-deliveries-uc.md).

## Bedingungstyp für Profilbegrenzung {#profile_cap}

Weitere Bedingungstypen werden in diesem Abschnitt beschrieben. [Abschnitt](../building-journeys/condition-activity.md).

Verwenden Sie diesen Bedingungstyp, um eine Höchstzahl von Profilen für einen Journey-Pfad festzulegen. Wenn diese Grenze erreicht ist, nehmen die Eingabeprofile einen alternativen Pfad an.

Mit diesem Bedingungstyp können Sie das Volumen Ihrer Sendungen erhöhen. Siehe dies [Anwendungsfall](../building-journeys/ramp-up-deliveries-uc.md).

Die Standardbegrenzung ist 1000. Sie können einen ganzzahligen Wert von 1 bis 20.000 festlegen.

Der Zähler gilt nur für die ausgewählte Journey-Version. Der Zähler wird nach einem Monat auf null zurückgesetzt. Nach dem Zurücksetzen nehmen die Eingabeprofile den nominalen Pfad erneut, bis die Zählergrenze erreicht ist.

Der nominale Pfad hat immer Vorrang vor dem alternativen Pfad, auch wenn Sie den alternativen Pfad über den nominalen Pfad auf der Journey-Arbeitsfläche verschieben.

![](../assets/profile-cap-condition.png)

## Anwendungsfall: Sendungen vorantreiben

Wenn Sie kürzlich zu einem anderen E-Mail-Dienstleister, einer IP-Adresse, einer E-Mail-Domain oder einer Subdomäne gewechselt haben, müssen Sie Ihre Reputation als Absender nachweisen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden. Erfahren Sie, wie Sie Ihre E-Mail-Reputation mit IP-Warming im [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Um Ihre IP-Adresse aufzuwärmen, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Mehr dazu [Zustellbarkeit in Journey Optimizer optimieren](../deliverability.md).

In diesem Anwendungsbeispiel wird eine Journey erstellt, um den E-Mail-Versand zu beschleunigen. Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen einer Journey. [Mehr dazu](../building-journeys/journey-gs.md).

1. Hinzufügen einer **[!UICONTROL Bedingung]** -Aktivität auf die Journey. [Mehr dazu](../building-journeys/condition-activity.md).

1. Im **[!UICONTROL Bedingung]** in den Aktivitätseinstellungen die maximale Empfängeranzahl für Ihren Versand festlegen:

   1. Im **[!UICONTROL Bedingung]** Aktivitätseinstellungen festlegen, legen Sie die **[!UICONTROL Typ]** -Feld zu **[!UICONTROL Profilbegrenzung]**. [Mehr dazu](profile-cap.md#profile_cap).

   1. Legen Sie die **[!UICONTROL Limit]** zur maximalen Anzahl an Empfängern für diesen Versand.

   ![](../assets/profile-cap-condition.png)

   Sie können diese Begrenzung schrittweise auf die Gesamtzahl Ihrer Abonnenten erhöhen.

1. Hinzufügen einer **[!UICONTROL Nachricht]** Aktivität zum nominalen Pfad nach **[!UICONTROL Bedingung]** Aktivität.

   ![](../assets/ramp-up-deliveries-message.png)

   Wenn die Journey ausgeführt wird, wird die Nachricht an die Eingabeprofile gesendet, bis zu der von Ihnen angegebenen Höchstzahl an Profilen. Wenn diese Grenze erreicht ist, nehmen die Eingabeprofile den alternativen Pfad an.

1. Füllen Sie die Journey mit den Aktivitäten Ihrer Wahl aus.

Nachdem sich Ihre IP erwärmt hat, können Sie diese Bedingung entfernen.

