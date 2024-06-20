---
solution: Journey Optimizer
product: journey optimizer
title: Anpassbare Fragmente
description: Erfahren Sie, wie Sie Fragmente anpassen können, indem Sie einige ihrer Felder bearbeitbar machen.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: c84c09aac2d888c689591f2517269c88bee0cda6
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 0%

---


# Anpassbare Fragmente {#customizable-fragments}

Wenn Fragmente in einer Journey- oder Kampagnenaktion verwendet werden, sind sie standardmäßig aufgrund der Vererbung gesperrt. Das bedeutet, dass alle an einem Fragment vorgenommenen Änderungen automatisch an alle Kampagnen und Journey weitergegeben werden, in denen das Fragment verwendet wird. Mit anpassbaren Fragmenten können bestimmte Felder in einem Fragment als bearbeitbar definiert werden, wenn das Fragment einer Journey- oder Kampagnenaktion hinzugefügt wird. Angenommen, Sie haben ein Fragment mit einem Banner, Text und einer Schaltfläche. Sie können bestimmte Felder wie die Bild- oder Schaltflächen-Ziel-URL als bearbeitbar festlegen. Auf diese Weise können Benutzer diese Elemente ändern, wenn sie das Fragment in ihre Kampagne oder Journey integrieren, wodurch ein benutzerdefiniertes Erlebnis ohne Beeinträchtigung des ursprünglichen Fragments geboten wird.

Durch anpassbare Fragmente entfällt die Notwendigkeit, die Fragmentvererbung zu unterbrechen, wodurch zentralisierte Änderungen auf Fragmentebene zuvor an die Kampagnen und Journey weitergeleitet wurden. Dieser Ansatz ermöglicht es, Inhaltsabschnitte zum Zeitpunkt der Verwendung anzupassen, wodurch die Flexibilität geboten wird, Standardwerte mit kontextspezifischen Details zu überschreiben.

Durch die Nutzung anpassbarer Fragmente können Sie Ihre Inhalte effizient verwalten und personalisieren, ohne völlig neue Inhaltsbausteine zu erstellen oder die Vererbung vom ursprünglichen Fragment zu unterbrechen. Dadurch wird sichergestellt, dass auf Fragmentebene vorgenommene Änderungen weiterhin propagiert werden, während gleichzeitig eine erforderliche Anpassung auf Kampagnen- oder Journey-Ebene möglich ist.

Sowohl visuelle als auch Ausdrucksfragmente können als anpassbar markiert werden. Detaillierte Anweisungen zum weiteren Vorgehen mit den einzelnen Fragmenttypen finden Sie in den folgenden Abschnitten.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## Hinzufügen bearbeitbarer Felder in visuellen Fragmenten {#visual}

Gehen Sie wie folgt vor, um Teile eines visuellen Fragments bearbeitbar zu machen:

