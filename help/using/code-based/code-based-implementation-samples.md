---
title: Code-basierte Implementierungsbeispiele
description: Auf dieser Seite finden Sie Beispiele für die Implementierungsmethode für die Code-basierte Funktion in Journey Optimizer.
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 100%

---

# Beispiele für Implementierungsmethoden für Code-basierte Erlebnisse {#implementation-samples}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit dem Code-basierten Kanal](get-started-code-based.md)
* [Code-basierte Voraussetzungen](code-based-prerequisites.md)
* **[Implementierungsbeispiele für Code-basierte Erlebnisse](code-based-implementation-samples.md)**
* [Erstellen von Code-basierten Erlebnissen](create-code-based.md)

>[!ENDSHADEBOX]

Code-basierte Erlebnisse unterstützen jede Art von Kundenimplementierung. Auf dieser Seite finden Sie Beispiele für die einzelnen Implementierungsmethoden:

* [Client-seitig](#client-side-implementation)
* [Server-seitig](#server-side-implementation)
* [Hybrid](#hybrid-implementation)

Sie können auch [diesem Link](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} folgen, um Beispielimplementierungen für verschiedene Anwendungsfälle für Personalisierung und Experimente zu finden. Sehen Sie sich die Anwendungsfälle an und führen Sie sie aus, um besser zu verstehen, welche Implementierungsschritte erforderlich sind und wie der vollständige Personalisierungsfluss funktioniert.

## Client-seitige Implementierung {#client-side-implementation}

Wenn Sie eine Client-seitige Implementierung haben, können Sie eines der AEP-Client-SDKs verwenden: AEP Web SDK oder AEP Mobile SDK. Die folgenden Schritte beschreiben den Prozess, um die Inhalte abzurufen, die von den Code-basierten Erlebniskampagnen in einer Beispielimplementierung mit dem Web SDK veröffentlicht wurden, und die personalisierten Inhalte anzuzeigen.

### Funktionsweise

1. Das [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de){target="_blank"} ist auf der Seite enthalten.

1. Sie müssen den Befehl `sendEvent` verwenden und den Oberflächen-URI angeben, um den Personalisierungsinhalt abzurufen.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Elemente von Code-basierten Erlebnissen sollten vom Implementierungs-Code manuell angewendet werden (unter Verwendung der Methode [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"}), um das DOM basierend auf der Entscheidung zu aktualisieren.

1. Bei Code-basierten Erlebniskampagnen müssen Anzeigeereignisse manuell gesendet werden, um anzugeben, wann der Inhalt angezeigt wurde. Dies geschieht über den Befehl `sendEvent`.

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

### Wichtige Beobachtungen

**Cookies**

Cookies werden verwendet, um die Benutzeridentität und Cluster-Informationen beizubehalten. Bei Verwendung einer Hybridimplementierung übernimmt das Web SDK das Speichern und Senden dieser Cookies während des Lebenszyklus der Anfrage automatisch.

| Cookie | Zweck | Gespeichert von | Gesendet von |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | Enthält Details zur Benutzeridentität | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | Gibt an, welcher Erlebnis-Edge-Cluster zur Erfüllung der Anfragen verwendet werden soll | Web SDK | Web SDK |

**Anfordern einer Platzierung**

Anfragen an die Adobe Experience Platform-API sind erforderlich, um Vorschläge abzurufen und eine Benachrichtigung zur Anzeige zu senden. Bei Verwendung einer Client-seitigen Implementierung sendet das Web SDK diese Anfragen, wenn der Befehl `sendEvent` verwendet wird.

| Anfrage | Gemacht von |
| ---------------------------------------------- | ----------------------------------- |
| Interaktionsanfrage zum Abrufen von Vorschlägen | Web SDK mit dem Befehl „sendEvent“ |
| Interaktionsanfrage zum Senden von Anzeigebenachrichtigungen | Web SDK mit dem Befehl „sendEvent“ |

**Flussdiagramm**

![](assets/code-based-client-side-implementation.png)

## Server-seitige Implementierung {#server-side-implementation}

Bei einer Server-seitigen Implementierung, kann eine der AEP Edge Network-APIs verwendet werden. Die folgenden Schritte beschreiben den Prozess, um die Inhalte abzurufen, die von den Code-basierten Erlebniskampagnen in einer Beispielimplementierung mit dem Edge Network-API für eine Web-Seite veröffentlicht wurden und die personalisierten Inhalte anzeigen.

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

1. Das JSON-Erlebnis aus der Code-basierten Erlebniskampagne wird aus der Antwort gelesen und beim Erstellen der HTML-Antwort verwendet.
1. Bei Code-basierten Erlebniskampagnen müssen Anzeigeereignisse manuell in der Implementierung gesendet werden, um anzugeben, wann der Kampagneninhalt angezeigt wurde. In diesem Beispiel wird die Benachrichtigung Server-seitig während des Lebenszyklus der Anfrage gesendet.

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

**Anfordern einer Platzierung**

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
