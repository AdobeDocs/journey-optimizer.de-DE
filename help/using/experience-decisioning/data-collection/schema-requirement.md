---
product: experience platform
solution: Experience Platform
title: Konfigurieren der Ereigniserfassung
description: Erfahren Sie, wie Sie Ihr Angebotsschema zur Erfassung von Ereignissen konfigurieren
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
hide: true
hidefromtoc: true
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
source-git-commit: 0bba63855360d0dcd7daa98a2083f23995b88b94
workflow-type: ht
source-wordcount: '271'
ht-degree: 100%

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

## Verfolgen von Impressions {#track-impressions}

Stellen Sie sicher, dass der Ereignistyp und die Quelle wie folgt aussehen:

**Erlebnisereignistyp:** `decisioning.propositionDisplay`
**Quelle:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Aufnahme
+++**Beispiel-Payload:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## Verfolgen von Klicks {#track-clicks}

Stellen Sie sicher, dass der Ereignistyp und die Quelle wie folgt aussehen:

**Erlebnisereignistyp:** `decisioning.propositionInteract`
**Quelle:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Aufnahme
+++**Beispiel-Payload:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## Verfolgen benutzerdefinierter Ereignisse {#track-custom-events}

Bei benutzerdefinierten Ereignissen muss das im Datensatz verwendete Schema auch die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** aufweisen, die damit verknüpft ist. Es gibt jedoch keine spezielle Anforderung für den Erlebnisereignistyp, die zum Taggen dieser Ereignisse verwendet werden muss.

>[!NOTE]
>
>Damit Ihre benutzerdefinierten Ereignisse bei der [Begrenzung](../items.md#capping) berücksichtigt werden, müssen Sie das Erlebnisereignis mit Adobe Experience Platform-Endpunkten verbinden, indem Sie es an einen dieser beiden Edge-Datenerfassungsendpunkte senden:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Wenn Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} oder das [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=de){target="_blank"} verwenden, wird die Verbindung automatisch hergestellt.
