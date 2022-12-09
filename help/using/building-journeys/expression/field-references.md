---
solution: Journey Optimizer
product: journey optimizer
title: Feldverweise
description: Erfahren Sie mehr über Feldverweise in erweiterten Ausdrücken
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# Feldverweise {#field-references}

Ein Feldverweis kann an ein Ereignis oder eine Feldergruppe angehängt werden. Die einzigen aussagekräftigen Informationen sind der Name des Felds und sein Pfad.

Wenn Sie Sonderzeichen in einem Feld verwenden, müssen Sie doppelte Anführungszeichen oder einfache Anführungszeichen verwenden. Dies sind die Fälle, in denen Anführungszeichen benötigt werden:

* das Feld beginnt mit numerischen Zeichen
* das Feld beginnt mit dem Zeichen &quot;-&quot;
* das Feld enthält andere Elemente als: _a_-_z_, _A_-_Z_, _0_-_9_, _ , _-_

Wenn Ihr Feld beispielsweise _3 h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@{<event name>.<XDM path to the field>}
@{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

Im Ausdruck wird auf Ereignisfelder mit &quot;@&quot;und auf Datenquellenfelder mit &quot;#&quot;verwiesen.

Eine Syntaxfarbe wird verwendet, um Ereignisfelder (grün) optisch von Feldergruppen (blau) zu unterscheiden.

## Standardwerte für Feldverweise {#default-value}

Ein Standardwert kann mit einem Feldnamen verknüpft werden. Die Syntax lautet wie folgt:

```json
// event field
@{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>Der Feldtyp und der Standardwert müssen identisch sein. Beispiel: @{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2} ist ungültig, da der Standardwert eine Ganzzahl ist, während der erwartete Wert eine Zeichenfolge sein sollte.

Beispiele:

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @{OrderEvent.orderId}                                    -> "12345"
- @{OrderEvent.producdId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @{OrderEvent.productId}                                  -> null
 
 
// for an entity 'Profile' on datasource 'ACP' having fields person/lastName, with fetched data such as:
{
    "person": {
        "lastName":"Snow"
    },
    "emails": [
        { "email":"john.snow@winterfell.westeros" },
        { "email":"snow@thewall.westeros" }
    ]
}
 
expression examples:
- #{ACP.Profile.person.lastName}                 -> "Snow"
- #{ACP.Profile.emails.at(1).email}              -> "snow@thewall.westeros"
- #{ACP.Profile.person.age, defaultValue : -1}   -> -1 // default value, age is not a field present in the payload
- #{ACP.Profile.person.age}                      -> null
```

Sie können jede Art von Ausdruck als Standardwert hinzufügen. Die einzige Einschränkung besteht darin, dass der Ausdruck den erwarteten Datentyp zurückgeben muss. Bei Verwendung einer Funktion muss die Funktion mit () gekapselt werden.

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## Verweis auf ein Feld in Sammlungen

Die in Kollektionen definierten Elemente werden mithilfe der spezifischen Funktionen referenziert `all`, `first` und `last`. Weitere Informationen finden Sie unter [diese Seite](../expression/collection-management-functions.md).

Beispiel :

```json
@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## Verweis auf ein in einer Zuordnung definiertes Feld

### `entry` function

Um ein Element in einer Zuordnung abzurufen, verwenden wir die Eingabefunktion mit einem bestimmten Schlüssel. Sie wird beispielsweise bei der Definition des Ereignisschlüssels entsprechend dem ausgewählten Namespace verwendet. Weitere Informationen finden Sie unter [diese Seite](../../event/about-creating.md#select-the-namespace).

```json
@{MyEvent.identityMap.entry('Email').first().id}
```

In diesem Ausdruck erhalten wir den Eintrag für den Schlüssel &quot;E-Mail&quot;des Felds &quot;IdentityMap&quot;eines Ereignisses. Der Eintrag &quot;E-Mail&quot;ist eine Kollektion, aus der wir die &quot;ID&quot;im ersten Element mit &quot;first()&quot;verwenden. Weitere Informationen finden Sie unter [diese Seite](../expression/collection-management-functions.md).

### `firstEntryKey` function

Um den ersten Eintragsschlüssel einer Zuordnung abzurufen, verwenden Sie die `firstEntryKey` -Funktion.

In diesem Beispiel wird gezeigt, wie die erste E-Mail-Adresse der Abonnenten einer bestimmten Liste abgerufen wird:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

In diesem Beispiel erhält die Abonnementliste den Namen `daily-email`. E-Mail-Adressen werden als Schlüssel im `subscribers` -Karte, die mit der Abonnementlisten-Karte verknüpft ist.

### `keys` function

Um alle Schlüssel einer Zuordnung abzurufen, verwenden Sie die `keys` -Funktion.

In diesem Beispiel wird gezeigt, wie für ein bestimmtes Profil alle E-Mail-Adressen abgerufen werden, die mit den Abonnenten einer bestimmten Liste verknüpft sind:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## Parameterwerte einer Datenquelle (dynamische Datenquellenwerte)

Wenn Sie ein Feld aus einer externen Datenquelle auswählen, für das ein Parameter aufgerufen werden muss, wird rechts eine neue Registerkarte angezeigt, auf der Sie diesen Parameter angeben können. Siehe [diese Seite](../expression/expressionadvanced.md).

Wenn Sie für komplexere Anwendungsfälle die Parameter der Datenquelle in den Hauptausdruck aufnehmen möchten, können Sie deren Werte mit dem Keyword _params_. Ein Parameter kann ein beliebiger gültiger Ausdruck sein, selbst aus einer anderen Datenquelle, die auch einen anderen Parameter enthält.

>[!NOTE]
>
>Wenn Sie die Parameterwerte im Ausdruck definieren, wird die Registerkarte rechts ausgeblendet.

Verwenden Sie die folgende Syntax:

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`**: exakter Name des ersten Parameters aus der Datenquelle.
* **`<params-1-value>`**: den Wert des ersten Parameters. Es kann sich um einen beliebigen gültigen Ausdruck handeln.

Beispiel:

```json
#{Weather.main.temperature, params: {localisation: @{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @{Profile.address.city}}}}}
```