>[!NOTE]
>
>Bearbeitbare Felder können zu **image**, **text** und **button** Komponenten. Für **HTML** -Komponenten und bearbeitbaren Felder werden ähnlich wie Ausdrucksfragmente mithilfe des Personalisierungseditors hinzugefügt. [Erfahren Sie, wie Sie bearbeitbare Felder in HTML-Komponenten und Ausdrucksfragmenten hinzufügen.](#expression)

1. Öffnen Sie den Bildschirm zur Inhaltsbearbeitung des Fragments.

1. Wählen Sie die Komponente in Ihrem Fragment aus, in der Sie bearbeitbare Felder konfigurieren möchten.

1. Der Bereich für die Komponenteneigenschaften wird auf der rechten Seite geöffnet. Wählen Sie die **Bearbeitbare Felder** Registerkarte und dann umschalten **Bearbeitung aktivieren** -Option.

1. Alle Felder, die für die ausgewählte Komponente bearbeitet werden können, werden im Bereich aufgelistet. Die zur Bearbeitung verfügbaren Felder hängen vom ausgewählten Komponententyp ab.

   Im unten stehenden Beispiel erlauben wir die Bearbeitung der Schaltfläche &quot;Hier klicken&quot;-URL.

   ![](assets/fragment-param-enable.png)

1. Klicken Sie auf **Übersicht** , um alle bearbeitbaren Felder und deren Standardwerte zu überprüfen.

   In diesem Beispiel wird das Feld für die Schaltflächen-URL mit dem in der Komponente definierten Standardwert angezeigt. Dieser Wert kann von Benutzern angepasst werden, nachdem sie das Fragment zu ihrem Inhalt hinzugefügt haben.

   ![](assets/fragment-param-preview.png)

1. Wenn Sie fertig sind, speichern Sie Ihre Änderungen, um das Fragment zu aktualisieren.

1. Nach dem Hinzufügen des Fragments zu einer E-Mail können Benutzer alle im Fragment konfigurierten bearbeitbaren Felder anpassen. [Erfahren Sie, wie Sie bearbeitbare Felder in einem visuellen Fragment anpassen.](../email/use-visual-fragments.md#customize-fields)

## Hinzufügen bearbeitbarer Felder in HTML-Komponenten und Ausdrucksfragmenten {#expression}

Damit Teile einer HTML-Komponente oder eines Ausdrucksfragments bearbeitbar sind, müssen Sie eine bestimmte Syntax im Ausdruckseditor verwenden. Dazu gehört die Deklarierung einer **Variable** mit einem Standardwert, den Benutzer überschreiben können, nachdem sie das Fragment zu ihrem Inhalt hinzugefügt haben.

Angenommen, Sie möchten ein Fragment erstellen, das zu Ihren E-Mails hinzugefügt werden soll, und Benutzern ermöglichen, eine bestimmte Farbe anzupassen, die an verschiedenen Stellen verwendet wird, z. B. in Rahmen oder Schaltflächen-Hintergrundfarben. Bei der Erstellung des Fragments müssen Sie eine Variable mit einer **eindeutige ID**, beispielsweise &quot;Farbe&quot;und rufen Sie sie an den gewünschten Stellen im Fragmentinhalt auf, an denen Sie diese Farbe anwenden möchten. Beim Hinzufügen des Fragments zum Inhalt können Benutzer die Farbe anpassen, die überall dort verwendet wird, wo auf die Variable verwiesen wird.

Bei HTML-Komponenten können nur bestimmte Elemente zu bearbeitbaren Feldern werden. Erweitern Sie den Abschnitt unten für weitere Informationen.

+++Bearbeitbare Elemente in HTML-Komponenten:

Die folgenden Elemente können in einer HTML-Komponente zu bearbeitbaren Feldern werden:

* Ein Textteil
* Eine vollständige URL für Link oder Bild (funktioniert nicht mit dem Teil einer URL)
* Gesamte CSS-Eigenschaft (funktioniert nicht mit Teileigenschaft)

Im folgenden Code kann jedes rot hervorgehobene Element beispielsweise zu einer Eigenschaft werden:

![](assets/fragment-html.png){width="70%"}

+++

Gehen Sie wie folgt vor, um eine Variable zu deklarieren und sie in Ihrem Fragment zu verwenden:

1. Öffnen Sie das Ausdrucksfragment und bearbeiten Sie seinen Inhalt im Personalisierungs-Editor. Wählen Sie für HTML-Komponenten die Komponente im Fragment aus und klicken Sie auf die **Quellcode anzeigen** Schaltfläche.

   ![](assets/fragment-html-edit.png)

1. Deklarieren Sie die Variable, die Benutzer bearbeiten sollen. Navigieren Sie zum **Helper-Funktionen** im linken Navigationsbereich und fügen Sie die **inline** Helper-Funktion. Die Syntax zum Deklarieren und Aufrufen der Variablen wird automatisch in Ihren Inhalt eingefügt.

   ![](assets/fragment-add-helper.png)

1. Ersetzen `"name"` mit einer eindeutigen ID, um das bearbeitbare Feld zu identifizieren.

   >[!NOTE]
   >
   >Die Feld-ID muss eindeutig sein und darf keine Leerzeichen enthalten. Diese ID sollte überall in Ihrem Inhalt verwendet werden, wo der Wert der Variablen angezeigt werden soll.

1. Passen Sie die Syntax an Ihre Anforderungen an, indem Sie die in der folgenden Tabelle aufgeführten Parameter hinzufügen:

   | Aktion | Parameter | Beispiel |
   | ------- | ------- | ------- |
   | Deklarieren eines bearbeitbaren Felds mit einer **Standardwert**. Wenn Sie das Fragment zu Ihrem Inhalt hinzufügen, wird dieser Standardwert verwendet, wenn Sie es nicht anpassen. | Fügen Sie den Standardwert zwischen den Inline-Tags hinzu. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Definieren Sie eine **label** für das bearbeitbare Feld. Diese Bezeichnung wird in der E-Mail-Designer angezeigt, wenn die Fragmentfelder bearbeitet werden. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | Deklarieren Sie ein editierbares Feld mit einem **Bildquelle** die veröffentlicht werden müssen. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | Deklarieren Sie ein editierbares Feld mit einem **URL** , die verfolgt werden müssen.<br/>Beachten Sie, dass vordefinierte Bausteine &quot;URL der Mirrorseite&quot;und &quot;Link abmelden&quot;nicht zu bearbeitbaren Feldern werden können. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. Verwenden Sie die `{{{name}}}` -Syntax in Ihrem Code an jeder Stelle, an der Sie den Wert des bearbeitbaren Felds anzeigen möchten. Ersetzen `name` mit der eindeutigen Kennung des zuvor definierten Felds.

   ![](assets/fragment-call-variable.png)

1. Speichern Sie Ihr Fragment.

Beim Hinzufügen des Fragments zum E-Mail-Inhalt können Benutzer jetzt die Standardwerte der Variablen mit ihren ausgewählten Werten überschreiben:

* Für Ausdrucksfragmente wird eine bestimmte Syntax verwendet, um Variablenwerte zu überschreiben. [Erfahren Sie, wie Sie bearbeitbare Felder in einem Ausdrucksfragment anpassen.](../personalization/use-expression-fragments.md#customize-fields)

* Bei HTML-Komponenten wird die Variable in der Liste der bearbeitbaren Felder in der E-Mail-Designer angezeigt. [Erfahren Sie, wie Sie bearbeitbare Felder in einem visuellen Fragment anpassen.](../email/use-visual-fragments.md#customize-fields)

## Beispiel für ein bearbeitbares Ausdrucksfragment {#example}

Im folgenden Beispiel wird ein Ausdrucksfragment erstellt, das neue Sportkollektionen enthält. Standardmäßig zeigt das Fragment diesen Inhalt an: *Suchen Sie mehr? Verpassen Sie nicht unsere neueste Sportsammlung!*

Wir möchten Benutzern ermöglichen, &quot;Sport&quot;in diesem Inhalt durch den Sport ihrer Wahl zu ersetzen. Beispiel: *Suchen Sie mehr? Verpassen Sie nicht unsere neueste Yoga-Kollektion!*

Gehen Sie dazu wie folgt vor:

1. Deklarieren Sie eine &quot;sport&quot;-Variable mit der ID &quot;sport&quot;.

   Wenn Benutzer den Wert der Variablen nach dem Hinzufügen des Fragments nicht ändern, zeigt dies standardmäßig den Wert an, der zwischen der Variablen `{{#inline}}` und `{{/inline}}` Tags, d. h. &quot;Sport&quot;.

1. Fügen Sie die ``{{{sport}}}`` -Syntax im Fragmentinhalt verwenden, in der Sie den Variablenwert anzeigen möchten, d. h. standardmäßig &quot;Sport&quot;oder den von Benutzern ausgewählten Wert.

   ![](assets/fragment-expression-custom.png)

1. Beim Hinzufügen des Ausdrucksfragments zum Inhalt können Benutzer den Wert der Variablen direkt im Ausdruckseditor mit ihrer Auswahl ändern. [Erfahren Sie, wie Sie bearbeitbare Felder in einem Ausdrucksfragment anpassen.](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)
