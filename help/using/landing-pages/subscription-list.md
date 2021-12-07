---
title: Abonnementliste erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer eine Abonnementliste einrichten.
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# Abonnementlisten {#create-subscription-list}

## Was ist eine Abonnementliste?

Ein Anmeldedienst bezieht sich auf Marketing-Waren und -Dienstleistungen, die Kunden angeboten werden, die sich für den Erhalt von Mitteilungen zu einem bestimmten Thema/Ereignis/Interesse usw. entschieden haben. fortlaufend. In [!DNL Journey Optimizer], werden diese angemeldeten Kunden in einer Abonnementliste erfasst.

Ein Anmeldedienst kann:

* einen Newsletter, z. B.: &quot;Laufende Serie&quot;
* ein Ereignis, z. B.: &quot;Gipfel 2021&quot;
* ein Webinar, z. B.: &quot;Erfahren Sie mehr über &quot;crypto&quot;
* Interesse an einem bestimmten Produkt/Sport/Service usw., z. B.: &quot;Interesse daran, in den nächsten 12 Monaten ein Haus zu kaufen&quot;
* eine Präferenz für die Benachrichtigung, z. B.: &quot;Empfangen neuer Song-Benachrichtigungen per E-Mail&quot;

Die Profile können über eine [Landingpage](create-lp.md). Ein Beispiel finden Sie unter [diesem Abschnitt](lp-use-cases.md#subscription-to-a-service).

## Abonnementliste definieren {#define-subscription-list}

Gehen Sie wie folgt vor, um eine Abonnementliste zu erstellen.

1. Um auf die Abonnementlisten zuzugreifen, wählen Sie **[!UICONTROL Kunde]** > **[!UICONTROL Abonnementliste]**.

   ![](../assets/lp_subscription-lists.png)

1. Wählen Sie die **[!UICONTROL Abonnementliste erstellen]** Schaltfläche.

   ![](../assets/lp_create-subscription-list.png)

1. Fügen Sie einen Namen und eine Beschreibung hinzu. Diese Felder sind Pflichtfelder.

1. Sie können ein Start- und ein Enddatum definieren.

   ![](../assets/lp_subscription-list-dates.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

In der Liste werden alle erstellten Abonnementlisten angezeigt. Sie können sie nach dem Erstellungsdatum oder Änderungsdatum und ihrem Status filtern.

![](../assets/lp_subscription-filters.png)

Folgende Status sind möglich:

* **[!UICONTROL Nicht gestartet]**: Sie haben ein Startdatum definiert, das nach dem aktuellen Tag liegt. Die abonnierten Profile erhalten noch keine Nachrichten zu dieser Abonnementliste.
* **[!UICONTROL Live]**: Der aktuelle Tag besteht zwischen dem Start- und dem Enddatum der Abonnementliste oder Sie haben kein Enddatum/Startdatum definiert, was bedeutet, dass die Abonnementliste immer live ist.
* **[!UICONTROL Abgelaufen]**: Das Enddatum wird übergeben, sodass die Abonnementliste nicht mehr gültig ist. An abonnierte Profile werden keine weiteren Mitteilungen zu dieser Abonnementliste gesendet.

Nachdem die Abonnementliste erstellt wurde, können Sie sie in einer Landingpage verwenden. Die Profile, die sich über das Landingpage-Formular anmelden, werden der Liste hinzugefügt. [Weitere Informationen](design-lp.md)

Sie können Abonnementlisten auch als Segmente verwenden, wenn Sie [Journey bauen](../building-journeys/journey-gs.md#jo-build) und Personalisierung hinzufügen.

>[!NOTE]
>
>Sie können die Auswirkungen Ihrer Abonnementliste über spezifische Berichte überwachen. [Weitere Informationen](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
