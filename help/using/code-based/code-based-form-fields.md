---
title: Verwenden bearbeitbarer Formularfelder in Code-basierten Erlebnissen
description: Erfahren Sie, wie Sie bearbeitbare Felder zu Journey Optimizer-Code-basierten Erlebnis-Inhaltsvorlagen hinzufügen und wie Sie sie in Kampagnen oder Journey verwenden
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 5dd46ea8-acba-4c42-a65a-c18e45cba2cd
source-git-commit: 92247adabc56f369c9b11cdc519cdc7bf30c99f1
workflow-type: tm+mt
source-wordcount: '1218'
ht-degree: 18%

---

# Verwenden bearbeitbarer Formularfelder in Code-basierten Erlebnissen {#code-based-form-fields}

Um sowohl die Flexibilität zu erhöhen als auch die Kontrolle über die Code-basierten Erlebnisse zu verbessern, ermöglicht [!DNL Journey Optimizer] Ihrem Entwicklungs-Team die Erstellung von JSON- oder HTML-Inhaltsvorlagen mit bestimmten vordefinierten bearbeitbaren Feldern.

Beim Erstellen eines Code-basierten Erlebnisses können Marketing-Experten, die nicht technisch sind, diese Felder direkt in der Benutzeroberfläche bearbeiten, ohne den Personalisierungseditor öffnen oder andere Code-Elemente in ihrem Journey oder ihrer Kampagne berühren zu müssen.

Diese Funktion bietet Marketing-Benutzern ein vereinfachtes Erlebnis und ermöglicht Entwicklern gleichzeitig eine bessere Kontrolle über den Code-Inhalt, was zu weniger Spielraum für Fehler führt.

## Verstehen der Formularfeldsyntax {#form-field-syntax}

Um Teile einer HTML- oder JSON-Code-Payload bearbeitbar zu machen, müssen Sie eine bestimmte Syntax im Ausdruckseditor verwenden. Dazu gehört das Deklarieren einer **Variablen** mit einem Standardwert, den Benutzer überschreiben können, nachdem sie die Inhaltsvorlage auf ihr Code-basiertes Erlebnis angewendet haben.

Angenommen, Sie möchten eine Inhaltsvorlage erstellen, um sie auf Ihre Code-basierten Erlebnisse anzuwenden und Benutzern die Möglichkeit zu geben, eine bestimmte Farbe anzupassen, die an verschiedenen Stellen verwendet wird, z. B. in den Hintergrundfarben von Frames oder Schaltflächen.

Beim Erstellen Ihrer Inhaltsvorlage müssen Sie eine Variable mit einer **eindeutigen ID**, z. B. &quot;*color*, deklarieren und an den gewünschten Stellen im Inhalt aufrufen, an denen Sie diese Farbe anwenden möchten.

Wenn Benutzende die Inhaltsvorlage auf ihren Inhalt anwenden, können sie die Farbe anpassen, die dort verwendet wird, wo auf die Variable verwiesen wird.

## Hinzufügen bearbeitbarer Felder zu HTML- oder JSON-Inhaltsvorlagen {#add-editable-fields}

>[!CONTEXTUALHELP]
>id="ajo_cbe_preview_form_fields"
>title="Überprüfen des Renderings der Formularfelder"
>abstract="In JSON- oder HTML-Inhaltsvorlagen können Sie bestimmte bearbeitbare Felder definieren, die es technisch nicht versierten Benutzenden ermöglichen, Inhalte in Code-basierten Erlebnissen einfach und ohne Code-Änderungen zu bearbeiten. Erstellen Sie diese Felder mit der dedizierten Syntax und zeigen Sie sie mithilfe dieser Schaltfläche in der Vorschau an."

Damit ein Teil Ihres JSON- oder HTML-Codes bearbeitet werden kann, erstellen Sie zunächst ein Code-basiertes Erlebnis [Inhaltsvorlage](../content-management/content-templates.md) in dem Sie bestimmte Formularfelder definieren können.

>[!NOTE]
>
>Dieser Schritt wird in der Regel von einer Entwicklerrolle ausgeführt.

