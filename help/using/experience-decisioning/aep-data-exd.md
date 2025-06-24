---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Adobe Experience Platform-Daten für die Entscheidungsfindung (Beta)
description: Erfahren Sie, wie Sie Adobe Experience Platform-Daten für die Entscheidungsfindung verwenden.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor
source-git-commit: 7e378cbda6ee2379a8bd795588c328cb14107aa4
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 2%

---

# Verwenden von Adobe Experience Platform-Daten für Entscheidungen{#aep-data}

>[!CONTEXTUALHELP]
>id="ajo_exd_rules_dataset_lookup"
>title="Datensatz-Suche"
>abstract="Durch die Verwendung von Adobe Experience Platform-Daten in Entscheidungsregeln können Sie Eignungskriterien definieren, die auf dynamischen, externen Attributen basieren, sodass Entscheidungselemente nur angezeigt werden, wenn sie relevant sind. Erstellen Sie eine Zuordnung, um festzulegen, wie der Adobe Experience Platform-Datensatz mit Daten in [!DNL Journey Optimizer] verbunden wird. Wählen Sie den Datensatz mit den erforderlichen Attributen und einen Verbindungsschlüssel aus, der sowohl in den Attributen des Entscheidungselements als auch im Datensatz vorhanden ist."

>[!CONTEXTUALHELP]
>id="ajo_exd_formula_dataset_lookup"
>title="Datensatz-Suche"
>abstract="Rangfolgeformeln definieren die Priorität von Entscheidungselementen. Durch Verwendung [!DNL Adobe Experience Platform] Datensatzattribute können Sie die Rangfolgelogik dynamisch anpassen, um reale Bedingungen widerzuspiegeln. Erstellen Sie eine Zuordnung, um festzulegen, wie der Adobe Experience Platform-Datensatz mit Daten in [!DNL Journey Optimizer] verbunden wird. Wählen Sie den Datensatz mit den erforderlichen Attributen und einen Verbindungsschlüssel aus, der sowohl in den Attributen des Entscheidungselements als auch im Datensatz vorhanden ist"

>[!AVAILABILITY]
>
>Diese Funktion steht derzeit allen Kunden als öffentliche Beta-Version zur Verfügung. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Zugriff auf diese Funktion wünschen

[!DNL Journey Optimizer] ermöglicht die Nutzung von Daten aus [!DNL Adobe Experience Platform] zur Entscheidungsfindung. Auf diese Weise können Sie die Definition Ihrer Entscheidungsattribute auf zusätzliche Daten in Datensätzen für Massenaktualisierungen erweitern, die sich regelmäßig ändern, ohne die Attribute einzeln manuell aktualisieren zu müssen. Beispielsweise Verfügbarkeit, Wartezeiten usw.

## Einschränkungen und Richtlinien der Beta-Version {#guidelines}

Bevor Sie beginnen, beachten Sie die folgenden Einschränkungen und Richtlinien:

* Eine Entscheidungsrichtlinie kann für alle Entscheidungsregeln und Rangfolgenformeln zusammen auf bis zu drei Datensätze insgesamt verweisen. Wenn Ihre Regeln beispielsweise zwei Datensätze verwenden, können Ihre Formeln nur einen zusätzlichen Datensatz verwenden.
* Eine Entscheidungsregel kann drei Datensätze verwenden.
* Eine Rangfolgenformel kann drei Datensätze verwenden.
* Wenn eine Entscheidungsrichtlinie ausgewertet wird, führt das System insgesamt bis zu 1.000 Datensatzabfragen (Lookups) durch. Jede Datensatzzuordnung, die von einem Entscheidungselement verwendet wird, zählt als eine Abfrage. Beispiel: Wenn ein Entscheidungselement zwei Datensätze verwendet, zählt die Auswertung dieses Angebots als zwei Abfragen bis zum Limit von 1.000 Abfragen.

## Aktivieren eines Datensatzes für Datensuchen {#enable}

Um Daten aus einem [!DNL Adobe Experience Platform] Datensatz für die Entscheidungsfindung zu verwenden, müssen Sie ihn zunächst über einen API-Aufruf für die Suche aktivieren. Detaillierte Anweisungen finden Sie in diesem Abschnitt: [Nutzen von Adobe Experience Platform-Datensätzen in Journey Optimizer](../data/lookup-aep-data.md).

## Verwenden von Adobe Experience Platform-Daten für Entscheidungen

Sobald ein Datensatz für die Suche aktiviert ist, können Sie seine Attribute verwenden, um Ihre Entscheidungslogik mit externen Daten anzureichern. Dies ist besonders nützlich bei Attributen, die sich häufig ändern, z. B. Produktverfügbarkeit oder Echtzeit-Preisen.

Attribute aus Adobe Experience Platform-Datensätzen können in zwei Teilen der Entscheidungslogik verwendet werden:

