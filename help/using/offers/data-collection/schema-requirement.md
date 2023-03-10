---
product: experience platform
solution: Experience Platform
title: Konfigurieren der Ereigniserfassung
description: Erfahren Sie, wie Sie Ihr Angebotsschema zur Erfassung von Ereignissen konfigurieren
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 15%

---

# Datenerfassung konfigurieren {#schema-requirements}

<!--To send in feedback data, you must define how the experience events will be captured.-->

Um Feedback zu anderen Ereignistypen als Entscheidungsereignissen zu erhalten, müssen Sie für jeden Ereignistyp in einer **Erlebnisereignis** wird an Adobe Experience Platform gesendet.

Stellen Sie für jeden Ereignistyp sicher, dass das im Datensatz verwendete Schema die Variable **[!UICONTROL Erlebnisereignis - Interaktionen bei Vorschlägen]** mit ihr verknüpfte Feldergruppe. [Weitere Informationen](create-dataset.md)

Im Folgenden finden Sie die Schemaanforderungen, die Sie in Ihren JavaScript-Code implementieren müssen.

>[!NOTE]
>
>Entscheidungsereignisse müssen nicht gesendet werden, da die Entscheidungsverwaltung diese Ereignisse automatisch generiert und in der Variablen **[!UICONTROL ODE DecisionEvents]** Datensatz<!--to check--> wird automatisch generiert.

## Impressionen verfolgen

Stellen Sie sicher, dass Ereignistyp und -quelle wie folgt aussehen:

**Erlebnisereignistyp:** `decisioning.propositionDisplay`
**Quelle:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Erfassung
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

## Klicks verfolgen

Stellen Sie sicher, dass Ereignistyp und -quelle wie folgt aussehen:

**Erlebnisereignistyp:** `decisioning.propositionInteract`
**Quelle:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Erfassung
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

## Benutzerspezifische Ereignisse verfolgen

Bei benutzerdefinierten Ereignissen muss das im Datensatz verwendete Schema auch die Variable **[!UICONTROL Erlebnisereignis - Interaktionen bei Vorschlägen]** Feldergruppe, die mit ihr verknüpft ist, es gibt jedoch keine spezielle Anforderung für den Erlebnisereignistyp, die zum Taggen dieser Ereignisse verwendet werden muss.

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
