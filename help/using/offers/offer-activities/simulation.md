---
title: Erstellen von Simulationen
description: Erfahren Sie, wie Sie simulieren, welche Angebote für eine bestimmte Platzierung bereitgestellt werden, um Ihre Entscheidungslogik zu validieren
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 60ccb9b918284b3fcb62101bc94bf64d2272e8e2
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 64%

---

# Erstellen von Simulationen {#create-simulations}

## Über die Simulation {#about-simulation}

Zur Validierung Ihrer Entscheidungslogik können Sie simulieren, welche Angebote für eine bestimmte Platzierung an ein Testprofil gesendet werden.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Dadurch können Sie verschiedene Versionen Ihrer Angebote testen und anpassen, ohne dass dies Auswirkungen auf die ausgewählten Empfänger hat.

>[!NOTE]
>
>Diese Funktion simuliert eine einzelne Anfrage an die [!DNL Decisions]-API. Weitere Informationen finden Sie unter [Unterbreiten von Angeboten mithilfe der Decisions-API](../api-reference/decisions-api/deliver-offers.md).

Um auf diese Funktion zuzugreifen, wählen Sie die Registerkarte **[!UICONTROL Simulation]** aus dem Menü **[!UICONTROL Entscheidungs-Management]** > **[!UICONTROL Angebote]**.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Auswählen der Testprofile {#select-test-profiles}

Zunächst müssen Sie die Testprofile auswählen, die Sie für die Simulation verwenden möchten.

1. Klicken Sie auf **[!UICONTROL Profil verwalten]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Wählen Sie den Identity-Namespace aus, den Sie zur Identifizierung von Testprofilen verwenden möchten. In diesem Beispiel verwenden wir den Namespace **E-Mail**.

   >[!NOTE]
   >
   >Ein Identity-Namespace definiert den Kontext einer Kennung wie eine E-Mail-Adresse oder eine CRM-ID. Weitere Informationen zu Identity-Namespaces von Adobe Experience Platform finden Sie [in diesem Abschnitt](../../start/get-started-identity.md){target=&quot;_blank&quot;}.

1. Geben Sie den Identitätswert ein und klicken Sie auf **[!UICONTROL Ansicht]**, um die verfügbaren Profile aufzulisten.

   ![](../../assets/offers_simulation-add-profile.png)

1. Fügen Sie weitere Profile hinzu, wenn Sie verschiedene Profildaten testen möchten, und speichern Sie Ihre Auswahl.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Nach dem Hinzufügen werden alle Profile in der Dropdown-Liste unter **[!UICONTROL Testprofil]** aufgelistet. Sie können zwischen den gespeicherten Testprofilen wechseln, um die Ergebnisse für jedes ausgewählte Profil anzuzeigen.

   ![](../../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >Die ausgewählten Profile werden weiterhin als Testprofile im **[!UICONTROL Simulation]** von Sitzung zu Sitzung wechseln, bis sie mithilfe von **[!UICONTROL Profil verwalten]**.

1. Sie können auf den Link **[!UICONTROL Profildetails]** klicken, um die ausgewählten Profildaten anzuzeigen.

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## Hinzufügen von Entscheidungsumfängen {#add-decision-scopes}

Wählen Sie nun die Angebotsentscheidungen aus, die Sie für Ihre Testprofile simulieren möchten.

1. Wählen Sie **[!UICONTROL Entscheidungsumfang hinzufügen]** aus.

   ![](../../assets/offers_simulation-add-decision.png)

1. Wählen Sie eine Platzierung aus der Liste aus.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. Die verfügbaren Entscheidungen werden angezeigt.

   * Sie können das Suchfeld verwenden, um die Auswahl zu verfeinern.
   * Sie können auf den Link **[!UICONTROL Angebotsentscheidungen öffnen]** klicken, um die von Ihnen erstellte Liste aller Entscheidungen zu öffnen. Weitere Informationen finden Sie unter [Entscheidungen](create-offer-activities.md).

   Wählen Sie die gewünschte Entscheidung aus und klicken Sie auf **[!UICONTROL Hinzufügen]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. Der soeben definierte Entscheidungsumfang wird im Hauptarbeitsbereich angezeigt.

   Sie können einstellen, wie viele Angebote angefordert werden sollen. Wenn Sie beispielsweise „2“ auswählen, werden für diesen Entscheidungsumfang die besten zwei Angebote angezeigt.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Sie können bis zu 30 Angebote anfordern.

1. Wiederholen Sie die obigen Schritte, um so viele Entscheidungen wie nötig hinzuzufügen.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Selbst wenn Sie mehrere Entscheidungsumfänge definieren, wird nur eine API-Anfrage simuliert.

## Simulationseinstellungen definieren {#define-simulation-settings}

Gehen Sie wie folgt vor, um die Standardeinstellungen für Ihre Simulationen zu bearbeiten.

1. Klicken **[!UICONTROL Einstellungen]**.

   ![](../../assets/offers_simulation-settings.png)

1. Im **[!UICONTROL Deduplizierung]** können Sie festlegen, dass Angebote für alle Entscheidungen und/oder Platzierungen dupliziert werden. Dies bedeutet, dass mehreren Entscheidungen/Platzierungen möglicherweise dasselbe Angebot zugewiesen wird.

   ![](../../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >Alle Deduplizierungs-Flags sind standardmäßig für die Simulation aktiviert, d. h. das Entscheidungsmodul ermöglicht Duplikate und kann somit denselben Vorschlag für mehrere Entscheidungen/Platzierungen unterbreiten. Weitere Informationen zu den Eigenschaften von [!DNL Decisions]-API-Anfragen finden Sie in [diesem Abschnitt](../api-reference/decisions-api/deliver-offers.md).

1. Im **[!UICONTROL Antwortformat]** -Abschnitt können Sie wählen, ob Metadaten in die Codeansicht aufgenommen werden sollen. Aktivieren Sie die entsprechende Option und wählen Sie die Metadaten Ihrer Wahl aus. Sie werden bei der Auswahl in den Payloads für Anfragen und Antworten angezeigt **[!UICONTROL Code anzeigen]**. Weitere Informationen finden Sie unter [Anzeigen von Simulationsergebnissen](#simulation-results) Abschnitt.

   ![](../../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >Beim Aktivieren der Option werden standardmäßig alle Elemente ausgewählt.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

>[!NOTE]
>
>Für Simulationsdaten können Sie derzeit nur die Variable **[!UICONTROL Hub]** API.

<!--
In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Anzeigen von Simulationsergebnissen {#simulation-results}

Nachdem Sie einen Entscheidungsumfang hinzugefügt und ein Testprofil ausgewählt haben, können Sie die Ergebnisse anzeigen.

1. Klicken Sie auf **[!UICONTROL Ergebnisse anzeigen]**.

   ![](../../assets/offers_simulation-view-results.png)

1. Die besten verfügbaren Angebote werden entsprechend dem ausgewählten Profil für jede Entscheidung angezeigt.

   Wählen Sie ein Angebot aus, um dessen Details anzuzeigen.

   ![](../../assets/offers_simulation-offer-details.png)

1. Klicken **[!UICONTROL Code anzeigen]** , um die Anfrage- und Antwort-Payloads anzuzeigen. [Weitere Informationen](#view-code)

1. Wählen Sie ein anderes Profil aus der Liste aus, um die Ergebnisse der Angebotsentscheidungen für ein anderes Testprofil anzuzeigen.

1. Sie können die Entscheidungsumfänge beliebig oft hinzufügen, entfernen oder aktualisieren.

>[!NOTE]
>
>Jedes Mal, wenn Sie Profile ändern oder Entscheidungsumfänge aktualisieren, müssen Sie die Ergebnisse mit der Schaltfläche **[!UICONTROL Ergebnisse anzeigen]** aktualisieren.

## Code anzeigen {#view-code}

1. Verwenden Sie die **[!UICONTROL Code anzeigen]** -Schaltfläche zum Anzeigen der Anfrage- und Antwort-Payloads.

   ![](../../assets/offers_simulation-view-code.png)

   Die Codeansicht zeigt die Entwicklerinformationen für den aktuellen Benutzer an. Standardmäßig wird die **[!UICONTROL Antwort-Payload]** angezeigt.

   ![](../../assets/offers_simulation-request-payload.png)

1. Klicken **[!UICONTROL Antwort-Payload]** oder **[!UICONTROL Anfrage-Payload]** um zwischen den beiden Registerkarten zu navigieren.

   ![](../../assets/offers_simulation-response-payload.png)

1. So verwenden Sie die Anfrage-Payload außerhalb von [!DNL Journey Optimizer] - zur Fehlerbehebung, z. B. kopieren Sie sie mithilfe der **[!UICONTROL In Zwischenablage kopieren]** oberhalb der Codeansicht.

   ![](../../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >Stellen Sie beim Kopieren der Anfrage- oder Antwort-Payloads in Ihren eigenen Code sicher, dass Sie {USER_TOKEN} und {API_KEY} durch gültige Werte ersetzen. Erfahren Sie, wie Sie diese Werte in der [Adobe Experience Platform-APIs](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=de)Dokumentation zu {target=&quot;_blank&quot;}.

