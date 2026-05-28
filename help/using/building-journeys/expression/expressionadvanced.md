---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit dem erweiterten Ausdruckseditor
description: Erfahren Sie, wie Sie erweiterte Ausdrücke erstellen
feature: Journeys
role: Developer
level: Experienced
keywords: Ausdruckseditor, Daten, Journey
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/8RsF-CRRrsLiCzwsaqfJQnWcyy6frmKkdSJBKnIhGgE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: ac5d9310-7772-40fb-9d78-864562e1bfd6id: e51e8901-97d9-4f7d-a835-503025a90e32id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 716
ht-degree: 100%

---

# Arbeiten mit dem erweiterten Ausdruckseditor {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Informationen zum erweiterten Ausdruckseditor"
>abstract="Der erweiterte Ausdruckseditor kann verwendet werden, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Sie Ausdrücke erstellen, wenn Sie Journeys konfigurieren und verwenden oder eine Datenquellenbedingung definieren."

Verwenden Sie den erweiterten Journey-Ausdruckseditor, um in verschiedenen Bildschirmen der Benutzeroberfläche erweiterte Ausdrücke zu erstellen. Beispielsweise können Sie Ausdrücke erstellen, wenn Sie Journeys konfigurieren und verwenden oder eine Datenquellenbedingung definieren.

Er ist auch immer dann verfügbar, wenn Sie Aktionsparameter definieren müssen, die bestimmte Datenmanipulationen erfordern. Sie können Daten aus den Ereignissen oder zusätzliche Informationen aus der Datenquelle nutzen. Bei einer Journey ist die angezeigte Liste der Ereignisfelder kontextbezogen und variiert entsprechend den Ereignissen, die in der Journey hinzugefügt werden.

![](../assets/journey65.png)


Der erweiterte Ausdruckseditor bietet eine Reihe integrierter Funktionen und Operatoren, mit denen Sie Werte bearbeiten und einen Ausdruck definieren können, der Ihren Anforderungen entspricht. Mit dem erweiterten Ausdruckseditor können Sie auch die Werte des Parameters für die externe Datenquelle definieren sowie Zuordnungsfelder und Sammlungen bearbeiten.

>[!NOTE]
>
>Die im erweiterten Journey-Ausdruckseditor verfügbaren Funktionen und Fähigkeiten unterscheiden sich von denen im [Personalisierungseditor](../../personalization/functions/functions.md).

## Zugreifen auf den erweiterten Ausdruckseditor {#accessing-the-advanced-expression-editor}

Der erweiterte Ausdruckseditor kann für folgende Aufgaben verwendet werden:

* Erstellen [erweiterter Bedingungen](../conditions.md#data_source_condition) für Datenquellen und Ereignisinformationen
* Definieren benutzerdefinierter [Warteaktivitäten](../wait-activity.md#custom)
* Definieren der Zuordnung von Aktionsparametern

Wenn möglich, können Sie mithilfe der Schaltfläche **[!UICONTROL Erweiterter Modus]** / **[!UICONTROL Einfacher Modus]** zwischen den beiden Modi wechseln. Der einfache Modus wird [hier](../conditions.md#about_condition) beschrieben.

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

* **[!UICONTROL Zielgruppen]**: Wenn Sie ein **[!UICONTROL Zielgruppen-Qualifizierungsereignis]** eingefügt haben, wählen Sie die Zielgruppe aus, die in Ihrem Ausdruck verwendet werden soll. [Weitere Informationen](../conditions.md#using-a-segment)
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
