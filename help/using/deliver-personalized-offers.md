---
title: Hinzufügen personalisierter Angebote
description: Erfahren Sie, wie Sie Ihren Nachrichten personalisierte Angebote hinzufügen
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '272'
ht-degree: 100%

---

# Hinzufügen personalisierter Angebote {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## Informationen zum Entscheidungs-Management {#about-offer-decisioning}

Mit [!DNL Journey Optimizer] können Sie in E-Mail-Nachrichten Entscheidungen (früher als „Angebotsaktivitäten“ bezeichnet) einfügen, die die Offer Decision Engine nutzen, um das beste Angebot für Ihre Kunden auszuwählen.

Sie können beispielsweise eine Entscheidung hinzufügen, die in Ihrer E-Mail ein besonderes Angebot mit Rabatten anzeigt, das je nach Treuestufe des Empfängers variiert.

Weiterführende Informationen zur Erstellung und Verwaltung von Angeboten finden Sie in [diesem Abschnitt](offers/get-started/starting-offer-decisioning.md).

## Einfügen einer Entscheidung in eine E-Mail {#insert-offers}

Gehen Sie wie folgt vor, um eine Entscheidung in eine E-Mail-Nachricht einzufügen:

1. Erstellen Sie Ihre E-Mail und öffnen Sie dann Email Designer, um den Inhalt zu konfigurieren.

1. Fügen Sie eine Inhaltskomponente **[!UICONTROL Inhaltsentscheidung]** hinzu (siehe [Verwenden von Inhaltskomponenten](content-components.md)).

   ![](assets/deliver-offer-component.png)

1. Der Komponente wird eine Registerkarte **[!UICONTROL Angebotsentscheidung]** hinzugefügt. Klicken Sie auf **[!UICONTROL Personalisierung hinzufügen – Angebotsentscheidung]**, um eine Angebotsaktivität hinzuzufügen.

   ![](assets/deliver-offer-tab.png)

1. Wählen Sie die Platzierung aus, die den Angeboten entspricht, die Sie anzeigen möchten.

   Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden. In diesem Beispiel verwenden wir die Platzierung „E-Mail-Top-Bild“. Diese Platzierung wurde in der Angebotsbibliothek erstellt, um Angebote des Typs Bild oben am Anfang von Nachrichten anzuzeigen.

1. Wählen Sie die in der Inhaltskomponente zu verwendende Angebotsaktivität aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   >[!NOTE]
   >
   >Beachten Sie, dass nur Entscheidungen, die mit der ausgewählten Platzierung kompatibel sind, in der Liste angezeigt werden. In diesem Beispiel stimmt nur eine Angebotsaktivität mit der Platzierung „E-Mail-Top-Bild“ überein.

   ![](assets/deliver-offer-placement.png)

1. Die Angebotsaktivität wird nun der Komponente hinzugefügt. Sie können die verschiedenen Angebote, die Teil der Entscheidung sind, in der Vorschau anzeigen, indem Sie den Abschnitt **[!UICONTROL Angebote]** oder die Pfeile für die Inhaltskomponenten verwenden.

   ![](assets/deliver-offer-preview.png)
