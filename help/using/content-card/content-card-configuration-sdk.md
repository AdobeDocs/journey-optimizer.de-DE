---
title: Konfiguration von Inhaltskarten im Web SDK
description: Konfigurieren der Unterstützung für Inhaltskarten im Web SDK
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: bb67b55f-2eac-4775-a9f5-78288009477e
source-git-commit: 37862682a25843ce138c076e443f6d9b6229ece3
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 100%

---

# Konfigurieren der Unterstützung für Inhaltskarten im Web SDK {#content-card-configuration-sdk}

Dieses Beispiel zeigt, wie Inhaltskarten aus Adobe Journey Optimizer (AJO) mithilfe von Adobe Experience Platform abgerufen werden. Mit dem [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/home) werden die Personalisierungsinhalte vollständig auf der Client-Seite abgerufen und gerendert.

Beim ersten Laden der Seite wird der Standardzustand der Seite angezeigt. Wenn Sie jedoch mit den Schaltflächen **Mittel einzahlen** oder **In Social Media freigeben** interagieren, werden zusätzliche Inhaltskarten angezeigt. Diese Karten werden durch Client-seitige Bedingungen ausgelöst, sodass sie nur angezeigt werden, wenn bestimmte Aktionen ausgeführt werden.

![](assets/content-card-web-1.png)

## Ausführen des Beispiels {#run-sample}

>[!PREREQUISITES]
>
>Sie müssen node und npm installieren. [Weitere Informationen finden Sie in dieser Dokumentation](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)


1. Richten Sie lokale SSL-Zertifikate für HTTPS ein. Diese Beispiele erfordern lokal signierte SSL-Zertifikate, um Inhalte über HTTPS bereitzustellen:

   1. Installieren Sie `mkcert` auf Ihrem Computer.

   1. Führen Sie nach der Installation `mkcert -install` aus, um das `mkcert root`-Zertifikat zu installieren.

1. Klonen Sie das Repository auf Ihren lokalen Computer.

1. Öffnen Sie ein Terminal und navigieren Sie zum Ordner des Beispiels.

1. Installieren Sie die erforderlichen Abhängigkeiten, indem Sie `npm install` ausführen.

1. Starten Sie die Anwendung, indem Sie `npm start` ausführen.

1. Öffnen Sie Ihren Webbrowser und gehen Sie zu `https://localhost`.

## Funktionsweise {#setup}

