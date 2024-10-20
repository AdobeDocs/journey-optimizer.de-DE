---
title: Code-basierte Implementierungsbeispiele
description: Auf dieser Seite finden Sie Beispiele für die Implementierungsmethode für die Code-basierte Funktion in Journey Optimizer.
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: c3300b240bd0dc0563ed6d4e6de40bd9fa36a92e
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 75%

---

# Beispiele für Implementierungsmethoden für Code-basierte Erlebnisse {#implementation-samples}

Code-basierte Erlebnisse unterstützen jede Art von Kundenimplementierung. Auf dieser Seite finden Sie Beispiele für die einzelnen Implementierungsmethoden:

* [Client-seitig](#client-side-implementation)
* [Server-seitig](#server-side-implementation)
* [Hybrid](#hybrid-implementation)

>[!IMPORTANT]
>
>Folgen Sie [diesem Link](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}, um Beispielimplementierungen für verschiedene Anwendungsfälle für Personalisierung und Experimente zu finden. Sehen Sie sich die Anwendungsfälle an und führen Sie sie aus, um besser zu verstehen, welche Implementierungsschritte erforderlich sind und wie der vollständige Personalisierungsfluss funktioniert.

## Client-seitige Implementierung {#client-side-implementation}

Wenn Sie eine Client-seitige Implementierung haben, können Sie eines der AEP-Client-SDKs verwenden: AEP Web SDK oder AEP Mobile SDK.

* Die Schritte [unter ](#client-side-how) beschreiben den Prozess, den Inhalt abzurufen, der von den code-basierten Erlebnis-Journey und Kampagnen am Edge veröffentlicht wurde, und zwar in einer Beispielimplementierung des **Web SDK** und mit der Anzeige des personalisierten Inhalts.

* Die Schritte zur Implementierung eines Code-basierten Kanals mit **Mobile SDK** sind in [diesem Tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} beschrieben.

  >[!NOTE]
  >
  >Beispielimplementierungen für mobile Anwendungsfälle sind für [iOS-App](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} und [Android-App](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"} verfügbar.

### Funktionsweise – Web SDK {#client-side-how}

1. Das [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} ist auf der Seite enthalten.

1. Sie müssen den Befehl `sendEvent` verwenden und den [Oberflächen-URI](code-based-configuration.md#surface-definition)<!--( or location/path)--> angeben, um Personalisierungsinhalte abzurufen.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Elemente von Code-basierten Erlebnissen sollten vom Implementierungs-Code manuell angewendet werden (unter Verwendung der Methode [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"}), um das DOM basierend auf der Entscheidung zu aktualisieren.

1. Bei code-basierten Journey und Kampagnen müssen Anzeigeereignisse manuell gesendet werden, um anzugeben, wann der Inhalt angezeigt wurde. Dies geschieht über den Befehl `sendEvent`.

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

1. Bei code-basierten Journey und Kampagnen müssen Interaktionsereignisse manuell gesendet werden, um anzugeben, wann ein Benutzer mit dem Inhalt interagiert hat. Dies geschieht über den Befehl `sendEvent`.

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
               label: label
             },
           },
         },
       },
     });
   }
   ```

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

Die folgenden Schritte beschreiben den Prozess des Abrufs von Inhalten, die von den code-basierten Erlebnis-Journey und Kampagnen in einer Edge Network-API-Beispielimplementierung für eine Webseite veröffentlicht wurden, und der Anzeige der personalisierten Inhalte.

### Funktionsweise

1. Die Web-Seite wird angefordert und alle Cookies, die zuvor vom Browser mit dem Präfix `kndctr_` gespeichert wurden, sind enthalten.
1. Wenn die Seite vom Anwendungs-Server angefordert wird, wird ein Ereignis an den [Endpunkt der interaktiven Datenerfassung](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=de) gesendet, um Personalisierungsinhalte abzurufen. Diese Beispielanwendung verwendet Hilfsmethoden, um das Erstellen und Senden von Anfragen an die API zu vereinfachen (siehe [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}). Die Anfrage ist jedoch einfach eine `POST` mit einer Payload, die ein Ereignis und eine Abfrage enthält. Die Cookies (sofern verfügbar) aus dem vorherigen Schritt sind mit der Anfrage in dem Array `meta>state>entries` enthalten.

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

1. Das JSON-Erlebnis aus den code-basierten Erlebnis-Journey und Kampagnen wird aus der Antwort gelesen und bei der Erstellung der HTML-Antwort verwendet.

1. Bei code-basierten Journey und Kampagnen müssen Anzeigeereignisse in der Implementierung manuell gesendet werden, um anzugeben, wann der Journey- oder Kampagneninhalt angezeigt wurde. In diesem Beispiel wird die Benachrichtigung während des Anfragelebenszyklus serverseitig gesendet.

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
* SDK Dokumentation: [Hybride Personalisierung mit Web SDK und Edge Network Server-API](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html?lang=de){target="_blank"}
