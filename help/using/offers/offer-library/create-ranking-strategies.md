---
product: experience platform
solution: Experience Platform
title: Erstellen von Rangfolgestrategien
description: Erfahren Sie, wie Sie KI-Modelle erstellen, um Angebote zu reihen
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: f5627a23ceb0d00dd01db8766e72fed1b5d652a3
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 94%

---

# Erstellen von KI-Modellen {#ai-rankings}

[!DNL Journey Optimizer] ermöglicht Ihnen die Erstellung von **AI-Modelle** , um Angebote nach Ihren Geschäftszielen zu ordnen.

>[!CAUTION]
>
>Zum Erstellen, Bearbeiten oder Löschen von KI-Modellen benötigen Sie die **Verwalten von Ranking Strategies** Berechtigung. [Weitere Informationen](../../administration/high-low-permissions.md#manage-ranking-strategies)
>
>Einigen ausgewählten Benutzern wird derzeit vorab Zugriff auf die Verwendung der KI-Modelle gewährt.

Sobald ein KI-Modell erstellt wurde, können Sie dieses einer Platzierung in einer Entscheidung zuweisen. Weitere Informationen dazu finden Sie unter [Konfigurieren der Angebotsauswahl in Entscheidungen](../offer-activities/configure-offer-selection.md).

## Erstellen einer Rangfolgestrategie {#create-ranking-strategy}

Gehen Sie wie folgt vor, um ein KI-Modell als Ranking-Strategie zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Komponenten]** auf und wählen Sie dann die Registerkarte **[!UICONTROL KI-Rangfolgen]** aus.

   ![](../assets/ai-ranking-list.png)

   Alle bisher erstellten Rangfolgestrategien werden aufgelistet.

1. Klicken Sie auf den Button **[!UICONTROL Strategie erstellen]**.

