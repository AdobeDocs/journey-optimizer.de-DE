---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Adobe Experience Platform-Daten für die Entscheidungsfindung
description: Erfahren Sie, wie Sie Adobe Experience Platform-Daten für die Entscheidungsfindung verwenden.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Developer
level: Intermediate
keywords: Ausdruck, Editor
exl-id: 46d868b3-01d2-49fa-852b-8c2e2f54292f
version: Journey Orchestration
source-git-commit: abdce896a63f7d1eee7b45fea025405bf88cad2a
workflow-type: tm+mt
source-wordcount: '1200'
ht-degree: 99%

---

# Verwenden von Adobe Experience Platform-Daten für die Entscheidungsfindung {#aep-data}

>[!CONTEXTUALHELP]
>id="ajo_exd_catalogs_dataset"
>title="Datensatzsuche"
>abstract="Um Attribute aus Adobe Experience Platform für die Entscheidungsfindung zu verwenden, müssen Sie eine Zuordnung erstellen, um zu definieren, wie der Adobe Experience Platform-Datensatz mit Daten in [!DNL Journey Optimizer] verbunden wird."

>[!CONTEXTUALHELP]
>id="ajo_exd_catalogs_dataset_create"
>title="Datensatzsuche"
>abstract="Wählen Sie unter allen für die Suche aktivierten Adobe Experience Platform-Datensätzen den Datensatz mit den erforderlichen Attributen und dann einen Zuordnungsschlüssel (z. B. Flugnummer oder Kunden-ID) aus, der sowohl in den Entscheidungselementattributen als auch im Datensatz vorhanden ist."

>[!CONTEXTUALHELP]
>id="ajo_exd_rules_dataset_lookup"
>title="Datensatzsuche"
>abstract="Wählen Sie den Adobe Experience Platform-Datensatz mit den erforderlichen Attributen aus. Wenn der Datensatz nicht in der Liste angezeigt wird, stellen Sie sicher, dass Sie ihn für die Suche aktiviert und eine Suchzuordnung für den Datensatz erstellt haben."

>[!CONTEXTUALHELP]
>id="ajo_exd_formula_dataset_lookup"
>title="Datensatzsuche"
>abstract="Verwenden Sie Datensatzattribute aus [!DNL Adobe Experience Platform], um die Rangfolgelogik dynamisch anzupassen und reale Bedingungen widerzuspiegeln. Klicken Sie auf **[!UICONTROL Datensatz hinzufügen]**, um den Adobe Experience Platform-Datensatz mit den erforderlichen Attributen auszuwählen. Wenn der Datensatz nicht in der Liste angezeigt wird, stellen Sie sicher, dass Sie ihn für die Suche aktiviert und eine Suchzuordnung für den Datensatz erstellt haben."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_capping_dataset"
>title="Hinzufügen eines Datensatzes"
>abstract="Verwenden Sie Datensatzattribute aus [!DNL Adobe Experience Platform], um die Begrenzungskriterien basierend auf dynamischen, externen Attributen zu definieren. Klicken Sie auf **[!UICONTROL Datensatz hinzufügen]**, um den Adobe Experience Platform-Datensatz mit den erforderlichen Attributen auszuwählen. Wenn der Datensatz nicht in der Liste angezeigt wird, stellen Sie sicher, dass Sie ihn für die Suche aktiviert und eine Suchzuordnung für den Datensatz erstellt haben."

[!DNL Journey Optimizer] ermöglicht die Nutzung von [!DNL Adobe Experience Platform]-Daten für die Entscheidungsfindung. Auf diese Weise können Sie die Definition Ihrer Entscheidungsattribute auf zusätzliche Daten in Datensätzen für Massenaktualisierungen erweitern, die sich regelmäßig ändern, sodass die Attribute nicht einzeln manuell aktualisiert werden müssen. Beispielsweise Verfügbarkeit, Wartezeiten usw.

>[!AVAILABILITY]
>
>Diese Funktion steht derzeit allen Kundinnen und Kunden eingeschränkt zur Verfügung.

## Leitlinien und Einschränkungen {#guardrails}

* **Unterstützte Kanäle**: Die Datensatzsuche mit Entscheidungsfindung funktioniert derzeit für benutzerdefinierte E-Mail- und Journey-Aktionen. <!--Support for code-based experience channels is coming soon.-->
* **Attributverwendung**: Die Datensatzsuchfunktion für die Entscheidungsfindung erweitert Entscheidungselementdefinitionen mit zusätzlichen Attributen. Attribute werden nicht auf Profile erweitert.
* **Lookup-Limits**: [!DNL Journey Optimizer] unterstützt bis zu 1.000 Suchen pro Entscheidungsrichtlinie.

## Voraussetzungen

### Aktivieren von Datensätzen für die Suche

