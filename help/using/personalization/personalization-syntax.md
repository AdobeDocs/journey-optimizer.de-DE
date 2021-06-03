---
title: Personalisierungssyntax
description: Erfahren Sie, wie Sie die Personalisierungssyntax verwenden
source-git-commit: 5b7f3f58e7376b45993b6a2edc6e96f824fa2f44
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 56%

---


# Personalisierungssyntax {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

Die Personalisierung in [!DNL Journey Optimizer] basiert auf der Vorlagensyntax namens &quot;Handlebars&quot;.
Eine vollständige Beschreibung der Handlebars-Syntax finden Sie in der [HandlebarsJS-Dokumentation](https://handlebarsjs.com/).

Sie verwendet eine Vorlage und ein Eingabeobjekt, um HTML oder andere Textformate zu generieren. Handlebars-Vorlagen sehen wie normaler Text mit eingebetteten Handlebars-Ausdrücken aus.

Beispiel für einen einfachen Ausdruck:

```
{{profile.person.name}}
```

where:

* **profileis** ist ein Namespace.
* **person.name** ist ein Token, das aus Attributen besteht. Die Attributstruktur wird in einem XDM-Schema von Adobe Experience Platform definiert. [Weitere Infos](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de).

## Allgemeine Syntaxregeln

Kennungen können beliebige Unicode-Zeichen sein, mit Ausnahme folgender Einschränkungen:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

Die Syntax unterscheidet zwischen Groß- und Kleinschreibung.

Die Wörter **true**, **false**, **null** und **undefined** sind nur im ersten Teil eines Pfadausdrucks zulässig.

In Handlebars werden den von {{expression}} zurückgegebenen Werten **HTML-Escape-Zeichen** hinzugefügt. Wenn der Ausdruck `&` enthält, wird die zurückgegebene HTML-maskierte Ausgabe als `&amp;` generiert. Wenn Sie eine Rückgabe der Werte ohne Escape-Zeichen wünschen, verwenden Sie den „Triple-Stash“.

## Profil

Dieser Namespace erlaubt die Referenzierung aller im Profilschema definierten Attribute, die unter [Dokumentation zum Datenmodell (XDM) von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) beschrieben werden.

Die Attribute müssen im Schema definiert werden, bevor sie in einem Gestaltungsbaustein [!DNL Journey Optimizer] referenziert werden.

>[!NOTE]
>
>Erfahren Sie in [diesem Abschnitt](functions/helpers.md#if-function), wie Sie Profilattribute in Bedingungen nutzen können.

**Beispielverweise:**

```
{{profile.person.name.fullName}}
{{profile.person.name.firstName}}
{{profile.person.gender}}
{{profile.personalEmail.address}}
{{profile.mobilePhone.number}}
{{profile.homeAddress.city}}
{{profile.faxPhone.number}}
```

## Segmente{#perso-segments}

Erfahren Sie in [diesem Abschnitt](functions/helpers.md#if-function), wie Sie Profilattribute in Bedingungen nutzen können.

>[!NOTE]
>Weitere Informationen zu Segmentierungs- und Segmentierungsdienst finden Sie in [diesem Abschnitt](../segment/about-segments.md).


## Angebote

In diesem Namespace können Sie bestehende Angebote referenzieren.
Um ein Angebot zu referenzieren, müssen Sie einen Pfad mit den verschiedenen Informationen angeben, die das Angebot definieren.

Dieser Pfad weist die folgende Struktur auf:

```
offers.Type.[Placement Id].[Activity Id].Attribute
```

wobei:

* `offers` identifiziert den Pfadausdruck, der zum Angebots-Namespace gehört
* `Type`  bestimmt den Typ der Angebotsdarstellung. Mögliche Werte sind: `image`, `html` und `text`
* `Placement Id` und  `Activity Id` sind Platzierungs- und Aktivitätskennungen
* `Attributes` sind angebotspezifische Attribute, die vom Angebotstyp abhängen. Beispiel: `deliveryUrl` für Bilder.

Weitere Informationen zur Decisions-API und zur Angebotsdarstellung finden Sie auf [dieser Seite](../../using/offers/api-reference/decisions-api/deliver-offers.md)

Alle Verweise werden mit einem in [dieser Seite](personalization-validation.md) beschriebenen Validierungsmechanismus für das Angebotsschema validiert.

**Beispielverweise:**

* Speicherort, an dem das Bild gehostet wird:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* Target-URL beim Klicken auf das Bild:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Text-Content des Angebots aus der Decisioning-Engine:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML-Content des Angebots aus der Decisioning-Engine:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Helpers{#helpers-all}

Ein Handlebars-Helper ist eine einfache Kennung, auf die Parameter folgen können.
Jeder Parameter ist ein Handlebars-Ausdruck. Helper können in jedem Kontext einer Vorlage aufgerufen werden.

Diese Block-Helper werden durch ein # am Anfang des Helper-Namens gekennzeichnet und erfordern einen passenden Abschluss mit /, desselben Namens.
Blöcke sind Ausdrücke mit einer Blockeröffnung ({{# }}) und schließendem ({{/}}).


>[!NOTE]
>
>Hilfsfunktionen werden in [diesem Abschnitt](functions/helpers.md) beschrieben.


## Literaltypen

[!DNL Adobe Journey Optimizer] unterstützt die folgenden Literaltypen:

| Literal | Definition |
| ------- | ---------- |
| Zeichenfolge | Ein Datentyp, der aus Zeichen besteht, die von doppelten Anführungszeichen umgeben sind. <br>Beispiele: `"prospect"`, `"jobs"`, `"articles"` |
| Boolesch | Ein Datentyp, der entweder &quot;true&quot;oder &quot;false&quot;ist. |
| Ganzzahl | Ein Datentyp, der eine ganze Zahl darstellt. Sie kann positiv, negativ oder null sein. <br>Beispiele: `-201`, `0`, `412` |
| Array | Ein Datentyp, der als Gruppe anderer Literalwerte besteht. Zur Gruppierung werden eckige Klammern und Kommas verwendet, um zwischen verschiedenen Werten zu trennen. <br> **Hinweis:** Sie können nicht direkt auf die Eigenschaften von Elementen in einem Array zugreifen. <br> Beispiele: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>Die Variable **xEvent** ist in Personalisierungsausdrücken nicht verfügbar. Die Verwendung von xEvent führt zu Überprüfungsfehlern.
