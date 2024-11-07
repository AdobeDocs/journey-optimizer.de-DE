---
title: Sammlungen
description: Erfahren Sie, wie Sie mit Sammlungen arbeiten.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: 22eae783ec2a7db2209b2a12b78b286e4f97ee1b
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 100%

---

# Sammlungen {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="Erstellen von Sammlungen"
>abstract="Mit Sammlungen können Entscheidungselemente nach den eigenen Vorstellungen kategorisiert und gruppiert werden. Diese Kategorien werden durch das Verfassen von Regeln erstellt, die die Attribute von Entscheidungselementen nutzen."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="Definieren von Regeln für die eigene Sammlung"
>abstract="Eine oder mehrere Regeln hinzufügen, um die Elemente zu bestimmen, die in die Sammlung aufgenommen werden sollen. Ein Elementattribut auswählen, das als Kriterium verwendet werden soll. Den gewünschten Operator auswählen und den Wert eingeben, nach dem gefiltert werden soll. So viele Regeln wie nötig hinzufügen."

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="Eine Sammlung auswählen"
>abstract="Die Sammlung auswählen, die die zu berücksichtigenden Angebote enthält. Dieser Schritt ist bei der Erstellung einer Auswahlstrategie obligatorisch. Mit Sammlungen kann man Entscheidungselemente nach eigenen Vorstellungen kategorisieren und gruppieren. Beispielsweise kann man eine Sammlung erstellen, die alle Entscheidungselemente mit dem Wert „Yoga“ im benutzerdefinierten Attribut „Kategorie“ enthält."

Mit Sammlungen können Entscheidungselemente nach den eigenen Vorstellungen kategorisiert und gruppiert werden. Diese Kategorien werden durch das Verfassen von Regeln erstellt, die die Attribute von Entscheidungselementen nutzen.

Angenommen, Sie haben dem Katalogschema Ihrer Entscheidungselemente das benutzerdefinierte Attribut „Kategorie“ hinzugefügt. Auf diese Weise können Sie eine Sammlung erstellen, die alle Entscheidungselemente mit dem Wert „Yoga“ im Attribut „Kategorie“ enthält.

Die Liste der Sammlungen ist über das Menü **[!UICONTROL Kataloge]** zugänglich.

Gehen Sie wie folgt vor, um eine Sammlung zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Kataloge]** > **[!UICONTROL Sammlungen]** und klicken Sie auf **[!UICONTROL Sammlung erstellen]**.
1. Geben Sie einen Namen und eine Beschreibung für die Sammlung ein.
1. Eine oder mehrere Regeln hinzufügen, um die Elemente zu bestimmen, die in die Sammlung aufgenommen werden sollen. Gehen Sie dazu folgendermaßen vor:

   1. Ein Elementattribut auswählen, das als Kriterium verwendet werden soll. Die Attributliste enthält alle im Katalogschema definierten standardmäßigen und benutzerdefinierten Attribute. [Weitere Informationen zum Elementkatalog](catalogs.md)
   1. Den gewünschten Operator auswählen und den Wert eingeben, nach dem gefiltert werden soll.
   1. Wiederholen Sie diese Schritte gegebenenfalls, bis Sie die gewünschte Anzahl an Regeln hinzugefügt haben. Wenn mehrere Regeln hinzugefügt werden, können Sie zwischen den Operatoren **Und** und **Oder** wählen, um die Regeln zu kombinieren. Klicken Sie dazu auf das Operatorzeichen, um zwischen den beiden Optionen zu wechseln.
   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Sammlung in der Vorschau anzeigen]**, um die Elemente anzuzeigen, die den von Ihnen definierten Regeln entsprechen.

   ![](assets/collection-create.png)

1. Nachdem die Sammlungsregeln definiert wurden, klicken Sie auf **[!UICONTROL Erstellen]**. Die Sammlung wird nun in der Liste angezeigt.
