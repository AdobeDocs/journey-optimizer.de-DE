---
title: Erstellen von Simulationen
description: Erfahren Sie, wie Sie Simulationen erstellen
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: 899b8b47d6c6121c19e485376de368358049c05f
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 7%

---


# Erstellen von Simulationen

## Über die Simulation

Zur Validierung Ihrer Entscheidungslogik können Sie simulieren, welche Angebote für eine bestimmte Platzierung an ein Testprofil gesendet werden.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Dadurch können Sie verschiedene Versionen Ihrer Angebote testen und verfeinern, ohne dass dies Auswirkungen auf die Zielgruppenempfänger hat.

>[!NOTE]
>
>Diese Funktion simuliert eine einzelne Anforderung an die [!DNL Decisions] API. Weitere Informationen finden Sie unter [Angebote mithilfe der Decisions-API unterbreiten](../api-reference/decisions-api/deliver-offers.md).

Um auf diese Funktion zuzugreifen, wählen Sie die **[!UICONTROL Simulation]** Registerkarte aus **[!UICONTROL Entscheidungsmanagement]** > **[!UICONTROL Angebote]** Menü.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Auswählen der Testprofile

Zunächst müssen Sie die Testprofile auswählen, die Sie für die Simulation verwenden möchten.

1. Klicken **[!UICONTROL Profil verwalten]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Wählen Sie den Identitäts-Namespace aus, den Sie zur Identifizierung von Testprofilen verwenden möchten. In diesem Beispiel verwenden wir den Namespace **E-Mail.**

   >[!NOTE]
   >
   >Ein Identitäts-Namespace definiert den Kontext einer Kennung wie eine E-Mail-Adresse oder eine CRM-ID. Weitere Informationen zu Identity-Namespaces von Adobe Experience Platform finden Sie [in diesem Abschnitt](../../get-started-identity.md){target=&quot;_blank&quot;}.

1. Geben Sie den Identitätswert ein und klicken Sie auf **[!UICONTROL Ansicht]** , um die verfügbaren Profile aufzulisten.

   ![](../../assets/offers_simulation-add-profile.png)

1. Fügen Sie weitere Profile hinzu, wenn Sie verschiedene Profildaten testen möchten, und speichern Sie Ihre Auswahl.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Nach dem Hinzufügen werden alle Profile in der Dropdown-Liste unter **[!UICONTROL Testprofil]**. Sie können zwischen den gespeicherten Testprofilen wechseln, um die Ergebnisse für jedes ausgewählte Profil anzuzeigen.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. Sie können auf die **[!UICONTROL Profildetails]** -Link, um die ausgewählten Profildaten anzuzeigen.

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## Entscheidungsbereiche hinzufügen

Wählen Sie nun die Angebotsentscheidungen aus, die Sie für Ihre Testprofile simulieren möchten.

1. Auswählen **[!UICONTROL Entscheidungsbereich hinzufügen]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Wählen Sie eine Platzierung aus der Liste aus.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. Die verfügbaren Entscheidungen werden angezeigt.

   * Sie können das Suchfeld verwenden, um die Auswahl zu verfeinern.
   * Sie können auf die **[!UICONTROL Entscheidungsfindung bei Angeboten]** -Link, um die Liste aller von Ihnen erstellten Entscheidungen zu öffnen. Weitere Informationen finden Sie unter [Entscheidungen](create-offer-activities.md).

   Wählen Sie die Entscheidung Ihrer Wahl aus und klicken Sie auf **[!UICONTROL Hinzufügen]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. Der soeben definierte Entscheidungsbereich wird im Hauptarbeitsbereich angezeigt.

   Sie können die Anzahl der Angebote anpassen, die Sie anfordern möchten. Wenn Sie beispielsweise 2 auswählen, werden für diesen Entscheidungsbereich die besten 2 Angebote angezeigt.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Sie können bis zu 30 Angebote anfordern.

1. Wiederholen Sie die obigen Schritte, um so viele Entscheidungen wie nötig hinzuzufügen.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Selbst wenn Sie mehrere Entscheidungsbereiche definieren, wird nur eine API-Anfrage simuliert.
   >
   >Alle Deduplizierungs-Flags sind standardmäßig für die Simulation aktiviert, d. h. die Entscheidungs-Engine ermöglicht Duplikate und kann somit über mehrere Entscheidungen hinweg denselben Vorschlag unterbreiten. Weitere Informationen finden Sie unter [!DNL Decisions] Eigenschaften von API-Anfragen in [diesem Abschnitt](../api-reference/decisions-api/deliver-offers.md).

## Anzeigen von Simulationsergebnissen

Nachdem Sie einen Entscheidungsbereich hinzugefügt und ein Testprofil ausgewählt haben, können Sie die Ergebnisse anzeigen.

1. Klicken **[!UICONTROL Ergebnisse anzeigen]**.

   ![](../../assets/offers_simulation-view-results.png)

1. Die besten verfügbaren Angebote werden entsprechend dem ausgewählten Profil für jede Entscheidung angezeigt.

   Wählen Sie ein Angebot aus, um dessen Details anzuzeigen.

   ![](../../assets/offers_simulation-offer-details.png)

1. Wählen Sie ein anderes Profil aus der Liste aus, um die Ergebnisse der Angebotsentscheidungen für ein anderes Testprofil anzuzeigen.

1. Sie können die Entscheidungsbereiche beliebig oft hinzufügen, entfernen oder aktualisieren.

>[!NOTE]
>
>Jedes Mal, wenn Sie Profile ändern oder Entscheidungsbereiche aktualisieren, müssen Sie die Ergebnisse mit dem **[!UICONTROL Ergebnisse anzeigen]** Schaltfläche.

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->