* **Entscheidungsregeln**: Definieren, ob ein Entscheidungselement angezeigt werden kann.
* **Rangfolgeformeln**: Priorisieren von Entscheidungselementen basierend auf externen Daten.

In den nächsten Abschnitten wird erläutert, wie Sie Adobe Experience Platform-Daten in beiden Kontexten verwenden.

### Entscheidungsregeln {#rules}

Durch die Verwendung von Adobe Experience Platform-Daten in Entscheidungsregeln können Sie Eignungskriterien definieren, die auf dynamischen, externen Attributen basieren, sodass Entscheidungselemente nur angezeigt werden, wenn sie relevant sind.

Nehmen wir beispielsweise an, eine Online-retailer möchte Produktempfehlungen auf der Grundlage des lokalen Ladenbestands bewerben. Ein Produkt sollte nur dann für eine Empfehlung infrage kommen, wenn es am nächstgelegenen Standort vorrätig ist. Ein Datensatz mit täglichen Inventaraktualisierungen wird in Adobe Experience Platform hochgeladen. Die Regellogik prüft, ob der `inventory_count` für ein bestimmtes Produkt größer als 0 für den bevorzugten Speicher des Kunden ist. Wenn ja, ist das Entscheidungselement geeignet.

Gehen Sie wie folgt vor, um Adobe Experience Platform-Daten in Entscheidungsregeln zu verwenden:

1. Gehen Sie zum **[!UICONTROL Strategie einrichten]** / **[!UICONTROL Entscheidungsregeln]** und wählen Sie **[!UICONTROL Regel mit Datensatz erstellen]**.

   ![](assets/exd-lookup-rule.png)

1. Klicken Sie **[!UICONTROL Zuordnung erstellen]**, um festzulegen, wie der Adobe Experience Platform-Datensatz mit Daten in [!DNL Journey Optimizer] verbunden wird.

   * Wählen Sie den Datensatz mit den benötigten Attributen aus.
   * Wählen Sie einen Verbindungsschlüssel (z. B. Produkt-ID oder Store-ID) aus, der sowohl in den Attributen des Entscheidungselements als auch im Datensatz vorhanden ist.

   ![](assets/exd-lookup-mapping.png)

   >[!NOTE]
   >
   >Sie können bis zu 3 Zuordnungen pro Regel erstellen.

1. Klicken Sie **[!UICONTROL Weiter]**. Sie können jetzt auf die Datensatzattribute im Menü **[!UICONTROL Datensatzsuche]** zugreifen und sie in Ihren Regelbedingungen verwenden. [Erfahren Sie, wie Sie eine Entscheidungsregel erstellen können](../experience-decisioning/rules.md#create).

   ![](assets/exd-lookup-menu.png)

### Rangfolgeformeln

Rangfolgeformeln definieren die Priorität von Entscheidungselementen. Durch Verwendung [!DNL Adobe Experience Platform] Datensatzattribute können Sie die Rangfolgelogik dynamisch anpassen, um reale Bedingungen widerzuspiegeln.

Nehmen wir beispielsweise an, eine Fluggesellschaft verwendet eine Rangfolgenformel, um Upgrade-Angebote zu priorisieren. Wenn ein Kunde über eine hohe Treuestufe verfügt und die aktuelle Verfügbarkeit von Lizenzen niedrig ist (basierend auf einem Datensatz, der stündlich aktualisiert wird), erhält er eine höhere Priorität. Der Datensatz enthält Felder wie `flight_number`, `available_seats` und `loyalty_score`.

Gehen Sie wie folgt vor, um Adobe Experience Platform-Daten in Rangfolgeformeln zu verwenden:

1. Rangfolgenformel erstellen oder bearbeiten Klicken **[!UICONTROL Abschnitt „Datensatzsuche]** auf **[!UICONTROL Zuordnung erstellen]**.

1. Definieren Sie die Datensatzzuordnung:

   * Wählen Sie den entsprechenden Datensatz aus (z. B. Sitzplatzverfügbarkeit nach Flug).
   * Wählen Sie einen Verbindungsschlüssel (z. B. Flugnummer oder Kunden-ID) aus, der sowohl in den Attributen des Entscheidungselements als auch im Datensatz vorhanden ist.

   ![](assets/exd-lookup-formula-mapping.png)

   >[!NOTE]
   >
   >Sie können bis zu 3 Zuordnungen pro Rangfolgenformel erstellen.

1. Verwenden Sie die Datensatzfelder, um Ihre Rangfolgenformel wie gewohnt zu erstellen. [Erfahren Sie, wie Sie eine Rangfolgenformel erstellen](../experience-decisioning/exd-ranking-formulas.md#create-ranking-formula)

   ![](assets/exd-lookup-formula-criteria.png)
