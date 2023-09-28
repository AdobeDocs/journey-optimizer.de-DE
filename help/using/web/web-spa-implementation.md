---
title: Implementierung von Einzelseitenanwendungen
description: Erfahren Sie, wie Sie SPA Ansichten in Journey Optimizer implementieren
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 59412ecbb8df74c7185b67593131c610d6da4148
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 3%

---

# Implementierung von Einzelseitenanwendungen {#web-spa-implementation}

Adobe Experience Platform Web SDK bietet umfassende Funktionen, mit denen Ihr Unternehmen mithilfe von Client-seitigen Technologien der neuesten Generation, wie Single Page Applications (SPA), Personalisierungen ausführen kann.

Herkömmliche Websites arbeiten mit &quot;page-to-page&quot;-Navigationsmodellen, auch als mehrseitige Anwendungen bezeichnet, bei denen Website-Designs eng an URLs gekoppelt sind und Übergänge von einer Webseite zu einer anderen einen Seitenladevorgang erfordern.

Moderne Webanwendungen wie Einzelseiten-Apps (SPA) haben stattdessen ein Modell übernommen, das die schnelle Nutzung des Browser-UI-Renderings ermöglicht, das häufig unabhängig von Seitenneuladungen ist. Diese Erlebnisse können durch Kundeninteraktionen wie Bildläufe, Klicks und Cursorbewegungen ausgelöst werden. Da sich die Paradigmen des modernen Webs weiterentwickelt haben, funktioniert die Relevanz herkömmlicher generischer Ereignisse wie Seitenladevorgänge für die Bereitstellung von Personalisierung und Experimenten nicht mehr.

![](assets/web-spa-vs-traditional-lifecycle.png)

## Vorteile des AEP Web SDK für SPA

Hier einige Vorteile der Verwendung des Adobe Experience Platform Web SDK für Einzelseitenanwendungen:

* Möglichkeit zur Zwischenspeicherung aller Angebote beim Seitenladen, um mehrere Server-Aufrufe auf einen einzelnen Server-Aufruf zu reduzieren
* Das Benutzererlebnis auf Ihrer Site wird erheblich verbessert, da Angebote sofort über den Cache angezeigt werden, ohne dass durch herkömmliche Server-Aufrufe eine verzögerungsfreie Zeit entsteht.
* Durch die einmalige Einrichtung von Entwicklern können Marketing-Experten Personalisierungs- und Experimentierungsaktivitäten über den Web-Visual-Editor von Adobe Journey Optimizer auf Ihrer SPA erstellen und ausführen.

## XDM-Ansichten und Einzelseitenanwendungen

Die Adobe **[!UICONTROL Journey Optimizer]** Der Web-Editor nutzt ein Konzept namens &quot;Ansichten&quot;: eine logische Gruppe visueller Elemente, aus denen zusammen ein SPA Erlebnis besteht. Eine Einzelseitenanwendung kann daher als Übergang durch Ansichten anstelle von URLs betrachtet werden, basierend auf Benutzerinteraktionen. Eine Ansicht kann normalerweise eine ganze Site, eine einzelne Seite oder gruppierte visuelle Elemente innerhalb einer Seite darstellen.

Zur weiteren Erläuterung der Ansichten wird im folgenden Beispiel eine hypothetische E-Commerce-Website verwendet.

* Nachdem Sie zur Startseite navigiert sind, fördert ein Hero-Bild saisonale Sammlungen sowie die verschiedenen Produktkataloge, die auf der Site verfügbar sind. In diesem Fall kann eine Ansicht für den gesamten Startbildschirm definiert werden. Diese Ansicht könnte einfach als &quot;Zuhause&quot;bezeichnet werden.

  ![](assets/web-spa-home.png)

* Wenn sich der Kunde mehr für die Produkte interessiert, die das Unternehmen verkauft, entscheidet er, auf die **Männer** -Link. Ähnlich wie bei der Startseite ist die gesamte **Männer** -Seite kann als Ansicht definiert werden. Diese Ansicht könnte &quot;Männer&quot;heißen.

  ![](assets/web-spa-men.png)

* Da eine Ansicht als ganze Site oder eine Gruppe visueller Elemente auf einer Site definiert werden kann, können die vier auf der Produktseite angezeigten Produkte gruppiert und als Ansicht betrachtet werden. Diese Ansicht könnte &quot;Produkte&quot;heißen.

  ![](assets/web-spa-men-products.png)

* Wenn der Kunde sich entscheidet, auf die **PRODUKTE ALLER MÄNNER** -Schaltfläche, um weitere Produkte auf der Site zu untersuchen, ändert sich die Website-URL in diesem Fall nicht, aber hier kann eine Ansicht erstellt werden, die nur die zweite Zeile der angezeigten Produkte darstellt. Der Ansichtsname könnte &quot;products-page-2&quot;lauten.

