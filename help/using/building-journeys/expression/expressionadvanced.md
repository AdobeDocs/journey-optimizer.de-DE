---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit dem erweiterten Ausdruckseditor
description: Erfahren Sie, wie Sie erweiterte Ausdrücke erstellen
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: Ausdruckseditor, Daten, Journey
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: b69023669b6ca59ea5980b1a671a90c41eb665fb
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 100%

---

# Arbeiten mit dem erweiterten Ausdruckseditor {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Informationen zum erweiterten Ausdruckseditor"
>abstract="Der erweiterte Ausdruckseditor kann verwendet werden, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Ausdrücke erstellt werden, wenn Journeys konfiguriert und verwendt werden oder eine Bedingung für die Datenquelle definiert wird."

Verwenden Sie den erweiterten Journey-Ausdruckseditor, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Ausdrücke erstellt werden, wenn Journeys konfiguriert und verwendt werden oder eine Bedingung für die Datenquelle definiert wird.

Er ist auch immer dann verfügbar, wenn Sie Aktionsparameter definieren müssen, die bestimmte Datenmanipulationen erfordern. Sie können Daten aus den Ereignissen oder zusätzliche Informationen aus der Datenquelle nutzen. Bei einer Journey ist die angezeigte Liste der Ereignisfelder kontextbezogen und variiert entsprechend den Ereignissen, die in der Journey hinzugefügt werden.

![](../assets/journey65.png)


Der erweiterte Ausdruckseditor bietet eine Reihe integrierter Funktionen und Operatoren, mit denen Sie Werte bearbeiten und einen Ausdruck definieren können, der Ihren Anforderungen entspricht. Mit dem erweiterten Ausdruckseditor können Sie auch die Werte des Parameters für die externe Datenquelle definieren sowie Zuordnungsfelder und Sammlungen bearbeiten.

>[!NOTE]
>
>Die im erweiterten Journey-Ausdruckseditor verfügbaren Funktionen und Fähigkeiten unterscheiden sich von denen im [Personalisierungseditor](../../personalization/functions/functions.md).

## Zugreifen auf den erweiterten Ausdruckseditor {#accessing-the-advanced-expression-editor}

Der erweiterte Ausdruckseditor kann für folgende Aufgaben verwendet werden:

