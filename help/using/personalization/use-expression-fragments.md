---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Ausdrucksfragmenten
description: Erfahren Sie, wie Sie im Personalisierungseditor von  [!DNL Journey Optimizer]  Ausdrucksfragmente verwenden können.
feature: Personalization, Fragments
topic: Personalization
role: Developer
level: Intermediate
keywords: Ausdruck, Editor, Bibliothek, Personalisierung
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
TQID: https://experienceleague.adobe.com/0N5waBGElHBnlsk1pHhKT8roaly-A6srIjb3UPIDNqY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 2174
ht-degree: 60%

---

# Nutzen von Ausdrucksfragmenten {#use-expression-fragments}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Ausdrucksfragmente im Personalisierungseditor einfügen und wiederverwenden, mit impliziten Variablen arbeiten, Fragmente in Schleifen verwenden, bearbeitbare Felder anpassen und die Vererbung in Adobe Journey Optimizer aufheben.

>[!ENDSHADEBOX]

Bei Verwendung des **Personalisierungseditors** können Sie alle Ausdrucksfragmente nutzen, die in der aktuellen Sandbox erstellt oder gespeichert wurden.

Ein Fragment ist eine wiederverwendbare Komponente, die in [!DNL Journey Optimizer]-Kampagnen und -Journeys referenziert werden kann. Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, mit denen Marketing-Fachleute Inhalte schnell in einem verbesserten Design-Prozess zusammenstellen können. [Erfahren Sie mehr über Fragmente](../content-management/fragments.md)

