---
title: Verwenden von Entscheidungsrichtlinien in Nachrichten
description: Erfahren Sie, wie Sie Entscheidungsrichtlinien in Ihren Nachrichten verwenden.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 95%

---

# Verwenden von Entscheidungsrichtlinien in Nachrichten {#create-decision}

Nachdem eine Entscheidungsrichtlinie erstellt wurde, können die Richtlinie und die mit den zurückgegebenen Entscheidungselementen verknüpften Attribute in Ihrem Inhalt für die Personalisierung verwendet werden. Dazu muss der mit der Entscheidungsrichtlinie verknüpfte Code zunächst in Ihren Inhalt eingefügt werden. Anschließend können Sie die zugehörigen Attribute für die Personalisierung nutzen.

## Einfügen des Entscheidungsrichtlinien-Codes {#insert-code}

>[!BEGINTABS]

>[!TAB Code-basiertes Erlebnis]

1. Öffnen Sie den Personalisierungseditor und rufen Sie das Menü **[!UICONTROL Entscheidungsrichtlinie]** auf.

1. Klicken Sie auf **[!UICONTROL Richtlinie einfügen]**, um den Code hinzuzufügen, der der Entscheidungsrichtlinie entspricht. 

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Wenn die Schaltfläche zum Einfügen von Code nicht angezeigt wird, wurde möglicherweise bereits eine Entscheidungsrichtlinie für die übergeordnete Komponente konfiguriert.