* Erstellen [erweiterter Bedingungen](../condition-activity.md#about_condition) für Datenquellen und Ereignisinformationen
* Definieren benutzerdefinierter [Warteaktivitäten](../wait-activity.md#custom)
* Definieren der Zuordnung von Aktionsparametern

Wenn möglich, können Sie mithilfe der Schaltfläche **[!UICONTROL Erweiterter Modus]** / **[!UICONTROL Einfacher Modus]** zwischen den beiden Modi wechseln. Der einfache Modus wird [hier](../condition-activity.md#about_condition) beschrieben.

>[!NOTE]
>
>* Bedingungen können im einfachen oder erweiterten Ausdruckseditor definiert werden. Sie geben immer einen booleschen Typ zurück.
>
>* Aktionsparameter können durch die Auswahl von Feldern oder über den erweiterten Ausdruckseditor definiert werden. Sie geben je nach Ausdruck einen bestimmten Datentyp zurück.

Sie können auf verschiedene Weise auf den erweiterten Ausdruckseditor zugreifen:

* Wenn Sie eine Bedingung für die Datenquelle erstellen, können Sie auf den erweiterten Editor zugreifen, indem Sie auf **[!UICONTROL Erweiterter Modus]** klicken.

  ![](../assets/journeyuc2_33.png)

* Wenn Sie einen benutzerdefinierten Timer erstellen, wird der erweiterte Editor direkt angezeigt.
* Wenn Sie Aktionsparameter zuordnen, klicken Sie auf **[!UICONTROL Erweiterter Modus]**.

## Entdecken Sie die Benutzeroberfläche {#discovering-the-interface}

In diesem Bildschirm können Sie Ihren Ausdruck manuell schreiben.

![](../assets/journey70.png)

Auf der linken Bildschirmseite werden die verfügbaren Felder und Funktionen angezeigt:

* **[!UICONTROL Ereignisse]**: Wählen Sie eines der Felder aus, die vom eingehenden Ereignis empfangen wurden. Die angezeigte Liste der Ereignisfelder ist kontextbezogen und variiert entsprechend den Ereignissen, die in der Journey hinzugefügt werden. [Weitere Informationen](../../event/about-events.md)

  >[!CAUTION]
  >
  >Das Erstellen von Ausdrücken mithilfe von Erlebnisereignissen wird nicht unterstützt. Alternative Ansätze und Best Practices zum Erstellen von Ausdrücken/Logik mit Erlebnisereignissen sind [hier](../../building-journeys/exp-event-lookup.md) zu finden

* **[!UICONTROL Zielgruppen]**: Wenn Sie ein **[!UICONTROL Zielgruppen-Qualifizierungsereignis]** eingefügt haben, wählen Sie die Zielgruppe aus, die in Ihrem Ausdruck verwendet werden soll. [Weitere Informationen](../condition-activity.md#using-a-segment)
* **[!UICONTROL Datenquellen]**: Wählen Sie aus der Liste der Felder aus, die in den Feldergruppen Ihrer Datenquellen verfügbar sind. [Weitere Informationen](../../datasource/about-data-sources.md)
* **[!UICONTROL Journey-Eigenschaften]**: Dieser Abschnitt gruppiert die technischen Felder neu, die mit der Journey für ein bestimmtes Profil verbunden sind. [Weitere Informationen](journey-properties.md)
* **[!UICONTROL Funktionen]**: Wählen Sie aus der Liste der integrierten Funktionen, die eine komplexe Filterung ermöglichen. Die Funktionen sind nach Kategorien geordnet. [Weitere Informationen](functions.md)

![](../assets/journey65.png)

Ein Mechanismus zur automatischen Vervollständigung zeigt kontextbezogene Vorschläge an.

![](../assets/journey68.png)

Ein Mechanismus zur Syntax-Validierung überprüft die Integrität Ihres Codes. Fehler werden über dem Editor angezeigt.

![](../assets/journey69.png)


>[!TIP]
>
>Stellen Sie beim Erstellen von Bedingungen im erweiterten Ausdruckseditor sicher, dass Ihre Ausdrücke keine ausgeblendeten oder nicht druckbaren Zeichen enthalten. Verwenden Sie außerdem einzeilige Ausdrücke, um Analysefehler zu vermeiden.


**Bedarf an Parametern beim Erstellen von Bedingungen mit dem erweiterten Ausdruckseditor**

Wenn Sie ein Feld aus einer externen Datenquelle auswählen, für das ein Parameter aufgerufen werden muss (siehe [diese Seite](../../datasource/external-data-sources.md)), wird rechts ein neuer Tab angezeigt, auf dem Sie den Parameter angeben können. Der Parameterwert kann aus den auf der Journey positionierten Ereignissen oder aus der Experience Platform-Datenquelle (und nicht aus anderen externen Datenquellen) stammen. In einer wetterbezogenen Datenquelle lautet der häufig verwendete Parameter beispielsweise „city“. Daher müssen Sie auswählen, wo Sie diesen Parameter „city“ abrufen möchten. Funktionen können auch auf Parameter angewendet werden, um Formatänderungen oder Verkettungen durchzuführen.

![](../assets/journeyuc2_19.png)

Bei komplexeren Anwendungsfällen können Sie, wenn Sie die Parameter der Datenquelle in den Hauptausdruck aufnehmen möchten, deren Werte mit dem Keyword „params“ definieren. Weitere Informationen finden Sie auf [dieser Seite](../expression/field-references.md).
