---
title: Code-basierte Implementierungsbeispiele
description: Auf dieser Seite finden Sie Beispiele für die Implementierungsmethode für die Code-basierte Funktion in Journey Optimizer.
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: 05f076f19a348032e5bb21d7d1682509bd5d2658
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 82%

---

# Beispiele für Implementierungsmethoden für Code-basierte Erlebnisse {#implementation-samples}

Code-basierte Erlebnisse unterstützen jede Art von Kundenimplementierung. Auf dieser Seite finden Sie Beispiele für die einzelnen Implementierungsmethoden:

* [Client-seitig](#client-side-implementation)
* [Server-seitig](#server-side-implementation)
* [Hybrid](#hybrid-implementation)

>[!IMPORTANT]
>
>Folgen Sie [diesem Link](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}, um Beispielimplementierungen für verschiedene Anwendungsfälle für Personalisierung und Experimente zu finden. Sehen Sie sich die Anwendungsfälle an und führen Sie sie aus, um besser zu verstehen, welche Implementierungsschritte erforderlich sind und wie der End-to-End-Personalisierungsfluss funktioniert.

➡️ Weitere Informationen zum Konfigurieren von Web SDK für Code-basierte Erlebnisse und Entscheidungen finden Sie in [diesen Tutorials](code-based-decisioning-implementations.md#tutorials)

## Client-seitige Implementierung {#client-side-implementation}

Wenn Sie eine Client-seitige Implementierung haben, können Sie eines der AEP-Client-SDKs verwenden: AEP Web SDK oder AEP Mobile SDK.

* Die [folgenden](#client-side-how) Schritte beschreiben den Prozess zum Abrufen von Inhalten, die von Code-basierten Erlebnis-Journeys und -kampagnen in einer Beispielimplementierung mit dem **Web SDK** am Edge veröffentlicht wurden, und zum Anzeigen der personalisierten Inhalte.

* Die Schritte zur Implementierung eines Code-basierten Kanals mit **Mobile SDK** sind in [diesem Tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} beschrieben.

  >[!NOTE]
  >
  >Beispielimplementierungen für Mobile-Anwendungsfälle sind für die [iOS-App](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} und [Android-App](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"} verfügbar.

### Funktionsweise – Web SDK {#client-side-how}

1. Das [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} ist auf der Seite enthalten.

1. Sie müssen den Befehl `sendEvent` verwenden und den [Oberflächen-URI](code-based-surface.md)<!--( or location/path)--> angeben, um den Personalisierungsinhalt abzurufen.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Elemente von Code-basierten Erlebnissen sollten vom Implementierungs-Code manuell angewendet werden (unter Verwendung der Methode [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"}), um das DOM basierend auf der Entscheidung zu aktualisieren.

1. Bei Code-basierten Erlebnis-Journeys und -kampagnen müssen Anzeigeereignisse manuell gesendet werden, um anzugeben, wann der Inhalt angezeigt wurde. Dies geschieht über den Befehl `sendEvent`.

   ```javascript
   function sendDisplayEvent(decision) {
     const { id, scope, scopeDetails = {} } = decision;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionDisplay",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
           },
         },
       },
     });
   }
   ```

1. Bei Code-basierten Erlebnis-Journeys und -kampagnen müssen Interaktionsereignisse manuell gesendet werden, um anzugeben, wann die Benutzerin oder der Benutzer mit dem Inhalt interagiert hat.  Dies geschieht über den Befehl `sendEvent`.

   ```javascript
   function sendInteractEvent(label, proposition) {
     const { id, scope, scopeDetails = {} } = proposition;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionInteract",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
             propositionEventType: {
               interact: 1
             },
             propositionAction: {
               id: label,
               label: label,
               tokens: proposition.items?.[0]?.characteristics?.tokens || []
             },
           },
         },
       },
     });
   }
   ```

   >[!IMPORTANT]
   >
   >Das `tokens` Feld in `propositionAction` ist für das präzise Tracking und die Attribution in Adobe Journey Optimizer Decisioning von entscheidender Bedeutung. Diese Token ermöglichen Folgendes:
   >* Korrekte Klick-Attribution für Entscheidungsaktivitäten
   >* Präzises Reporting von Benutzerinteraktionen mit Entscheidungsinhalten
   >* Optimierung der Angebotsleistung basierend auf der Benutzerinteraktion
   >
   >Die Token befinden sich normalerweise in `proposition.items[0].characteristics.tokens` und sollten immer beim Verfolgen von Benutzerinteraktionen mit Entscheidungsinhalten einbezogen werden.

### Wichtige Beobachtungen

**Cookies**

Cookies werden verwendet, um die Benutzeridentität und Cluster-Informationen beizubehalten. Bei Verwendung einer Hybridimplementierung übernimmt das Web SDK das Speichern und Senden dieser Cookies während des Lebenszyklus der Anfrage automatisch.

| Cookie | Zweck | Gespeichert von | Gesendet von |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | Enthält Details zur Benutzeridentität | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | Gibt an, welcher Erlebnis-Edge-Cluster zur Erfüllung der Anfragen verwendet werden soll | Web SDK | Web SDK |

**Anfrage-Platzierung**

Anfragen an die Adobe Experience Platform-API sind erforderlich, um Vorschläge abzurufen und eine Benachrichtigung zur Anzeige zu senden. Bei Verwendung einer Client-seitigen Implementierung sendet das Web SDK diese Anfragen, wenn der Befehl `sendEvent` verwendet wird.

| Anfrage | Gemacht von |
| ---------------------------------------------- | ----------------------------------- |
| Interaktionsanfrage zum Abrufen von Vorschlägen | Web SDK mit dem Befehl „sendEvent“ |
| Interaktionsanfrage zum Senden von Anzeigebenachrichtigungen | Web SDK mit dem Befehl „sendEvent“ |

**Flussdiagramm**

![](assets/code-based-client-side-implementation.png)

## Server-seitige Implementierung {#server-side-implementation}

Bei einer Server-seitigen Implementierung, kann eine der AEP Edge Network-APIs verwendet werden.

Die folgenden Schritte beschreiben den Prozess, um die Inhalte abzurufen, die von den Code-basierten Erlebnis-Journeys und -kampagnen in einer Beispielimplementierung mit dem Edge Network-API für eine Web-Seite am Edge veröffentlicht wurden und die personalisierten Inhalte anzeigen.

### Funktionsweise

1. Die Web-Seite wird angefordert und alle Cookies, die zuvor vom Browser mit dem Präfix `kndctr_` gespeichert wurden, sind enthalten.
1. Wenn die Seite vom Anwendungs-Server angefordert wird, wird ein Ereignis an den [Endpunkt der interaktiven Datenerfassung](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de) gesendet, um Personalisierungsinhalte abzurufen. Diese Beispielanwendung verwendet Helper-Methoden, um das Erstellen und Senden von Anfragen an die API zu vereinfachen (siehe [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}). Die Anfrage ist jedoch einfach eine `POST` mit einer Payload, die ein Ereignis und eine Abfrage enthält. Die Cookies (sofern verfügbar) aus dem vorherigen Schritt sind mit der Anfrage in dem Array `meta>state>entries` enthalten.

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. Das JSON-Erlebnis aus den Code-basierten Erlebnis-Journeys und der Erlebniskampagne wird aus der Antwort gelesen und beim Erstellen der HTML-Antwort verwendet.

1. Bei Code-basierten Erlebnis-Journeys und -kampagnen müssen Anzeigeereignisse manuell in der Implementierung gesendet werden, um anzugeben, wann der Journey- oder Kampagneninhalt angezeigt wurde. In diesem Beispiel wird die Benachrichtigung Server-seitig während des Lebenszyklus der Anfrage gesendet.

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. Wenn die HTML-Antwort zurückgegeben wird, werden die Identitäts- und Cluster-Cookies in der Antwort vom Anwendungs-Server gesetzt.

### Wichtige Beobachtungen

**Cookies**

Cookies werden verwendet, um die Benutzeridentität und Cluster-Informationen beizubehalten. Bei Verwendung einer Server-seitigen Implementierung muss der Anwendungs-Server das Speichern und Senden dieser Cookies während des Lebenszyklus der Anfrage übernehmen.

| Cookie | Zweck | Gespeichert von | Gesendet von |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | Enthält Details zur Benutzeridentität | Anwendungs-Server | Anwendungs-Server |
| kndctr_AdobeOrg_cluster | Gibt an, welcher Erlebnis-Edge-Cluster zur Erfüllung der Anfragen verwendet werden soll | Anwendungs-Server | Anwendungs-Server |

**Anfrage-Platzierung**

Anfragen an die Adobe Experience Platform-API sind erforderlich, um Vorschläge abzurufen und eine Benachrichtigung zur Anzeige zu senden. Bei Verwendung einer Client-seitigen Implementierung sendet das Web SDK diese Anfragen, wenn der Befehl `sendEvent` verwendet wird.

| Anfrage | Gemacht von |
| ---------------------------------------------- | ------------------------------------------------------------ |
| Interaktionsanfrage zum Abrufen von Vorschlägen | Anwendungs-Server, der die Adobe Experience Platform-API aufruft |
| Interaktionsanfrage zum Senden von Anzeigebenachrichtigungen | Anwendungs-Server, der die Adobe Experience Platform-API aufruft |

**Flussdiagramm**

![](assets/code-based-server-side-implementation.png)

## Hybridimplementierung {#hybrid-implementation}

Wenn Sie eine hybride Implementierung haben, sehen Sie sich die folgenden Links an.

* Adobe Tech Blog: [Hybride Personalisierung im Adobe Experience Platform Web SDK](https://blog.developer.adobe.com/de/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* SDK-Dokumentation: [Hybride Personalisierung mit Web SDK und Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html?lang=de){target="_blank"}

## Debuggen von Edge-Netzwerk-API-Aufrufen mit Adobe Experience Platform Assurance {#debugging-edge-api-assurance}

Wenn Sie die Edge Network-API direkt für Code-basierte Erlebnisse verwenden (nicht mit Web SDK oder Mobile SDK), können Sie Ihre API-Aufrufe mit Adobe Experience Platform Assurance debuggen, indem Sie die Assurance-Sitzungs-ID als Validierungs-Token-Kopfzeile angeben.

1. Rufen Sie Ihre Assurance-Sitzungs-ID aus einer aktiven Adobe Experience Platform Assurance-Sitzung ab oder erstellen Sie eine solche mithilfe der Assurance-API.

1. Fügen Sie den `x-adobe-aep-validation-token`-Header mit Ihrer Assurance-Sitzungs-ID hinzu, um Ihre Edge Network-API-Anfragen durch die Assurance-Sitzung zu leiten.

   **Beispiel:**

   ```bash
   curl -v 'https://edge.adobedc.net/ee/v1/interact?configId={DATASTREAM_ID}&requestId={REQUEST_ID}' \
   --header 'Content-Type: application/json' \
   --header 'x-adobe-aep-validation-token: {ASSURANCE_SESSION_ID}' \
   --data-raw '{
       "xdm": {
         "identityMap": {
               "ECID": [
                   {
                       "id": "{ECID_VALUE}"
                   }
               ]
           }
       },
       "events": [
           {
               "xdm": {
                   "eventType": "test",
                   "timestamp": "{TIMESTAMP}"
               }
           }
       ]
   }'
   ```

1. Öffnen Sie nach der Konfiguration Ihre Assurance-Sitzung und wählen Sie die Ansicht **[!UICONTROL Edge Delivery]** aus, um Edge Network-API-Anfragen und -Antworten in Echtzeit anzuzeigen, einschließlich Anfrage-Payloads, Antwortinhalte, Personalisierungsvorschläge und Fehlermeldungen.


<!--
## Implementation guides and tutorials {#implementation-guides}

To help you get started with implementing code-based experiences, refer to the comprehensive step-by-step tutorials below:

* **Mobile SDK implementation**: Follow [this tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} to learn how to set up code-based experiences on mobile apps using the Adobe Experience Platform Mobile SDK.

* **Web SDK implementation**: Learn how to configure the Web SDK for decisioning and code-based experiences in [these tutorials](code-based-decisioning-implementations.md#tutorials).

* **Decisioning implementation**: To learn how to implement decisioning capabilities on a code-based campaign, follow [this use case tutorial](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/decisioning/experience-decisioning/experience-decisioning-uc){target="_blank"}.-->