1. Füllen Sie die folgenden Felder aus:

   ![](../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**: Eindeutiger Name, den Sie angeben müssen.

   * **[!UICONTROL Modelltyp]**: Derzeit wird in [!DNL Journey Optimizer] nur der Modelltyp **[!UICONTROL Automatische Optimierung]** unterstützt. [Weitere Informationen](ai-ranking.md#auto-optimization)

   * **[!UICONTROL Optimierungsmetrik]**:

      Mit dieser Option können Marketer auswählen, wie das Modell für maschinelles Lernen erstellt und trainiert werden soll: basierend auf den angezeigten Angeboten, auf in E-Mails angeklickten Angeboten und/oder auf im Internet angeklickten Angeboten.

      >[!NOTE]
      >
      >Sie können bei Bedarf alle Metriktypen auswählen.

      Es gibt zwei Arten von Optimierungsmetriken:
      * **[!UICONTROL Impression]**: Derzeit entsprechen Impressionsereignisse allen angezeigten Angeboten.
      * **[!UICONTROL Konversion]**: Konversionsereignisse entsprechen allen Angeboten, die zu Klicks per E-Mail oder Internet führen.

      Alle ausgewählten Impressionsereignisse und/oder Konversionsereignisse werden automatisch mit dem bereitgestellten Web SDK oder dem Mobile SDK erfasst. Weiterführende Informationen dazu finden Sie in der [Übersicht über das Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de).

   * **[!UICONTROL Datensatz-ID]**: Für die Konversion müssen Sie einen Datensatz in der Dropdown-Liste auswählen, in dem Ereignisse gesammelt werden. In [diesem Abschnitt](#create-dataset) erfahren Sie, wie Sie einen solchen Datensatz erstellen.<!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >In der Dropdown-Liste werden nur Datensätze angezeigt, die aus Schemas erstellt wurden, die mit der Feldergruppe (früher als Mixin bezeichnet) **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft sind.

1. Speichern und aktivieren Sie die Rangfolgestrategie.

   ![](../assets/ai-ranking-save-activate.png)

Sie kann nun bei der Entscheidung über die Rangfolge der für eine Platzierung geeigneten Angebote verwendet werden. Weiterführende Informationen finden Sie in diesem [Abschnitt](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->.

## Datensatz zum Erfassen von Ereignissen erstellen {#create-dataset}

Sie müssen einen Datensatz erstellen, in dem Konversionsereignisse erfasst werden. Erstellen Sie zunächst das Schema, das in Ihrem Datensatz verwendet werden soll:

1. Wählen Sie im Menü **[!UICONTROL Daten-Management]** die Option **[!UICONTROL Schema]** aus, wechseln Sie zur Registerkarte **[!UICONTROL Durchsuchen]** und klicken Sie auf **[!UICONTROL Schema erstellen]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Wählen Sie **[!UICONTROL XDM ExperienceEvent]** aus.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    Weitere Informationen zu XDM-Schemas und Feldergruppen finden Sie in der [Dokumentation zur XDM-Systemübersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de).


1. Geben Sie im Feld **[!UICONTROL Suche]** „Interaktion mit Vorschlägen“ ein und wählen Sie die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** aus.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    Mit dem Schema, das in Ihrem Datensatz verwendet wird, muss die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft sein. Andernfalls können Sie es nicht in Ihrer Rangfolgestrategie verwenden.

1. Klicken Sie auf **[!UICONTROL Feldergruppen hinzufügen]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Die Feldergruppen wurden früher als Mixins bezeichnet.

1. Geben Sie einen Namen ein und speichern Sie das Schema.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Erfahren Sie mehr über das Erstellen von Schemas in [Grundlagen der Schemakomposition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de?lang=de#understanding-schemas).

Sie können jetzt einen Datensatz unter Verwendung dieses Schemas erstellen. Gehen Sie dazu wie folgt vor:

1. Wählen Sie im Menü **[!UICONTROL Daten-Management]** die Option **[!UICONTROL Datensätze]** aus, wechseln Sie zur Registerkarte **[!UICONTROL Durchsuchen]** und klicken Sie auf **[!UICONTROL Datensatz erstellen]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Wählen Sie **[!UICONTROL Datensatz aus Schema erstellen]** aus.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Wählen Sie das soeben erstellte Schema aus der Liste aus.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Klicken Sie auf **[!UICONTROL Weiter]**.

1. Geben Sie im Feld **[!UICONTROL Name]** einen eindeutigen Namen für den Datensatz ein und klicken Sie auf **[!UICONTROL Beenden]**.

   ![](../assets/ai-ranking-dataset-name.png)

Der Datensatz kann jetzt ausgewählt werden, um Ereignisdaten zu erfassen, wenn [eine Rangfolgestrategie erstellt wird](#create-ranking-strategy).

## Anforderungen an Angebotsschemas {#schema-requirements}

An dieser Stelle müssen Sie:

* die Rangfolgestrategie erstellt haben,
* definiert haben, welcher Ereignistyp erfasst werden soll – angezeigtes Angebot (Impression) und/oder angeklicktes Angebot (Konversion),
* und definiert haben, in welchem Datensatz Sie die Ereignisdaten erfassen möchten.

Jedes Mal, wenn ein Angebot angezeigt und/oder angeklickt wird, soll das entsprechende Ereignis automatisch von der Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** mithilfe des [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=de#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;} oder Mobile SDK erfasst werden.

Um Ereignistypen (angezeigtes Angebot oder angeklicktes Angebot) senden zu können, müssen Sie für jeden Ereignistyp in einem Erlebnisereignis, das an Adobe Experience Platform gesendet wird, den richtigen Wert festlegen. Im Folgenden finden Sie die Schemaanforderungen, die Sie in Ihren JavaScript-Code implementieren müssen:

### Szenario mit angezeigtem Angebot

**Ereignistyp:** `decisioning.propositionDisplay`
**Quelle:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Aufnahme
+++**Beispiel-Payload:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

+++

### Szenario mit angeklicktem Angebot

**Ereignistyp:** `decisioning.propositionInteract`
**Quelle:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Aufnahme
+++**Beispiel-Payload:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->

