---
solution: Journey Optimizer
product: journey optimizer
title: Feldverweise
description: Erfahren Sie mehr über Feldverweise in erweiterten Ausdrücken
feature: Journeys
role: Developer
level: Experienced
keywords: Journey, Feld, Ausdruck, Ereignis
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/G8ooc1R2PwL06V89EBs-jH8Lf43F6q5xj3I4Wl6hDHk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 53%

---

# Feldverweise {#field-references}

Ein Feldverweis kann an ein Ereignis oder eine Feldgruppe angehängt werden. Die einzigen aussagekräftigen Informationen sind der Name des Feldes und sein Pfad.

Wenn Sie in einem Feld Sonderzeichen verwenden, müssen Sie doppelte oder einfache Anführungszeichen nutzen. In den folgenden Fällen sind Anführungszeichen erforderlich:

* das Feld beginnt mit numerischen Zeichen;
* das Feld beginnt mit dem Zeichen „-“;
* das Feld enthält andere Zeichen als: _a_–_z_, _A_–_Z_, _0_–_9_, _,_-_.

Wenn Ihr Feld zum Beispiel folgendermaßen lautet: _3h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@event{<event name>.<XDM path to the field>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

Im Ausdruck wird auf Ereignisfelder mit „@“ und auf Datenquellenfelder mit „#“ verwiesen.

Es wird eine Syntaxfarbe verwendet, um die Ereignisfelder (grün) optisch von Feldgruppen (blau) zu unterscheiden.

## Standardwerte für Feldverweise {#default-value}

Ein Standardwert kann mit einem Feldnamen verknüpft werden. Es gilt folgende Syntax:

```json
// event field
@event{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>Der Feldtyp und der Standardwert müssen übereinstimmen. Beispielsweise ist `@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2}` ungültig, da der Standardwert eine Ganzzahl ist, während der erwartete Wert eine Zeichenfolge ist.

Beispiele:

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @event{OrderEvent.orderId}                                    -> "12345"
- @event{OrderEvent.productId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @event{OrderEvent.productId}                                  -> null
 
 
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

Sie können jede Art von Ausdruck als Standardwert hinzufügen. Die einzige Einschränkung besteht darin, dass der Ausdruck den erwarteten Datentyp zurückgeben muss. Bei Verwendung einer Funktion muss diese in Klammern () eingeschlossen werden.

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## Verweis auf ein Feld in Sammlungen

Auf die in Sammlungen definierten Elemente wird mit den speziellen Funktionen `all`, `first` und `last` verwiesen. Weitere Informationen dazu finden Sie auf [dieser Seite](../expression/collection-management-functions.md).

Beispiel:

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## Verweis auf ein in einer Zuordnung definiertes Feld

### `entry`-Funktion

Um ein Element in einer Zuordnung abzurufen, verwenden Sie die Eingabefunktion mit einem bestimmten Schlüssel. Sie wird beispielsweise verwendet, wenn der Schlüssel eines Ereignisses entsprechend dem ausgewählten Namespace definiert wird. Weitere Informationen finden Sie auf [dieser Seite](../../event/about-creating.md#select-the-namespace).

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

In diesem Ausdruck erhalten wir den Eintrag für den Schlüssel „Email“ des Felds „IdentityMap“ eines Ereignisses. Der Eintrag „Email“ ist eine Sammlung, aus der wir mithilfe von „first()“ die „ID“ im ersten Element übernehmen. Weitere Informationen finden Sie auf [dieser Seite](../expression/collection-management-functions.md).

### `firstEntryKey`-Funktion

Verwenden Sie die `firstEntryKey`-Funktion, um den ersten Eintragsschlüssel einer Zuordnung abzurufen.

In diesem Beispiel wird gezeigt, wie die erste E-Mail-Adresse der Abonnenten aus einer bestimmten Liste abgerufen wird:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

In diesem Beispiel erhält die Abonnement-Liste den Namen `daily-email`. E-Mail-Adressen werden als Schlüssel in der Zuordnung `subscribers` definiert, die mit der Zuordnung der Abonnement-Liste verknüpft ist.

### `keys`-Funktion

Um alle Schlüssel einer Zuordnung abzurufen, verwenden Sie die `keys`-Funktion.

In diesem Beispiel wird gezeigt, wie für ein bestimmtes Profil alle E-Mail-Adressen abgerufen werden, die mit den Abonnenten aus einer bestimmten Liste verknüpft sind:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## Parameterwerte einer Datenquelle (dynamische Werte der Datenquelle)

Wenn Sie ein Feld aus einer externen Datenquelle auswählen, für das ein Parameter aufgerufen werden muss, wird rechts eine neue Registerkarte angezeigt, auf der Sie diesen Parameter spezifizieren können. Weitere Informationen finden Sie auf [dieser Seite](../expression/expressionadvanced.md).

Bei komplexeren Anwendungsfällen können Sie, wenn Sie die Parameter der Datenquelle in den Hauptausdruck einbeziehen möchten, deren Werte mit dem Keyword _params_ definieren. Ein Parameter kann ein beliebiger gültiger Ausdruck sein und selbst aus einer anderen Datenquelle stammen, die ebenfalls einen anderen Parameter enthält.

>[!NOTE]
>
>Wenn Sie die Parameterwerte im Ausdruck definieren, wird die Registerkarte auf der rechten Seite ausgeblendet.

Verwenden Sie die folgende Syntax:

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`**: genauer Name des ersten Parameters aus der Datenquelle.
* **`<params-1-value>`**: der Wert des ersten Parameters. Dies kann ein beliebiger gültiger Ausdruck sein.

