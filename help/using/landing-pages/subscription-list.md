---
title: Abonnementliste erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer eine Abonnementliste einrichten.
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 1%

---

# Abonnementliste erstellen {#create-subscription-list}

## Was ist eine Abonnementliste?

Ein Anmeldedienst bezieht sich auf Marketing-Waren und -Dienstleistungen, die Kunden angeboten werden, die sich für den Erhalt von Mitteilungen zu einem bestimmten Thema/Ereignis/Interesse usw. entschieden haben. fortlaufend. In [!DNL Journey Optimizer], werden diese angemeldeten Kunden in einer Abonnementliste erfasst.

Ein Anmeldedienst kann:

* einen Newsletter, z. B. &quot;Laufende Serie&quot;
* Veranstaltung, z. B. &quot;Summit 2021&quot;
* ein Webinar, z. B. &quot;Weitere Informationen über Kryptographie&quot;
* ein Interesse an einem bestimmten Produkt/Sport/Service/etc., z. B. &quot;Interesse an einem Haus in den nächsten 12 Monaten&quot;
* eine Präferenz für die Benachrichtigung, z. B. &quot;Empfangen neuer Song-Benachrichtigungen per E-Mail&quot;

Die Profile können über eine [Landingpage](create-lp.md). Ein Beispiel finden Sie unter [diesem Abschnitt](get-started-lp.md#subscription-to-a-service).

## Abonnementliste definieren {#define-subscription-list}

Gehen Sie wie folgt vor, um eine Abonnementliste zu erstellen.

1. Um auf die Abonnementlisten zuzugreifen, wählen Sie **[!UICONTROL Kunde]** > **[!UICONTROL Abonnementliste]**.

   ![](../assets/lp_subscription-lists.png)

1. Klicken Sie in der Abonnementliste auf **[!UICONTROL Abonnement erstellen]** Liste.

   ![](../assets/lp_create-subscription-list.png)

1. Fügen Sie einen Namen und eine Beschreibung hinzu. Diese Felder sind Pflichtfelder.

1. Sie können ein Start- und ein Enddatum definieren.

   ![](../assets/lp_subscription-list-dates.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

In der Liste werden alle erstellten Abonnementlisten angezeigt. Sie können sie nach dem Erstellungsdatum oder Änderungsdatum filtern.

![](../assets/lp_subscription-filters.png)

Folgende Status sind möglich:

* **[!UICONTROL Nicht gestartet]**: Sie haben ein Startdatum definiert, das nach dem aktuellen Tag liegt. Die Profile, die diese Liste abonniert haben, erhalten noch keine Mitteilungen zu dieser Abonnementliste.
* **[!UICONTROL Live]**: Der aktuelle Tag besteht zwischen dem Start- und dem Enddatum der Abonnementliste oder Sie haben kein Enddatum/Startdatum definiert, was bedeutet, dass die Abonnementliste immer live ist.
* **[!UICONTROL Abgelaufen]**: Das Enddatum wird übergeben, die Abonnementliste ist nicht mehr gültig. Alle Profile, die diese Liste abonniert haben, erhalten keine weiteren Mitteilungen zu dieser Abonnementliste.

Nachdem die Abonnementliste erstellt wurde, können Sie sie auf einer Landingpage verwenden, damit sich die Profile über ein Formular anmelden und der Liste hinzugefügt werden können. [Weitere Informationen](design-lp.md)

Sie können Abonnementlisten auch beim Erstellen von Journey und Personalisierung als Segmente verwenden.

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->