Bevor Sie beginnen, müssen für die Entscheidungsfindung erforderliche Datensätze zunächst für die Suche aktiviert werden. Führen Sie die in diesem Abschnitt beschriebenen Schritte aus: [Verwenden von Adobe Experience Platform-Daten](../data/lookup-aep-data.md).

### Erstellen von Zuordnungen

Um Attribute aus Adobe Experience Platform für die Entscheidungsfindung zu verwenden, müssen Sie eine Zuordnung erstellen, um zu definieren, wie der Adobe Experience Platform-Datensatz mit Daten in [!DNL Journey Optimizer] verbunden wird. Gehen Sie dazu wie folgt vor:

1. Navigieren Sie zu **[!UICONTROL Kataloge]** / **[!UICONTROL Datensatzsuche]** und klicken Sie dann auf **[!UICONTROL Erstellen]**.

   ![](assets/exd-lookup-mapping.png)

1. Konfigurieren Sie die Zuordnung:

   1. Klicken Sie auf **[!UICONTROL Datensatz auswählen]**, um alle Adobe Experience Platform-Datensätze anzuzeigen, die für die Suche aktiviert wurden. Wählen Sie den Datensatz mit den benötigten Attributen aus.

   1. Klicken Sie auf **[!UICONTROL Schlüssel auswählen]**, um einen Verbindungsschlüssel auszuwählen (z. B. Flugnummer oder Kunden-ID), der sowohl in den Attributen des Entscheidungselements als auch im Datensatz vorhanden ist.

   ![](assets/exd-lookup-mapping-create.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Nutzen von Adobe Experience Platform-Daten {#leverage-aep-data}

Sobald ein Datensatz für die Suche aktiviert ist und Zuordnungen erstellt wurden, können Sie die Daten verwenden, um Ihre Entscheidungslogik mit externen Daten anzureichern. Dies ist besonders nützlich bei Attributen, die sich häufig ändern, beispielsweise die Produktverfügbarkeit oder Echtzeitpreise.

Attribute aus Adobe Experience Platform-Datensätzen können in zwei Teilen der Entscheidungslogik verwendet werden:

* **Entscheidungsregeln**: Definieren, ob ein Entscheidungselement angezeigt werden kann.
* **Rangfolgenformeln**: Priorisieren Entscheidungselemente basierend auf externen Daten.
* **Begrenzungsregeln**: Nutzen Sie externe Daten, um den Schwellenwert für Begrenzungsregeln zu berechnen.

In den nächsten Abschnitten wird erläutert, wie Sie Adobe Experience Platform-Daten in diesen Kontexten verwenden.

### Entscheidungsregeln {#rules}

Durch die Verwendung von Adobe Experience Platform-Daten in Entscheidungsregeln können Sie Eignungskriterien definieren, die auf dynamischen, externen Attributen basieren, sodass Entscheidungselemente nur angezeigt werden, wenn sie relevant sind.

Nehmen wir beispielsweise an, ein Online-Einzelhändler möchte Produktempfehlungen auf der Grundlage des lokalen Ladenbestands bewerben. Ein Produkt sollte nur dann für eine Empfehlung infrage kommen, wenn es am nächstgelegenen Standort vorrätig ist. Ein Datensatz mit täglichen Inventaraktualisierungen wird in Adobe Experience Platform hochgeladen. Die Regellogik prüft, ob `inventory_count` für ein bestimmtes Produkt am bevorzugten Standort der Kundin bzw. des Kunden größer als 0 ist. Wenn dies der Fall ist, ist das Entscheidungselement geeignet.

Gehen Sie wie folgt vor, um Adobe Experience Platform-Daten in Entscheidungsregeln zu verwenden:

1. Navigieren Sie zum Menü **[!UICONTROL Strategie-Setup]**/**[!UICONTROL Entscheidungsregeln]** und wählen Sie **[!UICONTROL Regel mit Datensatz erstellen]** aus.

   ![](assets/exd-lookup-rule.png)

1. Klicken Sie auf **[!UICONTROL Datensatz hinzufügen]**, um den Datensatz mit den erforderlichen Attributen auszuwählen. 

   ![](assets/exd-lookup-select-dataset.png)

1. Klicken Sie auf **[!UICONTROL Fortfahren]**. Sie können jetzt im Menü **[!UICONTROL Datensatzsuche]** auf die Datensatzattribute zugreifen und sie in Ihren Regelbedingungen verwenden. [Erfahren Sie, wie Sie eine Entscheidungsregel erstellen können](../experience-decisioning/rules.md#create).

   ![](assets/exd-lookup-menu.png)

### Rangfolgenformeln {#ranking-formulas}

Rangfolgenformeln definieren die Priorität von Entscheidungselementen. Durch Verwendung von Datensatzattributen aus [!DNL Adobe Experience Platform] können Sie die Rangfolgelogik dynamisch anpassen, um reale Bedingungen widerzuspiegeln. 

Nehmen wir beispielsweise an, eine Fluggesellschaft verwendet eine Rangfolgenformel, um Upgrade-Angebote zu priorisieren. Wenn eine Kundin bzw. ein Kunde über eine hohe Treuestufe verfügt und die aktuelle Verfügbarkeit von Sitzplätzen niedrig ist (basierend auf einem Datensatz, der stündlich aktualisiert wird), erhält die Person eine höhere Priorität. Der Datensatz enthält Felder wie `flight_number`, `available_seats` und `loyalty_score`.

Gehen Sie wie folgt vor, um Adobe Experience Platform-Daten in Rangfolgenformeln zu verwenden:

1. Erstellen oder bearbeiten Sie eine Rangfolgenformel.

1. Klicken Sie im Abschnitt **[!UICONTROL Datensatzsuche]** auf **[!UICONTROL Datensatz hinzufügen]**.

1. Wählen Sie den entsprechenden Datensatz aus. 

   ![](assets/exd-lookup-formula-dataset.png)

   >[!NOTE]
   >
   >Wenn der Datensatz, nach dem Sie suchen, nicht in der Liste angezeigt wird, vergewissern Sie sich, dass Sie ihn für die Suche aktiviert und eine Suchzuordnung für den Datensatz erstellt haben. Weitere Informationen finden Sie im Abschnitt [Voraussetzungen](#prerequisites).

1. Verwenden Sie die Datensatzfelder, um Ihre Rangfolgenformel wie gewohnt zu erstellen. [Weitere Informationen zum Erstellen einer Rangfolgenformel](ranking/ranking-formulas.md#create-ranking-formula)

   ![](assets/exd-lookup-formula-criteria.png)

### Begrenzungsregeln {#capping-rules}

Begrenzungsregeln dienen als Einschränkungen, um festzulegen, wie oft ein Entscheidungselement maximal angezeigt werden darf. Durch die Verwendung von Adobe Experience Platform-Daten in Begrenzungsregeln können Sie Begrenzungskriterien definieren, die auf dynamischen, externen Attributen basieren. Verwenden Sie dazu einen Ausdruck in Ihrer Begrenzungsregel, um den gewünschten Begrenzungsschwellenwert zu berechnen.

Beispielsweise kann ein Einzelhändler ein Angebot auf der Grundlage des Echtzeit-Produktinventars begrenzen. Anstatt einen festen Schwellenwert von 500 festzulegen, verwendet er einen Ausdruck, der aus einem Adobe Experience Platform-Datensatz auf das Feld `inventory_count` verweist. Wenn der Datensatz zeigt, dass noch 275 Artikel auf Lager sind, wird das Angebot nur bis zu dieser Zahl zugestellt.

>[!NOTE]
>
>**Ausdrücke** für Begrenzungsregeln sind derzeit für alle Benutzenden als Funktion mit eingeschränkter Verfügbarkeit verfügbar und werden nur beim Begrenzungstyp **[!UICONTROL Insgesamt]** unterstützt.

Gehen Sie wie folgt vor, um Adobe Experience Platform-Daten in Ausdrücken für Begrenzungsregeln zu verwenden:

1. Erstellen oder bearbeiten Sie ein Entscheidungselement.

1. Klicken Sie beim Definieren der Elementeignung auf **[!UICONTROL Datensatz hinzufügen]** und wählen Sie den entsprechenden Datensatz aus.

   ![](assets/exd-lookup-capping.png)

   >[!NOTE]
   >
   >Wenn der Datensatz, nach dem Sie suchen, nicht in der Liste angezeigt wird, vergewissern Sie sich, dass Sie ihn für die Suche aktiviert und eine Suchzuordnung für den Datensatz erstellt haben. Weitere Informationen finden Sie im Abschnitt [Voraussetzungen](#prerequisites).

1. Wählen Sie den Begrenzungstyp **[!UICONTROL Insgesamt]** und aktivieren Sie dann die Option **[!UICONTROL Ausdruck]**.

   ![](assets/exd-lookup-capping-expression.png)

   >[!NOTE]
   >
   >Wenn der Datensatz, nach dem Sie suchen, nicht in der Liste angezeigt wird, vergewissern Sie sich, dass Sie ihn für die Suche aktiviert und eine Suchzuordnung für den Datensatz erstellt haben. Weitere Informationen finden Sie im Abschnitt [Voraussetzungen](#prerequisites).

1. Bearbeiten Sie den Ausdruck und verwenden Sie die Datensatzfelder, um Ihren Ausdruck zu erstellen.

   ![](assets/exd-lookup-capping-attribute.png)

1. Schließen Sie die Konfiguration Ihrer Begrenzung und des Entscheidungsregelelements wie gewohnt ab. [Erfahren Sie, wie Sie Begrenzungsregeln konfigurieren können](../experience-decisioning/items.md#capping)