➡️ [In diesem Video erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden](../content-management/fragments.md#video-fragments)

## Verwenden eines Ausdrucksfragments {#use-expression-fragment}

Um Ausdrucksfragmente zu Ihren Inhalten hinzuzufügen, gehen Sie folgendermaßen vor.

>[!NOTE]
>
>Sie können für einen Versand bis zu 30 Fragmente hinzufügen. Fragmente können nur bis zu einer Ebene verschachtelt werden.

1. Öffnen Sie den [Personalisierungseditor](personalization-build-expressions.md) und wählen Sie die Schaltfläche **[!UICONTROL Fragmente]** im linken Bereich aus.

   In der Liste werden alle Ausdrucksfragmente angezeigt, die in der aktuellen Sandbox als Fragmente erstellt oder gespeichert wurden. [Erfahren Sie, wie Sie Fragmente erstellen](../content-management/create-fragments.md)
Sie sind nach Erstellungsdatum sortiert: Kürzlich hinzugefügte Ausdrucksfragmente werden in der Liste zuerst angezeigt.

   ![](assets/expression-fragments-pane.png)

   Sie können diese Liste auch aktualisieren.

   >[!NOTE]
   >
   >Wenn einige Fragmente während der Bearbeitung des Inhalts geändert oder hinzugefügt wurden, wird die Liste mit den neuesten Änderungen aktualisiert.

1. Klicken Sie auf das Symbol „+“ neben einem Ausdrucksfragment, um die entsprechende Fragment-ID in den Editor einzufügen.

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >Sie können jeden **Entwurf** und jedes **Live-Fragment** zu Ihrem Inhalt hinzufügen. Sie können Ihre Journey oder Kampagne jedoch nicht aktivieren, wenn darin ein Fragment mit dem Status **Entwurf** verwendet wird. Bei der Veröffentlichung einer Journey oder Kampagne wird bei Fragmententwürfen ein Fehler angezeigt. Sie müssen sie erst genehmigen, um sie veröffentlichen zu können.

1. Wenn die Fragment-ID einmal hinzugefügt worden ist, werden die Änderungen synchronisiert, sobald Sie das entsprechende Ausdrucksfragment öffnen und [bearbeiten](../content-management/manage-fragments.md#edit-fragments). Sie werden automatisch an alle Entwürfe oder Live-Journeys/Kampagnen übertragen, die diese Fragment-ID enthalten.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Mehr Aktionen]** neben einem Fragment. Wählen Sie aus dem sich öffnenden Kontextmenü die Option **[!UICONTROL Fragment anzeigen]** aus, um weitere Informationen zu diesem Fragment zu erhalten. Die **[!UICONTROL Fragment-ID]** wird ebenfalls angezeigt und kann von hier aus kopiert werden.

   ![](assets/expression-fragment-view.png)

1. Sie können das Ausdrucksfragment in einem anderen Fenster öffnen, um seinen Inhalt und seine Eigenschaften zu bearbeiten – entweder im Kontextmenü mithilfe der Option **[!UICONTROL Fragment öffnen]** oder im Bereich **[!UICONTROL Fragmentinformationen]**. [Erfahren Sie, wie ein Fragment bearbeitet wird](../content-management/manage-fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Anschließend können Sie Ihre Inhalte wie gewohnt mit allen Personalisierungs- und Authoring-Funktionen des [Personalisierungseditors](personalization-build-expressions.md) anpassen und validieren.

1. In einigen Fällen müssen Sie nur Variablen berechnen. Daher können Sie den Inhalt des Ausdrucksfragments ausblenden. Verwenden Sie dazu das Attribut `render` und legen Sie es auf `false` fest. Beispiel:

   ```
   Hi {{profile.person.name.firstName|fragment id='ajo:fragmentId/variantId' mode ='inline' render=false}}
   ```

>[!NOTE]
>
>Wenn Sie ein Ausdrucksfragment erstellen, das mehrere Zeilenumbrüche enthält, und dieses in [SMS](../mobile/create-mobile-message.md#sms-content)- oder [Push](../push/design-push.md)-Inhalten verwenden, bleiben die Zeilenumbrüche erhalten. Testen Sie daher Ihre [SMS](../mobile/send-mobile-message.md)- oder [Push](../push/send-push.md)-Nachricht vor dem Versand.

## Verwenden implizierter Variablen {#implicit-variables}

Die impliziten Variablen verbessern die vorhandene Fragmentfunktion, um die Effizienz der Wiederverwendbarkeit und Skripterstellung von Inhalten zu verbessern. Fragmente können Eingabevariablen verwenden und Ausgabevariablen erstellen, die in Kampagnen- und Journey-Inhalten verwendet werden können.

Diese Funktion kann beispielsweise verwendet werden, um Tracking-Parameter Ihrer E-Mails basierend auf der aktuellen Kampagne oder Journey zu initialisieren und diese Parameter in den personalisierten Links zu verwenden, die zum E-Mail-Inhalt hinzugefügt werden.

Folgende Anwendungsfälle sind möglich:

1. **Verwenden Sie Eingabevariablen in einem Fragment.**

   Wenn ein Fragment im Inhalt einer Kampagnen-/Journey-Aktion verwendet wird, kann es Variablen nutzen, die außerhalb des Fragments deklariert wurden. Es folgt ein Beispiel:

   ![](../personalization/assets/variable-in-a-fragment.png)

   Oben sehen Sie, dass die Variable `utm_content` im Kampagneninhalt deklariert ist. Wenn das Fragment **Hero block** verwendet wird, wird ein Link angezeigt, an den der Parameterwert `utm_content` angehängt wird. Das Ergebnis lautet: `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`.

1. **Verwenden Sie Ausgabevariablen aus einem Fragment.**

   In einem Fragment berechnete oder definierte Variablen können in Ihren Inhalten verwendet werden. Im folgenden Beispiel deklariert ein Fragment **F1** einen Variablensatz:

   ![](../personalization/assets/personalize-with-variables.png)

   Ein E-Mail-Inhalt kann die folgende Personalisierung aufweisen:

   ![](../personalization/assets/use-fragment-variable.png)

   Das Fragment F1 initialisiert die folgenden Variablen: `utm_campaign`und `utm_content`. Dann werden dem Link im Nachrichteninhalt diese Parameter angehängt. Das Ergebnis lautet: `https://luma.enablementadobe.com?utm_campaign= Product_launch&utm_content= start_shopping`.

>[!NOTE]
>
>Zur Laufzeit erweitert das System, was sich in Fragmenten befindet, und interpretiert dann den Personalisierungs-Code von oben nach unten. Unter Berücksichtigung dieser Tatsache können komplexere Anwendungsfälle erreicht werden. Sie können beispielsweise ein Fragment F1 Variablen an ein anderes Fragment F2 übergeben lassen, das darunter sitzt. Sie können auch ein visuelles Fragment F1 Variablen an ein verschachteltes Ausdrucksfragment F2 übergeben lassen.

## Verwenden von Ausdrucksfragmenten in Schleifen {#fragments-in-loops}

Bei der Verwendung von Ausdrucksfragmenten in `{{#each}}`-Schleifen ist die Variablenauswahl von entscheidender Bedeutung. Ausdrucksfragmente können auf globale Variablen zugreifen, die im Nachrichteninhalt definiert sind, sie können jedoch keine schleifenspezifischen Variablen als Parameter empfangen.

### Unterstützte Muster: Verwenden globaler Variablen {#global-variables-in-loops}

Ausdrucksfragmente können auf globale Variablen verweisen, die außerhalb des Fragments definiert sind, selbst wenn das Fragment aus einer Schleife heraus aufgerufen wird. Dies ist der empfohlene Ansatz, wenn Sie Fragmente in iterativen Kontexten verwenden müssen.

**Beispiel: Verwenden eines Fragments mit globalen Variablen in einer Schleife**

Definieren Sie in Ihrem Nachrichteninhalt eine globale Variable und verwenden Sie ein Fragment, das darauf verweist:

```handlebars
{% let globalDiscount = 15 %}

{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Price: ${{product.price}}</p>
    {{fragment id='ajo:fragment123/variant456' mode='inline'}}
  </div>
{{/each}}
```

Im Ausdrucksfragment (fragment123) können Sie auf die Variable `globalDiscount` verweisen:

```handlebars
<p class="discount-info">Save {{globalDiscount}}% on all items!</p>
```

Dieses Muster funktioniert, weil die globale Variable in der gesamten Nachricht verfügbar ist, auch in Fragmenten, unabhängig vom Schleifenkontext.

### Nicht unterstützt: Übergeben von Schleifenvariablen als Fragmentparameter {#loop-variables-limitations}

Sie können das aktuelle Iterationselement (z. B. `product` im obigen Beispiel) nicht als Parameter an ein Ausdrucksfragment übergeben. Das Fragment kann aus dem umgebenden `{{#each}}`-Block nicht direkt auf Variablen im Schleifenbereich zugreifen.

**Beispiel: Was NICHT funktioniert**

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <!-- This will NOT work as expected -->
  {{fragment id='ajo:fragment123/variant456' mode='inline' currentProduct=product}}
{{/each}}
```

Das Fragment kann nicht `product` als Parameter empfangen und intern verwenden, da die Parameterübergabe für schleifenspezifische Variablen in der aktuellen Implementierung nicht unterstützt wird.

### Empfohlene Problemumgehungen {#fragments-in-loops-workarounds}

Wenn Sie Ausdrucksfragmente mit Daten aus einer Schleife verwenden müssen, sollten Sie die folgenden Ansätze berücksichtigen:

1. **Einfügen von Logik direkt in die Nachricht:** Statt ein Fragment für eine schleifenspezifische Logik zu verwenden, fügen Sie den Personalisierungs-Code direkt in Ihrem `{{#each}}`-Block ein.

   ```handlebars
   {{#each context.journey.actions.GetProducts.items as |product|}}
     <div class="product">
       <h3>{{product.name}}</h3>
       <p>Price: ${{product.price}}</p>
       {{#if product.price > 100}}
         <span class="premium-badge">Premium Product</span>
       {{/if}}
     </div>
   {{/each}}
   ```

2. **Verwenden von Fragmenten außerhalb von Schleifen:** Wenn der Fragmentinhalt nicht schleifenabhängig ist, rufen Sie das Fragment vor oder nach dem Iterationsblock auf.

   ```handlebars
   {{fragment id='ajo:fragment123/variant456' mode='inline'}}
   
   {{#each context.journey.actions.GetProducts.items as |product|}}
     <div class="product">
       <h3>{{product.name}}</h3>
       <p>Price: ${{product.price}}</p>
     </div>
   {{/each}}
   ```

3. **Festlegen mehrerer globaler Variablen:** Wenn Sie verschiedene Werte an ein Fragment über mehrere Iterationen hinweg übergeben müssen, legen Sie vor jedem Fragmentaufruf globale Variablen fest (obwohl dies die Flexibilität einschränkt).

>[!NOTE]
>
>Informationen zum Iterieren über kontextuelle Daten und zum Arbeiten mit Schleifen finden Sie im umfassenden Leitfaden zum [Iterieren über kontextuelle Daten](iterate-contextual-data.md) mit Best Practices, Tipps zur Fehlerbehebung und erweiterten Mustern.

## Anpassen bearbeitbarer Felder {#customize-fields}

Wenn bestimmte Teile eines Ausdrucksfragments mithilfe von Variablen bearbeitbar gemacht wurden, können Sie deren Standardwerte mithilfe einer speziellen Syntax überschreiben. [Informationen dazu, wie Sie Ihre Fragmente anpassbar machen können](../content-management/customizable-fragments.md)

Gehen Sie wie folgt vor, um die Felder anzupassen:

1. Fügen Sie das Fragment über das Menü **[!UICONTROL Fragmente]** in ihren Code ein.

1. Verwenden Sie den Code `<fieldId>="<value>"` am Ende der Syntax, um den Standardwert der Variablen zu überschreiben.

   Im folgenden Beispiel wird der Wert einer Variablen, deren ID „sports“ lautet, mit dem Wert „Yoga“ überschrieben. Dadurch wird „Yoga“ überall dort in Ihrem Fragmentinhalt angezeigt, wo auf die Variable „sport“ verwiesen wird.

   ![](../content-management/assets/fragment-expression-use.png)

Ein Beispiel für das Hinzufügen von bearbeitbaren Feldern zu einem Ausdrucksfragment und zum Überschreiben ihrer Werte beim Erstellen einer E-Mail finden Sie in [diesem Abschnitt](../content-management/customizable-fragments.md#example).

## Dynamische Fragmentauflösung verwenden {#dynamic-resolution}

Anstatt eine Fragment-ID zur Entwurfszeit statisch einzubetten, können Sie die Fragment-ID zur Laufzeit pro Empfänger dynamisch auflösen. Dadurch können verschiedene Profile innerhalb derselben Kampagne oder Journey völlig unterschiedliche Inhaltsblöcke empfangen, die auf Profilattributen, Datensatzsuchen oder Kontextdaten basieren.

[Erfahren Sie, wie Sie dynamische Fragmente verwenden](../content-management/dynamic-fragments.md)

## Unterbrechen der Vererbung {#break-inheritance}

Beim Hinzufügen einer Fragment-ID zum Personalisierungseditor werden die Änderungen am ursprünglichen Ausdrucksfragment synchronisiert.

Sie können jedoch auch den Inhalt eines Ausdrucksfragments in den Editor einfügen. Wählen Sie im Kontextmenü die Option **[!UICONTROL Fragment einfügen]** aus, um diesen Inhalt einzufügen.

![](assets/expression-fragment-paste.png)

In diesem Fall ist die Vererbung aus dem ursprünglichen Fragment fehlerhaft. Der Inhalt des Fragments wird in den Editor kopiert und die Änderungen werden nicht mehr synchronisiert.

Es wird zu einem eigenständigen Element, das nicht mehr mit dem ursprünglichen Fragment verknüpft ist. Sie können es wie jedes andere Element in Ihrem Code bearbeiten.

## Kurzübersicht {#quick-reference}

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

>[!BEGINTABS]

>[!TAB Übersicht]

**TL;DR**

Auf dieser Seite wird erläutert, wie Sie Ausdrucksfragmente im Personalisierungseditor einfügen, anpassen und verwalten können - einschließlich impliziter Variablen, der Verwendung von Fragmenten in Schleifen, bearbeitbarer Felder, dynamischer Auflösung und Unterbrechungen der Vererbung.

**Intents**

* Einfügen eines Ausdrucksfragments aus dem Menü Fragmente und Grundlegendes zur automatischen Übertragung von Änderungen
* Verwenden impliziter Variablen: Eingabevariablen (außerhalb des Fragments deklariert, innerhalb verwendet) und Ausgabevariablen (innerhalb des Fragments deklariert, im Nachrichteninhalt verwendet)
* Verwenden von Ausdrucksfragmenten in Schleifen - Nutzen Sie globale Variablen für den Fragmentzugriff; verstehen Sie die Einschränkung bei der Übergabe von Variablen im Schleifenbereich als Parameter
* Überschreiben bearbeitbarer Felder in einem anpassbaren Fragment mithilfe `<fieldId>="<value>"` Syntax
* Dynamisches Auflösen von Fragment-IDs zur Laufzeit basierend auf Profilattributen, Datensatzsuchen oder Kontextdaten
* Unterbrechen der Vererbung durch Einfügen des Fragmentinhalts direkt in den Editor

>[!TAB Glossar]

* **Ausdrucksfragment**: Eine wiederverwendbare Ausdruckskomponente für Personalisierung, auf die über Kampagnen und Journey hinweg von der ID verwiesen wird. Änderungen am Fragment werden automatisch auf alle darauf verweisenden Inhalte übertragen. *(produktspezifisch)*
* **Implizite Variablen**: Variablen, die die Fragmentfunktionalität erweitern - Eingabevariablen (deklariert im Kampagnen-/Journey-Inhalt, genutzt innerhalb des Fragments) und Ausgabevariablen (deklariert innerhalb des Fragments, verfügbar im umgebenden Nachrichteninhalt). *(produktspezifisch)*
* **Eingabevariable**: Eine Variable, die außerhalb des Fragments (im Kampagnen- oder Journey-Inhalt) deklariert wurde und auf die das Fragment intern verweisen und sie verwenden kann.
* **Ausgabevariable**: Eine innerhalb eines Fragments deklarierte oder berechnete Variable, die für die Verwendung im umgebenden Nachrichteninhalt verfügbar wird, nachdem das Fragment aufgerufen wurde.
* **Bearbeitbare Felder**: Fragmentvariablen, die bereitgestellt werden, damit der einfügende Benutzer Standardwerte mithilfe `<fieldId>="<value>"` Syntax überschreiben kann, ohne die Fragmentquelle zu bearbeiten. *(produktspezifisch)*
* **Dynamische Fragmentauflösung**: Die Möglichkeit, zur Laufzeit eine Fragment-ID aufzulösen (basierend auf Profilattributen, Datensatzsuchen oder Kontextdaten), anstatt zur Entwurfszeit eine statische Fragment-ID einzubetten. *(produktspezifisch)*
* **Vererbung unterbrechen**: Mit „Fragment einfügen“ im Kontextmenü wird der Inhalt des Fragments als eigenständiges Element in den Editor kopiert, das nicht mehr mit dem ursprünglichen Fragment synchronisiert wird. *(produktspezifisch)*

>[!TAB Terminologie]

* **Kanonischer Name:** Ausdrucksfragment — Varianten: Fragment, Ausdrucksfragment
* **Synonyme:** „fragment ID“ = die Kennung, die verwendet wird, um das Fragment in Ausdrücken zu referenzieren
* **Nicht verwechseln:** Einfügen eines Fragments nach ID (referenziert; Änderungen werden automatisch auf alle Inhalte übertragen) ≠ Unterbrechen der Vererbung/Einfügen des Fragments (Inhalt in den Editor kopiert; eigenständiges Element, nicht mehr mit Original verknüpft)
* **Verwechseln Sie nicht** Eingabevariablen (deklariert außerhalb des Fragments, konsumiert innerhalb) ≠ Ausgabevariablen (deklariert innerhalb des Fragments, konsumiert außerhalb im umgebenden Nachrichteninhalt)
* **Nicht verwechseln:** Entwurfsfragment (kann zum Inhalt hinzugefügt werden, blockiert jedoch die Journey-/Kampagnenveröffentlichung bis zur Genehmigung) ≠ Live-Fragment (vollständig veröffentlicht; sicher für aktive Journey und Kampagnen)

>[!TAB Leitplanken und Einschränkungen]

* Pro Versand können maximal 30 Fragmente hinzugefügt werden.
* Fragmente können nur bis zu einer Ebene verschachtelt werden.
* Eine Journey oder Kampagne kann nicht aktiviert oder veröffentlicht werden, wenn sie ein Fragment mit dem Status Entwurf enthält. Entwurfsfragmente müssen vor der Veröffentlichung genehmigt werden.
* Ausdrucksfragmente können keine Variablen mit Schleifenumfang (das aktuelle `{{#each}}` Iterationselement) als Parameter empfangen. Dies ist eine bekannte Einschränkung. Verwenden Sie globale Variablen oder Inline-Logik als Problemumgehung.
* Wenn ein Fragment, das mehrere Zeilenumbrüche enthält, in SMS- oder Push-Inhalten verwendet wird, werden Zeilenumbrüche beibehalten. Testen Sie den Inhalt vor dem Senden.

>[!TAB FAQs]

**F: Wie viele Fragmente können in einem Versand hinzugefügt werden?**

Bis zu 30 Fragmente.

**F: Können Fragmente in anderen Fragmenten verschachtelt werden?**

Ja, aber nur bis zu einer Verschachtelungsebene.

**F: Was passiert, wenn ich ein Entwurfsfragment in einer Journey oder Kampagne verwende?**

Sie können ein Entwurfsfragment zu Inhalten hinzufügen, die Journey oder Kampagne jedoch erst aktivieren oder veröffentlichen, wenn das Fragment genehmigt wurde und sich sein Status in Live ändert.

**F: Kann ein Ausdrucksfragment das aktuelle Schleifenelement (z. B. `product` in `{{#each}}`) als Parameter empfangen?**

Nein. Ausdrucksfragmente können keine Variablen im Schleifenbereich als Parameter empfangen. Verwenden Sie globale Variablen, die außerhalb der Schleife deklariert wurden (auf die das Fragment zugreifen kann), oder schließen Sie die Personalisierungslogik direkt in die Schleife ein, anstatt ein Fragment zu verwenden.

**F: Was bedeutet eine Unterbrechung der Vererbung und wann sollte ich sie verwenden?**

Eine Unterbrechung der Vererbung bedeutet, dass „Fragment einfügen“ aus dem Kontextmenü verwendet wird, um den Inhalt des Fragments direkt in den Editor zu kopieren. Der eingefügte Inhalt wird zu einem eigenständigen Element, das nicht mehr mit dem ursprünglichen Fragment synchronisiert wird - verwenden Sie diese Option, wenn Sie den Inhalt über das hinaus anpassen müssen, was bearbeitbare Felder zulassen, da Sie wissen, dass zukünftige Änderungen am ursprünglichen Fragment nicht an diese Kopie weitergegeben werden.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 64745ff0 -->

