---
solution: Journey Optimizer
product: journey optimizer
title: Personalisierungssyntax
description: Erfahren Sie, wie Sie die Personalisierungssyntax verwenden.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: Ausdruck, Editor, Syntax, Personalisierung
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
  - id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1299
ht-degree: 48%

---

# Personalisierungssyntax {#personalization-syntax}

Personalization in [!DNL Journey Optimizer] verwendet zwei komplementäre Syntaxen, die im selben Ausdruck zusammenarbeiten:

* **Handlebars** (`{{...}}`) - Wird zum Rendern von Profilattributen, zum Durchlaufen von Arrays und zum Aufrufen von Block-Helfern verwendet. Eine vollständige Referenz finden [&#x200B; in der &#x200B;](https://handlebarsjs.com/) zu HandlebarsJS .
* **Profile Query Language (PQL)** (`{%= ... %}`) - Wird zum Aufrufen integrierter Funktionen (z. B. `upperCase()`, `formatDate()`, `dateDiff()`) und zum Auswerten bedingter Ausdrücke verwendet.

Um Laufzeitfehler zu vermeiden, ist es von entscheidender Bedeutung zu verstehen, in welchem Kontext Sie sich befinden. Beispielsweise schlägt ein in `{{...}}` platzierter PQL-Funktionsaufruf fehl, weil Handlebars versucht, ihn als Helper aufzulösen, anstatt ihn als PQL-Ausdruck zu bewerten.

**Beispiele:**

| Anwendungsfall | Syntax |
|----------|--------|
| Rendern eines Profilattributs | `{{profile.person.name.firstName}}` |
| Aufrufen einer PQL-Funktion | `{%= upperCase(profile.person.name.firstName) %}` |
| Bedingter Block | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| Über ein Array schleifen | `{{#each profile.orders}}...{{/each}}` |

Die Attributstruktur wird in einem XDM-Schema von Adobe Experience Platform definiert. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}.

>[!TIP]
>
>Gebrauchsfertige Ausdrücke, die diese Syntaxen auf reale Szenarien anwenden - Datumsformatierung, Countdowns, bedingte Fallbacks und mehr - finden Sie auf der Seite **[Personalization-Rezepte](personalization-recipes.md)**.

## Allgemeine Syntaxregeln {#general-rules}

* Kennungen können beliebige Unicode-Zeichen sein, mit Ausnahme der folgenden Sonderzeichen, die für die Handlebars-Syntax reserviert sind:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* Die Syntax unterscheidet zwischen Groß- und Kleinschreibung.

* Die Wörter **true**, **false**, **null** und **undefined** sind nur im ersten Teil eines Pfadausdrucks zulässig.

* In Handlebars werden den von {{expression}} zurückgegebenen Werten **HTML-Escape-Zeichen hinzugefügt**. Wenn der Ausdruck „`&`“ enthält, wird die Ausgabe mit HTML-Escape-Zeichen als „`&amp;`“ generiert. Wenn Sie wünschen, dass Handlebars einen Wert nicht escapen, verwenden Sie drei geschweifte Klammern.

  Angenommen, der Wert des Felds `profile.person.name` lautet „Mark &amp; Mary“. Die Syntax `{{profile.person.name}}` zeigt `Mark &amp; Mary` an, während `{{{profile.person.name}}}` `Mark & Mary` anzeigt.

