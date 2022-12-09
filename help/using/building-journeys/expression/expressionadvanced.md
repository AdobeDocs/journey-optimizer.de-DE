---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zum erweiterten Ausdruckseditor
description: Erfahren Sie, wie Sie erweiterte Ausdrücke erstellen
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Informationen zum erweiterten Ausdruckseditor {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Informationen zum erweiterten Ausdruckseditor"
>abstract="Verwenden Sie den erweiterten Ausdruckseditor, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Sie Ausdrücke erstellen, wenn Sie Journeys konfigurieren und verwenden und eine Datenquellenbedingung definieren."

Verwenden Sie den erweiterten Ausdruckseditor, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Sie Ausdrücke erstellen, wenn Sie Journeys konfigurieren und verwenden und eine Datenquellenbedingung definieren.
Sie ist auch immer dann verfügbar, wenn Sie Aktionsparameter definieren müssen, die bestimmte Datenmanipulationen erfordern. Sie können Daten aus den Ereignissen oder zusätzliche Informationen aus der Datenquelle nutzen. In einer Journey ist die angezeigte Liste von Ereignisfeldern kontextbezogen und variiert je nach den Ereignissen, die in der Journey hinzugefügt werden.

Der erweiterte Ausdruckseditor bietet eine Reihe integrierter Funktionen und Operatoren, mit denen Sie Werte bearbeiten und einen Ausdruck definieren können, der Ihren Anforderungen entspricht. Mit dem erweiterten Ausdruckseditor können Sie auch die Werte des Parameters für die externe Datenquelle definieren, Zuordnungsfelder und Sammlungen bearbeiten, z. B. Erlebnisereignisse.

![](../assets/journey65.png)

_Benutzeroberfläche des erweiterten Ausdruckseditors_

Der erweiterte Ausdruckseditor kann für folgende Aufgaben verwendet werden:

* erstellen [erweiterte Bedingungen](../condition-activity.md#about_condition) zu Datenquellen und Ereignisinformationen
* Definieren benutzerdefinierter [Warteaktivitäten](../wait-activity.md#custom)
* Definieren der Zuordnung von Aktionsparametern

Wenn möglich, können Sie mithilfe der **[!UICONTROL Advanced mode]** / **[!UICONTROL Simple mode]** Schaltfläche. Der einfache Modus wird beschrieben [here](../condition-activity.md#about_condition).

>[!NOTE]
>
>Bedingungen können im einfachen oder erweiterten Ausdruckseditor definiert werden. Sie geben immer einen booleschen Typ zurück.
>
>Aktionsparameter können durch die Auswahl von Feldern oder über den erweiterten Ausdruckseditor definiert werden. Sie geben je nach Ausdruck einen bestimmten Datentyp zurück.

## Zugriff auf den erweiterten Ausdruckseditor {#accessing-the-advanced-expression-editor}

Sie haben verschiedene Möglichkeiten, auf den erweiterten Ausdruckseditor zuzugreifen:

* Wenn Sie eine Bedingung der Datenquelle erstellen, können Sie auf den erweiterten Editor zugreifen, indem Sie auf **[!UICONTROL Advanced mode]**.

   ![](../assets/journeyuc2_33.png)

* Wenn Sie einen benutzerdefinierten Timer erstellen, wird der erweiterte Editor direkt angezeigt.
* Wenn Sie Aktionsparameter zuordnen, klicken Sie auf **[!UICONTROL Advanced mode]**.

## Benutzeroberfläche{#discovering-the-interface}

In diesem Bildschirm können Sie Ihren Ausdruck manuell schreiben.

![](../assets/journey70.png)

Auf der linken Bildschirmseite werden die verfügbaren Felder und Funktionen angezeigt:

* **[!UICONTROL Events]**: Wählen Sie eines der Felder aus, die vom eingehenden Ereignis empfangen wurden. Die angezeigte Liste von Ereignisfeldern ist kontextbezogen und variiert je nach den Ereignissen, die in der Journey hinzugefügt werden. [Mehr dazu](../../event/about-events.md)
* **[!UICONTROL Segments]**: wenn Sie eine **[!UICONTROL Segment qualification]** -Ereignis verwenden, wählen Sie das Segment aus, das Sie in Ihrem Ausdruck verwenden möchten. [Mehr dazu](../condition-activity.md#using-a-segment)
* **[!UICONTROL Data Sources]**: Wählen Sie aus der Liste der Felder aus, die in den Feldergruppen Ihrer Datenquellen verfügbar sind. [Mehr dazu](../../datasource/about-data-sources.md)
* **[!UICONTROL Journey properties]**: In diesem Abschnitt werden die technischen Felder für die Journey eines bestimmten Profils zusammengefasst. [Mehr dazu](journey-properties.md)
* **[!UICONTROL Functions]**: Wählen Sie aus der Liste der integrierten Funktionen, die eine komplexe Filterung ermöglichen. Die Funktionen sind nach Kategorien geordnet. [Mehr dazu](functions.md)

![](../assets/journey65.png)

Ein Mechanismus zur automatischen Vervollständigung zeigt kontextbezogene Vorschläge an.

![](../assets/journey68.png)

Ein Syntaxvalidierungsmechanismus überprüft die Integrität Ihres Codes. Fehler werden über dem Editor angezeigt.

![](../assets/journey69.png)

**Bedarf an Parametern beim Erstellen von Bedingungen mit dem erweiterten Ausdruckseditor**

Wenn Sie ein Feld aus einer externen Datenquelle auswählen, für das ein Parameter aufgerufen werden muss (siehe [diese Seite](../../datasource/external-data-sources.md). In einer wetterbezogenen Datenquelle lautet beispielsweise der häufig verwendete Parameter &quot;city&quot;. Daher müssen Sie auswählen, wo Sie diesen Parameter &quot;city&quot;abrufen möchten. Funktionen können auch auf Parameter angewendet werden, um Formatänderungen oder Verkettungen durchzuführen.

![](../assets/journeyuc2_19.png)

Bei komplexeren Anwendungsfällen können Sie, wenn Sie die Parameter der Datenquelle in den Hauptausdruck aufnehmen möchten, deren Werte mit dem Keyword &quot;params&quot;definieren. Siehe [diese Seite](../expression/field-references.md).
