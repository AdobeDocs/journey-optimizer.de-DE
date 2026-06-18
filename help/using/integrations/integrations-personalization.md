---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden externer Integrationen
description: Integrieren Sie externe Integrationen in den Prozess der Kanalerstellung, um Inhalte mit personalisierten und dynamischen Informationen anzureichern, einschließlich der Antworten der Adobe Target-Bereitstellungs-API
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: Integration
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: d16f7424-4847-4b90-a37c-4b52cbdabee5
source-git-commit: bfb28a935dffca7c381fe72339abc840d2ab297b
workflow-type: tm+mt
source-wordcount: 842
ht-degree: 19%

---


# Verwenden externer Integrationen für die Personalisierung {#integrations-personalization}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Marketing-Experten konfigurierte Integrationen anwenden, um E-Mail-, SMS- und Push-Inhalte zu personalisieren und einen API-Aufruf an einen anderen zu verketten, um umfangreicheres und dynamisches Messaging zu ermöglichen.

>[!ENDSHADEBOX]

Bevor Sie externe Integrationen in Ihren Inhalten verwenden, bestätigen Sie, dass ein Administrator jede Integration **konfiguriert und aktiviert** (Endpunkt, Authentifizierung, Richtlinien, Antwort-Payload und Aktivierung) hat, wie in [Arbeiten mit Integrationen](integrations.md) beschrieben.

Sie können bis zu **3** Integrationen pro **[!UICONTROL Fragment]** und bis zu **5** der Nachricht hinzufügen. Integrationen, die nur aus Fragmenten stammen, werden nicht für die **5** gezählt.

## Anwenden der Integrationspersonalisierung auf Ihre Inhalte {#apply-integration-personalization}

Als Marketing-Fachleute können Sie konfigurierte Integrationen verwenden, um Ihre Inhalte zu personalisieren. Führen Sie folgende Schritte aus:

