---
title: Personalisierungssyntax
description: Erfahren Sie, wie Sie die Personalisierungssyntax verwenden
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: fe39570b-cbd2-4b24-af10-e12990a9a885
source-git-commit: 1cf3475d7b2b990db4b2217bb03a47b76692142c
workflow-type: tm+mt
source-wordcount: '648'
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
* `person.name` ist ein Token, das aus Attributen besteht. Die Attributstruktur wird in einem XDM-Schema von Adobe Experience Platform definiert. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target=&quot;_blank&quot;}.

## Allgemeine Syntaxregeln

Kennungen können beliebige Unicode-Zeichen sein, mit Ausnahme folgender Einschränkungen:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

Die Syntax unterscheidet zwischen Groß- und Kleinschreibung.

Die Wörter **true**, **false**, **null** und **undefined** sind nur im ersten Teil eines Pfadausdrucks zulässig.

In Handlebars werden den von {{expression}} zurückgegebenen Werten **HTML-Escape-Zeichen** hinzugefügt. Wenn der Ausdruck „`&`“ enthält, wird die Ausgabe mit HTML-Escape-Zeichen als „`&amp;`“ generiert. Wenn Sie eine Rückgabe der Werte ohne Escape-Zeichen wünschen, verwenden Sie den „Triple-Stash“.

## Profil

Dieser Namespace ermöglicht die Referenzierung aller im Profilschema definierten Attribute, die unter [Dokumentation zum Datenmodell (XDM) von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;} beschrieben werden.

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

## Angebote

In diesem Namespace können Sie bestehende Entscheidungen referenzieren.
Um ein Angebot zu referenzieren, müssen Sie einen Pfad mit den verschiedenen Informationen angeben, die das Angebot definieren.

Dieser Pfad weist die folgende Struktur auf:

`offers.Type.[Placement Id].[Activity Id].Attribute`

Hier gilt:

* `offers` identifiziert den Pfadausdruck, der zum Angebots-Namespace gehört.
* `Type` bestimmt den Typ der Angebotsdarstellung. Zu den möglichen Werten gehören `image`, `html` und `text`
* `Placement Id` und `Activity Id` sind Platzierungs- und Aktivitätskennungen.
* `Attributes` sind angebotsspezifische Attribute, die vom Angebotstyp abhängen. Beispiel: `deliveryUrl` für Bilder

Weitere Informationen zur Entscheidungs-API und zur Angebotsdarstellung finden Sie auf [dieser Seite](../../using/offers/api-reference/decisions-api/deliver-offers.md).

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
Blöcke sind Ausdrücke mit einer Blockeröffnung ({{# }}) und schließendem ({{/}}).


>[!NOTE]
>
>Hilfsfunktionen sind in [diesem Abschnitt](functions/helpers.md) ausführlich beschrieben.

## Literaltypen

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

Mit Journey Orchestration können Sie eine oder mehrere URLs in Ihrer Nachricht personalisieren, indem Sie ihnen Personalisierungsfelder hinzufügen. Gehen Sie dazu folgendermaßen vor:

* Erstellen Sie einen Link im Inhalt Ihrer E-Mail oder Push-Benachrichtigung. Weitere Informationen zur Link-Erstellung finden Sie auf [dieser Seite](../message-tracking.md#insert-links).
* Klicken Sie auf das Personalisierungssymbol. Dieses Symbol ist für diese spezifischen Link-Typen verfügbar: **Externer Link**, **Abmelde-Link** und **Opt-out-Link**.

![](assets/perso-url.png)

>[!NOTE]
>
>Wenn Sie im Ausdruckseditor eine personalisierte URL bearbeiten, sind Helper-Funktionen und die Segmentzugehörigkeit aus Sicherheitsgründen deaktiviert.

** Beispiele für personalisierte URLs **

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