* Bezüglich der Argumente für Literalfunktionen unterstützt der Sprach-Parser für Vorlagen keinen einfachen umgekehrten Schrägstrich ohne Escape-Sequenz (`\`). Dieses Zeichen muss mit einem zusätzlichen umgekehrten Schrägstrich (`\`) mit Escape-Sequenz versehen werden. Beispiel:

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* Um ein **literales doppeltes Anführungszeichen** in einen Zeichenfolgenwert einzuschließen (z. B. beim Generieren einer JSON-Ausgabe), Escape-Zeichen mit einem umgekehrten Schrägstrich (`\"`):

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  Ausgabe: `{ "message": "Hello \"John\"" }`

  Alternativ können Sie die Triple-Stash-`{{{ }}}` verwenden, um HTML ohne Escape-Zeichen auszugeben, wenn der Wert selbst Sonderzeichen enthält, die nicht in HTML codiert werden sollen.

## Reservierte Keywords {#reserved-keywords}

Bestimmte Keywords sind in Profile Query Language (PQL) reserviert und können nicht direkt als Feld- oder Variablennamen in Personalisierungsausdrücken verwendet werden. Wenn Ihr XDM-Schema Felder mit Namen enthält, die reservierten Keywords entsprechen, müssen Sie diese mit Backticks (`` ` ``) maskieren, wenn Sie in Ihren Ausdrücken darauf verweisen möchten.

**Zu den reservierten Keywords zählen:**

* `next`
* `last`
* `this`

**Beispiel:**

Wenn Ihr Profilschema ein Feld mit dem Namen `next` enthält, müssen Sie es in Backticks einschließen:

```
{{profile.person.`next`.name}}
```

Ohne die Backticks gibt die Validierung des Personalisierungseditors einen Fehler zurück.

>[!NOTE]
>
>Backtick-Escaping für reservierte Keywords gilt sowohl für `{{...}}` Handlebars-Pfade als auch für `{%= ... %}` PQL-Ausdrücke, da diese Keywords auf der Pfadauflösungsebene reserviert sind. Dies unterscheidet sich von den Feldnamen mit Bindestrich, bei denen Backtick-Escaping nur innerhalb von PQL-Ausdrücken unterstützt wird. Siehe [Schlüssel für getrennte Attribute](#hyphenated-keys).

## PQL-Syntaxregeln für spezielle Attributschlüssel {#pql-special-keys}

Neben reservierten Keywords erfordern zwei zusätzliche Fälle Backtick-Escaping in PQL-Ausdrücken.

### Getrennte Attributschlüssel {#hyphenated-keys}

Wenn Ihr XDM-Schema Feldnamen mit Bindestrichen (z. B. `my-field`, `event-type`) oder Namen enthält, die mit Zahlen beginnen oder Zahlen enthalten, schließen Sie den Schlüssel in Backticks in PQL-Ausdrücken ein:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>Backtick-Escaping wird nur innerhalb von PQL-Ausdrücken (`{%= ... %}`) unterstützt. Sie wird in der Handlebars-Interpolation (`{{...}}`) nicht unterstützt. Trennzeichen können jedoch direkt in `{{...}}` referenziert werden (z. B. `{{profile.my-custom-field}}`); nur die Backtick-Syntax schlägt dort fehl.

Ohne Backticks in einem PQL-Ausdruck wird der Bindestrich als Subtraktionsoperator interpretiert und verursacht einen PQL-Syntaxfehler.

### Numerische Ereignis-IDs in Kontextattributen {#numeric-event-ids}

Wenn Sie auf Kontextereignisattribute verweisen, bei denen die Ereignis-ID eine Zahl ist (z. B. `1697323153`), schließen Sie sie in Backticks ein. Dies gilt auch für Funktionen wie `formatDate()`:

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## Typzwang {#type-coercion}

PQL ist stark typisiert. Beim Vergleichen oder Übergeben von Werten müssen beide Seiten vom gleichen Typ sein. Häufige Fälle:

| Szenario | Lösung |
|----------|----------|
| Numerischer Wert, der als Zeichenfolge gespeichert wird | `stringToNumber()` vor Arithmetik oder Vergleich verwenden: `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| Ganze Zahl gespeichert als String | `string_to_integer()` oder `stringToNumber()` vor der Arithmetik verwenden |
| Boolescher Wert, als Zeichenfolge gespeichert | `toBool()` zum Konvertieren verwenden: `{%= toBool(profile.consents.email.val) = true %}` |

## Verfügbare Namespaces {#namespaces}

* **Profil**

  Dieser Namespace erlaubt die Referenzierung aller im Profilschema definierten Attribute, die unter [Dokumentation zum Datenmodell (XDM) von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"} beschrieben werden.

  Die Attribute müssen im Schema definiert sein, damit sie in einem Personalisierungsblock in [!DNL Journey Optimizer] referenziert werden können.

  Weitere Informationen zur Verwendung von Profilattributen in Bedingungen finden Sie in [diesem Abschnitt](functions/helpers.md#if-function).

  +++Beispielverweise

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **Zielgruppe**

  Weitere Informationen zum Segmentierungs-Service finden Sie in [dieser Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de){target="_blank"}.

* **Angebote**

  In diesem Namespace können Sie bestehende Entscheidungen referenzieren.

  Um ein Angebot zu referenzieren, müssen Sie einen Pfad mit den verschiedenen Informationen angeben, die das Angebot definieren. Dieser Pfad weist die folgende Struktur auf:

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  Hier gilt:

   * `offers` identifiziert den Pfadausdruck, der zum Angebots-Namespace gehört.
   * `Type` bestimmt den Typ der Angebotsdarstellung. Zu den möglichen Werten gehören `image`, `html` und `text`
   * `Placement Id` und `Activity Id` sind Platzierungs- und Aktivitätskennungen.
   * `Attributes` sind angebotsspezifische Attribute, die vom Angebotstyp abhängen. Beispiel: `deliveryUrl` für Bilder

  Weitere Informationen zur Entscheidungs-API und zu Angebotsdarstellungen finden Sie auf [dieser Seite](../offers/api-reference/offer-delivery-api/decisioning-api.md).

  Ein Validierungsmechanismus, der auf [dieser Seite](../personalization/personalization-build-expressions.md) beschrieben wird, validiert alle Verweise anhand des Angebotsschemas.

  +++Beispielverweise

   * Speicherort, an dem das Bild gehostet wird:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * Ziel-URL beim Klicken auf das Bild:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * Text-Inhalt des Angebots aus der Entscheidungs-Engine:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * HTML-Inhalt des Angebots aus der Entscheidungs-Engine:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## Helper {#helpers-all}

Ein Handlebars-Helper ist eine einfache Kennung, auf die Parameter folgen können. Jeder Parameter ist ein Handlebars-Ausdruck. Helper können in jedem Kontext einer Vorlage aufgerufen werden.

Diese Block-Helper werden durch ein `#` am Anfang des Helper-Namens gekennzeichnet und erfordern einen passenden schließenden `/` am Ende des Namens.

Blöcke sind Ausdrücke mit einer Blockeröffnung (`{{# }}`) und schließendem (`{{/}}`).

Weitere Informationen zu Hilfsfunktionen finden Sie [diesem Abschnitt](functions/helpers.md).

## Literaltypen {#literal-types}

[!DNL Adobe Journey Optimizer] unterstützt die folgenden Literaltypen:

| Literal | Definition |
| ------- | ---------- |
| Zeichenfolge | Ein Datentyp, der aus Zeichen besteht, die von doppelten Anführungszeichen umgeben sind. <br>Beispiele: `"prospect"`, `"jobs"`, `"articles"` |
| Boolesch | Ein Datentyp, der entweder „true“ oder „false“ ist. |
| Ganzzahl | Ein Datentyp, der eine ganze Zahl darstellt. Sie kann positiv, negativ oder null sein. <br>Beispiele: `-201`, `0`, `412` |
| Array | Ein Datentyp, der aus einer Gruppe anderer Literalwerte besteht. Zur Gruppierung werden eckige Klammern und Kommas verwendet, um zwischen verschiedenen Werten zu trennen. <br> **Hinweis:** Sie können nicht direkt auf die Eigenschaften von Elementen in einem Array zugreifen. <br> Beispiele: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>Die Variable **xEvent** ist in Personalisierungsausdrücken nicht verfügbar. Die Verwendung von xEvent führt zu Überprüfungsfehlern.

## Best Practices {#best-practices}

Überprüfen Sie diese Syntaxregeln, bevor Sie Personalisierungsausdrücke erstellen. Die meisten Laufzeitfehler rühren aus der Vermischung von Handlebars- und PQL-Kontexten her.

**Verwenden Sie die richtige Syntax für bedingte Blöcke**

Verwenden Sie immer `{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`. Die Syntax `{% if %}` / `{% elseif %}` / `{% endif %}` wird nicht unterstützt.

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**Rufen Sie keine PQL-Funktionen in `{{...}}` Handlebars-Blöcken auf**

`{{...}}` löst nur Handlebars-Variablen und -Helfer auf - es wird PQL nicht ausgewertet. Das Umschließen einer PQL-Funktion wie `upperCase()` in `{{...}}` verursacht den Fehler „Helper konnte nicht gefunden werden“. Verwenden Sie stattdessen `{%= ... %}`:

| Inkorrekt | Korrekt |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**Verwenden eines Alias für eine benannte Schleife beim Kombinieren von `{{#each}}` mit`{%#if%}`**

`this.field` wird vom Handlebars-Renderer aufgelöst, nicht jedoch vom PQL-Auswerter innerhalb einer `{%#if%}`. Definieren Sie einen benannten Alias mit `as |item|`, damit beide Kontexte das Feld auflösen können:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**Weisen Sie einer Variablen vor der Schleife Ergebnisse der PQL-Funktion zu**

PQL-UDFs wie `topN` können nicht direkt in `{{#each}}` aufgerufen werden. Bewerten Sie sie zunächst mit `{% let %}` und durchlaufen Sie dann das Ergebnis:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**Verwenden Sie `{% let %}`, um zu vermeiden, dass Funktionsaufrufe wiederholt werden**

Wenn ein berechneter Wert mehrmals benötigt wird, speichern Sie ihn in einer Variablen. Dies verbessert die Lesbarkeit und verhindert redundante Auswertungen:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**Verwenden Sie die richtige Argumentreihenfolge für`dateDiff`**

`dateDiff(start, end)` nimmt das frühere Datum zuerst. Um die bis zu einem zukünftigen Datum verbleibenden Tage zu berechnen, übergeben Sie das aktuelle Datum als erstes Argument:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**Verwenden von `=` für Gleichheitsvergleiche in PQL, nicht`==`**

PQL verwendet für Gleichheit einen einzelnen `=`. Die Verwendung von `==` führt zu einem Syntaxfehler.

**Backticks für Feldnamen mit Bindestrichen verwenden - nur in PQL-Ausdrücken**

Wenn ein XDM-Schemafeldname einen Bindestrich enthält (z. B. `order-total`), schließen Sie ihn in Backticks ein, um zu verhindern, dass der Bindestrich als Subtraktionsoperator geparst wird. Dies wird nur innerhalb `{%= ... %}` PQL-Ausdrücke unterstützt, nicht in `{{...}}` Handlebars-Blöcken:

```sql
{%= profile.events.`order-total` > 100 %}
```

Gebrauchsfertige Ausdrücke, die Sie direkt in Ihren Inhalt kopieren können, finden Sie unter [Personalization-Rezepte](personalization-recipes.md).