* Der Kunde beschließt, einige Produkte von der Site zu kaufen, und fährt mit dem Checkout-Bildschirm fort. Der Warenkorbbildschirm selbst kann mit einer Ansicht namens &quot;Warenkorb&quot;verknüpft werden. Oder Sie können eine andere Ansicht im Checkout-Bildschirm haben, um die unten empfohlenen Produkte zu verarbeiten.

  ![](assets/web-spa-cart.png)

Das Konzept der Ansichten kann noch viel weiter ausgeweitet werden. Dies sind nur einige Beispiele für Ansichten, die auf einer Site definiert werden können.

## Implementieren von XDM-Ansichten {#implement-xdm-views}

XDM-Ansichten können in Adobe Journey Optimizer genutzt werden, um Marketingexperten zu ermöglichen, Web-Personalisierungs- und Erlebniskampagnen auf SPA über den Web-Visual-Editor von Journey Optimizer durchzuführen.

Dazu müssen Sie die folgenden Schritte ausführen, um eine einmalige Entwicklereinrichtung abzuschließen:

1. Installieren [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=de){target="_blank"} und überprüfen Sie die [Voraussetzungen für Webkanäle](web-prerequisites.md) Seite.

2. Bestimmen Sie alle XDM-Ansichten in Ihrer Einzelseitenanwendung, die Sie personalisieren möchten.

3. Nach dem Definieren der XDM-Ansichten müssen Sie, um Inhalte für diese Ansichten bereitzustellen, die `sendEvent()` Funktion mit `renderDecisions` auf `true` und der entsprechenden XDM-Ansicht in Ihrer Einzelseitenanwendung. Die XDM-Ansicht muss übergeben werden `xdm.web.webPageDetails.viewName`. Auf diese Weise können Marketingexperten diese Ansichten im Journey Optimizer-Web-Editor erkennen und Inhaltsänderungen darauf anwenden:

```
 alloy("sendEvent", {
  "renderDecisions": true,
  "xdm": {
   "web": {
    "webPageDetails": {
    "viewName":"home"
   }
  }
 }
});
```

>[!NOTE]
>
>Zum ersten `sendEvent()` aufrufen, werden alle XDM-Ansichten abgerufen und zwischengespeichert, die an den Endbenutzer gerendert werden sollen. Nachstehend `sendEvent()` -Aufrufe mit übergebenen XDM-Ansichten werden aus dem Cache gelesen und ohne Serveraufruf gerendert.

## `sendEvent()` Funktionsbeispiele

In diesem Abschnitt werden zwei Beispiele zum Aufrufen der `sendEvent()` -Funktion in React für eine hypothetische E-Commerce-SPA verwenden.

### Beispiel 1: Startseite eines A/B-Tests

Das Marketing-Team möchte A/B-Tests auf der gesamten Startseite durchführen.

![](assets/web-spa-home.png)

So führen Sie A/B-Tests auf der gesamten Homepage durch: `sendEvent()` muss mit dem XDM aufgerufen werden `viewName` auf `home`:

```
function onViewChange() {

  var viewName = window.location.hash; // or use window.location.pathName if router works on path and not hash

  viewName = viewName || 'home'; // view name cannot be empty

  // Sanitize viewName to get rid of any trailing symbols derived from URL

  if (viewName.startsWith('#') || viewName.startsWith('/')) {
    viewName = viewName.substr(1);
  }

  alloy("sendEvent", {
    "renderDecisions": true,

    "xdm": {
      "web": {
        "webPageDetails": {
          "viewName":"home"
        }
      }
    }
  });
}

// react router v4

const history = syncHistoryWithStore(createBrowserHistory(), store);

history.listen(onViewChange);

// react router v3

<Router history={hashHistory} onUpdate={onViewChange} >
```

### Beispiel 2: Personalisierte Produkte

Das Marketing-Team möchte die zweite Reihe von Produkten personalisieren, indem es die Farbe der Preisbeschriftung in Rot ändert, nachdem ein Benutzer klickt, um alle Men-Produkte anzuzeigen.

![](assets/web-spa-men-products.png)

```
function onViewChange(viewName) {

  alloy("sendEvent", {
    "renderDecisions": true,
    "xdm": {
      "web": {
        "webPageDetails": {
          "viewName": viewName
        }
      }
    }
  });
}

class Products extends Component {

  render() {
    return (

        <button type="button" onClick={this.handleLoadMoreClicked}>All Men's Products</button>
    );
  }

  handleLoadMoreClicked() {
    var page = this.state.page + 1; // assuming page number is derived from component's state
    this.setState({page: page});
    onViewChange('PRODUCTS-PAGE-' + page);
  }

}
```
