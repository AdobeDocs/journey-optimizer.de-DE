---
title: Posteingang erstellen
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer einen Posteingang erstellen und konfigurieren, um persistente, nicht aufdringliche Nachrichten an Ihre Benutzerinnen und Benutzer zu senden.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 44%

---

# Erstellen eines Posteingangs {#inbox-create}

Bevor Sie einen Posteingang erstellen, führen Sie die Schritte unter [Konfiguration des Posteingangs](inbox-configuration.md) aus. Die Kanalkonfiguration identifiziert die Zielanwendung oder -website, die Seite oder Regel und die Platzierung, an der der Posteingang gerendert wird.

Gehen Sie wie folgt vor, um über eine Kampagne einen Nachrichten-Posteingang zu erstellen:

1. Erstellen einer Kampagne. [Weitere Informationen](../campaigns/create-campaign.md)

1. Wählen Sie den Kampagnentyp aus, den Sie ausführen möchten:

   * **[!UICONTROL Geplant – Marketing]**: die Kampagne wird sofort oder an einem bestimmten Datum ausgeführt. Geplante Kampagnen dienen dem Versand von Nachrichten des Typs **Marketing**. Sie werden über die Benutzeroberfläche konfiguriert und ausgeführt.

   * **[!UICONTROL API-ausgelöst – Marketing/Transaktion]**: die Kampagne wird mithilfe eines API-Aufrufs ausgeführt.  API-ausgelöste Kampagnen zielen auf den Versand von Nachrichten des Typs **Marketing** oder **Transaktion** ab. Beim Typ „Transaktion“ handelt es sich um Nachrichten, die nach einer von einem Kontakt durchgeführten Aktion verschickt werden: Zurücksetzen des Passworts, Verlassen des Warenkorbs usw. [Erfahren Sie, wie Sie eine Kampagne mithilfe von APIs auslösen](../campaigns/api-triggered-campaigns.md)

1. Geben **[!UICONTROL auf der Registerkarte]** Eigenschaften“ einen Namen und eine Beschreibung für die Kampagne an.

1. Wählen Sie auf **[!UICONTROL Registerkarte]** die Aktion **[!UICONTROL Posteingang]** aus.

   ![](assets/inbox-create-1.png)

1. Wählen oder erstellen Sie eine neue [Posteingangskonfiguration](inbox-configuration.md).

   ![](assets/inbox-create-2.png)

1. Greifen Sie auf die Registerkarte Inhalt zu, um Ihre Nachricht mit dem Content Designer zu entwerfen. [Weitere Informationen](inbox-design.md)

1. Klicken Sie auf der **[!UICONTROL Zielgruppe]** auf die Schaltfläche **[!UICONTROL Zielgruppe auswählen]**, um die Liste der verfügbaren Adobe Experience Platform-Zielgruppen anzuzeigen. [Weitere Informationen zu Zielgruppen](../audience/about-audiences.md)

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll. [Weitere Informationen zu Namespaces](../event/about-creating.md#select-the-namespace)

1. Sie können Ihre Kampagne auf ein bestimmtes Datum festlegen oder so einstellen, dass sie in regelmäßigen Abständen wiederholt werden. [Weitere Informationen](../campaigns/create-campaign.md#schedule)

1. Überprüfen und aktivieren Sie Ihre Kampagne, um Nachrichten an den Posteingang zu senden.

Sie können diesen Posteingang jetzt beim Erstellen Ihrer [Inhaltskarten-Kampagne](../content-card/create-content-card.md) auswählen.
