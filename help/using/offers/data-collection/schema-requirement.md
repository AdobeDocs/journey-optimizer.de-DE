---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Konfigurieren der Ereigniserfassung
description: Erfahren Sie, wie Sie Ihr Angebotsschema zur Erfassung von Ereignissen konfigurieren
badge: label="Vorgängerversion" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DhaXO7sS2zR9iewgoQjrN5ptYNpYSt97e-hflU2iq7c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 94%

---

# Konfigurieren der Datenerfassung {#schema-requirements}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Um zu anderen Ereignistypen als Entscheidungsereignissen Feedback erhalten zu können, müssen Sie für jeden Ereignistyp in einem **Erlebnisereignis**, das an Adobe Experience Platform gesendet wird, den richtigen Wert festlegen.

>[!CAUTION]
>
>Stellen Sie für jeden Ereignistyp sicher, dass mit dem im Datensatz verwendeten Schema die Feldergruppe **[!UICONTROL Erlebnisereignis – Vorschlagsinteraktionen]** verknüpft ist. [Weitere Informationen](create-dataset.md)

Im Folgenden finden Sie die Schemaanforderungen, die Sie in Ihren JavaScript-Code implementieren müssen.

>[!NOTE]
>
>Entscheidungsereignisse müssen nicht gesendet werden, da das Entscheidungs-Management diese Ereignisse automatisch generiert und im Datensatz **[!UICONTROL ODE DecisionEvents]**<!--to check--> speichert, der automatisch generiert wird.

## Nachverfolgen von Impressions {#track-impressions}

Stellen Sie sicher, dass der Ereignistyp und die Quelle wie folgt aussehen:

**Erlebnisereignistyp:** `decisioning.propositionDisplay`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Aufnahme
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
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) oder Batch-Aufnahme
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
>Damit Ihre benutzerdefinierten Ereignisse bei der [Frequenzbegrenzung](../offer-library/add-constraints.md#capping) berücksichtigt werden, müssen Sie das Erlebnisereignis mit Adobe Experience Platform-Endpunkten verbinden, indem Sie es an einen dieser beiden Edge-Datenerfassungsendpunkte senden:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Wenn Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} oder das [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=de){target="_blank"} verwenden, wird die Verbindung automatisch hergestellt.