➡️ [In diesem Video erfahren Sie, wie Sie bearbeitbare Felder zu Code-basierten Erlebnisvorlagen hinzufügen](#video)

1. Erstellen Sie eine Inhaltsvorlage und wählen Sie den Kanal **[!UICONTROL Code-basiertes Erlebnis]** aus. [Erfahren Sie, wie Sie Vorlagen erstellen.](../content-management/create-content-templates.md)

1. Wählen Sie den Authoring-Modus aus: HTML oder JSON.

   >[!CAUTION]
   >
   >Das Ändern des Authoring-Modus führt zum Verlust des gesamten aktuellen Codes. Die auf dieser Vorlage basierenden Code-basierten Erlebnisse müssen denselben Autorenmodus verwenden.

1. Öffnen Sie den [Personalisierungseditor](../personalization/personalization-build-expressions.md), um Ihren Code-Inhalt zu bearbeiten.

1. Um ein bearbeitbares Formularfeld zu <!--To declare the variable you want users to edit-->, navigieren Sie zum Menü **[!UICONTROL Hilfsfunktionen]** im linken Navigationsbereich und fügen Sie das Attribut **inline** hinzu. Die Syntax zum Deklarieren und Aufrufen der Variablen wird automatisch in Ihren Inhalt eingefügt.

   ![](assets/cbe-template-helper-inline.png){width="85%"}

1. Ersetzen Sie `"name"` durch eine eindeutige ID, um das bearbeitbare Feld zu identifizieren. Geben Sie beispielsweise „imgURL“ ein.

   >[!NOTE]
   >
   >Die Feld-ID muss eindeutig sein und darf keine Leerzeichen enthalten. Diese ID sollte überall dort in Ihrem Inhalt verwendet werden, wo der Wert der Variablen angezeigt werden soll.

1. Passen Sie die Syntax an Ihre Anforderungen an, indem Sie die in der folgenden Tabelle aufgeführten Parameter hinzufügen:

   | Aktion | Parameter | Beispiel |
   | ------- | ------- | ------- |
   | Deklarieren eines bearbeitbaren Felds mit einem **Standardwert**. Beim Hinzufügen der Vorlage zu Ihrem Inhalt wird dieser Standardwert verwendet, wenn Sie ihn nicht anpassen. | Hinzufügen des Standardwerts zwischen den Inline-Tags. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Definieren eines **Labels** für das bearbeitbare Feld. Diese Beschriftung wird im Code-Editor beim Bearbeiten der Vorlagenfelder angezeigt. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |

   <!--
    | Action | Parameter| Example |
    | ------- | ------- | ------- |
    |Declare an editable field containing an **image source** that needs to be published.|`assetType="image"`|`{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}`|
    |Declare an editable field containing an **URL** that needs to be tracked.br/>Note that out-of-the-box "Mirror page URL" and "Unsubscribe link" predefined blocks cannot become editable fields.>|`assetType="url"`|`{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}`|
    -->

1. Klicken Sie **[!UICONTROL Formularfelder in Vorschau anzeigen]**, um zu überprüfen, wie die bearbeitbaren Formularfelder in den Code-basierten Erlebnissen angezeigt werden, die diese Vorlage anwenden.

   ![](assets/cbe-template-form-field-preview.png){width="85%"}

1. Verwenden Sie die Syntax `{{{name}}}` in Ihrem Code überall dort, wo der Wert des bearbeitbaren Felds angezeigt werden soll. Ersetzen Sie `name` durch die eindeutige ID des zuvor definierten Felds.

   ![](assets/cbe-template-call-variable.png){width="85%"}

1. Gehen Sie ähnlich vor, um weitere bearbeitbare Felder hinzuzufügen, indem Sie sie jeweils mit den Tags `{{#inline}}` und `{{/inline}}` einschließen.

1. Bearbeiten Sie den Rest Ihres Codes nach Bedarf, einschließlich der IDs, die den von Ihnen definierten bearbeitbaren Feldern entsprechen. [Weitere Informationen](create-code-based.md#edit-code)

   ![](assets/cbe-template-form-field-inline.png)

1. Speichern Sie Ihre Vorlage.

### Verwenden von Entscheidungsrichtlinien in bearbeitbaren Feldformularen {#decision-policy-in-form-fields}

Beim Erstellen einer Code-basierten Erlebnis-Inhaltsvorlage können Sie eine Entscheidungsrichtlinie verwenden, um Angebote in Ihren bearbeitbaren Formularfeldern zu nutzen.

1. Erstellen Sie eine Code-basierte Erlebnisvorlage wie oben [ beschrieben](#add-editable-fields).

1. Klicken Sie **[!UICONTROL Entscheidungsrichtlinie hinzufügen]** entweder über das Symbol **[!UICONTROL Entscheidungsrichtlinie anzeigen]** in der rechten Leiste des Bearbeitungsbildschirms oder im Abschnitt **[!UICONTROL Entscheidungsrichtlinie]** im linken Menü auf Ausdruckseditor.

   Wie Sie eine Entscheidungsrichtlinie erstellen, erfahren Sie in [diesem Abschnitt](../experience-decisioning/create-decision.md#add-decision).

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Richtlinie einfügen]**. Der Code, der der Entscheidungsrichtlinie entspricht, wird hinzugefügt.

   ![](assets/cbe-template-insert-policy.png)

1. Fügen Sie nach dem `{{#each}}`-Tag den Code ein, der den bearbeitbaren Formularfeldern entspricht, die Sie hinzufügen möchten, und verwenden Sie dabei die **inline**-Syntax [oben](#add-editable-fields). Ersetzen Sie `"name"` durch eine eindeutige ID, um Ihr bearbeitbares Feld zu identifizieren. Verwenden Sie in diesem Beispiel „title“.

   ![](assets/cbe-template-policy-inline.png){width="90%"}

1. Klicken Sie **[!UICONTROL Formularfelder in Vorschau anzeigen]**, um zu überprüfen, wie die bearbeitbaren Formularfelder in den Code-basierten Erlebnissen angezeigt werden, die diese Vorlage anwenden.

   ![](assets/cbe-template-policy-preview.png){width="70%"}

1. Fügen Sie den Rest Ihres Codes über dem `{{/each}}`-Tag ein. Verwenden Sie die `{{{name}}}` in Ihrem Code an jeder Stelle, an der Sie den Wert Ihres bearbeitbaren Felds anzeigen möchten. Ersetzen Sie in diesem Beispiel `name` durch „title“.

   ![](assets/cbe-template-policy-variable.png){width="85%"}

1. Speichern Sie Ihre Vorlage.

### Code-Beispiele {#code-examples}

Im Folgenden finden Sie einige Beispiele für JSON- und HTML-Vorlagen, darunter einige Entscheidungsrichtlinien.

**JSON-Vorlage:**

```
{{#inline "title" name="Title"}}Best gear for winter is here for you!{{/inline}} 
{{#inline "description" name="Description"}}Add description{{/inline}} 
{{#inline "imgURL" name="Image Link"}}Add link{{/inline}} 
{{#inline "number_of_items" name="Number of items"}}23{{/inline}}

{
  "title": "{{{title}}}",
  "description": "{{{description}}}",
  "imageUrl": "{{{imgURL}}}",
  "number_of_items": {{{number_of_items}}}, 
  "code": "DEFAULT"
}
```

>[!NOTE]
>
>Beim Referenzieren der Inline-Felder in der JSON-Payload:
>
>* Felder vom Typ Zeichenfolge müssen in doppelte Anführungszeichen gesetzt werden.
>* Ganzzahlen oder boolesche Werte dürfen NICHT in doppelte Anführungszeichen gesetzt werden. (Siehe das Feld `number_of_items` im obigen Beispiel.)

**JSON-Vorlage mit Decisioning:**

```
{ 
"offer": [ 
{{#each decisionPolicy.fff709b7-7fef-4e4e-83d7-594fbcf196c1.items as |item|}} 
{{#inline "title" name="Title"}}{{item._mobiledx.Title1}}{{/inline}} {{#inline "description" name="Description"}}{{item._mobiledx.Title2}}{{/inline}} {{#inline "imgURL" name="Image Link"}}https://luma.enablementadobe.com/content/luma/us/en/experience/warming-up/_jcr_content/root/hero_image.coreimg.jpeg{{/inline}} 

{ 
"title": "{{{title}}}", 
"description": "{{{description}}}", 
"imageUrl": "{{{imgURL}}}", 
"link": "https://lumaenablement.adobe.com/web/luma/home", "code": "DEFAULT" 
}, 
{{/each}}
] 
}
```

>[!NOTE]
>
>Inline-Felder, für die Sie Entscheidungselemente verwenden möchten, müssen innerhalb des Entscheidungsrichtlinienblocks zwischen den Tags `{{#each}}` und `{{/each}}` platziert werden.

**HTML-Vorlage:**

```
{{#inline "title" name="Title"}}Please enter title here{{/inline}} 
{{#inline "imgSrc" name="Image link"}}{{/inline}} 

<div class="TopRibbon__content"><img style="padding: 5px 10px;" class="TopRibbon__image" src="{{{imgSrc}}}" />{{{title}}}</div> 
<style> .theme-luma .TopRibbon { background-color: #200098; }</style>
```

**HTML-Vorlage mit Entscheidungsfindung:**

```
{{#each decisionPolicy.f112884a-5654-43ad-9d6d-dbd32ae23ee6.items as |item|}} 
{{#inline "title" name="Title"}}Title is: {{item._mobiledx.Title1}}{{/inline}} 

<div class="TopRibbon__content"><img style="padding: 5px 10px;" class="TopRibbon__image" src="{{item._mobiledx.HeroBannerImage.sourceURL}}" />{{{title}}}</div> 
<style> .theme-luma .TopRibbon { background-color: #200098; }</style> 

{{/each}}
```

## Bearbeiten von Formularfeldern in einem Code-basierten Erlebnis {#edit-form-fields}

>[!CONTEXTUALHELP]
>id="ajo_code_based_form_fields"
>title="Was sind Formularfelder?"
>abstract="Dieses Code-basierte Erlebnis enthält Formularfelder, die Sie einfach bearbeiten können, ohne Code im Personalisierungseditor bearbeiten zu müssen."

Nachdem die Inhaltsvorlage mit vordefinierten bearbeitbaren Formularfeldern erstellt wurde, können Sie mit dieser Inhaltsvorlage ein Code-basiertes Erlebnis erstellen.

Sie können die Formularfelder einfach von einer Code-basierten Erlebnis-Journey oder Kampagne bearbeiten, ohne den Personalisierungseditor öffnen zu müssen.

>[!NOTE]
>
>Dieser Schritt wird in der Regel von einer Marketing-Rolle ausgeführt.

1. Wählen Sie auf dem Bildschirm Journey-Aktivität oder Kampagnenbearbeitung die Inhaltsvorlage aus, die bearbeitbare Formularfelder enthält. [Informationen zur Verwendung von Inhaltsvorlagen](../content-management/use-content-templates.md)

   ![](assets/cbe-campaign-apply-template.png){width="60%"}

   >[!CAUTION]
   >
   >Die verfügbaren Vorlagen werden je nach zuvor ausgewählter Kanalkonfiguration entweder auf HTML oder auf JSON angewendet. Es werden nur kompatible Vorlagen angezeigt.

1. Die Felder, die in der ausgewählten Inhaltsvorlage vordefiniert waren, sind im rechten Bereich verfügbar. <!--The code preview is displayed with the rest of the code.-->

   ![](assets/cbe-campaign-form-fields.png)

1. Im Abschnitt **[!UICONTROL Bearbeitbare Formularfelder]** haben Sie folgende Möglichkeiten:

   * Bearbeiten Sie jeden Wert direkt in den bearbeitbaren Feldern, ohne den Code-Editor zu öffnen.

   ![](assets/cbe-campaign-form-fields-edit.png){width="60%"}

   * Klicken Sie auf das Personalisierungssymbol, um jedes Feld mit dem [Code-Editor“ ](../personalization/personalization-build-expressions.md) bearbeiten.

   ![](assets/cbe-campaign-form-fields-edit-perso.png){width="70%"}

   >[!NOTE]
   >
   >In beiden Fällen können Sie jeweils nur ein Feld und nicht den Rest des Code-basierten Erlebnisinhalts bearbeiten.

1. Wenn [ Inhaltsvorlage eine ](#decision-policy-in-form-fields)Entscheidungsrichtlinie“ hinzugefügt wurde, enthält sie alle im [Angebotskatalogschema“ verfügbaren Attribute](../experience-decisioning/catalogs.md). Sie können das Entscheidungselement inline oder mit dem Ausdruckseditor bearbeiten.

1. Um den Rest des Codes zu bearbeiten, klicken Sie auf die Schaltfläche **[!UICONTROL Code bearbeiten]** und aktualisieren Sie Ihre gesamten Code-basierten Erlebnisinhalte, einschließlich der bearbeitbaren Formularfelder. [Weitere Informationen](create-code-based.md#edit-code)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie bearbeitbare Felder zu Code-basierten Inhaltsvorlagen von Erlebniskanälen hinzufügen.

>[!VIDEO](https://video.tv.adobe.com/v/3463990/?learn=on&#x26;enablevpops)
