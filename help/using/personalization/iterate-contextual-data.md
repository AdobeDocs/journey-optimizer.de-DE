---
solution: Journey Optimizer
product: journey optimizer
title: Iteration über kontextuelle Daten
description: Erfahren Sie, wie Sie Arrays aus verschiedenen Kontextquellen mithilfe der Handlebars-Syntax durchlaufen.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: Ausdruck, Editor, Handlebars, Iteration, Arrays, Kontext, Personalisierung
source-git-commit: 20421485e354b0609dd445f2db2b7078ee81d891
workflow-type: tm+mt
source-wordcount: '3008'
ht-degree: 0%

---

# Iteration über kontextuelle Daten {#personalization-contexts}

Erfahren Sie, wie Sie mit der Handlebars-Iterationssyntax dynamische Listen von Daten aus verschiedenen Quellen in Ihren Nachrichten anzeigen können, einschließlich Ereignissen, benutzerdefinierten Aktionsantworten und anderen kontextuellen Daten.

## Überblick {#overview}

Journey Optimizer bietet während der [Nachrichtenpersonalisierung“ Zugriff auf kontextuelle Daten aus mehreren &#x200B;](personalize.md). Sie können Arrays aus diesen Quellen mithilfe der Handlebars-Syntax in nativen Kanälen ([E-Mail](../email/get-started-email-design.md), [Push](../push/create-push.md), [SMS](../sms/create-sms.md)) durchlaufen, um dynamische Inhalte wie Produktlisten, Empfehlungen oder andere sich wiederholende Elemente anzuzeigen.

**Verfügbare Kontextquellen:**

* **[Ereignisse](#event-data)**: Daten aus Journey-Ereignissen (Geschäftsereignisse, unitäre Ereignisse)
* **[Benutzerdefinierte Aktionsantworten](#custom-action-responses)**: Daten, die von externen API-Aufrufen über benutzerdefinierte Aktionen zurückgegeben werden
* **[Datensatzsuche](#dataset-lookup)**: Angereicherte Daten, die aus Adobe Experience Platform-Datensätzen abgerufen wurden
* **[Technische Eigenschaften](#technical-properties)**: Journey von Metadaten wie Journey-ID und zusätzliche Kennungen
* **[Journey-Kontext](#other-contexts)**: Andere Journey-bezogene Daten, die während der Ausführung zugänglich sind

In diesem Handbuch erfahren Sie, wie Sie die Arrays aus den einzelnen Quellen in Ihren Nachrichten durchlaufen und wie Sie beim Konfigurieren von Journey-Aktivitäten mit Arrays arbeiten. Beginnen Sie mit [Handlebars-Iterationssyntax](#syntax) um die Grundlagen der Nachrichtenpersonalisierung zu verstehen, oder gehen Sie zu [Arbeiten mit Arrays in Journey-Ausdrücken](#arrays-in-journeys) um zu erfahren, wie Sie Array-Daten an benutzerdefinierte Aktionen und Datensatzsuchen übergeben.

## Handlebars-Iterationssyntax {#syntax}

Handlebars bietet die `{{#each}}` [Helper](functions/helpers.md) zum Iterieren über Arrays. Die grundlegende Syntax lautet:

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**Wichtigste Punkte:**

* Ersetzen Sie `arrayPath` durch den Pfad zu Ihren Array-Daten.
* Ersetzen Sie `item` durch einen beliebigen Variablennamen (z. B. `product`, `response`, `element`)
* Zugreifen auf Eigenschaften jedes Elements über `{{item.propertyName}}`
* Sie können mehrere `{{#each}}` für Arrays mit mehreren Ebenen verschachteln

## Iteration der Ereignisdaten {#event-data}

Ereignisdaten sind verfügbar, wenn Ihr Journey durch ein „Ereignis[&#x200B; ausgelöst &#x200B;](../event/about-events.md). Dies ist nützlich, um Daten anzuzeigen, die zum Zeitpunkt des Starts der Journey erfasst wurden, wie z. B. den Inhalt des Warenkorbs, Bestellelemente oder Formularübermittlungen.

>[!TIP]
>
>Sie können Ereignisdaten mit anderen Quellen kombinieren. Beispiele finden [&#x200B; unter „Kombinieren &#x200B;](#combine-sources) Kontextquellen“.

### Kontextpfad für Ereignisse

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`: Die eindeutige ID Ihres Ereignisses, wie auf der Journey konfiguriert
* `<fieldPath>`: Der Pfad zum Feld oder Array in Ihrem Ereignisschema

### Beispiel: Artikel aus einem Warenkorb-Ereignis

Wenn Ihr [Ereignisschema](../event/experience-event-schema.md) ein `productListItems`-Array enthält ([XDM-Format](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html?lang=de){target="_blank"}), können Sie den Inhalt des Warenkorbs wie im folgenden Beispiel beschrieben anzeigen.

+++ Beispiel-Code anzeigen

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

+++

### Beispiel: Verschachtelte Arrays in Ereignissen

Verwenden Sie für verschachtelte Strukturen verschachtelte `{{#each}}`.

+++ Beispiel-Code anzeigen

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

+++

Erfahren Sie mehr über die Verschachtelung in [Best Practices](#best-practices).

## Iteration über benutzerdefinierte Aktionsantworten {#custom-action-responses}

[Benutzerdefinierte Aktion](../action/about-custom-action-configuration.md) Antworten enthalten Daten, die von externen API-Aufrufen zurückgegeben werden. Dies ist nützlich für die Anzeige von Echtzeitinformationen aus Ihren Systemen, z. B. Treuepunkte, Produktempfehlungen, Bestandsstatus oder personalisierte Angebote.

>[!NOTE]
>
>Benutzerdefinierte Aktionen müssen mit einer Antwort-Payload konfiguriert werden, um diese Funktion verwenden zu können. Weitere Informationen finden Sie [&#x200B; (diesem Abschnitt](../action/action-response.md#config-response). Sie können auch benutzerdefinierte Aktionsantworten mit Ereignisdaten oder Datensatzsuchen kombinieren. Beispiele finden Sie unter [Kombinieren mehrerer &#x200B;](#combine-sources)).

### Kontextpfad für benutzerdefinierte Aktionen

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`: Der Name Ihrer [benutzerdefinierten Aktion](../action/about-custom-action-configuration.md) wie auf der Journey konfiguriert
* `<fieldPath>`: Der Pfad zum Feld oder Array in der Antwort-Payload

### Beispiel: Produktempfehlungen von einer API

Um eine Reihe von Produktempfehlungen zu durchlaufen, die von einer benutzerdefinierten Aktion zurückgegeben wurden, und sie als individuelle Karten in Ihrer Nachricht anzuzeigen, sehen Sie sich das folgende Beispiel an.

+++ Beispiel-Code anzeigen

**API-Antwort:**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**Nachrichtenpersonalisierung:**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

+++

### Beispiel: Verschachtelte Arrays aus benutzerdefinierten Aktionen

Um über eine benutzerdefinierte Aktionsantwort zu iterieren, die verschachtelte Arrays enthält (ein Array von Objekten, wobei jedes Objekt ein anderes Array enthält), sehen Sie sich das folgende Beispiel an. Dies zeigt die Verwendung verschachtelter `{{#each}}`-Schleifen für den Zugriff auf mehrere Datenebenen.

+++ Beispiel-Code anzeigen

**API-Antwort:**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**Nachrichtenpersonalisierung:**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

+++

Informationen zu komplexeren Verschachtelungsmustern finden Sie unter [Best Practices](#best-practices).

### Beispiel: Vorteile der Treuestufe

Um dynamische Vorteile basierend auf dem Treuestatus anzuzeigen, sehen Sie sich das folgende Beispiel an.

+++ Beispiel-Code anzeigen

**API-Antwort:**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**Nachrichtenpersonalisierung:**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

+++

## Iteration der Ergebnisse der Datensatzsuche {#dataset-lookup}

Mit [&#x200B; Aktivität „Datensatzsuche](../building-journeys/dataset-lookup.md) können Sie während des Journey-[&#x200B; Daten aus &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de){target="_blank"}Adobe Experience Platform-Datensätzen abrufen. Die angereicherten Daten werden als Array gespeichert und können in Ihren Nachrichten iteriert werden.

>[!AVAILABILITY]
>
>Die Aktivität Datensatzsuche ist nur für eine begrenzte Anzahl von Organisationen verfügbar. Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

Weitere Informationen zum Konfigurieren der Aktivität „Datensatzsuche“ finden Sie [&#x200B; diesem Abschnitt](../building-journeys/dataset-lookup.md). Die Datensatzsuche ist besonders leistungsstark in Kombination mit Ereignisdaten. Ein praktischer Anwendungsfall finden Sie unter [Beispiel: &#x200B;](#combine-sources) angereicherte Ereignisdaten mit Datensatzsuche .

### Kontextpfad für die Datensatzsuche

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`: Die eindeutige ID Ihrer Aktivität „Datensatzsuche“
* `entities`: Das Array der angereicherten Daten, die aus dem Datensatz abgerufen werden

### Beispiel: Produktdetails aus einem Datensatz

Wenn Sie eine Aktivität zur Datensatzsuche verwenden, um Produktinformationen basierend auf SKUs abzurufen, finden Sie unten ein Beispiel.

+++ Beispiel-Code anzeigen

**Konfiguration der Datensatzsuche:**

* Lookup keys: `list(@event{purchase_event.products.sku})`
* Zurückzugebende Felder: `["SKU", "category", "price", "name"]`

**Nachrichtenpersonalisierung:**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

+++

### Beispiel: Gefilterte Iteration mit Datensatzdaten

Verwenden Sie bedingte `{{#if}}`-Anweisungen in Ihrer `{{#each}}`-Schleife, um die Suchergebnisse des Datensatzes während der Iteration zu filtern und nur Elemente anzuzeigen, die bestimmten Kriterien entsprechen (z. B. Produkte aus einer bestimmten Kategorie). Siehe folgendes Beispiel.

+++ Beispiel-Code anzeigen

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

+++

Weitere Informationen zur bedingten Filterung finden Sie unter [Best Practices](#best-practices).

### Beispiel: Gesamtwerte aus der Datensatzsuche berechnen

Informationen zum Berechnen und Anzeigen von Gesamtsummen bei der Iteration durch die Ergebnisse der Datensatzsuche finden Sie im folgenden Beispiel.

+++ Beispiel-Code anzeigen

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

+++

## Verwenden technischer Journey-Eigenschaften {#technical-properties}

Technische Journey-Eigenschaften ermöglichen den Zugriff auf Metadaten über die Journey-Ausführung, z. B. die Journey-ID und zusätzliche Kennungen. Diese können in Kombination mit Iterationsmustern nützlich sein, insbesondere zum Filtern von Arrays basierend auf bestimmten Journey-Instanzen.

### Verfügbare technische Eigenschaften

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### Beispiel: Filtern von Array-Elementen mithilfe einer zusätzlichen Kennung

Bei Verwendung zusätzlicher IDs in ereignisgesteuerten Journey mit Arrays können Sie so filtern, dass nur das für die aktuelle Journey-Instanz relevante Element angezeigt wird. Weitere Informationen zu zusätzlichen Kennungen finden Sie in [diesem Handbuch](../building-journeys/supplemental-identifier.md).

**Szenario**: Bei mehreren Buchungen wird eine Journey ausgelöst, Sie möchten jedoch nur Informationen zu der spezifischen Buchung anzeigen (identifiziert durch eine zusätzliche ID), die diese Journey-Instanz ausgelöst hat.

+++ Beispiel-Code anzeigen

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

+++

### Beispiel: Journey-ID für Tracking einschließen

Um die Journey-ID zu Tracking-Zwecken in Ihre Nachricht aufzunehmen, sehen Sie sich das folgende Beispiel an.

+++ Beispiel-Code anzeigen

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

+++

## Kombinieren mehrerer Kontextquellen {#combine-sources}

Sie können Daten aus verschiedenen Quellen in derselben Nachricht kombinieren, um umfassende, personalisierte Erlebnisse zu schaffen. Dieser Abschnitt zeigt praktische Beispiele für die gemeinsame Verwendung mehrerer Kontextquellen.

**Kontextquellen, die Sie kombinieren können:**

* [Ereignisdaten](#event-data) + [Benutzerdefinierte Aktionsantworten](#custom-action-responses)
* [Ereignisdaten](#event-data) + [Datensatzsuche](#dataset-lookup)
* [Mehrere Quellen](#combine-sources) + [Technische Eigenschaften](#technical-properties)

### Beispiel: Artikel im Warenkorb mit Echtzeit-Inventar

Um Ereignisdaten (Warenkorbinhalte) mit benutzerdefinierten Aktionsdaten (Inventarstatus) zu kombinieren, sehen Sie sich das folgende Beispiel an.

+++ Beispiel-Code anzeigen

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### Beispiel: Ereignisdaten angereichert mit Datensatzsuche

Um [Ereignis-SKUs](#event-data) mit detaillierten Produktinformationen aus einer [Datensatzsuche](#dataset-lookup) zu kombinieren, sehen Sie sich das folgende Beispiel an.

+++ Beispiel-Code anzeigen

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

+++

### Beispiel: Kombinieren mehrerer Quellen mit technischen Eigenschaften

Um mehrere Kontextquellen (Profildaten, Ereignisdaten, benutzerdefinierte Aktionen und technische Eigenschaften) in einer einzigen Nachricht zu kombinieren, sehen Sie sich das folgende Beispiel an.

+++ Beispiel-Code anzeigen

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

+++

## Andere Kontexttypen {#other-contexts}

Während sich dieses Handbuch auf die Iteration über Arrays konzentriert, stehen andere Kontexttypen für die Personalisierung zur Verfügung, die in der Regel keine Iteration erfordert. Auf diese wird direkt zugegriffen, anstatt sie in Schleifen zu überschreiben:

* **[Profilattribute](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target="_blank"}** (`profile.*`): Einzelne Profilfelder aus Adobe Experience Platform
* **[Audiences](../audience/about-audiences.md)** (`inAudience()`): Prüfungen der Zielgruppenzugehörigkeit
* **[Angebotsentscheidungen](../offers/get-started/starting-offer-decisioning.md)**: Entscheidungs-Management-Angebote
* **[Zielattribute](../orchestrated/activities/channels.md#add-personalization)** (nur orchestrierte Kampagnen): Auf der Kampagnen-Arbeitsfläche berechnete Attribute
* **Token** (`context.token`): Sitzungs- oder Authentifizierungs-Token

Die vollständige Personalisierungssyntax und Beispiele, die diese Quellen verwenden, finden Sie unter:

* [Hinzufügen von Personalisierung](personalization-build-expressions.md)
* [Personalisierungssyntax](personalization-syntax.md)

## Arbeiten mit Arrays in Journey-Ausdrücken {#arrays-in-journeys}

Während sich die vorherigen Abschnitte auf die Iteration über Arrays bei der Nachrichtenpersonalisierung mithilfe von Handlebars konzentrieren, können Sie beim Konfigurieren von Journey-Aktivitäten auch mit Arrays arbeiten. In diesem Abschnitt wird erläutert, wie Sie Array-Daten aus Ereignissen in Journey-Ausdrücken verwenden, insbesondere wenn Sie Daten an benutzerdefinierte Aktionen übergeben oder Arrays mit Datensatzsuchen verwenden.

>[!IMPORTANT]
>
>Journey-Ausdrücke verwenden eine andere Syntax als die Handlebars-Personalisierung. In der Journey-Konfiguration (z. B. mit benutzerdefinierten Aktionsparametern oder Bedingungen) verwenden Sie den [Journey-Ausdruckseditor](../building-journeys/expression/expressionadvanced.md) mit Funktionen wie `first`, `all` und `serializeList`. Im Nachrichteninhalt verwenden Sie die Handlebars-Syntax mit `{{#each}}`.

### Übergeben von Array-Werten an benutzerdefinierte Aktionsparameter {#arrays-to-custom-actions}

Beim Konfigurieren [benutzerdefinierter Aktionen](../action/about-custom-action-configuration.md) müssen Sie häufig Werte aus Ereignis-Arrays extrahieren und als Parameter übergeben. In diesem Abschnitt werden gängige Muster behandelt.

Weitere Informationen zum Übergeben von Sammlungen in [Übergeben von Sammlungen in benutzerdefinierte Aktionsparameter](../building-journeys/collections.md#passing-collection).

#### Extrahieren eines einzelnen Werts aus einem Array

**Anwendungsfall**: Abrufen eines bestimmten Felds aus einem Ereignis-Array, das als Abfrageparameter in einer GET-Anfrage übergeben wird.

+++ Beispiel-Code anzeigen

**Beispielszenario**: Extrahieren Sie die erste SKU mit einem Preis größer als 0 aus einer Produktliste.

**Beispiel für ein**:

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**Konfiguration benutzerdefinierter Aktionen**:

1. Konfigurieren Sie in Ihrer benutzerdefinierten Aktion einen Abfrageparameter (z. B. `sku`) vom Typ `string`
2. Als `Variable` markieren, um dynamische Werte zuzulassen

**Journey-Ausdruck im Aktionsparameter**:

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**Erläuterung**:

* `@event{YourEventName}`: Verweist auf Ihr Journey-Ereignis
* `.first(currentEventField.condition)`: Gibt das erste Array-Element zurück, das der Bedingung entspricht
* `currentEventField`: Stellt jedes Element im Ereignis-Array dar, während Sie es durchlaufen
* `.SKU`: Extrahiert das SKU-Feld aus dem zugeordneten Element
* Ergebnis: `"SKU-1"` (eine für den Aktionsparameter geeignete Zeichenfolge)

Erfahren Sie mehr über die `first` in [Funktionen zur Sammlungsverwaltung](../building-journeys/expression/collection-management-functions.md).

+++

#### Erstellen einer Werteliste aus einem Array

**Anwendungsfall**: Erstellen einer kommagetrennten Liste von IDs, die als Abfrageparameter übergeben werden (z. B. `/products?ids=sku1,sku2,sku3`).

+++ Beispiel-Code anzeigen

**Konfiguration benutzerdefinierter Aktionen**:

1. Konfigurieren Sie einen Abfrageparameter (z. B. `ids`) vom Typ `string`
2. Als `Variable` markieren

**Journey-Ausdruck**:

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**Erläuterung**:

* `.all(currentEventField.condition)`: Gibt alle Array-Elemente zurück, die der Bedingung entsprechen (gibt eine Liste zurück)
* `currentEventField`: Stellt jedes Element im Ereignis-Array dar, während Sie es durchlaufen
* `.SKU`: Projekte in der Liste, die nur SKU-Werte enthalten sollen
* `serializeList(list, delimiter, addQuotes)`: Fügt die Liste zu einer Zeichenfolge zusammen
   * `","`: Komma als Trennzeichen verwenden
   * `true`: Hinzufügen von Anführungszeichen um jedes Zeichenfolgenelement
* Ergebnis: `"SKU-1,SKU-3"` (für einen Abfrageparameter geeignet)

Weitere Informationen über:

* [`all`](../building-journeys/expression/collection-management-functions.md)
* [`serializeList`](../building-journeys/functions/list-functions.md#serializeList)

Die Verarbeitung von Sammlungen für benutzerdefinierte Aktionen wird unter [Übergeben von Sammlungen an benutzerdefinierte Aktionsparameter](../building-journeys/collections.md#passing-collection) beschrieben.

+++

#### Übergeben eines Arrays von Objekten an eine benutzerdefinierte Aktion

**Anwendungsfall**: Senden eines vollständigen Arrays von Objekten in einem Anfrageinhalt (für POST oder GET mit Hauptteil).

+++ Beispiel-Code anzeigen

**Beispiel für einen Anfragetext**:

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**Konfiguration benutzerdefinierter Aktionen**:

1. Definieren Sie im Anfragetext `products` als Typ `listObject`
2. Als `Variable` markieren
3. Definieren der Objektfelder: `id`, `name`, `price`, `color` (jedes wird zuordnungsfähig)

**Journey-Arbeitsfläche-Konfiguration**:

1. Legen Sie im erweiterten Modus den Sammlungsausdruck fest:

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. In der Benutzeroberfläche für die Sammlungszuordnung:
   * `id` → `productListItems.SKU` zuordnen
   * `name` → `productListItems.name` zuordnen
   * `price` → `productListItems.priceTotal` zuordnen
   * `color` → `productListItems.color` zuordnen

Journey Optimizer erstellt das Array von Objekten, die Ihrer Aktions-Payload-Struktur entsprechen.

>[!NOTE]
>
>Verwenden Sie beim Arbeiten mit Ereignis-Arrays `currentEventField` , um auf jedes Element zu verweisen. Verwenden Sie für Datenquellensammlungen (Adobe Experience Platform) `currentDataPackField`. Verwenden Sie für Sammlungen von benutzerdefinierten Aktionsantworten `currentActionField`.

Weitere Informationen finden Sie unter [Übergeben von Sammlungen an benutzerdefinierte Aktionsparameter](../building-journeys/collections.md#passing-collection).

+++

### Verwenden von Arrays mit Datensatzabfragen {#arrays-with-dataset-lookup}

Bei Verwendung der Aktivität [Datensatzsuche](../building-journeys/dataset-lookup.md) können Sie ein Array von Werten als Lookup-Schlüssel übergeben, um angereicherte Daten abzurufen.

**Beispiel**: Produktdetails für alle SKUs in einem Ereignis-Array nachschlagen.

+++ Beispiel-Code anzeigen

**Konfiguration der Datensatzsuche**:

Verwenden Sie im Feld Suchschlüssel `list()` , um einen Array-Pfad in eine Liste zu konvertieren:

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

Dadurch wird eine Liste aller SKU-Werte erstellt, die im Datensatz nachgeschlagen werden sollen. Die Ergebnisse sind als Array `context.journey.datasetLookup.<activityID>.entities` verfügbar, über das Sie in Ihrer Nachricht iterieren können (siehe [Iterieren der Ergebnisse der Datensatzsuche](#dataset-lookup)).

+++

### Einschränkungen und Muster {#array-limitations}

Beachten Sie diese Einschränkungen beim Arbeiten mit Arrays in Journey:

#### Keine dynamische Schleife über Arrays im Journey-Fluss

Journey können keine dynamischen Schleifen erstellen, bei denen ein Aktionsknoten mehrmals für jedes Element in einem Array ausgeführt wird. Dadurch sollen Ausreißer-Leistungsprobleme verhindert werden.

**Was Sie nicht tun können**:

* Eine benutzerdefinierte Aktion einmal pro Array-Element dynamisch ausführen
* Erstellen mehrerer Journey-Verzweigungen basierend auf der Array-Länge

**Empfohlene Muster stattdessen**:

1. **Alle Elemente gleichzeitig senden**: Übergeben Sie das gesamte Array oder eine serialisierte Liste an eine einzelne benutzerdefinierte Aktion, die alle Elemente verarbeitet. Siehe [Erstellen einer Werteliste aus einem Array](#arrays-to-custom-actions).

2. **Externe Aggregation verwenden**: Lassen Sie Ihre externe API mehrere IDs akzeptieren und kombinierte Ergebnisse in einem einzigen Aufruf zurückgeben.

3. **Vorberechnen in AEP**: Verwenden Sie [berechnete Attribute](../audience/computed-attributes.md) um Werte aus Arrays auf Profilebene vorab zu berechnen.

4. **Einzelwertextraktion**: Wenn Sie nur einen Wert benötigen, extrahieren Sie ihn mithilfe von `first` oder `head`. Siehe [Extrahieren eines einzelnen Werts aus einem Array](#arrays-to-custom-actions).

Weitere Informationen finden Sie unter [Leitplanken und Einschränkungen](../start/guardrails.md).

#### Überlegungen zur Array-Größe

Große Arrays können die Journey-Leistung beeinträchtigen:

* **Ereignis-Arrays**: Ereignis-Payloads unter insgesamt 50 KB halten
* **Benutzerdefinierte Aktionsantworten**: Antwort-Payloads sollten unter 100 KB sein
* **Ergebnisse der Datensatzsuche**: Anzahl der Lookup-Schlüssel und zurückgegebenen Entitäten begrenzen

### Vollständiges Beispiel: Ereignis-Array für benutzerdefinierte Aktion {#complete-example}

Im Folgenden finden Sie einen vollständigen Workflow, der zeigt, wie ein Ereignis-Array mit einer benutzerdefinierten Aktion verwendet wird.

**Szenario**: Wenn ein Benutzer seinen Warenkorb verlässt, senden Sie Warenkorbdaten an eine externe Recommendations-API, um personalisierte Vorschläge zu erhalten, und zeigen Sie diese dann in einer E-Mail an.

+++ Beispiel-Code anzeigen

**Schritt 1: Konfigurieren der benutzerdefinierten Aktion**

Erstellen Sie eine benutzerdefinierte Aktion „GetCartRecommendations“:

* **Methode**: POST
* **URL**: `https://api.example.com/recommendations`
* **Anfragetext**:

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* `cartItems` als Typ `listObject` und `Variable` markieren
* Felder definieren: `sku` (Zeichenfolge), `price` (Zahl), `quantity` (Ganzzahl)

Weitere Informationen finden Sie unter [Konfigurieren einer benutzerdefinierten Aktion](../action/about-custom-action-configuration.md).

**Schritt 2: Antwort-Payload konfigurieren**

Konfigurieren Sie in der benutzerdefinierten Aktion die Antwort:

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

Weitere Informationen finden Sie unter [Verwenden von API-Aufrufantworten](../action/action-response.md).

**Schritt 3: Verdrahten Sie die Aktion in der Journey**

1. Fügen Sie nach dem Warenkorbabbruch-Ereignis die benutzerdefinierte Aktion hinzu
1. Im erweiterten Modus für die `cartItems`:

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. Zuordnen der Sammlungsfelder:
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**Schritt 4: Antwort in E-Mail verwenden**

Iterieren Sie in Ihrem E-Mail-Inhalt über die Empfehlungen:

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**Schritt 5: Testen Sie Ihre Konfiguration**

Bevor Sie eine Live-Journey ausführen, testen Sie die benutzerdefinierte Aktion mit der Funktion „Testanfrage senden“ in der Aktionskonfiguration, um die erstellte Anfrage und die Werte zu überprüfen.

1. [Journey-Testmodus verwenden](../building-journeys/testing-the-journey.md)
2. Trigger mit Beispielereignisdaten, einschließlich eines `productListItems` Arrays
3. Überprüfen, ob die benutzerdefinierte Aktion die richtige Array-Struktur erhält
4. Überprüfen Sie die [Aktionstestprotokolle](../action/action-response.md#test-mode-logs)
5. Vorschau der E-Mail zur Bestätigung, dass beide Arrays korrekt angezeigt werden

Weitere Informationen finden Sie unter [Fehlerbehebung bei benutzerdefinierten Aktionen](../action/troubleshoot-custom-action.md).

+++

## Best Practices {#best-practices}

Befolgen Sie diese Best Practices bei der Iteration über kontextuelle Daten, um eine verwaltbare, leistungsstarke Personalisierung zu erstellen.

### Verwenden beschreibender Variablennamen

Wählen Sie Variablennamen, die klar angeben, worüber Sie iterieren. Dadurch wird der Code besser lesbar und leichter zu verwalten. Weitere Informationen über [Personalisierungssyntax](personalization-syntax.md):

+++ Beispiel-Code anzeigen

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

+++

### Ausdrucksfragmente in Schleifen

Wenn Sie [Ausdrucksfragmente](use-expression-fragments.md) in `{{#each}}` Schleifen verwenden, beachten Sie, dass Sie keine Variablen mit Schleifenbereich als Fragmentparameter übergeben können. Fragmente können jedoch auf globale Variablen zugreifen, die im Nachrichteninhalt außerhalb des Fragments definiert sind.

+++ Beispiel-Code anzeigen

**Unterstütztes Muster - Globale Variablen verwenden:**

```handlebars
{% let globalDiscount = 15 %}

{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{fragment id='ajo:fragment123/variant456' mode='inline'}}
  </div>
{{/each}}
```

Das Fragment kann auf `globalDiscount` verweisen, da es global in der Nachricht definiert ist.

**Nicht unterstützt - Übergeben von Schleifenvariablen:**

```handlebars
{{#each products as |product|}}
  <!-- This will NOT work as expected -->
  {{fragment id='ajo:fragment123/variant456' currentProduct=product}}
{{/each}}
```

**Problemumgehung**: Fügen Sie die Personalisierungslogik direkt in Ihre Schleife ein, anstatt ein Fragment zu verwenden, oder rufen Sie das Fragment außerhalb der Schleife auf.

+++

Erfahren Sie mehr über [Verwendung von Ausdrucksfragmenten in Schleifen](use-expression-fragments.md#fragments-in-loops) einschließlich detaillierter Beispiele und zusätzlicher Problemumgehungen.



### Verarbeiten leerer Arrays

Verwenden Sie die `{{else}}`-Klausel, um Fallback-Inhalte bereitzustellen, wenn ein Array leer ist. Weitere Informationen zu [Hilfsfunktionen](functions/helpers.md):

+++ Beispiel-Code anzeigen

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

+++

### Kombinieren mit bedingten Helfern

Verwenden Sie `{{#if}}` in Schleifen für bedingte Inhalte. Weitere Informationen zu [bedingten Regeln](create-conditions.md) und Beispiele finden Sie [&#x200B; den Abschnitten Benutzerdefinierte &#x200B;](#custom-action-responses)und [Datensatzsuche](#dataset-lookup).

+++ Beispiel-Code anzeigen

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### Iteration auf Leistung begrenzen

Bei großen Arrays sollten Sie die Anzahl der Iterationen einschränken:

+++ Beispiel-Code anzeigen

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

+++

### Zugriff auf Array-Metadaten

Handlebars bieten spezielle Variablen in Schleifen, die bei erweiterten Iterationsmustern helfen:

* `@index`: Aktueller Iterationsindex (0-basiert)
* `@first`: True für die erste Iteration
* `@last`: True für die letzte Iteration

+++ Beispiel-Code anzeigen

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

+++

>[!NOTE]
>
>Diese Handlebars-Variablen (`@index`, `@first`, `@last`) sind nur in `{{#each}}` Schleifen der Nachrichtenpersonalisierung verfügbar. Verwenden Sie zum Arbeiten mit Arrays in Journey-Ausdrücken (z. B. Abrufen des ersten Elements aus einem Array vor der Übergabe an eine benutzerdefinierte Aktion) Array-Funktionen wie [`head`](../personalization/functions/arrays-list.md#head), [`first`](../building-journeys/expression/collection-management-functions.md) oder [`all`](../building-journeys/expression/collection-management-functions.md). Weitere [&#x200B; finden Sie unter „Arbeiten mit Arrays &#x200B;](#arrays-in-journeys) Journey-Ausdrücken“.

## Fehlerbehebung {#troubleshooting}

Haben Sie Probleme mit der Iteration? In diesem Abschnitt werden gängige Probleme und Lösungen behandelt.

### Array wird nicht angezeigt

**Problem**: Ihre Array-Iteration zeigt keine Inhalte an.

+++ Mögliche Ursachen und Lösungen anzeigen

**Mögliche Ursachen und**:

1. **Falscher Pfad**: Überprüfen Sie den genauen Pfad zu Ihrem Array basierend auf der Kontextquelle:
   * Für [Ereignisse](#event-data): `context.journey.events.<event_ID>.<fieldPath>`
   * Für [benutzerdefinierte Aktionen](#custom-action-responses): `context.journey.actions.<actionName>.<fieldPath>`
   * Für [Datensatzsuche](#dataset-lookup): `context.journey.datasetLookup.<activityID>.entities`

2. **Array ist leer**: Fügen Sie eine `{{else}}` hinzu, um zu überprüfen, ob das Array keine Daten enthält. Beispiele finden [&#x200B; unter &#x200B;](#best-practices) Practices .

3. **Daten noch nicht verfügbar**: Stellen Sie sicher, dass die benutzerdefinierte Aktion, das Ereignis oder die Datensatz-Suchaktivität vor der Nachrichtenaktivität in Ihrem Journey-Fluss ausgeführt wurde.

+++

### Syntaxfehler

**Problem**: Die Ausdrucksvalidierung schlägt fehl oder die Nachricht wird nicht gerendert.

+++ Häufige Fehler anzeigen

**Häufige**:

* Fehlende schließende Tags: Jedes `{{#each}}` muss über ein `{{/each}}` verfügen. Überprüfen Sie [Handlebars-Iterationssyntax](#syntax) auf die richtige Struktur.
* Falscher Variablenname: Stellen Sie sicher, dass der Variablenname im gesamten Block konsistent verwendet wird. Siehe [Best Practices](#best-practices) für Namenskonventionen.
* Falsche Pfadtrennzeichen: Verwenden Sie Punkte (`.`) anstelle von Schrägstrichen oder anderen Zeichen

+++

### Ausdrucksfragmente funktionieren nicht in Schleifen

**Problem**: Ein Ausdrucksfragment zeigt nicht den erwarteten Inhalt an, wenn es in einer `{{#each}}` verwendet wird, oder zeigt eine leere/unerwartete Ausgabe an.

+++ Mögliche Ursachen und Lösungen anzeigen

**Mögliche Ursachen und**:

1. **Versuch, Schleifenvariablen als Parameter zu übergeben**: Ausdrucksfragmente können keine Variablen mit Schleifenumfang (wie das aktuelle Iterationselement) als Parameter empfangen. Dies ist eine bekannte Einschränkung.

   **Lösung**: Verwenden Sie eine der folgenden Problemumgehungen:

   * Definieren Sie globale Variablen in Ihrer Nachricht, auf die das Fragment zugreifen kann
   * Personalisierungslogik direkt in die Schleife einbinden, anstatt ein Fragment zu verwenden
   * Rufen Sie das Fragment außerhalb der Schleife auf, wenn es keine schleifenspezifischen Daten benötigt

2. **Fragment erwartet einen Parameter, der nicht verfügbar ist**: Wenn Ihr Fragment für den Empfang bestimmter Eingabeparameter konzipiert wurde, funktioniert es nicht ordnungsgemäß, wenn diese Parameter nicht aus einer Schleife heraus übergeben werden können.

   **Lösung**: Strukturieren Sie Ihren Ansatz so um, dass globale Variablen verwendet werden, auf die das Fragment zugreifen kann. Beispiele finden [&#x200B; unter „Best Practices - Ausdrucksfragmente in &#x200B;](#best-practices)&quot;.

3. **Falscher Variablenbereich**: Das Fragment versucht möglicherweise, auf eine Variable zu verweisen, die nur innerhalb des Schleifenbereichs vorhanden ist.

   **Lösung**: Definieren Sie alle Variablen, die das Fragment benötigt, auf Nachrichtenebene (außerhalb der Schleife), damit sie global zugänglich sind.

Erfahren Sie mehr über [Verwendung von Ausdrucksfragmenten in Schleifen](use-expression-fragments.md#fragments-in-loops) einschließlich detaillierter Erläuterungen, Beispiele und empfohlener Muster.

+++

### Testen von Iterationen

Verwenden Sie den [Journey-Testmodus](../building-journeys/testing-the-journey.md) um Ihre Iterationen zu überprüfen. Dies ist besonders wichtig bei der Verwendung von [benutzerdefinierten Aktionen](#custom-action-responses) oder [Datensatzsuchen](#dataset-lookup):

+++ Testschritte anzeigen

1. Journey im [&#x200B; starten](../building-journeys/testing-the-journey.md)
2. Trigger des Ereignisses oder der benutzerdefinierten Aktion mit Beispieldaten
3. Überprüfen Sie die [Nachrichtenvorschau](../content-management/preview.md), um sicherzustellen, dass die Iteration korrekt angezeigt wird
4. Überprüfen Sie die Testmodusprotokolle auf Fehler (siehe [Testmodusprotokolle für benutzerdefinierte Aktionen](../action/action-response.md#test-mode-logs))

+++

## Verwandte Themen {#related-topics}

**Personalization-Grundlagen:** [Erste Schritte mit der Personalisierung](personalize.md) | [Personalisierung hinzufügen](personalization-build-expressions.md) | [Personalization-Syntax](personalization-syntax.md) | [Hilfsfunktionen](functions/helpers.md) | [Erstellen von bedingten Regeln](create-conditions.md)

**Journey-Konfiguration:** [Über Ereignisse](../event/about-events.md) | [Konfigurieren von benutzerdefinierten Aktionen](../action/about-custom-action-configuration.md) | [Übergeben von Sammlungen in benutzerdefinierte Aktionsparameter](../building-journeys/collections.md#passing-collection) | [Verwenden von API-Aufrufantworten in benutzerdefinierten Aktionen](../action/action-response.md) | [Fehlerbehebung bei benutzerdefinierten Aktionen](../action/troubleshoot-custom-action.md) | [Verwenden von Adobe Experience Platform-Daten in Journey](../building-journeys/dataset-lookup.md) | [Zusätzliche Kennungen in Journey verwenden](../building-journeys/supplemental-identifier.md) | [Leitplanken und Einschränkungen](../start/guardrails.md) | [Journey testen](../building-journeys/testing-the-journey.md)

**Journey-Ausdrucksfunktionen:** [Erweiterter Ausdruckseditor](../building-journeys/expression/expressionadvanced.md) | [Funktionen zur Sammlungsverwaltung](../building-journeys/expression/collection-management-functions.md) (zunächst alle, zuletzt) | [Listenfunktionen](../building-journeys/functions/list-functions.md) (serializeList, filter, sort) | [Array-Funktionen](../personalization/functions/arrays-list.md) (Kopf, Schwanz)

**Personalization-Anwendungsfälle:** [E-Mail zu Warenkorbabbruch](personalization-use-case-helper-functions.md) | [Benachrichtigung zum Bestellstatus](personalization-use-case.md)

**Nachrichtendesign:** [Erste Schritte beim Gestalten von E-Mails](../email/get-started-email-design.md) | [Push-Benachrichtigungen erstellen](../push/create-push.md) | [Erstellen von SMS-Nachrichten](../sms/create-sms.md) | [Vorschau und Testen von Inhalten](../content-management/preview-test.md)

