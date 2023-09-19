---
title: Erstellen von Auswahlstrategien
description: Erfahren Sie, wie Sie Auswahlstrategien erstellen
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 32%

---

# Erstellen von Auswahlstrategien {#selection-strategies}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit Experience Decisioning](gs-experience-decisioning.md)
* Verwalten von Entscheidungselementen
   * [Konfigurieren des Elementkatalogs](catalogs.md)
   * [Erstellen von Entscheidungselementen](items.md)
   * [Verwalten von Elementsammlungen](collections.md)
* Elementauswahl konfigurieren
   * [Erstellen von Entscheidungsregeln](rules.md)
   * [Erstellen von Ranking-Methoden](ranking.md)
* **[Erstellen von Auswahlstrategien](selection-strategies.md)**
* [Entscheidungsrichtlinien erstellen](create-decision.md)

>[!ENDSHADEBOX]

Eine Auswahlstrategie ist ein wiederverwendbares Element, das aus einer Kollektion besteht, die mit einer Eignungsbegrenzung verknüpft ist, und einer Ranking-Methode, mit der bestimmt wird, welche Angebote bei Auswahl in einem [Entscheidungspolitik](create-decision.md).

## Zugreifen auf und Verwalten von Auswahlstrategien

1. Navigieren Sie zu **[!UICONTROL Erlebnisentscheidungen]** > **[!UICONTROL Konfiguration]** > **[!UICONTROL Auswahlstrategien]**.

1. Alle bisher erstellten Auswahlstrategien werden aufgelistet. Es stehen Filter zur Verfügung, mit denen Sie Strategien gemäß der Rangmethode abrufen können.

   ![](assets/strategy-list-filters.png)

1. Klicken Sie auf den Namen einer Auswahlstrategie, um sie zu bearbeiten.

1. Die für die einzelnen Strategien ausgewählte Kollektions-, Ranking- und Eignungsmethode wird ebenfalls angezeigt. Sie können auf das Symbol neben jedem Sammlungsnamen klicken, um eine Sammlung direkt zu bearbeiten.

   ![](assets/strategy-list-edit-collection.png)

## Erstellen einer Auswahlstrategie

Gehen Sie wie folgt vor, um eine Auswahlstrategie zu erstellen.

1. Aus dem **[!UICONTROL Auswahlstrategien]** inventory, click **[!UICONTROL Auswahlstrategie erstellen]**.

   ![](assets/strategy-create-button.png)

1. Fügen Sie einen Namen für Ihre Strategie hinzu.

   >[!NOTE]
   >
   >Derzeit ist nur die Standardeinstellung **[!UICONTROL Angebote]** Katalog verfügbar.

1. Füllen Sie die Details für Ihre Auswahlstrategie aus, beginnend mit dem Namen.

   ![](assets/strategy-create-screen.png)

1. Angebot auswählen [collection](collections.md) , der die zu berücksichtigenden Angebote enthält.

1. Verwenden Sie die **[!UICONTROL Förderfähigkeit]** -Feld, um die Auswahl der Angebote für diese Auswahlstrategie zu beschränken.

   ![](assets/strategy-create-eligibility.png)

   * Um die Angebotsauswahl auf die Mitglieder einer Experience Platform-Audience zu beschränken, wählen Sie **[!UICONTROL Zielgruppen]** und wählen Sie eine Zielgruppe aus der Liste aus. [Erfahren Sie, wie Sie mit Zielgruppen arbeiten.](../audience/about-audiences.md)

   * Wenn Sie eine Auswahlbegrenzung mit einer Entscheidungsregel hinzufügen möchten, verwenden Sie die Option **[!UICONTROL Entscheidungsregel]** und wählen Sie die gewünschte Regel aus. [Erfahren Sie, wie Sie eine Regel erstellen](rules.md)

1. Definieren Sie die Ranking-Methode, die Sie zur Auswahl des besten Angebots für jedes Profil verwenden möchten. [Weitere Informationen](#select-ranking-method)

   ![](assets/strategy-create-ranking.png)

   * Wenn mehrere Angebote für diese Strategie infrage kommen, wird die [Angebotspriorität](#offer-priority) verwendet den in den Angeboten definierten Wert.

   * Wenn Sie ein bestimmtes berechnetes Ergebnis verwenden möchten, um zu entscheiden, welches geeignete Angebot geliefert werden soll, wählen Sie [Formel](#ranking-formula) oder [KI-Modell](#ai-ranking).

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Sie kann jetzt in einer [Entscheidung](create-decision.md)

## Auswählen einer Ranking-Methode {#select-ranking-method}

Wenn mehrere Angebote für eine bestimmte Auswahlstrategie infrage kommen, können Sie bei der Erstellung einer Auswahlstrategie für jedes Profil die Methode auswählen, nach der das beste Angebot ausgewählt wird. Sie können Angebote nach folgenden Kriterien sortieren:

* [Angebotspriorität](#offer-priority)
* [Formel](#ranking-formula)
* [KI-Rangfolge](#ai-ranking)

### Angebotspriorität {#offer-priority}

Wenn mehrere Angebote für eine bestimmte Platzierung in einer Entscheidung infrage kommen, sind die Artikel mit den höchsten **priority** werden zuerst an die Kunden geliefert.

![](assets/item-priority.png)

Beim Erstellen einer [Entscheidungspunkt](items.md).

### Rangfolgenformel {#ranking-formula}

Zusätzlich zur Angebotspriorität können Sie mit Journey Optimizer **Rangfolgenformeln** erstellen. Dabei handelt es sich um Formeln, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst präsentiert werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Sie können beispielsweise die Priorität aller Angebote erhöhen, deren Enddatum weniger als 24 Stunden entfernt ist, oder die Priorität von Angeboten aus der Kategorie „Laufen“ erhöhen, wenn das Interesse eines Profils „Laufen“ ist. Näheres dazu, wie Sie eine Rangfolgenformel erstellen, finden Sie in [diesem Abschnitt](ranking.md).

Nach der Erstellung können Sie diese Formel in einer Auswahlstrategie verwenden. Wenn bei Verwendung dieser Auswahlstrategie mehrere Angebote unterbreitet werden können, berechnet die Entscheidung anhand der ausgewählten Formel, welches Angebot zuerst unterbreitet werden soll.

### KI-Rangfolge {#ai-ranking}

Sie können auch ein System mit trainierten Modellen verwenden, das automatisch eine Rangfolge der Angebote erstellt, die für ein bestimmtes Profil angezeigt werden sollen, indem Sie ein KI-Modell auswählen. In [diesem Abschnitt](ranking.md) erfahren Sie, wie Sie ein KI-Modell erstellen.

Nachdem ein KI-Modell erstellt wurde, können Sie es in einer Auswahlstrategie verwenden. Wenn mehrere Angebote infrage kommen, bestimmt das trainierte Modellsystem, welches Angebot für diese Auswahlstrategie zuerst unterbreitet werden soll.

