---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Konfigurieren der Ereigniserfassung
description: Erfahren Sie, wie Sie Ihr Angebotsschema zur Erfassung von Ereignissen konfigurieren
badge: label="Legacy" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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
>Damit Ihre benutzerdefinierten Ereignisse bei der [Frequenzbegrenzung](../offer-library/add-constraints.md#capping) berücksichtigt werden, müssen Sie das Erlebnisereignis mit Adobe Experience Platform-Endpunkten verbinden, indem Sie es an einen dieser beiden Edge-Datenerfassungsendpunkte senden:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Wenn Sie das [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} oder das [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=de){target="_blank"} verwenden, wird die Verbindung automatisch hergestellt.
