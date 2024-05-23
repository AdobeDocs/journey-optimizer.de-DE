---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zum erweiterten Ausdruckseditor
description: Erfahren Sie, wie Sie erweiterte Ausdrücke erstellen
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Ausdruckseditor, Daten, Journey
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 26%

---

# Informationen zum erweiterten Ausdruckseditor {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Informationen zum erweiterten Ausdruckseditor"
>abstract="Verwenden Sie den erweiterten Ausdruckseditor, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Sie Ausdrücke erstellen, wenn Sie Journeys konfigurieren und verwenden oder eine Bedingung für die Datenquelle definieren."

Verwenden Sie den erweiterten Journey-Ausdruckseditor, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Sie Ausdrücke erstellen, wenn Sie Journeys konfigurieren und verwenden oder eine Bedingung für die Datenquelle definieren.

>[!NOTE]
>
>Die im erweiterten Ausdruckseditor verfügbaren Funktionen und Funktionen des Journey unterscheiden sich von den im Abschnitt [Personalisierungseditor](../../personalization/functions/functions.md).

Sie ist auch immer dann verfügbar, wenn Sie Aktionsparameter definieren müssen, die bestimmte Datenmanipulationen erfordern. Sie können Daten aus den Ereignissen oder zusätzliche Informationen aus der Datenquelle nutzen. Bei einer Journey ist die angezeigte Ereignisfeldliste kontextbezogen und variiert je nach Ereignis(en), das/die auf der Journey hinzugefügt wird.

Der erweiterte Ausdruckseditor bietet eine Reihe integrierter Funktionen und Operatoren, mit denen Sie Werte bearbeiten und einen Ausdruck definieren können, der Ihren Anforderungen entspricht. Mit dem erweiterten Ausdruckseditor können Sie auch die Werte des Parameters für die externe Datenquelle definieren, Zuordnungsfelder und Sammlungen bearbeiten, z. B. Erlebnisereignisse.

![](../assets/journey65.png)

_Benutzeroberfläche des erweiterten Ausdruckseditors_

Der erweiterte Ausdruckseditor kann für folgende Aufgaben verwendet werden:

* erstellen [erweiterte Bedingungen](../condition-activity.md#about_condition) zu Datenquellen und Ereignisinformationen
* Definieren benutzerdefinierter [Warteaktivitäten](../wait-activity.md#custom)
* Definieren der Zuordnung von Aktionsparametern

Wenn möglich, können Sie mithilfe der **[!UICONTROL Erweiterter Modus]** / **[!UICONTROL Einfacher Modus]** Schaltfläche. Der einfache Modus wird beschrieben [here](../condition-activity.md#about_condition).

>[!NOTE]
>
>Bedingungen können im einfachen oder erweiterten Ausdruckseditor definiert werden. Sie geben immer einen booleschen Typ zurück.
>
>Aktionsparameter können durch die Auswahl von Feldern oder über den erweiterten Ausdruckseditor definiert werden. Sie geben je nach Ausdruck einen bestimmten Datentyp zurück.

## Zugriff auf den erweiterten Ausdruckseditor {#accessing-the-advanced-expression-editor}

Sie haben verschiedene Möglichkeiten, auf den erweiterten Ausdruckseditor zuzugreifen:

* Wenn Sie eine Bedingung der Datenquelle erstellen, können Sie auf den erweiterten Editor zugreifen, indem Sie auf **[!UICONTROL Erweiterter Modus]**.

  ![](../assets/journeyuc2_33.png)

* Wenn Sie einen benutzerdefinierten Timer erstellen, wird der erweiterte Editor direkt angezeigt.
* Wenn Sie Aktionsparameter zuordnen, klicken Sie auf **[!UICONTROL Erweiterter Modus]**.

## Benutzeroberfläche{#discovering-the-interface}

In diesem Bildschirm können Sie Ihren Ausdruck manuell schreiben.

![](../assets/journey70.png)

Auf der linken Bildschirmseite werden die verfügbaren Felder und Funktionen angezeigt:

* **[!UICONTROL Veranstaltungen]**: Wählen Sie eines der Felder aus, die vom eingehenden Ereignis empfangen wurden. Die angezeigte Liste der Ereignisfelder ist kontextbezogen und variiert je nach den Ereignissen, die auf der Journey hinzugefügt werden. [Weitere Informationen](../../event/about-events.md)
* **[!UICONTROL Zielgruppen]**: Wenn Sie ein **[!UICONTROL Zielgruppen-Qualifizierungsereignis]** eingefügt haben, wählen Sie die Zielgruppe aus, die in Ihrem Ausdruck verwendet werden soll. [Weitere Informationen](../condition-activity.md#using-a-segment)
* **[!UICONTROL Data Sources]**: Wählen Sie aus der Liste der Felder aus, die in den Feldergruppen Ihrer Datenquellen verfügbar sind. [Weitere Informationen](../../datasource/about-data-sources.md)
* **[!UICONTROL Journey-Eigenschaften]**: Dieser Abschnitt enthält die technischen Felder, die mit der Journey für ein bestimmtes Profil verbunden sind. [Weitere Informationen](journey-properties.md)
* **[!UICONTROL Funktionen]**: Wählen Sie aus der Liste der integrierten Funktionen, die eine komplexe Filterung ermöglichen. Die Funktionen sind nach Kategorien geordnet. [Weitere Informationen](functions.md)

![](../assets/journey65.png)

Ein Mechanismus zur automatischen Vervollständigung zeigt kontextbezogene Vorschläge an.

![](../assets/journey68.png)

Ein Syntaxvalidierungsmechanismus überprüft die Integrität Ihres Codes. Fehler werden über dem Editor angezeigt.

![](../assets/journey69.png)

**Bedarf an Parametern beim Erstellen von Bedingungen mit dem erweiterten Ausdruckseditor**

Wenn Sie ein Feld aus einer externen Datenquelle auswählen, für das ein Parameter aufgerufen werden muss (siehe [diese Seite](../../datasource/external-data-sources.md)), wird rechts ein neuer Tab angezeigt, auf dem Sie den Parameter angeben können. Der Parameterwert kann aus den auf der Journey positionierten Ereignissen oder aus der Experience Platform-Datenquelle (und nicht aus anderen externen Datenquellen) stammen. In einer wetterbezogenen Datenquelle lautet beispielsweise der häufig verwendete Parameter &quot;city&quot;. Daher müssen Sie auswählen, wo Sie diesen Parameter &quot;city&quot;abrufen möchten. Funktionen können auch auf Parameter angewendet werden, um Formatänderungen oder Verkettungen durchzuführen.

![](../assets/journeyuc2_19.png)

Bei komplexeren Anwendungsfällen können Sie, wenn Sie die Parameter der Datenquelle in den Hauptausdruck aufnehmen möchten, deren Werte mit dem Keyword &quot;params&quot;definieren. Weitere Informationen finden Sie auf [dieser Seite](../expression/field-references.md).
