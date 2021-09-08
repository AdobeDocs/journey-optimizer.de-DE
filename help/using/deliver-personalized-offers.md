---
title: Hinzufügen personalisierter Angebote
description: Erfahren Sie, wie Sie Ihren Nachrichten personalisierte Angebote hinzufügen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 100%

---

# Hinzufügen personalisierter Angebote {#deliver-personalized-offers}

Mit [!DNL Journey Optimizer] können Sie in E-Mail-Nachrichten Entscheidungen (früher als „Angebotsaktivitäten“ bezeichnet) einfügen, die das Offer Decisioning-Modul nutzen, um das beste Angebot für Ihre Kunden auszuwählen.

Sie können beispielsweise eine Entscheidung hinzufügen, die in Ihrer E-Mail ein besonderes Angebot mit Rabatten anzeigt, das je nach Treuestufe des Empfängers variiert.

Weiterführende Informationen zur Erstellung und Verwaltung von Angeboten finden Sie in [diesem Abschnitt](offers/get-started/starting-offer-decisioning.md).

Ein **vollständiges Beispiel**, das zeigt, wie Angebote konfiguriert, in Entscheidungen verwendet und diese Entscheidungen in E-Mails eingesetzt werden, finden Sie in [diesem Abschnitt](offers/offers-e2e.md#insert-decision-in-email).

➡️ [In diesem Video erfahren Sie, wie Sie Angebote als Personalisierung hinzufügen können](#video-offers).

## Einfügen einer Entscheidung in eine E-Mail {#insert-offers}

>[!CAUTION]
>
>Bevor Sie beginnen, müssen Sie [eine Angebotsentscheidung definieren](offers/offer-activities/create-offer-activities.md).

Gehen Sie wie folgt vor, um eine Entscheidung in eine E-Mail-Nachricht einzufügen:

1. Erstellen Sie Ihre E-Mail und öffnen Sie dann Email Designer, um den Inhalt zu konfigurieren.

1. Fügen Sie die Inhaltskomponente **[!UICONTROL Angebotsentscheidung]** hinzu.

   ![](assets/deliver-offer-component.png)

   In [diesem Abschnitt](content-components.md) erfahren Sie, wie Sie Inhaltskomponenten verwenden.

1. Die Registerkarte **[!UICONTROL Angebotsentscheidung]** wird in der rechten Palette angezeigt. Klicken Sie auf **[!UICONTROL Angebotsentscheidung auswählen]**.

   ![](assets/deliver-offer-tab.png)

1. Wählen Sie im sich öffnenden Fenster die Platzierung aus, die den anzuzeigenden Angeboten entspricht.

   [Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden. ](offers/offer-library/creating-placements.md) In diesem Beispiel verwenden wir die Platzierung „E-Mail-Top-Bild“. Diese Platzierung wurde in der Angebotsbibliothek erstellt, um Angebote des Typs Bild oben am Anfang von Nachrichten anzuzeigen.

1. Wählen Sie die in der Inhaltskomponente zu verwendende Angebotsaktivität aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   >[!NOTE]
   >
   >Beachten Sie, dass nur Entscheidungen, die mit der ausgewählten Platzierung kompatibel sind, in der Liste angezeigt werden. In diesem Beispiel stimmt nur eine Angebotsaktivität mit der Platzierung „E-Mail-Top-Bild“ überein.

   ![](assets/deliver-offer-placement.png)

Die Angebotsaktivität wird nun der Komponente hinzugefügt.


## Angebotsvorschau in einer E-Mail {#preview-offers-in-email}

Sie können die verschiedenen Angebote, die Teil der Entscheidung sind, in der Vorschau anzeigen, indem Sie den Abschnitt **[!UICONTROL Angebote]** oder die Pfeile für die Inhaltskomponenten verwenden.

![](assets/deliver-offer-preview.png)

Gehen Sie wie folgt vor, um die verschiedenen Angebote anzuzeigen, die Teil der Entscheidung bei einem Kundenprofil sind.

1. Klicken Sie auf **[!UICONTROL Vorschau]**. 

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >Um Ihre Nachrichten in der Vorschau anzuzeigen, benötigen Sie Testprofile. Hier erfahren Sie, wie Sie ein [Testprofil erstellen](building-journeys/creating-test-profiles.md).

1. Um den Namespace auszuwählen, der zur Identifizierung von Testprofilen verwendet werden soll, wählen Sie **[!UICONTROL E-Mail]** im Feld **[!UICONTROL Identity-Namespace]** aus.

   >[!NOTE]
   >
   >In diesem Beispiel verwenden wir den Namespace **E-Mail**. Weitere Informationen zu Identity-Namespaces von Adobe Experience Platform finden Sie [in diesem Abschnitt](get-started-identity.md).

1. Wählen Sie in der Liste der Identity-Namespaces **[!UICONTROL E-Mail]** aus und klicken Sie auf **[!UICONTROL Auswählen]**.

1. Geben Sie im Feld **[!UICONTROL Identitätswert]** den Wert ein, der das Testprofil identifiziert . Geben Sie in diesem Beispiel die E-Mail-Adresse eines Testprofils ein.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. Fügen Sie weitere Profile hinzu, damit Sie je nach den Profildaten verschiedene Varianten der Nachricht testen können.

   ![](assets/deliver-offer-test-profiles.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Vorschau]**, um Ihre Nachricht zu prüfen.

1. Wählen Sie ein Testprofil aus. Das Angebot, das dem ausgewählten Profil (Frau) entspricht, wird angezeigt.

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. Wählen Sie für jede Nachrichtenvariante weitere Testprofile aus, um die Vorschau des E-Mail-Inhalts anzuzeigen. Im Nachrichteninhalt wird nun das Angebot angezeigt, das dem ausgewählten Testprofil (jetzt ein Mann) entspricht.

   ![](assets/deliver-offer-test-profile-male-preview.png)

Weitere Informationen zu den detaillierten Schritten zur Überprüfung der Nachrichtenvorschau finden Sie in [diesem Abschnitt](#preview-your-messages).

## Anleitungsvideo{#video-offers}

Erfahren Sie, wie Sie in [!DNL Journey Optimizer] eine Offer Decisioning-Komponente zu Nachrichten hinzufügen.

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
