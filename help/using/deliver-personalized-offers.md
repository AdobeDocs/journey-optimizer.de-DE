---
title: hinzufügen personalisierte Angebot
description: Erfahren Sie, wie Sie Ihren Nachrichten personalisierte Angebot hinzufügen
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# hinzufügen personalisierte Angebot {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## Informationen zur Entscheidungsverwaltung {#about-offer-decisioning}

Mit [!DNL Journey Optimizer] können Sie Entscheidungen in E-Mail-Nachrichten (früher als Angebot-Aktivitäten bezeichnet) einfügen, die die Angebot Decision Engine nutzen, um das beste Angebot für Ihre Kunden auszuwählen.

Sie können beispielsweise eine Entscheidung hinzufügen, die in Ihrer E-Mail ein besonderes Angebot mit Rabatten anzeigt, das je nach Treuestufe des Empfängers variiert.

Weitere Informationen zum Erstellen und Verwalten von Angeboten finden Sie in [diesem Abschnitt](offers/get-started/starting-offer-decisioning.md).

## Eine Entscheidung in eine E-Mail {#insert-offers} einfügen

Gehen Sie wie folgt vor, um eine Entscheidung in eine E-Mail-Nachricht einzufügen:

1. Erstellen Sie Ihre E-Mail und öffnen Sie dann den E-Mail-Designer, um den Inhalt zu konfigurieren.

1. hinzufügen einer Inhaltskomponente **[!UICONTROL Inhaltsentscheidung]** (siehe [Inhaltskomponenten verwenden](content-components.md)).

   ![](assets/deliver-offer-component.png)

1. Der Komponente wird eine Registerkarte **[!UICONTROL Angebot Decision]** hinzugefügt. Klicken Sie auf **[!UICONTROL Hinzufügen Personalisierung - Angebot Decision]**, um eine Angebot-Aktivität hinzuzufügen.

   ![](assets/deliver-offer-tab.png)

1. Wählen Sie die Platzierung aus, die den anzuzeigenden Angeboten entspricht.

   Platzierungen sind Container, mit denen Ihre Angebot präsentiert werden. In diesem Beispiel verwenden wir die Platzierung &quot;E-Mail-Top-Bild&quot;. Diese Platzierung wurde in der Angebot-Bibliothek erstellt, um Angebote mit Bildtyp am Anfang von Nachrichten anzuzeigen.

1. Wählen Sie die in der Inhaltskomponente zu verwendende Angebot-Aktivität aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

   >[!NOTE]
   >
   >Beachten Sie, dass nur Entscheidungen, die mit der ausgewählten Platzierung kompatibel sind, in der Liste angezeigt werden. In diesem Beispiel stimmt nur eine Angebot-Aktivität mit der Platzierung &quot;Top-Bild für E-Mail&quot;überein.

   ![](assets/deliver-offer-placement.png)

1. Die Angebot-Aktivität wird nun der Komponente hinzugefügt. Sie können die verschiedenen Angebot, die Teil der Entscheidung sind, mit dem **[!UICONTROL Angebots]**-Abschnitt oder den Pfeilen für Inhaltskomponenten Vorschau werden.

   ![](assets/deliver-offer-preview.png)