Beispiel:

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird erläutert, wie Sie in Journey-Ausdrücken auf Ereignisfelder und Datenquellenfeldgruppen verweisen können, einschließlich Standardwertsyntax, Zuordnungszugriffsfunktionen (`entry`, `firstEntryKey`, `keys`) und Inline-Datenquellenparametern, die mit dem `params`-Schlüsselwort übergeben werden.

**intents:**

* Referenzieren eines Ereignisfelds in einem Ausdruck mithilfe der `@event{eventName.fieldPath}` Syntax
* Referenzieren einer Datenquellenfeldgruppe mithilfe der `#{dataSourceName.fieldGroupName.fieldPath}`
* Weisen Sie einer Feldreferenz einen Fallback-Standardwert zu, damit Ausdrücke nicht null zurückgeben
* Abrufen eines bestimmten Eintrags aus einer Identitätszuordnung oder Abonnementzuordnung mithilfe der `entry()`
* Abrufen aller Schlüssel aus einem Zuordnungsfeld mithilfe der `keys()`
* Übergeben von Parameterwerten an eine externe Datenquelle inline mithilfe des `params`-Schlüsselworts

**Glossar:**

* **Feldreferenz**: Eine Ausdruckssyntax, die auf ein benanntes Feld innerhalb einer Ereignis-Payload oder Datenquellenfeldgruppe verweist *(produktspezifisch)*
* **defaultValue**: Ein optionaler Fallback-Ausdruck, der an einen Feldverweis angehängt wird, der zurückgegeben wird, wenn das Feld fehlt oder null *(produktspezifisch)*
* **entry(key)**: Eine Zuordnungsfunktion, die den Sammlungseintrag abruft, der mit dem angegebenen Schlüssel verknüpft ist *(produktspezifisch)*
* **firstEntryKey()**: Eine Zuordnungsfunktion, die den ersten Schlüssel eines Zuordnungsfelds zurückgibt *(produktspezifisch)*
* **keys()**: Eine Zuordnungsfunktion, die alle Schlüssel eines Zuordnungsfelds zurückgibt *(produktspezifisch)*
* **params-Schlüsselwort**: Inline-Syntax zur Angabe von Parameterwerten für externe Datenquellenfelder im Hauptausdruck *(produktspezifisch)*

**Leitplanken:**

* Feldnamen, die Sonderzeichen enthalten (beginnend mit einer Ziffer, die `-` enthält, oder Zeichen außerhalb von `a-z A-Z 0-9 _`) müssen in einfache oder doppelte Anführungszeichen gesetzt werden
* Der Ausdruck für den Standardwert muss denselben Datentyp wie das Feld zurückgeben - nicht übereinstimmende Typen sind ungültig
* Wenn das Keyword `params` verwendet wird, um Parameterwerte inline zu definieren, verschwindet die separate Parameterregisterkarte rechts neben dem Editor
* Als Standardwerte verwendete Funktionen müssen in Klammern eingeschlossen sein

**Terminologie:**

* Kanonischer Name: Feldverweise — Akronym: none — Varianten: Feldpfad, Feldausdruck
* Synonyme: `@event{...}` = „Ereignisfeldverweis“; `#{...}` = „Datenquellenfeldverweis“
* Nicht verwechseln: Ereignisfelder (mit Präfix `@`) ≠ Datenquellenfelder (mit Präfix `#`)

**FAQ:**

* **F: Wie verweise ich auf ein Feld, dessen Name mit einer Zahl beginnt?** — Umbrechen des Feldnamens in einfache oder doppelte Anführungszeichen, z. B. `#{OpenWeather.weatherData.rain.'3h'}`.
* **F: Was passiert, wenn ein referenziertes Feld in der Ereignis-Payload fehlt und kein Standardwert festgelegt ist?** — Der Ausdruck gibt `null` zurück.
* **F: Wie stelle ich einen dynamischen Standardwert mithilfe einer Funktion ein?** — Schließen Sie den Funktionsaufruf in Klammern ein, z. B. `defaultValue: (now())`.
* **F: Wie kann ich die E-Mail-Adresse abrufen, die als erster Schlüssel in einer Abonnentenzuordnung gespeichert ist?** — Verwenden Sie die Funktion `firstEntryKey()` im Feld Abonnenten-Zuordnung .
* **F: Wie übergebe ich einen Parameter an eine externe Datenquelle, ohne die rechte Registerkarte zu verwenden?** — Verwenden Sie das `params` inline: `#{DataSource.group.field, params: {paramName: value}}`.

+++