1. Greifen Sie auf Ihren Kampagneninhalt zu und klicken Sie in Ihren Text- oder HTML-**[!UICONTROL Komponenten]** auf **[!UICONTROL Personalisierung hinzufügen]**.

   [Weitere Informationen zu Komponenten](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Navigieren Sie zum Abschnitt **[!UICONTROL Integrationen]** und klicken Sie auf **[!UICONTROL Integrationen öffnen]**, um alle aktiven Integrationen anzuzeigen.

   Beachten Sie, dass **Journey Optimizer-Fragmente** für Integrationen verfügbar sind, aber nur ausgehende Kanäle unterstützen. Nach der Veröffentlichung eines Fragments ist das Hinzufügen und Speichern neuer Integrationen deaktiviert, um Auswirkungen auf bestehende Journey und Kampagnen zu vermeiden.

   ![](assets/external-integration-content-2.png)

1. Wählen Sie eine Integration aus und klicken Sie auf **[!UICONTROL Speichern]**.

   ![](assets/external-integration-content-3.png)

1. Aktivieren Sie den **[!UICONTROL Pillen-Modus]**, um das erweiterte Integrationsmenü zu entsperren.

   ![](assets/external-integration-content-4.png)

1. Wenn Sie die Integrationspersonalisierung erstellen, enthält der Integrations-Helper ein **`required`**, das definiert, wie Fehler oder fehlende Daten mit Standardinhalten interagieren:

   * **`required=true`** (Standard): Das Rendern dieser Nachricht wird angehalten. Der Versand wird mit **`ExternalDataLookupExclusion`** ausgeschlossen und dieser Ausschluss wird im **Nachrichten-Feedback-Datensatz“**.
   * **`required=false`**: Die Ergebnisvariable wird auf **`null`** festgelegt und das Rendern wird fortgesetzt. Verwenden Sie Standardtext, Fallbacks oder bedingte Logik in Ihrer Vorlage, damit Profile keine leeren Inhalte erhalten, wenn die Integration keine Daten zurückgibt.

     ![](assets/external-integration-content-8.png)

1. Um die Einrichtung der Integration abzuschließen, definieren Sie die Integrationsattribute, die zuvor bei der [Konfiguration](integrations.md#configure) angegeben wurden.

   Sie können diesen Attributen Werte zuweisen – entweder mithilfe statischer Werte, die konstant bleiben, oder mithilfe von Profilattributen, die Informationen dynamisch aus Benutzerprofilen abrufen.

   ![](assets/external-integration-content-5.png)

1. Sobald die Integrationsattribute definiert sind, können Sie die Integrationsfelder in Ihren Inhalten für personalisierte Nachrichten verwenden, indem Sie auf das Symbol ![Hinzufügen](assets/do-not-localize/Smock_Add_18_N.svg) klicken.

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >Token in Ihrer Vorlage dürfen nur Felder verwenden, die der Administrator in der Integrationskonfiguration bereitgestellt hat. Beispielsweise ist `{{weatherResponse.temperature}}` gültig, wenn `temperature` verfügbar gemacht wird; `{{weatherResponse.humidity}}` wird im Editor abgelehnt, wenn `humidity` nicht verfügbar ist.

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Ihre Integrationspersonalisierung wird jetzt erfolgreich auf Ihre Inhalte angewendet, sodass alle Empfängerinnen und Empfänger ein maßgeschneidertes, relevantes Erlebnis erhalten, das auf den von Ihnen konfigurierten Attributen basiert.

![](assets/external-integration-content-7.png)

## Einen API-Aufruf einem anderen zuordnen {#map-integration-chain}

Sie können Integrationen verketten, sodass die Ergebnisse eines Aufrufs an den nächsten weitergeleitet werden, z. B. Pfadsegmente, Kopfzeilen oder Abfrageparameter. Die Aufrufe werden in der richtigen Reihenfolge in derselben Nachricht ausgeführt, was eine umfassendere Personalisierung ohne benutzerdefinierten Code unterstützt.

Bevor Sie beginnen, stellen Sie Folgendes sicher:

* Ein Administrator hat jede benötigte Integration konfiguriert und aktiviert. Siehe [Konfigurieren der Integration](integrations.md).
* Platzhalter, Kopfzeilen und Abfrageparameter für Variablenpfade werden in der Integrationskonfiguration mit Marketer-orientierten Kennzeichnungen eingerichtet.
* Der Administrator legte die Antwortfelder offen, die Sie für jede Integration in der **[!UICONTROL Antwort-Payload]** benötigen, damit sie beim Authoring angezeigt werden.

Im folgenden Beispiel wird eine Reservierungsintegration verwendet, die eine Flugnummer aus der Buchung des Profils zurückgibt, dann eine Fluginformationsintegration, die diese Nummer für den Live-Status (Verspätungen, Ziel) verwendet. Sie ordnen die Eingaben der zweiten Integration der Antwort des ersten Aufrufs zu.

1. Öffnen Sie Ihre Nachricht oder Ihr Fragment und öffnen Sie den Personalisierungseditor.

   ![](assets/uc-integrations-1.png)

1. Klicken **[!UICONTROL unter]** auf **[!UICONTROL Integrationen öffnen]**.

   ![](assets/uc-integrations-2.png)

1. Fügen Sie die Integration hinzu, deren Antwort den nächsten Aufruf bedient, z. B. Reservierungs- oder Buchungsdaten, die die Flugkennung enthalten.

   ![](assets/uc-integrations-3.png)

1. (Optional) Öffnen Sie das Menü **[!UICONTROL Hilfsfunktion]** und fügen Sie einen Helper hinzu, z. B. die `Let`-Funktion, wenn Sie eine benannte Variable an die Reservierungsantwort binden möchten.

   >[!NOTE]
   >
   > Es sind nur Felder verfügbar, die in der vom Administrator definierten **[!UICONTROL Antwort-Payload]** verfügbar sind. Sie können nicht auf Eigenschaften verweisen, die in der Konfiguration nicht bereitgestellt wurden.

1. Wenn Sie eine Hilfsvariable verwenden, ordnen Sie diese Variable dem Feld zu, das die Reservierungsintegration für die nachgelagerte Verwendung zurückgibt, z. B. die Flugnummer in der Passagier- oder Buchungs-Payload.

   ![](assets/uc-integrations-4.png)

1. Fügen Sie im **[!UICONTROL Integrationen öffnen]** die zweite Integration hinzu, z. B. „Flugstatus“.

   ![](assets/uc-integrations-5.png)

1. Öffnen Sie in der zweiten Integration **[!UICONTROL Integrationsattribute]**. Wählen Sie für jede Eingabe, die Daten aus dem ersten Aufruf wiederverwenden muss, z. B. eine Pfadvariable, Kopfzeile oder Abfrageparameter, eine Zuordnungsquelle aus der ersten Integrationsantwort aus.

   Beim **[!UICONTROL Pillen]**-Erlebnis können Sie die Ausgabe des ersten Aufrufs direkt der Eingabe des zweiten Aufrufs ohne `Let`-Anweisung zuordnen. Wenn Sie `Let` verwendet haben, können Sie stattdessen diese Variable zuordnen.

   ![](assets/uc-integrations-6.png)

1. Fügen Sie Token aus der zweiten Integration mit dem Steuerelement ![add](assets/do-not-localize/Smock_Add_18_N.svg) in Ihren Inhalt ein, z. B. Ziel aus der Fluginformationsantwort.

   ![](assets/uc-integrations-8.png)

1. Speichern Sie Ihren Inhalt.

Beim **[!UICONTROL Simulieren]** oder Senden führt Journey Optimizer Integrationen der Reihe nach aus: Der erste Aufruf verwendet den konfigurierten Profilkontext und das Ergebnis erstellt die zweite Anfrage. Ob eine bestimmte Integration zur Simulations- oder Sendezeit ausgeführt wird, hängt von Ihrer Einrichtung und Ihrem Kanal ab.

![](assets/uc-integrations-7.png)

<!--
## Use Adobe Target data in templates {#use-adobe-target-in-templates}

This section explains how to use **Integrations** in Adobe Journey Optimizer to fetch personalization data from **[!DNL Adobe Target]** at send time and use it in message templates. It assumes the Target Delivery API has already been configured as an integration.

For configuration steps, see [Work with Integrations](integrations.md) and the [Adobe Target Recommendations](vendor-integration.md#adobe-target-recommendations) sample.

The Target Delivery API returns a `prefetch.mboxes` array. Each mbox includes an `options` object with `content` and `type` fields. The `type` value determines how you use `content` in your template. Open the tab that matches your mbox response, then follow the steps to use that data in your message.

>[!BEGINTABS]

>[!TAB JSON content]

When `type` is `json`, the `content` field is a **JSON string**. Parse it before you access nested fields. The example below shows a typical Delivery API response for a JSON mbox.

```json
{
  "status": 200,
  "prefetch": {
    "mboxes": [
      {
        "index": 0,
        "name": "SummerOffer",
        "options": {
          "content": "{\"recommendations\":[{\"productId\":\"p101\",\"name\":\"Noise Smartwatch\",\"price\":2999},{\"productId\":\"p205\",\"name\":\"Boat Earbuds\",\"price\":1499}],\"strategy\":\"collaborative-filtering\"}",
          "type": "json"
        }
      }
    ]
  }
}
```

Use three helpers in sequence to fetch, extract, and parse the Target response.

1. **Fetch the Target response.** Call your configured Target integration with `externalDataLookup`. Set `integrationName` to the **[!UICONTROL Name]** of that integration (replace the example placeholder `target_recommendations`). Use the `result` parameter to name the template variable that holds the full Delivery API payload—for example, `targetResponse`.

    ```handlebars
    {{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
    ```

1. **Extract a specific mbox using valueAtPath.** `valueAtPath` extracts an element from an array by its 0-based index and assigns it to a template variable. Use the `idx` parameter to specify which element to access.

    ```handlebars
    {{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
    ```

    | Parameter | Description |
    | --- | --- |
    | `path` | Path to the array (positional, no keyword) |
    | `idx` | 0-based index for array access (optional) |
    | `result` | Variable name to store the extracted value |

    >[!NOTE]
    >
    > If `idx` is out of bounds, rendering throws an exception. Guard invalid indexes with `{%#if idx >= 0 and idx < count(targetResponse.prefetch.mboxes)%}` when the index may be invalid. PQL expressions cannot be used as the path. **Available since release 2025.9.0.**

1. **Parse the JSON string using parseJson.** The mbox `options.content` field is a raw JSON string. `parseJson` converts it into a structured object whose fields can then be accessed directly in the template.

    ```handlebars
    {{parseJson jsonStr=summerOffer.options.content result="summerOfferContent"}}
    ```

    | Parameter | Description |
    | --- | --- |
    | `jsonStr` | Path to the string field containing valid JSON |
    | `result` | Variable name to store the parsed object |

    >[!NOTE]
    >
    > If the JSON string is invalid or the reference is null, `result` is set to `null` — no rendering error is thrown. Test with your actual Target response to confirm the content is valid JSON. **Available since: 2026.6.0**

1. **Access the data.** Once parsed, use dot notation to access fields from `summerOfferContent`. To render a list of recommendations:

    ```handlebars
    {{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
    {{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
    {{parseJson jsonStr=summerOffer.options.content result="summerOfferContent"}}

    Strategy: {{summerOfferContent.strategy}}
    {{#each summerOfferContent.recommendations as |rec|}}
      {{rec.name}} — {{rec.price}}
    {{/each}}
    ```

>[!TAB HTML content]

When `type` is `html`, the `content` field is a ready-to-render HTML string. You do not need to parse it. The example below shows a typical Delivery API response for an HTML mbox.

```json
{
  "status": 200,
  "prefetch": {
    "mboxes": [
      {
        "index": 0,
        "name": "SummerOffer",
        "options": {
          "content": "<div class=\"offer\"><h2>Summer Sale</h2><p>50% off Smartwatch</p></div>",
          "type": "html"
        }
      }
    ]
  }
}
```

Fetch and extract the mbox, then render `content` directly. Skip `parseJson`.

```handlebars
{{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
{{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
{{{summerOffer.options.content}}}
```

>[!NOTE]
>
> Use **triple braces** `{{{...}}}` to render HTML content as-is. Double braces `{{...}}` will escape HTML entities and render raw tag strings instead of the HTML.

>[!ENDTABS]

-->

## Anleitungsvideo {#video}

In diesem Video wird gezeigt, wie **Integrationen** Adobe Journey Optimizer mit externen APIs verbinden, damit Sie Live-Daten und -Inhalte in **ausgehende** Kanäle, E-Mail, SMS und Push-Benachrichtigungen übertragen können, um eine relevantere Personalisierung zu erzielen.

>[!VIDEO](https://video.tv.adobe.com/v/3484127/?captions=ger&learn=on)
