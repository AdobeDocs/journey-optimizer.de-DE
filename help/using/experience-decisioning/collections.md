---
title: Sammlungen
description: Erfahren Sie, wie Sie mit Sammlungen arbeiten.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '518'
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
   1. Wählen Sie den gewünschten Operator aus und geben Sie den zu filternden Wert ein. Verwenden Sie hierzu explizit die einzelnen Angebotsnamen oder erstellen Sie ein Tag „luma-summer“ und weisen Sie es den einzelnen Angeboten zu.

      >[!NOTE]
      >
      >Der **CONTAINS**-Operator unterstützt keine Teil- oder Platzhalterübereinstimmungen. Er funktioniert wie ein **IN**-Operator, d. h. Sie müssen ein Array von exakten Werten für das Attribut angeben.
      >
      >Angenommen, Sie möchten mehrere Sommerangebote in eine Sammlung aufnehmen: *„luma-summer-yoga“*, *„luma-summer-fitness“* und *„luma-summer-running“*. Um diese Elemente einzubeziehen, müssen Sie eine Regel wie „Angebotsname“ CONTAINS „luma-summer-yoga“, „luma-summer-fitness“, „luma-summer-running“ definieren. Diese Regel gibt nur Angebote zurück, die genau mit einem der Namen in der Liste übereinstimmen.
      >
      >Wenn Sie eine teilweise Übereinstimmung benötigen (z. B. alle Angebote, die *„luma-summer“* enthalten), wird dies derzeit nicht unterstützt. Sie müssen jeden Angebotsnamen explizit angeben oder jedem Angebot ein Tag *„luma-summer“* zuweisen und dieses Tag in Ihrer Regel verwenden.

   1. Wiederholen Sie diese Schritte gegebenenfalls, bis Sie die gewünschte Anzahl an Regeln hinzugefügt haben. Wenn mehrere Regeln hinzugefügt werden, können Sie zwischen den Operatoren **Und** und **Oder** wählen, um die Regeln zu kombinieren. Klicken Sie dazu auf das Operatorzeichen, um zwischen den beiden Optionen zu wechseln.
   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Sammlung in der Vorschau anzeigen]**, um die Elemente anzuzeigen, die den von Ihnen definierten Regeln entsprechen.

   ![](assets/collection-create.png)

1. Nachdem die Sammlungsregeln definiert wurden, klicken Sie auf **[!UICONTROL Erstellen]**. Die Sammlung wird nun in der Liste angezeigt.

>[!NOTE]
>
>Jede Elementsammlung kann bis zu 500 Angebotselemente enthalten. [Weitere Informationen zu den Leitlinien und Einschränkungen für die Entscheidungsfindung](gs-experience-decisioning.md#guardrails)
