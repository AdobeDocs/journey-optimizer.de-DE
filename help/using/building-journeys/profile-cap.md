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
workflow-type: ht
source-wordcount: '454'
ht-degree: 100%

---


# Reputation als Absender etablieren

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Siehe diesen [Anwendungsfall](../building-journeys/ramp-up-deliveries-uc.md).

## Bedingungstyp „Profilbegrenzung“ {#profile_cap}

Weitere Bedingungstypen werden in diesem [Abschnitt](../building-journeys/condition-activity.md)beschrieben.

Verwenden Sie diesen Bedingungstyp, um eine Höchstzahl von Profilen für einen Journey-Pfad festzulegen. Wenn diese Grenze erreicht ist, folgen die eintretenden Profile einem alternativen Pfad.

Mit diesem Bedingungstyp kann das Volumen Ihrer Sendungen erhöht werden. Siehe diesen [Anwendungsfall](../building-journeys/ramp-up-deliveries-uc.md).

Die Standardbegrenzung ist 1.000. Sie können einen ganzzahligen Wert von 1 bis 20.000 festlegen.

Der Zähler gilt nur für die ausgewählte Journey-Version. Der Zähler wird nach einem Monat auf null zurückgesetzt. Nach dem Zurücksetzen folgen die eintretenden Profile erneut dem nominalen Pfad, bis die Zählergrenze erreicht ist.

Der nominale Pfad hat immer Vorrang vor dem alternativen Pfad, auch wenn der alternativen Pfad über den nominalen Pfad auf der Journey-Arbeitsfläche verschoben wird.

![](../assets/profile-cap-condition.png)

## Anwendungsfall: Steigern der Versandaktivität

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden. Im [Handbuch zu Best Practices zur Zustellbarkeit ](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de){ target=&quot;_blank&quot;} erfahren Sie, wie die Mail-Reputation mit IP-Warming verbessern können.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Mehr dazu erfahren Sie unter [Zustellbarkeit in Journey Optimizer optimieren](../deliverability.md).

In diesem Anwendungsbeispiel wird eine Journey erstellt, um die Versandaktivität Ihrer E-Mails zu steigern. Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen Sie eine Journey. [Weitere Informationen](../building-journeys/journey-gs.md).

1. Fügen Sie zur Journey die Aktivität **[!UICONTROL Bedingung]** hinzu. [Weitere Informationen](../building-journeys/condition-activity.md).

1. Legen Sie in den Einstellungen für die Aktivität **[!UICONTROL Bedingung]** die maximale Empfängeranzahl für Ihren Versand fest:

   1. Wählen Sie in den Einstellungen für die Aktivität **[!UICONTROL Bedingung]** für das Feld **[!UICONTROL Typ]** die Option **[!UICONTROL Profilbegrenzung]** aus. [Weitere Informationen](profile-cap.md#profile_cap).

   1. Legen Sie das Feld **[!UICONTROL Limit]** auf die maximale Anzahl an Empfängern für diesen Versand fest.

   ![](../assets/profile-cap-condition.png)

   Sie können dieses Limit schrittweise auf die Gesamtzahl Ihrer Abonnenten erhöhen.

1. Fügen Sie im nominalen Pfad nach der Aktivität **[!UICONTROL Bedingung]** die Aktivität **[!UICONTROL Nachricht]** hinzu.

   ![](../assets/ramp-up-deliveries-message.png)

   Wenn die Journey ausgeführt wird, wird die Nachricht bis zu der von Ihnen angegebenen Höchstzahl an Profilen an die eingehenden Profile gesendet. Wenn dieses Limit erreicht ist, nehmen die eingehenden Profile den alternativen Pfad.

1. Vervollständigen Sie die Journey mit den Aktivitäten Ihrer Wahl.

Nach dem Aufwärmen Ihrer IP können Sie diese Bedingung entfernen.