1. Fügen Sie das [Web SDK](https://experienceleague.adobe.com/de/docs/experience-platform/web-sdk/home) auf der Seite ein und konfigurieren Sie es mithilfe der Einstellungen aus der Datei `.env` im Beispielordner.

   ```
   <script src="https://cdn1.adoberesources.net/alloy/2.18.0/alloy.min.js" async></script>
   alloy("configure", {
       defaultConsent: "in",
       edgeDomain: "{{edgeDomain}}",
       edgeConfigId: "{{edgeConfigId}}",
       orgId:"{{orgId}}",
       debugEnabled: false,
       personalizationStorageEnabled: true,
       thirdPartyCookiesEnabled: false
   });
   ```

1. Verwenden Sie den Befehl `sendEvent`, um personalisierten Inhalt abzurufen.

   ```
   alloy("sendEvent", {
       renderDecisions: true,
       personalization: {
           surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       },
   });
   ```

1. Abonnieren Sie Inhaltskarten für eine bestimmte Oberfläche mit dem Befehl `subscribeRulesetItems`. Handhaben Sie bei jeder Auswertung von Regelsätzen das Ergebnisobjekt im Callback, das `propositions` mit Inhaltskartendaten enthält.

   ```
   const contentCardManager = createContentCardManager("content-cards");
   
   alloy("subscribeRulesetItems", {
       surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       schemas: ["https://ns.adobe.com/personalization/message/content-card"],
       callback: (result, collectEvent) => {
           const { propositions = [] } = result;
           contentCardManager.refresh(propositions, collectEvent);
       },
   });
   ```

1. Verwalten Sie die Darstellung von Inhaltskarten und senden Sie die Ereignisse `interact` und `display` mithilfe des Objekts `contentCardsManager` in `script.js`. Extrahieren, sortieren und verarbeiten Sie Inhaltskarten aus den empfangenen Vorschlägen.

   ```
   const createContentCard = (proposition, item) => {
       const { data = {}, id } = item;
       const {
           content = {},
           meta = {},
           publishedDate,
           qualifiedDate,
           displayedDate,
       } = data;
   
       return {
           id,
           ...content,
           meta,
           qualifiedDate,
           displayedDate,
           publishedDate,
           getProposition: () => proposition,
       };
   };
   
   const extractContentCards = (propositions) =>
       propositions
           .reduce((allItems, proposition) => {
           const { items = [] } = proposition;
   
           return [
               ...allItems,
               ...items.map((item) => createContentCard(proposition, item)),
           ];
       }, [])
       .sort(
           (a, b) =>
               b.qualifiedDate - a.qualifiedDate || b.publishedDate - a.publishedDate
       );
   
   const contentCards = extractContentCards(propositions);
   ```

1. Rendern Sie die Inhaltskarten basierend auf den für jede Kampagne definierten Details. Jede Karte enthält einen `title`, einen `body`, eine `imageUrl` und andere benutzerdefinierte Datenwerte.

   ```
   const renderContentCards = () => {
       const contentCardsContainer = document.getElementById(containerElementId);
       contentCardsContainer.addEventListener("click", handleContentCardClick);
   
       let contents = "";
   
       contentCards.forEach((card) => {
           const { id, title, body, imageUrl, meta = {} } = card;
           const { buttonLabel = "" } = meta;
   
           contents += `
               <div class="col">
                   <div data-id="${id}" class="card h-100">
                       <img src="${imageUrl}" class="card-img-top" alt="...">
                       <div class="card-body d-flex flex-column">
                           <h5 class="card-title">${title}</h5>
                           <p class="card-text">${body}</p>
                           <a href="#" class="mt-auto btn btn-primary">${buttonLabel}</a>
                       </div>
                   </div>
                </div>
            `;
       });
   
       contentCardsContainer.innerHTML = contents;
       collectEvent(
           "display",
           contentCards.map((card) => card.getProposition())
        );
   };
   ```

1. Wenn der Rückruf `subscribeRulesetItems` aufgerufen wird, wird auch eine Hilfsfunktion namens `collectEvent` bereitgestellt. Diese Funktion wird zum Senden von Experience Edge-Ereignissen verwendet, um Interaktionen, Anzeigen und andere Benutzeraktionen zu verfolgen. In diesem Beispiel verfolgt collectEvent, wenn auf eine Inhaltskarte geklickt wird. Wenn außerdem auf die Schaltfläche auf der Inhaltskarte geklickt wird, wird der Browser zu der `actionUrl` weitergeleitet, die von der Kampagne angegeben wurde.

   ```
   const handleContentCardClick = (evt) => {
       const cardEl = evt.target.closest(".card");
   
       if (!cardEl) {
           return;
       }
   
       const isAnchor = evt.target.nodeName === "A";
       const card = contentCards.find((card) => card.id === cardEl.dataset.id);
   
       if (!card) {
           return;
       }
   
       collectEvent("interact", [card.getProposition()]);
   
       if (isAnchor) {
           evt.preventDefault();
           evt.stopImmediatePropagation();
           const { actionUrl } = card;
           if (actionUrl && actionUrl.length > 0) {
               window.location.href = actionUrl;
           }
       }
   };
   ```

## Wichtige Beobachtungen {#key-observations}

### personalizationStorageEnabled

Die Option `personalizationStorageEnabled` ist im Befehl `configure` auf `true` gesetzt. Dadurch wird sichergestellt, dass zuvor qualifizierte Inhaltskarten gespeichert werden und weiterhin über Benutzersitzungen hinweg angezeigt werden.

### Trigger

Inhaltskarten unterstützen benutzerdefinierte Trigger, die auf der Client-Seite ausgewertet werden. Wenn eine Trigger-Regel erfüllt ist, werden zusätzliche Inhaltskarten angezeigt. In diesem Beispiel werden vier verschiedene Kampagnen verwendet, eine für jede Inhaltskarte, die alle dieselbe Oberfläche aufweisen: `web://alloy-samples.adobe.com/#content-cards-sample`. In der folgenden Tabelle werden die Trigger-Regeln für jede einzelnen Kampagnen und deren Erfüllung erläutert.

<table>
    <tr>
        <th>Trigger-Regel</th>
        <th>Karte</th>
        <th>Erfüllen der Trigger-Regel</th>
    </tr>
    <tr>
        <td>Keine</td>
        <td><img src="assets/content-card-web-2.png"></td>
        <td>sendEvent command. Keine Client-seitige Regel zu erfüllen.</td>
    </tr>
    <tr>
        <td>Keine</td>
        <td><img src="assets/content-card-web-3.png"></td>
        <td>sendEvent command. Keine Client-seitige Regel zu erfüllen.</td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-4.png"></td>
        <td><img src="assets/content-card-web-5.png"></td>
        <td><img src="assets/content-card-web-6.png"></td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-7.png"></td>
        <td><img src="assets/content-card-web-8.png"></td>
        <td><img src="assets/content-card-web-9.png"></td>
    </tr>
</table>

Der Befehl `evaluateRulesets` wird durch Klicken auf die Schaltflächen „Mittel einzahlen“ und „In Social Media freigeben“ ausgelöst. Jede Schaltfläche gibt den relevanten `decisionContext` an, um die für die jeweiligen Kampagnen definierten Regeln zu erfüllen.

```
document.getElementById("action-button-1").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "deposit-funds",
            },
        },
    });
});

document.getElementById("action-button-2").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "social-media",
            },
        },
    });
});
```
