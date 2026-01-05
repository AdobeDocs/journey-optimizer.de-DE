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
source-git-commit: 9c013883e1bcdbf7dffffa599a910178def80e39
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 88%

---

# Personalisierungssyntax {#personalization-syntax}

Die Personalisierung in [!DNL Journey Optimizer] basiert auf der Vorlagensyntax „Handlebars“. Eine vollständige Beschreibung der Handlebars-Syntax finden Sie in der [Dokumentation zu HandlebarsJS](https://handlebarsjs.com/).

Sie verwendet eine Vorlage und ein Eingabeobjekt, um HTML oder andere Textformate zu generieren. Handlebars-Vorlagen sehen wie normaler Text mit eingebetteten Handlebars-Ausdrücken aus.

Beispiel für einen einfachen Ausdruck:

`{{profile.person.name}}`

Hier gilt:

* `profile` ist ein Namespace.
* `person.name` ist ein Token, das aus Attributen besteht. Die Attributstruktur wird in einem XDM-Schema von Adobe Experience Platform definiert. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}.

## Allgemeine Syntaxregeln {#general-rules}

* Kennungen können beliebige Unicode-Zeichen sein, mit Ausnahme folgender Einschränkungen:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* Die Syntax unterscheidet zwischen Groß- und Kleinschreibung.

* Die Wörter **true**, **false**, **null** und **undefined** sind nur im ersten Teil eines Pfadausdrucks zulässig.

* In Handlebars werden den von {{expression}} zurückgegebenen Werten **HTML-Escape-Zeichen hinzugefügt**. Wenn der Ausdruck „`&`“ enthält, wird die Ausgabe mit HTML-Escape-Zeichen als „`&amp;`“ generiert. Wenn Sie wünschen, dass Handlebars einen Wert nicht escapen, verwenden Sie drei geschweifte Klammern.

  Angenommen, der Wert des Felds `profile.person.name` lautet „Mark &amp; Mary“. Die Syntax `{{profile.person.name}}` zeigt `Mark &amp; Mary` an, während `{{{profile.person.name}}}` `Mark & Mary` anzeigt.

* Bezüglich der Argumente für literale Funktionen unterstützt der Sprach-Parser für Vorlagen keinen einfachen umgekehrten Schrägstrich (`\`), der nicht escaped ist. Dieses Zeichen muss mit einem zusätzlichen umgekehrten Schrägstrich (`\`) escaped werden. Beispiel:

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Reservierte Schlüsselwörter {#reserved-keywords}

Bestimmte Schlüsselwörter sind in Profile Query Language (PQL) reserviert und können nicht direkt als Feld- oder Variablennamen in Personalisierungsausdrücken verwendet werden. Wenn Ihr XDM-Schema Felder mit Namen enthält, die reservierten Schlüsselwörtern entsprechen, müssen Sie diese mit Backticks (`` ` ``) maskieren, um in Ihren Ausdrücken darauf zu verweisen.

**Reservierte Schlüsselwörter beinhalten:**

* `next`
* `last`
* `this`

**Beispiel:**

Wenn Ihr Profilschema ein Feld mit dem Namen `next` enthält, müssen Sie es in Backticks einschließen:

```
{{profile.person.`next`.name}}
```

Ohne die Backticks schlägt die Validierung des Personalisierungseditors mit einem Fehler fehl.

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

## Helper{#helpers-all}

Ein Handlebars-Helper ist eine einfache Kennung, auf die Parameter folgen können. Jeder Parameter ist ein Handlebars-Ausdruck. Helper können in jedem Kontext einer Vorlage aufgerufen werden.

Diese Block-Helper werden durch ein `#` am Anfang des Helper-Namens gekennzeichnet und erfordern einen passenden schließenden `/` am Ende des Namens.

Blöcke sind Ausdrücke mit einer Blockeröffnung (`{{# }}`) und schließendem (`{{/}}`).

Weitere Informationen zu Helper-Funktionen finden Sie in [diesem Abschnitt](functions/helpers.md).

## Literaltypen {#literal-types}

[!DNL Adobe Journey Optimizer] unterstützt die folgenden Literaltypen:

| Literal | Definition |
| ------- | ---------- |
| String | Ein Datentyp, der aus Zeichen besteht, die von doppelten Anführungszeichen umgeben sind. <br>Beispiele: `"prospect"`, `"jobs"`, `"articles"` |
| Boolesch | Ein Datentyp, der entweder „true“ oder „false“ ist. |
| Ganzzahl | Ein Datentyp, der eine ganze Zahl darstellt. Sie kann positiv, negativ oder null sein. <br>Beispiele: `-201`, `0`, `412` |
| Array | Ein Datentyp, der aus einer Gruppe anderer Literalwerte besteht. Zur Gruppierung werden eckige Klammern und Kommas verwendet, um zwischen verschiedenen Werten zu trennen. <br> **Hinweis:** Sie können nicht direkt auf die Eigenschaften von Elementen in einem Array zugreifen. <br> Beispiele: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>Die Variable **xEvent** ist in Personalisierungsausdrücken nicht verfügbar. Die Verwendung von xEvent führt zu Überprüfungsfehlern.
