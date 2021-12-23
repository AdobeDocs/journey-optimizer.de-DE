---
title: Erstellen einer Abonnementliste
description: Erfahren Sie, wie in Journey Optimizer eine Abonnementliste eingerichtet wird.
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: ht
source-wordcount: '363'
ht-degree: 100%

---

# Abonnementlisten {#create-subscription-list}

## Was ist eine Abonnementliste?

Ein Anmeldedienst unterstützt die Vermarktung von Waren und Dienstleistungen, die Kunden angeboten werden, die sich für den laufenden Erhalt von Mitteilungen zu einem bestimmten Thema/Ereignis/Interesse usw. entschieden haben. In [!DNL Journey Optimizer] werden diese angemeldeten Kunden in einer Abonnementliste erfasst.

Ein Anmeldedienst kann sein:

* ein Newsletter, z. B.: „Laufende Serie“
* ein Ereignis, z. B.: „Summit 2021“
* ein Webinar, z. B.: „Mehr über Kryptowährungen erfahren“
* Interesse an einem bestimmten Produkt/Sport/Service usw., z. B.: „Interesse daran, in den nächsten 12 Monaten ein Haus zu kaufen“
* eine Präferenz für die Art der Benachrichtigung, z. B.: „Empfangen neuer Song-Benachrichtigungen per E-Mail“

Die Profile können über eine [Landingpage](create-lp.md) zu einer Abonnementliste hinzugefügt werden. Ein Beispiel dazu finden Sie in [diesem Abschnitt](lp-use-cases.md#subscription-to-a-service).

## Definieren einer Abonnementliste {#define-subscription-list}

Gehen Sie wie folgt vor, um eine Abonnementliste zu erstellen.

1. Um auf die Abonnementlisten zuzugreifen, wählen Sie **[!UICONTROL Kunde]** > **[!UICONTROL Abonnementliste]** aus.

   ![](../assets/lp_subscription-lists.png)

1. Wählen Sie die Schaltfläche **[!UICONTROL Abonnementliste erstellen]** aus.

   ![](../assets/lp_create-subscription-list.png)

1. Geben Sie einen Namen und eine Beschreibung ein. Dies sind Pflichtfelder.

1. Sie können ein Start- und Enddatum definieren.

   ![](../assets/lp_subscription-list-dates.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

In der Liste werden alle erstellten Abonnementlisten angezeigt. Sie können sie nach dem Erstellungs- oder Änderungsdatum und ihrem Status filtern.

![](../assets/lp_subscription-filters.png)

Folgende Status sind möglich:

* **[!UICONTROL Nicht gestartet]**: Sie haben ein Startdatum definiert, das nach dem aktuellen Datum liegt. Die abonnierten Profile erhalten noch keine Nachrichten, die für diese Abonnementliste bestimmt sind.
* **[!UICONTROL Live]**: Das aktuelle Datum liegt zwischen dem Start- und dem Enddatum der Abonnementliste oder Sie haben kein Start-/Enddatum definiert, was bedeutet, dass die Abonnementliste immer live ist.
* **[!UICONTROL Abgelaufen]**: Das Enddatum wurde überschritten, sodass die Abonnementliste nicht mehr gültig ist. Profile mit Abonnements erhalten keine weiteren Mitteilungen mehr, die für diese Abonnementliste bestimmt sind.

Nachdem die Abonnementliste erstellt wurde, kann sie in einer Landingpage verwendet werden. Die Profile, die sich über das Landingpage-Formular anmelden, werden der Liste hinzugefügt. [Weitere Informationen](design-lp.md)

Abonnementlisten können auch als Segmente verwendet werden, wenn [Journeys erstellt werden](../building-journeys/journey-gs.md#jo-build) und Personalisierung hinzugefügt wird.

>[!NOTE]
>
>Die Wirkung von Abonnementlisten kann über spezifische Berichte überwacht werden. [Weitere Informationen](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
