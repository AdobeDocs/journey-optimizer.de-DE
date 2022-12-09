---
product: experience platform
solution: Experience Platform
title: Ereigniserfassung konfigurieren
description: Erfahren Sie, wie Sie Ihr Angebotsschema zur Erfassung von Ereignissen konfigurieren
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Ereigniserfassung konfigurieren {#schema-requirements}

An dieser Stelle müssen Sie über Folgendes verfügen:

* das KI-Modell erstellt hat,
* definiert, welcher Ereignistyp erfasst werden soll - angezeigtes Angebot (Impression) und/oder angeklicktes Angebot (Konversion);
* und in welchem Datensatz Sie die Ereignisdaten erfassen möchten.

Jedes Mal, wenn ein Angebot angezeigt und/oder angeklickt wird, soll das entsprechende Ereignis automatisch von der **[!UICONTROL Experience Event - Proposition Interactions]** Feldergruppe mithilfe der [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;} oder Mobile SDK.

Um Ereignistypen (angezeigtes Angebot oder angeklicktes Angebot) senden zu können, müssen Sie für jeden Ereignistyp in einem Erlebnisereignis, das an Adobe Experience Platform gesendet wird, den richtigen Wert festlegen. Im Folgenden finden Sie die Schemaanforderungen, die Sie in Ihren JavaScript-Code implementieren müssen:

## Angezeigte Angebote

**Ereignistyp:** `decisioning.propositionDisplay`
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

### Angebotsszenario

**Ereignistyp:** `decisioning.propositionInteract`
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
