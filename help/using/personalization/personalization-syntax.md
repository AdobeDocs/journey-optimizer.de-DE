---
solution: Journey Optimizer
product: journey optimizer
title: Personalisierungssyntax
description: Erfahren Sie, wie Sie die Personalisierungssyntax verwenden.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor, Syntax, Personalisierung
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: ht
source-wordcount: '730'
ht-degree: 100%

---

# Personalisierungssyntax {#personalization-syntax}

Die Personalisierung in [!DNL Journey Optimizer] basiert auf der Vorlagensyntax „Handlebars“.
Eine vollständige Beschreibung der Handlebars-Syntax finden Sie in der [Dokumentation zu HandlebarsJS](https://handlebarsjs.com/).

Sie verwendet eine Vorlage und ein Eingabeobjekt, um HTML oder andere Textformate zu generieren. Handlebars-Vorlagen sehen wie normaler Text mit eingebetteten Handlebars-Ausdrücken aus.

Beispiel für einen einfachen Ausdruck:

`{{profile.person.name}}`

Hier gilt:

* `profile` ist ein Namespace.
* `person.name` ist ein Token, das aus Attributen besteht. Die Attributstruktur wird in einem XDM-Schema von Adobe Experience Platform definiert. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}.

## Allgemeine Syntaxregeln {#general-rules}

Kennungen können beliebige Unicode-Zeichen sein, mit Ausnahme folgender Einschränkungen:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

Die Syntax unterscheidet zwischen Groß- und Kleinschreibung.

Die Wörter **true**, **false**, **null** und **undefined** sind nur im ersten Teil eines Pfadausdrucks zulässig.

In Handlebars werden den von {{expression}} zurückgegebenen Werten **HTML-Escape-Zeichen hinzugefügt**. Wenn der Ausdruck „`&`“ enthält, wird die Ausgabe mit HTML-Escape-Zeichen als „`&amp;`“ generiert. Wenn Sie eine Rückgabe der Werte ohne Escape-Zeichen wünschen, verwenden Sie dreifache geschweifte Klammern („Triple-Stash“).

Bezüglich der Argumente für literale Funktionen unterstützt der Sprach-Parser für Vorlagen keinen einfachen umgekehrten Schrägstrich (`\`), der nicht escaped ist. Dieses Zeichen muss mit einem zusätzlichen umgekehrten Schrägstrich (`\`) escaped werden. Beispiel:

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Profil

Dieser Namespace erlaubt die Referenzierung aller im Profilschema definierten Attribute, die unter [Dokumentation zum Datenmodell (XDM) von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"} beschrieben werden.

Die Attribute müssen im Schema definiert sein, damit sie in einem Personalisierungsblock in [!DNL Journey Optimizer] referenziert werden können.

>[!NOTE]
>
>In [diesem Abschnitt](functions/helpers.md#if-function) erfahren Sie, wie Sie Profilattribute in Bedingungen verwenden können.

**Beispielverweise:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Segmente{#perso-segments}

In [diesem Abschnitt](functions/helpers.md#if-function) erfahren Sie, wie Sie Profilattribute in Bedingungen verwenden können.

>[!NOTE]
>Weitere Informationen zur Segmentierung und zum Segmentierungs-Service finden Sie in [diesem Abschnitt](../segment/about-segments.md).

## Angebote {#offers-syntax}

In diesem Namespace können Sie bestehende Entscheidungen referenzieren.
Um ein Angebot zu referenzieren, müssen Sie einen Pfad mit den verschiedenen Informationen angeben, die das Angebot definieren.

Dieser Pfad weist die folgende Struktur auf:

`offers.Type.[Placement Id].[Activity Id].Attribute`

Hier gilt:

* `offers` identifiziert den Pfadausdruck, der zum Angebots-Namespace gehört.
* `Type` bestimmt den Typ der Angebotsdarstellung. Zu den möglichen Werten gehören `image`, `html` und `text`
* `Placement Id` und `Activity Id` sind Platzierungs- und Aktivitätskennungen.
* `Attributes` sind angebotsspezifische Attribute, die vom Angebotstyp abhängen. Beispiel: `deliveryUrl` für Bilder

Weitere Informationen zur Entscheidungs-API und zur Angebotsdarstellung finden Sie auf [dieser Seite](../offers/api-reference/offer-delivery-api/decisioning-api.md).

Ein Validierungsmechanismus, der [auf dieser Seite](personalization-validation.md) beschrieben wird, validiert alle Verweise anhand des Angebotsschemas.

**Beispielverweise:**

* Speicherort, an dem das Bild gehostet wird:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* Ziel-URL beim Klicken auf das Bild:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Text-Inhalt des Angebots aus der Entscheidungs-Engine:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML-Inhalt des Angebots aus der Entscheidungs-Engine:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Helper{#helpers-all}

Ein Handlebars-Helper ist eine einfache Kennung, auf die Parameter folgen können.
Jeder Parameter ist ein Handlebars-Ausdruck. Helper können in jedem Kontext einer Vorlage aufgerufen werden.

Diese Block-Helper werden durch ein # am Anfang des Helper-Namens gekennzeichnet und erfordern einen passenden schließenden / am Ende des Namens.
Blöcke sind Ausdrücke mit einer Blockeröffnung ({{# }}) and closing ({{/}}).


>[!NOTE]
>
>Hilfsfunktionen sind in [diesem Abschnitt](functions/helpers.md) ausführlich beschrieben.

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

## URL-Personalisierung{#perso-urls}

Personalisierte URLs führen Empfänger je nach den Profilattributen zu bestimmten Seiten einer Website oder zu einer personalisierten Microsite. In Adobe Journey Optimizer können Sie jetzt zu URLs im Nachrichteninhalt eine Personalisierung hinzufügen. Die URL-Personalisierung kann auf Text und Bilder angewendet werden und Profil- oder kontextuelle Daten verwenden.

Mit Journey Optimizer können Sie eine oder mehrere URLs in Ihrer Nachricht personalisieren, indem Sie zu ihnen Personalisierungsfelder hinzufügen. Gehen Sie wie folgt vor, um eine URL zu personalisieren:

1. Erstellen Sie einen Link in Ihrem Nachrichteninhalt. [Weitere Informationen](../email/message-tracking.md#insert-links)
1. Wählen Sie über das Personalisierungssymbol die Attribute aus. Das Personalisierungssymbol ist nur für folgende Arten von Links verfügbar: **Externer Link**, **Abmelde-Link** und **Opt-out**.

   ![](assets/perso-url.png)

>[!NOTE]
>
>Wenn Sie im Ausdruckseditor eine personalisierte URL bearbeiten, werden Hilfsfunktionen und die Segmentzugehörigkeit aus Sicherheitsgründen deaktiviert.

**Beispiele für personalisierte URLs**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Leerzeichen werden in den Personalisierungs-Token, die in URLs verwendet werden, nicht unterstützt.
