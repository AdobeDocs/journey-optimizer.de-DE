---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer Abonnement-Liste
description: Erfahren Sie, wie in Journey Optimizer eine Abonnement-Liste eingerichtet wird.
feature: Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: Landing, Landingpage, Liste, Abonnement, Service
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: c66fe22f0cf81cf8e14592df1433739735afbe43
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 61%

---

# Abonnement-Listen {#create-subscription-list}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="Einrichten einer Abonnement-Liste"
>abstract="Erstellen Sie eine Abonnement-Liste, um Profile zu erfassen, die sich für den Empfang von Nachrichten zu einem bestimmten Thema oder Ereignis entschieden haben. "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html?lang=de#define-subscription-list" text="Erstellen einer Abonnement-Liste"

Ein Anmeldedienst unterstützt die Vermarktung von Waren und Dienstleistungen, die Kunden angeboten werden, die sich für den laufenden Erhalt von Mitteilungen zu einem bestimmten Thema/Ereignis/Interesse usw. entschieden haben. In [!DNL Journey Optimizer] werden diese angemeldeten Kunden in einer Abonnement-Liste erfasst.

Ein Abonnement-Service kann für Folgendes verwendet werden:

* ein Newsletter, z. B.: „Laufen als Sport“
* ein Ereignis, z. B.: „Summit 2021“
* ein Webinar, z. B.: „Mehr über Kryptowährungen erfahren“
* Interesse an einem bestimmten Produkt/Sport/Service usw., z. B.: „Interesse daran, in den nächsten 12 Monaten ein Haus zu kaufen“
* eine Präferenz für die Art der Benachrichtigung, z. B.: „Empfangen neuer Song-Benachrichtigungen per E-Mail“

Die Profile können über eine [Landingpage](create-lp.md) zu einer Abonnement-Liste hinzugefügt werden. Ein Beispiel dazu finden Sie in [diesem Abschnitt](lp-use-cases.md#subscription-to-a-service).

## Erstellen einer Abonnement-Liste {#define-subscription-list}

Gehen Sie wie folgt vor, um eine Abonnement-Liste zu erstellen.

1. Um auf die Abonnement-Listen zuzugreifen, wählen Sie **[!UICONTROL Kunde]** > **[!UICONTROL Abonnement-Liste]** aus.

   ![](assets/lp_subscription-lists.png)

1. Wählen Sie die Schaltfläche **[!UICONTROL Abonnement-Liste erstellen]** aus.

   ![](assets/lp_create-subscription-list.png)

1. Fügen Sie einen Titel und eine Beschreibung hinzu. Dies sind Pflichtfelder.

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >Derzeit können Sie im Feld **[!UICONTROL Titel]** keine Leerzeichen verwenden oder einen Namen eingeben, der bereits für eine andere Abonnement-Liste existiert.

1. Sie können ein Start- und Enddatum definieren.

   ![](assets/lp_subscription-list-dates.png)

1. Wählen oder erstellen Sie Adobe Experience Platform-Tags aus dem Feld **[!UICONTROL Tags]**, um Ihre Landingpage für eine verbesserte Suche zu kategorisieren. [Weitere Informationen](../start/search-filter-categorize.md#tags)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Abonnement-Liste verwenden {#use-subscription-lists}

Nachdem die Abonnement-Liste erstellt wurde, können Sie:

* Hinzufügen von Profilen zur Abonnement-Liste

  Sie können Personen zur Teilnahme **der Liste einladen** indem Sie sich für einen Newsletter anmelden oder sich für eine Veranstaltung registrieren. Sie können auch **personalisierte Nachrichten senden** an Abonnenten senden.

  Um beispielsweise eine Zielgruppe zur Anmeldung zu einer Veranstaltung einzuladen oder einen Newsletter zu abonnieren, können Sie ihr eine Nachricht mit einem Link zu einer Landingpage senden, auf der sie der Veranstaltung beitreten oder sich abonnieren kann. Profile, die sich über das Landingpage-Formular anmelden, werden der zu diesem Zweck erstellten Abonnement-Liste hinzugefügt.

* Senden von Nachrichten an Abonnenten

  Abonnement-Listen können auch als Zielgruppen verwendet werden, wenn Journey erstellt und Personalisierungen hinzugefügt werden.

  Wenn sich ein Kunde beispielsweise für einen Streaming-Service anmeldet, kann dies den sofortigen Versand einer Begrüßungs-E-Mail-Serie zum Trigger bringen, wodurch der Kunde aufgefordert wird, sich zum ersten Mal bei der App anzumelden und seine Anzeigevoreinstellungen festzulegen.

In diesem Anwendungsfall erfahren Sie, wie Sie [ Abonnement-Liste ](lp-use-cases.md#subscription-to-a-service).


## Durchsuchen von Abonnement-Listen {#browse-subscription-lists}

In der Liste werden alle erstellten Abonnement-Listen angezeigt. Sie können sie nach dem Erstellungs- oder Änderungsdatum und ihrem Status filtern.

![](assets/lp_subscription-filters.png)

Folgende Status sind möglich:

* **[!UICONTROL Nicht gestartet]**: Sie haben ein Startdatum definiert, das nach dem aktuellen Datum liegt. Die angemeldeten Profile erhalten noch keine Nachrichten, die für diese Abonnement-Liste bestimmt sind.
* **[!UICONTROL Live]**: Das aktuelle Datum liegt zwischen dem Start- und dem Enddatum der Abonnement-Liste oder Sie haben kein Start-/Enddatum definiert, was bedeutet, dass die Abonnement-Liste immer live ist.
* **[!UICONTROL Abgelaufen]**: Das Enddatum wurde überschritten, sodass die Abonnement-Liste nicht mehr gültig ist. Profile mit Abonnements erhalten keine weiteren Mitteilungen mehr, die für diese Abonnement-Liste bestimmt sind.


## Abonnement-Listen überwachen {#monitor-subscription-lists}

Sie können die Wirkung Ihrer Abonnement-Liste mithilfe dedizierter Berichte überwachen. Sie können auf zwei Berichtstypen zugreifen:

* Live-Bericht zur Abonnement-Liste

  Live-Berichte, auf die über die Registerkarte „Letzte 24 Std.“ zugegriffen werden kann, zeigen Ereignisse an, die innerhalb der letzten 24 Stunden stattgefunden haben. Der Zeitraum ab dem Auftreten des Ereignisses beträgt mindestens zwei Minuten. [Weitere Informationen](../reports/subscription-report-live.md)

* Abonnement-Liste Alle Zeitberichte, mit Customer Journey Analytics

  Diese Berichte konzentrieren sich auf Ereignisse, die vor mindestens zwei Stunden aufgetreten sind, und decken Ereignisse über einen ausgewählten Zeitraum ab. Der **Abonnementbericht** bietet wichtige Einblicke in die An- und Abmeldungen von Profilen, die mit bestimmten Listen verbunden sind, und hilft Ihnen zu verstehen, wie wirksam verschiedene Abonnementkampagnen und Initiativen sind, um die Interaktion und Konversionen zu fördern. [Weitere Informationen](../reports/subscription-report-global-cja.md)
