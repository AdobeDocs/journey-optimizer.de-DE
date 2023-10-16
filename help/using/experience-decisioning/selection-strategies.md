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
exl-id: 1b73b398-050a-40bb-a8ae-1c66e3e26ce8
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 100%

---

# Erstellen von Auswahlstrategien {#selection-strategies}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit Offer Decisioning](gs-experience-decisioning.md)
* Verwalten Ihrer Entscheidungselemente
   * [Konfigurieren des Elementkatalogs](catalogs.md)
   * [Erstellen von Entscheidungselementen](items.md)
   * [Verwalten von Elementsammlungen](collections.md)
* Konfigurieren der Elementauswahl
   * [Erstellen von Entscheidungsregeln](rules.md)
   * [Erstellen von Rangfolgemethoden](ranking.md)
* **[Erstellen von Auswahlstrategien](selection-strategies.md)**
* [Erstellen von Entscheidungsrichtlinien](create-decision.md)

>[!ENDSHADEBOX]

Eine Auswahlstrategie ist ein wiederverwendbares Element, das aus einer Sammlung besteht, die mit einer Eignungsbegrenzung verknüpft ist, und einer Rangfolgenmethode, mit der bestimmt wird, welche Angebote angezeigt werden, wenn sie in einer [Entscheidungsrichtlinie](create-decision.md) ausgewählt sind.

## Zugreifen auf und Verwalten von Auswahlstrategien

1. Navigieren Sie zu **[!UICONTROL Erlebnisentscheidungen]** > **[!UICONTROL Konfiguration]** > **[!UICONTROL Auswahlstrategien]**.

1. Es werden alle Auswahlstrategien aufgelistet, die bisher erstellt wurden. Es stehen Filter zur Verfügung, mit denen Sie Strategien gemäß der Rangfolgenmethode abrufen können.

   ![](assets/strategy-list-filters.png)

1. Klicken Sie auf den Namen einer Auswahlstrategie, um sie zu bearbeiten.

1. Es werden auch die Sammlung, Rangfolgenmethode und Eignung angezeigt, die für jede Strategie ausgewählt wurden. Sie können auf das Symbol neben jedem Sammlungsnamen klicken, um eine Sammlung direkt zu bearbeiten.

   ![](assets/strategy-list-edit-collection.png)

## Erstellen einer Auswahlstrategie

Gehen Sie wie folgt vor, um eine neue Auswahlstrategie zu erstellen.

1. Klicken Sie im Bestand der **[!UICONTROL Auswahlstrategien]** auf **[!UICONTROL Auswahlstrategie erstellen]**.

   ![](assets/strategy-create-button.png)

1. Fügen Sie einen Namen für Ihre Strategie hinzu.

   >[!NOTE]
   >
   >Derzeit ist nur der Standardkatalog für **[!UICONTROL Angebote]** verfügbar.

1. Füllen Sie die Details für Ihre Auswahlstrategie aus, beginnend mit dem Namen.

   ![](assets/strategy-create-screen.png)

1. Wählen Sie die [Angebotssammlung](collections.md) aus, die die zu berücksichtigenden Angebote enthält.

1. Verwenden Sie das Feld **[!UICONTROL Eignung]**, um die Auswahl der Angebote für diese Platzierung zu beschränken.

   ![](assets/strategy-create-eligibility.png)

   * Um die Angebotsauswahl auf die Mitglieder einer Experience Platform-Zielgruppe zu beschränken, wählen Sie **[!UICONTROL Zielgruppen]** aus und wählen Sie dann eine Zielgruppe aus der Liste. [Erfahren Sie, wie Sie mit Zielgruppen arbeiten können](../audience/about-audiences.md)

   * Wenn Sie eine Auswahlbegrenzung mit einer Entscheidungsregel hinzufügen möchten, verwenden Sie die Option **[!UICONTROL Entscheidungsregel]** und wählen Sie die gewünschte Regel aus. [Erfahren Sie, wie Sie eine Regel erstellen](rules.md)

1. Definieren Sie die Rangfolgenmethode, die Sie zur Auswahl des besten Angebots für jedes Profil verwenden möchten. [Weitere Informationen](#select-ranking-method)

   ![](assets/strategy-create-ranking.png)

   * Wenn mehrere Angebote für diese Strategie infrage kommen, verwendet die Methode [Angebotspriorität](#offer-priority) den Wert, der in den Angeboten definiert ist.

   * Wenn Sie ein bestimmtes berechnetes Ergebnis verwenden möchten, um zu entscheiden, welches geeignete Angebot geliefert werden soll, wählen Sie [Formel](#ranking-formula) oder [KI-Modell](#ai-ranking).

1. Klicken Sie auf **[!UICONTROL Erstellen]**. Es kann jetzt in einer [Entscheidung](create-decision.md) verwendet werden

## Auswählen einer Rangfolgenmethode {#select-ranking-method}

Wenn mehrere Angebote für eine bestimmte Platzierung infrage kommen, können Sie beim Erstellen einer Entscheidungsstrategie die Methode wählen, die für jedes Profil das beste Angebot auswählt. Sie können Angebote nach folgenden Kriterien sortieren:

* [Angebotspriorität](#offer-priority)
* [Formel](#ranking-formula)
* [KI-Rangfolge](#ai-ranking)

### Angebotspriorität {#offer-priority}

Wenn mehrere Angebote für eine bestimmte Platzierung in einer Entscheidung infrage kommen, werden standardmäßig die Angebote mit der höchsten **Priorität** zuerst an die Kundinnen und Kunden gesendet.

![](assets/item-priority.png)

Die Prioritätswerte der Angebote werden beim Erstellen eines [Entscheidungselements](items.md) zugewiesen.

### Rangfolgenformel {#ranking-formula}

Zusätzlich zur Angebotspriorität können Sie mit Journey Optimizer **Rangfolgenformeln** erstellen. Dabei handelt es sich um Formeln, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst präsentiert werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Sie können beispielsweise die Priorität aller Angebote erhöhen, deren Enddatum weniger als 24 Stunden entfernt ist, oder die Priorität von Angeboten aus der Kategorie „Laufen“ erhöhen, wenn das Interesse eines Profils „Laufen“ ist. Näheres dazu, wie Sie eine Rangfolgenformel erstellen, finden Sie in [diesem Abschnitt](ranking.md).

Wenn sie erstellt wurde, können Sie diese Formel in einer Auswahlstrategie verwenden. Wenn mit dieser Auswahlstrategie mehrere Angebote für diese Platzierung infrage kommen, verwendet die Entscheidung die ausgewählte Formel, um zu berechnen, welches Angebot zuerst bereitgestellt werden soll.

### KI-Rangfolge {#ai-ranking}

Sie können auch ein System mit trainierten Modellen verwenden, das automatisch eine Rangfolge der Angebote erstellt, die für ein bestimmtes Profil angezeigt werden sollen, indem Sie ein KI-Modell auswählen. In [diesem Abschnitt](ranking.md) erfahren Sie, wie Sie ein KI-Modell erstellen.

Wenn ein KI-Modell erstellt wurde, können Sie es in einer Auswahlstrategie verwenden. Wenn mehrere Angebote geeignet sind, bestimmt das System mit trainierten Modellen, welches Angebot für diese Auswahlstrategie zuerst gezeigt werden soll.