1. Der Code für die Entscheidungsrichtlinie wird hinzugefügt. Diese Sequenz wird so oft wiederholt, wie Sie die Entscheidungsrichtlinie zurückgeben möchten. Wenn Sie beispielsweise bei der [Erstellung der Entscheidung](#add-decision) 2 Elemente zurückgeben möchten, wird dieselbe Sequenz zweimal wiederholt.

>[!TAB E-Mail]

1. Öffnen Sie den Personalisierungseditor und rufen Sie das Menü **[!UICONTROL Entscheidungsrichtlinie]** auf.

1. Klicken Sie auf **[!UICONTROL Syntax einfügen]**, um den Code hinzuzufügen, der der Entscheidungsrichtlinie entspricht. 

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Wenn die Schaltfläche zum Einfügen von Code nicht angezeigt wird, wurde möglicherweise bereits eine Entscheidungsrichtlinie für die übergeordnete Komponente konfiguriert.

1. Wenn der Komponente noch keine Platzierung zugeordnet wurde, wählen Sie eine Platzierung aus der Liste aus und klicken Sie auf **[!UICONTROL Zuweisen]**.

   ![](assets/decision-policy-placement.png)

>[!ENDTABS]

Nachdem der Code für die Entscheidungsrichtlinie hinzugefügt wurde, wird diese Sequenz so oft wiederholt, wie oft Sie möchten, dass die Entscheidungsrichtlinie zurückgegeben wird. Wenn Sie beispielsweise bei der [Erstellung der Entscheidung](#add-decision) 2 Elemente zurückgeben möchten, wird dieselbe Sequenz zweimal wiederholt.

## Verwenden von Attributen von Entscheidungselementen {#attributes}

Jetzt können Sie alle gewünschten Entscheidungsattribute zu diesem Code hinzufügen.  Die verfügbaren Attribute werden im Schema des Katalogs **[!UICONTROL Angebote]** gespeichert. Benutzerdefinierte Attribute werden im Ordner **`_<imsOrg`>** und Standardattribute im Ordner **`_experience`** gespeichert. [Weitere Informationen zum Schema des Angebotskatalogs](catalogs.md)

![](assets/decision-code-based-decision-attributes.png)

>[!NOTE]
>
>Für das Tracking von Entscheidungsrichtlinienelementen muss das Attribut `trackingToken` wie folgt dem Inhalt der Entscheidungsrichtlinie hinzugefügt werden:
>`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

Klicken Sie auf das Symbol „+“ neben einem Attribut, um es hinzuzufügen. Sie können beliebig viele Attribute zum Code hinzufügen.

![](assets/decision-code-based-add-decision-attributes.png)

Die `#each`-Schleife muss in ein Paar eckige Klammern `[ ]` eingeschlossen sein und und direkt vor der schließenden `/each` muss ein Komma eingefügt werden.

![](assets/decision-code-based-wrap-code.png)

Sie können auch jedes beliebige Attribut hinzufügen, das im Personalisierungseditor verfügbar ist, z. B. Profilattribute.

![](assets/decision-code-based-decision-profile-attribute.png)

## Nutzen von Fragmenten (Code-basiertes Erlebnis) {#fragments}

Wenn Ihre Entscheidungsrichtlinie Entscheidungselemente einschließlich Fragmenten enthält, können Sie diese Fragmente im Entscheidungsrichtlinien-Code nutzen. [Erfahren Sie mehr über Fragmente](../content-management/fragments.md)

>[!CAUTION]
>
>Diese Funktion ist derzeit nur für den Code-basierten Erlebniskanal verfügbar.
>
>Derzeit können nur [Ausdrucksfragmente](../personalization/use-expression-fragments.md) verwendet werden. Verschachtelte Fragmente (Fragmente, die auf andere Fragmente verweisen) werden nicht unterstützt.

Angenommen, Sie möchten verschiedene Inhalte für mehrere Mobilgerätemodelle anzeigen. Stellen Sie sicher, dass Sie Fragmente, die diesen Geräten entsprechen, zu dem Entscheidungselement hinzugefügt haben, das Sie in der Entscheidungsrichtlinie verwenden. [Weitere Informationen](items.md#attributes).

![](assets/item-fragments.png){width=70%}

Anschließend können Sie eine der folgenden Methoden verwenden:

>[!BEGINTABS]

>[!TAB Code direkt einfügen]

Kopieren Sie einfach den unten stehenden Code-Block in den Entscheidungsrichtlinien-Code. Ersetzen Sie `variable` durch die Fragment-ID und `placement` durch den Fragmentverweisschlüssel:

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB Befolgen Sie die detaillierten Schritte]

1. Navigieren Sie zu den **[!UICONTROL Hilfsfunktionen]** und fügen Sie die **Let**-Funktion `{% let variable = expression %} {{variable}}` zum Code-Bereich hinzu, in dem Sie die Variable für Ihr Fragment deklarieren können.

   ![](assets/decision-let-function.png)

1. Verwenden Sie die auf **Map** > **Get** basierende Funktion `{%= get(map, string) %}`, um Ihren Ausdruck zu erstellen. Die Zuordnung ist das Fragment, auf das im Entscheidungselement verwiesen wird, und die Zeichenfolge kann das Gerätemodell sein, das Sie im Entscheidungselement als **[!UICONTROL Fragmentverweisschlüssel]** eingegeben haben.

   ![](assets/decision-map-function.png)

1. Sie können auch ein kontextuelles Attribut verwenden, das diese Gerätemodell-ID enthält.

   ![](assets/decision-contextual-attribute.png)

1. Fügen Sie die Variable hinzu, die Sie für Ihr Fragment als Fragment-ID ausgewählt haben.

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

Die Fragment-ID und der Referenzschlüssel werden später im Abschnitt **[!UICONTROL Fragmente]** des Entscheidungselements ausgewählt.

>[!WARNING]
>
>Wenn der Fragmentschlüssel falsch oder der Fragmentinhalt ungültig ist, schlägt das Rendern fehl und verursacht einen Fehler im Edge-Aufruf.

### Leitlinien bei der Verwendung von Fragmenten {#fragments-guardrails}

**Entscheidungselement- und Kontextattribute**

Entscheidungselementattribute und kontextuelle Attribute werden in [!DNL Journey Optimizer] Fragmenten nicht standardmäßig unterstützt. Sie können jedoch stattdessen globale Variablen verwenden, wie unten beschrieben.

Angenommen, Sie möchten die Variable *sport* in Ihrem Fragment verwenden.

1. Verweisen Sie auf diese Variable im Fragment, z. B.:

   ```
   Elevate your practice with new {{sport}} gear!
   ```

1. Definieren Sie die Variable mit der Funktion **Let** im Entscheidungsrichtlinienblock. Im folgenden Beispiel wird *sport* mit dem Entscheidungsattribut definiert:

   ```
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

**Inhaltsvalidierung von Entscheidungselementfragmenten**

* Aufgrund der Dynamik dieser Fragmente wird bei Verwendung in einer Kampagne die Nachrichtenvalidierung während der Erstellung des Kampagneninhalts für Fragmente übersprungen, auf die in Entscheidungselementen verwiesen wird.

* Die Validierung des Fragmentinhalts erfolgt nur während der Erstellung und Veröffentlichung des Fragments.

* Im Fall von JSON-Fragmenten wird die Gültigkeit des JSON-Objekts nicht sichergestellt. Stellen Sie sicher, dass der Ausdrucksfragmentinhalt ein gültiger JSON-Inhalt ist, damit er in Entscheidungselementen verwendet werden kann.

Zur Laufzeit wird der Kampagneninhalt (einschließlich des Fragmentinhalts aus Entscheidungselementen) validiert. Im Falle eines Validierungsfehlers wird die Kampagne nicht gerendert.

## Nächste Schritte {#final-steps}

Sobald Ihr Inhalt fertig ist, überprüfen und veröffentlichen Sie Ihre Kampagne oder Journey:

* [Veröffentlichen einer Journey](../building-journeys/publish-journey.md)
* [Überprüfen und Aktivieren einer Kampagne](../campaigns/review-activate-campaign.md)
* [Veröffentlichen und Aktivieren eines Code-basierten Erlebnisses](../code-based/publish-code-based.md)

Sobald Ihre Entwickelnden bei Code-basierten Erlebnissen einen API- oder SDK-Aufruf zum Abrufen von Inhalten für die in Ihrer Kanalkonfiguration definierte Oberfläche starten, werden die Änderungen auf Ihre Web-Seite oder App angewendet.

>[!NOTE]
>
>Derzeit können Sie in einer Kampagne oder Journey mit [Code-basiertem Erlebnis](../code-based/create-code-based.md) keine Inhalte über die Benutzeroberfläche mithilfe von Entscheidungen simulieren. Eine Problemumgehung finden Sie in [diesem Abschnitt ](../code-based/code-based-decisioning-implementations.md).

Um zu sehen, wie Ihre Entscheidungen funktionieren, können Sie benutzerdefinierte [Reporting-Dashboards für Customer Journey Analytics](cja-reporting.md) erstellen.

