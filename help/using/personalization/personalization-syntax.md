---
title: Personalisierungssyntax
description: Erfahren Sie, wie Sie die Personalisierungssyntax verwenden
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Personalisierungssyntax {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## Einführung

Die Personalisierung in Journey Optimizer basiert auf der Vorlagensyntax Handlebars.
Eine vollständige Beschreibung der Handlebars-Syntax finden Sie unter [HandlebarsJS](https://handlebarsjs.com/).

Es verwendet eine Vorlage und ein Eingabeobjekt, um HTML oder andere Textformate zu generieren. Handlebars-Vorlagen sehen wie normaler Text mit eingebetteten Handlebars-Ausdrücken aus.

Einfaches Ausdruck-Beispiel:

```
{{profile.person.name}}
```

where:

* **profileis** ein Namensraum.
* **person.** nameis ist ein Token, das aus Attributen besteht. Die Attributstruktur wird in einem Adobe Experience Platform XDM-Schema definiert. [Mehr dazu](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

## Allgemeine Syntaxregeln

Bezeichner können beliebige Unicode-Zeichen sein, mit Ausnahme der folgenden:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

Bei der Syntax wird zwischen Groß- und Kleinschreibung unterschieden.

Die Wörter **true**, **false**, **null** und **undefined** sind nur im ersten Ausdruck eines Pfades zulässig.

In Handlebars sind die von {{Ausdruck}} zurückgegebenen Werte **HTML-Escaped**. Wenn der Ausdruck &quot;&amp;&quot;enthält, wird die zurückgegebene Ausgabe mit HTML-Escape-Zeichen als &amp; generiert. Wenn Sie nicht möchten, dass Handlebars einem Wert entkommen, verwenden Sie den &quot;Triple-Stash&quot;.

## Profil

Mit diesem Namensraum können Sie auf alle Attribute verweisen, die im Profil-Schema definiert sind, das unter [Adobe Experience Platform Data Model (XDM) documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) beschrieben wird.

Die Attribute müssen im Schema definiert werden, bevor sie in einem Journey Optimizer-Personalisierungsblock referenziert werden.

Alle Verweise werden mit einem Überprüfungsmechanismus validiert, der [hier](personalization-validation.md) beschrieben wird, und zwar mit einem Profil-Schema.

**Beispielverweise:**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**E-Mail-Adresserweiterung** bestimmen:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## Segmente

Weitere Informationen zum Segmentierungs- und Segmentierungsdienst finden Sie in diesem [Abschnitt](../segment/about-segments.md).

**Sie können unterschiedliche Inhalte basierend auf der Segmentmitgliedschaft** rendern:

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**Stellen Sie fest, ob ein Profil bereits Mitglied** ist:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## Angebote

In diesem Namensraum können Sie auf bestehende Angebote verweisen.
Um auf ein Angebot zu verweisen, müssen Sie einen Pfad mit den verschiedenen Informationen angeben, die ein Angebot definieren.

Dieser Pfad hat die folgende Struktur:
0 - &quot;Angebote: identifiziert den Pfad-Ausdruck, der zu Angebot Namensraum gehört
1 - Typ: bestimmt den Typ der Angebotsdarstellung. Gültige Werte sind &quot;image&quot;, &quot;html&quot;und &quot;text&quot;
2 - Platzierungs-ID
3 - Aktivitäten-ID
4 - Angebot-spezifische Attribute. Je nach Angebot können unterstützte Attribute verwendet werden. Beispiel für Bilder `deliveryUrl`.

Weitere Informationen zur Entscheidungen-API finden Sie auf dieser [Seite](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api)

Weitere Informationen zur Darstellung von Angeboten finden Sie auf dieser [Seite](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers).

Alle Verweise werden mit einem Überprüfungsmechanismus validiert, der [hier](personalization-validation.md) beschrieben wird, und zwar mit einem Angebot-Schema.

**Beispielverweise:**

* Speicherort, an dem das Bild gehostet wird:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* Zielgruppen-URL beim Klicken auf das Bild:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* Textinhalt des Angebots aus der Entscheidungsmaschine:

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* HTML-Inhalt des Angebots aus der Entscheidungsmaschine:

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## Helfer

Ein Handlebars Helper ist ein einfacher Bezeichner, dem Parameter folgen können.
Jeder Parameter ist ein Handlebars-Ausdruck. Diese Helfer können von jedem beliebigen Kontext in einer Vorlage aufgerufen werden.

Diese Blockhelfer werden durch ein # identifiziert, das dem Helfernamen vorausgeht, und erfordern ein passendes Schließen /, mit demselben Namen.
Blöcke sind Ausdruck mit Blocköffnungs- ({{# }}) und -schließenden ({{/}}).

### if

Der Helfer **if** wird zum Definieren eines bedingten Blocks verwendet.
Wenn die Auswertung des Ausdrucks &quot;true&quot;zurückgibt, wird der Block gerendert, andernfalls wird er übersprungen.

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Nach dem Helfer **if** können Sie eine **else**-Anweisung eingeben, um einen Codeblock anzugeben, der ausgeführt werden soll, wenn dieselbe Bedingung &quot;false&quot;lautet.
Die **else if**-Anweisung gibt eine neue Testbedingung an, wenn die erste Anweisung &quot;false&quot;zurückgibt.

**Verschiedene Store-Links basierend auf bedingten Ausdrücken** rendern:

```
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### Sofern

**#** unlesshelper wird verwendet, um einen bedingten Block zu definieren. Wenn die Auswertung des Ausdrucks &quot;false&quot;zurückgibt, wird der Block entgegen dem Helfer **#if** gerendert.

**Rendering einiger Inhalte basierend auf der E-Mail-Adresserweiterung**:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### Jeder

Der **Jeder**-Helfer wird verwendet, um über ein Array zu iterieren.
Die Syntax des Helfers ist ```{{#each ArrayName}}``` YourContent {{/each}}
Wir können auf die einzelnen Array-Elemente verweisen, indem wir den Suchbegriff **this** innerhalb des Blocks verwenden. Der Index des Elements des Arrays kann mithilfe von {{@index}} gerendert werden.

Beispiel:

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Eine Liste von Produkten, die dieser Benutzer im Warenkorb** hat, rendern:

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### with

Der **#with**-Helfer wird verwendet, um das Bewertungstoken des Vorlagenteils zu ändern.

Beispiel:

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Der **#with**-Helfer ist nützlich, um auch eine Kontextvariable zu definieren.

**Verwenden Sie dies zum Aliasing langer Variablennamen für kürzere**:

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## Einschränkungen

* Die Verwendung der Variablen **xEvent** ist in Personalisierungs-Ausdrücken nicht verfügbar. Jeder Verweis auf xEvent führt zu Überprüfungsfehlern.
