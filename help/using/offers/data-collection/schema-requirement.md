---
product: experience platform
solution: Experience Platform
title: Konfigurieren der Ereigniserfassung
description: Erfahren Sie, wie Sie Ihr Angebotsschema zur Erfassung von Ereignissen konfigurieren
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 34d30a4c45f007da6197999dbf1d0b283fba8248
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 79%

---

# Konfigurieren der Datenerfassung {#schema-requirements}

Um zu anderen Ereignistypen als Entscheidungsereignissen Feedback erhalten zu können, müssen Sie für jeden Ereignistyp in einem **Erlebnisereignis**, das an Adobe Experience Platform gesendet wird, den richtigen Wert festlegen.

>[!CAUTION]
>
>Stellen Sie für jeden Ereignistyp sicher, dass mit dem im Datensatz verwendeten Schema die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft ist. [Weitere Informationen](create-dataset.md)

Im Folgenden finden Sie die Schemaanforderungen, die Sie in Ihren JavaScript-Code implementieren müssen.

>[!NOTE]
>
>Entscheidungsereignisse müssen nicht gesendet werden, da das Entscheidungs-Management diese Ereignisse automatisch generiert und im Datensatz **[!UICONTROL ODE DecisionEvents]**<!--to check--> speichert, der automatisch generiert wird.

## Verfolgen von Impressions

Stellen Sie sicher, dass der Ereignistyp und die Quelle wie folgt aussehen:

**Erlebnisereignistyp:** `decisioning.propositionDisplay`
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
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## Verfolgen von Klicks

Stellen Sie sicher, dass der Ereignistyp und die Quelle wie folgt aussehen:

**Erlebnisereignistyp:** `decisioning.propositionInteract`
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

## Verfolgen benutzerdefinierter Ereignisse

Bei benutzerdefinierten Ereignissen muss das im Datensatz verwendete Schema auch die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** aufweisen, die damit verknüpft ist. Es gibt jedoch keine spezielle Anforderung für den Erlebnisereignistyp, die zum Taggen dieser Ereignisse verwendet werden muss.

>[!NOTE]
>
>So lassen Sie Ihre benutzerdefinierten Ereignisse in [Frequenzlimitierung](../offer-library/add-constraints.md#capping)müssen Sie das Erlebnisereignis mit den Adobe Experience Platform-Endpunkten verbinden, indem Sie es an einen dieser beiden Edge-Datenerfassungsendpunkte senden:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Wenn Sie die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=de){target="_blank"}, wird die Verbindung automatisch hergestellt.

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
